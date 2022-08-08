---
title: Novità o modifiche in Project Operations, ottobre 2021 per scenari basati su materiali stoccati/produzione
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di ottobre 2021 di Project Operations per scenari basati su materiali stoccati/produzione.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029948"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novità o modifiche in Project Operations, ottobre 2021 per scenari basati su materiali stoccati/produzione

_**Si applica a:** Project Operations per scenari basati su materiali stoccati/produzione_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.22
 
## <a name="quality-updates"></a>Aggiornamenti di qualità

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
|--------------|------------------|----------------|
| Contabilità e gestione dei progetti | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Gli importi del semilavorato (WIP, Work in Process) del progetto e dei ricavi sospesi non vengono stornati correttamente quando viene registrata una fattura cliente interaziendale. |
| Contabilità e gestione dei progetti | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | La funzionalità **Impedisci la chiusura del progetto se esistono transazioni aperte** non funziona. |
| Contabilità e gestione dei progetti | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | La classificazione della priorità di pagamento su una fattura a testo libero non viene compilata automaticamente nelle dimensioni dei progetti quando tale funzionalità è abilitata. |
| Contabilità e gestione dei progetti | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Negli scenari non interaziendali gli importi del semilavorato (WIP, Work in Process) e dei ricavi sospesi non vengono stornati correttamente quando la fattura del progetto viene registrata. |
| Contabilità e gestione dei progetti | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | I valori Dare e Avere vengono scambiati quando il componente aggiuntivo Microsoft Excel viene usato con il giornale di registrazione spese di progetto e il campo **Tipo di conto di contropartita** è impostato su **Progetto**. |
| Contabilità e gestione dei progetti | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | L'importo registrato nelle transazioni di progetto è sopravvalutato in un ordine fornitore del progetto che include articoli stoccati e che ha importi delle imposte non deducibili quando **UseTax** è contrassegnato. |
| Contabilità e gestione dei progetti | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Il sistema suddivide l'importo tra i report di profitti e perdite del progetto e i report WIP del progetto. |
| Contabilità e gestione dei progetti | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Le scorte disponibili non sono corrette dopo la rettifica di una richiesta di articoli parzialmente restituiti. |
| Contabilità e gestione dei progetti | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | I nomi delle risorse vengono duplicati in Project Operations quando vengono modificati in Microsoft Project. |
| Contabilità e gestione dei progetti | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Le note spese interaziendali con i costi della fattura di fornitori interaziendali in sospeso per la contabilità fornitori vengono prima registrati nel tipo di pubblicazione **Costo del progetto WIP**. Durante l'elaborazione i costi relativi alla stima vengono tuttavia registrati nel tipo di registrazione **Costo progetto** anziché in **Costi interaziendali**. |
| Contabilità e gestione dei progetti | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | I risultati della ritenuta di garanzia del fornitore nelle transazioni di spesa del progetto non vengono mostrati. |
| Contabilità e gestione dei progetti | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Il foglio presenze deve arrotondare l'importo della transazione nella valuta della transazione a un numero specificato di posizioni decimali su tutte le distribuzioni contabili e nelle voci di allocazione di registrazioni C/G. |
| Contabilità e gestione dei progetti | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Le quantità delle richieste di articoli del progetto vengono aggiornate automaticamente quando gli ordini pianificati vengono confermati. |
| Contabilità e gestione dei progetti | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Il numero di giustificativo, il saldo del fornitore del tipo di transazione e il numero di conto non possono essere stornati nella fattura di pagamento anticipato di un ordine fornitore. |
| Contabilità e gestione dei progetti | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La fattura fornitore interaziendale viene interrotta quando l'integrazione della fattura fornitore è attivata. |
| Contabilità e gestione dei progetti | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Quando si crea un giornale di registrazione spese di progetto, l'importo del costo viene mostrato nel campo **Credito**. |
| Contabilità e gestione dei progetti | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Le condizioni di pagamento sulle fatture del progetto non funzionano come previsto. |
| Contabilità e gestione dei progetti | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | I giustificativi foglio presenze potrebbero essere riusati quando la sequenza numerica è impostata come continua. |
| Contabilità e gestione dei progetti | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIA. La logica **Importo ritenuta manuale** non corrisponde alla logica **Importo ritenuta automatico** nella proposta di fatturazione del contratto di progetto. |
| Contabilità e gestione dei progetti | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quando viene rilasciata la ritenuta fornitore, la registrazione del giustificativo presenta righe aggiuntive non corrette. |
| Contabilità e gestione dei progetti | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Quando il campo **Data fattura** nella pagina **Crea proposta di fatturazione** viene modificato, potrebbe verificarsi il seguente errore: "Riferimento all'oggetto non impostato su un'istanza dell'oggetto". |
| Contabilità e gestione dei progetti | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Si verifica un errore quando si tenta di approvare un foglio presenza dal flusso di lavoro **TSLine** ed esistono criteri foglio presenze per sabato e domenica. |
| Contabilità e gestione dei progetti | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Il tipo di elemento del progetto di saldo iniziale è escluso da **Riepiloghi transazioni di proposte di fatturazione** quando viene calcolato il totale della fattura della proposta di fatturazione. |
| Contabilità e gestione dei progetti | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Se il costo del consumo in un ordine di produzione del progetto è 0 (zero), si verifica il seguente errore quando si tenta di eseguire la stima: "Tentativo di divisione per zero". |
| Contabilità e gestione dei progetti | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | L'app per dispositivi mobili Project Timesheet per Android non risponde. Il problema è correlato a **TimeEntryDataManager ArgumentNullException**. |
| Contabilità e gestione dei progetti | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Il giornale di registrazione di integrazione Project Operations restituisce un errore quando viene contabilizzato, perché mancano le dimensioni per un account. L'account per cui mancano le dimensioni non è tuttavia l'account in cui si esegue la registrazione. |
| Contabilità e gestione dei progetti | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Il filtro **ToDate** nelle ricerche non viene cancellato quando viene rimosso dalla finestra di dialogo **Selezione** nella pagina **Registra costo**. |
| Contabilità e gestione dei progetti | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Ripristina tutta la distribuzione** non riesce e restituisce un errore per i fogli presenze creati per un progetto di tipo **Solo ora**. |
| Contabilità e gestione dei progetti | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | La scheda **Progetto** non è modificabile su una fattura fornitore in sospeso quando la categoria di approvvigionamento è assegnata all'articolo. |
| Contabilità e gestione dei progetti | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Il riquadro di spostamento non è disponibile se non hai effettuato l'accesso a Project Operations Dataverse. |
| Contabilità e gestione dei progetti | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Per le transazioni di rettifica del progetto interaziendale, sono presenti problemi nella società di destinazione. |
| Contabilità e gestione dei progetti | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | I costi impegnati per un progetto calcolano la quantità e il prezzo di costo errati se l'ordine fornitore è stato elaborato tramite **Elaborazione di fine anno ordini fornitore** in contabilità generale. |
| Contabilità e gestione dei progetti | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Quando un ordine di produzione del progetto con ordini di qualità è dichiarato finito, si verifica il seguente errore: "Nessuna transazione virtuale contrassegnata con transazione di magazzino". |
| Contabilità e gestione dei progetti | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Quando viene registrata una fattura della contabilità fornitori relativa al progetto, si verifica il seguente errore: "Testo enumerato Progetto - costo - articolo non esiste". |
| Contabilità e gestione dei progetti | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | I costi indiretti vengono raddoppiati quando si accumulano manualmente i ricavi. |
| Contabilità e gestione dei progetti | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Ricavi sospesi e registrazione WIP non producono transazioni. |
| Contabilità e gestione dei progetti | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | L'attivazione del prezzo in sospeso non riesce per un articolo di costo standard quando esiste un ordine fornitore del progetto ricevuto. |
| Contabilità e gestione dei progetti | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Il valore WIP stornato da una registrazione della fattura è diverso dal valore WIP registrato originale da un inserimento ora. |
| Contabilità e gestione dei progetti | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Si tratta di un problema di registrazione dei ricavi fatturati del progetto nei casi di ritenuta applicati in cui le transazioni su giustificativo non vengono bilanciate. |
| Contabilità e gestione dei progetti | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La creazione di una stima dopo la registrazione di una proposta di fattura blocca l'importazione delle righe di correzione in Project Operations. |
| Contabilità e gestione dei progetti | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Non dovrebbe essere possibile modificare un record dei passaggi fondamentali fatturato. |
| Contabilità e gestione dei progetti | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Quando vengono usati gli addebiti automatici, non è possibile registrare la fattura cliente interaziendale per un foglio presenze e viene visualizzato un messaggio di errore. |
| Contabilità e gestione dei progetti | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | L'indirizzo in un sottoprogetto non è aggiornato correttamente. |
| Contabilità e gestione dei progetti | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Il prezzo di costo nei fabbisogni di articoli viene aggiornato con il prezzo di acquisto per gli ordini fornitore consolidati. |
| Contabilità e gestione dei progetti | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Il costo registrato non è corretto dopo che il prezzo di acquisto è stato aggiornato e il parametro **Attiva gestione modifiche** è abilitato. |
| Viaggi e spese | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Tutte le spese dell'utente sono visibili quando si cerca una categoria nell'app per dispositivi mobili Gestione spese. |
| Viaggi e spese | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Gli importi non corretti sulle transazioni IVA e fornitori vengono registrati da una spesa creata da una transazione con carta di credito. |
| Viaggi e spese | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Un messaggio di avviso irrilevante viene visualizzato quando si aggiornano le pagine delle note spese. |
| Viaggi e spese | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Il responsabile approvazione provvisorio errato viene usato quando si elimina un responsabile approvazione provvisorio e quindi si esegue di nuovo l'invio tramite il flusso di lavoro. |
| Viaggi e spese | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Si verifica un errore di registrazione correlato all'impostazione del chilometraggio. |
| Viaggi e spese | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | La distribuzione non aggiorna la persona giuridica quando una transazione non collegata viene aggiunta nuovamente alla nota spese su una spesa interaziendale. |

### <a name="regulatory-updates"></a>Aggiornamenti normativi

Per informazioni sugli aggiornamenti normativi per le app per la finanza e le operazioni, vedi [Aggiornamenti normativi](/dynamics365/finance/localizations/regulatory-updates). È anche possibile accedere a Microsoft Dynamics Lifecycle Services (LCS) e usare lo strumento Ricerca argomento per visualizzare gli aggiornamenti normativi pianificati. Ricerca argomento consente di cercare per paese o area geografica, tipo di funzionalità e versione.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
