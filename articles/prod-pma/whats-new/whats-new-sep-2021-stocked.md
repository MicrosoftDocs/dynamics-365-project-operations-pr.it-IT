---
title: Novità o modifiche in Project Operations, settembre 2021 per scenari di materiali stoccati basati sulla produzione
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di settembre 2021 di Project Operations per scenari basati su materiali stoccati/produzione.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 24de8626199a3ed56bb6703b78d746ff7a43a089
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582025"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novità o modifiche in Project Operations, settembre 2021 per scenari di materiali stoccati basati sulla produzione

_**Si applica a:** Project Operations per scenari basati su materiali stoccati/produzione_

Questo argomento si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.21
 
## <a name="quality-updates"></a>Aggiornamenti di qualità

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
|---|---|---|
| Contabilità e gestione dei progetti | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Se al ruolo di responsabile acquisti viene concesso l'accesso a una persona giuridica, tale ruolo ottiene anche l'accesso a tutti i progetti in tutte le persone giuridiche. |
| Contabilità e gestione dei progetti | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Si verifica un problema di arrotondamento dell'IVA mentre una nota di accredito viene liquidata a fronte di una fattura di progetto originale. |
| Contabilità e gestione dei progetti | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Uso di un budget di progetto alternativo per la verifica del budget. |
| Contabilità e gestione dei progetti | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Il gruppo di prezzi **Prezzo di vendita - Ora** non viene calcolato sulla struttura di suddivisione del lavoro per le offerte di progetto. |
| Contabilità e gestione dei progetti | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | L'eliminazione della stima non riesce quando la funzionalità **Abilita la valuta del contratto di progetto per il calcolo della stima** è abilitata. |
| Contabilità e gestione dei progetti | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | La fattorizzazione IVA per quantità viene aggiunta all'importo del prezzo di vendita quando l'imposta di utilizzo viene usata nella fascia IVA del giornale di registrazione spese di progetto. |
| Contabilità e gestione dei progetti | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | L'imposta condizionale non viene calcolata correttamente per l'ultimo pagamento quando la ritenuta fornitore e il pagamento anticipato sono stati applicati alle fatture dell'ordine di acquisto. |
| Contabilità e gestione dei progetti | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | La traccia di rettifica non funziona per i giornali di registrazione del saldo iniziale. |
| Contabilità e gestione dei progetti | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Allocazione revisione budget di progetto per periodo** è suddiviso in tutti i periodi di budget. Quando l'allocazione viene inviata, il record non viene cancellato. |
| Contabilità e gestione dei progetti | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Le registrazioni WIP nella contabilità generale hanno un importo errato. |
| Contabilità e gestione dei progetti | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | L'approvazione del giornale di registrazione ore del progetto non funziona. |
| Contabilità e gestione dei progetti | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Il prezzo di vendita di rettifica del progetto non viene aggiornato con i costi indiretti quando il limite di finanziamento non è contrassegnato. |
| Contabilità e gestione dei progetti | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Non è possibile creare una richiesta di articoli quando l'intestazione della tabella delle vendite viene fatturata e l'ordine di acquisto di supporto per le righe esistenti è stato finalizzato. |
| Contabilità e gestione dei progetti | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | L'importo della ritenuta per una regola di fatturazione che ha un'attività cardine per un progetto diverso non viene registrato nell'ID progetto corrispondente selezionato per l'attività cardine. Viene invece pubblicato con il primo progetto. |
| Contabilità e gestione dei progetti | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Quando selezioni **Set di dimensioni finanziarie** su una proposta di fatturazione, si verifica il seguente errore: "Impossibile eseguire il cast dell'oggetto di tipo 'Dynamics.AX.Application.FormIntControl' nel tipo 'Dynamics.AX.Application.FormStringControl'." |
| Contabilità e gestione dei progetti | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Il report **Fattura progetto** salta le righe. |
| Contabilità e gestione dei progetti | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Si verifica un errore quando si calcola il controllo dei costi per un progetto di investimento. |
| Contabilità e gestione dei progetti | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Il metodo **ProjTable::InitFromCustTable - canDeletePostalAddress** provoca un problema di prestazioni. |
| Contabilità e gestione dei progetti | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Il messaggio di errore dovrebbe essere più chiaro di "Errore imprevisto". |
| Contabilità e gestione dei progetti | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Il processo batch di registrazione della fattura di progetto elabora e registra la proposta di fattura anche se le righe della fattura non sono state generate. |
| Contabilità e gestione dei progetti | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Si verifica un problema di arrotondamento quando la chiave di configurazione della licenza del settore pubblico è disattivata. Viene generato un costo o un prezzo di vendita non corretto nelle ore del foglio presenze per i contratti che hanno più origini di finanziamento. |
| Contabilità e gestione dei progetti | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Il prezzo di vendita del progetto in un ordine di acquisto del progetto fatturato viene calcolato in modo errato quando il modello di prezzo di vendita è **Rapporto di contribuzione**. |
| Contabilità e gestione dei progetti | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Il sistema non considera i giorni attivi intermedi quando calcola la tariffa di manodopera effettiva per un dipendente. |
| Contabilità e gestione dei progetti | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Si verifica un errore di registrazione nel foglio presenze interaziendale a causa del seguente errore di convalida: "Nessun partner commerciale è configurato per la persona giuridica". |
| Contabilità e gestione dei progetti | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | La descrizione di un ordine fornitore con una categoria di spesa non viene recuperata nell'elenco delle transazioni di progetto registrate. |
| Contabilità e gestione dei progetti | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | È presente una conversione errata nei giornali di registrazione articoli registrati in un progetto. |
| Contabilità e gestione dei progetti | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Puoi confermare un ordine di acquisto anche se il limite di finanziamento è stato superato. |
| Contabilità e gestione dei progetti | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | La sezione **Correzione/Annulla fattura** su una fattura a testo libero scompare quando viene selezionato un ID progetto. |
| Contabilità e gestione dei progetti | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Si verificano problemi di prestazioni quando una proposta di fatturazione del progetto viene registrata da un ordine di vendita del progetto che include un articolo stoccato. |
| Contabilità e gestione dei progetti | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Impossibile registrare le fatture di acquisto del progetto perché si verifica il seguente errore: "La funzione AccDistProcessorProjectExtension.createForProjectRevenueLine è stata chiamata in modo errato". |
| Contabilità e gestione dei progetti | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Aggiornamento della creazione dei processi batch di stima del progetto per supportare l'esecuzione di più attività secondarie. |
| Contabilità e gestione dei progetti | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Lo stato di un foglio presenze non può essere aggiornato in **Bozza** quando il flusso di lavoro è bloccato in uno stato **Annullato**. |
| Contabilità e gestione dei progetti | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Gli importi della ritenuta non vengono calcolati nella proposta di fatturazione della nota di accredito se esistono più righe. |
| Contabilità e gestione dei progetti | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Quando si tenta di modificare l'importo su una fattura generata da un ordine di acquisto, si verifica il seguente errore: "Le transazioni su giustificativo non vengono bilanciate secondo XX/XX/XXXX. (valuta di contabilizzazione: 0,00 - valuta contabile: 0,01)". |
| Contabilità e gestione dei progetti | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Si verifica un problema di prestazioni quando una proposta di fatturazione del progetto viene registrata in modalità batch, a causa del join a **GeneralJournalAccountEntry**. |
| Contabilità e gestione dei progetti | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Si verificano problemi di prestazioni quando viene pubblicato un foglio presenze. |
| Contabilità e gestione dei progetti | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | La gerarchia delle stime dei costi della struttura di suddivisione del lavoro non viene allineata correttamente dopo che tutte le attività sono state espanse o dopo che una singola attività è stata espansa manualmente. |
| Contabilità e gestione dei progetti | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Il modello Excel di offerta di progetto non può essere aggiunto al menu **Apri in Excel**. |
| Contabilità e gestione dei progetti | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Il numero di esenzione fiscale per una persona giuridica non viene incluso in una fattura di progetto stampata. |
| Contabilità e gestione dei progetti | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Nessun dato finanziario viene aggiornato nell'errore dell'unità di magazzino quando un progetto viene rettificato in relazione alle linee di credito. |
| Contabilità e gestione dei progetti | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Dopo aver applicato la KB 461935, non è possibile pubblicare stime se si passa a sequenze numeriche continue. |
| Contabilità e gestione dei progetti | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** provoca la mancata risposta dell'app per dispositivi mobili del foglio presenze di progetto per Android. |
| Contabilità e gestione dei progetti | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Il valore WIP stornato da una registrazione della fattura è diverso dal valore WIP registrato in origine da un inserimento ora. |
| Contabilità e gestione dei progetti | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Nei casi di ritenuta applicati le transazioni su un giustificativo non vengono bilanciate quando i ricavi fatturati di un progetto vengono registrati. |
| Contabilità e gestione dei progetti | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Quando la funzionalità **Miglioramento delle prestazioni della pianificazione delle risorse di progetto** è abilitata, i valori decimali vengono arrotondati in modo errato per la disponibilità e la capacità delle risorse. |
| Contabilità e gestione dei progetti | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Quando la funzionalità **Crea stime di progetto usando più attività batch** è abilitata, la creazione delle stime in un batch con più attività secondarie funziona solo per il periodo corrente. |
| Viaggi e spese | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | I criteri di richiesta di viaggio vengono ignorati e il flusso di lavoro viene approvato senza errori. |
| Viaggi e spese | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>L'app per dispositivi mobili Gestione spese non salva le seguenti informazioni nella riga spese:</p><ul><li>ID del progetto</li><li>Se la spesa è fatturabile</li><li>Il numero di impegno</li></ul> |
| Viaggi e spese | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Il campo **Entrate collegate** è impostato su **Sì** anche se alla riga spese non è collegata una ricevuta. |
| Viaggi e spese | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Si verifica un errore quando si tenta di modificare la categoria di spesa in **Personale**. |
| Viaggi e spese | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Non è possibile collegare una ricevuta né modificare la spesa padre dopo che una transazione con carta di credito è stata suddivisa in una spesa personale. |
| Viaggi e spese | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | I criteri di spesa per le transazioni interaziendali con un ID progetto non funzionano correttamente. |
| Viaggi e spese | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Mancano le informazioni sulla data di registrazione per le note spese registrate. |
| Viaggi e spese | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Ci sono problemi con il metodo di pagamento nell'app per dispositivi mobili Gestione spese. |
| Viaggi e spese | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Una richiesta di viaggio creata per un lavoratore può essere usata per la nota spese di un altro lavoratore prima della data del delegato. |
| Viaggi e spese | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Quando si crea una spesa, le modifiche dei valori della dimensione finanziaria non vengono aggiornate correttamente a livello di distribuzione contabile nell'area di lavoro **Gestione delle spese**. |
| Viaggi e spese | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Lo stato di approvazione della riga spese principale non è sincronizzato con lo stato di approvazione del flusso di lavoro della riga dettagliata. |
| Viaggi e spese | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Si verifica un errore se si registra una nota spese e il recupero imposte è abilitato. |
| Viaggi e spese | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Un delegato non può eliminare i documenti di spesa per un dipendente licenziato. |
| Viaggi e spese | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | L'eliminazione di una riga spese richiede più tempo del previsto e ha impatto sulle prestazioni. |
| Viaggi e spese | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** provoca un record **TaxUncommitted** orfano perché è stato eliminato solo **SourceDocumentLine**. |
| Viaggi e spese | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** non rispetta **trvExpTrans.ReferenceDataAreaId** per creare la nuova sequenza numerica. |

## <a name="regulatory-updates"></a>Aggiornamenti normativi

Per informazioni sugli aggiornamenti normativi per le app per la finanza e le operazioni, vedi [Aggiornamenti normativi](/dynamics365/finance/localizations/regulatory-updates). È anche possibile accedere a Microsoft Dynamics Lifecycle Services (LCS) e usare lo strumento Ricerca argomento per visualizzare gli aggiornamenti normativi pianificati. Ricerca argomento consente di cercare per paese o area geografica, tipo di funzionalità e versione.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
