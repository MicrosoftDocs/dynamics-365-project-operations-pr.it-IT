---
title: Panoramica dei valori effettivi
description: In questo argomento vengono fornite informazioni sui valori effettivi di progetto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146128"
---
# <a name="actuals-overview"></a><span data-ttu-id="bfc7e-103">Panoramica dei valori effettivi</span><span class="sxs-lookup"><span data-stu-id="bfc7e-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bfc7e-104">I valori effettivi sono la quantità di lavoro completata in un progetto.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="bfc7e-105">È possibile risalire ai valori effettivi di progetto fino ai relativi documenti di origine.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="bfc7e-106">Questi documenti di origine includono inserimenti ore, voci di spesa e scritture contabili nonché fatture.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Come risalire ai valori effettivi di progetto fino a documenti di origine](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="bfc7e-108">Inviare un inserimento ore</span><span class="sxs-lookup"><span data-stu-id="bfc7e-108">Submitting a time entry</span></span>

<span data-ttu-id="bfc7e-109">In PSA, quando un inserimento ore viene inviato per un progetto mappato a una voce di contratto tempistica e materiali, vengono create due righe giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="bfc7e-110">Una riga è per i costi e l'altra per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="bfc7e-111">Quando un inserimento ore viene inviato per un progetto mappato a una voce di contratto a prezzo fisso, una riga giornale di registrazione viene creata solo per i costi.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="bfc7e-112">La logica di immissione dei prezzi predefiniti risiede nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="bfc7e-113">Tutti i valori di campo di un inserimento ore vengono copiati nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="bfc7e-114">Questi campi includono la data della transazione, la voce di contratto a cui il progetto è mappato e la valuta nel listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="bfc7e-115">I campi che determinano i prezzi predefiniti, ad esempio **Ruolo** e **Unità organizzativa**, causano l'immissione di un prezzo appropriato per impostazione predefinita nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="bfc7e-116">Se aggiungi un campo personalizzato nell'inserimento ore e il valore di campo deve essere propagato ai valori effettivi, crea il campo nell'entità Valori effettivi e utilizza i mapping dei campi per copiare il campo dall'inserimento ore nel valore effettivo.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="bfc7e-117">Inviare una voce di spesa</span><span class="sxs-lookup"><span data-stu-id="bfc7e-117">Submitting an expense entry</span></span>

<span data-ttu-id="bfc7e-118">In PSA, quando una voce di spesa viene inviata per un progetto mappato a una voce di contratto di tempo e materiale, vengono create due righe giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="bfc7e-119">Una riga è per i costi e l'altra per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="bfc7e-120">Quando una voce di spesa viene inviata per un progetto mappato a una voce di contratto a prezzo fisso, una riga giornale di registrazione viene creata solo per i costi.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="bfc7e-121">La logica per l'immissione di prezzi predefiniti per le spese è basata sulla categoria di spesa selezionata nella pagina **Voce di spesa**.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="bfc7e-122">La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="bfc7e-123">Tuttavia, per il prezzo stesso, l'importo immesso dall'utente viene impostato direttamente per impostazione predefinita nelle righe giornale di registrazione correlate per costi e vendite.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="bfc7e-124">Nella versione corrente di PSA, la voce basata su categoria dei prezzi predefiniti unitari nelle voci di spesa non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="bfc7e-125">Utilizzare giornali di registrazione inserimenti per registrare i costi</span><span class="sxs-lookup"><span data-stu-id="bfc7e-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="bfc7e-126">In PSA, i giornali di registrazione inserimenti ti consentono di registrare costi o ricavi nelle classi di materiali, imposte, tempo, spese o transazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="bfc7e-127">Un giornale di registrazione ha un'intestazione, righe e un'azione **Conferma**.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="bfc7e-128">Di seguito sono riportati alcuni scenari in cui puoi utilizzare un giornale di registrazione:</span><span class="sxs-lookup"><span data-stu-id="bfc7e-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="bfc7e-129">Devi registrare vendite e costi effettivi di materiali in un progetto.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="bfc7e-130">Devi spostare gli effettivi di transazioni da un altro sistema a PSA.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="bfc7e-131">Devi registrare i costi incorsi in un altro sistema, ad esempio costi di approvvigionamento o conto lavoro.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfc7e-132">L'utilizzo dei giornali di registrazione inserimenti per creare i valori effettivi deve essere eseguito solo da un utente che sia pienamente consapevole dell'impatto contabile che i dati effettivi hanno sul progetto.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="bfc7e-133">Questo perché l'applicazione non convalida il tipo di riga di giornale di registrazione o il prezzo correlato immesso nella riga di giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="bfc7e-134">A causa dell'impatto di questo tipo di giornale, presta la dovuta attenzione a chi ha accesso per creare giornali di registrazione inserimenti.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="bfc7e-135">Registrare effettivi basati su eventi di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-135">Recording actuals based on project events</span></span>

