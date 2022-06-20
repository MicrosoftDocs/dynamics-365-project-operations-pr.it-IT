---
title: Novità di marzo 2022 - Project Operations per scenari basati su risorse/non stoccate
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di marzo 2022 di Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910911"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di marzo 2022 - Project Operations per scenari basati su risorse/non stoccate

*Si applica a: Project Operations per scenari basati su risorse/materiali non stoccati*

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.30.0.99
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.25

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

Le diarie giornaliere sono ora supportate nella nuova e moderna alrea di lavoro per le spese riprogettata. Le aziende che utilizzano le diarie giornaliere possono abilitare questa funzione per offrire agli utenti un modo semplice per inviare ed essere rimborsati per le loro spese giornaliere. Per ulteriori informazioni, vedi [Spese giornaliere](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

L'elenco seguente mostra le mappe a doppia scrittura che sono state modificate o aggiunte nella versione Project Operations di marzo 2022.

| **Mapping entità** | **Versione aggiornata** | **Commenti** |
| --- | --- | --- |
| Entità di esportazione riga di fattura fornitore progetto integrazione Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Mapping aggiornati per allinearli all'entità riga di fattura fornitore in Dataverse. <br>Non attivare la versione del mapping 1.0.0.4. Sarà pronta per l'uso in combinazione con l'ambiente Finance versione 10.0.26 nel prossimo aggiornamento mensile. |

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Tempistica e spesa | 2388011 | Mostra i commenti di rifiuto ai mittenti di inserimenti ore durante l'approvazione in blocco. |
| Pianificazione e rilevamento dei progetti | 2495294 | I dettagli del progetto non devono essere modificabili sulla pagina **Dettagli attività**. |
| Determinazione dei prezzi e fatturazione | 2499605 | I passaggi fondamentali del contratto creati dai passaggi fondamentali dell'offerta vengono erroneamente contrassegnati come di sola lettura. |
| Pianificazione e rilevamento dei progetti | 2506050 | Il set di operazioni rimane in sospeso per un'ora se non ci sono modifiche da salvare. Il set viene quindi contrassegnato erroneamente come **non riuscito**, mentre dovrebbe essere completato immediatamente. |
| Determinazione dei prezzi e fatturazione | 2507401 | Le unità di contratto predefinite vengono immesse in modo errato nei progetti a causa di una memorizzazione nella cache errata. |
| Determinazione dei prezzi e fatturazione | 2541660 | **Convalida della creazione dell'ordine di vendita** in doppia scrittura deve essere solo per ordini basati su progetto. |
| Determinazione dei prezzi e fatturazione | 2552745 | L'imposta non viene suddivisa tra i clienti che hanno impostato regole di fatturazione divise. |
| Determinazione dei prezzi e fatturazione | 2558859 | Messaggi di errore migliorati per l'impostazione delle dimensioni dei prezzi. |
| Determinazione dei prezzi e fatturazione | 2558933 | **Importa da stime di progetto** non riesce quando **msdyn\_project** viene aggiunto come dimensione di prezzo. |
| Determinazione dei prezzi e fatturazione | 2559101 | L'eliminazione dei parametri di progetto non è bloccata e causa problemi. |
| Gestione delle opportunità | 2570390 | Il plug-in a doppia scrittura forza il tipo di conto su offerte, ordini e opportunità come **Cliente**, anche quando quel tipo di conto non è corretto. |
| Determinazione dei prezzi e fatturazione | 2586097 | I costi effettivi fatturati suddivisi non vengono stornati quando un progetto viene rimosso da una riga di contratto di progetto. |
| Determinazione dei prezzi e fatturazione | 2589619 | L'imposta sul materiale fuori catalogo viene propagata alle vendite effettive non fatturate e alla fattura. |
| Gestione delle opportunità | 2594015 | Un'offerta non può essere chiusa come acquisita per i clienti che hanno condizioni di pagamento **Net60**. |
| Pianificazione e rilevamento dei progetti | 2595841 | In Project for the Web, gli utenti ricevono un messaggio di errore su un **msdyn\_actualstart** mancante quando creano una nuova richiesta di risorse. |
| Ore e spesa | 2602511 | Il campo **Rifiutato da** per gli inserimenti ore mostra **Sistema** invece di un utente nominato come autore del rifiuto. |
| Ore e spesa | 2602528 | Un responsabile dell'approvazione del progetto può approvare il tempo sui progetti per i quali non è elencato come responsabile dell'approvazione. |
| Determinazione dei prezzi e fatturazione | 2608550 | Una fattura correttiva può essere confermata anche se non ci sono modifiche all'originale. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestione progetti e contabilità in Dynamics 365 Finance

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Contabilità e gestione dei progetti | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | C'è una discrepanza tra Finance e Project Operations nella lunghezza consentita del campo **ID categoria**. |
| Contabilità e gestione dei progetti | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | I progetti a prezzo fisso non possono essere eliminati quando il campo **Fatturazione acconti** è impostato su **Profitti e perdite** e il principio **Percentuale completata** viene usato. |
| Contabilità e gestione dei progetti | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Viene immessa una fascia IVA predefinita errata dall'impostazione del progetto nelle righe di spesa nel giornale di registrazione dell'integrazione Project Operations. |
| Contabilità e gestione dei progetti | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Non è possibile modificare le dimensioni dell'intestazione della proposta di fattura del progetto in una distribuzione integrata con Project Operations. |
| Contabilità e gestione dei progetti | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Le fatture fornitore interaziendali non devono essere integrate con Dataverse. |
| Contabilità e gestione dei progetti | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | C'è una mancata corrispondenza tra la valuta dei saldi cliente e la valuta di dichiarazione. |
| Contabilità e gestione dei progetti | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | È possibile registrare una fattura di progetto anche se il cliente è in attesa per tutte le fatture. |
| Contabilità e gestione dei progetti | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Il pulsante **Elimina tutte le righe** non è presente nelle proposte di fattura di progetto che hanno le viste **Intestazione** e **Righe**. |
| Contabilità e gestione dei progetti | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Quando registri una fattura fornitore, si verifica il seguente errore: "La data contabile per la fattura deve essere nello stesso anno contabile dell'ordine acquistato correlato. Esegui il processo di fine anno dell'ordine di acquisto o modifica la data nell'anno contabile corrente." |
| Viaggi e spese | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Il costo impegnato per un progetto non viene rilasciato dopo il rilascio del costo impegnato della richiesta di viaggio. |
| Viaggi e spese | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Il seguente errore si verifica quando si invia una nota spese "Analisi dello stack: la società non esiste." |
| Viaggi e spese | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | L'**ID progetto** predefinito non viene inserito nelle note spese quando il parametro **Richiedi attività per giornale di registrazione** è selezionato nel progetto. |
| Viaggi e spese | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Il pulsante **Registra spese** non funziona correttamente in Project Operations per scenari di risorse/non stoccate. |
| Viaggi e spese | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Si verifica un problema con **Tariffa per miglio** per una nota spese a chilometraggio che include i passeggeri. |
| Viaggi e spese | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Le tariffe a chilometraggio di spesa per i dipendenti non vengono sommate correttamente quando vengono utilizzati due diversi tipi di veicoli nella categoria di spesa **Livelli di tariffa per chilometraggio**. |
| Viaggi e spese | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | La ricerca del campo **Progetto** su una riga di richiesta di viaggio non restituisce l'elenco corretto dei progetti. |
| Viaggi e spese | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Chilometraggio in revisione** mostra un avviso sulle note spese. |
| Viaggi e spese | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Il servizio di riconoscimento ottico dei caratteri (OCR) della ricevuta non funziona a causa di un problema con l'URL del servizio OCR delle spese. |
| Viaggi e spese | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Quando la funzionalità **Possibilità di dettagliare rapidamente le spese ricorrenti** è abilitata, gli importi nelle righe di dettaglio delle note spese cambiano ogni volta che si apre la pagina **Dettaglia**. |
| Viaggi e spese | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Non è possibile eliminare una nota spese quando l'elenco provvisorio ha più di un approvatore. |

## <a name="removed-and-deprecated-features"></a>Funzionalità rimosse e deprecate

L'articolo [Funzionalità rimosse o deprecate in Project Operations](removed-depreciated-features-project.md) descrive le funzionalità che sono state rimosse o deprecate per Dynamics 365 Project Operations.

- Una funzionalità rimossa non è più disponibile nel prodotto.
- Una funzionalità deprecata non si trova nella fase attiva di sviluppo e potrebbe essere rimossa in un aggiornamento futuro.

Nell'articolo verrà visualizzato un avviso di ritiro [Funzionalità rimosse o deprecate in Project Operations](removed-depreciated-features-project.md) 12 mesi prima della rimozione di qualsiasi funzionalità dal prodotto.

Per le modifiche significative che influiscono solo sui tempi di compilazione, ma che sono binari compatibili con sandbox e ambienti di produzione, il tempo di deprecazione sarà inferiore a 12 mesi. In genere, si tratta di aggiornamenti funzionali che è necessario apportare al compilatore.
