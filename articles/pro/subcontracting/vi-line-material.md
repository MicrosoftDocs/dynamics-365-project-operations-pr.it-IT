---
title: Righe di fattura fornitore per prodotti
description: Questo articolo spiega come registrare le righe di fattura fornitore per i prodotti e utilizzare i diversi campi per registrare gli acquisti di prodotti dai fornitori.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261563"
---
# <a name="vendor-invoice-lines-for-products"></a>Righe di fattura fornitore per prodotti

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Una fattura fornitore in Microsoft Dynamics 365 Project Operations può avere le righe di fattura fornitore per i prodotti (denominati anche materiali). I project manager possono utilizzare le righe di fattura fornitore per i prodotti per registrare i costi dei prodotti acquistati nei progetti.

Le righe di fattura fornitore per i prodotti possono o meno fare riferimento a una riga di conto lavoro per i materiali. Se una riga di fattura fornitore per prodotti fa riferimento a un conto lavoro, i project manager saranno in grado di confrontare e verificare i prodotti fatturati dalla riga di fattura fornitore con l'utilizzo dei prodotti acquistati registrati e approvati dai project manager.

La tabella seguente fornisce informazioni sui campi delle righe di fattura fornitore per i prodotti.

| Campo | Description | Impatto funzionale |
| --- | --- | --- |
| Name | Nome della riga di fattura fornitore per facilitare l'identificazione. | Questo nome verrà mostrato come prima colonna in tutte le ricerche basate sulle righe di fattura fornitore. |
| Description | Una breve descrizione dei prodotti fatturati dal fornitore nella riga di fattura fornitore. | None |
| Conto lavoro | Il conto lavoro in base al quale i prodotti sono stati originariamente ordinati. | Quando viene selezionato un conto lavoro per la fattura fornitore, tutte le righe di fattura fornitore erediteranno tale selezione. Una fattura fornitore non può avere righe di fattura fornitore che fanno riferimento a diversi conti lavoro. |
| Riga conto lavoro | La riga conto lavoro in base al quale i prodotti sono stati ordinati. L'elenco delle righe di conto lavoro selezionabili è limitato alle righe del conto lavoro selezionato. | Quando viene selezionata una riga di conto lavoro in una riga di fattura fornitore per i prodotti, i valori predefiniti per i campi **Progetto**, **Attività**, e **Prodotto** vengono inseriti dai campi corrispondenti nella riga di conto lavoro. Se la riga di conto lavoro selezionata ha valori nei campi **Progetto**, **Attività**, e **Prodotto**, i valori dei campi corrispondenti nella riga do fattura fornitore non possono differire da tali valori. |
| Data transazione | La data in cui il costo effettivo della riga di fattura fornitore verrà registrato nel progetto. | None|
| Classe di transazione | Quando i prodotti vengono fatturati, questo campo deve essere impostato su **Materiale**. | Il valore **Materiale** indica che la riga di fattura fornitore viene utilizzata per registrare l'importo della fattura per i materiali che sono stati acquistati. |
| Project | Il nome del progetto su cui sono stati utilizzati i prodotti fatturati. | Campo obbligatorio che non può essere lasciato vuoto. |
| Attività | Il nome dell'attività di progetto su cui sono stati utilizzati i prodotti fatturati. Questo campo è disponibile solo se è selezionato un progetto. La selezione di un'attività di progetto è facoltativa. | Se questo campo viene lasciato vuoto, il project manager può abbinare la riga di fattura fornitore al prodotto acquistato che viene utilizzato su qualsiasi attività del progetto. Se la riga di fattura fornitore non fa riferimento a una riga di conto lavoro e questo campo viene lasciato vuoto, il costo effettivo creato dalla riga di fattura fornitore non sarà collegato ad alcuna vendita effettiva non fatturata. In questo caso, se è impostata la fatturazione basata su attività, i costi possono non essere fatturabili al cliente finale. |
| Seleziona prodotto | Seleziona se il prodotto che viene fatturato è un prodotto esistente del catalogo o un prodotto fuori catalogo. | Il valore predefinito viene immesso dalla riga di conto lavoro quando viene selezionata una riga di conto lavoro. |
| Prodotto | Seleziona il prodotto dal catalogo. Se il prodotto è fuori catalogo digita il nome del prodotto. | Questo campo viene utilizzato per inserire i prezzi di acquisto predefiniti per i prodotti esistenti. |
| Quantità | Immetti la quantità di materiale fatturata dal fornitore nella riga di fattura. | None |
| Unità di vendita | Seleziona il gruppo di unità in cui è espressa la quantità fatturata. | None |
| Unità | Il valore predefinito è l'unità di base del gruppo di unità selezionato. Puoi modificare questo valore per pagare in altre unità del gruppo di unità selezionato. | La combinazione dei valori **Prodotto** e **Unità** verrà utilizzata come valore predefinito o calcolato per il campo **Prezzo unitario** per la riga di fattura fornitore. |
| Prezzo unitario | Il prezzo unitario predefinito utilizza la combinazione dei valori **Prodotto** e **Unità** dal listino prezzi del progetto applicabile alla data di transazione della riga di fattura fornitore. | None |
| Subtotale | Questo è un campo di sola lettura che viene calcolato come *Quantità* &times; *Prezzo unitario*, se vengono immessi sia i valori di **quantità** che di **prezzo unitario** nei campi. Se uno o entrambi i campi sono vuoti, puoi inserire un valore in questo campo. | None |
| IVA | Immetti l'importo IVA. | None |
| Importo totale | L'importo totale della riga di fattura fornitore, tasse incluse. Questo campo viene calcolato come *Subtotale* + *IVA*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
