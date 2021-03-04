---
title: Richiamare inserimenti ore o voci di spesa approvati
description: In questo argomento vengono fornite informazioni su come richiamare una transazione di tempo o spesa approvata precedentemente.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147844"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="4f096-103">Richiamare inserimenti ore o voci di spesa approvati</span><span class="sxs-lookup"><span data-stu-id="4f096-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4f096-104">Un membro del team di progetto o un'altra persona che invia un inserimento ore o una voce di spesa può richiamare tale inserimento o voce dopo l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="4f096-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="4f096-105">La procedura per richiamare un inserimento ore o una voce di spesa approvato comporta due passaggi:</span><span class="sxs-lookup"><span data-stu-id="4f096-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="4f096-106">L'autore dell'invio richiede un richiamo.</span><span class="sxs-lookup"><span data-stu-id="4f096-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="4f096-107">Un responsabile approvazione approva il richiamo.</span><span class="sxs-lookup"><span data-stu-id="4f096-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="4f096-108">Richiedere un richiamo</span><span class="sxs-lookup"><span data-stu-id="4f096-108">Request a recall</span></span>

<span data-ttu-id="4f096-109">Segui questi passaggi per richiedere il richiamo di un inserimento ore o una voce di spesa approvato.</span><span class="sxs-lookup"><span data-stu-id="4f096-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="4f096-110">Per gli inserimenti ore, seleziona **Progetti** \> **Attività personali** \> **Inserimento ore**.</span><span class="sxs-lookup"><span data-stu-id="4f096-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="4f096-111">OPPURE</span><span class="sxs-lookup"><span data-stu-id="4f096-111">–or–</span></span>

    <span data-ttu-id="4f096-112">Per le voci di spesa, seleziona **Progetti** \> **Attività personali** \> **Spese**.</span><span class="sxs-lookup"><span data-stu-id="4f096-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="4f096-113">Per gli inserimenti ore, seleziona tutti gli inserimenti di una specifica combinazione di progetto e attività.</span><span class="sxs-lookup"><span data-stu-id="4f096-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="4f096-114">In alternativa, nella griglia, seleziona le singole celle di tempo a una data specifica per un progetto specifico.</span><span class="sxs-lookup"><span data-stu-id="4f096-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="4f096-115">OPPURE</span><span class="sxs-lookup"><span data-stu-id="4f096-115">–or–</span></span>

    <span data-ttu-id="4f096-116">Per le voci di spesa, seleziona la riga della voce di spesa da richiamare.</span><span class="sxs-lookup"><span data-stu-id="4f096-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="4f096-117">Seleziona **Richiama**.</span><span class="sxs-lookup"><span data-stu-id="4f096-117">Select **Recall**.</span></span> <span data-ttu-id="4f096-118">Viene visualizzata una finestra di dialogo di conferma.</span><span class="sxs-lookup"><span data-stu-id="4f096-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="4f096-119">Se l'inserimento ore e la voce di spesa selezionati sono già stati approvati, ti viene richiesto di immettere un motivo per il richiamo.</span><span class="sxs-lookup"><span data-stu-id="4f096-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="4f096-120">Immetti un motivo per il richiamo e quindi seleziona **OK** per confermare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4f096-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="4f096-121">Il sistema invia alla persona che ha approvato la voce di spesa o l'inserimento ore una richiesta di approvazione del richiamo.</span><span class="sxs-lookup"><span data-stu-id="4f096-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="4f096-122">Sebbene sia possibile richiamare inserimenti ore e voci di spesa, se uno di questi è già stato fatturato al cliente, una richiesta di richiamo non può essere creata.</span><span class="sxs-lookup"><span data-stu-id="4f096-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="4f096-123">Un utente che cerca di creare una richiesta di richiamo riceverà un messaggio indicante che l'inserimento ore o la voce di spesa non può essere richiamato in quanto è già stata fatturato.</span><span class="sxs-lookup"><span data-stu-id="4f096-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="4f096-124">Approvare o rifiutare una richiesta di richiamo</span><span class="sxs-lookup"><span data-stu-id="4f096-124">Approve or reject a recall request</span></span>

<span data-ttu-id="4f096-125">Segui questi passaggi per approvare o rifiutare una richiesta di richiamo.</span><span class="sxs-lookup"><span data-stu-id="4f096-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="4f096-126">Seleziona **Progetti** \> **Attività personali** \> **Approvazioni**.</span><span class="sxs-lookup"><span data-stu-id="4f096-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="4f096-127">Nella pagina elenco **Approvazioni**, seleziona la vista **Richieste di richiamo da approvare**.</span><span class="sxs-lookup"><span data-stu-id="4f096-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="4f096-128">Viene visualizzato un elenco di richieste di richiamo.</span><span class="sxs-lookup"><span data-stu-id="4f096-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="4f096-129">Seleziona uno o più inserimenti o voci e quindi seleziona **Approva** o **Rifiuta**.</span><span class="sxs-lookup"><span data-stu-id="4f096-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="4f096-130">Se selezioni **Approva**, viene visualizzato un messaggio di avviso che spiega l'impatto dell'approvazione.</span><span class="sxs-lookup"><span data-stu-id="4f096-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="4f096-131">Seleziona **OK** per confermare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4f096-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="4f096-132">La richiesta di richiamo viene approvata.</span><span class="sxs-lookup"><span data-stu-id="4f096-132">The recall request is approved.</span></span>

    <span data-ttu-id="4f096-133">OPPURE</span><span class="sxs-lookup"><span data-stu-id="4f096-133">–or–</span></span>

    <span data-ttu-id="4f096-134">Se hai selezionato **Rifiuta**, la richiesta di richiamo viene rifiutata.</span><span class="sxs-lookup"><span data-stu-id="4f096-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="4f096-135">Come avviene quando si richiede un richiamo, anche per l'approvazione di un richiamo il sistema verifica le attività di fatturazione negli inserimenti ore o nelle voci di spesa.</span><span class="sxs-lookup"><span data-stu-id="4f096-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="4f096-136">Se un inserimento ore o una voce di spesa è già stata fatturato o se si trova in una bozza di fattura, il responsabile approvazione riceve un messaggio di errore che indica che l'inserimento ore o la voce di spesa non può essere approvato in quanto è già stato fatturato.</span><span class="sxs-lookup"><span data-stu-id="4f096-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="4f096-137">Impatto di una richiesta di richiamo</span><span class="sxs-lookup"><span data-stu-id="4f096-137">Impact of a recall request</span></span>

