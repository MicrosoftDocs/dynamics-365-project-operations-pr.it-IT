---
title: Novità della versione di settembre 2022 - Project Operations per scenari basati su risorse/materiali non stoccati
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di settembre 2022 di Microsoft Dynamics 365 Project Operations per scenari basati su risorse/materiali non stoccati.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634810"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità della versione di settembre 2022 - Project Operations per scenari basati su risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.46.0.60
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.29

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

| Area funzionalità | Nome funzionalità | Altre informazioni |
| --- | --- | --- |
| Gestione delle opportunità | **Revisione e attivazione delle offerte**<br>Project Operations garantisce il pieno supporto del processo di vendita. È possibile attivare le offerte di progetto per rappresentare uno stato in cui l'offerta è di sola lettura e viene esaminata. Le offerte attivate possono essere riviste per creare nuove offerte con un numero di revisione incrementato. Le offerte o le revisioni di offerte di progetto attivate possono essere chiuse come acquisite o perse. | [Revisione e attivazione di un'offerta di progetto](/dynamics365/project-operations/sales/activation-and-revision) |
| Prezzi e fatturazione | **Impostazione automatica del prezzo indipendente dal fuso orario**<br>Project Operations ha introdotto il concetto di una data indipendente dal fuso orario su tutti i valori effettivi del progetto. Un nuovo campo, **Data transazione**, è ora disponibile nelle righe del giornale di registrazione e nei valori effettivi e verrà usato per memorizzare la data in cui si è verificata la transazione, ma senza convertire tale data in Coordinated Universal Time. Questa data verrà usata per i processi a valle come l'impostazione automatica del prezzo e la creazione di fatture. | <p>[Determinare i tassi di costo per stime e valori effettivi basati su progetto](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Determinare i prezzi di vendita per stime e valori effettivi basati su progetto](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Prezzi e fatturazione | **Sostituzioni del prezzo alla data di validità in Project Operations**<br>Sostituzioni prezzo data di validità fornisce un modo per ignorare o modificare prezzi specifici nel listino prezzi. | [Sostituzioni prezzo data di validità](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Conto lavoro | **Conto lavoro e riconciliazione delle fatture fornitore**<br>Questa funzionalità consente ai clienti di creare conti lavoro per acquisto di tempo delle risorse, categorie di spesa e materiali utilizzati per il lavoro di progetto. Permette inoltre ai clienti di registrare, nelle app per la finanza e le operazioni, le fatture fornitore che saranno disponibili per i project manager in Dataverse per la verifica. | <p>[Gestione dei conto lavoro](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Creare fatture fornitore](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Ore e spesa | **Responsabile approvatore globale**<br>Questa funzionalità consente l'approvazione centralizzata e del fornitore di software indipendente (ISV), indipendentemente dal progetto o dallo stato del membro del team nel progetto. | [Sicurezza e approvazioni](/dynamics365/project-operations/approvals/approvals-security) |
| Gestione spese | **Possibilità di registrare la passività di spesa nella valuta del fornitore**<br>Questa funzionalità permette di registrare le note spese in una valuta del fornitore per il metodo di pagamento in contanti. | [Possibilità di registrare la passività di spesa nella valuta del fornitore](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Approvvigionamento di progetti | **Pagamenti del fornitore con pagamento su pagamento**<br>Questa funzionalità consente di usare la funzionalità Pagamento su pagamento (PWP) con ambienti non di magazzino di Project Operations. Permette di bloccare/trattenere i pagamenti ai fornitori, in base a termini di ritenuta, fino al ricevimento del pagamento da parte del cliente. | [Pagamenti del fornitore con pagamento su pagamento](/dynamics365/project-operations/procurement/pay-when-paid) |
| Approvvigionamento di progetti | **Richieste di acquisto di progetto**<br>Questa funzionalità consente agli utenti di creare ordini di acquisto correlati al progetto in persone giuridiche in cui è abilitata l'integrazione di Project Operations on Dynamics 365 Customer Engagement. Gli ordini di acquisto del progetto possono essere usati per registrare l'approvvigionamento di materiale non stoccato a fronte del progetto per i singoli utenti tipo del reparto acquisti. Gli ordini di acquisto del progetto non verranno sincronizzati con Dataverse. Tuttavia, puoi usare un'entità virtuale per visualizzare le righe dell'ordine di acquisto del progetto in Dataverse per informazioni sul project manager. Il costo della fattura fornitore relativo al progetto è integrato con l'entità Valori effettivi di progetto in Dataverse. Il costo del progetto viene registrato nel giornale di registrazione secondario usando il giornale di integrazione di Project Operations. | |
|Pianificazione e rilevamento dei progetti|**Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione** </br> </br>L'API di modifica del contorno dell'assegnazione delle risorse consente agli sviluppatori di specificare a livello di codice il lavoro di un assegnatario di attività in qualsiasi intervallo di date supportato per una pianificazione più dettagliata del lavoro in fasi temporali.|[Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

La tabella seguente mostra le mappe a doppia scrittura che sono state modificate o aggiunte nella versione di Project Operations di settembre 2022.

| Mapping entità | Versione aggiornata | Commenti |
| -------------- | ------------------- | ------------|
| Valori effettivi dell'integrazione di Project Operations (msdyn_actuals) | 1.0.0.15 | Questa mappa supporta l'elaborazione dei valori effettivi del conto lavoro con Project Operations per gli scenari basati sulle risorse. |
| Entità di esportazione fattura fornitore progetto integrazione Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Questa mappa supporta l'elaborazione dei valori effettivi del conto lavoro con Project Operations per gli scenari basati sulle risorse. |
| Entità di esportazione riga fattura fornitore progetto integrazione Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Questa mappa supporta l'elaborazione dei valori effettivi del conto lavoro con Project Operations per gli scenari basati sulle risorse. |

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Prezzi e fatturazione | 2754422 | Le stime di materiali e spese non vengono inviate a Finance quando i progetti vengono copiati in Dataverse. |
| Ore e spesa | 2787409 | Un responsabile approvazione non valido può approvare una voce di tempo non di progetto. |
| Gestione delle opportunità | 2788907 | Messaggio di errore aggiornato sulla convalida dell'univocità per le righe ordine che includono flag. |
| Ore e spesa | 2842253 | Gestione delle eccezioni null per l'approvazione del tempo. |
| Prezzi e fatturazione | 2844181 | Il mancato ottenimento dell'ID di correlazione blocca la creazione della fattura. |
| Prezzi e fatturazione | 2876628 | QLD, CLD: la stima della risoluzione del listino prezzi deve usare i campi dell'intervallo di date legacy del listino prezzi. |
| Conto lavoro | 2893222 | Se non viene specificato alcun ruolo per una riga del conto lavoro, dovrebbe essere possibile selezionare quella riga su un membro del team per qualsiasi ruolo. |

### <a name="project-management-and-accounting-in-finance"></a>Contabilità e gestione dei progetti in Finance

Per informazioni sulle correzioni di bug incluse in questo aggiornamento, accedi a Microsoft Dynamics Lifecycle Services e visualizza [l'articolo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funzionalità attivate per impostazione predefinita nella prossima versione

Questa tabella elenca le funzionalità attivate per impostazione predefinita nella versione 10.0.30. La maggior parte delle funzionalità che sono state attivate automaticamente può essere disattivata in [Gestione funzionalità](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). In futuro, alcune funzionalità che sono state attivate automaticamente potrebbero essere rimosse da Gestione funzionalità e diventare obbligatorie. Questa modifica garantisce l'uso della funzionalità corrente da parte dei clienti, di modo che i miglioramenti possano essere basati sulla funzionalità corrente man mano che vengono aggiunti. Le funzionalità non verranno mai abilitate automaticamente in meno di un anno, a meno che non siano ritenute essenziali.

| Nome funzionalità | Data abilitazione | Funzionalità aggiunta | Stato funzionalità | Modulo |
| --- | --- | --- |--- |--- |
| Abilitare l'operazione asincrona quando l'utente deve passare dalle operazioni sincrone a quelle asincrone | 21 ottobre 2022 | 9 aprile 2021 | Attiva per impostazione predefinita | Gestione spese |
| Valutazione dei criteri di spesa per le entrate richieste | 21 ottobre 2022 | 20 Dicembre 2021 | Attiva per impostazione predefinita | Gestione spese |
| Visualizzazione dell'elenco delle note spese create mediante delega ai lavoratori | 21 ottobre 2022 | 19 febbraio 2020 | Attiva per impostazione predefinita | Gestione spese |
| Calcolo delle indennità di trasferta totali per anno fiscale | 21 ottobre 2022 | 10 Maggio 2022 | Attiva per impostazione predefinita | Gestione spese |
