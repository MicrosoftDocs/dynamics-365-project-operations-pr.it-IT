---
title: Impostazioni del contratto di progetto - semplice
description: Questo argomento fornisce informazioni sui campi che influiscono sulle righe del contratto e le informazioni sul contratto che vengono riepilogate in tutte le voci.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28dfb256eb75ca9484161f053969c205fcd60965
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180918"
---
# <a name="project-contract-settings---lite"></a>Impostazioni del contratto di progetto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento fornisce informazioni sui campi che si applicano all'intero contratto di progetto, comprese le impostazioni che influiscono su tutte le voci di contratto. Sono incluse anche le informazioni sul contratto che vengono riepilogate in tutte le voci per guidare i KPI del contratto di progetto.

La tabella seguente elenca i campi su un contratto di progetto che sono univoci per Dynamics 365 Project Operations o presentano alcune importanti modifiche nel comportamento rispetto agli ordini di vendita in Dynamics 365 Sales.

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| Digita | Scheda **Riepilogo** (nascosta) | Questo è un campo di set di opzioni con le seguenti opzioni:</br>- **Basato su lavoro** (disponibile solo quando è installato Project Operations)</br>- **Basato su articolo** (disponibile solo quando sono installati Project Operations e Sales)</br>- **Basato su manutenzione di servizio** (disponibile quando Dynamics 365 Field Service è installato ) | In Project Operations, il valore di questo campo predefinito è **Basato sul lavoro** e classifica il contratto come contratto basato su progetto. Un contratto deve essere basato su progetto per abilitare tutte le estensioni e funzionalità specifiche del progetto. |
| Potenziale cliente | Scheda **Riepilogo** | Il riferimento alla società o al record di account del cliente. Quando un contratto viene creato da un'offerta, questo campo viene copiato dal campo corrispondente nel record dell'offerta. | La valuta del contratto di progetto viene impostata in modo predefinito in base alla valuta del cliente. Questa impostazione può essere modificata prima di salvare il contratto. |
| Gestione account | Scheda **Riepilogo** | Il nome del responsabile della gestione account per questa transazione. Quando un contratto viene creato da un'offerta, questo campo viene copiato dal campo corrispondente nel record dell'offerta. | Il responsabile della gestione account è responsabile della gestione del rapporto con il cliente fino al completamento del progetto. In base al record della risorsa prenotabile collegato al responsabile della gestione account, l'unità contratto è predefinita nel contratto di progetto. |
| Unità contratto | Scheda **Riepilogo** | L'unità organizzativa responsabile della consegna dei progetti associati a questo contratto. Quando un contratto viene creato da un'offerta, questo campo viene copiato dal campo corrispondente nel record dell'offerta. | L'unità di contratto è la divisione dell'azienda che esegue i progetti. Ogni unità contratto ha una valuta e questa valuta viene utilizzata per riportare i costi stimati ed effettivi sostenuti durante il progetto. |
| Listino prezzi prodotto | Scheda **Riepilogo** | Questo listino prezzi viene utilizzato per i prezzi predefiniti nelle voci di contratto basate su prodotto. L'elenco a discesa delle opzioni per questo campo mostra un elenco di listini prezzi in cui la valuta del listino prezzi corrisponde alla valuta del contratto. Quando un contratto viene creato da un'offerta, questo campo viene copiato dal campo corrispondente nel record dell'offerta. Nel contratto di progetto, questo campo è predefinito in base al record di account ma può essere modificato. | Nessuna rilevanza downstream per questo campo. |
| Valuta | Scheda **Riepilogo** | La valuta utilizzata per indicare il valore di questa transazione e la valuta usata per fatturare al cliente. Quando un contratto viene creato da un'offerta, questo campo viene copiato dal campo corrispondente nel record dell'offerta. Nel contratto di progetto, questo campo è predefinito in base al record di account ma può essere modificato. | Dopo aver salvato un contratto, questo campo non è più modificabile. Il campo viene utilizzato per impostare in modo predefinito i listini prezzi dei prodotti e dei progetti nel contratto. La valuta del contratto viene utilizzata per corrispondere alla valuta del listino prezzi. |
| Limite da non superare | Scheda **Riepilogo** | Questo campo indica il limite massimo negoziato per il valore finale che il cliente accetta per questa transazione. | Il limite massimo viene valutato durante l'esecuzione ed è applicabile a tutte le voci e i progetti associati a questa transazione. |
| Data consegna richiesta | Scheda **Riepilogo** | Quando un contratto viene creato da un'offerta di progetto, questo campo viene copiato dal campo corrispondente nell'offerta di progetto. | Questa data viene utilizzata come data di fine per generare le pianificazioni di fatturazione. |

