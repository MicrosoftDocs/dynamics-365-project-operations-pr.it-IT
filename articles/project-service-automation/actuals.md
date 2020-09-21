---
title: Valori effettivi
description: In questo argomento vengono fornite informazioni sui valori effettivi di progetto.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752708"
---
# <a name="actuals"></a><span data-ttu-id="a72cb-103">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="a72cb-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a72cb-104">I valori effettivi sono la quantità di lavoro completata in un progetto.</span><span class="sxs-lookup"><span data-stu-id="a72cb-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="a72cb-105">È possibile risalire ai valori effettivi di progetto fino ai relativi documenti di origine.</span><span class="sxs-lookup"><span data-stu-id="a72cb-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="a72cb-106">Questi documenti di origine includono inserimenti ore, voci di spesa e scritture contabili nonché fatture.</span><span class="sxs-lookup"><span data-stu-id="a72cb-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Come risalire ai valori effettivi di progetto fino a documenti di origine](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="a72cb-108">Inviare un inserimento ore</span><span class="sxs-lookup"><span data-stu-id="a72cb-108">Submitting a time entry</span></span>

<span data-ttu-id="a72cb-109">In PSA, quando un inserimento ore viene inviato per un progetto mappato a una voce di contratto tempistica e materiali, vengono create due righe giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a72cb-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a72cb-110">Una riga è per i costi e l'altra per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="a72cb-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a72cb-111">Quando un inserimento ore viene inviato per un progetto mappato a una voce di contratto a prezzo fisso, una riga giornale di registrazione viene creata solo per i costi.</span><span class="sxs-lookup"><span data-stu-id="a72cb-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="a72cb-112">La logica di immissione dei prezzi predefiniti risiede nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a72cb-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="a72cb-113">Tutti i valori di campo di un inserimento ore vengono copiati nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a72cb-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="a72cb-114">Questi campi includono la data della transazione, la voce di contratto a cui il progetto è mappato e la valuta nel listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="a72cb-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="a72cb-115">I campi che determinano i prezzi predefiniti, ad esempio **Ruolo** e **Unità organizzativa**, causano l'immissione di un prezzo appropriato per impostazione predefinita nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a72cb-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="a72cb-116">Se aggiungi un campo personalizzato nell'inserimento ore e il valore di campo deve essere propagato ai valori effettivi, crea il campo nell'entità Valori effettivi e utilizza i mapping dei campi per copiare il campo dall'inserimento ore nel valore effettivo.</span><span class="sxs-lookup"><span data-stu-id="a72cb-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="a72cb-117">Inviare una voce di spesa</span><span class="sxs-lookup"><span data-stu-id="a72cb-117">Submitting an expense entry</span></span>

<span data-ttu-id="a72cb-118">In PSA, quando una voce di spesa viene inviata per un progetto mappato a una voce di contratto di tempo e materiale, vengono create due righe giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a72cb-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a72cb-119">Una riga è per i costi e l'altra per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="a72cb-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a72cb-120">Quando una voce di spesa viene inviata per un progetto mappato a una voce di contratto a prezzo fisso, una riga giornale di registrazione viene creata solo per i costi.</span><span class="sxs-lookup"><span data-stu-id="a72cb-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="a72cb-121">La logica per l'immissione di prezzi predefiniti per le spese è basata sulla categoria di spesa selezionata nella pagina **Voce di spesa**.</span><span class="sxs-lookup"><span data-stu-id="a72cb-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="a72cb-122">La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="a72cb-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a72cb-123">Tuttavia, per il prezzo stesso, l'importo immesso dall'utente viene impostato direttamente per impostazione predefinita nelle righe giornale di registrazione correlate per costi e vendite.</span><span class="sxs-lookup"><span data-stu-id="a72cb-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="a72cb-124">Nella versione corrente di PSA, la voce basata su categoria dei prezzi predefiniti unitari nelle voci di spesa non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="a72cb-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="a72cb-125">Utilizzare giornali di registrazione per registrare i costi</span><span class="sxs-lookup"><span data-stu-id="a72cb-125">Using journals to record costs</span></span>

<span data-ttu-id="a72cb-126">In PSA, i giornali di registrazione ti consentono di registrare costi o ricavi nelle classi di materiali, imposte, tempo, spese o transazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="a72cb-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a72cb-127">Un giornale di registrazione ha un'intestazione, righe e un'azione **Conferma**.</span><span class="sxs-lookup"><span data-stu-id="a72cb-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="a72cb-128">Di seguito sono riportati alcuni scenari in cui puoi utilizzare un giornale di registrazione:</span><span class="sxs-lookup"><span data-stu-id="a72cb-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="a72cb-129">Devi registrare vendite e costi effettivi di materiali in un progetto.</span><span class="sxs-lookup"><span data-stu-id="a72cb-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="a72cb-130">Devi spostare gli effettivi di transazioni da un altro sistema a PSA.</span><span class="sxs-lookup"><span data-stu-id="a72cb-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="a72cb-131">Devi registrare i costi incorsi in un altro sistema, ad esempio costi di approvvigionamento o conto lavoro.</span><span class="sxs-lookup"><span data-stu-id="a72cb-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="a72cb-132">Registrare effettivi basati su eventi di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-132">Recording actuals based on project events</span></span>

