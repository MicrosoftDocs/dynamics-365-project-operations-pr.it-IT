---
title: Costo delle voci di contratto basate su prodotto - semplice
description: In questo argomento vengono fornite informazioni sulla creazione
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273698"
---
# <a name="cost-product-based-contract-lines---lite"></a>Costo delle voci di contratto basate su prodotto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_


Le righe di contratto basate sul prodotto in Dynamics 365 Project Operations includono il campo **Prezzo di costo** che memorizza il prezzo di costo del prodotto per i calcoli della redditività downstream.

Quando viene creata una riga di contratto basata sul prodotto per un prodotto catalogo, il costo della riga viene impostato per impostazione predefinita dal campo **Costo standard** nel catalogo prodotti. Il campo del **costo standard** nel catalogo dei prodotti viene impostato nella valuta di base dell'organizzazione. Quando il costo unitario è predefinito nella voce di contratto, viene convertito nella valuta di vendita del contratto.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Costo unitario su una voce di contratto basata su prodotto

Avere un costo unitario su una voce di contratto basata su prodotto consente costi diversi per un prodotto per ciascuna unità di vendita. Sebbene non sempre necessario, esistono alcuni scenari in cui il costo del prodotto può essere scontato per il cliente dal fornitore. Prendi in considerazione lo scenario seguente:

Fabrikam Robotics sta installando bracci robotici presso le linee di assemblaggio di Adatum Corporation. Fabrikam fornisce servizi di installazione ma Robotic Arms proviene da Trey Research. Se l'installazione di bracci robotici presso Adatum Corporation apre un nuovo settore verticale per Trey Research, potrebbero concedere uno sconto speciale per questo accordo a Fabrikam. In questo caso, Fabrikam crea una riga di contratto basata sul prodotto per Robotic Arms. Per questo contratto viene inserito un costo unitario. Il costo è diverso dal costo di Robotic Arms di Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]