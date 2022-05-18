---
title: Stime finanziarie per spese nei progetti
description: Questo argomento fornisce informazioni sulla definizione o sulla stima delle spese basate sul progetto.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589477"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Stime finanziarie per spese nei progetti
_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations consente ai responsabili di progetto di definire le spese basate su progetto per ogni progetto o attività. Ogni voce di spesa può essere associata a una specifica attività di progetto. Le spese sono classificate in diverse categorie di spesa, definite a livello organizzativo. I prezzi e i costi di ciascuna categoria di spesa sono definiti nel listino prezzi. 

Completa i seguenti passaggi per visualizzare, aggiungere o eliminare una spesa di progetto.

1. Vai a **Progetti** e seleziona il progetto su cui vuoi lavorare.
2. Seleziona la scheda **Stime di progetto** e visualizza l'elenco delle spese di progetto.
3. Seleziona **Nuova spesa** per aggiungere una spesa. In alternativa, seleziona una spesa da eliminare, quindi seleziona **Elimina spesa**.

La tabella seguente fornisce informazioni sui campi nella **Riga di stima della spesa** in un progetto. 

| **Campo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- |
| Attività | Un elenco di attività nel progetto. Ciò include attività di riepilogo e nodo foglia. | La selezione di un'attività per una riga di stima di spesa influirà sul costo di spesa stimato e sulle vendite di spesa stimate per un'attività. Se questo campo viene lasciato vuoto, la stima di spesa viene registrata e riepilogata solo a livello di progetto. |
| Categoria. | Un elenco di categorie di transazioni che hanno categorie di spesa collegate nell'applicazione. | La selezione di una categoria determina prezzi e costi nella riga della stima di spesa. |
| Data di inizio | La data prevista in cui si verificherà la spesa. | Non vi è alcun impatto downstream per questo campo. |
| Unità di vendita | Il valore predefinito in questo campo proviene dall'unità di vendita impostata come predefinita nella categoria selezionata. Puoi aggiornare questo campo per selezionare un'altra unità di vendita. | Non vi è alcun impatto downstream per questo campo. |
| Unità | Il valore predefinito di questo campo è l'unità predefinita della categoria selezionata. Puoi aggiornare questo campo per selezionare un'altra unità. | La modifica dell'unità comporta un costo e un prezzo unitario predefiniti differenti. |
| Quantità | La quantità della spesa stimata che dovrai sostenere. | Non vi è alcun impatto downstream per questo campo. |
| Costo unitario | Il costo della combinazione di categoria e unità selezionata come impostato nel listino prezzi di costo applicabile | Il costo unitario viene sempre mostrato nella valuta del costo del progetto. |
| Prezzo unitario | Il prezzo della combinazione di categoria e unità selezionata come impostato nel listino prezzi di vendita applicabile. | Il prezzo unitario viene sempre mostrato nella valuta di vendita del progetto. |
| Costo totale | L'importo del costo calcolato come quantità \* costo unitario.| L'importo dei costi viene sempre visualizzato nella valuta di costo del progetto. |
| Totale vendite | L'importo delle vendite calcolato come quantità \* prezzo unitario. | L'importo delle vendite viene sempre visualizzato nella valuta di vendita del progetto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