<span data-ttu-id="bfc7e-136">PSA registra le transazioni finanziarie che si hanno durante un progetto.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="bfc7e-137">Queste transazioni vengono registrate come **valori effettivi**.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="bfc7e-138">Nella tabella seguente sono riportati i differenti tipi di valori effettivi creati, a seconda se il progetto è un progetto tempistica e materiali, prezzo fisso, interno o in fase di prevendita.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="bfc7e-139">**La risorsa appartiene alla stessa unità organizzativa dell'unità contratto del progetto**</span><span class="sxs-lookup"><span data-stu-id="bfc7e-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="bfc7e-140">Event</span><span class="sxs-lookup"><span data-stu-id="bfc7e-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="bfc7e-141">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="bfc7e-142">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="bfc7e-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="bfc7e-143">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="bfc7e-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="bfc7e-144">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="bfc7e-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="bfc7e-145">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="bfc7e-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bfc7e-146">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="bfc7e-146">Actuals</span></span></th>
<th><span data-ttu-id="bfc7e-147">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="bfc7e-147">Transaction currency</span></span></th>
<th><span data-ttu-id="bfc7e-148">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="bfc7e-148">Fixed price</span></span></th>
<th><span data-ttu-id="bfc7e-149">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="bfc7e-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bfc7e-150">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="bfc7e-151">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="bfc7e-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-152">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="bfc7e-153">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="bfc7e-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfc7e-154">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bfc7e-155">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-155">Cost actual</span></span></td>
<td><span data-ttu-id="bfc7e-156">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-157">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-158">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="bfc7e-159">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-160">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-161">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="bfc7e-162">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfc7e-163">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bfc7e-164">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-164">Cost actual</span></span></td>
<td><span data-ttu-id="bfc7e-165">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-166">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-167">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-168">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-169">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-170">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="bfc7e-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bfc7e-171">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-172">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="bfc7e-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfc7e-173">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfc7e-174">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bfc7e-175">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="bfc7e-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bfc7e-176">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-177">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="bfc7e-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-178">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-179">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-180">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-181">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="bfc7e-181">Billed sales</span></span></td>
<td><span data-ttu-id="bfc7e-182">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfc7e-183">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bfc7e-184">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="bfc7e-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bfc7e-185">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-186">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-187">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-188">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-189">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-190">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="bfc7e-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bfc7e-191">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-192">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="bfc7e-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfc7e-193">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfc7e-194">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bfc7e-195">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="bfc7e-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bfc7e-196">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="bfc7e-197">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="bfc7e-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="bfc7e-198">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="bfc7e-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="bfc7e-199">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bfc7e-200">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="bfc7e-201">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-202">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="bfc7e-202">Billed sales</span></span></td>
<td><span data-ttu-id="bfc7e-203">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfc7e-204">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bfc7e-205">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="bfc7e-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bfc7e-206">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-207">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="bfc7e-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="bfc7e-208">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-209">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="bfc7e-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfc7e-210">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bfc7e-211">**La risorsa appartiene a un'unità organizzativa che differisce dall'unità contratto del progetto**</span><span class="sxs-lookup"><span data-stu-id="bfc7e-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="bfc7e-212">Event</span><span class="sxs-lookup"><span data-stu-id="bfc7e-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="bfc7e-213">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="bfc7e-214">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="bfc7e-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="bfc7e-215">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="bfc7e-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="bfc7e-216">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="bfc7e-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="bfc7e-217">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="bfc7e-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bfc7e-218">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="bfc7e-218">Actuals</span></span></th>
<th><span data-ttu-id="bfc7e-219">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="bfc7e-219">Transaction currency</span></span></th>
<th><span data-ttu-id="bfc7e-220">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="bfc7e-220">Fixed price</span></span></th>
<th><span data-ttu-id="bfc7e-221">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="bfc7e-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bfc7e-222">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="bfc7e-223">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="bfc7e-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-224">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="bfc7e-225">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="bfc7e-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="bfc7e-226">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bfc7e-227">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-227">Cost actual</span></span></td>
<td><span data-ttu-id="bfc7e-228">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="bfc7e-229">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="bfc7e-230">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="bfc7e-231">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="bfc7e-232">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-233">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="bfc7e-234">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-235">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="bfc7e-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="bfc7e-236">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="bfc7e-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-237">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="bfc7e-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="bfc7e-238">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="bfc7e-239">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bfc7e-240">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-240">Cost actual</span></span></td>
<td><span data-ttu-id="bfc7e-241">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bfc7e-242">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="bfc7e-243">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bfc7e-244">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="bfc7e-245">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="bfc7e-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-246">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="bfc7e-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="bfc7e-247">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="bfc7e-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-248">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="bfc7e-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="bfc7e-249">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-250">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="bfc7e-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bfc7e-251">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-252">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="bfc7e-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfc7e-253">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfc7e-254">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bfc7e-255">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="bfc7e-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bfc7e-256">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-257">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="bfc7e-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-258">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-259">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="bfc7e-260">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-261">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="bfc7e-261">Billed sales</span></span></td>
<td><span data-ttu-id="bfc7e-262">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfc7e-263">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bfc7e-264">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="bfc7e-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bfc7e-265">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-266">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-267">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-268">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bfc7e-269">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-270">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="bfc7e-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bfc7e-271">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-272">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="bfc7e-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfc7e-273">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bfc7e-274">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bfc7e-275">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="bfc7e-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bfc7e-276">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="bfc7e-277">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="bfc7e-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="bfc7e-278">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="bfc7e-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="bfc7e-279">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bfc7e-280">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="bfc7e-281">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="bfc7e-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-282">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="bfc7e-282">Billed sales</span></span></td>
<td><span data-ttu-id="bfc7e-283">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bfc7e-284">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bfc7e-285">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="bfc7e-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bfc7e-286">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-287">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="bfc7e-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="bfc7e-288">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bfc7e-289">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="bfc7e-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="bfc7e-290">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="bfc7e-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
