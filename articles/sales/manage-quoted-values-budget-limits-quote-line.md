---
title: Panoramica delle righe di offerta di progetto
description: Questo argomento fornisce informazioni sull'utilizzo di righe di offerta di progetto per il lavoro del progetto.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 72feb791e48c9bacd4a0b7ea5cd77ddc8eb5f514
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996301"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="a358d-103">Panoramica delle righe di offerta di progetto</span><span class="sxs-lookup"><span data-stu-id="a358d-103">Project quote lines overview</span></span>

<span data-ttu-id="a358d-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="a358d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a358d-105">Le righe di offerta basate su progetto sono progettate per aiutare a stimare il lavoro del progetto per un impegno.</span><span class="sxs-lookup"><span data-stu-id="a358d-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="a358d-106">La struttura di una riga di offerta basata su progetto è estesa per le stime di progetto con i seguenti concetti:</span><span class="sxs-lookup"><span data-stu-id="a358d-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="a358d-107">Metodo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="a358d-107">Billing Method</span></span>
- <span data-ttu-id="a358d-108">Mapping del progetto</span><span class="sxs-lookup"><span data-stu-id="a358d-108">Project Mapping</span></span>
- <span data-ttu-id="a358d-109">Classi di transazione incluse</span><span class="sxs-lookup"><span data-stu-id="a358d-109">Included Transaction classes</span></span>
- <span data-ttu-id="a358d-110">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="a358d-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="a358d-111">Impostazione dell'esigibilità</span><span class="sxs-lookup"><span data-stu-id="a358d-111">Chargeability setup</span></span>
- <span data-ttu-id="a358d-112">Stima che utilizza i dettagli della riga di offerta</span><span class="sxs-lookup"><span data-stu-id="a358d-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="a358d-113">Clienti riga di offerta</span><span class="sxs-lookup"><span data-stu-id="a358d-113">Quote line Customers</span></span>

