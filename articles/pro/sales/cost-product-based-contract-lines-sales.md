---
title: Costo delle voci del contratto basate sul prodotto
description: In questo argomento vengono fornite informazioni sulla creazione
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4079107"
---
# <a name="costing-product-based-contract-lines"></a>Costo delle voci del contratto basate sul prodotto

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_


Le voci di contratto basate su prodotto in Dynamics 365 Project Operations includono il campo **Prezzo di costo** che memorizza il prezzo di costo del prodotto per i calcoli della redditività downstream.

Quando una voce di contratto basata su prodotto viene creata per un prodotto del catalogo, il costo della riga di offerta basata su prodotto viene derivato per impostazione predefinita dal campo **Costo standard** nel catalogo prodotti. Il campo del **costo standard** nel catalogo dei prodotti viene impostato nella valuta di base dell'organizzazione. Quando il costo unitario è predefinito nella voce di contratto, viene convertito nella valuta di vendita del contratto.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Costo unitario su una voce di contratto basata su prodotto

Avere un costo unitario su una voce di contratto basata su prodotto consente costi diversi per un prodotto per ciascuna unità di vendita. Sebbene non sempre necessario, esistono alcuni scenari in cui il costo del prodotto può essere scontato per il cliente dal fornitore. Prendi in considerazione lo scenario seguente:

Fabrikam Robotics sta installando bracci robotici presso le linee di assemblaggio di Adatum Corporation. Fabrikam fornisce servizi di installazione, ma i bracci robotici vengono acquistati da Trey Research. Se l'installazione di bracci robotici presso Adatum Corporation apre un nuovo settore verticale per Trey Research, potrebbero concedere uno sconto speciale per questo accordo a Fabrikam. In questo caso, Fabrikam crea una voce di contratto basata su prodotto per i bracci robotici e immette un costo unitario per questo contratto diverso dal costo standard dei bracci robotici di Trey Research.
