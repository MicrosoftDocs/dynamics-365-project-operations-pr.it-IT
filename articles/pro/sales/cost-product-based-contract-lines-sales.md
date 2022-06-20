---
title: Costo delle voci di contratto basate su prodotto - semplice
description: In questo articolo sono riportate informazioni sulla creazione
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922917"
---
# <a name="cost-product-based-contract-lines---lite"></a>Costo delle voci di contratto basate su prodotto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_


Le righe di contratto basate sul prodotto in Dynamics 365 Project Operations includono il campo **Prezzo di costo** che memorizza il prezzo di costo del prodotto per i calcoli della redditività downstream.

Quando viene creata una riga di contratto basata sul prodotto per un prodotto catalogo, il costo della riga viene impostato per impostazione predefinita dal campo **Costo standard** nel catalogo prodotti. Il campo del **costo standard** nel catalogo dei prodotti viene impostato nella valuta di base dell'organizzazione. Quando il costo unitario è predefinito nella voce di contratto, viene convertito nella valuta di vendita del contratto.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Costo unitario su una voce di contratto basata su prodotto

Avere un costo unitario su una voce di contratto basata su prodotto consente costi diversi per un prodotto per ciascuna unità di vendita. Sebbene non sempre necessario, esistono alcuni scenari in cui il costo del prodotto può essere scontato per il cliente dal fornitore. Prendi in considerazione lo scenario seguente:

Fabrikam Robotics sta installando bracci robotici presso le linee di assemblaggio di Adatum Corporation. Fabrikam fornisce servizi di installazione ma Robotic Arms proviene da Trey Research. Se l'installazione di bracci robotici presso Adatum Corporation apre un nuovo settore verticale per Trey Research, potrebbero concedere uno sconto speciale per questo accordo a Fabrikam. In questo caso, Fabrikam crea una riga di contratto basata sul prodotto per Robotic Arms. Per questo contratto viene inserito un costo unitario. Il costo è diverso dal costo di Robotic Arms di Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]