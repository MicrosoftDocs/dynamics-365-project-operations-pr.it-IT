---
title: Esaminare il backlog di fatturazione in progetti e contratti di progetto
description: In questo argomento vengono fornite informazioni su come esaminare backlog relativi a tempo, spese e prodotti e su come contrassegnarli come pronti per la fatturazione.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079085"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="48046-103">Esaminare il backlog di fatturazione in progetti e contratti di progetto</span><span class="sxs-lookup"><span data-stu-id="48046-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="48046-104">Quando una transazione è pronta affinché una fattura venga creata ed elaborata, la transazione deve essere contrassegnata con **Pronta per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="48046-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="48046-105">In questo argomento vengono descritti i tipi di transazioni che è possibile creare.</span><span class="sxs-lookup"><span data-stu-id="48046-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="48046-106">Esaminare il backlog di fatturazione di tempo e materiali</span><span class="sxs-lookup"><span data-stu-id="48046-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="48046-107">Quando un inserimento ore o una voce di spesa viene inviata e approvata per un progetto, PSA crea un valore effettivo del progetto.</span><span class="sxs-lookup"><span data-stu-id="48046-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="48046-108">Se la combinazione di progetto e classe di transazione è mappata a una voce di contratto per un progetto tempo e materiali, vengono creati due valori effettivi quando la voce viene approvata:</span><span class="sxs-lookup"><span data-stu-id="48046-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="48046-109">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="48046-109">Cost actual</span></span> 
- <span data-ttu-id="48046-110">Valore effettivo vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="48046-110">Unbilled sales actual</span></span>

<span data-ttu-id="48046-111">I valori effettivi di vendite non fatturate rappresentano il backlog di fatturazione e il relativo stato di fatturazione deve essere impostato su **Pronto per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="48046-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="48046-112">Quando una fattura di progetto viene creata, i valori effettivi di vendite non fatturate contrassegnati con **Pronto per la fatturazione** vengono copiati come dettagli della riga fattura.</span><span class="sxs-lookup"><span data-stu-id="48046-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="48046-113">Per esaminare il backlog di fatturazione per tempo e materiali, seleziona **Vendite** \> **Fatturazione** \> **Backlog di fatturazione tempo e materiali**.</span><span class="sxs-lookup"><span data-stu-id="48046-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="48046-114">Seleziona tutti i valori effettivi di vendite non fatturate pronti per essere fatturati e quindi seleziona **Pronto per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="48046-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="48046-115">Lo stato di fatturazione di questi valori effettivi diventa **Pronto per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="48046-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Backlog di fatturazione tempo e materiale](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="48046-117">Esaminare il backlog di fatturazione prodotto</span><span class="sxs-lookup"><span data-stu-id="48046-117">Review the product billing backlog</span></span>

<span data-ttu-id="48046-118">In PSA, quando un contratto di progetto include voci di contratto basate su prodotto, tali voci vengono considerate per la fatturazione ogni volta che viene creata una fattura per il contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="48046-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="48046-119">Qualsiasi prodotto con voci di contratto contrassegnate con **Pronto per la fatturazione** viene copiato nella fattura di progetto come righe fattura di progetto.</span><span class="sxs-lookup"><span data-stu-id="48046-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="48046-120">Per esaminare il backlog di fatturazione per i prodotti, seleziona **Vendite** \> **Fatturazione** \> **Backlog di fatturazione prodotto**.</span><span class="sxs-lookup"><span data-stu-id="48046-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="48046-121">Seleziona tutte le voci di contratto basate su prodotto pronte per essere fatturate e quindi seleziona **Pronto per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="48046-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="48046-122">Lo stato di fatturazione di queste righe diventa **Pronto per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="48046-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Backlog di fatturazione prodotto](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="48046-124">Esaminare i passaggi fondamentali di fatturazione in contratti a prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="48046-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="48046-125">Ogni voce di contratto di progetto con un metodo di fatturazione a prezzo fisso deve definire i passaggi fondamentali del contratto.</span><span class="sxs-lookup"><span data-stu-id="48046-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="48046-126">Questi passaggi fondamentali possono essere fatturati solo se sono contrassegnati come **Pronto per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="48046-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="48046-127">Per esaminare i passaggi fondamentali di fatturazione, seleziona **Vendite** \> **Fatturazione** \> **Passaggi fondamentali prezzo fisso**.</span><span class="sxs-lookup"><span data-stu-id="48046-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="48046-128">Seleziona i passaggi fondamentali che sono pronti per essere fatturati e quindi seleziona **Pronto per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="48046-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="48046-129">Lo stato di fatturazione di questi passaggi fondamentali diventa **Pronto per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="48046-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Passaggi fondamentali prezzo fisso](media/FPBacklog.png)
