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
# <a name="resource-estimates"></a><span data-ttu-id="b5a15-103">Stime delle risorse</span><span class="sxs-lookup"><span data-stu-id="b5a15-103">Resource estimates</span></span>

<span data-ttu-id="b5a15-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="b5a15-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b5a15-105">Le stime delle risorse provengono dal lavoro su scala cronologica definito nella struttura di suddivisione del lavoro insieme alle dimensioni di determinazione dei prezzi applicabili.</span><span class="sxs-lookup"><span data-stu-id="b5a15-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="b5a15-106">In genere, il calcolo è **tasso/ora per ogni ruolo x ore**.</span><span class="sxs-lookup"><span data-stu-id="b5a15-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="b5a15-107">Il lavoro su scala cronologica per ciascuna risorsa viene archiviato nel record di assegnazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="b5a15-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="b5a15-108">I prezzi sono archiviati in un listino prezzi predefinito.</span><span class="sxs-lookup"><span data-stu-id="b5a15-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="b5a15-109">La conversione di unità viene applicata in base al listino prezzi applicabile.</span><span class="sxs-lookup"><span data-stu-id="b5a15-109">Unit conversion is applied based on the applicable price list.</span></span>

![Stime delle risorse](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="b5a15-111">Prezzo di costo e valuta di costo predefiniti</span><span class="sxs-lookup"><span data-stu-id="b5a15-111">Default cost price and cost currency</span></span>

<span data-ttu-id="b5a15-112">I prezzi di costo vengono impostati in modo predefinito dall'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="b5a15-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="b5a15-113">Tasso di fatturazione e valuta di vendita predefiniti</span><span class="sxs-lookup"><span data-stu-id="b5a15-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="b5a15-114">I prezzi di vendita vengono applicati una volta per transazione.</span><span class="sxs-lookup"><span data-stu-id="b5a15-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="b5a15-115">La gerarchia per l'impostazione dei valori predefiniti del listino prezzi di vendita è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b5a15-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="b5a15-116">Azienda</span><span class="sxs-lookup"><span data-stu-id="b5a15-116">Organization</span></span>
2. <span data-ttu-id="b5a15-117">Cliente</span><span class="sxs-lookup"><span data-stu-id="b5a15-117">Customer</span></span>
3. <span data-ttu-id="b5a15-118">Offerta/contratto</span><span class="sxs-lookup"><span data-stu-id="b5a15-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]