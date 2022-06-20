---
title: Usare le API di pianificazione dei progetti con Power Automate
description: Questo articolo fornisce un flusso di esempio che utilizza le API di pianificazione del progetto.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2527375ff3f3d631f3bb3de1458abb3b8838db54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916339"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Usare le API di pianificazione dei progetti con Power Automate

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo articolo descrive un flusso di esempio che mostra come creare una pianificazione del progetto completa utilizzando Microsoft Power Automate, come creare un set di operazioni e come aggiornare un'entità. L'esempio mostra come creare un progetto, un membro del team di progetto, set di operazioni, attività di progetto e assegnazioni di risorse. Questo articolo spiega anche come aggiornare un'entità ed eseguire un set di operazioni.

Di seguito è riportato un elenco completo dei passaggi documentati nel flusso di esempio in questo articolo:

1. [Creare un trigger PowerApps](#1)
2. [Creare un progetto](#2)
3. [Inizializzare una variabile per il membro del team](#3)
4. [Creare un membro del team generico](#4)
5. [Creare un set di opzioni](#5)
6. [Creare un bucket di progetto](#6)
7. [Inizializzare una variabile per lo stato del collegamento](#7)
8. [Inizializzare una variabile per il numero di attività](#8)
9. [Inizializzare una variabile per l'ID attività di progetto](#9)
10. [Continua finché](#10)
11. [Impostare un'attività di progetto](#11)
12. [Creare un'attività di progetto](#12)
13. [Creare un'assegnazione di risorsa](#13)
14. [Diminuire una variabile](#14)
15. [Rinominare un'attività di progetto](#15)
16. [Eseguire un set di opzioni](#16)

## <a name="assumptions"></a>Presupposti

Questo articolo presuppone che tu abbia una conoscenza di base della piattaforma Dataverse, flussi cloud e API di pianificazione del progetto. Per ulteriori informazioni, vedi la sezione [Riferimenti](#references) più avanti in questo articolo.

## <a name="create-a-flow"></a>Crea un flusso

### <a name="select-an-environment"></a>Seleziona un ambiente

È possibile creare il flusso Power Automate nell'ambiente.

1. Vai a <https://flow.microsoft.com> e usa le credenziali di amministratore per accedere.
2. Nell'angolo superiore destro seleziona **Ambienti**.
3. Nell'elenco, seleziona l'ambiente in cui Dynamics 365 Project Operations è installato.

### <a name="create-a-solution"></a>Creare una soluzione

Segui questi passaggi per creare un [flusso con riconoscimento della soluzione](/power-automate/overview-solution-flows). Creando un flusso con riconoscimento della soluzione, puoi esportare più facilmente il flusso per usarlo in seguito.

1. Nel riquadro di spostamento, seleziona **Soluzioni**.
2. Nella pagina **Soluzioni**, seleziona **Nuova soluzione**.
3. Nella finestra di dialogo **Nuova soluzione**, imposta i campi obbligatori e quindi seleziona **Crea**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Passaggio 1: Creare un trigger PowerApps

1. Nella pagina **Soluzioni**, sceglie la soluzione creata, quindi seleziona **Nuovo**.
2. Nel riquadro a sinistra, seleziona **Flussi cloud** \> **Automazione** \> **Flusso cloud** \> **Immediato**.
3. Nel campo **Nome flusso** immetti **Flusso demo API di pianificazione**.
4. Nell'elenco **Scegli come attivare questo flusso** seleziona **Power Apps**. Quando crei un trigger Power Apps, la logica dipende da te in qualità di autore. In questo articolo, lascia vuoti i parametri di input a scopo di test.
5. Seleziona **Crea**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Passaggio 2: crea un progetto

Segui questi passaggi per creare un progetto di esempio.

1. Nel flusso che hai creato, seleziona **Nuovo passaggio**.

    ![Aggiunta di un nuovo passaggio.](media/newstep.png)

2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **esegui un'azione non associata**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.

    ![Selezione di un'operazione.](media/chooseactiontab.png)

3. Nel nuovo passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.

![Ridenominazinoe di un passaggio.](media/renamestep.png)

4. Rinomina il passaggio **Crea progetto**.
5. Nel campo **Nome azione**, seleziona **msdyn\_CreateProjectV1**.
6. Sotto il campo **msdyn\_subject**, seleziona **Aggiungi contenuto dinamico**.
7. Sulla scheda **Espressione** nel campo funzione, immetti **Nome progetto - utcNow()**.
8. Seleziona **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Passaggio 3: Inizializzare una variabile per il membro del team

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **inizializza variabile**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel nuovo passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **inizializza membro del team**.
5. Nel campo **Nome** immetti **TeamMemberAction**.
6. Nel campo **Tipo** seleziona **Stringa**.
7. Nel campo **Valore** immetti **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Passaggio 4: Creare un membro del team generico

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **esegui un'azione non associata**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel nuovo passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **Crea membro del team**.
5. Per il campo **Nome azione** seleziona **TeamMemberAction** nella la finestra di dialogo **Contenuto dinamico**.
6. Nel campo **Parametri di azione** immetti le seguenti informazioni sui parametri.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Di seguito è riportata una spiegazione dei parametri:

    - **\@\@odata.type** – Il nome dell'entità. Ad esempio, immetti **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – La chiave primaria dell'ID team di progetto. Il valore è un'espressione di identificatore univoco globale (GUID).   L'ID viene generato dalla scheda dell'espressione.

    - **msdyn\_project\@odata.bind** – L'ID progetto del progetto proprietario. Il valore sarà il contenuto dinamico che deriva dalla risposta del passaggio "Crea progetto". Assicurati di inserire il percorso completo e di aggiungere il contenuto dinamico tra parentesi. Le virgolette sono obbligatorie. Ad esempio, immetti **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – Nome del membro del team. Ad esempio, immetti **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Passaggio 5: Creare un set di opzioni

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **esegui un'azione non associata**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel nuovo passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **Crea set di operazioni**.
5. Nel campo **Nome azione** seleziona l'azione personalizzata **msdyn\_CreateOperationSetV1** Dataverse.
6. Nel campo **Descrizione** immetti **ScheduleAPIDemoOperationSet**.
7. Nel campo **Progetto** immetti **/msdyn\_projects(**.
8. Nella finestra di dialogo **Contenuto dinamico** seleziona **msdyn\_CreateProjectV1Response ProjectId**.
9. Nel campo **Progetto** immetti **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Passaggio 6: Creare un bucket di progetto

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **aggiungi nuova riga**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel nuovo passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **Crea bucket**.
5. Nel campo **Nome tabella**, seleziona **Bucket di progetto**.
6. Nel campo **Nome** immetti **ScheduleAPIDemoBucket1**.
7. Per il campo **Progetto** seleziona **msdyn\_CreateProjectV1Response ProjectId** nella finestra di dialogo **Contenuto dinamico**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Passaggio 7: Inizializzare una variabile per lo stato del collegamento

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **inizializza variabile**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel nuovo passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **inizializzare linkstatus**.
5. Nel campo **Nome** immetti **linkstatus**.
6. Nel campo **Tipo** seleziona **Intero**.
7. Nel campo **Valore** immettere **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Passaggio 8: Inizializzare una variabile per il numero di attività

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **inizializza variabile**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel nuovo passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **inizializzare numero di attività**.
5. Nel campo **Nome** immetti **numero di attività**.
6. Nel campo **Tipo** seleziona **Intero**.
7. Nel campo **Valore** immettere **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Passaggio 9: Inizializzare una variabile per l'ID attività di progetto

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **inizializza variabile**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel nuovo passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **inizializza ProjectTaskID**.
5. Nel campo **Nome** immetti **numero di attività**.
6. Nel campo **Tipo** seleziona **Stringa**.
7. Per il campo **Valore** immetti **guid()** nel generatore di espressioni.

## <a name="step-10-do-until"></a><a id="10"></a>Passaggio 10: Continua finché

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **continua finché**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Imposta il primo valore nell'istruzione condizionale sulla variabile **numero di attività** dalla finestra di dialogo **Contenuti dinamici**.
4. Imposta la condizione su **minore di o uguale a**.
5. Imposta il secondo valore nell'istruzione condizionale su **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Passaggio 11: Impostare un'attività di progetto

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **imposta variabile**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel nuovo passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **imposta attività di progetto**.
5. Nel campo **Nome** seleziona **msdyn\_projecttaskid**.
6. Per il campo **Valore** immetti **guid()** nel generatore di espressioni.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Passaggio 12: Creare un'attività di progetto

Segui questi passaggi per creare un'attività di progetto con un ID univoco che appartiene al progetto corrente e al bucket di progetto che hai creato.

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **esegui un'azione non associata**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **Crea attività di progetto**.
5. Nel campo **Nome azione**, seleziona **msdyn\_PssCreateV1**.
6. Nel campo **Entità** immetti le seguenti informazioni sui parametri.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Di seguito è riportata una spiegazione dei parametri:

    - **\@\@odata.type** – Il nome dell'entità. Ad esempio, immetti **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – ID univoco dell'attività. Il valore deve essere impostato su una variabile dinamica da **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – L'ID progetto del progetto proprietario. Il valore sarà il contenuto dinamico che deriva dalla risposta del passaggio "Crea progetto". Assicurati di inserire il percorso completo e di aggiungere il contenuto dinamico tra parentesi. Le virgolette sono obbligatorie. Ad esempio, immetti **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – Qualsiasi nome di attività.
    - **msdyn\_projectbucket\@odata.bind** – Il bucket di progetto che contiene le attività. Il valore sarà il contenuto dinamico che deriva dalla risposta del passaggio "Crea bucket". Assicurati di inserire il percorso completo e di aggiungere il contenuto dinamico tra parentesi. Le virgolette sono obbligatorie. Ad esempio, immetti **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Contenuto dinamico per la data di inizio. Ad esempio, domani sarà rappresentato come **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Data di inizio pianificata. Ad esempio, domani sarà rappresentato come **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – La data di fine pianificata. Seleziona una data futura. Ad esempio, specifica **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Stato del collegamento. Ad esempio, immetti **"192350000"**.

7. Per il campo **OperationSetId** seleziona **msdyn\_CreateOperationSetV1Response** nella finestra di dialogo **Contenuto dinamico**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Passaggio 13: Creare un'assegnazione di risorsa

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **esegui un'azione non associata**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **Crea assegnazione**.
5. Nel campo **Nome azione**, seleziona **msdyn\_PssCreateV1**.
6. Nel campo **Entità** immetti le seguenti informazioni sui parametri.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Per il campo **OperationSetId** seleziona **msdyn\_CreateOperationSetV1Response** nella finestra di dialogo **Contenuto dinamico**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Passaggio 14: Diminuire una variabile

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **diminuire variabile**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel campo **Nome** seleziona **numero di attività**.
4. Nel campo **Valore** immettere **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Passaggio 15: Rinominare un'attività di progetto

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **esegui un'azione non associata**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **Rinomina attività di progetto**.
5. Nel campo **Nome azione**, seleziona **msdyn\_PssUpdateV1**.
6. Nel campo **Entità** immetti le seguenti informazioni sui parametri.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Per il campo **OperationSetId** seleziona **msdyn\_CreateOperationSetV1Response** nella finestra di dialogo **Contenuto dinamico**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Passaggio 16: Eseguire un set di opzioni

1. Nel flusso, seleziona **Nuovo passaggio**.
2. Nella finestra di dialogo **Scegli un'operazione**, nel campo di ricerca, immetti **esegui un'azione non associata**. Poi, sulla scheda **Azioni** seleziona l'operazione nell'elenco dei risultati.
3. Nel passaggio seleziona i puntini di sospensione (**...**), e quindi **Rinomina**.
4. Rinomina il passaggio **Esegui set di operazioni**.
5. Nel campo **Nome azione**, seleziona **msdyn\_ExecuteOperationSetV1**.
6. Per il campo **OperationSetId** seleziona **msdyn\_CreateOperationSetV1Response OperationSetId** nella finestra di dialogo **Contenuto dinamico**.

## <a name="references"></a>Riferimenti

- [Panoramica su come integrare i flussi con Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione](schedule-api-preview.md)
- [Panoramica dei flussi cloud - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Panoramica dei flussi con riconoscimento della soluzione - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
