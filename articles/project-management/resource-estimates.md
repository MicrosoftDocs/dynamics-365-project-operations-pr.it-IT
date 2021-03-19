---
title: Stime delle risorse
description: Questo argomento fornisce informazioni su come vengono calcolate le stime delle risorse in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286523"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]