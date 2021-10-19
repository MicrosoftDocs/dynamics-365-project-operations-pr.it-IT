---
title: Novità di agosto 2021 - Project Operations per scenari di risorse/materiali non stoccati
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di agosto 2021 di Project Operations per scenari di risorse/materiali non stoccati.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501376"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di agosto 2021 - Project Operations per scenari di risorse/materiali non stoccati

*Si applica a: Project Operations per scenari basati su risorse/materiali non stoccati*

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

   - Project Operations in ambiente Microsoft Dataverse versione 4.13.0.152.
   - Gestione progetti e contabilità in ambiente Dynamics 365 Finance versione 10.0.20.

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- **Set di approvazione**: i set di approvazione consentono di raggruppare le richieste di approvazione di ore, spese o utilizzo dei materiali in sottoinsiemi di operazioni più piccoli. Questo raggruppamento consente di elaborare le approvazioni per progetto, in un ordine specifico e consente di riprovare e mettere in sequenza. Il raggruppamento delle richieste migliora l'affidabilità e la tracciabilità del processo di approvazione per grandi volumi di approvazioni. Per ulteriori informazioni, vedi [Set di approvazione](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Non sono disponibili aggiornamenti per le mappe a doppia scrittura di Project Operations in questa versione.

Per un elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni della mappa a doppia scrittura di Project Operations](../environment/resource-dual-write-maps.md).

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità e capacità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella pagina **Doppia scrittura** nella colonna **Versione**. Attiva una nuova versione della mappa selezionando **Versioni mappa della tabella**, selezionando la versione più recente, quindi salvando la versione selezionata. Se hai personalizzato una mappa di tabella predefinita, riapplica le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema con le colonne della tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi di scrittura doppia.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Determinazione dei prezzi e fatturazione | 2295625 | Il nome del passaggio fondamentale deve essere copiato dalla pianificazione delle fatture nei dettagli della voce della fattura. |
| Determinazione dei prezzi e fatturazione | 2316323 | Lo sconto non deve essere modificabile su una fattura proforma in Project Operations per scenari basati sulle risorse. |
| Gestione delle opportunità | 2338619 | Le regole di business **Opportunità** e **Offerta** devono essere invocate solo nelle pagine. |
| Gestione delle risorse | 2316523 | Usando **Invia richiesta** da un requisito di risorsa a cui è associato un ruolo non dovrebbe visualizzare un errore. |
| Gestione delle risorse | 2326885 | La creazione di un requisito di risorse tramite un progetto non dovrebbe visualizzare un errore. |
| Tempistica e spesa | 2335584 | Flussi di attività deprecati nell'inserimento ore. |
| Tempistica e spesa | 2336884 | Il pulsante dell'inserimento ore **Copia settimana** deve funzionare non solo per l'utente corrente. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Contabilità e gestione dei progetti in Dynamics 365 Finance

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Viaggi e spese | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Quando viene creata una spesa da una transazione con carta di credito, vengono registrati importi di transazione fornitore e IVA errati. |
| Viaggi e spese | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | La liquidazione errata sono righe create quando viene generato il giornale di registrazione pagamenti. |
| Viaggi e spese | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Quando viene creata una spesa da una transazione con carta di credito, vengono registrati importi di transazione IVA. |
| Viaggi e spese | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | L'eliminazione di una riga di spesa potrebbe richiedere molto tempo. |
| Contabilità di progetto | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Il sistema non supporta l'impostazione della sequenza numerica continua quando si pubblica una stima dopo aver applicato KB 4619395. |
| Contabilità di progetto | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | La registrazione della fattura fornitore potrebbe non riuscire con il messaggio di errore "Le transazioni sul giustificativo non si bilanciano come al 17/05/2021. (valuta di contabilizzazione: 0,00 - valuta contabile: 0,01)" |
