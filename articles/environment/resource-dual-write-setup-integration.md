---
title: Configurazione di Project Operations e integrazione dei dati di configurazione
description: Questo argomento fornisce informazioni sull'impostazione e la configurazione delle mappe a doppia scrittura di Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586901"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configurazione di Project Operations e integrazione dei dati di configurazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento fornisce informazioni sull'integrazione a doppia scrittura di Project Operations per l'impostazione e la configurazione delle entità.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratti di progetto, righe di contratto e progetti

I contratti di progetto, le righe di contratto e i progetti vengono creati in Dataverse e sincronizzati con le app per la finanza e le operazioni per una contabilità aggiuntiva. I record in queste entità possono essere creati ed eliminati solo in Dataverse. Tuttavia, gli attributi contabili come le impostazioni predefinite della fascia IVA e le dimensioni finanziarie possono essere aggiunti a questi record nelle app per la finanza e le operazioni.

  ![Concetti di integrazione del contratto di progetto.](./media/1ProjectContract.jpg)

Vengono monitorati i lead, le opportunità e i preventivi delle attività di vendita in Dataverse e non viene eseguita la sincronizzazione con le app per la finanza e le operazioni perché non esiste una contabilità a valle associata a questa attività.

La funzionalità del contratto di progetto in Dataverse crea un record del contratto di progetto nelle app per la finanza e le operazioni utilizzando la mappa della tabella **Intestazioni contratto di progetto (ordini di vendita)**. Il salvataggio di un contratto di progetto in Dataverse avvia la creazione di un record dell'entità cliente del contratto di progetto. Questo record viene sincronizzato con le app per la finanza e le operazioni utilizzando la mappa della tabella **Fonte di finanziamento progetto (msdyn\_projectcontractssplitbillingrules)**. Questa mappa sincronizza anche le aggiunte, gli aggiornamenti e le eliminazioni dei clienti del contratto di progetto. Le percentuali di fatturazione suddivise tra i clienti del contratto di progetto vengono gestite solo in Dataverse e non vengono sincronizzate con le app per la finanza e le operazioni.

Dopo la creazione di un contratto di progetto in Dataverse, il contabile di progetto può aggiornare gli attributi contabili per questo contratto di progetto nelle app per la finanza e le operazioni accedendo a **Gestione progetti e contabilità** > **Contratti di progetto** > **Impostazione** > **Mostra contabilità predefinita**. Il contabile può rivedere gli attributi del contratto di progetto operativo, come la data di consegna richiesta e l'importo del contratto, selezionando l'ID contratto di progetto nelle app per la finanza e le operazioni che apre il record di contratto di progetto correlato in Dataverse.

L'entità del progetto viene sincronizzata con le app per la finanza e le operazioni utilizzando la mappa della tabella **Progetti V2 (msdyn\_projects)**. Il contabile di progetto può:

  - Esamina i progetti nelle app per la finanza e le operazioni andando in **Gestione progetti e contabilità** > **Tutti i progetti**. 
  - Aggiorna gli attributi contabili per il progetto nelle app per la finanza e le operazioni andando in **Gestione progetti e contabilità** > **Tutti i progetti** > **Impostazione** > **Mostra contabilità predefinita**.  
  - Esamina gli attributi operativi del progetto, come le date di inizio e fine stimate, selezionando l'ID progetto nelle app per la finanza e le operazioni che apre il record del progetto correlato in Dataverse.

Un progetto è associato a un contratto di progetto tramite l'entità **Riga contratto di progetto**.

Le righe di contratto di progetto in Dataverse creano una regola di fatturazione del contratto di progetto nelle app per la finanza e le operazioni utilizzando la mappa della tabella **Righe di contratto di progetto (dettagli ordini di vendita)**. Il metodo di fatturazione definisce il tipo di regola di fatturazione del contratto di progetto nelle app per la finanza e le operazioni:

  - Le righe di contratto di progetto con un metodo di fatturazione di tempo e materiali creano una regola di fatturazione di tipo tempo e materiali.
  - Le righe di contratto del metodo di fatturazione a prezzo fisso creano una regola di fatturazione passaggio fondamentale.

