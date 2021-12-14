---
title: Novità di novembre 2021 - Project Operations per scenari basati su risorse/non stoccate
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di novembre 2021 di Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827331"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di novembre 2021 - Project Operations per scenari basati su risorse/non stoccate

*Si applica a: Project Operations per scenari basati su risorse/materiali non stoccati*

Questo argomento si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.26.0.145, 4.26.0.148 o 4.26.0.150
- Gestione del progetto e contabilità in un ambiente Dynamics 365 Finance versione 10.0.22

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- Le API del servizio di pianificazione del progetto supportano ora la possibilità di creare ed eliminare i bucket di progetto.

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Non sono disponibili aggiornamenti per le mappe a doppia scrittura di Project Operations in questa versione. Per un elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni della mappa a doppia scrittura di Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-in-dataverse"></a>Project Operations in Dataverse

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Prezzi e fatturazione | 2240080 | Il campo **Condizioni di pagamento** non deve essere duplicato sulla fattura proforma. |
| Prezzi e fatturazione | 2358236 | La correzione fattura deve consentire correzioni con righe a prezzo zero. |
| Gestione risorse | 2410072 | Consente la configurazione di una risorsa assegnata all'attività come project manager. |
| Prezzi e fatturazione | 2430234 | Risoluzione di un problema di calcolo delle prestazioni di costo. |
| Ore e spesa | 2436978 | Possibilità di immettere l'ora nel formato hh:mm. |
| Prezzi e fatturazione | 2448623 | Possibilità di aggiornare i listini prezzi dopo che sono stati associati a un'unità organizzativa. |
| Ore e spesa | 2460396 | Possibilità di eliminare un inserimento ore cancellando la cella. |
| Prezzi e fatturazione | 2467386 | Possibilità di eliminare un progetto con un'attività, anche quando l'attività è associata a un'offerta acquisita. |
| Ore e spesa | 2461744 | La visualizzazione **Approvazioni personali non riuscite** contiene solo le approvazioni di progetto nella fase **Inviato**. |
| Ore e spesa | 2464082 | Rimozione del collegamento dalle approvazioni del progetto nel set di approvazioni in caso di corrispondenza della stato di destinazione. |
| Ore e spesa | 2468108 | Il lavoro di pianificazione non deve impostare uno stato **Elaborazione** per il set di approvazione. |
| Ore e spesa | 2471503 | Eliminazione dei set di approvazione che risalgono a sette giorni prima. |
| Prezzi e fatturazione | 2480687 | Il riferimento alla riga dell'offerta non deve essere rimosso quando viene creato un passaggio fondamentale riga di offerta. |

### <a name="project-management-and-accounting-in-finance"></a>Contabilità e gestione dei progetti in Finance

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Contabilità e gestione dei progetti | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Gli importi dei fornitori non distribuiti nelle transazioni di spesa del progetto non vengono visualizzati nell'elenco delle transazioni. |
| Contabilità e gestione dei progetti | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La fattura fornitore interaziendale viene interrotta quando l'integrazione della fattura fornitore è attivata. |
| Contabilità e gestione dei progetti | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Le condizioni di pagamento sulle fatture del progetto non funzionano come previsto. |
| Contabilità e gestione dei progetti | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quando viene rilasciata la ritenuta fornitore, la registrazione del giustificativo presenta righe aggiuntive non corrette. |
| Contabilità e gestione dei progetti | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Quando il giornale di registrazione di integrazione di Project Operations viene contabilizzato, si verifica un errore a causa delle dimensioni mancanti per un account in cui non viene registrato. |
| Contabilità e gestione dei progetti | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | La scheda **Progetto** non è modificabile su una fattura fornitore in sospeso quando la categoria di approvvigionamento è assegnata all'articolo. |
| Contabilità e gestione dei progetti | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Il riquadro di spostamento non è disponibile se non hai effettuato l'accesso a Project Operations Dataverse. |
| Contabilità e gestione dei progetti | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Quando si registrano i ricavi da una fattura di progetto in un caso di ritenuta applicato, si verifica un problema perché le transazioni sul giustificativo non si bilanciano. |
| Contabilità e gestione dei progetti | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La creazione di una stima dopo la registrazione di una proposta di fatturazione impedisce l'importazione delle righe di correzione. |
| Contabilità e gestione dei progetti | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Non dovrebbe essere possibile modificare un record dei passaggi fondamentali fatturato. |
| Viaggi e spese | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Tutte le note spese sono visibili quando si cerca una categoria nell'app per dispositivi mobili Gestione spese. |
| Viaggi e spese | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Gli importi non corretti sulle transazioni IVA e fornitori vengono registrati da una spesa creata da una transazione con carta di credito. |
| Viaggi e spese | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Un avviso irrilevante si verifica quando si aggiorna la pagina **Nota spese**. |
| Viaggi e spese | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Il responsabile approvazione provvisorio errato viene usato quando si elimina un responsabile approvazione provvisorio e quindi si invia di nuovo una nota spese tramite il flusso di lavoro. |
| Viaggi e spese | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Si verifica un errore di registrazione correlato all'impostazione del chilometraggio. |
