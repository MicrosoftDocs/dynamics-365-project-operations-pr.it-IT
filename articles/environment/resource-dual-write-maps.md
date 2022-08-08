---
title: Versioni della mappa a doppia scrittura di Project Operations
description: Questo articolo fornisce l'elenco delle mappe a doppia scrittura richieste per Dynamics 365 Project Operations.
author: sigitac
ms.date: 07/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e904ad18b6ea94cd6d31d1878b5bc9e7c52be741
ms.sourcegitcommit: c8b8fef5626790208c5290b1bb92b17a5d90d286
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112434"
---
# <a name="project-operations-dual-write-map-versions"></a>Versioni della mappa a doppia scrittura di Project Operations

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Utilizzando Dynamics 365 Project Operations per scenari di risorse/materiali non stoccati, è necessario che nell'ambiente sia in esecuzione una serie di mappe a doppia scrittura. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Prerequisiti delle mappe: soluzione di orchestrazione doppia scrittura

Le mappe seguenti sono prerequisiti obbligatori per la soluzione Project Operations. Assicurati di eseguire le mappe elencate nella tabella seguente e tutte le mappe delle tabelle correlate nel tuo ambiente.

| Mapping tabella | Sincronizzazione iniziale |
| --- | --- |
| Libro mastro (msdyn_ledgers) | Richiede la sincronizzazione iniziale per la mappa della tabella e tutti i prerequisiti. Le app per la finanza e le operazioni sono il master per la sincronizzazione iniziale. |
| Persone giuridiche (cdm_companies) | Non obbligatorio. Il sistema popola questa entità automaticamente quando gli ambienti sono collegati utilizzando la doppia scrittura. |
| Clienti V3 (accounts) | Non obbligatorio per il provisioning. |
| Fornitori V2 (msdyn_vendors) | Non obbligatorio per il provisioning. |

1. Dall'elenco dei mapping, seleziona la mappa Libro mastro **(msdyn\_ledgers)** con tutti i prerequisiti e seleziona la casella di controllo **Sincronizzazione iniziale**. Nel campo **Master per la sincronizzazione iniziale** seleziona **App per la finanza e le operazioni** sia per la mappa del contabilità generale che per tutte le mappe dei prerequisiti. Selezionare **Esegui**.

![Sincronizzazione dei mapping del libro mastro.](media/DW6.png)

2. Segui gli stessi passaggi per tutte le mappe della tabella rimanenti elencate nella tabella sopra. Non selezionare la casella di controllo **Sincronizzazione iniziale** durante l'esecuzione di tali mappe.

## <a name="project-operations-dual-write-maps"></a>Mappe a doppia scrittura di Project Operations

Le mappe seguenti sono obbligatorie per una soluzione Project Operations. Le versioni della mappa a doppia scrittura sono elencate a partire dall'aggiornamento di Project Operations di maggio 2021, versione 4.10.0.186.

| Mapping entità | Ultima versione | Sincronizzazione iniziale | Versione di Dynamics 365 Finance richiesta |
| --- | --- | --- | --- |
| Entità di integrazione per le relazioni di transazione del progetto (msdyn\_transactionconnections) | 1.0.0.0 | Non obbligatorio per il provisioning. ||
| Intestazioni del contratto di progetto (ordini di vendita) | 1.0.0.1 | Non obbligatorio per il provisioning. ||
| Voci del contratto di progetto (salesorderdetails) | 1.0.0.0 | Non obbligatorio per il provisioning. ||
| Fonte di finanziamento di progetto (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Non obbligatorio per il provisioning. ||
| Tabella di integrazione di progetto per le stime dei materiali (msdyn\_estimatelines) | 1.0.0.0 | Non obbligatorio per il provisioning. ||
| Proposte di fattura di progetto V2 (invoices) | 1.0.0.3 | Non obbligatorio per il provisioning. ||
| Valori effettivi dell'integrazione di Project Operations (msdyn_actuals) | 1.0.0.14 | Non obbligatorio per il provisioning. ||
| Passaggi fondamentali delle righe del contratto per l'integrazione di Project Operations (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Non obbligatorio per il provisioning. ||
| Entità dell'integrazione di Project Operations per stime delle spese (msdyn_estimatelines) | 1.0.0.2 | Non obbligatorio per il provisioning. ||
| Entità di integrazione per stime orarie di Project Operations (msdyn_estimateslines) | 1.0.0.5 | Non obbligatorio per il provisioning. ||
| Entità di esportazione categorie delle spese di progetto di integrazione di Project Operations (msdyn_expensecategories) | 1.0.0.1 | Non obbligatorio per il provisioning. ||
| Entità di esportazione delle spese di progetto di integrazione di Project Operations (msdyn_expenses) | 1.0.0.3 | Non obbligatorio per il provisioning. ||
| Entità di esportazione fattura fornitore progetto integrazione Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Non obbligatorio per il provisioning. |10.0.26 o successive|
| Entità di esportazione riga fattura fornitore progetto integrazione Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.4 | Non obbligatorio per il provisioning. | 10.0.26 o successive |
| Ruoli delle risorse di progetto per tutte le aziende (bookableresourcecategories) | 1.0.0.1 | Richiede una sincronizzazione iniziale per la mappa della tabella per sincronizzare i ruoli delle risorse del responsabile di progetto e del membro del team che sono popolati nell'ambiente Dynamics 365 Dataverse durante il provisioning. Dataverse è la fonte principale per la sincronizzazione iniziale. ||
| Attività di progetto (msdyn_projecttasks) | 1.0.0.4 | Non obbligatorio per il provisioning. ||
| Categorie di transazione di progetto (msdyn_transactioncategories) | 1.0.0.0 | Non obbligatorio per il provisioning. ||
| Progetti V2 (msdyn_projects) | 1.0.0.2 | Non obbligatorio per il provisioning. ||

Completa i seguenti passaggi per eseguire le mappe elencate.

1. Abilita i ruoli delle risorse di progetto per la mappa della tabella **Tutte le società (bookableresourcecategories)** poiché questa mappa richiede la sincronizzazione iniziale. Nel campo **Master per la sincronizzazione iniziale** seleziona **Common Data Service**. 

 ![Sincronizzazione della mappa della tabella dei ruoli di risorse.](media/6ResourceInitialSync.jpg)

 Attendi fino a quando lo stato della mappa è **In esecuzione** prima di passare alla fase successiva.

2. Seleziona tutte le mappe obbligatorie rimanenti. Puoi filtrarle nell'elenco delle mappe a doppia scrittura utilizzando la parola chiave **Progetto** nella ricerca nell'angolo in alto a destra. È possibile selezionare tutte le mappe e quindi eseguirle. Per ulteriori informazioni, vedi [Gestire più mappe di tabelle](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Assicurati di abilitare ed eseguire anche le mappe di entità correlate.

### <a name="project-operations-dual-write-map-versions"></a>Versioni della mappa a doppia scrittura di Project Operations

Esegui sempre l'ultima versione della mappa nel tuo ambiente. Alcune funzionalità e capacità potrebbero non funzionare correttamente se esiste una delle seguenti condizioni:

- Una mappa non è attivata.
- L'ultima versione della mappa non è attivata. 
- Le mappe di tabella correlate non sono attivate.

Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Puoi attivare una nuova versione della mappa selezionando **Versioni mappa tabella** e quindi selezionando l'ultima versione e salvando la versione selezionata. Se hai personalizzato una mappa di tabella predefinita, dovrai riapplicare le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
