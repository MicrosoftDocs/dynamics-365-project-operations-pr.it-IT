---
title: Costo delle righe dell'offerta basate sul prodotto
description: Questo argomento fornisce informazioni sull'applicazione di un prezzo di costo a una riga di offerta basata su prodotto.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d9c03fa1a8f43cc110565efbafd7f5aba69f65f96bec7f15f2bd492123f639c7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001886"
---
# <a name="costing-product-based-quote-lines"></a>Costo delle righe dell'offerta basate sul prodotto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


Le righe di offerta basata su prodotto in Dynamics 365 Project Operations hanno anche un campo **Prezzo di costo**. Questo campo viene utilizzato per tener traccia del prezzo di costo del prodotto nella riga di offerta e per i calcoli della redditività downstream.

Quando una riga di offerta basata su prodotto viene creata per un prodotto del catalogo, il costo della riga di offerta basata sul prodotto viene derivato per impostazione predefinita dal campo **Costo standard** nel catalogo prodotti. Il campo del costo standard nel catalogo dei prodotti viene impostato nella valuta di base dell'organizzazione. Il costo unitario predefinito nella riga dell'offerta basata sul prodotto viene convertito nella valuta di vendita dell'offerta.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Costo unitario su una riga dell'offerta basata sul prodotto

Lo scopo di avere un costo unitario su una riga di offerta basata sul prodotto è quello di consentire costi diversi per un prodotto per ciascuna vendita. Questo non è uno scenario tipico, ma a volte il costo del prodotto può essere scontato dal fornitore a seconda del cliente della vendita finale.

Ad esempio:

Fabrikam Robotics sta installando bracci robotici presso le linee di assemblaggio di A Datum Corporation. Fabrikam fornisce servizi di installazione, ma i bracci robotici vengono acquistati da Trey Robotics. Se l'installazione di bracci robotici presso A Datum Corporation apre un nuovo settore verticale per i bracci robotici di Trey, Trey potrebbe concedere uno sconto speciale per questo accordo a Fabrikam.

In questo caso, Fabrikam creerà una riga di offerta basata sul prodotto per Bracci robotici e inserirà un costo unitario speciale per questa offerta. Questo costo è diverso dal costo standard di Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]