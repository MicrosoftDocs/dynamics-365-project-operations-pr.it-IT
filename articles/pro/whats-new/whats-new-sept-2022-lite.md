---
title: Novità della versione di settembre 2022 - Distribuzione di Project Operations Lite
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di settembre 2022 della distribuzione lite di Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634857"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Novità della versione di settembre 2022 - Distribuzione di Project Operations Lite

_**Si applica a:** Distribuzione lite: dalla transazione alla fatturazione proforma_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.46.0.60

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

| Area funzionalità | Nome funzionalità | Altre informazioni |
| --- | --- | --- |
| Gestione delle opportunità | **Revisione e attivazione delle offerte**<br>Project Operations garantisce il pieno supporto del processo di vendita. È possibile attivare le offerte di progetto per rappresentare uno stato in cui l'offerta è di sola lettura e viene esaminata. Le offerte attivate possono essere riviste per creare nuove offerte con un numero di revisione incrementato. Le offerte o le revisioni di offerte di progetto attivate possono essere chiuse come acquisite o perse. | [Revisione e attivazione di un'offerta di progetto](/dynamics365/project-operations/sales/activation-and-revision) |
| Prezzi e fatturazione | **Impostazione automatica del prezzo indipendente dal fuso orario**<br>Project Operations ha introdotto il concetto di una data indipendente dal fuso orario su tutti i valori effettivi del progetto. Un nuovo campo, **Data transazione**, è ora disponibile nelle righe del giornale di registrazione e nei valori effettivi e verrà usato per memorizzare la data in cui si è verificata la transazione, ma senza convertire tale data in Coordinated Universal Time. Questa data verrà usata per i processi a valle come l'impostazione automatica del prezzo e la creazione di fatture. | <p>[Determinare i tassi di costo per stime e valori effettivi basati su progetto](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Determinare i prezzi di vendita per stime e valori effettivi basati su progetto](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Prezzi e fatturazione | **Sostituzioni del prezzo alla data di validità in Project Operations**<br>Sostituzioni prezzo data di validità fornisce un modo per ignorare o modificare prezzi specifici nel listino prezzi. | [Sostituzioni prezzo data di validità](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Ore e spesa | **Responsabile approvatore globale**<br>Questa funzione consente l'approvazione centralizzata e del fornitore di software indipendente (ISV), indipendentemente dal progetto o dallo stato del membro del team nel progetto. | [Sicurezza e approvazioni](/dynamics365/project-operations/approvals/approvals-security) |
|Pianificazione e rilevamento dei progetti|**Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione** </br> </br>L'API di modifica del contorno dell'assegnazione delle risorse consente agli sviluppatori di specificare a livello di codice il lavoro di un assegnatario di attività in qualsiasi intervallo di date supportato per una pianificazione più dettagliata del lavoro in fasi temporali.|[Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Aggiornamenti di qualità

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Prezzi e fatturazione | 2754422 | Le stime di materiali e spese non vengono inviate a Dynamics 365 Finance quando i progetti vengono copiati in Dataverse. |
| Ore e spesa | 2787409 | Un responsabile approvazione non valido può approvare una voce di tempo non di progetto. |
| Gestione delle opportunità | 2788907 | Messaggio di errore aggiornato sulla convalida dell'univocità per le righe ordine che includono flag. |
| Ore e spesa | 2842253 | Gestione delle eccezioni null per l'approvazione del tempo. |
| Prezzi e fatturazione | 2844181 | Il mancato ottenimento dell'ID di correlazione blocca la creazione della fattura. |
| Prezzi e fatturazione | 2876628 | QLD, CLD: la stima della risoluzione del listino prezzi deve usare i campi dell'intervallo di date legacy del listino prezzi. |
| Conto lavoro | 2893222 | Se non viene specificato alcun ruolo per una riga del conto lavoro, dovrebbe essere possibile selezionare quella riga su un membro del team per qualsiasi ruolo. |
