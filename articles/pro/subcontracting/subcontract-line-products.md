---
title: Righe conto lavoro per prodotti
description: Questo articolo spiega come registrare le righe conto lavoro per i prodotti e utilizzare i diversi campi per registrare gli acquisti di prodotti dai fornitori.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff9636f86102fa671a443d7646614070b3e2ee79
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934371"
---
# <a name="subcontract-lines-for-products"></a>Righe conto lavoro per prodotti

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Un conto lavoro in Dynamics 365 Project Operations può avere una voce di conto lavoro per i prodotti. Queste righe consentono a un responsabile di progetto di acquistare prodotti dai fornitori che può quindi utilizzare nelle attività del progetto.

Completare i seguenti passaggi per creare una voce di conto lavoro per i prodotti in Project Operations.

1. Nella pagina di navigazione, seleziona **Conti lavoro**, quindi apri il conto lavoro con cui desideri lavorare. 
2. Nella scheda **Voci di conto lavoro**, seleziona **+ Nuovo** per creare una nuova riga conto lavoro.
3. Nella pagina **Creazione rapida**, nel campo **Classe di transazione**, seleziona **Materiale** e inserisci o seleziona le informazioni richieste per il campo. 
4. Seleziona **Salva**.

La tabella seguente fornisce informazioni sui campi nella pagina **Dettagli voce conto lavoro** e nella pagina **Creazione rapida** in quanto rilevanti per l'acquisto di prodotti.

| Campo | Descrizione | Impatto funzionale|
| ----- | ----------- | ----------- |
| Nome | Nome della riga di conto lavoro per facilitare l'identificazione. |Questa verrà mostrata come prima colonna in tutte le ricerche basate sulle righe di conto lavoro.
| Descrizione | Una breve descrizione dei prodotti ordinati nella voce di conto lavoro. | Nessuna |
| Tipo di linea | Il valore predefinito di questo campo è **Basato su quantità**. |Nessuna |
| Metodo di fatturazione | Questo è un set di opzioni che rappresenta i due principali modelli di contrattazione supportati da Project Operations: **Prezzo fisso** e **Tempistica e materiali**. | In base al metodo di fatturazione selezionato, se è stato selezionato il metodo di fatturazione a prezzo fisso, per le righe del conto di lavoro viene resa disponibile una pianificazione fattura basata su passaggi fondamentali. |
| Classe di transazione |Il valore predefinito di questo campo è **Data/Ora**. Per creare voci di conto lavoro per l'acquisto di prodotti, impostare il campo **Classe di transazione** su **Materiali**.  | Ciò indica che la riga del conto lavoro viene utilizzata per registrare l'acquisto di prodotti da utilizzare sui progetti. |
| Selezione prodotto | Selezionare se il prodotto acquistato è mantenuto nel catalogo prodotti o è un prodotto fuori catalogo. |Nessuna |
| Prodotto | Seleziona un prodotto attivo dal catalogo. Questo campo è disponibile solo quando **Seleziona prodotto** è impostato su **Esistente**. |La combinazione di **Prodotto** e **Unità** verrà utilizzata come valore predefinito o calcolato per il prezzo unitario per la riga di conto lavoro.
| Prodotto fuori catalogo | Immetti il nome del prodotto fuori catalogo. Questo campo è disponibile solo quando **Seleziona prodotto** è impostato su **Fuori catalogo**.  |Il prezzo di acquisto non verrà compilato automaticamente per i prodotti già inseriti.|
| Data di consegna richiesta | Inserisci la data di consegna richiesta per i prodotti.| Questa data viene utilizzata anche per selezionare un listino prezzi per il progetto dai listini allegati al conto lavoro. Il costo del prodotto nella voce del conto lavoro viene quindi predefinito da quel listino prezzi. |
| Data di consegna di contratto | Inserisci la data in cui i prodotti sono contrattualmente concordati per essere consegnati.  |Nessuna|
| Quantità ordinata | Inserisci la quantità del prodotto acquistato dal venditore.| Questa verrà utilizzata per visualizzare avvisi quando un responsabile di progetto sta andando oltre questa quantità.|
| Unità di vendita | Questo valore è predefinito solo per i prodotti del catalogo. |Quando **Prodotto** e **Data consegna richiesta** sono entrambi selezionati, il sistema seleziona il listino prezzi applicabile in base alla data di consegna. Le relative voci di listino vengono interrogate per il prodotto corrispondente. I valori predefiniti dell'unità e del gruppo di unità dall'impostazione nel record dell'elemento del listino prezzi. |
| Unità | Il valore predefinito è l'unità impostata nel record dell'articolo del listino prezzi. Se necessario, puoi cambiarlo con un'altra unità.| La combinazione di prodotto e unità viene utilizzata per impostare il prezzo unitario predefinito nella voce del conto lavoro per i prodotti del catalogo esistenti. |
| Prezzo unitario | Il prezzo unitario viene predefinito utilizzando la combinazione di prodotto e unità dalle voci di listino relative al listino prezzi del progetto applicabile per la data di consegna richiesta della riga di conto lavoro.  |Nessuna |
| Subtotale | Questo campo di sola lettura viene calcolato come Quantità x Prezzo unitario se entrambi i campi hanno valori immessi. Se il campo **Quantità**, **Prezzo unitario** o entrambi sono vuoti, puoi inserire un valore manualmente.  |Nessuna |
| IVA | Immetti il valore dell'IVA. |Nessuna |
| Totale importo | Questo campo calcolato mostra l'importo totale della voce di conto lavoro dopo l'inclusione delle imposte. Il valore in questo campo viene calcolato come subtotale + imposte. |Nessuna |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
