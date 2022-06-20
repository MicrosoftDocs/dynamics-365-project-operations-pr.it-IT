---
title: Migrare i passaggi fondamentali di fatturazione completamente fatturati al cutover
description: Questo articolo spiega come migrare i passaggi fondamentali di fatturazione a prezzo fisso che sono stati fatturati al cliente per i contratti di progetto aperti prima della data di inizio.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912245"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrare i passaggi fondamentali di fatturazione completamente fatturati al cutover

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

## <a name="scenario"></a>Scenario

Contoso sarà disponibile con Microsoft Dynamics 365 Project Operations per scenari di risorse/non stoccate. Nell'ambito delle attività di cutover, il team di implementazione deve migrare i contratti di progetto aperti dal vecchio sistema. Alcuni contratti di progetto includono righe di contratto che utilizzano il metodo di fatturazione a prezzo fisso e sono già state parzialmente fatturate al cliente finale. Il team di implementazione deve migrare questi passaggi fondamentali di fatturazione come **Fattura cliente registrata**, perché devono essere inclusi nel valore totale del contratto ai fini del riconoscimento dei ricavi. Tuttavia, i saldi dei clienti in Contabilità clienti e Contabilità generale non devono essere interessati.

## <a name="solution"></a>Soluzione

### <a name="prerequisites"></a>Prerequisiti

- È necessario installare Dynamics 365 Finance 10.0.24 o versioni successive.
- L'ambiente in cui verranno completati i passaggi di migrazione deve essere in modalità di manutenzione. Non devono essere eseguite altre attività durante la migrazione dei passaggi fondamentali.
- I passaggi di migrazione devono essere seguiti esattamente come descritto qui e possono essere utilizzati solo per l'attività di cutover. Microsoft non supporta nessun altro utilizzo di questa funzionalità.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Creare una versione completa della mappa a doppia scrittura dei passaggi fondamentali della voce di contratto di integrazione di Project Operations 

1. Assicurati che la mappatura di destinazione per l'entità **Passaggi fondamentali della voce di contratto di integrazione di Project Operations** sia aggiornata. 

    1. In Finance, vai a **Gestione dati** \> **Entità di dati** e seleziona l'entità **Passaggi fondamentali della voce di contratto di integrazione di Project Operations**. 
    2. Seleziona **Modifica mapping di destinazione**. 
    3. Sulla pagina **Mappa gestione temporanea a destinazione**, seleziona **Genera mappa**, quindi conferma di voler generare la mappa.

2. Arresta e aggiorna la mappa a doppia scrittura **Passaggi fondamentali della voce di contratto di integrazione di Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Vai a **Gestione dati** \> **Doppia scrittura**, seleziona la mappa e apri i dettagli. 
    2. Seleziona **Arresta** e attendi che il sistema arresti la mappa. 
    3. Seleziona **Aggiorna tabelle**.

3. Aggiungi una mappa per lo stato della transazione.

    1. Seleziona **Aggiungi mapping**.
    2. Sulla nuova riga, nella colonna **App per la finanza e le operazioni**, seleziona il campo **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Nella colonna **Microsoft Dataverse** seleziona **msdyn\_invoicestatus \[Invoice status\]**.
    4. Nella colonna **Tipo di mappa** seleziona la freccia a destra (**\>**).
    5. Nella finestra di dialogo che appare, nel campo **Direzione sincronizzazione** seleziona **Da Dataverse alle app per la finanza e le operazioni**.
    6. Seleziona **Aggiungi trasformazione**.
    7. Nel campo **Tipo di trasformazione** seleziona **ValueMap**.
    8. Seleziona **Aggiungi mapping valori**.
    9. Nel campo a sinistra immetti **4**. Nel campo a destra immetti **192350001**. 
    10. Seleziona **Salva** e quindi chiudi la finestra di dialogo.

4. Seleziona **Salva con nome** per salvare la versione della mappa a doppia scrittura. 
5. Nel riquadro **Aggiungi tabella** nel campo **Editore** seleziona **Editore predefinito**.
6. Nel campo **Versione** immetti la versione.
7. Nel campo **Descrizione** inserisci una nota su questa versione cutover della mappa. 
8. Seleziona **Salva**.
9. Avvia la mappa.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrarere i passaggi fondamentali fatturati all'ambiente Dataverse

1. Nell'ambiente Dataverse di Project Operations, crea i passaggi fondamentali con uno stato della fattura di **Pronto per la fatturazione**. A questo punto, non migrare i passaggi fondamentali che non sono stati fatturati.

    > [!NOTE]
    > Prima di migrare i passaggi fondamentali di fatturazione, accertati che le dimensioni finanziarie correlate alla riga del contratto di progetto siano impostate come previsto. Le dimensioni finanziarie non possono essere modificate una volta completata la migrazione.

2. Dopo che tutti passaggi fondamentali sono state migrati, interrompi le seguenti mappe a doppia scrittura:

    - Passaggi fondamentali delle righe del contratto per l'integrazione di Project Operations (msdyn\_contractlinescheduleofvalues)
    - Valori effettivi dell'integrazione di Project Operations (msdyn\_actuals)
    - Proposta di fattura di progetto V2 (fatture)

    Per interrompere le mappe, attieniti alla seguente procedura:

    1. In Finance, vai a **Gestione dati** \> **Doppia scrittura**, seleziona una mappa e apri i dettagli.
    2. Seleziona **Arresta** e attendi che il sistema arresti la mappa.

3. Nell'ambiente Dataverse di Project Operations, crea e conferma le fatture pro-forma per i passaggi fondamentali di fatturazione. 

    1. Nella mappa del sito, vai ai contratti di progetto, seleziona i contratti e quindi seleziona **Crea fatture**.
    2. Dopo aver creato le fatture, aprile dal menu **Fatture** nella mappa del sito, quindi seleziona **Conferma**.

    Questo passaggio crea i record richiesti nell'ambiente Dataverse. Tuttavia, non influisce sui dati finanziari e sulla contabilità clienti, perché le mappe a doppia scrittura elencate in precedenza sono state interrotte.

4. Dopo che tutte le fatture proforma sono state confermate, riporta tutte le mappe a doppia scrittura allo stato iniziale.

    1. Aggiorna la versione della mappa a doppia scrittura **Passaggi fondamentali della voce di contratto di integrazione di Project Operations** (**msdyn\_contractlinescheduleofvalues**) di nuovo sull'originale. 
    2. Seleziona la mappa a doppia scrittura nell'elenco delle mappe, seleziona **Versione mappa tabella** e quindi seleziona la versione originale della mappa tabella.
    3. Seleziona **Salva**.
    4. Riavvia le seguenti mappe a doppia scrittura:

        - Passaggi fondamentali delle righe del contratto per l'integrazione di Project Operations (msdyn\_contractlinescheduleofvalues)
        - Valori effettivi dell'integrazione di Project Operations (msdyn\_actuals)
        - Proposta di fattura di progetto V2 (fatture)

I passaggi fondamentali sono ora migrati e il sistema è pronto per le fasi successive dell'attività di cutover.
