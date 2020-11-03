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
# <a name="resource-estimates"></a><span data-ttu-id="8c969-103">Stime delle risorse</span><span class="sxs-lookup"><span data-stu-id="8c969-103">Resource estimates</span></span>

<span data-ttu-id="8c969-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="8c969-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8c969-105">Le stime delle risorse provengono dal lavoro su scala cronologica definito nella struttura di suddivisione del lavoro insieme alle dimensioni di determinazione dei prezzi applicabili.</span><span class="sxs-lookup"><span data-stu-id="8c969-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="8c969-106">In genere, il calcolo è **tasso/ora per ogni ruolo x ore**.</span><span class="sxs-lookup"><span data-stu-id="8c969-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="8c969-107">Il lavoro su scala cronologica per ciascuna risorsa viene archiviato nel record di assegnazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8c969-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="8c969-108">I prezzi sono archiviati in un listino prezzi predefinito.</span><span class="sxs-lookup"><span data-stu-id="8c969-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="8c969-109">La conversione di unità viene applicata in base al listino prezzi applicabile.</span><span class="sxs-lookup"><span data-stu-id="8c969-109">Unit conversion is applied based on the applicable price list.</span></span>

![Stime delle risorse](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="8c969-111">Prezzo di costo e valuta di costo predefiniti</span><span class="sxs-lookup"><span data-stu-id="8c969-111">Default cost price and cost currency</span></span>

<span data-ttu-id="8c969-112">I prezzi di costo vengono impostati in modo predefinito dall'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="8c969-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="8c969-113">Tasso di fatturazione e valuta di vendita predefiniti</span><span class="sxs-lookup"><span data-stu-id="8c969-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="8c969-114">I prezzi di vendita vengono applicati una volta per transazione.</span><span class="sxs-lookup"><span data-stu-id="8c969-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="8c969-115">La gerarchia per l'impostazione dei valori predefiniti del listino prezzi di vendita è la seguente:</span><span class="sxs-lookup"><span data-stu-id="8c969-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="8c969-116">Azienda</span><span class="sxs-lookup"><span data-stu-id="8c969-116">Organization</span></span>
2. <span data-ttu-id="8c969-117">Cliente</span><span class="sxs-lookup"><span data-stu-id="8c969-117">Customer</span></span>
3. <span data-ttu-id="8c969-118">Offerta/contratto</span><span class="sxs-lookup"><span data-stu-id="8c969-118">Quote/contract</span></span>
