---
title: Crediti e fatture corrette
description: Questo argomento fornisce informazioni sulle fatture corrette in Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078987"
---
# <a name="credits-and-corrected-invoices"></a><span data-ttu-id="d6719-103">Crediti e fatture corrette</span><span class="sxs-lookup"><span data-stu-id="d6719-103">Credits and corrected invoices</span></span>

<span data-ttu-id="d6719-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="d6719-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d6719-105">Una fattura di progetto confermata può essere corretta per elaborare modifiche o crediti come negoziato con il cliente e il project manager.</span><span class="sxs-lookup"><span data-stu-id="d6719-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="d6719-106">Per apportare modifiche a una fattura confermata, apri la fattura confermata e seleziona **Correggi questa fattura**.</span><span class="sxs-lookup"><span data-stu-id="d6719-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="d6719-107">Questa selezione non è disponibile se la fattura di progetto non è confermata.</span><span class="sxs-lookup"><span data-stu-id="d6719-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="d6719-108">Viene creata una nuova fattura in bozza dalla fattura confermata.</span><span class="sxs-lookup"><span data-stu-id="d6719-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="d6719-109">Tutti i dettagli della riga della fattura confermata in precedenza vengono copiati nella nuova bozza.</span><span class="sxs-lookup"><span data-stu-id="d6719-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="d6719-110">Di seguito sono riportati alcuni dei punti chiave da comprendere sui dettagli della riga sulla nuova fattura corretta:</span><span class="sxs-lookup"><span data-stu-id="d6719-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="d6719-111">Tutte le quantità vengono aggiornate a zero.</span><span class="sxs-lookup"><span data-stu-id="d6719-111">All quantities are updated to zero.</span></span> <span data-ttu-id="d6719-112">L'applicazione presuppone che tutti gli articoli fatturati siano completamente accreditati.</span><span class="sxs-lookup"><span data-stu-id="d6719-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="d6719-113">Se necessario puoi aggiornare manualmente queste quantità per riflettere la quantità che viene fatturata e non la quantità che viene accreditata.</span><span class="sxs-lookup"><span data-stu-id="d6719-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="d6719-114">In base alla quantità immessa, l'applicazione calcola la quantità accreditata.</span><span class="sxs-lookup"><span data-stu-id="d6719-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="d6719-115">Questo importo si riflette nei valori effettivi creati quando la fattura corretta viene confermata.</span><span class="sxs-lookup"><span data-stu-id="d6719-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="d6719-116">Se stai apportando modifiche all'importo delle imposte, devi immettere l'importo delle imposte corretto e non l'importo delle imposte che viene accreditato.</span><span class="sxs-lookup"><span data-stu-id="d6719-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="d6719-117">Le voci di contratto basate su prodotto confermate in precedenza non vengono copiate.</span><span class="sxs-lookup"><span data-stu-id="d6719-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="d6719-118">L'elaborazione delle correzioni su una fattura di progetto basata su prodotto non è supportata.</span><span class="sxs-lookup"><span data-stu-id="d6719-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="d6719-119">Le correzioni fondamentali vengono sempre elaborate come crediti completi.</span><span class="sxs-lookup"><span data-stu-id="d6719-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="d6719-120">Gli importi di acconto o anticipo possono essere corretti se al cliente è stato fatturato un importo errato.</span><span class="sxs-lookup"><span data-stu-id="d6719-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="d6719-121">Le riconciliazioni di acconti e anticipi possono essere corrette se è stato utilizzato un importo errato per la riconciliazione con gli addebiti di una fattura precedentemente confermata.</span><span class="sxs-lookup"><span data-stu-id="d6719-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6719-122">I dettagli della riga fattura che sono correzioni ad altri addebiti già fatturati hanno il campo **Correzione** impostato su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="d6719-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="d6719-123">Le fatture con i dettagli della riga fattura corretti hanno anche un campo chiamato **Include correzioni** impostato su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="d6719-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="d6719-124">I valori effettivi creati alla conferma di una fattura correttiva:</span><span class="sxs-lookup"><span data-stu-id="d6719-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="d6719-125">Di seguito sono riportati i valori effettivi creati dall'applicazione alla conferma di una correzione in base alle operazioni eseguite sulla bozza di fattura correttiva prima della conferma.</span><span class="sxs-lookup"><span data-stu-id="d6719-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="d6719-126">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d6719-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="d6719-127">
                    <strong>Valori effettivi creati alla conferma</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d6719-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="d6719-128">Conferma la correzione di un anticipo o un acconto fatturato.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d6719-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-129">Uno storno delle vendite non fatturate dell'acconto o dell'anticipo creato per la riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="d6719-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d6719-130">Questo importo è positivo perché ha lo scopo di annullare il negativo che è stato creato al momento della fatturazione dell'acconto o dell'anticipo.</span><span class="sxs-lookup"><span data-stu-id="d6719-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-131">Viene creato un valore effettivo di storno delle vendite fatturate per l'importo dell'acconto o dell'anticipo per stornare le vendite fatturate originali.</span><span class="sxs-lookup"><span data-stu-id="d6719-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-132">Viene creato un nuovo valore effettivo di vendite fatturate per l'importo corretto nella riga fattura corretta basata sull'anticipo o sull'acconto.</span><span class="sxs-lookup"><span data-stu-id="d6719-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-133">Un valore effettivo delle vendite non fatturate dell'importo negativo della riga fattura corretta basata sull'acconto o sull'anticipo che verrà utilizzata per la riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="d6719-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="d6719-134">Una conferma della correzione di un acconto o un anticipo precedentemente riconciliato.</span><span class="sxs-lookup"><span data-stu-id="d6719-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-135">Uno storno delle vendite non fatturate dell'acconto o dell'anticipo creato per la riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="d6719-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d6719-136">Questo importo è positivo e ha lo scopo di annullare il negativo che è stato creato al momento della precedente riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="d6719-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-137">Un valore effettivo di storno delle vendite fatturate per l'importo della fattura precedente.</span><span class="sxs-lookup"><span data-stu-id="d6719-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-138">Un nuovo valore effettivo di vendite fatturate per l'importo dell'acconto corretto applicato nella fattura corretta.</span><span class="sxs-lookup"><span data-stu-id="d6719-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-139">Un valore effettivo delle vendite non fatturate con un importo negativo dell'acconto o dell'anticipo corretto rimanente che verrà utilizzato per la riconciliazione di fatture successive.</span><span class="sxs-lookup"><span data-stu-id="d6719-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d6719-140">La fatturazione del credito completo di una transazione temporale precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="d6719-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-141">Uno storno delle vendite fatturate per le ore e l'importo nei dettagli della riga fattura originale per il tempo.</span><span class="sxs-lookup"><span data-stu-id="d6719-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-142">Un nuovo valore effettivo delle vendite non fatturate per le ore e l'importo nei dettagli della riga fattura originale per il tempo.</span><span class="sxs-lookup"><span data-stu-id="d6719-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d6719-143">La fatturazione dell'accredito parziale su una transazione temporale.</span><span class="sxs-lookup"><span data-stu-id="d6719-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-144">Uno storno delle vendite fatturate per le ore e l'importo fatturato nei dettagli della riga fattura originale per il tempo.</span><span class="sxs-lookup"><span data-stu-id="d6719-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-145">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nei dettagli della riga fattura modificata, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="d6719-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-146">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo rimanente dopo aver dedotto le cifre corrette nei dettagli della riga fattura.</span><span class="sxs-lookup"><span data-stu-id="d6719-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d6719-147">La fatturazione del credito completo di una transazione di spesa precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="d6719-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-148">Uno storno delle vendite fatturate per la quantità e l'importo nei dettagli della riga fattura originale per la spesa.</span><span class="sxs-lookup"><span data-stu-id="d6719-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-149">Un nuovo valore effettivo delle vendite non fatturate per la quantità e l'importo nei dettagli della riga fattura originale per la spesa.</span><span class="sxs-lookup"><span data-stu-id="d6719-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d6719-150">La fatturazione del credito parziale di una transazione di spesa precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="d6719-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-151">Uno storno delle vendite fatturate per la quantità e l'importo fatturato nei dettagli della riga fattura originale per una spesa.</span><span class="sxs-lookup"><span data-stu-id="d6719-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-152">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nei dettagli della riga fattura corretta, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="d6719-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-153">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo rimanente dopo aver dedotto le cifre corrette nei dettagli della riga fattura.</span><span class="sxs-lookup"><span data-stu-id="d6719-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d6719-154">La fatturazione del credito completo di una transazione di commissione precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="d6719-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-155">Uno storno delle vendite fatturate per la quantità e l'importo nei dettagli della riga fattura originale per la commissione.</span><span class="sxs-lookup"><span data-stu-id="d6719-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-156">Un nuovo valore effettivo delle vendite non fatturate per la quantità e l'importo nei dettagli della riga fattura originale per la commissione.</span><span class="sxs-lookup"><span data-stu-id="d6719-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d6719-157">La fatturazione del credito parziale di una transazione di commissione precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="d6719-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-158">Uno storno delle vendite fatturate per la quantità e l'importo fatturato nei dettagli della riga fattura originale per la commissione.</span><span class="sxs-lookup"><span data-stu-id="d6719-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-159">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nei dettagli della riga fattura correttiva modificata, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="d6719-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d6719-160">La fatturazione del credito completo di un passaggio fondamentale precedentemente fatturato.</span><span class="sxs-lookup"><span data-stu-id="d6719-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-161">Uno storno delle vendite fatturate per l'importo nei dettagli della riga fattura originale per il passaggio fondamentale.</span><span class="sxs-lookup"><span data-stu-id="d6719-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="d6719-162">La fattura del passaggio fondamentale o lo stato di fatturazione nella riga contratto di progetto viene aggiornato su **Pronto per la fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="d6719-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d6719-163">La fatturazione del credito parziale di un passaggio fondamentale precedentemente fatturato.</span><span class="sxs-lookup"><span data-stu-id="d6719-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-164">Non supportato</span><span class="sxs-lookup"><span data-stu-id="d6719-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d6719-165">Crediti e correzioni di una voce di contratto basata su prodotto precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="d6719-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6719-166">Non supportato</span><span class="sxs-lookup"><span data-stu-id="d6719-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
