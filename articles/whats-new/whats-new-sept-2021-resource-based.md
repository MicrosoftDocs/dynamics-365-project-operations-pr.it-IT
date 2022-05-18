---
title: Novità della versione di settembre 2021 - Project Operations per scenari basati su risorse/materiali non stoccati
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di settembre 2021 di Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06f23630ef0205394f376e5bb93a29ae8a9eab15
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582899"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità della versione di settembre 2021 - Project Operations per scenari basati su risorse/materiali non stoccati

*Si applica a: Project Operations per scenari basati su risorse/materiali non stoccati*

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

   - Project Operations in ambiente Microsoft Dataverse versione 4.14.0.99.
   - Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Non sono disponibili aggiornamenti per le mappe a doppia scrittura di Project Operations in questa versione. Per un elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni della mappa a doppia scrittura di Project Operations](../environment/resource-dual-write-maps.md).

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità e capacità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella pagina **Doppia scrittura** nella colonna **Versione**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato una mappa di tabella predefinita, riapplica le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Tempistica e spesa | 1811407 | Adeguato il ruolo di sicurezza del responsabile dell'approvazione del progetto per l'approvazione delle voci di spesa. |
| Tempistica e spesa | 1811438 | Adeguato il ruolo di sicurezza del responsabile della cancellazione dell'approvazione dell'inserimento ore. |
| Tempistica e spesa | 2370126 | Icone **Attività di progetto** e **Ruolo** aggiornate nell'entità **Inserimento ore**. |
| Tempistica e spesa | 2379879 | Corretta la funzionalità **Copia settimana** nell'immissione delle ore quando si utilizza Dynamics 365 da telefono. |
| Prezzi e fatturazione | 2371906 | L'importo totale della fattura proforma non deve essere regolabile in Project Operations per le distribuzioni basate sulle risorse. |
| Prezzi e fatturazione | 2385802 | Risolto l'errore che si verificava con le ore effettive negative quando i totali del progetto vengono aggiornati. |
| Prezzi e fatturazione | 2389675 | Comportamento di conferma della fattura proforma migliorato. L'entità dei lavori di lunga durata deve prendere in considerazione l'attività richiesta per scrivere i risultati di conferma per la contabilità. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestione progetti e contabilità in Dynamics 365 Finance

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Viaggi e spese | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Gli importi sulle transazioni IVA e fornitori registrati da una spesa creata da una transazione con carta di credito non sono corretti. |
| Viaggi e spese | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Le righe di liquidazione errate vengono create quando viene generato il giornale di registrazione pagamenti. |
| Viaggi e spese | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Gli importi sulle transazioni IVA registrati da una spesa creata da una transazione con carta di credito non sono corretti. |
| Viaggi e spese | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | L'eliminazione di una riga di spesa potrebbe richiedere molto tempo. |
| Contabilità di progetto | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Dopo aver applicato KB 4619395, cambiando la sequenza numerica in **Continuo** non è supportato e quando si invia una stima, si verifica il seguente errore: "Il sistema non supporta l'installazione 'continua' della sequenza numerica Proj_X". |
| Contabilità di progetto | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | La registrazione di una fattura fornitore potrebbe non riuscire con il seguente messaggio di errore: "Le transazioni sul giustificativo non si bilanciano come per il 17/05/2021. (valuta di contabilizzazione: 0,00 - valuta contabile: 0,01)". |
