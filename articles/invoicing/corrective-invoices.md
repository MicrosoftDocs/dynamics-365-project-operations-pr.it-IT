---
title: Creare fatture basate su progetto correttive
description: Questo argomento fornisce informazioni sulle fatture correttive in Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788868"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="95a05-103">Creare fatture basate su progetto correttive</span><span class="sxs-lookup"><span data-stu-id="95a05-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="95a05-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="95a05-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="95a05-105">Una fattura di progetto confermata può essere corretta per elaborare modifiche o crediti come negoziato con il cliente e il project manager.</span><span class="sxs-lookup"><span data-stu-id="95a05-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="95a05-106">Per apportare modifiche a una fattura confermata, apri la fattura confermata e seleziona **Correggi questa fattura**.</span><span class="sxs-lookup"><span data-stu-id="95a05-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="95a05-107">Questa selezione non è disponibile se la fattura di progetto non è confermata.</span><span class="sxs-lookup"><span data-stu-id="95a05-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="95a05-108">Viene creata una nuova fattura in bozza dalla fattura confermata.</span><span class="sxs-lookup"><span data-stu-id="95a05-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="95a05-109">Tutti i dettagli della riga della fattura confermata in precedenza vengono copiati nella nuova bozza.</span><span class="sxs-lookup"><span data-stu-id="95a05-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="95a05-110">Di seguito sono riportati alcuni punti chiave per aiutarti a comprendere meglio i dettagli della riga nella nuova fattura corretta:</span><span class="sxs-lookup"><span data-stu-id="95a05-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="95a05-111">Tutte le quantità vengono aggiornate a zero.</span><span class="sxs-lookup"><span data-stu-id="95a05-111">All quantities are updated to zero.</span></span> <span data-ttu-id="95a05-112">Ciò presuppone che tutti gli articoli fatturati siano completamente accreditati.</span><span class="sxs-lookup"><span data-stu-id="95a05-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="95a05-113">Se necessario puoi aggiornare manualmente queste quantità per riflettere la quantità che viene fatturata e non la quantità che viene accreditata.</span><span class="sxs-lookup"><span data-stu-id="95a05-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="95a05-114">In base alla quantità immessa, l'applicazione calcola la quantità accreditata.</span><span class="sxs-lookup"><span data-stu-id="95a05-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="95a05-115">Questo importo si riflette nei valori effettivi creati quando la fattura corretta viene confermata.</span><span class="sxs-lookup"><span data-stu-id="95a05-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="95a05-116">Se stai apportando modifiche all'importo delle imposte, devi immettere l'importo delle imposte corretto e non l'importo delle imposte che viene accreditato.</span><span class="sxs-lookup"><span data-stu-id="95a05-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="95a05-117">Le correzioni fondamentali vengono sempre elaborate come crediti completi.</span><span class="sxs-lookup"><span data-stu-id="95a05-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="95a05-118">Gli importi di acconto o anticipo possono essere corretti se al cliente è stato fatturato un importo errato.</span><span class="sxs-lookup"><span data-stu-id="95a05-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="95a05-119">Le riconciliazioni di acconti e anticipi possono essere corrette se è stato utilizzato un importo errato per la riconciliazione con gli addebiti di una fattura precedentemente confermata.</span><span class="sxs-lookup"><span data-stu-id="95a05-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95a05-120">Per i dettagli della riga fattura che sono correzioni ad altri addebiti già fatturati, il campo **Correzione** è impostato su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="95a05-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="95a05-121">Le fatture con i dettagli della riga fattura corretti hanno anche un campo chiamato **Include correzioni** impostato su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="95a05-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="95a05-122">Valori effettivi creati alla conferma di una fattura correttiva</span><span class="sxs-lookup"><span data-stu-id="95a05-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="95a05-123">La tabella seguente elenca i valori effettivi creati quando viene confermata una fattura correttiva.</span><span class="sxs-lookup"><span data-stu-id="95a05-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="95a05-124">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95a05-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="95a05-125">
                    <strong>Valori effettivi creati alla conferma</strong>
                </span><span class="sxs-lookup"><span data-stu-id="95a05-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="95a05-126">Conferma la correzione di un anticipo o un acconto fatturato.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="95a05-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-127">Uno storno delle vendite non fatturate dell'acconto o dell'anticipo creato per la riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="95a05-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="95a05-128">Questo importo è positivo perché ha lo scopo di annullare il negativo che è stato creato al momento della fatturazione dell'acconto o dell'anticipo.</span><span class="sxs-lookup"><span data-stu-id="95a05-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-129">Viene creato un valore effettivo di storno delle vendite fatturate per l'importo dell'acconto o dell'anticipo per stornare le vendite fatturate originali.</span><span class="sxs-lookup"><span data-stu-id="95a05-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-130">Viene creato un nuovo valore effettivo di vendite fatturate per l'importo corretto nella riga fattura corretta basata sull'anticipo o sull'acconto.</span><span class="sxs-lookup"><span data-stu-id="95a05-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-131">Un valore effettivo delle vendite non fatturate dell'importo negativo della riga fattura corretta basata sull'acconto o sull'anticipo che verrà utilizzata per la riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="95a05-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="95a05-132">Una conferma della correzione di un acconto o un anticipo precedentemente riconciliato.</span><span class="sxs-lookup"><span data-stu-id="95a05-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-133">Uno storno delle vendite non fatturate dell'acconto o dell'anticipo creato per la riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="95a05-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="95a05-134">Questo importo è positivo e ha lo scopo di annullare il negativo che è stato creato al momento della precedente riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="95a05-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-135">Un valore effettivo di storno delle vendite fatturate per l'importo della fattura precedente.</span><span class="sxs-lookup"><span data-stu-id="95a05-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-136">Un nuovo valore effettivo di vendite fatturate per l'importo dell'acconto corretto applicato nella fattura corretta.</span><span class="sxs-lookup"><span data-stu-id="95a05-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-137">Un valore effettivo delle vendite non fatturate con un importo negativo dell'acconto o dell'anticipo corretto rimanente che verrà utilizzato per la riconciliazione di fatture successive.</span><span class="sxs-lookup"><span data-stu-id="95a05-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95a05-138">La fatturazione del credito completo di una transazione temporale precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="95a05-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-139">Uno storno delle vendite fatturate per le ore e l'importo nel dettaglio della riga fattura originale per il tempo.</span><span class="sxs-lookup"><span data-stu-id="95a05-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-140">Un nuovo valore effettivo delle vendite non fatturate per le ore e l'importo nel dettaglio della riga fattura originale per il tempo.</span><span class="sxs-lookup"><span data-stu-id="95a05-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="95a05-141">La fatturazione dell'accredito parziale su una transazione temporale.</span><span class="sxs-lookup"><span data-stu-id="95a05-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-142">Uno storno delle vendite fatturate per le ore e l'importo fatturato nel dettaglio della riga fattura originale per il tempo.</span><span class="sxs-lookup"><span data-stu-id="95a05-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-143">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nel dettaglio della riga fattura modificata, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="95a05-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-144">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo rimanente dopo aver dedotto le cifre corrette nel dettaglio della riga fattura.</span><span class="sxs-lookup"><span data-stu-id="95a05-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95a05-145">La fatturazione del credito completo di una transazione di spesa precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="95a05-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-146">Uno storno delle vendite fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la spesa.</span><span class="sxs-lookup"><span data-stu-id="95a05-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-147">Un nuovo valore effettivo delle vendite non fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la spesa.</span><span class="sxs-lookup"><span data-stu-id="95a05-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="95a05-148">La fatturazione del credito parziale di una transazione di spesa precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="95a05-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-149">Uno storno delle vendite fatturate per la quantità e l'importo fatturato nel dettaglio della riga fattura originale per una spesa.</span><span class="sxs-lookup"><span data-stu-id="95a05-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-150">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura corretta, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="95a05-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-151">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo rimanente dopo aver dedotto le cifre corrette nel dettaglio della riga fattura.</span><span class="sxs-lookup"><span data-stu-id="95a05-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95a05-152">La fatturazione del credito completo di una transazione di commissione precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="95a05-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-153">Uno storno delle vendite fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la commissione.</span><span class="sxs-lookup"><span data-stu-id="95a05-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-154">Un nuovo valore effettivo delle vendite non fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la commissione.</span><span class="sxs-lookup"><span data-stu-id="95a05-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="95a05-155">La fatturazione del credito parziale di una transazione di commissione precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="95a05-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-156">Uno storno delle vendite fatturate per la quantità e l'importo fatturato nel dettaglio della riga fattura originale per la commissione.</span><span class="sxs-lookup"><span data-stu-id="95a05-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-157">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura correttiva modificata, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="95a05-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="95a05-158">La fatturazione del credito completo di un passaggio fondamentale precedentemente fatturato.</span><span class="sxs-lookup"><span data-stu-id="95a05-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-159">Uno storno delle vendite fatturate per l'importo nel dettaglio della riga fattura originale per il passaggio fondamentale.</span><span class="sxs-lookup"><span data-stu-id="95a05-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="95a05-160">Lo stato della fattura nel passaggio fondamentale viene aggiornato da <b>Fattura cliente registrata</b> a <b>Pronto per la fatturazione</b>.</span><span class="sxs-lookup"><span data-stu-id="95a05-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="95a05-161">La fatturazione del credito parziale di un passaggio fondamentale precedentemente fatturato.</span><span class="sxs-lookup"><span data-stu-id="95a05-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="95a05-162">Non supportato</span><span class="sxs-lookup"><span data-stu-id="95a05-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
