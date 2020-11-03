---
title: Stime delle risorse
description: Questo argomento fornisce informazioni su come vengono calcolate le stime delle risorse in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078796"
---
# <a name="resource-estimates"></a>Stime delle risorse

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le stime delle risorse provengono dal lavoro su scala cronologica definito nella struttura di suddivisione del lavoro insieme alle dimensioni di determinazione dei prezzi applicabili. In genere, il calcolo è **tasso/ora per ogni ruolo x ore**. Il lavoro su scala cronologica per ciascuna risorsa viene archiviato nel record di assegnazione delle risorse. I prezzi sono archiviati in un listino prezzi predefinito. La conversione di unità viene applicata in base al listino prezzi applicabile.

![Stime delle risorse](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Prezzo di costo e valuta di costo predefiniti

I prezzi di costo vengono impostati in modo predefinito dall'unità organizzativa.

## <a name="default-bill-rate-and-sales-currency"></a>Tasso di fatturazione e valuta di vendita predefiniti

I prezzi di vendita vengono applicati una volta per transazione. La gerarchia per l'impostazione dei valori predefiniti del listino prezzi di vendita è la seguente:

1. Azienda
2. Cliente
3. Offerta/contratto
