---
title: Crea un nuovo progetto
description: In questo argomento vengono fornite informazioni su come creare un nuovo progetto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee576561e9d360c198a57f5885c27aa782267fd1
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685061"
---
# <a name="create-a-new-project"></a>Crea un nuovo progetto

[!include [banner](../includes/banner.md)]

Completa i passaggi seguenti per creare un nuovo progetto.

1. Nella pagina **Gestione dei progetti**, seleziona **Nuovo progetto**, quindi immetti i valori seguenti:

    - **Tipo di progetto:** tempo e materiale
    - **Nome progetto:** fase di aggiornamento XYZ 2
    - **Gruppo di progetto:** TM\_WIP
    - **ID contratto di progetto:** 00000002

2. Seleziona **Crea progetto**.

## <a name="assign-a-resource-to-a-project"></a>Assegnare una risorsa a un progetto

1. Nella pagina **Lavoratori** pagina, nell'elenco **Lavoratori**, seleziona il record per il lavoratore per cui hai impostato in precedenza le competenze e apri il record del lavoratore.
2. Nel riquadro azioni, nella scheda **Progetto**, nel gruppo **Imposta**, seleziona **Assegna progetti**.
3. Nella pagina **Assegnazioni di progetti di convalida delle risorse**, nella scheda **Progetti**, nel campo **Aggiungi il progetto ai progetti selezionati**, filtra nel progetto **Fase di aggiornamento XYZ 2**.
4. Nel riquadro **Progetti rimanenti**, seleziona un progetto, quindi seleziona il pulsante freccia per aggiungerlo al riquadro **Progetti selezionati**.

Puoi inoltre assegnare categorie a una risorsa in base alle tue esigenze. Il tipo di categoria è **Costo** o **Ricavi**. Il tipo di categoria è determinato dalla tua organizzazione. Se nessuna categoria è assegnata a una risorsa, Finance cerca la categoria predefinita sui prezzi orari per costi e ricavi.

## <a name="set-up-project-resource-and-role-characteristics"></a>Configurare le caratteristiche di ruolo e risorsa del progetto

Un project manager può utilizzare la funzionalità di assegnazione delle risorse del progetto per creare i ruoli richiesti per il progetto. I ruoli possono essere utilizzati se le risorse confermate sono ancora sconosciute quando le risorse vengono prenotate. I ruoli possono essere riservati temporaneamente come risorse pianificate, in modo da poter continuare le fasi di pianificazione del progetto.

[![Esempio di un ruolo.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso è stato assunto per completare un progetto di tempistica e materiali con uno statuto progetto approvato. Il project manager junior sta ancora completando l'ambito del progetto. Il responsabile delle risorse sta attualmente individuando risorse specifiche che saranno prenotate per lavorare sul nuovo progetto. A causa della natura critica del progetto, lo sponsor del progetto ha richiesto il Senior Project Manager come uno dei ruoli. Il responsabile delle risorse deve acquisire la nuova risorsa e definire il ruolo nel sistema nel caso in cui il project manager junior richieda le informazioni sulla risorsa durante la pianificazione del progetto.

I passaggi seguenti mostrano come il responsabile delle risorse può configurare il ruolo di Senior project manager e associarvi le caratteristiche della risorsa. Successivamente, il ruolo può essere utilizzato per cercare le risorse disponibili che corrispondono alle competenze delle risorse richieste.

1. Nella pagina **Configura ruoli**, seleziona **Nuovo**, quindi immetti i valori seguenti:

    - **ID ruolo:** Senior Project Manager
    - **Descrizione:** Senior Project Manager

2. Seleziona **Crea**.
3. Seleziona il ruolo **Senior Project Manager**, quindi seleziona **Configura caratteristiche**.
4. Nel campo **Tipo di caratteristiche**, seleziona **Competenza**.
5. Nel campo **Caratteristiche disponibili**, immetti la competenza da cercare.
6. Nel campo **Tipo di caratteristica**, seleziona **Certificato**.
7. Nel campo **Caratteristiche disponibili**, immetti il tipo di certificato da cercare.

## <a name="assign-a-project-resource-to-a-project"></a>Assegnare una risorsa di progetto a un progetto

1. Nella pagina **Tutti i progetti**, seleziona il progetto **Fase di aggiornamento XYZ 2**.
2. Nella scheda **Team progetto e programmazione**, seleziona **Aggiungi**.
3. Nel campo **Ruolo**, seleziona **Membro del team**.
4. Seleziona **Prenota da calendario**.
5. Nella pagina **Disponibilità risorse**, seleziona **Visualizza impostazioni**.
6. Nella pagina **Modifica impostazioni visualizzazione**, immetti i seguenti valori:

    - **Formato per la visualizzazione dell'intervallo di date:** giornaliero
    - **Visualizza descrizioni disponibili:** Sì
    - **Visualizza capacità rimanente:** Sì

7. Seleziona una risorsa dall'elenco delle risorse.
8. Seleziona **Prenota definitivamente** e **Piena capacità**.

## <a name="assign-a-resource-to-a-default-role"></a>Assegnare una risorsa a un ruolo predefinito

Per aiutare i responsabili di progetto o risorse possono eseguire il drill-down sulle risorse che possono essere prenotate per un progetto. Puoi associare un ruolo predefinito a una risorsa esistente o a una risorsa appena acquisita. Ad esempio, quando è stato assunto Daniel, aveva l'esperienza e le competenze per ricoprire il ruolo di analista aziendale. Il responsabile delle risorse ha assegnato questo ruolo come ruolo predefinito di Daniel. Pertanto, il responsabile delle risorse ha aggiunto Daniel a un pool di analisti aziendali disponibili a lavorare sui progetti.

Durante la prenotazione delle risorse, i project manager possono filtrare le risorse ruolo disponibili per lavorare sui progetti. Possono utilizzare queste informazioni come un criterio quando eseguono l'analisi decisionale multicriterio durante l'evasione delle risorse. Possono anche aggiungere altre caratteristiche delle risorse al filtro per cercare risorse con competenze, istruzione ed esperienza specifiche per un determinato progetto.

**Scenario:** è stato avviato un progetto approvato e il ruolo di Senior project manager è stato riservato come risorsa pianificata durante la fase di pianificazione del progetto. Il responsabile delle risorse ha ora acquisito una risorsa per svolgere il ruolo di Senior project manager.

1. Nella pagina **Elenco risorse**, seleziona **Daniel Goldschmidt**.
2. Nella pagina **Ruolo risorsa**, seleziona **Nuovo**, quindi immetti i valori seguenti:

    - **Validità:** immetti la data corrente.
    - **Scadenza:** immetti **Mai**.
    - **Ruolo:** immetti **Senior Project Manager**.

3. Seleziona **Salva** e quindi chiudi la pagina.
4. Nella scheda **Competenze**, aggiungi la competenza **ProjectMgmt** e il certificato **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]