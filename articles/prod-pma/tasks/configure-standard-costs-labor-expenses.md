---
title: Configurare i costi standard per manodopera e spese
description: Questo argomento spiega come configurare i costi standard per la manodopera e le spese per un progetto.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078933"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="aa065-103">Configurare i costi standard per manodopera e spese</span><span class="sxs-lookup"><span data-stu-id="aa065-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa065-104">Questo argomento spiega come configurare i costi standard per la manodopera e le spese per un progetto.</span><span class="sxs-lookup"><span data-stu-id="aa065-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="aa065-105">Questa attività utilizza il set di dati USSI.</span><span class="sxs-lookup"><span data-stu-id="aa065-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="aa065-106">Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Prezzi > Prezzo di costo (ora)**.</span><span class="sxs-lookup"><span data-stu-id="aa065-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="aa065-107">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="aa065-107">Select **New**.</span></span>
3. <span data-ttu-id="aa065-108">Nel campo **Data di validità** , inserisci una data.</span><span class="sxs-lookup"><span data-stu-id="aa065-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="aa065-109">Nel campo **Prezzo di costo** , inserisci un numero.</span><span class="sxs-lookup"><span data-stu-id="aa065-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="aa065-110">Puoi configurare un prezzo di costo standard per la categoria del progetto oppure configurare un prezzo di costo per numero di lavoratore, numero di progetto, categoria, data o qualsiasi combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="aa065-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="aa065-111">Il prezzo di costo applicato è il prezzo di costo con il livello di dettaglio più elevato.</span><span class="sxs-lookup"><span data-stu-id="aa065-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="aa065-112">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="aa065-112">Select **Save**.</span></span>
6. <span data-ttu-id="aa065-113">Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Prezzi > Prezzo di vendita (ora)**.</span><span class="sxs-lookup"><span data-stu-id="aa065-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="aa065-114">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="aa065-114">Select **New**.</span></span>
8. <span data-ttu-id="aa065-115">Nel campo **Data di validità** , inserisci una data.</span><span class="sxs-lookup"><span data-stu-id="aa065-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="aa065-116">Nel campo **Valido per** , seleziona un'opzione.</span><span class="sxs-lookup"><span data-stu-id="aa065-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="aa065-117">Nel campo **Prezzi** , inserisci un numero.</span><span class="sxs-lookup"><span data-stu-id="aa065-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="aa065-118">Puoi configurare un prezzo di vendita standard per le transazioni orarie o per una categoria di progetto.</span><span class="sxs-lookup"><span data-stu-id="aa065-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="aa065-119">Puoi inoltre configurare i prezzi di vendita per numero lavoratore, numero progetto, categoria, data transazione o qualsiasi combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="aa065-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="aa065-120">Il prezzo di vendita effettivo, che viene applicato quando un lavoratore immette una transazione nel giornale di registrazione Ore, è il prezzo di vendita con il livello di dettaglio più elevato.</span><span class="sxs-lookup"><span data-stu-id="aa065-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="aa065-121">Ad esempio, se vengono configurati sia un prezzo di vendita generale che un prezzo di vendita specifico del lavoratore, viene utilizzato il prezzo di vendita specifico del lavoratore.</span><span class="sxs-lookup"><span data-stu-id="aa065-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="aa065-122">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="aa065-122">Select **Save**.</span></span>
12. <span data-ttu-id="aa065-123">Chiudi la pagina.</span><span class="sxs-lookup"><span data-stu-id="aa065-123">Close the page.</span></span>
13. <span data-ttu-id="aa065-124">Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Prezzi > Prezzo di costo (spesa)**.</span><span class="sxs-lookup"><span data-stu-id="aa065-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="aa065-125">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="aa065-125">Select **New**.</span></span>
15. <span data-ttu-id="aa065-126">Nel campo **Data di validità** , inserisci una data.</span><span class="sxs-lookup"><span data-stu-id="aa065-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="aa065-127">Nel campo **Prezzo di costo** , inserisci un numero.</span><span class="sxs-lookup"><span data-stu-id="aa065-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="aa065-128">È possibile compilare più campi, ma questo è il minimo necessario per salvare il record.</span><span class="sxs-lookup"><span data-stu-id="aa065-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="aa065-129">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="aa065-129">Select **Save**.</span></span>
18. <span data-ttu-id="aa065-130">Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Prezzi > Prezzo di vendita (spesa)**.</span><span class="sxs-lookup"><span data-stu-id="aa065-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="aa065-131">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="aa065-131">Select **New**.</span></span>
20. <span data-ttu-id="aa065-132">Nel campo **Data di validità** , inserisci una data.</span><span class="sxs-lookup"><span data-stu-id="aa065-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="aa065-133">Nel campo **Valido per** , seleziona un'opzione.</span><span class="sxs-lookup"><span data-stu-id="aa065-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="aa065-134">Nel campo **Prezzi** , inserisci un numero.</span><span class="sxs-lookup"><span data-stu-id="aa065-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="aa065-135">Il prezzo di vendita effettivo, che viene applicato quando un lavoratore immette le transazioni nel giornale di registrazione delle spese, è il prezzo di vendita con il livello di dettaglio più elevato.</span><span class="sxs-lookup"><span data-stu-id="aa065-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="aa065-136">Ad esempio, se vengono configurati sia un prezzo di vendita generale che un prezzo di vendita specifico del lavoratore, viene utilizzato il prezzo di vendita specifico del lavoratore.</span><span class="sxs-lookup"><span data-stu-id="aa065-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="aa065-137">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="aa065-137">Select **Save**.</span></span>

