---
title: Novità di giugno 2021 - Project Operations per scenari di risorse/materiali non stoccati
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di giugno 2021 di Project Operations per scenari di risorse/materiali non stoccati.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c6a40335df89cc6b2bb35e54832140aac6eb9ac6
ms.sourcegitcommit: 03414a74ddf1f2d63043d734ebdee7485f1aadd2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679214"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di giugno 2021 - Project Operations per scenari di risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

- Project Operations in ambiente Dynamics 365 Dataverse versione 4.11.0.156 o 4.11.0.164.
- Gestione di progetti e contabilità nella versione degli ambienti delle app Finance and Operations 10.0.19.

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- Possibilità di eliminare le [righe proposta fattura di progetto per scenari di rettifica](../invoicing/correct-project-invoice-proposals.md).
- Le righe di spesa dettagliate riflettono i nomi delle sottocategorie nella nota spese [Note spese reinventate: nuove funzionalità](../expense/expense-reports-reimagined.md#new-features).
- Il metodo di pagamento è disponibile nel nuovo riquadro delle spese quando si crea una nuova spesa.
- Disponibilità generale delle API di pianificazione del progetto. Questa nuova funzionalità consente ai clienti di eseguire in modo programmatico operazioni di creazione, aggiornamento ed eliminazione su attività di progetto, assegnazioni di risorse, dipendenze di attività e record di membri del team di progetto. Per ulteriori informazioni, vedi [Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Non sono disponibili aggiornamenti per le mappe a doppia scrittura di Project Operations in questa versione. 

Per un elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni della mappa a doppia scrittura di Project Operations](../environment/resource-dual-write-maps.md).

È necessario eseguire sempre la versione più recente della mappa nel proprio ambiente e abilitare tutte le mappe delle tabelle correlate durante l'aggiornamento della soluzione Project Operations Dataverse e della versione della soluzione delle app Finance and Operations. Alcune funzionalità e capacità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella pagina **Doppia scrittura** nella colonna **Versione**. Attiva una nuova versione della mappa selezionando **Versioni mappa della tabella**, selezionando la versione più recente, quindi salvando la versione selezionata. Se hai personalizzato una mappa di tabella predefinita, riapplica le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema con le colonne della tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi di scrittura doppia.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Prezzi e fatturazione | 2281417 | Risolto il problema relativo all'esito negativo dell'azione di creazione automatica della fattura tramite la pianificazione fatturazione. |
| Prezzi e fatturazione | 2287835 | Miglioramento delle prestazioni di conferma della fattura. |
| Gestione delle opportunità | 2222555 | L'addebito delle stime dei materiali deve essere copiato correttamente nei dettagli della riga del preventivo quando si utilizza **Importa da stima di progetto**. |
| Gestione delle opportunità | 2223427 | Le personalizzazioni sono ora consentite per l'azione **GenerateRetainersFromRetainerScheduleOptions**. |
| Gestione delle opportunità | 2277528 | Calcolo del valore fisso del passaggio fondamentale di fatturazione per righe di contratto di progetto con più clienti. |
| Pianificazione e rilevamento dei progetti | 2226110 | Risolto il problema intermittente con la funzione **Genera requisito** nella griglia **Team di progetto**. |
| Pianificazione e rilevamento dei progetti | 2208109 | Gli utenti non possono creare un progetto in una valuta con attività correlate in un'altra valuta. |
| Pianificazione e rilevamento dei progetti | 2258228 | L'elenco dei campi autorizzati alla modifica con le entità **Pianificazione** che utilizzano l'API di pianificazione sono state aggiornate. |
| Pianificazione e rilevamento dei progetti | 2293989 | La lingua e le impostazioni internazionali corrette devono essere trasmesse alla griglia **Attività di progetto**. |
| Gestione risorse | 2220493 | Risolto il problema con l'esperienza dell'utente nella griglia **Attività** quando si contrassegna rapidamente una richiesta di risorse come completata. |
| Gestione risorse | 2330496 | Risolto il problema di caricamento della **Scheda di pianificazione**. L'aggiornamento della qualità è disponibile nella versione 4.11.0.164 |
| Ore e spesa | 2194431 | La griglia **Inserimento ore** deve onorare l'inizio della settimana come stabilito nelle **Impostazioni di sistema**. |
| Ore e spesa | 2277311 | Dopo aver eliminato il valore in una cella nella griglia **Inserimento ore** il cursore rimane nella griglia. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Contabilità e gestione dei progetti in Dynamics 365 Finance

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Contabilità e gestione dei progetti | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Note modulo** e **Configurazione modulo** non sono visibili nella **configurazione della gestione dei progetti** nelle persone giuridiche di Finance integrate con Project Operations. |
| Contabilità e gestione dei progetti | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | La descrizione predefinita per l'IVA è vuota quando il **tipo di registrazione** = **IVA** per i giustificativi fattura progetto. |
| Contabilità e gestione dei progetti | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Doppie transazioni vengono registrate quando viene utilizzata la fatturazione basata sull'attività in Dataverse con l'integrazione di Project Operations. |
| Contabilità e gestione dei progetti | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | La percentuale di completamento per il riconoscimento dei ricavi non è corretta quando si utilizza l'integrazione di Project Operations. |
| Contabilità e gestione dei progetti | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | L'accumulo di ricavi viene raddoppiato in una fattura fornitore in sospeso in uno scenario integrato di Project Operations. |
| Contabilità e gestione dei progetti | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Impossibile registrare il giornale di registrazione dell'integrazione quando la regola del profilo ricavi è impostata su **Configurazione dei gruppi**. |
| Contabilità e gestione dei progetti | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Non è possibile registrare una fattura di acquisto per ordini fornitore di progetto con righe con più unità di misura. |
| Contabilità e gestione dei progetti | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | La dimensione finanziaria predefinita in un progetto non può essere aggiornata utilizzando l'entità dati **Progetti V2**. |
| Contabilità e gestione dei progetti | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Il processo batch per creare le stime di progetto richiede troppo tempo per essere completato. |
| Contabilità e gestione dei progetti | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | L'eliminazione di un contratto elimina anche l'indirizzo associato al cliente. |
| Viaggi e spese | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | La condizione del flusso di lavoro di approvazione della nota spese non viene valutata correttamente. |
| Viaggi e spese | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Il criterio della nota spese non valuta correttamente l'ID progetto. |
| Viaggi e spese | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | L'azione **Dividi in personale per le transazioni di spesa interaziendale** non funziona correttamente. |
| Viaggi e spese | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Le giustificazioni di una riga di nota spese vengono accidentalmente eliminate quando vengono eliminate le richieste di viaggio. Ciò si verifica quando il recID della nota spese e della richiesta di viaggio coincidono. |
| Viaggi e spese | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Si verifica un problema nell'app per dispositivi mobili Spesa quando il campo **ID progetto** è richiesto nei criteri di nota spese. |
| Viaggi e spese | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Le spese interaziendali associate a un progetto non possono essere modificate. Viene visualizzato il seguente messaggio di errore "Riferimento all'oggetto non impostato su un'istanza di un oggetto". |
| Viaggi e spese | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Dopo la registrazione di una nota spese, la valuta e l'importo errati vengono elencati nella contabilità ausiliaria della banca. |
| Viaggi e spese | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Sono stati apportati miglioramenti alla funzione *Elimina transazioni con carta di credito*.  |
| Viaggi e spese | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | L'IVA inclusa in una nota spese non viene calcolata in modo coerente quando viene specificata una valuta di dichiarazione diversa in una persona giuridica. |
| Viaggi e spese | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Le prestazioni sono influenzate dall'aggiunta di una nuova spesa di viaggio in contanti. |
| Viaggi e spese | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Le regole dei criteri di spesa non vengono attivate in una nota spese. |
| Viaggi e spese | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Il caricamento di una nuova categoria condivisa utilizzando Data Management Framework rimuove tutte le sottocategorie per tutte le categorie condivise. |
| Viaggi e spese | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Quando si crea una riga di spesa e si seleziona una categoria, viene visualizzato il seguente messaggio di errore: "La combinazione di fascia IVA DOM e fascia IVA articoli STD non è valida". |
| Viaggi e spese | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Ci sono problemi di sincronizzazione nell'applicazione per dispositivi mobili Spesa. |
