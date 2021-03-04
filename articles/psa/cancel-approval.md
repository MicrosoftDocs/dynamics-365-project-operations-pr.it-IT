---
title: Annullare inserimenti ore e voci di spesa approvate precedentemente
description: In questo argomento vengono fornite informazioni su come annullare una transazione di tempo e spesa di progetto approvata.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150583"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="603d0-103">Annullare inserimenti ore o voci di spesa approvate precedentemente</span><span class="sxs-lookup"><span data-stu-id="603d0-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="603d0-104">Nell'ultima versione di Dynamics 365 Project Service Automation, i responsabili approvazione possono annullare gli inserimenti ore o le voci di spesa approvate precedentemente.</span><span class="sxs-lookup"><span data-stu-id="603d0-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="603d0-105">Annullare un inserimento ore o una voce di spesa approvata precedentemente</span><span class="sxs-lookup"><span data-stu-id="603d0-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="603d0-106">Segui questi passaggi per annullare un inserimento ore o una voce di spesa approvata precedentemente.</span><span class="sxs-lookup"><span data-stu-id="603d0-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="603d0-107">Seleziona **Progetti** \> **Attività personali** \> **Approvazioni**.</span><span class="sxs-lookup"><span data-stu-id="603d0-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="603d0-108">Nella pagina elenco **Approvazioni**, seleziona la vista **Approvazioni personali passate**.</span><span class="sxs-lookup"><span data-stu-id="603d0-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="603d0-109">Viene visualizzato un elenco di inserimenti ore e voci di spesa approvate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="603d0-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="603d0-110">Seleziona una o più voci o inserimenti e quindi seleziona **Annulla approvazione**.</span><span class="sxs-lookup"><span data-stu-id="603d0-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="603d0-111">Viene visualizzato un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="603d0-111">You receive a warning message.</span></span>
4. <span data-ttu-id="603d0-112">Seleziona **OK** per annullare l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="603d0-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="603d0-113">Comprendere l'impatto dell'annullamento dell'approvazione di un inserimento ore o di una voce di spesa</span><span class="sxs-lookup"><span data-stu-id="603d0-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="603d0-114">Quando si annulla un'approvazione, si ha un impatto operativo e un impatto finanziario.</span><span class="sxs-lookup"><span data-stu-id="603d0-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="603d0-115">Impatto operativo</span><span class="sxs-lookup"><span data-stu-id="603d0-115">Operational impact</span></span>

<span data-ttu-id="603d0-116">Per quanto riguarda le operazioni, quando si annulla un'approvazione, lo stato del record diventa **Bozza** e l'approvazione non è più visualizzata nella vista **Approvazioni personali passate**.</span><span class="sxs-lookup"><span data-stu-id="603d0-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="603d0-117">L'approvazione annullata è invece visualizzata nella vista **Inserimenti ore per l'approvazione** o nella vista **Voci di spesa per l'approvazione**, a seconda se si tratti di un inserimento ore o di una voce di spesa.</span><span class="sxs-lookup"><span data-stu-id="603d0-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="603d0-118">Inoltre, lo stato dell'inserimento ore o della voce di spesa correlata diventa **Inviato**, di modo che la voce o l'inserimento correlato sia coerente con le approvazioni il cui stato è **Bozza**.</span><span class="sxs-lookup"><span data-stu-id="603d0-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="603d0-119">Come responsabile approvazione, puoi modificare alcuni campi di un'approvazione il cui stato è **Bozza**.</span><span class="sxs-lookup"><span data-stu-id="603d0-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="603d0-120">Questi campi includono **Tipo di fatturazione** e **Ore fatturabili per inserimenti ore**.</span><span class="sxs-lookup"><span data-stu-id="603d0-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="603d0-121">Dopo avere apportato le modifiche, puoi approvare di nuovo il record.</span><span class="sxs-lookup"><span data-stu-id="603d0-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="603d0-122">In alternativa, puoi rifiutare la voce o l'inserimento.</span><span class="sxs-lookup"><span data-stu-id="603d0-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="603d0-123">Se rifiuti l'approvazione di un inserimento ore, lo stato dell'inserimento diventa **Restituito**.</span><span class="sxs-lookup"><span data-stu-id="603d0-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="603d0-124">Se rifiuti l'approvazione di una voce di spesa, lo stato diventa **Rifiutato**.</span><span class="sxs-lookup"><span data-stu-id="603d0-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="603d0-125">Da un punto di vista funzionale, le voci e gli inserimenti restituiti e rifiutati hanno lo stesso comportamento di quelli il cui stato è **Bozza**.</span><span class="sxs-lookup"><span data-stu-id="603d0-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="603d0-126">Un membro del team di progetto può apportare qualsiasi modifica necessaria alla voce o all'inserimento e quindi inviarlo di nuovo per l'approvazione oppure eliminarlo completamente.</span><span class="sxs-lookup"><span data-stu-id="603d0-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="603d0-127">Impatto finanziario</span><span class="sxs-lookup"><span data-stu-id="603d0-127">Financial impact</span></span>

<span data-ttu-id="603d0-128">L'annullamento di un'approvazione ha anche un impatto finanziario su un progetto.</span><span class="sxs-lookup"><span data-stu-id="603d0-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="603d0-129">Innanzitutto, i valori effettivi corrispondenti di costo e vendita vengono aggiornati nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="603d0-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="603d0-130">Lo stato di rettifica diventa **Rettificato**.</span><span class="sxs-lookup"><span data-stu-id="603d0-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="603d0-131">Lo stato di fatturazione diventa **Annullato**.</span><span class="sxs-lookup"><span data-stu-id="603d0-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="603d0-132">Quindi, nella tabella Valori effettivi vengono create scritture di storno.</span><span class="sxs-lookup"><span data-stu-id="603d0-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="603d0-133">Per creare scritture di storno, il sistema copia i valori di campo dai valori effettivi originali.</span><span class="sxs-lookup"><span data-stu-id="603d0-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="603d0-134">I soli valori che non vengono copiati sono i valori di quantità.</span><span class="sxs-lookup"><span data-stu-id="603d0-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="603d0-135">Questi valori vengono invece stornati.</span><span class="sxs-lookup"><span data-stu-id="603d0-135">These values are reversed instead.</span></span> <span data-ttu-id="603d0-136">Valori effettivi stornati vengono creati per i valori effettivi **Costo** e **Vendite non fatturate**.</span><span class="sxs-lookup"><span data-stu-id="603d0-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="603d0-137">Il campo **Stato rettifica** dei valori effettivi stornati viene impostato su **Non rettificabile** e lo stato di fatturazione viene impostato su **Annullato**.</span><span class="sxs-lookup"><span data-stu-id="603d0-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="603d0-138">Dopo aver eseguito tali modifiche, l'importo che viene registrato come speso nel progetto e nel backlog dei ricavi del progetto non include più gli importi che questi valori effettivi rappresentano.</span><span class="sxs-lookup"><span data-stu-id="603d0-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
