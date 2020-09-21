---
title: Ricevere gli articoli nell'ordine di acquisto dal requisito dell'articolo
description: Questo argomento spiega come ricevere articoli in un ordine di acquisto da un requisito articolo.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752581"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="6ca18-103">Ricevere gli articoli nell'ordine di acquisto dal requisito dell'articolo</span><span class="sxs-lookup"><span data-stu-id="6ca18-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ca18-104">Questo argomento spiega come ricevere articoli in un ordine di acquisto da un requisito articolo.</span><span class="sxs-lookup"><span data-stu-id="6ca18-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="6ca18-105">Utilizzando un requisito articolo invece di una transazione articolo, è possibile pianificare la consegna appena prima che l'articolo venga effettivamente utilizzato, creare un ordine di acquisto, includere l'articolo nel quadro dell'accordo commerciale e includere il requisito articolo nella pianificazione della produzione.</span><span class="sxs-lookup"><span data-stu-id="6ca18-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="6ca18-106">Questa attività utilizza il set di dati USSI.</span><span class="sxs-lookup"><span data-stu-id="6ca18-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="6ca18-107">Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Progetti > Tutti i progetti**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="6ca18-108">Nell'elenco, seleziona il collegamento nella riga desiderata.</span><span class="sxs-lookup"><span data-stu-id="6ca18-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="6ca18-109">Nel riquadro Azioni seleziona **Piano**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="6ca18-110">Seleziona **Requisiti articolo**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="6ca18-111">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-111">Select **New**.</span></span>
6. <span data-ttu-id="6ca18-112">Nella nuova riga, inserisci o seleziona un valore nel campo **Codice articolo**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="6ca18-113">Nel campo **Quantità**, inserisci un numero.</span><span class="sxs-lookup"><span data-stu-id="6ca18-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="6ca18-114">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-114">Select **Save**.</span></span>
9. <span data-ttu-id="6ca18-115">Nel riquadro Azioni seleziona **Gestisci**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="6ca18-116">Seleziona **Funzioni**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-116">Select **Functions**.</span></span>
11. <span data-ttu-id="6ca18-117">Seleziona **Crea ordine di acquisto**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="6ca18-118">Seleziona la casella di controllo **Includi tutto**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="6ca18-119">Nel campo **Account fornitore**, inserisci o seleziona un valore.</span><span class="sxs-lookup"><span data-stu-id="6ca18-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="6ca18-120">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-120">Select **OK**.</span></span>
15. <span data-ttu-id="6ca18-121">Nel riquadro di spostamento, vai a **Moduli > Contabilità fornitori > Ordini fornitore > Tutti gli ordini fornitore**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="6ca18-122">Nell'elenco, seleziona il collegamento nella riga desiderata.</span><span class="sxs-lookup"><span data-stu-id="6ca18-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="6ca18-123">Nel riquadro Azioni seleziona **Acquista**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="6ca18-124">Seleziona **Conferma**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="6ca18-125">Nel riquadro Azioni seleziona **Ricevi**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="6ca18-126">Seleziona **Entrata prodotti**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="6ca18-127">Nel campo **Entrata prodotti**, digita un valore.</span><span class="sxs-lookup"><span data-stu-id="6ca18-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="6ca18-128">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ca18-128">Select **OK**.</span></span>

