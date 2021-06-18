---
title: Ordini di acquisto per un progetto
description: In questo articolo vengono descritti i vari metodi che puoi utilizzare per creare ordini di acquisto per un progetto. Il metodo utilizzato dipende dallo scopo dell'ordine di acquisto e da quando gli articoli vengono utilizzati e addebitati in un progetto.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999361"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="a9611-104">Ordini di acquisto per un progetto</span><span class="sxs-lookup"><span data-stu-id="a9611-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9611-105">In questo articolo vengono descritti i vari metodi che puoi utilizzare per creare ordini di acquisto per un progetto.</span><span class="sxs-lookup"><span data-stu-id="a9611-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="a9611-106">Il metodo utilizzato dipende dallo scopo dell'ordine di acquisto e da quando gli articoli vengono utilizzati e addebitati in un progetto.</span><span class="sxs-lookup"><span data-stu-id="a9611-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="a9611-107">Metodi per creare un ordine di acquisto</span><span class="sxs-lookup"><span data-stu-id="a9611-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="a9611-108">Puoi utilizzare uno dei seguenti metodi per creare un ordine di acquisto in Gestione progetti e contabilità.</span><span class="sxs-lookup"><span data-stu-id="a9611-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="a9611-109">Lo scopo dell'ordine di acquisto determina quando l'ordine di acquisto viene consumato e, di conseguenza, quando gli articoli vengono addebitati in un progetto.</span><span class="sxs-lookup"><span data-stu-id="a9611-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9611-110">Metodo</span><span class="sxs-lookup"><span data-stu-id="a9611-110">Method</span></span></th>
<th><span data-ttu-id="a9611-111">Scopo</span><span class="sxs-lookup"><span data-stu-id="a9611-111">Purpose</span></span></th>
<th><span data-ttu-id="a9611-112">Utilizzo di articoli</span><span class="sxs-lookup"><span data-stu-id="a9611-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9611-113">Crea un ordine di acquisto direttamente da un progetto.</span><span class="sxs-lookup"><span data-stu-id="a9611-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="a9611-114">Utilizza questo metodo per acquistare articoli da un fornitore esterno per l'utilizzo in un progetto.</span><span class="sxs-lookup"><span data-stu-id="a9611-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="a9611-115">L'ordine di acquisto può essere creato in due modi:</span><span class="sxs-lookup"><span data-stu-id="a9611-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="a9611-116">Dal progetto stesso.</span><span class="sxs-lookup"><span data-stu-id="a9611-116">From the project itself.</span></span> <span data-ttu-id="a9611-117">In questo caso, il progetto è già definito per l'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="a9611-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="a9611-118">Mediante accesso all'ordine di acquisto del progetto.</span><span class="sxs-lookup"><span data-stu-id="a9611-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="a9611-119">Devi selezionare sia il fornitore che il progetto per cui creare l'ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="a9611-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="a9611-120">Gli articoli vengono utilizzati quando la fattura fornitore viene aggiornata.</span><span class="sxs-lookup"><span data-stu-id="a9611-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9611-121">Crea un ordine di acquisto da un ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="a9611-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="a9611-122">Utilizza questo metodo per acquistare articoli quando crei un ordine di vendita da un progetto.</span><span class="sxs-lookup"><span data-stu-id="a9611-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="a9611-123">Gli articoli vengono utilizzati quando l'ordine di vendita viene fatturato al cliente.</span><span class="sxs-lookup"><span data-stu-id="a9611-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9611-124">Crea un ordine di acquisto da un requisito articolo.</span><span class="sxs-lookup"><span data-stu-id="a9611-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="a9611-125">Utilizza questo metodo per acquistare articoli quando crei un requisito articolo da un progetto.</span><span class="sxs-lookup"><span data-stu-id="a9611-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="a9611-126">Gli articoli vengono utilizzati quando viene aggiornato il documento di trasporto del requisito articolo.</span><span class="sxs-lookup"><span data-stu-id="a9611-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="a9611-127">Quando aggiorni la fattura fornitore o il documento di trasporto, viene richiesto di aggiornare il documento di trasporto relativo al requisito dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="a9611-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="a9611-128">Per altre informazioni, vedi [Ricevere gli articoli nell'ordine di acquisto dal requisito dell'articolo](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="a9611-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]