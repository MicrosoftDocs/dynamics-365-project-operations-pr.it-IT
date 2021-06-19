---
title: Disattivare una dimensione di determinazione dei prezzi
description: In questo argomento viene descritto come configurare dimensioni di determinazione dei prezzi nella soluzione Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014301"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="2e71d-103">Disattivare una dimensione di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="2e71d-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2e71d-104">È possibile che sia necessario esaminare e aggiornare regolarmente la strategia di determinazione dei prezzi dopo alcuni anni.</span><span class="sxs-lookup"><span data-stu-id="2e71d-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="2e71d-105">L'aggiornamento potrebbe richiedere la disattivazione di una dimensione di determinazione dei prezzi esistente e la creazione di una nuova dimensione.</span><span class="sxs-lookup"><span data-stu-id="2e71d-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="2e71d-106">Ad esempio, è possibile che in precedenza si siano determinati i prezzi per **Ruolo**, ma che ora si intenda farlo per **Esperienza di lavoro**.</span><span class="sxs-lookup"><span data-stu-id="2e71d-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="2e71d-107">Ciò può richiedere la disattivazione di **Ruolo** come dimensione di determinazione dei prezzi e la creazione di **Esperienza di lavoro** come nuova dimensione di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="2e71d-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="2e71d-108">Per disattivare la dimensione di determinazione dei prezzi, indipendentemente dal fatto che sia predefinita o personalizzata, impostare i campi **Vendite applicabili a** e **Costo applicabile a** della dimensione di determinazione dei prezzi su **No**.</span><span class="sxs-lookup"><span data-stu-id="2e71d-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="2e71d-109">Tuttavia, quando si esegue tale operazione, potrebbe essere visualizzato il messaggio di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="2e71d-109">However, when you do this, you might receive the following error message.</span></span>

![Errore processo aziendale probabile quando si disattiva una dimensione di determinazione dei prezzi](media/Business-Process-Error.png)


<span data-ttu-id="2e71d-111">Questo messaggio di errore indica che vi sono record di prezzi impostati precedentemente per la dimensione che si sta disattivando.</span><span class="sxs-lookup"><span data-stu-id="2e71d-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="2e71d-112">Tutti i record **Prezzo ruolo** e **Ricarico prezzo ruolo** che fanno riferimento a una dimensione devono essere eliminati prima di impostare l'applicabilità della dimensione su **No**.</span><span class="sxs-lookup"><span data-stu-id="2e71d-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="2e71d-113">Tale regola si applica alle dimensioni di determinazione dei prezzi predefinite e a quelle personalizzate eventualmente create.</span><span class="sxs-lookup"><span data-stu-id="2e71d-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="2e71d-114">Il motivo di questa convalida è dovuto al fatto che Project Service presenta un vincolo secondo il quale ogni record **Prezzo ruolo** deve avere una combinazione univoca di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="2e71d-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="2e71d-115">Ad esempio, in un listino denominato **Tasso di costo USA 2018**, si hanno le seguenti righe **Prezzo ruolo**.</span><span class="sxs-lookup"><span data-stu-id="2e71d-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="2e71d-116">Titolo standard</span><span class="sxs-lookup"><span data-stu-id="2e71d-116">Standard Title</span></span>         | <span data-ttu-id="2e71d-117">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="2e71d-117">Org Unit</span></span>    |<span data-ttu-id="2e71d-118">Unità</span><span class="sxs-lookup"><span data-stu-id="2e71d-118">Unit</span></span>   |<span data-ttu-id="2e71d-119">Prezzo</span><span class="sxs-lookup"><span data-stu-id="2e71d-119">Price</span></span>  |<span data-ttu-id="2e71d-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="2e71d-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="2e71d-121">Sistemista</span><span class="sxs-lookup"><span data-stu-id="2e71d-121">Systems Engineer</span></span>|<span data-ttu-id="2e71d-122">Contoso (USA)</span><span class="sxs-lookup"><span data-stu-id="2e71d-122">Contoso US</span></span>|<span data-ttu-id="2e71d-123">Ora</span><span class="sxs-lookup"><span data-stu-id="2e71d-123">Hour</span></span>| <span data-ttu-id="2e71d-124">100</span><span class="sxs-lookup"><span data-stu-id="2e71d-124">100</span></span>|<span data-ttu-id="2e71d-125">USD</span><span class="sxs-lookup"><span data-stu-id="2e71d-125">USD</span></span>|
| <span data-ttu-id="2e71d-126">Sistemista esperto</span><span class="sxs-lookup"><span data-stu-id="2e71d-126">Senior Systems Engineer</span></span>|<span data-ttu-id="2e71d-127">Contoso (USA)</span><span class="sxs-lookup"><span data-stu-id="2e71d-127">Contoso US</span></span>|<span data-ttu-id="2e71d-128">Ora</span><span class="sxs-lookup"><span data-stu-id="2e71d-128">Hour</span></span>| <span data-ttu-id="2e71d-129">150</span><span class="sxs-lookup"><span data-stu-id="2e71d-129">150</span></span>| <span data-ttu-id="2e71d-130">USD</span><span class="sxs-lookup"><span data-stu-id="2e71d-130">USD</span></span>|


<span data-ttu-id="2e71d-131">Quando si disattiva **Titolo standard** come dimensione di determinazione dei prezzi e il motore di determinazione dei prezzi di Project Service cerca un prezzo, questo utilizzerà solo il valore **Unità organizzativa** del contesto di input.</span><span class="sxs-lookup"><span data-stu-id="2e71d-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="2e71d-132">Se l'**Unità organizzativa** del contesto di input è "Contoso US", il risultato sarà non deterministico in quanto entrambe le righe corrisponderanno.</span><span class="sxs-lookup"><span data-stu-id="2e71d-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="2e71d-133">Per evitare questo scenario, quando si creano record **Prezzo ruolo**, Project Service verifica che la combinazione di dimensioni è univoca.</span><span class="sxs-lookup"><span data-stu-id="2e71d-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="2e71d-134">Se la dimensione viene disattivata dopo la creazione dei record **Prezzo ruolo**, il vincolo può essere violato.</span><span class="sxs-lookup"><span data-stu-id="2e71d-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="2e71d-135">Pertanto, prima di disattivare una dimensione, è necessario eliminare tutte le righe **Ricarico prezzo ruolo** e **Prezzo ruolo** in cui è presente il valore della dimensione.</span><span class="sxs-lookup"><span data-stu-id="2e71d-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]