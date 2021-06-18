---
title: Configurazione di Project Operations e integrazione dei dati di configurazione
description: Questo argomento fornisce informazioni sull'impostazione e la configurazione delle mappe a doppia scrittura di Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001071"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configurazione di Project Operations e integrazione dei dati di configurazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento fornisce informazioni sull'integrazione a doppia scrittura di Project Operations per l'impostazione e la configurazione delle entità.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratti di progetto, righe di contratto e progetti

I contratti di progetto, le righe di contratto e i progetti vengono creati in Dataverse e sincronizzati con le app Finance and Operations per la contabilità aggiuntiva. I record in queste entità possono essere creati ed eliminati solo in Dataverse. Tuttavia, è possibile aggiungere gli attributi contabili come i valori predefiniti della fascia IVA o le dimensioni finanziarie a questi record nelle app Finance and Operations.

  ![Concetti di integrazione del contratto di progetto](./media/1ProjectContract.jpg)

I lead, le opportunità e le offerte di impegni di vendita vengono tracciati in Dataverse e non sincronizzati con le app Finance and Operations perché non esiste una contabilità a valle associata a questo impegno.

La funzionalità del contratto di progetto in Dataverse crea un record del contratto di progetto nelle app Finance and Operations utilizzando la mappa di tabella **Intestazioni contratto di progetto (salesorders)**. Il salvataggio di un contratto di progetto in Dataverse avvia la creazione di un record dell'entità cliente del contratto di progetto. Questo record è sincronizzato con le app Finance and Operations che utilizzano la mappa di tabella **Fonte di finanziamento del progetto (msdyn\_projectcontractssplitbillingrules)**. Questa mappa sincronizza anche le aggiunte, gli aggiornamenti e le eliminazioni dei clienti del contratto di progetto. Le percentuali di fatturazione separata tra i clienti del contratto di progetto vengono gestite solo in Dataverse e non sono sincronizzate con le app Finance and Operations.

Dopo la creazione di un contratto di progetto in Dataverse, il contabile di progetto può aggiornare gli attributi di contabilità per questo contratto di progetto nelle app Finance and Operations andando in **Gestione progetti e contabilità** > **Contratti di progetto** > **Configura** > **Mostra contabilità predefinita**. Il contabile può esaminare gli attributi del contratto di progetto operativo, come la data di consegna richiesta e l'importo del contratto selezionando l'ID contratto di progetto nelle app Finance and Operations che apre il record del contratto di progetto correlato in Dataverse.

L'entità del progetto è sincronizzata con le app Finance and Operations utilizzando la mappa della tabella **Progetti V2 (msdyn\_projects)**. Il contabile di progetto può:

  - Rivedere i progetti nelle app Finance and Operations andando in **Gestione progetti e contabilità** > **Tutti i progetti**. 
  - Aggiornare gli attributi di contabilità per il progetto nelle app Finance and Operations andando in **Gestione progetti e contabilità** > **Tutti i progetti** > **Configura** > **Mostra contabilità predefinita**.  
  - Rivedere gli attributi del progetto operativo, come le date di inizio e di fine stimate, selezionando l'ID del progetto nelle app Finance and Operations che apre il record del progetto correlato in Dataverse.

Un progetto è associato a un contratto di progetto tramite l'entità **Riga contratto di progetto**.

Le righe di contratto di progetto in Dataverse creano una regola di fatturazione del contratto di progetto nelle app Finance and Operations utilizzando la mappa di tabella **Righe contratto di progetto (salesorderdetails)**. Il metodo di fatturazione definisce il tipo di regola di fatturazione del contratto di progetto nelle app Finance and Operations:

  - Le righe di contratto di progetto con un metodo di fatturazione di tempo e materiali creano una regola di fatturazione di tipo tempo e materiali.
  - Le righe di contratto del metodo di fatturazione a prezzo fisso creano una regola di fatturazione passaggio fondamentale.

