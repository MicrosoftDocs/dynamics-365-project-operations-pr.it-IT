---
title: Valori effettivi
description: Questo argomento fornisce informazioni su come utilizzare i valori effettivi in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368616"
---
# <a name="actuals"></a><span data-ttu-id="e10b5-103">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="e10b5-103">Actuals</span></span> 

<span data-ttu-id="e10b5-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="e10b5-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e10b5-105">I valori effettivi rappresentano l'avanzamento finanziario e programmato rivisto e approvato di un progetto.</span><span class="sxs-lookup"><span data-stu-id="e10b5-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="e10b5-106">Vengono creati come risultato dell'approvazione di voci di tempo, spese, utilizzo di materiale, scritture contabili e fatture.</span><span class="sxs-lookup"><span data-stu-id="e10b5-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="e10b5-107">Invio righe giornale di registrazione e tempo</span><span class="sxs-lookup"><span data-stu-id="e10b5-107">Journal lines and time submission</span></span>

<span data-ttu-id="e10b5-108">Per ulteriori informazioni sull'inserimento ore, vedi [Panoramica dell'inserimento ore](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e10b5-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="e10b5-109">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="e10b5-109">Time and materials</span></span>

<span data-ttu-id="e10b5-110">Quando un inserimento ore inviato è collegato a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="e10b5-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="e10b5-111">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="e10b5-111">Fixed price</span></span>

<span data-ttu-id="e10b5-112">Quando un inserimento ore inviato è collegato a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="e10b5-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="e10b5-113">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="e10b5-113">Default pricing</span></span>

<span data-ttu-id="e10b5-114">La logica di creazione dei prezzi predefiniti risiede nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="e10b5-115">I valori di campo di un inserimento ore vengono copiati nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="e10b5-116">Questi valori includono la data della transazione, la voce di contratto a cui il progetto è mappato e la valuta nel listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="e10b5-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="e10b5-117">I campi che determinano i prezzi predefiniti, ad esempio **Ruolo** e **Unità gestione risorse**, sono utilizzati per determinare il prezzo appropriato nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="e10b5-118">Puoi aggiungere un campo personalizzato all'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="e10b5-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="e10b5-119">Se il valore del campo deve essere propagato ai valori effettivi, crea il campo nelle tabelle **Valori effettivi** e **Riga giornale di registrazione**.</span><span class="sxs-lookup"><span data-stu-id="e10b5-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="e10b5-120">Utilizza il codice personalizzato per propagare il valore del campo selezionato da Inserimento ore a Valori effettivi attraverso la riga giornale di registrazione utilizzando le origini delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="e10b5-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="e10b5-121">Per ulteriori informazioni sulle origini e le connessioni delle transazioni, vedi [Collegamento dei valori effettivi ai record originali](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="e10b5-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="e10b5-122">Invio righe giornale di registrazione e spesa di base</span><span class="sxs-lookup"><span data-stu-id="e10b5-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="e10b5-123">Per ulteriori informazioni sull'inserimento spese, vedi [Panoramica della spesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e10b5-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="e10b5-124">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="e10b5-124">Time and materials</span></span>

<span data-ttu-id="e10b5-125">Quando una spesa di base inviata è collegata a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="e10b5-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="e10b5-126">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="e10b5-126">Fixed price</span></span>

<span data-ttu-id="e10b5-127">Quando una voce di spesa di base inviata viene collegata a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="e10b5-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="e10b5-128">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="e10b5-128">Default pricing</span></span>

<span data-ttu-id="e10b5-129">La logica per l'immissione dei prezzi predefiniti per le spese si basa sulla categoria di spesa.</span><span class="sxs-lookup"><span data-stu-id="e10b5-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="e10b5-130">La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="e10b5-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="e10b5-131">I campi che determinano i prezzi predefiniti, ad esempio **Categoria di transazione** e **Unità**, sono utilizzati per determinare il prezzo appropriato nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="e10b5-132">Tuttavia, ciò funziona solo quando il metodo di determinazione dei prezzi nel listino prezzi è **Prezzo unitario**.</span><span class="sxs-lookup"><span data-stu-id="e10b5-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="e10b5-133">Se il metodo di determinazione dei prezzi è **Al costo** o **Ricarico sul costo**, il prezzo immesso alla creazione della voce di spesa viene utilizzato per il costo e il prezzo nella riga giornale di registrazione vendite viene calcolato in base al metodo di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="e10b5-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="e10b5-134">È possibile aggiungere un campo personalizzato alla voce di spesa.</span><span class="sxs-lookup"><span data-stu-id="e10b5-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="e10b5-135">Se il valore del campo deve essere propagato ai valori effettivi, crea il campo nelle tabelle **Valori effettivi** e **Riga giornale di registrazione**.</span><span class="sxs-lookup"><span data-stu-id="e10b5-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="e10b5-136">Utilizza il codice personalizzato per propagare il valore del campo selezionato da Inserimento ore a Valori effettivi attraverso la riga giornale di registrazione utilizzando le origini delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="e10b5-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="e10b5-137">Per ulteriori informazioni sulle origini e le connessioni delle transazioni, vedi [Collegamento dei valori effettivi ai record originali](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="e10b5-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="e10b5-138">Righe giornale di registrazione e invio del registro dell'utilizzo di materiale</span><span class="sxs-lookup"><span data-stu-id="e10b5-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="e10b5-139">Per ulteriori informazioni sulla voce di spesa, vedi [Registro dell'utilizzo di materiale](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="e10b5-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="e10b5-140">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="e10b5-140">Time and materials</span></span>

<span data-ttu-id="e10b5-141">Quando una voce del registro dell'utilizzo di materiale inviata è collegata a un progetto mappato a una voce di contratto di tempo e materiali, il sistema crea due righe giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="e10b5-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="e10b5-142">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="e10b5-142">Fixed price</span></span>

<span data-ttu-id="e10b5-143">Quando una voce del registro dell'utilizzo di materiale viene collegata a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="e10b5-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="e10b5-144">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="e10b5-144">Default pricing</span></span>

<span data-ttu-id="e10b5-145">La logica per l'immissione dei prezzi predefiniti per il materiale si basa sulla combinazione di prodotto e unità.</span><span class="sxs-lookup"><span data-stu-id="e10b5-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="e10b5-146">La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="e10b5-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="e10b5-147">I campi che determinano i prezzi predefiniti, ad esempio **ID prodotto** e **Unità**, sono utilizzati per determinare il prezzo appropriato nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="e10b5-148">Tuttavia, ciò funziona solo per i prodotti del catalogo.</span><span class="sxs-lookup"><span data-stu-id="e10b5-148">However, this only works for catalog products.</span></span> <span data-ttu-id="e10b5-149">Per i prodotti fuori catalogo, il prezzo immesso quando viene creata la voce del registro dell'utilizzo di materiale viene utilizzata per il prezzo di costo e di vendita nelle righe giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="e10b5-150">È possibile aggiungere un campo personalizzato alla voce **Registro dell'utilizzo di materiale**.</span><span class="sxs-lookup"><span data-stu-id="e10b5-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="e10b5-151">Se il valore del campo deve essere propagato ai valori effettivi, crea il campo nelle tabelle **Valori effettivi** e **Riga giornale di registrazione**.</span><span class="sxs-lookup"><span data-stu-id="e10b5-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="e10b5-152">Utilizza il codice personalizzato per propagare il valore del campo selezionato da Inserimento ore a Valori effettivi attraverso la riga giornale di registrazione utilizzando le origini delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="e10b5-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="e10b5-153">Per ulteriori informazioni sulle origini e le connessioni delle transazioni, vedi [Collegamento dei valori effettivi ai record originali](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="e10b5-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="e10b5-154">Utilizza giornali di registrazione per registrare i costi</span><span class="sxs-lookup"><span data-stu-id="e10b5-154">Use entry journals to record costs</span></span>

<span data-ttu-id="e10b5-155">Puoi utilizzare i giornali di registrazione per registrare costi o ricavi nelle classi di materiali, imposte, tempo, spese o transazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="e10b5-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="e10b5-156">I giornali di registrazione possono per gli scopi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e10b5-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="e10b5-157">Sposta i valori effettivi di transazioni da un altro sistema in Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e10b5-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="e10b5-158">Registra i costi che si sono verificati in un altro sistema.</span><span class="sxs-lookup"><span data-stu-id="e10b5-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="e10b5-159">Questi costi possono includere costi di approvvigionamento o subappalto.</span><span class="sxs-lookup"><span data-stu-id="e10b5-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e10b5-160">L'applicazione non convalida il tipo di riga del giornale di registrazione o il prezzo correlato immesso nella riga del giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="e10b5-161">Pertanto, solo un utente che è pienamente consapevole dell'impatto contabile che i valori effettivi hanno sul progetto deve utilizzare i giornali di registrazione per creare i valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="e10b5-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="e10b5-162">A causa dell'impatto di questo tipo di giornale di registrazione, è consigliabile scegliere con attenzione chi ha accesso per creare i giornali di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="e10b5-163">Registrare valori effettivi basati su eventi di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-163">Record actuals based on project events</span></span>

<span data-ttu-id="e10b5-164">Project Operations registra le transazioni finanziarie che si hanno durante un progetto.</span><span class="sxs-lookup"><span data-stu-id="e10b5-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="e10b5-165">Queste transazioni vengono registrate come valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="e10b5-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="e10b5-166">Nella tabella seguente sono riportati i differenti tipi di valori effettivi creati, a seconda se il progetto è un progetto tempistica e materiali, prezzo fisso, interno o in fase di prevendita.</span><span class="sxs-lookup"><span data-stu-id="e10b5-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="e10b5-167">La risorsa appartiene alla stessa unità organizzativa dell'unità contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="e10b5-168">Event</span><span class="sxs-lookup"><span data-stu-id="e10b5-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="e10b5-169">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="e10b5-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="e10b5-170">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="e10b5-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="e10b5-171">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="e10b5-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="e10b5-172">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="e10b5-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="e10b5-173">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="e10b5-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e10b5-174">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="e10b5-174">Actuals</span></span></th>
<th><span data-ttu-id="e10b5-175">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="e10b5-175">Transaction currency</span></span></th>
<th><span data-ttu-id="e10b5-176">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="e10b5-176">Fixed price</span></span></th>
<th><span data-ttu-id="e10b5-177">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="e10b5-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e10b5-178">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="e10b5-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="e10b5-179">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="e10b5-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-180">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="e10b5-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="e10b5-181">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="e10b5-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e10b5-182">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e10b5-183">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-183">Cost actual</span></span></td>
<td><span data-ttu-id="e10b5-184">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-185">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-186">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="e10b5-187">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-188">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-189">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="e10b5-190">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e10b5-191">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e10b5-192">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-192">Cost actual</span></span></td>
<td><span data-ttu-id="e10b5-193">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-194">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-195">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-196">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-197">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-198">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="e10b5-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e10b5-199">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-200">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="e10b5-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e10b5-201">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e10b5-202">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="e10b5-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e10b5-203">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="e10b5-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e10b5-204">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-205">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="e10b5-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-206">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-207">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-208">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-209">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="e10b5-209">Billed sales</span></span></td>
<td><span data-ttu-id="e10b5-210">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e10b5-211">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="e10b5-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e10b5-212">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="e10b5-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e10b5-213">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-214">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-215">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-216">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-217">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-218">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="e10b5-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e10b5-219">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-220">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="e10b5-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e10b5-221">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e10b5-222">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="e10b5-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e10b5-223">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="e10b5-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e10b5-224">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="e10b5-225">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="e10b5-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="e10b5-226">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="e10b5-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="e10b5-227">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e10b5-228">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="e10b5-229">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-230">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="e10b5-230">Billed sales</span></span></td>
<td><span data-ttu-id="e10b5-231">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e10b5-232">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="e10b5-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e10b5-233">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="e10b5-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e10b5-234">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-235">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="e10b5-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="e10b5-236">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-237">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="e10b5-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="e10b5-238">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="e10b5-239">La risorsa appartiene a un'unità organizzativa che differisce dall'unità contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="e10b5-240">Event</span><span class="sxs-lookup"><span data-stu-id="e10b5-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="e10b5-241">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="e10b5-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="e10b5-242">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="e10b5-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="e10b5-243">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="e10b5-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="e10b5-244">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="e10b5-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="e10b5-245">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="e10b5-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e10b5-246">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="e10b5-246">Actuals</span></span></th>
<th><span data-ttu-id="e10b5-247">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="e10b5-247">Transaction currency</span></span></th>
<th><span data-ttu-id="e10b5-248">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="e10b5-248">Fixed price</span></span></th>
<th><span data-ttu-id="e10b5-249">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="e10b5-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e10b5-250">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="e10b5-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="e10b5-251">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="e10b5-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-252">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="e10b5-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="e10b5-253">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="e10b5-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="e10b5-254">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e10b5-255">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-255">Cost actual</span></span></td>
<td><span data-ttu-id="e10b5-256">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="e10b5-257">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="e10b5-258">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="e10b5-259">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="e10b5-260">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-261">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="e10b5-262">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-263">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="e10b5-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="e10b5-264">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="e10b5-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-265">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="e10b5-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="e10b5-266">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="e10b5-267">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="e10b5-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e10b5-268">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-268">Cost actual</span></span></td>
<td><span data-ttu-id="e10b5-269">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e10b5-270">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="e10b5-271">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e10b5-272">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="e10b5-273">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="e10b5-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-274">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="e10b5-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="e10b5-275">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="e10b5-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-276">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="e10b5-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="e10b5-277">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="e10b5-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-278">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="e10b5-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e10b5-279">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-280">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="e10b5-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e10b5-281">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e10b5-282">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="e10b5-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e10b5-283">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="e10b5-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e10b5-284">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-285">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="e10b5-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-286">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-287">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="e10b5-288">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-289">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="e10b5-289">Billed sales</span></span></td>
<td><span data-ttu-id="e10b5-290">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e10b5-291">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="e10b5-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e10b5-292">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="e10b5-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e10b5-293">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-294">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-295">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-296">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e10b5-297">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-298">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="e10b5-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e10b5-299">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-300">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="e10b5-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e10b5-301">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e10b5-302">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="e10b5-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e10b5-303">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="e10b5-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e10b5-304">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="e10b5-305">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="e10b5-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="e10b5-306">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="e10b5-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="e10b5-307">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e10b5-308">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="e10b5-309">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e10b5-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-310">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="e10b5-310">Billed sales</span></span></td>
<td><span data-ttu-id="e10b5-311">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e10b5-312">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="e10b5-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e10b5-313">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="e10b5-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e10b5-314">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-315">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="e10b5-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="e10b5-316">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e10b5-317">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="e10b5-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="e10b5-318">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="e10b5-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
