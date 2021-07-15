---
title: Panoramica delle righe di offerta basate su progetto
description: Questo argomento fornisce informazioni sull'utilizzo delle righe di offerta basate su progetto per il lavoro del progetto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369876"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="1a887-103">Panoramica delle righe di offerta basate su progetto</span><span class="sxs-lookup"><span data-stu-id="1a887-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="1a887-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="1a887-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1a887-105">Le righe di offerta basate su progetto sono progettate per aiutare a stimare il lavoro del progetto per un impegno.</span><span class="sxs-lookup"><span data-stu-id="1a887-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="1a887-106">La struttura di una riga di offerta basata su progetto è estesa per le stime di progetto con i seguenti concetti:</span><span class="sxs-lookup"><span data-stu-id="1a887-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="1a887-107">Metodo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="1a887-107">Billing Method</span></span>
- <span data-ttu-id="1a887-108">Mapping di progetti e attività</span><span class="sxs-lookup"><span data-stu-id="1a887-108">Project and Task Mapping</span></span>
- <span data-ttu-id="1a887-109">Classi di transazione incluse</span><span class="sxs-lookup"><span data-stu-id="1a887-109">Included Transaction classes</span></span>
- <span data-ttu-id="1a887-110">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="1a887-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="1a887-111">Impostazione dell'esigibilità</span><span class="sxs-lookup"><span data-stu-id="1a887-111">Chargeability setup</span></span>
- <span data-ttu-id="1a887-112">Stima che utilizza i dettagli della riga di offerta</span><span class="sxs-lookup"><span data-stu-id="1a887-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="1a887-113">Clienti riga di offerta</span><span class="sxs-lookup"><span data-stu-id="1a887-113">Quote line Customers</span></span>