<span data-ttu-id="4f096-138">Quando un'approvazione viene richiamata, si ha un impatto operativo e un impatto finanziario.</span><span class="sxs-lookup"><span data-stu-id="4f096-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="4f096-139">Impatto operativo</span><span class="sxs-lookup"><span data-stu-id="4f096-139">Operational impact</span></span>

<span data-ttu-id="4f096-140">Se una richiesta di richiamo viene approvata, il record dell'approvazione viene contrassegnato come **Rifiutato**.</span><span class="sxs-lookup"><span data-stu-id="4f096-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="4f096-141">Lo stato dell'inserimento ore o della voce di spesa diventa **Restituito** o **Rifiutato**, a seconda se si tratta di un inserimento ore o di una voce di spesa.</span><span class="sxs-lookup"><span data-stu-id="4f096-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="4f096-142">Il membro del team di progetto può visualizzare, modificare e quindi inviare di nuovo l'inserimento ore o la voce di spesa oppure eliminarlo completamente.</span><span class="sxs-lookup"><span data-stu-id="4f096-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="4f096-143">Se una richiesta di richiamo viene rifiutata, lo stato dell'inserimento ore o della voce di spesa rimane **Approvato** e l'inserimento o la voce non può essere modificato dal membro del team di progetto o dal responsabile approvazione per il progetto.</span><span class="sxs-lookup"><span data-stu-id="4f096-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="4f096-144">Impatto finanziario</span><span class="sxs-lookup"><span data-stu-id="4f096-144">Financial impact</span></span>

<span data-ttu-id="4f096-145">Se una richiesta di richiamo viene approvata, i valori effettivi corrispondenti per costo e vendite vengono aggiornati nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="4f096-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="4f096-146">Il campo **Stato rettifica** diventa **Rettificato**.</span><span class="sxs-lookup"><span data-stu-id="4f096-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="4f096-147">Il campo **Stato fatturazione** diventa **Annullato**.</span><span class="sxs-lookup"><span data-stu-id="4f096-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="4f096-148">Quindi, nella tabella Valori effettivi vengono create scritture di storno.</span><span class="sxs-lookup"><span data-stu-id="4f096-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="4f096-149">Per creare scritture di storno, il sistema copia i valori di campo dai valori effettivi originali.</span><span class="sxs-lookup"><span data-stu-id="4f096-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="4f096-150">I soli valori che non vengono copiati sono i valori di quantità.</span><span class="sxs-lookup"><span data-stu-id="4f096-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="4f096-151">Questi valori vengono invece stornati.</span><span class="sxs-lookup"><span data-stu-id="4f096-151">These values are reversed instead.</span></span> <span data-ttu-id="4f096-152">Valori effettivi stornati vengono creati per i valori effettivi **Costo** e **Vendite non fatturate**.</span><span class="sxs-lookup"><span data-stu-id="4f096-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="4f096-153">Il campo **Stato rettifica** dei valori effettivi stornati viene impostato su **Non rettificabile** e il campo **Stato di fatturazione** viene impostato su **Annullato**.</span><span class="sxs-lookup"><span data-stu-id="4f096-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="4f096-154">A seguito di tali modifiche, la spesa registrata e il backlog dei ricavi del progetto non includono più gli importi che questi valori effettivi rappresentano.</span><span class="sxs-lookup"><span data-stu-id="4f096-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="4f096-155">Se una richiesta di richiamo viene rifiutata, non si ha alcun impatto finanziario sul progetto.</span><span class="sxs-lookup"><span data-stu-id="4f096-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="4f096-156">Modifiche ai record degli inserimenti ore</span><span class="sxs-lookup"><span data-stu-id="4f096-156">Changes to time entry records</span></span>

<span data-ttu-id="4f096-157">Nella figura seguente vengono illustrate le modifiche che si verificano per gli inserimenti ore approvati quando vengono richiamati.</span><span class="sxs-lookup"><span data-stu-id="4f096-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Transizioni dello stato degli inserimenti ore](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="4f096-159">Modifiche ai record delle voci di spesa</span><span class="sxs-lookup"><span data-stu-id="4f096-159">Changes to expense entry records</span></span>

<span data-ttu-id="4f096-160">Nella figura seguente vengono illustrate le modifiche che si hanno per le voci di spesa approvate quando vengono richiamate.</span><span class="sxs-lookup"><span data-stu-id="4f096-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Transizioni dello stato delle voci di spesa](media/ExpenseEntryStateTransitions.png)
