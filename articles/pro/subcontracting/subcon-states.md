---
title: Transizioni di stato in un conto lavoro
description: Questo articolo spiega le transizioni di stato su un conto lavoro in Microsoft Dynamics 365 Project Operations quando il conto lavoro viene creato, eseguito e chiuso.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261207"
---
# <a name="state-transitions-on-a-subcontract"></a>Transizioni di stato in un conto lavoro 

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo articolo spiega le transizioni di stato su un conto lavoro in Microsoft Dynamics 365 Project Operations. Ogni stato è rappresentato come bozza, confermato, chiuso o annullato. L'immagine seguente rappresenta le transizioni di stato.

![Modello di stato del conto lavoro](../media/SubconStates.png)  

La tabella seguente fornisce una descrizione di ciò che ogni stato rappresenta nel ciclo di vita di un conto lavoro in Project Operations.

| Provincia | Description | Transizioni consentite |
| --- | --- | --- |
| Bozze | Rappresenta lo stato iniziale di un conto lavoro. Sono in corso trattative con il fornitore. Le righe e i prezzi sono soggetti a modifiche. Un conto lavoro in questo stato può essere utilizzato per stimare i requisiti del progetto del personale per risorse e materiali. Può anche essere riferimento per tempi, spese e utilizzo del materiale in un progetto. Un conto lavoro in questo stato può essere modificato ed eliminato. | Confermato |
| Confermato | Rappresenta la fase di un conto lavoro dopo il completamento delle negoziazioni con il fornitore sui prezzi e sugli articoli acquistati. Tuttavia, l'effettiva consegna di materiali e/o lavori da parte di risorse in conto lavoro è ancora in corso. Un conto lavoro in questo stato può essere utilizzato per stimare i requisiti del progetto del personale per risorse e materiali. Può anche essere riferimento per tempi, spese e utilizzo del materiale in un progetto. Un conto lavoro in questo stato non può essere modificato o eliminato. Il pulsante **Annulla** consente di annullare un conto lavoro confermato. Il pulsante **Riapri** permette di riaprire il conto lavoro per riportarlo nello stato **Bozza**. Utilizza il pulsante **Chiudi** per chiudere un conto lavoro confermato. | Chiusa <br> Annullati <br> Bozze |
| Chiusa | Rappresenta la fase di un conto lavoro in cui viene completata la consegna effettiva dei materiali e/o del lavoro da parte delle risorse in conto lavoro. Un conto lavoro in questo stato non può più essere utilizzato per stimare i requisiti del progetto del personale per risorse e materiali. Inoltre non può essere riferimento per tempi, spese e utilizzo del materiale in un progetto. Un conto lavoro in questo stato non può essere modificato o eliminato. | None |
| Annullati | Rappresenta la fase di un conto lavoro in cui non è più necessaria la consegna effettiva dei materiali e/o del lavoro da parte delle risorse in conto lavoro. Un conto lavoro in questo stato non può essere utilizzato per stimare e richiedere personale del progetto per risorse e materiali, né può essere riferimento per tempi, spese e utilizzo di materiale in un progetto. Un conto lavoro in questo stato non può essere modificato o eliminato. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
