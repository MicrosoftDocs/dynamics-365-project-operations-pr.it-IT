---
title: Panoramica delle righe di offerta basate su progetto
description: Questo argomento fornisce informazioni sull'utilizzo delle righe di offerta basate su progetto per il lavoro del progetto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994861"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="2fd3a-103">Panoramica delle righe di offerta basate su progetto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="2fd3a-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="2fd3a-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2fd3a-105">Le righe di offerta basate su progetto sono progettate per aiutare a stimare il lavoro del progetto per un impegno.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="2fd3a-106">La struttura di una riga di offerta basata su progetto è estesa per le stime di progetto con i seguenti concetti:</span><span class="sxs-lookup"><span data-stu-id="2fd3a-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="2fd3a-107">Metodo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="2fd3a-107">Billing Method</span></span>
- <span data-ttu-id="2fd3a-108">Mapping di progetti e attività</span><span class="sxs-lookup"><span data-stu-id="2fd3a-108">Project and Task Mapping</span></span>
- <span data-ttu-id="2fd3a-109">Classi di transazione incluse</span><span class="sxs-lookup"><span data-stu-id="2fd3a-109">Included Transaction classes</span></span>
- <span data-ttu-id="2fd3a-110">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="2fd3a-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="2fd3a-111">Impostazione dell'esigibilità</span><span class="sxs-lookup"><span data-stu-id="2fd3a-111">Chargeability setup</span></span>
- <span data-ttu-id="2fd3a-112">Stima che utilizza i dettagli della riga di offerta</span><span class="sxs-lookup"><span data-stu-id="2fd3a-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="2fd3a-113">Clienti riga di offerta</span><span class="sxs-lookup"><span data-stu-id="2fd3a-113">Quote line Customers</span></span>

