---
title: Novità di febbraio 2022 - Project Operations per scenari basati su risorse/non stoccate
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di febbraio 2022 di Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600839"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di febbraio 2022 - Project Operations per scenari basati su risorse/non stoccate

*Si applica a: Project Operations per scenari basati su risorse/materiali non stoccati*

Questo argomento si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.28.0.120
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.24

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

- A partire da questa versione, puoi aggiungere fino a 300 membri del team a un singolo progetto. In precedenza, il limite al numero di membri del team era 150. Per altre informazioni, consultare l'articolo sui [limiti del progetto](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Aggiornamenti del mapping di doppia scrittura di Project Operations

L'elenco seguente mostra le mappe a doppia scrittura che sono state modificate o aggiunte nella versione Project Operations di febbraio 2022.

| Mapping entità | Versione aggiornata | Commenti |
| --- | --- | --- |
| Entità di esportazione delle spese di progetto di integrazione di Project Operations (msdyn\_expenses) | 1.0.0.3 | Estesa per la sincronizzazione dell'attività del progetto a Dataverse. |

Per l'elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni di mappe a doppia scrittura di Project Operations](../environment/resource-dual-write-maps.md).

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Determinazione dei prezzi e fatturazione | 2415109 | Il valore predefinito nel campo **Condizioni di pagamento delle operazioni** deve essere il record del cliente del contratto di progetto e il record della fattura proforma. |
| Determinazione dei prezzi e fatturazione | 2497369 | La correzione del materiale deve seguire il valore della data nei parametri **Correzione**. |
| Determinazione dei prezzi e fatturazione | 2498697 | Migliorata la configurazione di sicurezza per **Richiamo inserimento ore**. |
| Determinazione dei prezzi e fatturazione | 2513824 | Per gli scenari basati sulle risorse, l'ID della categoria di transazione non deve superare i 28 caratteri in Project Operations. |
| Determinazione dei prezzi e fatturazione | 2517455 | L'azione **Aggiorna transazioni riga di fattura** non deve essere attivata più volte contemporaneamente per la stessa fattura. |
| Determinazione dei prezzi e fatturazione | 2517465 | L'azione **Disattiva dettagli riga di fattura** è bloccata perché non è supportata. |
| Determinazione dei prezzi e fatturazione | 2556660 | Risolto il problema con il controllo della validità della data che viene eseguito sul listino prezzi allegato a un record di parametri di progetto. |
| Gestione delle opportunità | 2369202 | Corretta la logica di business che verifica che i listini prezzi con date di validità sovrapposte possano essere collegati allo stesso contratto di progetto. |
| Gestione delle opportunità | 2385965 | Corretto il comportamento sulla scheda **Clienti** della pagina **Contratto di progetto** quando si seleziona **Salva e chiudi**. |
| Tempistica e spesa | 2538503 | Un'attività di progetto deve essere disponibile nell'entità **Valori effettivi del progetto** dopo la registrazione di una nota spese. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestione progetti e contabilità in Dynamics 365 Finance

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Contabilità e gestione dei progetti | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Durante l'importazione delle note di credito fornitore, si verifica un errore. Il messaggio di errore indica: "L'importo della ritenuta non può essere superiore all'importo netto rimanente". |
| Contabilità e gestione dei progetti | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Se una proposta di fattura include transazioni di commissione con importo zero che sono vendite effettive non fatturate, la fatturazione non può essere eseguita. |
| Contabilità e gestione dei progetti | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Il costo registrato non è corretto dopo che il prezzo di acquisto è stato aggiornato e **Attiva gestione modifiche** è abilitato.|
| Contabilità e gestione dei progetti | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | La registrazione della stima per un progetto a prezzo fisso utilizza la valuta e l'importo errati nel giustificativo di stima, anche quando la funzionalità **Abilita la valuta del contratto di progetto per il calcolo della stima** è abilitata. |
| Contabilità e gestione dei progetti | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** non deve effettuare una chiamata per abilitare il rilevamento delle modifiche senza rilevare le eccezioni per le entità che dispongono di chiavi di configurazione non abilitate. |
| Contabilità e gestione dei progetti | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Il processo batch viene corretto quando vengono registrati più giornali di registrazione avanzati e si verifica un errore. |
| Viaggi e spese | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | A causa di un problema di liquidazione correlato agli anticipi di cassa sulle note spese, l'importo dell'imposta non è coperto come parte dell'anticipo di cassa. |
| Viaggi e spese | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Le informazioni sull'IVA non sono incluse nel report **Spese - Transazioni registrate**. |
| Viaggi e spese | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | La violazione dei criteri di spesa **Ricevute richieste** mostra erroneamente un avviso sulle note spese. |
| Viaggi e spese | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Una transazione di progetto non include l'IVA non recuperabile nell'importo totale delle vendite quando la transazione è il risultato di una spesa a chilometraggio. |
| Viaggi e spese | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Quando una riga dettagliata ha imposte, non è possibile modificare la data della riga di dettaglio e si verifica un errore di stato del documento di origine. |

## <a name="removed-and-deprecated-features"></a>Funzionalità rimosse e deprecate

L'argomento [Funzionalità rimosse o deprecate in Project Operations](removed-depreciated-features-project.md) descrive le funzionalità che sono state rimosse o deprecate per Dynamics 365 Project Operations.

- Una funzionalità rimossa non è più disponibile nel prodotto.
- Una funzionalità deprecata non si trova nella fase attiva di sviluppo e potrebbe essere rimossa in un aggiornamento futuro.

Nell'argomento verrà visualizzato un avviso di ritiro [Funzionalità rimosse o deprecate in Project Operations](removed-depreciated-features-project.md) 12 mesi prima della rimozione di qualsiasi funzionalità dal prodotto.

Per le modifiche significative che influiscono solo sui tempi di compilazione, ma che sono binari compatibili con sandbox e ambienti di produzione, il tempo di deprecazione sarà inferiore a 12 mesi. In genere, si tratta di aggiornamenti funzionali che è necessario apportare al compilatore.
