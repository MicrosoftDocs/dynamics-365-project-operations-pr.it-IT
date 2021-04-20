---
title: Confermare una fattura basata su progetto proforma
description: Questo argomento fornisce informazioni sulla conferma di una fattura basata su progetto proforma.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867136"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="87bc4-103">Confermare una fattura basata su progetto proforma</span><span class="sxs-lookup"><span data-stu-id="87bc4-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="87bc4-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="87bc4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="87bc4-105">Dopo la conferma di una fattura proforma, lo stato della fattura di progetto viene aggiornato su **Confermato**.</span><span class="sxs-lookup"><span data-stu-id="87bc4-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="87bc4-106">Quando una fattura viene confermata, diventa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="87bc4-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="87bc4-107">In futuro, la fattura potrà essere corretta solo se sono presenti correzioni o accrediti avviati dal cliente.</span><span class="sxs-lookup"><span data-stu-id="87bc4-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="87bc4-108">Nella tabella seguente sono elencati i valori effettivi creati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="87bc4-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="87bc4-109">Questi valori effettivi vengono creati quando vengono eseguite determinate operazioni sulla bozza della fattura di progetto prima che venga confermata.</span><span class="sxs-lookup"><span data-stu-id="87bc4-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="87bc4-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="87bc4-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="87bc4-111">
                    <strong>Valori effettivi creati alla conferma</strong>
                </span><span class="sxs-lookup"><span data-stu-id="87bc4-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="87bc4-112">Fatturazione di un anticipo o di un acconto</span><span class="sxs-lookup"><span data-stu-id="87bc4-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-113">Un valore effettivo della vendita fatturata di tipo <strong>Acconto</strong> viene creato per l'importo dell'anticipo o dell'acconto.</span><span class="sxs-lookup"><span data-stu-id="87bc4-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-114">Un valore effettivo delle vendite non fatturate con un importo negativo dell'acconto o dell'anticipo da utilizzare per la riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="87bc4-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="87bc4-115">Dopo aver riconciliato completamente un acconto o un anticipo su una fattura.</span><span class="sxs-lookup"><span data-stu-id="87bc4-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-116">Uno storno delle vendite non fatturate dell'acconto o dell'anticipo creato per la riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="87bc4-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="87bc4-117">Questo importo è positivo perché ha lo scopo di annullare il negativo che è stato creato al momento della fatturazione dell'acconto o dell'anticipo.</span><span class="sxs-lookup"><span data-stu-id="87bc4-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-118">Un valore effettivo delle vendite fatturate per l'importo della fattura.</span><span class="sxs-lookup"><span data-stu-id="87bc4-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="87bc4-119">Dopo aver riconciliato parzialmente un acconto o un anticipo su una fattura.</span><span class="sxs-lookup"><span data-stu-id="87bc4-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-120">Uno storno delle vendite non fatturate dell'acconto o dell'anticipo creato per la riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="87bc4-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="87bc4-121">Questo importo è positivo perché ha lo scopo di annullare il negativo che è stato creato al momento della fatturazione dell'acconto o dell'anticipo.</span><span class="sxs-lookup"><span data-stu-id="87bc4-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-122">Un valore effettivo delle vendite fatturate per l'importo della fattura.</span><span class="sxs-lookup"><span data-stu-id="87bc4-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-123">Un valore effettivo negativo delle vendite non fatturate di un importo dell'acconto o dell'anticipo rimanente da utilizzare per la riconciliazione nelle future fatture.</span><span class="sxs-lookup"><span data-stu-id="87bc4-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="87bc4-124">Fatturazione di una transazione di tempo senza modifiche sulla fattura in bozza.</span><span class="sxs-lookup"><span data-stu-id="87bc4-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-125">Uno storno delle vendite non fatturate per le ore e l'importo nell'approvazione del tempo originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-126">Un valore effettivo delle vendite fatturate per le ore e l'importo sull'approvazione del tempo originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="87bc4-127">La fatturazione di una transazione temporale modificata per ridurre la quantità.</span><span class="sxs-lookup"><span data-stu-id="87bc4-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-128">Uno storno delle vendite non fatturate per le ore e l'importo nell'approvazione del tempo originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-129">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="87bc4-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-130">Un nuovo valore effettivo delle vendite non fatturate che non è addebitabile per l'importo e le ore rimanenti dopo la deduzione dei dati corretti nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite e un valore effettivo equivalente delle vendite fatturate.</span><span class="sxs-lookup"><span data-stu-id="87bc4-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="87bc4-131">La fatturazione di una transazione temporale modificata per aumentare la quantità.</span><span class="sxs-lookup"><span data-stu-id="87bc4-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-132">Uno storno delle vendite non fatturate per le ore e l'importo nell'approvazione del tempo originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-133">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="87bc4-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="87bc4-134">Fatturazione di una transazione di spesa senza modifiche sulla fattura in bozza.</span><span class="sxs-lookup"><span data-stu-id="87bc4-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-135">Uno storno delle vendite non fatturate per la quantità e l'importo sull'approvazione della spesa originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-136">Un valore effettivo delle vendite fatturate per la quantità e l'importo sull'approvazione della spesa originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="87bc4-137">La fatturazione di una transazione di spesa modificata per ridurre la quantità.</span><span class="sxs-lookup"><span data-stu-id="87bc4-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-138">Uno storno delle vendite non fatturate per la quantità e l'importo sull'approvazione della spesa originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-139">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="87bc4-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-140">Un nuovo valore effettivo delle vendite non fatturate non addebitabile per la quantità e l'importo rimanenti dopo la deduzione delle cifre corrette nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="87bc4-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="87bc4-141">La fatturazione di una transazione di spesa modificata per aumentare la quantità.</span><span class="sxs-lookup"><span data-stu-id="87bc4-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-142">Uno storno delle vendite non fatturate per la quantità e l'importo sull'approvazione della spesa originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-143">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="87bc4-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="87bc4-144">Fatturazione di una transazione materiale senza modifiche nella bozza di fattura.</span><span class="sxs-lookup"><span data-stu-id="87bc4-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-145">Uno storno vendite non fatturate per la quantità e l'importo nell'approvazione dell'utilizzo di materiale originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-146">Un valore effettivo delle vendite fatturate per la quantità e l'importo nell'approvazione dell'utilizzo di materiale originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="87bc4-147">Fatturazione di una transazione materiale modificata per ridurre la quantità.</span><span class="sxs-lookup"><span data-stu-id="87bc4-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-148">Uno storno vendite non fatturate per la quantità e l'importo nell'approvazione del tempo originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-149">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="87bc4-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-150">Un nuovo valore effettivo delle vendite non fatturate non addebitabile per la quantità e l'importo rimanenti dopo la deduzione delle cifre corrette nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="87bc4-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="87bc4-151">Fatturazione di una transazione materiale modificata per aumentare la quantità.</span><span class="sxs-lookup"><span data-stu-id="87bc4-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-152">Uno storno vendite non fatturate per la quantità e l'importo nell'approvazione dell'utilizzo di materiale originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-153">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nel dettaglio della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="87bc4-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="87bc4-154">Fatturazione di una commissione.</span><span class="sxs-lookup"><span data-stu-id="87bc4-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-155">Uno storno delle vendite non fatturate per l'importo della commissione nella riga di registrazione originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-156">Un valore effettivo delle vendite fatturate per la quantità e l'importo nella riga di registrazione della commissione originale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="87bc4-157">La fatturazione di un passaggio fondamentale.</span><span class="sxs-lookup"><span data-stu-id="87bc4-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="87bc4-158">Un valore effettivo delle vendite fatturate per l'importo nel passaggio fondamentale della voce di contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="87bc4-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
