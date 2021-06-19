---
title: Fatture basate su progetto correttive
description: Questo argomento fornisce informazioni su come creare e confermare fatture correttive basate su progetto in Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012276"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="6d27b-103">Fatture basate su progetto correttive</span><span class="sxs-lookup"><span data-stu-id="6d27b-103">Corrective project-based invoices</span></span>

<span data-ttu-id="6d27b-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="6d27b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6d27b-105">Una fattura di progetto confermata può essere corretta per elaborare modifiche o crediti come negoziato con il cliente e il project manager.</span><span class="sxs-lookup"><span data-stu-id="6d27b-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="6d27b-106">Per apportare modifiche a una fattura confermata, apri la fattura confermata e seleziona **Correggi questa fattura**.</span><span class="sxs-lookup"><span data-stu-id="6d27b-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="6d27b-107">Questa selezione non è disponibile a meno che una fattura di progetto non venga confermata o la fattura basata su progetto non contenga anticipi o acconti o riconciliazioni di anticipi o acconti.</span><span class="sxs-lookup"><span data-stu-id="6d27b-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="6d27b-108">Viene creata una nuova fattura in bozza dalla fattura confermata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="6d27b-109">Tutti i dettagli della riga della fattura confermata in precedenza vengono copiati nella nuova bozza.</span><span class="sxs-lookup"><span data-stu-id="6d27b-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="6d27b-110">Di seguito sono riportati alcuni dei punti chiave da comprendere sui dettagli della riga sulla nuova fattura corretta:</span><span class="sxs-lookup"><span data-stu-id="6d27b-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="6d27b-111">Tutte le quantità vengono aggiornate a zero.</span><span class="sxs-lookup"><span data-stu-id="6d27b-111">All quantities are updated to zero.</span></span> <span data-ttu-id="6d27b-112">Dynamics 365 Project Operations presuppone che tutti gli articoli fatturati siano completamente accreditati.</span><span class="sxs-lookup"><span data-stu-id="6d27b-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="6d27b-113">Se necessario puoi aggiornare manualmente queste quantità per riflettere la quantità che viene fatturata e non la quantità che viene accreditata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="6d27b-114">In base alla quantità immessa, l'applicazione calcola la quantità accreditata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="6d27b-115">Questo importo si riflette nei valori effettivi creati quando la fattura corretta viene confermata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="6d27b-116">Se stai apportando modifiche all'importo delle imposte, devi immettere l'importo delle imposte corretto e non l'importo delle imposte che viene accreditato.</span><span class="sxs-lookup"><span data-stu-id="6d27b-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="6d27b-117">Le correzioni fondamentali vengono sempre elaborate come crediti completi.</span><span class="sxs-lookup"><span data-stu-id="6d27b-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="6d27b-118">Per i dettagli della riga fattura che sono correzioni ad altri addebiti già fatturati, il campo **Correzione** è impostato su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="6d27b-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="6d27b-119">Per le fatture con dettagli della riga fattura corretti, il campo **Include correzioni** è impostato su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="6d27b-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="6d27b-120">Valori effettivi creati quando una fattura correttiva viene confermata</span><span class="sxs-lookup"><span data-stu-id="6d27b-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="6d27b-121">La tabella seguente elenca i valori effettivi creati quando viene confermata una fattura correttiva.</span><span class="sxs-lookup"><span data-stu-id="6d27b-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="6d27b-122">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d27b-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="6d27b-123">
                    <strong>Valori effettivi creati alla conferma</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6d27b-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d27b-124">La fatturazione del credito completo di una transazione temporale precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-125">Uno storno delle vendite fatturate per le ore e l'importo nel dettaglio della riga fattura originale per il tempo.</span><span class="sxs-lookup"><span data-stu-id="6d27b-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-126">Un nuovo valore effettivo delle vendite non fatturate per le ore e l'importo nel dettaglio della riga fattura originale per il tempo.</span><span class="sxs-lookup"><span data-stu-id="6d27b-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6d27b-127">La fatturazione dell'accredito parziale su una transazione temporale.</span><span class="sxs-lookup"><span data-stu-id="6d27b-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-128">Uno storno delle vendite fatturate per le ore e l'importo fatturato nel dettaglio della riga fattura originale per il tempo.</span><span class="sxs-lookup"><span data-stu-id="6d27b-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-129">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nel dettaglio della riga fattura modificata, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="6d27b-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-130">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo rimanente dopo aver dedotto le cifre corrette nel dettaglio della riga fattura.</span><span class="sxs-lookup"><span data-stu-id="6d27b-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d27b-131">La fatturazione del credito completo di una transazione di spesa precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-132">Uno storno delle vendite fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la spesa.</span><span class="sxs-lookup"><span data-stu-id="6d27b-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-133">Un nuovo valore effettivo delle vendite non fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la spesa.</span><span class="sxs-lookup"><span data-stu-id="6d27b-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6d27b-134">La fatturazione del credito parziale di una transazione di spesa precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-135">Uno storno delle vendite fatturate per la quantità e l'importo fatturato nel dettaglio della riga fattura originale per una spesa.</span><span class="sxs-lookup"><span data-stu-id="6d27b-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-136">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura corretta, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="6d27b-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-137">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo rimanente dopo aver dedotto le cifre corrette nel dettaglio della riga fattura.</span><span class="sxs-lookup"><span data-stu-id="6d27b-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d27b-138">Fatturazione dell'intero credito di una transazione materiale precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-139">Uno storno vendite fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per il materiale.</span><span class="sxs-lookup"><span data-stu-id="6d27b-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-140">Un nuovo valore effettivo di vendita non fatturata per la quantità e l'importo nel dettaglio della riga fattura originale per il materiale.</span><span class="sxs-lookup"><span data-stu-id="6d27b-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6d27b-141">Fatturazione dell'accredito parziale in una transazione materiale.</span><span class="sxs-lookup"><span data-stu-id="6d27b-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-142">Uno storno vendite fatturate per la quantità e l'importo fatturato nel dettaglio della riga fattura originale per il materiale.</span><span class="sxs-lookup"><span data-stu-id="6d27b-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-143">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, un relativo storno e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="6d27b-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-144">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo rimanente dopo aver dedotto le cifre corrette nel dettaglio della riga fattura.</span><span class="sxs-lookup"><span data-stu-id="6d27b-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d27b-145">La fatturazione del credito completo di una transazione di commissione precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-146">Uno storno delle vendite fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la commissione.</span><span class="sxs-lookup"><span data-stu-id="6d27b-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-147">Un nuovo valore effettivo delle vendite non fatturate per la quantità e l'importo nel dettaglio della riga fattura originale per la commissione.</span><span class="sxs-lookup"><span data-stu-id="6d27b-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6d27b-148">La fatturazione del credito parziale di una transazione di commissione precedentemente fatturata.</span><span class="sxs-lookup"><span data-stu-id="6d27b-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-149">Uno storno delle vendite fatturate per la quantità e l'importo fatturato nel dettaglio della riga fattura originale per la commissione.</span><span class="sxs-lookup"><span data-stu-id="6d27b-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-150">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura correttiva modificata, uno storno di essa e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="6d27b-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6d27b-151">La fatturazione del credito completo di un passaggio fondamentale precedentemente fatturato.</span><span class="sxs-lookup"><span data-stu-id="6d27b-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-152">Uno storno delle vendite fatturate per l'importo nel dettaglio della riga fattura originale per il passaggio fondamentale.</span><span class="sxs-lookup"><span data-stu-id="6d27b-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="6d27b-153">Lo stato della fattura del passaggio fondamentale viene aggiornato da <b>Fattura cliente registrata</b> a <b>Pronto per la fatturazione</b>.</span><span class="sxs-lookup"><span data-stu-id="6d27b-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6d27b-154">La fatturazione del credito parziale di un passaggio fondamentale precedentemente fatturato.</span><span class="sxs-lookup"><span data-stu-id="6d27b-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6d27b-155">Questo scenario non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6d27b-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
