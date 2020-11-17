---
title: Confermare una fattura proforma
description: Questo argomento fornisce informazioni sulla conferma di una fattura proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128108"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="70a78-103">Confermare una fattura proforma</span><span class="sxs-lookup"><span data-stu-id="70a78-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="70a78-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="70a78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="70a78-105">Dopo la conferma di una fattura proforma, lo stato della fattura di progetto viene aggiornato su **Confermato**.</span><span class="sxs-lookup"><span data-stu-id="70a78-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="70a78-106">Quando una fattura viene confermata, diventa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="70a78-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="70a78-107">In futuro, la fattura può essere corretta solo se sono presenti correzioni o accrediti avviati dal cliente o se è contrassegnata come pagata.</span><span class="sxs-lookup"><span data-stu-id="70a78-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="70a78-108">Nella tabella seguente sono elencati i valori effettivi creati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="70a78-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="70a78-109">Questi valori effettivi vengono creati quando vengono eseguite determinate operazioni sulla bozza della fattura di progetto prima che venga confermata.</span><span class="sxs-lookup"><span data-stu-id="70a78-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="70a78-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="70a78-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="70a78-111">
                    <strong>Valori effettivi creati alla conferma</strong>
                </span><span class="sxs-lookup"><span data-stu-id="70a78-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="70a78-112">Fatturazione di una transazione di tempo senza modifiche sulla fattura in bozza.</span><span class="sxs-lookup"><span data-stu-id="70a78-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-113">Uno storno delle vendite non fatturate per le ore e l'importo nell'approvazione del tempo originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-114">Un valore effettivo delle vendite fatturate per le ore e l'importo sull'approvazione del tempo originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="70a78-115">La fatturazione di una transazione temporale modificata per ridurre la quantità.</span><span class="sxs-lookup"><span data-stu-id="70a78-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-116">Uno storno delle vendite non fatturate per le ore e l'importo nell'approvazione del tempo originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-117">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="70a78-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-118">Un nuovo valore effettivo delle vendite non fatturate non addebitabile per le ore e l'importo rimanenti dopo la deduzione delle cifre corrette nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="70a78-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="70a78-119">La fatturazione di una transazione temporale modificata per aumentare la quantità.</span><span class="sxs-lookup"><span data-stu-id="70a78-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-120">Uno storno delle vendite non fatturate per le ore e l'importo nell'approvazione del tempo originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-121">Un nuovo valore effettivo delle vendite non fatturate addebitabile per le ore e l'importo nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="70a78-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="70a78-122">Fatturazione di una transazione di spesa senza modifiche sulla fattura in bozza.</span><span class="sxs-lookup"><span data-stu-id="70a78-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-123">Uno storno delle vendite non fatturate per la quantità e l'importo sull'approvazione della spesa originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-124">Un valore effettivo delle vendite fatturate per la quantità e l'importo sull'approvazione della spesa originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="70a78-125">La fatturazione di una transazione di spesa modificata per ridurre la quantità.</span><span class="sxs-lookup"><span data-stu-id="70a78-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-126">Uno storno delle vendite non fatturate per la quantità e l'importo sull'approvazione della spesa originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-127">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="70a78-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-128">Un nuovo valore effettivo delle vendite non fatturate non addebitabile per la quantità e l'importo rimanenti dopo la deduzione delle cifre corrette nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="70a78-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="70a78-129">La fatturazione di una transazione di spesa modificata per aumentare la quantità.</span><span class="sxs-lookup"><span data-stu-id="70a78-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-130">Uno storno delle vendite non fatturate per la quantità e l'importo sull'approvazione della spesa originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-131">Un nuovo valore effettivo delle vendite non fatturate addebitabile per la quantità e l'importo nei dettagli della riga fattura modificata, uno storno del valore effettivo delle vendite non fatturate e un valore effettivo delle vendite fatturate equivalente.</span><span class="sxs-lookup"><span data-stu-id="70a78-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="70a78-132">Fatturazione di una commissione.</span><span class="sxs-lookup"><span data-stu-id="70a78-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-133">Uno storno delle vendite non fatturate per l'importo della commissione nella riga di registrazione originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-134">Un valore effettivo delle vendite fatturate per la quantità e l'importo nella riga di registrazione della commissione originale.</span><span class="sxs-lookup"><span data-stu-id="70a78-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="70a78-135">La fatturazione di un passaggio fondamentale.</span><span class="sxs-lookup"><span data-stu-id="70a78-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="70a78-136">Un valore effettivo delle vendite fatturate per l'importo nel passaggio fondamentale della voce di contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="70a78-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
