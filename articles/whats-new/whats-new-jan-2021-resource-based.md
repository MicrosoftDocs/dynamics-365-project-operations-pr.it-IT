---
title: Novità di gennaio 2021 - Project Operations per scenari basati su risorse/materiali non stoccati
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di gennaio 2021 di Project Operations per scenari basati su risorse/materiali non stoccati.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 4b335503139964d9d0747f9ce7addc033a512f30
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029582"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di gennaio 2021 - Project Operations per scenari basati su risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_


Questo articolo si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

  - Project Operations in ambiente Dataverse versione 4.6.0.154
  - Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.16

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| **Distribuzione e configurazione** | 2106818 | Risolto il problema con la ridenominazione della risorsa web che causava problemi relativi alla personalizzazione di una pagina. |
| **Prezzi e fatturazione** | 2091908 | Risolta la visibilità delle opzioni **Blocca prezzi** e **Usa prezzo corrente** nella pagina **Fattura** quando Project Operations viene installato insieme a Dynamics 365 Field Service. |
| **Prezzi e fatturazione** | 2103058 | Aggiornati i **Totali di progetto** per gestire i valori nulli per il costo effettivo di un'attività. |
| **Prezzi e fatturazione** | 2116100 | Messaggi di errore migliorati utilizzati con la funzionalità, **Voci corrette su valori effettivi**. |
| **Prezzi e fatturazione** | 2116129 | Migliore visibilità delle stime di spesa nella scheda **Stime** della pagina **Progetti**. |
| **Prezzi e fatturazione** | 2119112 | L'aggregazione fissa delle vendite effettive e del costo effettivo quando tassi di cambio diversi vengono utilizzati. |
| **Prezzi e fatturazione** | 2134705 | Corretto l'errore "Impossibile leggere la proprietà **getResourceString** di non definito"quando la pagina **Fattura** viene visualizzata e viene installato Field Service. |
| **Gestione delle opportunità** | 2022195 | La griglia di fatturazione basata su attività nella pagina **Progetto** include un'icona che indica che c'è un contratto o una riga di offerta collegata a quell'attività. |
| **Gestione delle opportunità** | 2029135 | È stato risolto l'errore del processo aziendale che si verifica quando un utente tenta di aprire una riga di fattura su una fattura confermata con un importo anticipato fatturato. |
| **Gestione delle opportunità** | 2040713 | Risolto l'errore di script che si verifica durante la creazione di una fattura da un contratto e Field Service è installato. |
| **Pianificazione e rilevamento dei progetti** | 2090202 | Regole aziendali contrassegnate che non vengono più utilizzate come **Deprecato**. |
| **Ore e spesa** | 2091249 | Controlli rafforzati in modo che gli utenti non possano modificare l'attività su un inserimento ore inviato o approvato. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestione progetti e contabilità in Dynamics 365 Finance

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| **Contabilità e gestione dei progetti** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Importo del contratto errato sulla pagina **Sul conto** per un progetto a prezzo fisso con più fonti di finanziamento. |
| **Contabilità e gestione dei progetti** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Il segnaposto **Invoiceproposal.PSAnfRefProjId** non mostra l'ID progetto per il flusso di lavoro, **Rivedi le proposte di fatturazione del progetto**. |
| **Contabilità e gestione dei progetti** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | La data di sconto di cassa errata viene utilizzata durante la registrazione delle proposte di fattura del progetto. |
| **Contabilità e gestione dei progetti** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | La rimozione e la lettura delle assegnazioni di risorse in Project Operations raddoppiano le voci di previsione del progetto in Finance. |
| **Contabilità e gestione dei progetti** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | In Project Operations, non è possibile creare stime di progetto in Dataverse senza avere una riga di contratto sul progetto. |
| **Contabilità e gestione dei progetti** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | La dimensione finanziaria in una transazione di spesa di progetto non è sincronizzata con il giustificativo correlato e con la distribuzione contabile della nota spese quando i costi vengono registrati in Saldo. |
| **Contabilità e gestione dei progetti** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Il filtro **Stato fattura** per lo stato della fattura nelle transazioni di progetto registrate per i progetti a prezzo fisso non funziona. |
| **Contabilità e gestione dei progetti** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | L'eliminazione della stima stornata non funziona nella sezione **Periodico**. |
| **Contabilità e gestione dei progetti** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Le righe di proposta di fattura possono essere eliminate in Project Operations se integrate con Dataverse. |
| **Contabilità e gestione dei progetti** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Evita l'abilitazione della funzione righe di contratto multiple senza l'integrazione di Dataverse. |
| **Contabilità e gestione dei progetti** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Quando la fatturazione in acconto è uguale a profitti e perdite, i ricavi fatturati sono elencati come zero nella pagina Stime. |
| **Contabilità e gestione dei progetti** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Le correzioni delle fatture non funzionano in ambienti integrati. |
| **Contabilità e gestione dei progetti** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Quando si registra WIP: il valore delle vendite nella fatturazione del progetto interaziendale viene selezionato un conto errato. |
| **Contabilità e gestione dei progetti** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | In Project Operations, le dipendenze dalle attività di stima in Dataverse non può essere aggiornato. |
| **Contabilità e gestione dei progetti** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | L'eliminazione ripetuta dei giornali di integrazione Project Operations in Finance porta alla perdita di dati. |
| **Contabilità e gestione dei progetti** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Il seguente errore si verifica durante la registrazione di una proposta di fattura di progetto, "La transazione non viene distribuita sulla valuta di rendicontazione quando viene aggiunta la fattura anticipata detratta". |
| **Contabilità e gestione dei progetti** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | L'ID progetto errato viene incluso nelle detrazioni dopo l'aggiornamento del contratto di progetto predefinito in Project Operations. |
| **Contabilità e gestione dei progetti** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | La stima e il riconoscimento dei ricavi non possono essere completati quando Project Operations è abilitato. |
| **Contabilità e gestione dei progetti** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | In Project Operations, la rimozione di un progetto da un contratto non reimposta il progetto predefinito nel contratto. |
| **Contabilità e gestione dei progetti** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | In Project Operations, in una fattura interaziendale, le righe di spesa errate vengono visualizzate nell'elenco **Aggiungi riga**. |
| **Viaggi e spesa** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Le righe di spesa non possono essere registrate perché l'impostazione dell'ora manca nella riga del contratto. |
| **Viaggi e spesa** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Quando la convalida progetto/categoria è obbligatoria, le categorie di spesa associate al progetto non sono visibili nella nota spese. |
| **Viaggi e spesa** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Il saldo dell'anticipo in contanti non viene aggiornato quando una nota spese viene registrata per riga. |
| **Viaggi e spesa** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Il processo **Aggiorna informazioni di pagamento** non riesce dopo lo storno delle liquidazioni in cui una fattura è stata liquidata con due o più transazioni di pagamento. |
| **Viaggi e spesa** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Si verifica un problema con il calcolo della riduzione del pasto dell'ultimo giorno per la categoria di spesa giornaliera. |
| **Viaggi e spesa** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Il report **Tipo di spesa per dipendente** non mostra le spese dettagliate se la prima connessione di un utente era nella lingua es-MX. |
| **Viaggi e spesa** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Il pagamento fornitore per una fattura nota spese utilizza il conto di riepilogo errato per la registrazione della liquidazione. |
| **Viaggi e spesa** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Quando una nota spese viene pubblicata con **Consenti raggruppamento di transazioni in base al conto di contropartita di pagamento** e **Correzione della data di contabilizzazione durante la registrazione** attivate, le date contabili non sono raggruppate nella tabella **Distribuzione contabile**, che influisce sui record IVA. |
| **Viaggi e spesa** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Il mapping della sottocategoria di spesa viene rimosso quando la casella di controllo Utilizza in spesa viene deselezionata e quindi selezionata di nuovo. |
| **Viaggi e spesa** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Non è possibile creare la nota spese interaziendale se l'ID progetto viene aggiunto a livello di testata. |
| **Viaggi e spesa** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Si verifica un problema di pagamento delle spese quando l'importo della spesa è superiore all'importo dell'anticipo in contanti. |
| **Viaggi e spesa** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Il campo **ID progetto** in una nota spese interaziendale sono vuote se il ruolo utente è assegnato a un'organizzazione specifica. |
| **Viaggi e spesa** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | La categoria di spesa viene bloccata quando si aggiunge una nuova riga di spesa. |
| **Viaggi e spesa** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | La richiesta di dettaglio delle righe di nota spese già suddivise restituisce un giustificativo contabilità fornitori\contabilità generale registrato incompleto. A causa della duplicazione di **TRVEXPTRANS.SOURCEDOCUMENTLINE** anche Esplora origine contabilità è danneggiato. |
| **Viaggi e spesa** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | L'indice aggiunto nella tabella **TRVREQUISITIONLINE** per la quale il cliente ha duplicati, genera un errore durante l'aggiornamento. |
| **Viaggi e spesa** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | In Project Operations, l'ora con attività interaziendali in Dataverse non può essere creato o approvato. |

## <a name="regulatory-updates"></a>Aggiornamenti normativi

Per informazioni sugli aggiornamenti normativi per le app per la finanza e le operazioni, vedi [Aggiornamenti normativi](/dynamics365/finance/localizations/regulatory-updates). È inoltre possibile accedere a LCS e visualizzare gli aggiornamenti normativi pianificati utilizzando lo strumento di ricerca dei problemi. La ricerca dei problemi ti consente di cercare per paese, tipo di funzionalità e versione.


[!INCLUDE[footer-include](../includes/footer-banner.md)]