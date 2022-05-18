---
title: Dettagli di intestazione per le fatture fornitore
description: Questo argomento spiega la funzionalità fornita nell'intestazione della fattura fornitore in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17be106d5486358ff0bbf011af3da26a4c85a274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575585"
---
# <a name="header-details-for-vendor-invoices"></a>Dettagli di intestazione per le fatture fornitore

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento spiega la funzionalità fornita nell'intestazione della fattura fornitore in Microsoft Dynamics 365 Project Operations.

Quando i project manager pianificano ed eseguono progetti, possono assumere terzisti e acquistare prodotti e servizi dai fornitori. Durante l'esecuzione di un progetto, i costi vengono sostenuti da servizi, materiali e categorie di spesa che vengono acquistati in subappalti con i fornitori. I fornitori fatturano questi costi ai progetti creando fatture fornitore.

La tabella seguente fornisce informazioni sui campi delle intestazioni delle fatture fornitore in Project Operations.

| Campo | Description | Impatto funzionale |
| --- | --- | --- |
| Name | Nome della fattura fornitore. | In tutti gli elenchi a discesa delle fatture fornitore, il nome della fattura fornitore è elencato nella prima colonna per facilitare l'identificazione della fattura fornitore. Per impostazione predefinita, quando viene creata una fattura fornitore da un conto lavoro, il campo **Nome** della fattura fornitore è impostato su un valore costituito dal nome del conto lavoro più la data corrente. |
| Description | Una breve descrizione dei servizi e dei prodotti fatturati nella fattura fornitore. | None |
| Fornitore | Il nome dell'azienda che fattura i prodotti e servizi. Questa società deve essere un record di conto che ha un tipo di relazione di **Venditore** o **Fornitore**. | <p>In base al fornitore selezionato, i valori predefiniti vengono inseriti automaticamente nei seguenti campi:</p><ul><li>Valuta</li><li>Listini prezzi</li><li>Condizioni di pagamento</li><li>Indirizzo pagamento</li></ul> |
| Conto lavoro | Un riferimento al conto lavoro per la fattura fornitore. | <p>In base al conto lavoro selezionato, i valori predefiniti vengono inseriti automaticamente nei seguenti campi:</p><ul><li>Valuta</li><li>Listini prezzi</li><li>Condizioni di pagamento</li><li>Indirizzo pagamento</li></ul><p>Il conto lavoro selezionato nell'intestazione della fattura fornitore viene immesso per impostazione predefinita nelle righe di fattura fornitore e non può essere modificato in tali righe.</p> |
| Data di fattura | La data per i costi effettivi che verranno creati al momento della conferma della fattura fornitore. | La data della fattura viene utilizzata anche per selezionare il listino prezzi di acquisto corretto dai listini prezzi allegati al relativo fornitore o dai parametri del progetto. |
| Motivo stato | Stato della fattura fornitore. | <p>Lo stato determina dove si trova la fattura fornitore nel processo aziendale e se può essere modificato. Ecco alcuni dei valori disponibili:</p><ul><li>**Bozza**: La fattura fornitore può essere modificata.</li><li>**Confermato** – La fattura fornitore è stata verificata e confermata. Le fatture fornitore in questo stato non possono essere modificate o eliminate.</li><li>**In corso** – La fattura fornitore è in corso di revisione. Le fatture fornitore in questo stato possono essere modificate o ma non eliminate.</li><li>**Annullato** – La fattura fornitore è stata annullata. Le fatture fornitore in questo stato non possono essere modificate o eliminate.</li></ul> |
| Valuta | La valuta in cui il fornitore fattura i prodotti e i servizi nella fattura fornitore. | In una fattura fornitore che fa riferimento a un conto lavoro, la valuta del conto lavoro viene inserita per impostazione predefinita come valuta della fattura fornitore. In una fattura fornitore che non fa riferimento a un conto lavoro, il valore predefinito viene inserito dal record del conto fornitore e può essere modificato. Dopo aver salvato una fattura fornitore, la valuta non può più essere modificata. |
| Unità contratto | La divisione dell'azienda che è responsabile della ricezione dei servizi e/o dei prodotti dal venditore. | None |
| Condizioni di pagamento | I termini di pagamento sulle fatture fornitore emesse. Il valore predefinito viene inserito automaticamente dal record di account del fornitore. | I termini di pagamento di un conto lavoro vengono copiati in tutte le fatture fornitore correlate al conto lavoro. I termini di pagamento possono essere aggiornati se la fattura fornitore ha lo stato **Bozza**. |
| Indirizzo pagamento | L'indirizzo del fornitore a cui devono essere inviati i pagamenti. Il valore predefinito viene inserito automaticamente dal record di account del fornitore. | L'indirizzo di pagamento di un conto lavoro viene copiato come indirizzo di pagamento in tutte le fatture fornitore create per il conto lavoro. L'indirizzo di pagamento può essere aggiornato se la fattura fornitore ha lo stato **Bozza**. |
| Subtotale | Se la fattura fornitore non contiene righe, inserisci il totale parziale della fattura al lordo delle imposte. Se la fattura fornitore contiene righe, questo campo è di sola lettura. In questo caso, l'importo visualizzato è l'importo del subtotale di tutte le righe di fattura fornitore. | None |
| Totale imposte | Se la fattura fornitore non contiene righe, inserisci il totale delle imposte nel conto lavoro. Se la fattura fornitore contiene righe, questo campo è di sola lettura. In questo caso, l'importo visualizzato è la somma degli importi delle imposte di tutte le righe di fattura fornitore. | None |
| Importo totale | Questo campo calcolato mostra l'importo totale della fattura fornitore, imposte incluse. | None |

> [!NOTE]
> I seguenti campi di una fattura fornitore non possono essere modificati dopo il salvataggio della fattura fornitore: **Fornitore**, **Conto lavoro**, **Valuta**, **Unità contratto**, e **Termini di pagamento**. Se sono richieste modifiche a questi campi in una fattura fornitore, è necessario eliminare la fattura fornitore e crearne una nuova.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