Le righe del contratto di progetto possono essere esaminate dal contabile di progetto nelle app per la finanza e le operazioni andando in **Gestione progetti e contabilità** > **Contratti di progetto** > **Impostazione** > **Mostra contabilità predefinita**, e rivedendo i dettagli nella scheda **Righe di contratto**. Il contabile può anche impostare le dimensioni finanziarie predefinite per le righe di contratto del metodo di fatturazione a prezzo fisso in questa scheda.

## <a name="billing-milestones"></a>Passaggi fondamentali di fatturazione

Le righe di contratto di progetto che utilizzano il metodo di fatturazione a prezzo fisso vengono fatturate tramite i passaggi fondamentali di fatturazione. I passaggi fondamentali di fatturazione vengono sincronizzati per proiettare le transazioni in acconto nelle app per la finanza e le operazioni utilizzando la mappa della tabella **Passaggi fondamentali delle righe del contratto per l'integrazione di Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integrazione dei passaggi fondamentali di fatturazione.](./media/2Milestones.jpg)

Il contabile può esaminare le transazioni in acconto e modificare gli attributi contabili per tali transazioni accedendo in **Gestione progetti e contabilità** > **Contratti di progetto** > **Gestisci** > **Transazioni in acconto** o **Gestione progetti e contabilità** > **Tutti i progetti** > **Gestisci** > **Transazioni in acconto**.

Quando crei per la prima volta un passaggio fondamentale di fatturazione per una determinata riga di contratto di progetto, il sistema crea automaticamente un progetto di stima dei ricavi a prezzo fisso per il progetto associato a questa riga di contratto. I progetti di stima dei ricavi a prezzo fisso possono essere rivisti andando in **Gestione progetti e contabilità** > **Progetti di stima dei ricavi a prezzo fisso**.

### <a name="project-tasks"></a>Attività di progetto

Le attività di progetto vengono sincronizzate con le app per la finanza e le operazioni tramite la mappa della tabella **Attività di progetto (msdyn\_projecttasks)** solo a scopo di riferimento. La creazione, l'aggiornamento e l'eliminazione di operazioni non sono supportati tramite le app per la finanza e le operazioni.

  ![Integrazione di attività di progetto.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Risorse di progetto

L'entità **Ruoli delle risorse di progetto** viene sincronizzata con le app per la finanza e le operazioni tramite la mappa della tabella **Ruoli delle risorse di progetto per tutte le società (bookableresourcecategories)** solo a scopo di riferimento. Perché i ruoli delle risorse in Dataverse non sono specifici dell'azienda, il sistema crea automaticamente i rispettivi record dei ruoli delle risorse specifici dell'azienda nelle app per la finanza e le operazioni per tutte le persone giuridiche incluse nell'ambito dell'integrazione a doppia scrittura.

![Integrazione di ruoli di risorse.](./media/5Resources.jpg)

Le risorse di progetto in Project Operations sono mantenute in Dataverse e non sono sincronizzate con le app per la finanza e le operazioni.

### <a name="transaction-categories"></a>Categorie di transazioni

Le categorie di transazione sono mantenute in Dataverse e sincronizzate con le app per la finanza e le operazioni tramite la mappa della tabella **Categorie di transazioni di progetto (msdyn\_transactioncategories)**. Dopo che il record della categoria di transazione è stato sincronizzato, il sistema crea automaticamente quattro record di categoria condivisi. Ogni record corrisponde a un tipo di transazione nelle app per la finanza e le operazioni e lo collega al record della categoria di transazione.

![Integrazione di categorie di transazione.](./media/4TransactionCategories.jpg)

L'utilizzo delle categorie di transazione per le stime e i valori effettivi richiede che il contabile del progetto o l'amministratore di sistema crei le categorie di progetto corrispondenti in ogni persona giuridica. Per ulteriori informazioni, vedi [Configurare le categorie di progetto](../project-accounting/configure-project-categories.md).
