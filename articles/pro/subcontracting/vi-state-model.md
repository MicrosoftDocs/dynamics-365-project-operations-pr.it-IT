---
title: Transizioni di stato in una fattura fornitore
description: Questo articolo spiega le transizioni di stato su una fattura fornitore in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261021"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transizioni di stato in una fattura fornitore

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo articolo spiega le transizioni di stato su una fattura fornitore in Microsoft Dynamics 365 Project Operations. Vengono utilizzati i seguenti stati: **Bozza**, **In revisione**, **Confermato**, **In attesa**, e **Annullato**.

Le figure di seguito mostrano le transazioni di stato.

![Modello di transizione di stato di conto lavoro](../media/VI_State_Model.jpg)

La tabella seguente spiega ciò che ogni stato rappresenta nel ciclo di vita di una fattura fornitore in Project Operations.

| Provincia | Description | Transizioni consentite |
| --- | --- | --- |
| Bozze | Questo stato è lo stato iniziale di una fattura fornitore. Le righe e i prezzi sono soggetti a modifica. La fattura fornitore in questo stato non può essere modificata o eliminata. | In corso |
| In revisione | Questo stato rappresenta lo stato di elaborazione di una fattura fornitore. Almeno una riga della fattura fornitore ha uno stato di verifica di **In corso**. | Confermato, In attesa |
| Confermato | Questo stato rappresenta la fase di una fattura fornitore in cui l'applicazione ha creato i costi effettivi per ciascuna riga di fattura fornitore. Tutti i costi effettivi collegati che sono stati abbinati alle righe di fattura fornitore sono stati stornati e sostituiti con i costi effettivi di tali righe di fattura fornitore. Una fattura fornitore in questo stato non può essere modificata o eliminata. Puoi usare il pulsante **Annulla** per annullare una fattura fornitore confermata. L'azione Annulla annulla l'impatto dell'azione Conferma. | Annullati |
| In sospeso | <p>Questo stato rappresenta una fase di una fattura fornitore in cui la fattura fornitore non può essere spostata a causa di un problema con la fattura o con lo stato del fornitore. Una fattura fornitore in questo stato non può essere confermata, annullata, modificata o eliminata.</p><p>È possibile utilizzare l'azione Riapri per spostare la fattura fornitore nello stato **Bozza** o **In revisione**. Se almeno una riga di fattura fornitore ha uno stato di verifica **In corso** o **Completato**, la fattura fornitore verrà riaperta nello stato **In revisione**. Se tutte le righe di fattura fornitore hanno uno stato di verifica **Non avviato**, la fattura fornitore verrà riaperta nello stato **Bozza**.</p> | Bozza, In revisione |
| Annullati | Questo stato rappresenta la fase di un conto lavoro in cui non è più necessaria la consegna effettiva del materiale e/o del lavoro da parte delle risorse in conto lavoro. Un conto lavoro in questo stato non può essere utilizzato per stimare e richiedere personale del progetto per risorse e materiali, né può essere riferimento per tempi, spese e utilizzo di materiale in un progetto. Un conto lavoro in questo stato non può essere modificato o eliminato. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
