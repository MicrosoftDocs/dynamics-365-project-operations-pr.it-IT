---
title: Novità o modifiche di Project Operations, luglio 2021 per scenari di materiali stoccati basati sulla produzione
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di luglio 2021 di Project Operations per scenari stoccati basati sulla produzione.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: fb1814330b5e474ccbda0ab85dd67758a6f270a9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334558"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Novità o modifiche di Project Operations, luglio 2021 per scenari di materiali stoccati basati sulla produzione

_**Si applica a:** Project Operations per scenari basati su materiali stoccati/produzione_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

- Gestione progetti e contabilità in ambiente Dynamics 365 Finance versione 10.0.20
 
### <a name="quality-updates"></a>Aggiornamenti di qualità
                                                                                                                                                                                  
| Area funzionalità                      | Numero di riferimento| Aggiornamento di qualità                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Contabilità e gestione dei progetti | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | I record di impegno di costo da una richiesta di acquisto vengono cancellati non appena l'ordine di acquisto viene rilasciato dall'emissione della richiesta di acquisto.                                                                           |
| Contabilità e gestione dei progetti | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | La convalida del budget avviene due volte su una richiesta di acquisto. Questa duplicazione significa che la richiesta non può essere chiusa e l'ordine fornitore corrispondente non viene creato.                                                                                                                        |
| Contabilità e gestione dei progetti | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | La regola di fatturazione **Percentuale da fatturare** non viene completata a causa di un problema di arrotondamento.                                                                              |
| Contabilità e gestione dei progetti | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Quando si rettifica la transazione e la percentuale ha i decimali, il costo e il prezzo di vendita non vengono rettificati correttamente.                                      |
| Contabilità e gestione dei progetti | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | L'explorer dell'origine contabile mostra le ore per una singola riga del foglio presenze per più righe ddel foglio presenze con attività diverse.                                      |
| Contabilità e gestione dei progetti | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Le visualizzazioni salvate e la personalizzazione dei dettagli della riga del foglio presenze fanno sì che il sistema apra sempre i dettagli per il primo foglio presenze nell'elenco quando si tenta di aprire un foglio presenze.  |
| Contabilità e gestione dei progetti | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Il nodo radice del progetto scompare e i record della struttura di suddivisione del lavoro vengono eliminati dopo l'importazione.                                                                                             |
| Contabilità e gestione dei progetti | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Quando gli articoli vengono ricevuti ed emessi parzialmente dal fabbisogno di articoli, il sistema aggiorna il saldo dell'utilizzo di budget errato. |
| Contabilità e gestione dei progetti | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Gli ordini di acquisto con conservazione del progetto non mostrano i totali correttamente nel riquadro **Totali** o nella griglia **Fattura in sospeso**.                                                                  |
| Contabilità e gestione dei progetti | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Quando si chiude l'inventario, le rettifiche dei costi degli articoli del progetto vengono registrate nel conto del saldo anziché nel conto profitti e perdite.                                                            |
| Contabilità e gestione dei progetti | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Un giustificativo di transazione registrato di progetto e un giustificativo di stima utilizzano USD come valuta contabile, ma l'importo mostra quale sarebbe l'equivalente CAD.              |
| Contabilità e gestione dei progetti | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | I costi impegnati con un fabbisogno articolo e un ordine di acquisto sono errati nel processo di fatturazione dell'ordine di acquisto con entrata prodotti parziale e fatturazione parziale.       |
| Contabilità e gestione dei progetti | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | La rettifica del progetto non aggiorna correttamente l'importo delle vendite con costi indiretti.                                                                                    |
| Contabilità e gestione dei progetti | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Nella tabella **Foglio presenze** manca una relazione definita con la visualizzazione **Lavoratore/Risorsa**.                                                                                   |
| Contabilità e gestione dei progetti | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Impossibile popolare il campo **Numero attività** quando lo selezioni dal menu a discesa per un foglio presenze interaziendale.                                                                 |
| Contabilità e gestione dei progetti | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Impossibile aggiungere un campo personalizzato **Scopo** o **Descrizione impegno** alle seguenti pagine: **Transazione registrata del progetto**, **Creazione proposta fattura**, o **Proposta di fattura**.  |
| Contabilità e gestione dei progetti | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Il controllo della data di consegna errata viene fornito quando si creano i requisiti dell'articolo utilizzando la gestione dei dati (**ProjSalesItemRequirementEntity**).                                              |
| Contabilità e gestione dei progetti | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Quando si seleziona un ID contratto di progetto in Finance, l'ambiente integrato Project Operations apre la pagina per creare un nuovo record, invece del contratto di progetto esistente.                                                                                                                 |
| Contabilità e gestione dei progetti | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  L'etichetta "@SYS4083080" ("Impossibile trovare un record lavoratore univoco corrispondente ai valori inseriti") non è tradotto in danese.                                |
| Contabilità e gestione dei progetti | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Il campo **Fascia IVA articolo** non è modificabile su una proposta di fattura.                                                                               |
| Contabilità e gestione dei progetti | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Il costo impegnato è sovrastimato con importi fiscali non deducibili.                                                                                                    |
| Contabilità e gestione dei progetti | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | La registrazione di un foglio presenze interaziendale con più progetti e dimensioni finanziarie diverse genera valori imprevisti nella contabilità generale.                             |
| Contabilità e gestione dei progetti | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Le righe della proposta di fattura sono duplicate a causa di più istanze di processo periodico, **Importa da staging** in esecuzione contemporaneamente.                                      |
| Contabilità e gestione dei progetti | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Si è verificato un errore nella registrazione della proposta di fattura della nota di credito, quindi le transazioni sul giustificativo non sono bilanciate.    |
| Contabilità e gestione dei progetti | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | I costi impegnati del progetto sono errati dopo il rilascio delle fatture in sospeso.                                                                             |
| Contabilità e gestione dei progetti | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Non è possibile creare una nota di credito per un ordine cliente di progetto quando l'imposta è in una valuta diversa da quella della società.                                      |
| Contabilità e gestione dei progetti | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | L'eliminazione di un contratto elimina anche l'indirizzo associato al cliente.                                                                                     |
| Contabilità e gestione dei progetti | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Impossibile registrare una proposta di fattura restituita da una correzione della transazione temporale negativa.                                                                    |
| Viaggi e spese                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | L'imposta viene calcolata in modo diverso nelle note spese.                                                                                                                  |
| Viaggi e spese                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | L'aggiornamento del rilascio **DB72_Expense.updateTrvExpTransProjTransId()** non permette a **trvExpTrans.ReferenceDataAreaId** di creare la nuova sequenza numerica.                    |
| Viaggi e spese                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | L'importo compilato non viene visualizzato con il campo obbligatorio.                                                                                                             |
| Viaggi e spese                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Miglioramenti nelle prestazioni per allegare una spesa alla nota spese utilizzando l'interfaccia utente Note spese riprogettate.                                                            |
| Viaggi e spese                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | È possibile eliminare le note spese registrate.                                                                                           |
| Viaggi e spese                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Il messaggio Criterio spese viene visualizzato più volte.                                                                                                       |
| Viaggi e spese                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Il campo **Metodo di pagamento** è incluso nel riquadro **Nuova spesa**.                                                                                                      |
| Viaggi e spese                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Lo strumento **Reimposta stato del documento di spesa** deve reimpostare lo stato della nota spese su **Bozza** se il flusso di lavoro non è stato trovato. 

### <a name="regulatory-updates"></a>Aggiornamenti normativi
Per informazioni sugli aggiornamenti normativi per le app Finance and Operations, vedi [Aggiornamenti normativi](/dynamics365/finance/localizations/regulatory-updates). Puoi anche accedere a Lifecycle Services (LCS) e visualizzare gli aggiornamenti normativi pianificati utilizzando lo strumento di ricerca dei problemi. La ricerca dei problemi ti consente di cercare per paese, tipo di funzionalità e versione.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
