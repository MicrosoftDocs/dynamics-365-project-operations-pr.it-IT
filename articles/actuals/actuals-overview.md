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
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996616"
---
# <a name="actuals"></a><span data-ttu-id="9c2e1-103">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="9c2e1-103">Actuals</span></span> 

<span data-ttu-id="9c2e1-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="9c2e1-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c2e1-105">I valori effettivi rappresentano l'avanzamento finanziario e programmato rivisto e approvato di un progetto.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="9c2e1-106">Vengono creati come risultato dell'approvazione di voci di tempo, spese, utilizzo di materiale, scritture contabili e fatture.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="9c2e1-107">Invio righe giornale di registrazione e tempo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-107">Journal lines and time submission</span></span>

<span data-ttu-id="9c2e1-108">Per ulteriori informazioni sull'inserimento ore, vedi [Panoramica dell'inserimento ore](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9c2e1-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9c2e1-109">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="9c2e1-109">Time and materials</span></span>

<span data-ttu-id="9c2e1-110">Quando un inserimento ore inviato è collegato a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9c2e1-111">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="9c2e1-111">Fixed price</span></span>

<span data-ttu-id="9c2e1-112">Quando un inserimento ore inviato è collegato a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9c2e1-113">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="9c2e1-113">Default pricing</span></span>

<span data-ttu-id="9c2e1-114">La logica di creazione dei prezzi predefiniti risiede nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="9c2e1-115">I valori di campo di un inserimento ore vengono copiati nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="9c2e1-116">Questi valori includono la data della transazione, la voce di contratto a cui il progetto è mappato e la valuta nel listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="9c2e1-117">I campi che determinano i prezzi predefiniti, ad esempio **Ruolo** e **Unità gestione risorse**, sono utilizzati per determinare il prezzo appropriato nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="9c2e1-118">Puoi aggiungere un campo personalizzato all'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="9c2e1-119">Se il valore del campo deve essere propagato ai valori effettivi, crea il campo nelle tabelle **Valori effettivi** e **Riga giornale di registrazione**.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="9c2e1-120">Utilizza il codice personalizzato per propagare il valore del campo selezionato da Inserimento ore a Valori effettivi attraverso la riga giornale di registrazione utilizzando le origini delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="9c2e1-121">Per ulteriori informazioni sulle origini e le connessioni delle transazioni, vedi [Collegamento dei valori effettivi ai record originali](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="9c2e1-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="9c2e1-122">Invio righe giornale di registrazione e spesa di base</span><span class="sxs-lookup"><span data-stu-id="9c2e1-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="9c2e1-123">Per ulteriori informazioni sull'inserimento spese, vedi [Panoramica della spesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9c2e1-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9c2e1-124">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="9c2e1-124">Time and materials</span></span>

<span data-ttu-id="9c2e1-125">Quando una spesa di base inviata è collegata a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9c2e1-126">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="9c2e1-126">Fixed price</span></span>

<span data-ttu-id="9c2e1-127">Quando una voce di spesa di base inviata viene collegata a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9c2e1-128">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="9c2e1-128">Default pricing</span></span>

<span data-ttu-id="9c2e1-129">La logica per l'immissione dei prezzi predefiniti per le spese si basa sulla categoria di spesa.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="9c2e1-130">La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="9c2e1-131">I campi che determinano i prezzi predefiniti, ad esempio **Categoria di transazione** e **Unità**, sono utilizzati per determinare il prezzo appropriato nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="9c2e1-132">Tuttavia, ciò funziona solo quando il metodo di determinazione dei prezzi nel listino prezzi è **Prezzo unitario**.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="9c2e1-133">Se il metodo di determinazione dei prezzi è **Al costo** o **Ricarico sul costo**, il prezzo immesso alla creazione della voce di spesa viene utilizzato per il costo e il prezzo nella riga giornale di registrazione vendite viene calcolato in base al metodo di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="9c2e1-134">È possibile aggiungere un campo personalizzato alla voce di spesa.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="9c2e1-135">Se il valore del campo deve essere propagato ai valori effettivi, crea il campo nelle tabelle **Valori effettivi** e **Riga giornale di registrazione**.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="9c2e1-136">Utilizza il codice personalizzato per propagare il valore del campo selezionato da Inserimento ore a Valori effettivi attraverso la riga giornale di registrazione utilizzando le origini delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="9c2e1-137">Per ulteriori informazioni sulle origini e le connessioni delle transazioni, vedi [Collegamento dei valori effettivi ai record originali](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="9c2e1-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="9c2e1-138">Righe giornale di registrazione e invio del registro dell'utilizzo di materiale</span><span class="sxs-lookup"><span data-stu-id="9c2e1-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="9c2e1-139">Per ulteriori informazioni sulla voce di spesa, vedi [Registro dell'utilizzo di materiale](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="9c2e1-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9c2e1-140">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="9c2e1-140">Time and materials</span></span>

<span data-ttu-id="9c2e1-141">Quando una voce del registro dell'utilizzo di materiale inviata è collegata a un progetto mappato a una voce di contratto di tempo e materiali, il sistema crea due righe giornale di registrazione, una per i costi e una per le vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9c2e1-142">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="9c2e1-142">Fixed price</span></span>

<span data-ttu-id="9c2e1-143">Quando una voce del registro dell'utilizzo di materiale viene collegata a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9c2e1-144">Prezzi predefiniti</span><span class="sxs-lookup"><span data-stu-id="9c2e1-144">Default pricing</span></span>

<span data-ttu-id="9c2e1-145">La logica per l'immissione dei prezzi predefiniti per il materiale si basa sulla combinazione di prodotto e unità.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="9c2e1-146">La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="9c2e1-147">I campi che determinano i prezzi predefiniti, ad esempio **ID prodotto** e **Unità**, sono utilizzati per determinare il prezzo appropriato nella riga giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="9c2e1-148">Tuttavia, ciò funziona solo per i prodotti del catalogo.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-148">However, this only works for catalog products.</span></span> <span data-ttu-id="9c2e1-149">Per i prodotti fuori catalogo, il prezzo immesso quando viene creata la voce del registro dell'utilizzo di materiale viene utilizzata per il prezzo di costo e di vendita nelle righe giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="9c2e1-150">È possibile aggiungere un campo personalizzato alla voce **Registro dell'utilizzo di materiale**.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="9c2e1-151">Se il valore del campo deve essere propagato ai valori effettivi, crea il campo nelle tabelle **Valori effettivi** e **Riga giornale di registrazione**.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="9c2e1-152">Utilizza il codice personalizzato per propagare il valore del campo selezionato da Inserimento ore a Valori effettivi attraverso la riga giornale di registrazione utilizzando le origini delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="9c2e1-153">Per ulteriori informazioni sulle origini e le connessioni delle transazioni, vedi [Collegamento dei valori effettivi ai record originali](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="9c2e1-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="9c2e1-154">Utilizza giornali di registrazione per registrare i costi</span><span class="sxs-lookup"><span data-stu-id="9c2e1-154">Use entry journals to record costs</span></span>

<span data-ttu-id="9c2e1-155">Puoi utilizzare i giornali di registrazione per registrare costi o ricavi nelle classi di materiali, imposte, tempo, spese o transazioni fiscali.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="9c2e1-156">I giornali di registrazione possono per gli scopi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c2e1-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="9c2e1-157">Sposta i valori effettivi di transazioni da un altro sistema in Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="9c2e1-158">Registra i costi che si sono verificati in un altro sistema.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="9c2e1-159">Questi costi possono includere costi di approvvigionamento o subappalto.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c2e1-160">L'applicazione non convalida il tipo di riga del giornale di registrazione o il prezzo correlato immesso nella riga del giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="9c2e1-161">Pertanto, solo un utente che è pienamente consapevole dell'impatto contabile che i valori effettivi hanno sul progetto deve utilizzare i giornali di registrazione per creare i valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="9c2e1-162">A causa dell'impatto di questo tipo di giornale di registrazione, è consigliabile scegliere con attenzione chi ha accesso per creare i giornali di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="9c2e1-163">Registrare valori effettivi basati su eventi di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-163">Record actuals based on project events</span></span>

<span data-ttu-id="9c2e1-164">Project Operations registra le transazioni finanziarie che si hanno durante un progetto.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="9c2e1-165">Queste transazioni vengono registrate come valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="9c2e1-166">Nella tabella seguente sono riportati i differenti tipi di valori effettivi creati, a seconda se il progetto è un progetto tempistica e materiali, prezzo fisso, interno o in fase di prevendita.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="9c2e1-167">La risorsa appartiene alla stessa unità organizzativa dell'unità contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9c2e1-168">Event</span><span class="sxs-lookup"><span data-stu-id="9c2e1-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9c2e1-169">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9c2e1-170">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="9c2e1-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9c2e1-171">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="9c2e1-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9c2e1-172">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="9c2e1-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9c2e1-173">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="9c2e1-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9c2e1-174">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="9c2e1-174">Actuals</span></span></th>
<th><span data-ttu-id="9c2e1-175">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="9c2e1-175">Transaction currency</span></span></th>
<th><span data-ttu-id="9c2e1-176">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="9c2e1-176">Fixed price</span></span></th>
<th><span data-ttu-id="9c2e1-177">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="9c2e1-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9c2e1-178">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9c2e1-179">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="9c2e1-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-180">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9c2e1-181">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="9c2e1-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c2e1-182">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9c2e1-183">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-183">Cost actual</span></span></td>
<td><span data-ttu-id="9c2e1-184">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-185">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-186">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="9c2e1-187">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-188">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-189">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9c2e1-190">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c2e1-191">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9c2e1-192">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-192">Cost actual</span></span></td>
<td><span data-ttu-id="9c2e1-193">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-194">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-195">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-196">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-197">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-198">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="9c2e1-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9c2e1-199">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-200">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="9c2e1-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c2e1-201">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c2e1-202">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9c2e1-203">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="9c2e1-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9c2e1-204">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-205">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="9c2e1-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-206">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-207">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-208">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-209">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="9c2e1-209">Billed sales</span></span></td>
<td><span data-ttu-id="9c2e1-210">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c2e1-211">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9c2e1-212">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="9c2e1-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9c2e1-213">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-214">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-215">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-216">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-217">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-218">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="9c2e1-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9c2e1-219">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-220">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="9c2e1-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c2e1-221">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c2e1-222">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9c2e1-223">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="9c2e1-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9c2e1-224">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9c2e1-225">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="9c2e1-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9c2e1-226">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="9c2e1-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9c2e1-227">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9c2e1-228">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9c2e1-229">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-230">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="9c2e1-230">Billed sales</span></span></td>
<td><span data-ttu-id="9c2e1-231">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c2e1-232">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9c2e1-233">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="9c2e1-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9c2e1-234">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-235">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="9c2e1-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9c2e1-236">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-237">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="9c2e1-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c2e1-238">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="9c2e1-239">La risorsa appartiene a un'unità organizzativa che differisce dall'unità contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9c2e1-240">Event</span><span class="sxs-lookup"><span data-stu-id="9c2e1-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9c2e1-241">Progetto fatturabile o venduto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9c2e1-242">Progetto nella fase di prevendita</span><span class="sxs-lookup"><span data-stu-id="9c2e1-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9c2e1-243">Progetto interno</span><span class="sxs-lookup"><span data-stu-id="9c2e1-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9c2e1-244">Tempistica e materiali</span><span class="sxs-lookup"><span data-stu-id="9c2e1-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9c2e1-245">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="9c2e1-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9c2e1-246">Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="9c2e1-246">Actuals</span></span></th>
<th><span data-ttu-id="9c2e1-247">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="9c2e1-247">Transaction currency</span></span></th>
<th><span data-ttu-id="9c2e1-248">Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="9c2e1-248">Fixed price</span></span></th>
<th><span data-ttu-id="9c2e1-249">Valuta delle transazioni</span><span class="sxs-lookup"><span data-stu-id="9c2e1-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9c2e1-250">Viene creato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9c2e1-251">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="9c2e1-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-252">Viene inviato un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9c2e1-253">Nessuna impegno nell'entità Valori effettivi</span><span class="sxs-lookup"><span data-stu-id="9c2e1-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="9c2e1-254">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9c2e1-255">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-255">Cost actual</span></span></td>
<td><span data-ttu-id="9c2e1-256">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9c2e1-257">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9c2e1-258">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9c2e1-259">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9c2e1-260">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-261">Valore effettivo vendite non fatturate - Addebitabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9c2e1-262">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-263">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="9c2e1-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9c2e1-264">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="9c2e1-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-265">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="9c2e1-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9c2e1-266">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="9c2e1-267">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9c2e1-268">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-268">Cost actual</span></span></td>
<td><span data-ttu-id="9c2e1-269">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9c2e1-270">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9c2e1-271">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9c2e1-272">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9c2e1-273">Valore effettivo costo</span><span class="sxs-lookup"><span data-stu-id="9c2e1-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-274">Costo unità gestione risorse</span><span class="sxs-lookup"><span data-stu-id="9c2e1-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9c2e1-275">Valuta unitaria gestione risorse</span><span class="sxs-lookup"><span data-stu-id="9c2e1-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-276">Vendite interorganizzative</span><span class="sxs-lookup"><span data-stu-id="9c2e1-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9c2e1-277">Valuta unità contratto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-278">Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="9c2e1-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9c2e1-279">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-280">Valore effettivo vendite non fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="9c2e1-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c2e1-281">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c2e1-282">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9c2e1-283">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="9c2e1-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9c2e1-284">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-285">Vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="9c2e1-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-286">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-287">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9c2e1-288">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-289">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="9c2e1-289">Billed sales</span></span></td>
<td><span data-ttu-id="9c2e1-290">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c2e1-291">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9c2e1-292">Storno vendite non fatturate</span><span class="sxs-lookup"><span data-stu-id="9c2e1-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9c2e1-293">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-294">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-295">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-296">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9c2e1-297">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-298">Vendite fatturate - Addebitabile per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="9c2e1-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9c2e1-299">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-300">Vendite fatturate - Non addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="9c2e1-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c2e1-301">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9c2e1-302">Una fattura viene rettificata per aumentare la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9c2e1-303">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="9c2e1-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9c2e1-304">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9c2e1-305">Storno vendite fatturate per passaggio fondamentale</span><span class="sxs-lookup"><span data-stu-id="9c2e1-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9c2e1-306">Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></span><span class="sxs-lookup"><span data-stu-id="9c2e1-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9c2e1-307">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9c2e1-308">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9c2e1-309">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="9c2e1-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-310">Vendite fatturate</span><span class="sxs-lookup"><span data-stu-id="9c2e1-310">Billed sales</span></span></td>
<td><span data-ttu-id="9c2e1-311">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9c2e1-312">Una fattura viene rettificata per diminuire la quantità addebitabile.</span><span class="sxs-lookup"><span data-stu-id="9c2e1-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9c2e1-313">Vendite fatturate - Storno</span><span class="sxs-lookup"><span data-stu-id="9c2e1-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9c2e1-314">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-315">Vendite fatturate per la nuova quantità</span><span class="sxs-lookup"><span data-stu-id="9c2e1-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9c2e1-316">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9c2e1-317">Vendite non fatturate - Addebitabile per la differenza</span><span class="sxs-lookup"><span data-stu-id="9c2e1-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9c2e1-318">Valuta contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="9c2e1-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
