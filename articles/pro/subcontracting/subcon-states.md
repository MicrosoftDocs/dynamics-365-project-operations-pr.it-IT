---
title: Transizioni di stato in un conto lavoro
description: Questo argomento spiega le transizioni di stato su un conto lavoro in Microsoft Dynamics 365 Project Operations quando il conto lavoro viene creato, eseguito e chiuso.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903453"
---
# <a name="state-transitions-on-a-subcontract"></a>Transizioni di stato in un conto lavoro 

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento spiega le transizioni di stato su un conto lavoro in Microsoft Dynamics 365 Project Operations. Ogni stato è rappresentato come bozza, confermato, chiuso o annullato. L'immagine seguente rappresenta le transizioni di stato.

![Modello di stato del conto lavoro](../media/SubconStates.png)  

La tabella seguente fornisce una descrizione di ciò che ogni stato rappresenta nel ciclo di vita di un conto lavoro in Project Operations.

| Provincia | Description | Transizioni consentite |
| --- | --- | --- |
| Bozze | Rappresenta lo stato iniziale di un conto lavoro. Sono in corso trattative con il fornitore. Le righe e i prezzi sono soggetti a modifiche. Un conto lavoro in questo stato può essere utilizzato per stimare i requisiti del progetto del personale per risorse e materiali. Può anche essere riferimento per tempi, spese e utilizzo del materiale in un progetto. Un conto lavoro in questo stato può essere modificato ed eliminato. | Confermato |
| Confermato | Rappresenta la fase di un conto lavoro dopo il completamento delle negoziazioni con il fornitore sui prezzi e sugli articoli acquistati. Tuttavia, l'effettiva consegna di materiali e/o lavori da parte di risorse in conto lavoro è ancora in corso. Un conto lavoro in questo stato può essere utilizzato per stimare i requisiti del progetto del personale per risorse e materiali. Può anche essere riferimento per tempi, spese e utilizzo del materiale in un progetto. Un conto lavoro in questo stato non può essere modificato o eliminato. Il pulsante **Annulla** consente di annullare un conto lavoro confermato. Il pulsante **Riapri** permette di riaprire il conto lavoro per riportarlo nello stato **Bozza**. Utilizza il pulsante **Chiudi** per chiudere un conto lavoro confermato. | Chiusa <br> Annullati <br> Bozze |
| Chiusa | Rappresenta la fase di un conto lavoro in cui viene completata la consegna effettiva dei materiali e/o del lavoro da parte delle risorse in conto lavoro. Un conto lavoro in questo stato non può più essere utilizzato per stimare i requisiti del progetto del personale per risorse e materiali. Inoltre non può essere riferimento per tempi, spese e utilizzo del materiale in un progetto. Un conto lavoro in questo stato non può essere modificato o eliminato. | None |
| Annullati | Rappresenta la fase di un conto lavoro in cui non è più necessaria la consegna effettiva dei materiali e/o del lavoro da parte delle risorse in conto lavoro. Un conto lavoro in questo stato non può essere utilizzato per stimare e richiedere personale del progetto per risorse e materiali, né può essere riferimento per tempi, spese e utilizzo di materiale in un progetto. Un conto lavoro in questo stato non può essere modificato o eliminato. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