I seguenti KPI sono disponibili nella scheda **Prestazioni contratto** di un contratto di progetto.

| Campo | Ufficio | Descrizione |
| --- | --- | --- |
| Valore contratto | Contratto generale | Il valore totale del contratto di progetto. |
| Importo fatturato | Contratto generale | La somma degli importi su tutte le fatture relative a questo contratto. |
| Costi sostenuti | Contratto generale | La somma di tutti i costi effettivi registrati su tutti i progetti mappati al contratto. |
| Margine lordo | Contratto generale | Importo fatturato - Costo sostenuto fino alla data / Importo fatturato |
| Margine previsto | Contratto generale | (Valore del contratto - Costi stimati) / Valore del contratto Costi stimati = La somma di tutti i costi stimati su tutti i progetti associati al contratto.|
| Valore contratto | Righe basate su progetto | Valore della voce di contratto. |
| Importo fatturato | Righe basate su progetto | Per la voce di contratto a prezzo fisso: la somma degli importi su tutti i valori effettivi del passaggio fondamentale di vendita fatturati rispetto a questa voce di contratto su varie fatture create per questo contratto. Per la voce di contratto tempo e materiali: la somma degli importi su tutti i valori effettivi addebitabili di vendita fatturati rispetto a questa voce di contratto su varie fatture create per questo contratto. |
| Costi sostenuti | Righe basate su progetto | La somma di tutti i costi effettivi registrati su tutti i progetti mappati alla voce di contratto. |
| Margine lordo | Righe basate su progetto | (Importo fatturato - Costo sostenuto fino alla data) / Importo fatturato |
| Margine previsto | Righe basate su progetto | (Importo voce di contratto in valuta di base - Costi stimati per la voce di contratto in valuta di base) / Importo voce di contratto in valuta di base |
| Costi sostenuti | Dettaglio di una riga basata su progetto | Tempo: la somma dell'importo dei valori effettivi del costo del tempo registrati per il ruolo nel progetto mappato alla voce di contratto. Spese: la somma dell'importo dei valori effettivi del costo di tutte le spese per la categoria nel progetto mappato alla voce di contratto. |
| Quantità registrata | Dettaglio di una riga basata su progetto | Tempo: la quantità sui valori effettivi del costo del tempo totale per un ruolo nel progetto mappato a questa voce di contratto. Spese: tutte le quantità per la categoria di spesa nei valori effettivi dei costi di spesa nel progetto mappate alla voce di contratto. |
| Importo fatturato | Dettaglio di una riga basata su progetto | Per una voce di contratto a prezzo fisso, questo campo viene lasciato vuoto a livello di dettaglio e viene visualizzato solo a livello di voce di contratto. Per una voce di contratto tempo e materiali, i calcoli vengono completati a livello di dettagli. I dettagli mostrano la somma dell'importo su tutte le righe di ricavi fatturate rispetto a questa voce di contratto che sono addebitabili. |
| Quantità fatturata | Dettaglio di una riga basata su progetto | Per una voce di contratto a prezzo fisso, questo campo viene lasciato vuoto a livello di dettaglio e viene visualizzato solo a livello di voce di contratto. Per una voce di contratto tempo e materiali, i calcoli vengono completati a livello di dettagli per tempo e spese. Tempo: la somma delle ore su tutte le righe di ricavi fatturate per il ruolo rispetto a questa voce di contratto che sono addebitabili. Spese: tutte le quantità per la categoria di spesa nei valori effettivi dei costi di spesa nel progetto mappate alla voce di contratto. |
| Valore contratto | Righe basate su prodotto | Il valore della voce di contratto di questa voce di contratto basata su prodotto. |
| Importo fatturato | Righe basate su prodotto | La somma degli importi su tutte le righe di fattura rispetto a questa voce di contratto basata su prodotto in varie fatture create per questo contratto. |
| Costi sostenuti | Righe basate su prodotto | La somma di tutti i costi effettivi registrati per la voce di contratto basata su prodotto. |
| Margine lordo | Righe basate su progetto | Importo fatturato - Costo sostenuto fino alla data / Importo fatturato |
| Margine previsto | Righe basate su prodotto | (Valore voce di contratto - Costi stimati per la voce di contratto) / Valore voce di contratto |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]