<span data-ttu-id="1a887-114">La tabella seguente fornisce informazioni sui campi nella scheda **Generale** della riga di offerta basata su progetto.</span><span class="sxs-lookup"><span data-stu-id="1a887-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="1a887-115">Questi campi aiutano a creare le basi per una stima dettagliata e completa del lavoro del progetto.</span><span class="sxs-lookup"><span data-stu-id="1a887-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="1a887-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="1a887-116">**Field**</span></span> | <span data-ttu-id="1a887-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1a887-117">**Description**</span></span> | <span data-ttu-id="1a887-118">**Impatto downstream**</span><span class="sxs-lookup"><span data-stu-id="1a887-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1a887-119">Nome</span><span class="sxs-lookup"><span data-stu-id="1a887-119">Name</span></span> | <span data-ttu-id="1a887-120">Il nome della riga di offerta che ti consente di identificare la componente discreta dell'offerta che viene stimata.</span><span class="sxs-lookup"><span data-stu-id="1a887-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="1a887-121">Copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-122">Metodo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="1a887-122">Billing Method</span></span> | <span data-ttu-id="1a887-123">In un'offerta creata da un'opportunità, questo valore viene copiato dal campo corrispondente nella riga dell'opportunità.</span><span class="sxs-lookup"><span data-stu-id="1a887-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="1a887-124">Questo campo include i due principali modelli di contratto supportati da Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="1a887-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="1a887-125">- Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="1a887-125">- Fixed price</span></span></br><span data-ttu-id="1a887-126">- Tempistica e materiali.</span><span class="sxs-lookup"><span data-stu-id="1a887-126">- Time and material.</span></span>| <span data-ttu-id="1a887-127">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-128">Project</span><span class="sxs-lookup"><span data-stu-id="1a887-128">Project</span></span> | <span data-ttu-id="1a887-129">Utilizza questo campo facoltativo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno.</span><span class="sxs-lookup"><span data-stu-id="1a887-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="1a887-130">Quando un progetto viene mappato a una riga dell'offerta, viene semplificata l'impostazione delle attività addebitabili e anche l'inserimento di una stima basata sul progetto nella riga dell'offerta come dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="1a887-131">Quando un progetto non è mappato a una riga di offerta basata su progetto, la stima deve essere creata manualmente creando ogni dettaglio della riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="1a887-132">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="1a887-133">Attività incluse</span><span class="sxs-lookup"><span data-stu-id="1a887-133">Included Tasks</span></span> | <span data-ttu-id="1a887-134">Indica se questa riga dell'offerta viene utilizzata per tutte o alcune delle attività di progetto per il progetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="1a887-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="1a887-135">Di seguito sono riportati i valori possibili di questo campo:</span><span class="sxs-lookup"><span data-stu-id="1a887-135">This field has the following possible values:</span></span></br><span data-ttu-id="1a887-136">- Tutte le attività di progetto</span><span class="sxs-lookup"><span data-stu-id="1a887-136">- All project tasks</span></span></br><span data-ttu-id="1a887-137">- Solo le attività di progetto selezionate</span><span class="sxs-lookup"><span data-stu-id="1a887-137">- Selected project tasks only</span></span></br><span data-ttu-id="1a887-138">Un valore vuoto in questo campo equivale all'opzione **Tutte le attività di progetto**.</span><span class="sxs-lookup"><span data-stu-id="1a887-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="1a887-139">Quando è selezionata l'opzione **Solo le attività di progetto selezionate** nella pagina del progetto, la scheda **Configurazione fatturazione attività** consente di selezionare attività specifiche per associarle a questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="1a887-140">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-141">Includi tempo</span><span class="sxs-lookup"><span data-stu-id="1a887-141">Include Time</span></span> | <span data-ttu-id="1a887-142">Un valore **Sì**/**No** indica se le transazioni temporali o i costi di manodopera nel progetto selezionato saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a887-143">Un valore **No** indica che le transazioni temporali o i costi di manodopera non saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a887-144">Un valore **Sì** indica che le transazioni temporali o i costi di manodopera saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a887-145">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-146">Includi spesa</span><span class="sxs-lookup"><span data-stu-id="1a887-146">Include Expense</span></span> | <span data-ttu-id="1a887-147">Un valore **Sì**/**No** indica se i costi della spesa nel progetto selezionato saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a887-148">Un valore **No** indica che i costi di spesa non saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a887-149">Un valore **Sì** indica che i costi di spesa saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a887-150">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-151">Includi materiale</span><span class="sxs-lookup"><span data-stu-id="1a887-151">Include Material</span></span> | <span data-ttu-id="1a887-152">Un valore **Sì**/**No** indica se i costi materiale nel progetto selezionato saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a887-153">Un valore **No** indica che i costi materiale non saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a887-154">Un valore **Sì** indica che i costi materiale non saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a887-155">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-156">Includi commissione</span><span class="sxs-lookup"><span data-stu-id="1a887-156">Include Fee</span></span> | <span data-ttu-id="1a887-157">Un valore **Sì**/**No** indica se le commissioni nel progetto selezionato saranno incluse nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a887-158">Un valore **No** indica che le commissioni non saranno incluse nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a887-159">Un valore **Sì** indica che le commissioni saranno incluse nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a887-160">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-161">Importo offerto</span><span class="sxs-lookup"><span data-stu-id="1a887-161">Quoted Amount</span></span> | <span data-ttu-id="1a887-162">Si tratta dell'importo dell'offerta al cliente per tutto il lavoro previsto in questa riga di offerta basata su progetto.</span><span class="sxs-lookup"><span data-stu-id="1a887-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="1a887-163">In un'offerta creata da un'opportunità, questo valore viene copiato dal campo **Budget cliente** nella riga dell'opportunità.</span><span class="sxs-lookup"><span data-stu-id="1a887-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="1a887-164">Quando la riga di offerta basata su progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="1a887-165">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-166">Imposta stimata</span><span class="sxs-lookup"><span data-stu-id="1a887-166">Estimated Tax</span></span> | <span data-ttu-id="1a887-167">Questo è un campo modificabile che consente all'utente di aggiungere l'importo delle imposte stimate nella riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="1a887-168">Quando una riga di offerta basata su progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="1a887-169">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-170">Importo offerto al netto delle imposte</span><span class="sxs-lookup"><span data-stu-id="1a887-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="1a887-171">Questo campo rappresenta l'importo della riga dell'offerta al netto delle imposte ed è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1a887-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="1a887-172">L'importo in questo campo viene calcolato come *Importo offerto + imposte*.</span><span class="sxs-lookup"><span data-stu-id="1a887-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="1a887-173">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-174">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="1a887-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="1a887-175">Questo campo è modificabile ed è disponibile solo per le righe dell'offerta basate su progetto che hanno un metodo di fatturazione **Tempistica e materiali**.</span><span class="sxs-lookup"><span data-stu-id="1a887-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="1a887-176">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a887-177">Budget cliente</span><span class="sxs-lookup"><span data-stu-id="1a887-177">Customer Budget</span></span> | <span data-ttu-id="1a887-178">Questo campo è modificabile e viene copiato dal campo corrispondente nella riga dell'opportunità se l'offerta è stata creata da un'opportunità.</span><span class="sxs-lookup"><span data-stu-id="1a887-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="1a887-179">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="1a887-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="1a887-180">Regole di convalida per i campi nella scheda Generale delle righe di offerta basate su progetto</span><span class="sxs-lookup"><span data-stu-id="1a887-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="1a887-181">**Regola 1**: se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto**, un progetto è incluso nella riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="1a887-182">**Regola 2**: se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto**, un progetto e una determinata classe di transazione possono essere inclusi solo in una riga di offerta basata su progetto di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="1a887-183">**Regola 3**: se il campo **Attività incluse** è vuoto o se è impostato su **Solo le attività di progetto selezionate**, un progetto e una determinata classe di transazione possono essere inclusi in più righe di offerta basata su progetto di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="1a887-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="1a887-184">**Regola 4**: se un'opportunità ha più offerte, possono esserci righe di offerta da offerte diverse che fanno tutte riferimento allo stesso progetto e includono la stessa classe di transazione.</span><span class="sxs-lookup"><span data-stu-id="1a887-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="1a887-185">**Regola 5**: se le offerte non appartengono alla stessa opportunità, non possono includere lo stesso progetto e la stessa classe di transazione.</span><span class="sxs-lookup"><span data-stu-id="1a887-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="1a887-186">
                    <strong>Opportunità</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="1a887-187">
                    <strong>Offerta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="1a887-188">
                    <strong>Riga di offerta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="1a887-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="1a887-190">
                    <strong>Attività incluse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="1a887-191">
                    <strong>Includi tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="1a887-192">
                    <strong>Includi spesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="1a887-193">
                    <strong>Includi materiale</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="1a887-194">
                    <strong>Includi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="1a887-195">
                    <strong>Commissione</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="1a887-196">
                    <strong>Valido/Non valido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="1a887-197">
                    <strong>Motivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a887-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-198">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-199">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-200">QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-201">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-202">Vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-203">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-204">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-205">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-206">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-207">Non valido</span><span class="sxs-lookup"><span data-stu-id="1a887-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-208">Violazione della regola n. 2.</span><span class="sxs-lookup"><span data-stu-id="1a887-208">Violation of Rule #2.</span></span> <span data-ttu-id="1a887-209">Tempo, spesa e commissioni nel progetto P1 sono incluse nelle righe di offerta QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="1a887-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-210">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-211">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-212">QL2</span><span class="sxs-lookup"><span data-stu-id="1a887-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-213">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-214">Vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-215">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-216">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-217">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-218">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-219">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-220">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-221">QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-222">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-223">Vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-224">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-225">No</span><span class="sxs-lookup"><span data-stu-id="1a887-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-226">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-227">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-228">Non valido</span><span class="sxs-lookup"><span data-stu-id="1a887-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-229">Violazione della regola n. 2.</span><span class="sxs-lookup"><span data-stu-id="1a887-229">Violation of Rule #2.</span></span> <span data-ttu-id="1a887-230">Tempo, materiale e commissioni nel progetto P1 sono incluse nelle righe di offerta QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="1a887-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-231">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-232">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-233">QL2</span><span class="sxs-lookup"><span data-stu-id="1a887-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-234">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-235">Vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-236">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-237">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-238">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-239">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-240">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-241">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-242">QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-243">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-244">Vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-245">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-246">No</span><span class="sxs-lookup"><span data-stu-id="1a887-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-247">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-248">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-249">Valido</span><span class="sxs-lookup"><span data-stu-id="1a887-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-250">Tempo, materiale e commissioni nel progetto P1 sono incluse in QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="1a887-251">La spesa nel progetto P1 è inclusa in QL2</span><span class="sxs-lookup"><span data-stu-id="1a887-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="1a887-252">Nessuna sovrapposizione in ciò che viene incluso in ogni riga di offerta e quindi valido.</span><span class="sxs-lookup"><span data-stu-id="1a887-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-253">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-254">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-255">QL2</span><span class="sxs-lookup"><span data-stu-id="1a887-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-256">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-257">Vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-258">No</span><span class="sxs-lookup"><span data-stu-id="1a887-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-259">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-260">No</span><span class="sxs-lookup"><span data-stu-id="1a887-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-261">No</span><span class="sxs-lookup"><span data-stu-id="1a887-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-262">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-263">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-264">QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-265">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-266">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="1a887-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-267">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-268">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-269">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-270">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-271">Non valido</span><span class="sxs-lookup"><span data-stu-id="1a887-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-272">Violazione della regola n. 2</span><span class="sxs-lookup"><span data-stu-id="1a887-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="1a887-273">Q1 include tempo, materiale, spese e commissioni in un sottoinsieme di attività nel progetto P1</span><span class="sxs-lookup"><span data-stu-id="1a887-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="1a887-274">QL2 include tempo, spese e commissioni per l'intero progetto P1 e quindi si sovrappone a quanto incluso in Q1.</span><span class="sxs-lookup"><span data-stu-id="1a887-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-275">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-276">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-277">QL2</span><span class="sxs-lookup"><span data-stu-id="1a887-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-278">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-279">Vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-280">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-281">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-282">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-283">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-284">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-285">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-286">QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-287">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-288">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="1a887-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-289">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-290">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-291">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-292">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-293">Valido</span><span class="sxs-lookup"><span data-stu-id="1a887-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-294">Per la regola n. 3</span><span class="sxs-lookup"><span data-stu-id="1a887-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="1a887-295">Q1 include tempo, materiale, spese e commissioni in un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="1a887-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1a887-296">QL2 include tempo, materiale, spese e commissioni per un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="1a887-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1a887-297">L'unica convalida aggiuntiva riguarda il sottoinsieme di attività in QL1 che è diverso dal sottoinsieme di attività in QL2 per garantire che non vi siano sovrapposizioni.</span><span class="sxs-lookup"><span data-stu-id="1a887-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="1a887-298">Ciò viene eseguito dal sistema quando vengono associate le attività.</span><span class="sxs-lookup"><span data-stu-id="1a887-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-299">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-300">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-301">QL2</span><span class="sxs-lookup"><span data-stu-id="1a887-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-302">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-303">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="1a887-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-304">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-305">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-306">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-307">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-308">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-309">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-310">QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-311">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-312">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-313">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-314">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-315">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-316">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-317">Valido</span><span class="sxs-lookup"><span data-stu-id="1a887-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-318">Secondo la regola n. 5, Q1 e Q2 sono due offerte della stessa opportunità, quindi possono entrambe stimare gli stessi componenti di un progetto.</span><span class="sxs-lookup"><span data-stu-id="1a887-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-319">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-320">Secondo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-321">QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-322">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-323">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-324">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-325">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-326">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-327">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-328">O1</span><span class="sxs-lookup"><span data-stu-id="1a887-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-329">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-330">QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-331">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-332">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-333">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-334">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-335">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-336">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-337">Non valido</span><span class="sxs-lookup"><span data-stu-id="1a887-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a887-338">Secondo la regola n. 4, Q1 e Q2 sono due offerte di differenti opportunità, quindi non possono stimare gli stessi componenti di un stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="1a887-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="1a887-339">O2</span><span class="sxs-lookup"><span data-stu-id="1a887-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="1a887-340">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="1a887-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="1a887-341">QL1</span><span class="sxs-lookup"><span data-stu-id="1a887-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-342">P1</span><span class="sxs-lookup"><span data-stu-id="1a887-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="1a887-343">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="1a887-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="1a887-344">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="1a887-345">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1a887-346">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a887-347">Sì</span><span class="sxs-lookup"><span data-stu-id="1a887-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
