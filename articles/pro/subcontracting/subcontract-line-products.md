---
title: Righe conto lavoro per prodotti
description: Questo argomento spiega come registrare le righe di conto lavoro per i prodotti e utilizzare i vari campi per registrare gli acquisti di prodotti dai fornitori.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323691"
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

| Campo | Descrizione |
| ----- | ----------- |
| Nome | Il nome della voce di conto lavoro. |
| Descrizione | Una breve descrizione dei prodotti ordinati nella voce di conto lavoro. |
| Tipo di linea | Il valore predefinito di questo campo è **Basato su quantità**. |
| Metodo di fatturazione |  Il metodo di fatturazione della voce di conto lavoro. Per i metodi di fatturazione a prezzo fisso è disponibile una pianificazione di fatturazione basata su passaggi fondamentali. |
| Classe di transazione | Il valore predefinito di questo campo è **Ore**. Per creare voci di conto lavoro per l'acquisto di prodotti, nel campo **Classe di transazione** seleziona **Materiale**. Questa selezione indica che la voce del conto lavoro viene utilizzata per registrare un acquisto di prodotti da utilizzare nei progetti. |
| Selezione prodotto | Selezionare se il prodotto acquistato è mantenuto nel catalogo prodotti o è un prodotto fuori catalogo. |
| Prodotto | Seleziona un prodotto attivo dal catalogo. Questo campo è disponibile solo quando **Seleziona prodotto** è impostato su **Esistente**. |
| Prodotto fuori catalogo | Immetti il nome del prodotto fuori catalogo. Questo campo è disponibile solo quando **Seleziona prodotto** è impostato su **Fuori catalogo**.  |
| Data di consegna richiesta | Seleziona la data di consegna richiesta per i prodotti. Questa data viene utilizzata anche per selezionare un listino prezzi per il progetto dai listini allegati al conto lavoro. Il costo del prodotto nella voce del conto lavoro viene quindi predefinito da quel listino prezzi. |
| Data di consegna di contratto | Seleziona la data in cui i prodotti devono essere consegnati da contratto.  |
| Quantità ordinata | Inserisci la quantità del prodotto acquistato dal venditore. Se un responsabile di progetto eccede questa quantità, verrà visualizzato un avviso. |
| Unità di vendita | Questo valore è predefinito solo per i prodotti del catalogo. Quando **Prodotto** e **Data consegna richiesta** sono entrambi selezionati, il sistema seleziona il listino prezzi applicabile in base alla data di consegna. Le relative voci di listino vengono interrogate per il prodotto corrispondente. I valori predefiniti dell'unità e del gruppo di unità dall'impostazione nel record dell'elemento del listino prezzi. |
| Unità | Questo valore è predefinito per l'impostazione dell'unità nel record della voce di listino. Se necessario, puoi cambiarlo con un'altra unità. La combinazione di prodotto e unità viene utilizzata per impostare il prezzo unitario predefinito nella voce del conto lavoro per i prodotti del catalogo esistenti. |
| Prezzo unitario | Il prezzo unitario viene predefinito utilizzando la combinazione di prodotto e unità dalle voci di listino relative al listino prezzi del progetto applicabile per la data di consegna richiesta della riga di conto lavoro.  |
| Subtotale | Questo campo di sola lettura viene calcolato come Quantità x Prezzo unitario se entrambi i campi hanno valori immessi. Se il campo **Quantità**, **Prezzo unitario** o entrambi sono vuoti, puoi inserire un valore manualmente.  |
| IVA | Immetti il valore dell'IVA. |
| Totale importo | Questo campo calcolato mostra l'importo totale della voce di conto lavoro dopo l'inclusione delle imposte. Il valore in questo campo viene calcolato come subtotale + tasse. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
