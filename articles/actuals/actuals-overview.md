---
title: Home page di Valori effettivi
description: Questo argomento fornisce informazioni su come utilizzare i valori effettivi in Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907323"
---
# <a name="actuals"></a><span data-ttu-id="0798c-103">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="0798c-103">Actuals</span></span>

<span data-ttu-id="0798c-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="0798c-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0798c-105">I valori effettivi sono la quantità di lavoro completata in un progetto.</span><span class="sxs-lookup"><span data-stu-id="0798c-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="0798c-106">Vengono creati come risultato di inserimenti ore, voci di spesa e scritture contabili nonché fatture.</span><span class="sxs-lookup"><span data-stu-id="0798c-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="0798c-107">Invio righe giornale di registrazione e tempo</span><span class="sxs-lookup"><span data-stu-id="0798c-107">Journal lines and time submission</span></span>

<span data-ttu-id="0798c-108">Per ulteriori informazioni sull'inserimento ore, vedi [Panoramica dell'inserimento ore](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0798c-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="0798c-109">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="0798c-109">Time and materials</span></span>

<span data-ttu-id="0798c-110">Quando un inserimento ore inviato è collegato a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="0798c-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="0798c-111">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="0798c-111">Fixed price</span></span>

<span data-ttu-id="0798c-112">Quando un inserimento ore inviato è collegato a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="0798c-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="0798c-113">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="0798c-113">Default pricing</span></span>

<span data-ttu-id="0798c-114">La logica di creazione dei prezzi predefiniti risiede nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0798c-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="0798c-115">I valori di campo di un inserimento ore vengono copiati nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0798c-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="0798c-116">Questi valori includono la data della transazione, la voce di contratto a cui il progetto è mappato e la valuta nel listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="0798c-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="0798c-117">I campi che determinano i prezzi predefiniti, ad esempio **Ruolo** e **Unità organizzativa** vengono utilizzati per determinare il prezzo appropriato per impostazione predefinita nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0798c-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="0798c-118">Puoi aggiungere un campo personalizzato all'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="0798c-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="0798c-119">Se desideri che il valore di campo venga propagato ai valori effettivi, crea il campo nell'entità Valori effettivi e utilizza i mapping dei campi per copiare il campo dall'inserimento ore nel valore effettivo.</span><span class="sxs-lookup"><span data-stu-id="0798c-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="0798c-120">Invio righe giornale di registrazione e spesa di base</span><span class="sxs-lookup"><span data-stu-id="0798c-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="0798c-121">Per ulteriori informazioni sull'inserimento spese, vedi [Panoramica della spesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0798c-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="0798c-122">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="0798c-122">Time and materials</span></span>

<span data-ttu-id="0798c-123">Quando una spesa di base inviata è collegata a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="0798c-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="0798c-124">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="0798c-124">Fixed price</span></span>

<span data-ttu-id="0798c-125">Quando una spesa di base inviata è collegata a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="0798c-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="0798c-126">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="0798c-126">Default pricing</span></span>

<span data-ttu-id="0798c-127">La logica per l'immissione dei prezzi predefiniti per le spese si basa sulla categoria di spesa.</span><span class="sxs-lookup"><span data-stu-id="0798c-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="0798c-128">La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="0798c-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="0798c-129">Tuttavia, per impostazione predefinita, l'importo immesso per il prezzo stesso viene impostato direttamente per impostazione predefinita nelle righe giornale di registrazione correlate per costi e vendite.</span><span class="sxs-lookup"><span data-stu-id="0798c-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="0798c-130">La voce basata su categoria dei prezzi predefiniti unitari nelle voci di spesa non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0798c-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="0798c-131">Utilizza giornali di registrazione per registrare i costi</span><span class="sxs-lookup"><span data-stu-id="0798c-131">Use entry journals to record costs</span></span>

<span data-ttu-id="0798c-132">Puoi utilizzare i giornali di registrazione per registrare costi o ricavi nelle classi di materiali, imposte, tempo, spese o transazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="0798c-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="0798c-133">I giornali di registrazione possono per gli scopi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0798c-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="0798c-134">Registra il costo effettivo dei materiali e le vendite in un progetto.</span><span class="sxs-lookup"><span data-stu-id="0798c-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="0798c-135">Sposta i valori effettivi della transazione da un altro sistema a Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0798c-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="0798c-136">Registra i costi che si sono verificati in un altro sistema.</span><span class="sxs-lookup"><span data-stu-id="0798c-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="0798c-137">Questi costi possono includere costi di approvvigionamento o subappalto.</span><span class="sxs-lookup"><span data-stu-id="0798c-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0798c-138">L'applicazione non convalida il tipo di riga del giornale di registrazione o il prezzo correlato immesso nella riga del giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0798c-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="0798c-139">Pertanto, solo un utente che è pienamente consapevole dell'impatto contabile che i valori effettivi hanno sul progetto deve utilizzare i giornali di registrazione per creare i valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="0798c-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="0798c-140">A causa dell'impatto di questo tipo di giornale di registrazione, è consigliabile scegliere con attenzione chi ha accesso per creare i giornali di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0798c-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="0798c-141">Registrare valori effettivi basati su eventi di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-141">Record actuals based on project events</span></span>

<span data-ttu-id="0798c-142">Project Operations registra le transazioni finanziarie che si hanno durante un progetto.</span><span class="sxs-lookup"><span data-stu-id="0798c-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="0798c-143">Queste transazioni vengono registrate come valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="0798c-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="0798c-144">Nella tabella seguente sono riportati i differenti tipi di valori effettivi creati, a seconda se il progetto è un progetto tempistica e materiali, prezzo fisso, interno o in fase di prevendita.</span><span class="sxs-lookup"><span data-stu-id="0798c-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="0798c-145">La risorsa appartiene alla stessa unità organizzativa dell'unità contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0798c-146">Event</span><span class="sxs-lookup"><span data-stu-id="0798c-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0798c-147">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="0798c-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0798c-148">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="0798c-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0798c-149">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="0798c-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0798c-150">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="0798c-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0798c-151">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="0798c-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0798c-152">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="0798c-152">Actuals</span></span></th>
<th><span data-ttu-id="0798c-153">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="0798c-153">Transaction currency</span></span></th>
<th><span data-ttu-id="0798c-154">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="0798c-154">Fixed price</span></span></th>
<th><span data-ttu-id="0798c-155">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="0798c-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0798c-156">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="0798c-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0798c-157">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="0798c-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-158">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="0798c-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0798c-159">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="0798c-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0798c-160">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="0798c-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0798c-161">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-161">Cost actual</span></span></td>
<td><span data-ttu-id="0798c-162">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-163">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-164">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="0798c-165">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-166">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-167">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="0798c-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0798c-168">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0798c-169">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="0798c-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0798c-170">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-170">Cost actual</span></span></td>
<td><span data-ttu-id="0798c-171">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-172">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-173">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-174">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-175">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-176">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="0798c-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0798c-177">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-178">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="0798c-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0798c-179">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0798c-180">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="0798c-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0798c-181">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="0798c-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0798c-182">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-183">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="0798c-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-184">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-185">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-186">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-187">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="0798c-187">Billed sales</span></span></td>
<td><span data-ttu-id="0798c-188">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0798c-189">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="0798c-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0798c-190">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="0798c-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0798c-191">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-192">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-193">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-194">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-195">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-196">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="0798c-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0798c-197">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-198">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="0798c-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0798c-199">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0798c-200">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="0798c-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0798c-201">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="0798c-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0798c-202">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0798c-203">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="0798c-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0798c-204">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="0798c-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0798c-205">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0798c-206">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0798c-207">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-208">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="0798c-208">Billed sales</span></span></td>
<td><span data-ttu-id="0798c-209">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0798c-210">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="0798c-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0798c-211">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="0798c-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0798c-212">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-213">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="0798c-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0798c-214">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-215">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="0798c-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0798c-216">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="0798c-217">La risorsa appartiene a un'unità organizzativa che differisce dall'unità contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0798c-218">Event</span><span class="sxs-lookup"><span data-stu-id="0798c-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0798c-219">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="0798c-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0798c-220">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="0798c-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0798c-221">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="0798c-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0798c-222">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="0798c-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0798c-223">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="0798c-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0798c-224">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="0798c-224">Actuals</span></span></th>
<th><span data-ttu-id="0798c-225">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="0798c-225">Transaction currency</span></span></th>
<th><span data-ttu-id="0798c-226">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="0798c-226">Fixed price</span></span></th>
<th><span data-ttu-id="0798c-227">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="0798c-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0798c-228">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="0798c-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0798c-229">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="0798c-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-230">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="0798c-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0798c-231">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="0798c-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0798c-232">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="0798c-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0798c-233">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-233">Cost actual</span></span></td>
<td><span data-ttu-id="0798c-234">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0798c-235">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0798c-236">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0798c-237">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0798c-238">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-239">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="0798c-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0798c-240">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-241">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="0798c-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0798c-242">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="0798c-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-243">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="0798c-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0798c-244">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0798c-245">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="0798c-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0798c-246">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-246">Cost actual</span></span></td>
<td><span data-ttu-id="0798c-247">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0798c-248">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0798c-249">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0798c-250">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0798c-251">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="0798c-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-252">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="0798c-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0798c-253">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="0798c-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-254">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="0798c-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0798c-255">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="0798c-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-256">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="0798c-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0798c-257">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-258">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="0798c-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0798c-259">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0798c-260">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="0798c-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0798c-261">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="0798c-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0798c-262">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-263">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="0798c-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-264">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-265">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0798c-266">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-267">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="0798c-267">Billed sales</span></span></td>
<td><span data-ttu-id="0798c-268">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0798c-269">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="0798c-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0798c-270">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="0798c-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0798c-271">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-272">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-273">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-274">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0798c-275">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-276">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="0798c-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0798c-277">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-278">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="0798c-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0798c-279">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0798c-280">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="0798c-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0798c-281">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="0798c-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0798c-282">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0798c-283">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="0798c-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0798c-284">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="0798c-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0798c-285">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0798c-286">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0798c-287">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0798c-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-288">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="0798c-288">Billed sales</span></span></td>
<td><span data-ttu-id="0798c-289">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0798c-290">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="0798c-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0798c-291">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="0798c-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0798c-292">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-293">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="0798c-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0798c-294">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0798c-295">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="0798c-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0798c-296">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0798c-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