<span data-ttu-id="a72cb-133">PSA registra le transazioni finanziarie che si hanno durante un progetto.</span><span class="sxs-lookup"><span data-stu-id="a72cb-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a72cb-134">Queste transazioni vengono registrate come **valori effettivi**.</span><span class="sxs-lookup"><span data-stu-id="a72cb-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="a72cb-135">Nella tabella seguente sono riportati i differenti tipi di valori effettivi creati, a seconda se il progetto è un progetto tempistica e materiali, prezzo fisso, interno o in fase di prevendita.</span><span class="sxs-lookup"><span data-stu-id="a72cb-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="a72cb-136">**La risorsa appartiene alla stessa unità organizzativa dell'unità contratto del progetto**</span><span class="sxs-lookup"><span data-stu-id="a72cb-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a72cb-137">Event</span><span class="sxs-lookup"><span data-stu-id="a72cb-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a72cb-138">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="a72cb-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a72cb-139">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="a72cb-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a72cb-140">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="a72cb-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a72cb-141">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="a72cb-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a72cb-142">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="a72cb-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a72cb-143">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="a72cb-143">Actuals</span></span></th>
<th><span data-ttu-id="a72cb-144">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="a72cb-144">Transaction currency</span></span></th>
<th><span data-ttu-id="a72cb-145">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="a72cb-145">Fixed price</span></span></th>
<th><span data-ttu-id="a72cb-146">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="a72cb-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a72cb-147">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="a72cb-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a72cb-148">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="a72cb-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-149">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="a72cb-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a72cb-150">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="a72cb-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a72cb-151">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="a72cb-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a72cb-152">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-152">Cost actual</span></span></td>
<td><span data-ttu-id="a72cb-153">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-154">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-155">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a72cb-156">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-157">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-158">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a72cb-159">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a72cb-160">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="a72cb-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a72cb-161">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-161">Cost actual</span></span></td>
<td><span data-ttu-id="a72cb-162">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-163">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-164">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-165">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-166">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-167">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="a72cb-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a72cb-168">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-169">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="a72cb-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a72cb-170">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a72cb-171">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="a72cb-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a72cb-172">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="a72cb-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a72cb-173">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-174">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="a72cb-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-175">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-176">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-177">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-178">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="a72cb-178">Billed sales</span></span></td>
<td><span data-ttu-id="a72cb-179">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a72cb-180">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="a72cb-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a72cb-181">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="a72cb-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a72cb-182">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-183">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-184">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-185">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-186">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-187">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="a72cb-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a72cb-188">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-189">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="a72cb-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a72cb-190">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a72cb-191">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="a72cb-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a72cb-192">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="a72cb-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a72cb-193">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a72cb-194">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="a72cb-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a72cb-195">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="a72cb-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a72cb-196">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a72cb-197">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a72cb-198">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-199">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="a72cb-199">Billed sales</span></span></td>
<td><span data-ttu-id="a72cb-200">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a72cb-201">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="a72cb-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a72cb-202">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="a72cb-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a72cb-203">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-204">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="a72cb-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a72cb-205">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-206">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="a72cb-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a72cb-207">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a72cb-208">**La risorsa appartiene a un'unità organizzativa che differisce dall'unità contratto del progetto**</span><span class="sxs-lookup"><span data-stu-id="a72cb-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a72cb-209">Event</span><span class="sxs-lookup"><span data-stu-id="a72cb-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a72cb-210">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="a72cb-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a72cb-211">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="a72cb-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a72cb-212">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="a72cb-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a72cb-213">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="a72cb-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a72cb-214">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="a72cb-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a72cb-215">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="a72cb-215">Actuals</span></span></th>
<th><span data-ttu-id="a72cb-216">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="a72cb-216">Transaction currency</span></span></th>
<th><span data-ttu-id="a72cb-217">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="a72cb-217">Fixed price</span></span></th>
<th><span data-ttu-id="a72cb-218">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="a72cb-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a72cb-219">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="a72cb-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a72cb-220">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="a72cb-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-221">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="a72cb-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a72cb-222">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="a72cb-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a72cb-223">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="a72cb-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a72cb-224">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-224">Cost actual</span></span></td>
<td><span data-ttu-id="a72cb-225">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a72cb-226">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a72cb-227">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a72cb-228">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a72cb-229">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-230">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a72cb-231">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-232">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="a72cb-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a72cb-233">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="a72cb-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-234">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="a72cb-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a72cb-235">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a72cb-236">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="a72cb-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a72cb-237">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-237">Cost actual</span></span></td>
<td><span data-ttu-id="a72cb-238">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a72cb-239">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a72cb-240">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a72cb-241">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a72cb-242">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="a72cb-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-243">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="a72cb-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a72cb-244">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="a72cb-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-245">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="a72cb-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a72cb-246">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="a72cb-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-247">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="a72cb-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a72cb-248">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-249">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="a72cb-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a72cb-250">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a72cb-251">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="a72cb-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a72cb-252">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="a72cb-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a72cb-253">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-254">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="a72cb-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-255">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-256">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a72cb-257">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-258">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="a72cb-258">Billed sales</span></span></td>
<td><span data-ttu-id="a72cb-259">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a72cb-260">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="a72cb-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a72cb-261">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="a72cb-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a72cb-262">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-263">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-264">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-265">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a72cb-266">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-267">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="a72cb-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a72cb-268">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-269">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="a72cb-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a72cb-270">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a72cb-271">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="a72cb-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a72cb-272">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="a72cb-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a72cb-273">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a72cb-274">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="a72cb-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a72cb-275">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="a72cb-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a72cb-276">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a72cb-277">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a72cb-278">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="a72cb-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-279">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="a72cb-279">Billed sales</span></span></td>
<td><span data-ttu-id="a72cb-280">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a72cb-281">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="a72cb-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a72cb-282">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="a72cb-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a72cb-283">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-284">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="a72cb-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a72cb-285">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a72cb-286">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="a72cb-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a72cb-287">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a72cb-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
