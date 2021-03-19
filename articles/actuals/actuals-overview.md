---
title: Valori effettivi
description: Questo argomento fornisce informazioni su come utilizzare i valori effettivi in Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291804"
---
# <a name="actuals"></a><span data-ttu-id="67194-103">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="67194-103">Actuals</span></span> 

<span data-ttu-id="67194-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="67194-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="67194-105">I valori effettivi sono la quantità di lavoro completata in un progetto.</span><span class="sxs-lookup"><span data-stu-id="67194-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="67194-106">Vengono creati come risultato di inserimenti ore, voci di spesa e scritture contabili nonché fatture.</span><span class="sxs-lookup"><span data-stu-id="67194-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="67194-107">Invio righe giornale di registrazione e tempo</span><span class="sxs-lookup"><span data-stu-id="67194-107">Journal lines and time submission</span></span>

<span data-ttu-id="67194-108">Per ulteriori informazioni sull'inserimento ore, vedi [Panoramica dell'inserimento ore](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="67194-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="67194-109">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="67194-109">Time and materials</span></span>

<span data-ttu-id="67194-110">Quando un inserimento ore inviato è collegato a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="67194-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="67194-111">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="67194-111">Fixed price</span></span>

<span data-ttu-id="67194-112">Quando un inserimento ore inviato è collegato a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="67194-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="67194-113">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="67194-113">Default pricing</span></span>

<span data-ttu-id="67194-114">La logica di creazione dei prezzi predefiniti risiede nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="67194-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="67194-115">I valori di campo di un inserimento ore vengono copiati nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="67194-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="67194-116">Questi valori includono la data della transazione, la voce di contratto a cui il progetto è mappato e la valuta nel listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="67194-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="67194-117">I campi che determinano i prezzi predefiniti, ad esempio **Ruolo** e **Unità organizzativa** vengono utilizzati per determinare il prezzo appropriato per impostazione predefinita nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="67194-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="67194-118">Puoi aggiungere un campo personalizzato all'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="67194-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="67194-119">Se desideri che il valore di campo venga propagato ai valori effettivi, crea il campo nell'entità Valori effettivi e utilizza i mapping dei campi per copiare il campo dall'inserimento ore nel valore effettivo.</span><span class="sxs-lookup"><span data-stu-id="67194-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="67194-120">Invio righe giornale di registrazione e spesa di base</span><span class="sxs-lookup"><span data-stu-id="67194-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="67194-121">Per ulteriori informazioni sull'inserimento spese, vedi [Panoramica della spesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="67194-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="67194-122">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="67194-122">Time and materials</span></span>

<span data-ttu-id="67194-123">Quando una spesa di base inviata è collegata a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="67194-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="67194-124">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="67194-124">Fixed price</span></span>

<span data-ttu-id="67194-125">Quando una spesa di base inviata è collegata a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="67194-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="67194-126">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="67194-126">Default pricing</span></span>

<span data-ttu-id="67194-127">La logica per l'immissione dei prezzi predefiniti per le spese si basa sulla categoria di spesa.</span><span class="sxs-lookup"><span data-stu-id="67194-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="67194-128">La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="67194-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="67194-129">Tuttavia, per impostazione predefinita, l'importo immesso per il prezzo stesso viene impostato direttamente per impostazione predefinita nelle righe giornale di registrazione correlate per costi e vendite.</span><span class="sxs-lookup"><span data-stu-id="67194-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="67194-130">La voce basata su categoria dei prezzi predefiniti unitari nelle voci di spesa non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="67194-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="67194-131">Utilizza giornali di registrazione per registrare i costi</span><span class="sxs-lookup"><span data-stu-id="67194-131">Use entry journals to record costs</span></span>

<span data-ttu-id="67194-132">Puoi utilizzare i giornali di registrazione per registrare costi o ricavi nelle classi di materiali, imposte, tempo, spese o transazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="67194-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="67194-133">I giornali di registrazione possono per gli scopi seguenti:</span><span class="sxs-lookup"><span data-stu-id="67194-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="67194-134">Registra il costo effettivo dei materiali e le vendite in un progetto.</span><span class="sxs-lookup"><span data-stu-id="67194-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="67194-135">Sposta i valori effettivi di transazioni da un altro sistema in Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="67194-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="67194-136">Registra i costi che si sono verificati in un altro sistema.</span><span class="sxs-lookup"><span data-stu-id="67194-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="67194-137">Questi costi possono includere costi di approvvigionamento o subappalto.</span><span class="sxs-lookup"><span data-stu-id="67194-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67194-138">L'applicazione non convalida il tipo di riga del giornale di registrazione o il prezzo correlato immesso nella riga del giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="67194-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="67194-139">Pertanto, solo un utente che è pienamente consapevole dell'impatto contabile che i valori effettivi hanno sul progetto deve utilizzare i giornali di registrazione per creare i valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="67194-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="67194-140">A causa dell'impatto di questo tipo di giornale di registrazione, è consigliabile scegliere con attenzione chi ha accesso per creare i giornali di registrazione.</span><span class="sxs-lookup"><span data-stu-id="67194-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="67194-141">Registrare valori effettivi basati su eventi di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-141">Record actuals based on project events</span></span>

<span data-ttu-id="67194-142">Project Operations registra le transazioni finanziarie che si hanno durante un progetto.</span><span class="sxs-lookup"><span data-stu-id="67194-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="67194-143">Queste transazioni vengono registrate come valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="67194-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="67194-144">Nella tabella seguente sono riportati i differenti tipi di valori effettivi creati, a seconda se il progetto è un progetto tempistica e materiali, prezzo fisso, interno o in fase di prevendita.</span><span class="sxs-lookup"><span data-stu-id="67194-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="67194-145">La risorsa appartiene alla stessa unità organizzativa dell'unità contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="67194-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="67194-146">Event</span><span class="sxs-lookup"><span data-stu-id="67194-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="67194-147">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="67194-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="67194-148">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="67194-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="67194-149">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="67194-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="67194-150">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="67194-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="67194-151">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="67194-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="67194-152">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="67194-152">Actuals</span></span></th>
<th><span data-ttu-id="67194-153">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="67194-153">Transaction currency</span></span></th>
<th><span data-ttu-id="67194-154">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="67194-154">Fixed price</span></span></th>
<th><span data-ttu-id="67194-155">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="67194-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="67194-156">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="67194-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="67194-157">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="67194-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-158">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="67194-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="67194-159">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="67194-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="67194-160">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="67194-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="67194-161">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-161">Cost actual</span></span></td>
<td><span data-ttu-id="67194-162">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-163">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-164">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="67194-165">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-166">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-167">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="67194-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="67194-168">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="67194-169">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="67194-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="67194-170">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-170">Cost actual</span></span></td>
<td><span data-ttu-id="67194-171">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-172">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-173">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-174">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-175">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-176">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="67194-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="67194-177">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-178">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="67194-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="67194-179">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="67194-180">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="67194-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="67194-181">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="67194-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="67194-182">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-183">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="67194-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-184">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-185">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-186">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-187">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="67194-187">Billed sales</span></span></td>
<td><span data-ttu-id="67194-188">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="67194-189">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="67194-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="67194-190">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="67194-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="67194-191">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-192">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-193">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-194">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-195">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-196">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="67194-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="67194-197">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-198">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="67194-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="67194-199">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="67194-200">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="67194-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="67194-201">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="67194-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="67194-202">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="67194-203">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="67194-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="67194-204">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="67194-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="67194-205">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="67194-206">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="67194-207">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-208">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="67194-208">Billed sales</span></span></td>
<td><span data-ttu-id="67194-209">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="67194-210">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="67194-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="67194-211">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="67194-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="67194-212">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-213">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="67194-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="67194-214">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-215">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="67194-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="67194-216">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="67194-217">La risorsa appartiene a un'unità organizzativa che differisce dall'unità contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="67194-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="67194-218">Event</span><span class="sxs-lookup"><span data-stu-id="67194-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="67194-219">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="67194-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="67194-220">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="67194-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="67194-221">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="67194-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="67194-222">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="67194-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="67194-223">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="67194-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="67194-224">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="67194-224">Actuals</span></span></th>
<th><span data-ttu-id="67194-225">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="67194-225">Transaction currency</span></span></th>
<th><span data-ttu-id="67194-226">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="67194-226">Fixed price</span></span></th>
<th><span data-ttu-id="67194-227">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="67194-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="67194-228">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="67194-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="67194-229">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="67194-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-230">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="67194-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="67194-231">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="67194-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="67194-232">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="67194-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="67194-233">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-233">Cost actual</span></span></td>
<td><span data-ttu-id="67194-234">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="67194-235">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="67194-236">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="67194-237">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="67194-238">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-239">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="67194-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="67194-240">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-241">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="67194-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="67194-242">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="67194-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-243">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="67194-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="67194-244">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="67194-245">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="67194-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="67194-246">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-246">Cost actual</span></span></td>
<td><span data-ttu-id="67194-247">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="67194-248">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="67194-249">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="67194-250">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="67194-251">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="67194-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-252">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="67194-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="67194-253">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="67194-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-254">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="67194-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="67194-255">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="67194-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-256">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="67194-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="67194-257">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-258">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="67194-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="67194-259">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="67194-260">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="67194-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="67194-261">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="67194-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="67194-262">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-263">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="67194-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-264">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-265">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="67194-266">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-267">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="67194-267">Billed sales</span></span></td>
<td><span data-ttu-id="67194-268">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="67194-269">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="67194-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="67194-270">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="67194-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="67194-271">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-272">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-273">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-274">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="67194-275">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-276">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="67194-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="67194-277">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-278">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="67194-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="67194-279">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="67194-280">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="67194-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="67194-281">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="67194-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="67194-282">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="67194-283">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="67194-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="67194-284">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="67194-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="67194-285">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="67194-286">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="67194-287">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="67194-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-288">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="67194-288">Billed sales</span></span></td>
<td><span data-ttu-id="67194-289">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="67194-290">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="67194-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="67194-291">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="67194-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="67194-292">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-293">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="67194-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="67194-294">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="67194-295">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="67194-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="67194-296">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="67194-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]