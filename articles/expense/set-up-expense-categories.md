---
title: Configurare le categorie di spesa
description: Questo argomento fornisce informazioni su come configurare le categorie di spesa e le categorie condivise per le note spese.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276128"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="eccad-103">Configurare le categorie di spesa</span><span class="sxs-lookup"><span data-stu-id="eccad-103">Set up expense categories</span></span>

<span data-ttu-id="eccad-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="eccad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eccad-105">Quando i dipendenti creano note spese, ogni spesa che registrano deve essere associata a una categoria di spesa.</span><span class="sxs-lookup"><span data-stu-id="eccad-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="eccad-106">Le categorie di spesa derivano da categorie condivise che possono essere condivise tra le persone giuridiche dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="eccad-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="eccad-107">A seconda di come è definita l'organizzazione, queste categorie di spesa possono essere condivise anche in altre aree.</span><span class="sxs-lookup"><span data-stu-id="eccad-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="eccad-108">In base alla definizione dell'organizzazione e alle linee guida del team di implementazione, è necessario determinare se le categorie utilizzate nella gestione delle spese verranno utilizzate solo in Gestione spese o debbano essere condivise in altre aree.</span><span class="sxs-lookup"><span data-stu-id="eccad-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="eccad-109">Queste categorie possono essere condivise tra Gestione progetti e contabilità e Gestione spese oppure tra Gestione progetti e contabilità e Produzione.</span><span class="sxs-lookup"><span data-stu-id="eccad-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="eccad-110">Tuttavia, non possono essere condivise tra Gestione spese e Produzione.</span><span class="sxs-lookup"><span data-stu-id="eccad-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="eccad-111">Prima di poter iniziare il processo di configurazione, è necessario prendere le seguenti decisioni per ciascuna categoria di spesa:</span><span class="sxs-lookup"><span data-stu-id="eccad-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="eccad-112">Qual è la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="eccad-112">What is the expense category?</span></span> <span data-ttu-id="eccad-113">Gli esempi includono categorie per voli, hotel o chilometraggio.</span><span class="sxs-lookup"><span data-stu-id="eccad-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="eccad-114">La categoria di spesa può essere utilizzata anche in Gestione progetti e contabilità?</span><span class="sxs-lookup"><span data-stu-id="eccad-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="eccad-115">In caso affermativo, devi anche prendere le decisioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="eccad-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="eccad-116">Quali conti di costo verranno utilizzati per le seguenti spese?</span><span class="sxs-lookup"><span data-stu-id="eccad-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="eccad-117">Costo</span><span class="sxs-lookup"><span data-stu-id="eccad-117">Cost</span></span>
        - <span data-ttu-id="eccad-118">Allocazione retribuzioni</span><span class="sxs-lookup"><span data-stu-id="eccad-118">Payroll allocation</span></span>
        - <span data-ttu-id="eccad-119">WIP - valore costo</span><span class="sxs-lookup"><span data-stu-id="eccad-119">WIP-cost value</span></span>
        - <span data-ttu-id="eccad-120">Elemento di costo</span><span class="sxs-lookup"><span data-stu-id="eccad-120">Cost-item</span></span>
        - <span data-ttu-id="eccad-121">WIP - elemento valore di costo</span><span class="sxs-lookup"><span data-stu-id="eccad-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="eccad-122">Perdita maturata</span><span class="sxs-lookup"><span data-stu-id="eccad-122">Accrued loss</span></span>
        - <span data-ttu-id="eccad-123">WIP - perdita maturata</span><span class="sxs-lookup"><span data-stu-id="eccad-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="eccad-124">Quali conti ricavi verranno utilizzati per le seguenti fonti di ricavi?</span><span class="sxs-lookup"><span data-stu-id="eccad-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="eccad-125">Ricavi fatturati</span><span class="sxs-lookup"><span data-stu-id="eccad-125">Invoiced revenue</span></span>
        - <span data-ttu-id="eccad-126">Ricavi maturati - valore delle vendite</span><span class="sxs-lookup"><span data-stu-id="eccad-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="eccad-127">WIP - valore delle vendite</span><span class="sxs-lookup"><span data-stu-id="eccad-127">WIP-sales value</span></span>
        - <span data-ttu-id="eccad-128">Ricavi maturati - produzione</span><span class="sxs-lookup"><span data-stu-id="eccad-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="eccad-129">WIP - produzione</span><span class="sxs-lookup"><span data-stu-id="eccad-129">WIP-production</span></span>
        - <span data-ttu-id="eccad-130">Ricavi maturati - profitti</span><span class="sxs-lookup"><span data-stu-id="eccad-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="eccad-131">WIP - profitti</span><span class="sxs-lookup"><span data-stu-id="eccad-131">WIP-profit</span></span>
        - <span data-ttu-id="eccad-132">Ricavi maturati - abbonamento</span><span class="sxs-lookup"><span data-stu-id="eccad-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="eccad-133">WIP - abbonamento</span><span class="sxs-lookup"><span data-stu-id="eccad-133">WIP-subscription</span></span>

- <span data-ttu-id="eccad-134">Qual è il tipo di spesa?</span><span class="sxs-lookup"><span data-stu-id="eccad-134">What is the expense type?</span></span>
- <span data-ttu-id="eccad-135">Qual è il metodo di pagamento predefinito per la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="eccad-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="eccad-136">Le spese nella categoria di spesa devono essere dettagliate?</span><span class="sxs-lookup"><span data-stu-id="eccad-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="eccad-137">Qual è il conto predefinito principale per la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="eccad-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="eccad-138">Qual è la fascia IVA articoli predefinita per la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="eccad-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="eccad-139">Sono consentiti metodi di pagamento aggiuntivi per la categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="eccad-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="eccad-140">In caso affermativo, quali?</span><span class="sxs-lookup"><span data-stu-id="eccad-140">If so, what are they?</span></span>
- <span data-ttu-id="eccad-141">Ci sono sottocategorie in questa categoria di spesa?</span><span class="sxs-lookup"><span data-stu-id="eccad-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="eccad-142">In caso affermativo, devi anche prendere le decisioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="eccad-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="eccad-143">Alcune delle sottocategorie sono escluse dal recupero IVA?</span><span class="sxs-lookup"><span data-stu-id="eccad-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="eccad-144">Qual è la fascia IVA articoli delle sottocategorie?</span><span class="sxs-lookup"><span data-stu-id="eccad-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]