<span data-ttu-id="2fd3a-114">La tabella seguente fornisce informazioni sui campi nella scheda **Generale** della riga di offerta basata su progetto.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="2fd3a-115">Questi campi aiutano a creare le basi per una stima dettagliata e completa del lavoro del progetto.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="2fd3a-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="2fd3a-116">**Field**</span></span> | <span data-ttu-id="2fd3a-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2fd3a-117">**Description**</span></span> | <span data-ttu-id="2fd3a-118">**Impatto downstream**</span><span class="sxs-lookup"><span data-stu-id="2fd3a-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2fd3a-119">Nome</span><span class="sxs-lookup"><span data-stu-id="2fd3a-119">Name</span></span> | <span data-ttu-id="2fd3a-120">Il nome della riga di offerta che ti consente di identificare la componente discreta dell'offerta che viene stimata.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="2fd3a-121">Copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-122">Metodo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="2fd3a-122">Billing Method</span></span> | <span data-ttu-id="2fd3a-123">In un'offerta creata da un'opportunità, questo valore viene copiato dal campo corrispondente nella riga dell'opportunità.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="2fd3a-124">Questo campo include i due principali modelli di contratto supportati da Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="2fd3a-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="2fd3a-125">- Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="2fd3a-125">- Fixed price</span></span></br><span data-ttu-id="2fd3a-126">- Tempistica e materiali.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-126">- Time and material.</span></span>| <span data-ttu-id="2fd3a-127">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-128">Project</span><span class="sxs-lookup"><span data-stu-id="2fd3a-128">Project</span></span> | <span data-ttu-id="2fd3a-129">Utilizza questo campo facoltativo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="2fd3a-130">Quando un progetto viene mappato a una riga dell'offerta, viene semplificata l'impostazione delle attività addebitabili e anche l'inserimento di una stima basata sul progetto nella riga dell'offerta come dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="2fd3a-131">Quando un progetto non è mappato a una riga di offerta basata su progetto, la stima deve essere creata manualmente creando ogni dettaglio della riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="2fd3a-132">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="2fd3a-133">Attività incluse</span><span class="sxs-lookup"><span data-stu-id="2fd3a-133">Included Tasks</span></span> | <span data-ttu-id="2fd3a-134">Indica se questa riga dell'offerta viene utilizzata per tutte o alcune delle attività di progetto per il progetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="2fd3a-135">Di seguito sono riportati i valori possibili di questo campo:</span><span class="sxs-lookup"><span data-stu-id="2fd3a-135">This field has the following possible values:</span></span></br><span data-ttu-id="2fd3a-136">- Tutte le attività di progetto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-136">- All project tasks</span></span></br><span data-ttu-id="2fd3a-137">- Solo le attività di progetto selezionate</span><span class="sxs-lookup"><span data-stu-id="2fd3a-137">- Selected project tasks only</span></span></br><span data-ttu-id="2fd3a-138">Un valore vuoto in questo campo equivale all'opzione **Tutte le attività di progetto**.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="2fd3a-139">Quando è selezionata l'opzione **Solo le attività di progetto selezionate** nella pagina del progetto, la scheda **Configurazione fatturazione attività** consente di selezionare attività specifiche per associarle a questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="2fd3a-140">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-141">Includi tempo</span><span class="sxs-lookup"><span data-stu-id="2fd3a-141">Include Time</span></span> | <span data-ttu-id="2fd3a-142">Un valore **Sì**/**No** indica se le transazioni temporali o i costi di manodopera nel progetto selezionato saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2fd3a-143">Un valore **No** indica che le transazioni temporali o i costi di manodopera non saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2fd3a-144">Un valore **Sì** indica che le transazioni temporali o i costi di manodopera saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2fd3a-145">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-146">Includi spesa</span><span class="sxs-lookup"><span data-stu-id="2fd3a-146">Include Expense</span></span> | <span data-ttu-id="2fd3a-147">Un valore **Sì**/**No** indica se i costi della spesa nel progetto selezionato saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2fd3a-148">Un valore **No** indica che i costi di spesa non saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2fd3a-149">Un valore **Sì** indica che i costi di spesa saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2fd3a-150">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-151">Includi materiale</span><span class="sxs-lookup"><span data-stu-id="2fd3a-151">Include Material</span></span> | <span data-ttu-id="2fd3a-152">Un valore **Sì**/**No** indica se i costi materiale nel progetto selezionato saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2fd3a-153">Un valore **No** indica che i costi materiale non saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2fd3a-154">Un valore **Sì** indica che i costi materiale non saranno inclusi nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2fd3a-155">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-156">Includi commissione</span><span class="sxs-lookup"><span data-stu-id="2fd3a-156">Include Fee</span></span> | <span data-ttu-id="2fd3a-157">Un valore **Sì**/**No** indica se le commissioni nel progetto selezionato saranno incluse nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2fd3a-158">Un valore **No** indica che le commissioni non saranno incluse nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2fd3a-159">Un valore **Sì** indica che le commissioni saranno incluse nella stima in questa riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2fd3a-160">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-161">Importo offerto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-161">Quoted Amount</span></span> | <span data-ttu-id="2fd3a-162">Si tratta dell'importo dell'offerta al cliente per tutto il lavoro previsto in questa riga di offerta basata su progetto.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="2fd3a-163">In un'offerta creata da un'opportunità, questo valore viene copiato dal campo **Budget cliente** nella riga dell'opportunità.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="2fd3a-164">Quando la riga di offerta basata su progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="2fd3a-165">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-166">Imposta stimata</span><span class="sxs-lookup"><span data-stu-id="2fd3a-166">Estimated Tax</span></span> | <span data-ttu-id="2fd3a-167">Questo è un campo modificabile che consente all'utente di aggiungere l'importo delle imposte stimate nella riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="2fd3a-168">Quando una riga di offerta basata su progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="2fd3a-169">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-170">Importo offerto al netto delle imposte</span><span class="sxs-lookup"><span data-stu-id="2fd3a-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="2fd3a-171">Questo campo rappresenta l'importo della riga dell'offerta al netto delle imposte ed è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="2fd3a-172">L'importo in questo campo viene calcolato come *Importo offerto + imposte*.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="2fd3a-173">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-174">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="2fd3a-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="2fd3a-175">Questo campo è modificabile ed è disponibile solo per le righe dell'offerta basate su progetto che hanno un metodo di fatturazione **Tempistica e materiali**.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="2fd3a-176">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2fd3a-177">Budget cliente</span><span class="sxs-lookup"><span data-stu-id="2fd3a-177">Customer Budget</span></span> | <span data-ttu-id="2fd3a-178">Questo campo è modificabile e viene copiato dal campo corrispondente nella riga dell'opportunità se l'offerta è stata creata da un'opportunità.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="2fd3a-179">Questo valore viene copiato nella voce di contratto di progetto creata da questa riga di offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="2fd3a-180">Regole di convalida per i campi nella scheda Generale delle righe di offerta basate su progetto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="2fd3a-181">**Regola 1**: se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto**, un progetto è incluso nella riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="2fd3a-182">**Regola 2**: se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto**, un progetto e una determinata classe di transazione possono essere inclusi solo in una riga di offerta basata su progetto di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="2fd3a-183">**Regola 3**: se il campo **Attività incluse** è vuoto o se è impostato su **Solo le attività di progetto selezionate**, un progetto e una determinata classe di transazione possono essere inclusi in più righe di offerta basata su progetto di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="2fd3a-184">**Regola 4**: se un'opportunità ha più offerte, possono esserci righe di offerta da offerte diverse che fanno tutte riferimento allo stesso progetto e includono la stessa classe di transazione.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="2fd3a-185">**Regola 5**: se le offerte non appartengono alla stessa opportunità, non possono includere lo stesso progetto e la stessa classe di transazione.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="2fd3a-186">
                    <strong>Opportunità</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="2fd3a-187">
                    <strong>Offerta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="2fd3a-188">
                    <strong>Riga di offerta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="2fd3a-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="2fd3a-190">
                    <strong>Attività incluse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="2fd3a-191">
                    <strong>Includi tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="2fd3a-192">
                    <strong>Includi spesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="2fd3a-193">
                    <strong>Includi materiale</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="2fd3a-194">
                    <strong>Includi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="2fd3a-195">
                    <strong>Commissione</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="2fd3a-196">
                    <strong>Valido/Non valido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="2fd3a-197">
                    <strong>Motivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fd3a-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2fd3a-198">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-199">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-200">QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-201">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-202">Vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-203">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-204">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-205">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-206">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-207">Non valido</span><span class="sxs-lookup"><span data-stu-id="2fd3a-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-208">Violazione della regola n. 2.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-208">Violation of Rule #2.</span></span> <span data-ttu-id="2fd3a-209">Tempo, spesa e commissioni nel progetto P1 sono incluse nelle righe di offerta QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2fd3a-210">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-211">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-212">QL2</span><span class="sxs-lookup"><span data-stu-id="2fd3a-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-213">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-214">Vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-215">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-216">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-217">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-218">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-218">Yes</span></span> </p>
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
<span data-ttu-id="2fd3a-219">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-220">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-221">QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-222">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-223">Vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-224">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-225">No</span><span class="sxs-lookup"><span data-stu-id="2fd3a-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-226">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-227">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-228">Non valido</span><span class="sxs-lookup"><span data-stu-id="2fd3a-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-229">Violazione della regola n. 2.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-229">Violation of Rule #2.</span></span> <span data-ttu-id="2fd3a-230">Tempo, materiale e commissioni nel progetto P1 sono incluse nelle righe di offerta QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="2fd3a-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2fd3a-231">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-232">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-233">QL2</span><span class="sxs-lookup"><span data-stu-id="2fd3a-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-234">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-235">Vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-236">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-237">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-238">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-239">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-239">Yes</span></span> </p>
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
<span data-ttu-id="2fd3a-240">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-241">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-242">QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-243">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-244">Vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-245">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-246">No</span><span class="sxs-lookup"><span data-stu-id="2fd3a-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-247">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-248">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-249">Valido</span><span class="sxs-lookup"><span data-stu-id="2fd3a-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-250">Tempo, materiale e commissioni nel progetto P1 sono incluse in QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="2fd3a-251">La spesa nel progetto P1 è inclusa in QL2</span><span class="sxs-lookup"><span data-stu-id="2fd3a-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="2fd3a-252">Nessuna sovrapposizione in ciò che viene incluso in ogni riga di offerta e quindi valido.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2fd3a-253">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-254">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-255">QL2</span><span class="sxs-lookup"><span data-stu-id="2fd3a-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-256">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-257">Vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-258">No</span><span class="sxs-lookup"><span data-stu-id="2fd3a-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-259">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-260">No</span><span class="sxs-lookup"><span data-stu-id="2fd3a-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-261">No</span><span class="sxs-lookup"><span data-stu-id="2fd3a-261">No</span></span> </p>
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
<span data-ttu-id="2fd3a-262">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-263">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-264">QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-265">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-266">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="2fd3a-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-267">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-268">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-269">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-270">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-271">Non valido</span><span class="sxs-lookup"><span data-stu-id="2fd3a-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-272">Violazione della regola n. 2</span><span class="sxs-lookup"><span data-stu-id="2fd3a-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="2fd3a-273">Q1 include tempo, materiale, spese e commissioni in un sottoinsieme di attività nel progetto P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="2fd3a-274">QL2 include tempo, spese e commissioni per l'intero progetto P1 e quindi si sovrappone a quanto incluso in Q1.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2fd3a-275">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-276">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-277">QL2</span><span class="sxs-lookup"><span data-stu-id="2fd3a-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-278">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-279">Vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-280">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-281">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-282">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-283">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-283">Yes</span></span> </p>
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
<span data-ttu-id="2fd3a-284">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-285">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-286">QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-287">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-288">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="2fd3a-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-289">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-290">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-291">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-292">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-293">Valido</span><span class="sxs-lookup"><span data-stu-id="2fd3a-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-294">Per la regola n. 3</span><span class="sxs-lookup"><span data-stu-id="2fd3a-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="2fd3a-295">Q1 include tempo, materiale, spese e commissioni in un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2fd3a-296">QL2 include tempo, materiale, spese e commissioni per un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2fd3a-297">L'unica convalida aggiuntiva riguarda il sottoinsieme di attività in QL1 che è diverso dal sottoinsieme di attività in QL2 per garantire che non vi siano sovrapposizioni.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="2fd3a-298">Ciò viene eseguito dal sistema quando vengono associate le attività.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2fd3a-299">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-300">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-301">QL2</span><span class="sxs-lookup"><span data-stu-id="2fd3a-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-302">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-303">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="2fd3a-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-304">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-305">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-306">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-307">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-307">Yes</span></span> </p>
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
<span data-ttu-id="2fd3a-308">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-309">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-310">QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-311">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-312">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-313">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-314">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-315">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-316">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-317">Valido</span><span class="sxs-lookup"><span data-stu-id="2fd3a-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-318">Secondo la regola n. 5, Q1 e Q2 sono due offerte della stessa opportunità, quindi possono entrambe stimare gli stessi componenti di un progetto.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2fd3a-319">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-320">Secondo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-321">QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-322">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-323">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-324">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-325">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-326">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-327">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-327">Yes</span></span> </p>
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
<span data-ttu-id="2fd3a-328">O1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-329">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-330">QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-331">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-332">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-333">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-334">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-335">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-336">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-337">Non valido</span><span class="sxs-lookup"><span data-stu-id="2fd3a-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fd3a-338">Secondo la regola n. 4, Q1 e Q2 sono due offerte di differenti opportunità, quindi non possono stimare gli stessi componenti di un stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="2fd3a-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2fd3a-339">O2</span><span class="sxs-lookup"><span data-stu-id="2fd3a-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2fd3a-340">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="2fd3a-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2fd3a-341">QL1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-342">P1</span><span class="sxs-lookup"><span data-stu-id="2fd3a-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2fd3a-343">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="2fd3a-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2fd3a-344">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2fd3a-345">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fd3a-346">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2fd3a-347">Sì</span><span class="sxs-lookup"><span data-stu-id="2fd3a-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
