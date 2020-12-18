---
title: Voce di spesa (semplice)
description: Questo argomento fornisce informazioni su come lavorare con le voci di spesa in una distribuzione semplice.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590951"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="6e256-103">Voce di spesa (semplice)</span><span class="sxs-lookup"><span data-stu-id="6e256-103">Expense entry (lite)</span></span>

<span data-ttu-id="6e256-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="6e256-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6e256-105">La gestione delle spese di base, o semplice, è la capacità di registrare semplici spese.</span><span class="sxs-lookup"><span data-stu-id="6e256-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="6e256-106">È possibile registrare le spese a fronte di un progetto, quindi il responsabile dell'approvazione del progetto le esaminerà e le approverà.</span><span class="sxs-lookup"><span data-stu-id="6e256-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="6e256-107">Per ulteriori informazioni sulle funzionalità di spesa in Dynamics 365 Project Operations, vedi [Panoramica delle spese](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6e256-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="6e256-108">Acquisire una spesa di base</span><span class="sxs-lookup"><span data-stu-id="6e256-108">Capture a basic expense</span></span>

<span data-ttu-id="6e256-109">Puoi acquisire le tue spese in modo da poterle inviare al responsabile approvazione.</span><span class="sxs-lookup"><span data-stu-id="6e256-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="6e256-110">Vai a **Spese** e seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="6e256-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="6e256-111">Nella pagina **Nuova spesa** immetti le informazioni richieste sulla spesa, quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="6e256-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="6e256-112">Inviare una spesa di base</span><span class="sxs-lookup"><span data-stu-id="6e256-112">Submit a basic expense</span></span>

<span data-ttu-id="6e256-113">Dopo che hai acquisito tutte le spese e sei pronto per l'approvazione, devi inviarle.</span><span class="sxs-lookup"><span data-stu-id="6e256-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="6e256-114">Vai a **Spese** e seleziona una spesa.</span><span class="sxs-lookup"><span data-stu-id="6e256-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="6e256-115">Oppure seleziona tutte le spese utilizzando la casella di controllo nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="6e256-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="6e256-116">Seleziona **Invia**.</span><span class="sxs-lookup"><span data-stu-id="6e256-116">Select **Submit**.</span></span> <span data-ttu-id="6e256-117">Il sistema elabora le voci selezionate e quindi crea le richieste di approvazione delle spese.</span><span class="sxs-lookup"><span data-stu-id="6e256-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="6e256-118">Aggiungi un allegato</span><span class="sxs-lookup"><span data-stu-id="6e256-118">Add an attachment</span></span>

<span data-ttu-id="6e256-119">Potrebbe essere necessario fornire al revisore documentazione aggiuntiva sulle spese.</span><span class="sxs-lookup"><span data-stu-id="6e256-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="6e256-120">È possibile allegare una ricevuta nella cronologia della voce di spesa.</span><span class="sxs-lookup"><span data-stu-id="6e256-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="6e256-121">Seleziona **Modifica** e nella sezione **Sequenza temporale**, quindi seleziona l'icona della graffetta per allegare la ricevuta.</span><span class="sxs-lookup"><span data-stu-id="6e256-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="6e256-122">Richiamare una spesa di base</span><span class="sxs-lookup"><span data-stu-id="6e256-122">Recall a basic expense</span></span>

<span data-ttu-id="6e256-123">Quando invii una spesa per errore, puoi richiamarla.</span><span class="sxs-lookup"><span data-stu-id="6e256-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="6e256-124">Il tempo necessario per richiamare una voce di spesa dipende dalla sua fase di approvazione.</span><span class="sxs-lookup"><span data-stu-id="6e256-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="6e256-125">Se il responsabile approvazione non ha ancora approvato la voce, il richiamo può avvenire immediatamente.</span><span class="sxs-lookup"><span data-stu-id="6e256-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="6e256-126">Tuttavia, se la voce è già stata approvata, al responsabile approvazione viene chiesto di approvare il richiamo e di stornare le transazioni.</span><span class="sxs-lookup"><span data-stu-id="6e256-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="6e256-127">Vai a **Spese**, quindi, nell'elenco delle spese, seleziona la spesa da richiamare.</span><span class="sxs-lookup"><span data-stu-id="6e256-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="6e256-128">Seleziona **Richiama**.</span><span class="sxs-lookup"><span data-stu-id="6e256-128">Select **Recall**.</span></span> <span data-ttu-id="6e256-129">Se la voce di spesa non è stata ancora approvata, il sistema la richiama immediatamente.</span><span class="sxs-lookup"><span data-stu-id="6e256-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="6e256-130">Se la voce di spesa è già stata approvata, viene creata una richiesta di richiamo per notificare al responsabile approvazione che si desidera stornare la spesa.</span><span class="sxs-lookup"><span data-stu-id="6e256-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="6e256-131">Il responsabile approvazione confermerà quindi che lo storno può essere eseguito e la voce verrà restituita.</span><span class="sxs-lookup"><span data-stu-id="6e256-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="6e256-132">Eliminare una spesa di base</span><span class="sxs-lookup"><span data-stu-id="6e256-132">Delete a basic expense</span></span>

<span data-ttu-id="6e256-133">Le spese che non sono state ancora inviate possono essere eliminate.</span><span class="sxs-lookup"><span data-stu-id="6e256-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="6e256-134">Per eliminare una spesa già inviata, è necessario prima richiamarla.</span><span class="sxs-lookup"><span data-stu-id="6e256-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e256-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e256-135">See also</span></span>

- [<span data-ttu-id="6e256-136">Panoramica delle approvazioni</span><span class="sxs-lookup"><span data-stu-id="6e256-136">Approvals overview</span></span>](../approvals/approvals-overview.md)
