---
title: Righe di fattura fornitore per categorie di spesa
description: Questo articolo spiega come registrare le righe di fattura fornitore per le categorie di spesa.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261687"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Righe di fattura fornitore per categorie di spesa

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Una fattura fornitore in Microsoft Dynamics 365 Project Operations può avere righe di fattura fornitore per le categorie di spesa. I project manager possono utilizzare le righe di fattura fornitore per le categorie di spesa per registrare i costi dei servizi acquistati come categorie di spesa.

Le righe di fattura fornitore per le categorie di spesa possono o meno fare riferimento a una riga di conto lavoro per le categorie di spesa. Se una riga di fattura fornitore per categorie di spesa fa riferimento a un conto lavoro, i project manager saranno in grado di confrontare e verificare le spese fatturate dalla riga di fattura fornitore con le spese registrate in queste categorie di spesa e approvate dai project manager per il progetto.

La tabella seguente fornisce informazioni sui campi delle righe di fattura fornitore per le categorie di spesa.

| Campo | Description | Impatto funzionale |
| --- | --- | --- |
| Name | Nome della riga di fattura fornitore per facilitare l'identificazione. | Questo nome verrà mostrato come prima colonna in tutte le ricerche basate sulle righe di fattura fornitore. |
| Description | Una breve descrizione dei servizi fatturati dal fornitore nella riga di fattura fornitore. | None |
| Conto lavoro | Il conto lavoro in base al quale i servizi sono stati originariamente ordinati. | Quando viene selezionato un conto lavoro per la fattura fornitore, tutte le righe di fattura fornitore erediteranno tale selezione. Una fattura fornitore non può avere righe di fattura fornitore che fanno riferimento a diversi conti lavoro. |
| Riga conto lavoro | La riga conto lavoro in base al quale i servizi sono stati ordinati. L'elenco delle righe di conto lavoro selezionabili è limitato alle righe del conto lavoro selezionato. | Quando viene selezionata una riga di conto lavoro in una riga di fattura fornitore per le categorie di spesa, i valori predefiniti per i campi **Progetto**, **Attività**, e **Categoria di transazione** vengono inseriti dai campi corrispondenti nella riga di conto lavoro. Se la riga di conto lavoro selezionata ha valori nei campi **Progetto**, **Attività di progetto**, e **Categoria di transazione**, i valori dei campi corrispondenti nella riga do fattura fornitore non possono differire da tali valori. |
| Data transazione | La data in cui il costo effettivo della riga di fattura fornitore verrà registrato nel progetto. |None |
| Classe di transazione | Seleziona **Spese** per registrare una fattura fornitore per una categoria di spesa. | Il valore **Spese** indica che la riga di fattura fornitore viene utilizzata per registrare l'importo della fattura per i servizi che sono stati acquistati come categorie di spesa. |
| Project | Il nome del progetto su cui sono stati utilizzati i servizi fatturati. | Campo obbligatorio che non può essere lasciato vuoto. |
| Attività | Il nome dell'attività di progetto su cui sono stati utilizzati i servizi fatturati. Questo campo è disponibile solo se è selezionato un progetto. La selezione di un'attività di progetto è facoltativa. | Se questo campo viene lasciato vuoto, il project manager può abbinare la riga di fattura fornitore alle spese registrate su qualsiasi attività del progetto. Se la riga di fattura fornitore non fa riferimento a una riga di conto lavoro e questo campo viene lasciato vuoto, il costo effettivo creato dalla riga di fattura fornitore non sarà collegato ad alcuna vendita effettiva non fatturata. In questo caso, se è impostata la fatturazione basata su attività, i costi possono non essere fatturabili al cliente finale. |
| Categoria di transazione | La categoria di transazione che viene fatturata. È necessario creare una categoria di spesa corrispondente per la categoria di transazione selezionata. | La combinazione dei valori **Categoria di transazione** e **Unità** verrà utilizzata come valore predefinito o calcolato per il campo **Prezzo unitario** per la riga di fattura fornitore. |
| Quantità | Immetti la quantità fatturata dal fornitore nella riga di fattura. |None|
| Unità di vendita | Viene inserito un valore predefinito in base al gruppo di unità della categoria di transazione selezionata. | None |
| Unità | Il valore predefinito è l'unità di base del gruppo di unità selezionato. Puoi modificare questo valore per acquistare in altre unità del gruppo di unità. | La combinazione dei valori **Categoria di transazione** e **Unità** verrà utilizzata come valore predefinito o calcolato per il campo **Prezzo unitario** per la riga di fattura fornitore. |
| Prezzo unitario | Il prezzo unitario predefinito utilizza la combinazione dei valori **Categoria di transazione** e **Unità** dal listino prezzi del progetto applicabile alla data di transazione della riga di fattura fornitore. | Se il prezzo per il listino prezzi del progetto applicabile è impostato in un'unità diversa dall'unità nella riga di fattura fornitore, il sistema utilizza la conversione dell'unità per calcolare il prezzo unitario. |
| Subtotale | Questo è un campo di sola lettura che viene calcolato come *Quantità* &times; *Prezzo unitario*, se vengono immessi sia i valori di **quantità** che di **prezzo unitario** nei campi. Se uno o entrambi i campi sono vuoti, puoi inserire un valore in questo campo.| None |
| IVA | Immetti l'importo IVA. | None |
| Importo totale | L'importo totale della riga di fattura fornitore, tasse incluse. Questo campo viene calcolato come *Subtotale* + *IVA*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
