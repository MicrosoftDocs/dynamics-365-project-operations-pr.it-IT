---
title: Voce di spesa (semplice)
description: Questo argomento fornisce informazioni su come lavorare con le voci di spesa in una distribuzione semplice.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121088"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="2c235-103">Voce di spesa (semplice)</span><span class="sxs-lookup"><span data-stu-id="2c235-103">Expense entry (lite)</span></span>

<span data-ttu-id="2c235-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="2c235-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2c235-105">La gestione delle spese di base, o semplice, è la capacità di registrare semplici spese.</span><span class="sxs-lookup"><span data-stu-id="2c235-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="2c235-106">È possibile registrare le spese a fronte di un progetto, quindi il responsabile dell'approvazione del progetto le esaminerà e le approverà.</span><span class="sxs-lookup"><span data-stu-id="2c235-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="2c235-107">Per ulteriori informazioni sulle funzionalità di spesa in Dynamics 365 Project Operations, vedi [Panoramica delle spese](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2c235-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="2c235-108">Acquisire una spesa di base</span><span class="sxs-lookup"><span data-stu-id="2c235-108">Capture a basic expense</span></span>

<span data-ttu-id="2c235-109">Puoi acquisire le tue spese in modo da poterle inviare al responsabile approvazione.</span><span class="sxs-lookup"><span data-stu-id="2c235-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="2c235-110">Vai a **Spese** e seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="2c235-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="2c235-111">Nella pagina **Nuova spesa** immetti le informazioni richieste sulla spesa, quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="2c235-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="2c235-112">Inviare una spesa di base</span><span class="sxs-lookup"><span data-stu-id="2c235-112">Submit a basic expense</span></span>

<span data-ttu-id="2c235-113">Dopo che hai acquisito tutte le spese e sei pronto per l'approvazione, devi inviarle.</span><span class="sxs-lookup"><span data-stu-id="2c235-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="2c235-114">Vai a **Spese** e seleziona una spesa.</span><span class="sxs-lookup"><span data-stu-id="2c235-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="2c235-115">Oppure seleziona tutte le spese utilizzando la casella di controllo nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="2c235-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="2c235-116">Seleziona **Invia**.</span><span class="sxs-lookup"><span data-stu-id="2c235-116">Select **Submit**.</span></span> <span data-ttu-id="2c235-117">Il sistema elabora le voci selezionate e quindi crea le richieste di approvazione delle spese.</span><span class="sxs-lookup"><span data-stu-id="2c235-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="2c235-118">Richiamare una spesa di base</span><span class="sxs-lookup"><span data-stu-id="2c235-118">Recall a basic expense</span></span>

<span data-ttu-id="2c235-119">Quando invii una spesa per errore, puoi richiamarla.</span><span class="sxs-lookup"><span data-stu-id="2c235-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="2c235-120">Il tempo necessario per richiamare una voce di spesa dipende dalla sua fase di approvazione.</span><span class="sxs-lookup"><span data-stu-id="2c235-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="2c235-121">Se il responsabile approvazione non ha ancora approvato la voce, il richiamo può avvenire immediatamente.</span><span class="sxs-lookup"><span data-stu-id="2c235-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="2c235-122">Tuttavia, se la voce è già stata approvata, al responsabile approvazione viene chiesto di approvare il richiamo e di stornare le transazioni.</span><span class="sxs-lookup"><span data-stu-id="2c235-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="2c235-123">Vai a **Spese**, quindi, nell'elenco delle spese, seleziona la spesa da richiamare.</span><span class="sxs-lookup"><span data-stu-id="2c235-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="2c235-124">Seleziona **Richiama**.</span><span class="sxs-lookup"><span data-stu-id="2c235-124">Select **Recall**.</span></span> <span data-ttu-id="2c235-125">Se la voce di spesa non è stata ancora approvata, il sistema la richiama immediatamente.</span><span class="sxs-lookup"><span data-stu-id="2c235-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="2c235-126">Se la voce di spesa è già stata approvata, viene creata una richiesta di richiamo per notificare al responsabile approvazione che si desidera stornare la spesa.</span><span class="sxs-lookup"><span data-stu-id="2c235-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="2c235-127">Il responsabile approvazione confermerà quindi che lo storno può essere eseguito e la voce verrà restituita.</span><span class="sxs-lookup"><span data-stu-id="2c235-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="2c235-128">Eliminare una spesa di base</span><span class="sxs-lookup"><span data-stu-id="2c235-128">Delete a basic expense</span></span>

<span data-ttu-id="2c235-129">Le spese che non sono state ancora inviate possono essere eliminate.</span><span class="sxs-lookup"><span data-stu-id="2c235-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="2c235-130">Per eliminare una spesa già inviata, è necessario prima richiamarla.</span><span class="sxs-lookup"><span data-stu-id="2c235-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c235-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c235-131">See also</span></span>

- [<span data-ttu-id="2c235-132">Panoramica delle approvazioni</span><span class="sxs-lookup"><span data-stu-id="2c235-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