Le righe di contratto di progetto possono essere riviste dal contabile del progetto nelle app Finance and Operations andando in **Gestione progetti e contabilità** > **Contratti di progetto** > **Configura** > **Mostra contabilità predefinita** e rivedendo i dettagli nella scheda **Righe di contratto**. Il contabile può anche impostare dimensioni finanziarie predefinite per le righe di contratto del metodo di fatturazione a prezzo fisso in questa scheda.

## <a name="billing-milestones"></a>Passaggi fondamentali di fatturazione

Le righe di contratto di progetto che utilizzano il metodo di fatturazione a prezzo fisso vengono fatturate tramite i passaggi fondamentali di fatturazione. I passaggi fondamentali di fatturazione vengono sincronizzati per proiettare le transazioni in acconto nelle app Finance and Operations utilizzando la mappa della tabella **Passaggi fondamentali della riga di contratto di interazione di Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integrazione dei passaggi fondamentali di fatturazione](./media/2Milestones.jpg)

Il contabile può esaminare le transazioni in acconto e modificare gli attributi contabili per tali transazioni accedendo in **Gestione progetti e contabilità** > **Contratti di progetto** > **Gestisci** > **Transazioni in acconto** o **Gestione progetti e contabilità** > **Tutti i progetti** > **Gestisci** > **Transazioni in acconto**.

Quando crei per la prima volta un passaggio fondamentale di fatturazione per una determinata riga di contratto di progetto, il sistema crea automaticamente un progetto di stima dei ricavi a prezzo fisso per il progetto associato a questa riga di contratto. I progetti di stima dei ricavi a prezzo fisso possono essere rivisti andando in **Gestione progetti e contabilità** > **Progetti di stima dei ricavi a prezzo fisso**.

### <a name="project-tasks"></a>Attività di progetto

Le attività del progetto vengono sincronizzate nelle app Finance and Operations tramite la mappa della tabella **Attività di progetto (msdyn\_projecttasks)** solo a scopo di riferimento. Le operazioni di creazione, aggiornamento ed eliminazione non sono supportate tramite le app Finance and Operations.

  ![Integrazione di attività di progetto](./media/3Tasks.jpg)

## <a name="project-resources"></a>Risorse di progetto

L'entità **Ruoli di risorse di progetto** è sincronizzata con le app Finance and Operations utilizzando la mappa di tabella **Ruoli di risorse di progetto per tutte le società (bookableresourcecategories)** solo a scopo di riferimento. Dal momento che i ruoli di risorse in Dataverse non sono specifici dell'azienda, il sistema crea automaticamente i rispettivi record dei ruoli di risorse specifici dell'azienda nelle app Finance and Operations automaticamente per tutte le persone giuridiche incluse nell'ambito dell'integrazione a doppia scrittura.

![Integrazione di ruoli di risorse](./media/5Resources.jpg)

Le risorse di progetto in Project Operations vengono gestite in Dataverse e non sono sincronizzate con le app Finance and Operations.

### <a name="transaction-categories"></a>Categorie di transazioni

Le categorie di transazione vengono mantenute in Dataverse e sincronizzate con le app Finance and Operations utilizzando la mappa della tabella **Categorie di transazione di progetto (msdyn\_transactioncategories)**. Dopo che il record della categoria di transazione è stato sincronizzato, il sistema crea automaticamente quattro record di categoria condivisi. Ogni record corrisponde a un tipo di transazione nelle app Finance and Operations e lo collega al record della categoria di transazione.

![Integrazione di categorie di transazione](./media/4TransactionCategories.jpg)

L'utilizzo delle categorie di transazione per le stime e i valori effettivi richiede che il contabile del progetto o l'amministratore di sistema crei le categorie di progetto corrispondenti in ogni persona giuridica. Per ulteriori informazioni, vedi [Configurare le categorie di progetto](../project-accounting/configure-project-categories.md).