<span data-ttu-id="a358d-114">La tabella seguente fornisce informazioni sui campi nella scheda **Generale** della riga di offerta basata su progetto.</span><span class="sxs-lookup"><span data-stu-id="a358d-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="a358d-115">Questi campi aiutano a creare le basi per una stima dettagliata e completa del lavoro del progetto.</span><span class="sxs-lookup"><span data-stu-id="a358d-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="a358d-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="a358d-116">**Field**</span></span> | <span data-ttu-id="a358d-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a358d-117">**Description**</span></span> | <span data-ttu-id="a358d-118">**Impatto downstream**</span><span class="sxs-lookup"><span data-stu-id="a358d-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a358d-119">Nome</span><span class="sxs-lookup"><span data-stu-id="a358d-119">Name</span></span> | <span data-ttu-id="a358d-120">Il nome della riga dell'offerta che dovrebbe aiutarti a identificare il componente discreto dell'offerta che viene stimata.</span><span class="sxs-lookup"><span data-stu-id="a358d-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="a358d-121">Copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-122">Metodo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="a358d-122">Billing Method</span></span> | <span data-ttu-id="a358d-123">In un'offerta creata da un'opportunità, questo valore viene copiato dal campo corrispondente nella riga dell'opportunità.</span><span class="sxs-lookup"><span data-stu-id="a358d-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="a358d-124">Questo campo include i due principali modelli di contratto supportati da Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="a358d-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="a358d-125">- Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="a358d-125">- Fixed price</span></span></br><span data-ttu-id="a358d-126">- Tempistica e materiali.</span><span class="sxs-lookup"><span data-stu-id="a358d-126">- Time and material.</span></span>| <span data-ttu-id="a358d-127">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-128">Project</span><span class="sxs-lookup"><span data-stu-id="a358d-128">Project</span></span> | <span data-ttu-id="a358d-129">Utilizza questo campo facoltativo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno.</span><span class="sxs-lookup"><span data-stu-id="a358d-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="a358d-130">Quando un progetto viene mappato a una riga dell'offerta, viene semplificata l'impostazione delle attività addebitabili e anche l'inserimento di una stima basata sul progetto nella riga dell'offerta come dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="a358d-131">Quando un progetto non è mappato a una riga di offerta basata su progetto, la stima deve essere creata manualmente creando ogni dettaglio della riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="a358d-132">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-133">Includi tempo</span><span class="sxs-lookup"><span data-stu-id="a358d-133">Include Time</span></span> | <span data-ttu-id="a358d-134">Un contrassegno **Sì**/**No** indica se le transazioni temporali o i costi di manodopera sul progetto selezionato saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a358d-135">Un valore **No** indica che le transazioni temporali o i costi di manodopera non saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a358d-136">Un valore **Sì** indica che le transazioni temporali o i costi di manodopera saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a358d-137">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-138">Includi spesa</span><span class="sxs-lookup"><span data-stu-id="a358d-138">Include Expense</span></span> | <span data-ttu-id="a358d-139">Un contrassegno **Sì**/**No** indica se i costi di spesa sul progetto selezionato saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a358d-140">Un valore **No** indica che i costi di spesa non saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a358d-141">Un valore **Sì** indica che i costi di spesa saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a358d-142">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-143">Includi commissione</span><span class="sxs-lookup"><span data-stu-id="a358d-143">Include Fee</span></span> | <span data-ttu-id="a358d-144">Un contrassegno **Sì**/**No** indica se le commissioni sul progetto selezionato saranno incluse nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a358d-145">Un valore **No** indica che le commissioni non saranno incluse nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a358d-146">Un valore **Sì** indica che le commissioni saranno incluse nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a358d-147">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-148">Importo offerto</span><span class="sxs-lookup"><span data-stu-id="a358d-148">Quoted Amount</span></span> | <span data-ttu-id="a358d-149">Questo è l'importo che verrà offerto al cliente per tutto il lavoro previsto in questa riga di offerta basata su progetto.</span><span class="sxs-lookup"><span data-stu-id="a358d-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="a358d-150">In un'offerta creata da un'opportunità, questo valore viene copiato dal campo **Budget cliente** nella riga dell'opportunità.</span><span class="sxs-lookup"><span data-stu-id="a358d-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="a358d-151">Quando la riga di offerta basata su progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="a358d-152">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-153">Imposta stimata</span><span class="sxs-lookup"><span data-stu-id="a358d-153">Estimated Tax</span></span> | <span data-ttu-id="a358d-154">Questo è un campo modificabile che consente all'utente di aggiungere l'importo delle imposte stimate nella riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="a358d-155">Quando una riga di offerta basata su progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="a358d-156">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-157">Importo offerto al netto delle imposte</span><span class="sxs-lookup"><span data-stu-id="a358d-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="a358d-158">Questo campo rappresenta l'importo della riga dell'offerta al netto delle imposte ed è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a358d-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="a358d-159">L'importo in questo campo viene calcolato come *Importo offerto + imposte*.</span><span class="sxs-lookup"><span data-stu-id="a358d-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="a358d-160">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-161">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="a358d-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="a358d-162">Questo campo è modificabile ed è disponibile solo per le righe dell'offerta basate su progetto che hanno un metodo di fatturazione **Tempistica e materiali**.</span><span class="sxs-lookup"><span data-stu-id="a358d-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="a358d-163">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a358d-164">Budget cliente</span><span class="sxs-lookup"><span data-stu-id="a358d-164">Customer Budget</span></span> | <span data-ttu-id="a358d-165">Questo campo è modificabile e viene copiato dal campo corrispondente nella riga dell'opportunità se l'offerta è stata creata da un'opportunità.</span><span class="sxs-lookup"><span data-stu-id="a358d-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="a358d-166">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="a358d-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="a358d-167">Regole di convalida per i campi nella scheda Generale delle righe di offerta basate su progetto</span><span class="sxs-lookup"><span data-stu-id="a358d-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="a358d-168">**Regola 1**: una determinata classe di transazione sul progetto selezionato può essere inclusa solo in una riga di offerta basata su progetto di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="a358d-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="a358d-169">**Regola 2**: se un'opportunità ha più offerte, possono esserci righe di offerta da offerte diverse che fanno tutte riferimento allo stesso progetto e includono la stessa classe di transazione.</span><span class="sxs-lookup"><span data-stu-id="a358d-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="a358d-170">**Regola 3**: se le offerte non appartengono alla stessa opportunità, non possono includere lo stesso progetto e la stessa classe di transazione.</span><span class="sxs-lookup"><span data-stu-id="a358d-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="a358d-171">
                    <strong>Opportunità</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="a358d-172">
                    <strong>Offerta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a358d-173">
                    <strong>Riga di offerta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a358d-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a358d-175">
                    <strong>Includi tempistica</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a358d-176">
                    <strong>Includi spesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a358d-177">
                    <strong>Includi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="a358d-178">
                    <strong>Commissione</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="a358d-179">
                    <strong>Valido/Non valido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="a358d-180">
                    <strong>Motivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a358d-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-181">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-182">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-183">QL1</span><span class="sxs-lookup"><span data-stu-id="a358d-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-184">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-185">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-186">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-187">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a358d-188">Non valido</span><span class="sxs-lookup"><span data-stu-id="a358d-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a358d-189">Violazione della regola n. 1.</span><span class="sxs-lookup"><span data-stu-id="a358d-189">Violation of Rule #1.</span></span> <span data-ttu-id="a358d-190">Tempistica, spesa e commissioni sul progetto P1 sono inclusi in entrambe le righe dell'offerta, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="a358d-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-191">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-192">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-193">QL2</span><span class="sxs-lookup"><span data-stu-id="a358d-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-194">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-195">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-196">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-197">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-198">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-199">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-200">QL1</span><span class="sxs-lookup"><span data-stu-id="a358d-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-201">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-202">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-203">No</span><span class="sxs-lookup"><span data-stu-id="a358d-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-204">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a358d-205">Non valido</span><span class="sxs-lookup"><span data-stu-id="a358d-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a358d-206">Violazione della regola n. 1.</span><span class="sxs-lookup"><span data-stu-id="a358d-206">Violation of Rule #1.</span></span> <span data-ttu-id="a358d-207">Tempistica e commissioni sul progetto P1 sono incluse in entrambe le righe dell'offerta, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="a358d-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-208">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-209">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-210">QL2</span><span class="sxs-lookup"><span data-stu-id="a358d-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-211">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-212">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-213">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-214">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-215">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-216">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-217">QL1</span><span class="sxs-lookup"><span data-stu-id="a358d-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-218">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-219">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-220">No</span><span class="sxs-lookup"><span data-stu-id="a358d-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-221">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a358d-222">Valido</span><span class="sxs-lookup"><span data-stu-id="a358d-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="a358d-223">Tempistica e commissioni sul progetto P1 sono incluse in QL1.</span><span class="sxs-lookup"><span data-stu-id="a358d-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="a358d-224">La spesa sul progetto P1 è inclusa in QL2.</span><span class="sxs-lookup"><span data-stu-id="a358d-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="a358d-225">Non c'è sovrapposizione tra gli elementi inclusi in ogni riga dell'offerta quindi è valido.</span><span class="sxs-lookup"><span data-stu-id="a358d-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-226">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-227">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-228">QL2</span><span class="sxs-lookup"><span data-stu-id="a358d-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-229">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-230">No</span><span class="sxs-lookup"><span data-stu-id="a358d-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-231">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-232">No</span><span class="sxs-lookup"><span data-stu-id="a358d-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-233">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-234">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-235">QL1</span><span class="sxs-lookup"><span data-stu-id="a358d-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-236">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-237">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-238">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-239">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a358d-240">Non valido</span><span class="sxs-lookup"><span data-stu-id="a358d-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a358d-241">Violazione della regola n. 1 precedente</span><span class="sxs-lookup"><span data-stu-id="a358d-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="a358d-242">Q1 include tempistica, spese e commissioni per l'intero progetto P1.</span><span class="sxs-lookup"><span data-stu-id="a358d-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a358d-243">QL2 include tempistica, spese e commissioni per l'intero progetto P1 e si sovrappone a quanto incluso in Q1.</span><span class="sxs-lookup"><span data-stu-id="a358d-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-244">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-245">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-246">QL2</span><span class="sxs-lookup"><span data-stu-id="a358d-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-247">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-248">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-249">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-250">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-251">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-252">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-253">QL1</span><span class="sxs-lookup"><span data-stu-id="a358d-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-254">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-255">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-256">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-257">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="a358d-258">Valido</span><span class="sxs-lookup"><span data-stu-id="a358d-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a358d-259">In base alla regola n. 2, Q1 e Q2 sono due offerte della stessa opportunità, quindi possono entrambe eseguire una stima per gli stessi componenti di un progetto.</span><span class="sxs-lookup"><span data-stu-id="a358d-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-260">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-261">Secondo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-262">QL1 su Q2</span><span class="sxs-lookup"><span data-stu-id="a358d-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-263">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-264">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-265">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-266">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-267">O1</span><span class="sxs-lookup"><span data-stu-id="a358d-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-268">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-269">QL1</span><span class="sxs-lookup"><span data-stu-id="a358d-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-270">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-271">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-272">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-273">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="a358d-274">Valido</span><span class="sxs-lookup"><span data-stu-id="a358d-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a358d-275">In base alla regola n. 3, Q1 e Q2 sono due offerte di opportunità diverse, quindi non possono eseguire una stima per gli stessi componenti dello stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="a358d-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a358d-276">O2</span><span class="sxs-lookup"><span data-stu-id="a358d-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a358d-277">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="a358d-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-278">QL1</span><span class="sxs-lookup"><span data-stu-id="a358d-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-279">P1</span><span class="sxs-lookup"><span data-stu-id="a358d-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-280">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a358d-281">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a358d-282">Sì</span><span class="sxs-lookup"><span data-stu-id="a358d-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="a358d-283">Non valido</span><span class="sxs-lookup"><span data-stu-id="a358d-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
