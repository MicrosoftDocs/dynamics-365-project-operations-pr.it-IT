---
title: Stime finanziarie per materiali nei progetti
description: Questo argomento fornisce informazioni sulla definizione o sulla stima dei materiali basati su progetto.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788867"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Stime finanziarie per materiali nei progetti

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations consente ai responsabili di progetto di definire i costi dei materiali basati su progetto per ogni progetto o attività. Ogni stima di materiale può essere associata a una specifica attività di progetto. Le spese sono classificate in diverse categorie di spesa, definite a livello organizzativo. I prezzi e i costi di ciascuna categoria di spesa sono definiti nel listino prezzi. 

Completa i seguenti passaggi per visualizzare, aggiungere o eliminare una stima di materiale di progetto.

1. Vai a **Progetti** e seleziona il progetto che desideri aggiornare.
2. Nella scheda **Stime materiali**, visualizza l'elenco delle stime dei materiali di progetto.
3. Seleziona **Nuova stima materiale** per creare una nuova stima materiale. Oppure seleziona una stima materiale da eliminare, quindi seleziona **Elimina stima materiale**.

La tabella seguente fornisce informazioni sui campi nella **Riga di stima materiale** in un progetto. 

| **Campo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- |
| Attività | Un elenco di attività nel progetto. Ciò include attività di riepilogo e nodo foglia. | Quando selezioni un'attività per una riga di stima materiale, vengono influenzati il costo del materiale stimato e le vendite di materiale stimate per un'attività. Se questo campo è vuoto, la stima materiale viene registrata e riepilogata solo a livello di progetto. |
| Selezione prodotto |  Puoi specificare se la riga di stima è per un prodotto esistente (catalogo) o un prodotto fuori catalogo. | Questo campo determina se si seleziona un prodotto del catalogo o un prodotto fuori catalogo. |
| Prodotto | L'ID del prodotto nel catalogo prodotti. Quando selezioni un ID prodotto, il valore nel campo **Selezione prodotto** diventa automaticamente **Prodotto esistente**. L'ID viene utilizzato per recuperare il prezzo di costo e vendita dal listino prezzi. | Non vi è alcun impatto downstream per questo campo. |
| Descrizione prodotto fuori catalogo | Un campo di testo in cui immettere il nome del prodotto. Questo campo deve essere utilizzato quando è selezionato **Fuori catalogo** nel campo **Seleziona prodotto**.| Non vi è alcun impatto downstream per questo campo. |
| Data di inizio | La data prevista per l'utilizzo di materiale. | Non vi è alcun impatto downstream per questo campo. |
| Unità di vendita | Il valore predefinito in questo campo proviene dall'unità di vendita predefinita nel prodotto del catalogo. Puoi aggiornare questo campo per selezionare un'altra unità di vendita. | Non vi è alcun impatto downstream per questo campo. |
| Unità | Il valore in questo campo proviene dall'unità predefinita del prodotto selezionato. Puoi aggiornare questo campo per selezionare un'altra unità. | La modifica dell'unità comporta un costo e un prezzo unitario predefiniti differenti. |
| Quantità | La quantità stimata del prodotto che verrà utilizzata nel progetto. | Non vi è alcun impatto downstream per questo campo. |
| Costo unitario | Il costo unitario della combinazione di prodotto e unità selezionati come impostato nel listino prezzi di costo applicabile. | Il costo unitario viene sempre mostrato nella valuta del costo del progetto. Se non è presente alcuna impostazione del costo unitario per la combinazione di prodotto e unità impostata nel listino prezzi, il costo unitario verrà impostato automaticamente su 0,00. |
| Prezzo unitario | Il prezzo della combinazione di prodotto e unità selezionati come impostato nel listino prezzi di vendita applicabile. | Il prezzo unitario viene sempre mostrato nella valuta di vendita del progetto. Se non è presente alcuna impostazione del prezzo unitario per la combinazione di prodotto e unità impostata nel listino prezzi, il prezzo unitario verrà impostato automaticamente su 0,00.|
| Costo totale | L'importo del costo calcolato come quantità \* costo unitario.| L'importo dei costi viene sempre visualizzato nella valuta di costo del progetto. |
| Totale vendite | L'importo delle vendite calcolato come quantità \* prezzo unitario. | L'importo delle vendite viene sempre visualizzato nella valuta di vendita del progetto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]