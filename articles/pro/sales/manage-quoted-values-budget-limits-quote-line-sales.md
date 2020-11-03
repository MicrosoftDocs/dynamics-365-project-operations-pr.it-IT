---
title: Righe dell'offerta basate sul progetto (Pro)
description: Questo argomento fornisce informazioni sull'utilizzo delle righe dell'offerta basate sul progetto per il lavoro del progetto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078806"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="862ba-104">Righe dell'offerta basate sul progetto (Pro)</span><span class="sxs-lookup"><span data-stu-id="862ba-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="862ba-105">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="862ba-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="862ba-106">Le righe dell'offerta basate sul progetto sono progettate per aiutare a stimare il lavoro del progetto per un impegno.</span><span class="sxs-lookup"><span data-stu-id="862ba-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="862ba-107">La struttura di una riga dell'offerta basata sul progetto è estesa per le stime di progetto con i seguenti concetti:</span><span class="sxs-lookup"><span data-stu-id="862ba-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="862ba-108">Metodo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="862ba-108">Billing Method</span></span>
- <span data-ttu-id="862ba-109">Mapping di progetti e attività</span><span class="sxs-lookup"><span data-stu-id="862ba-109">Project and Task Mapping</span></span>
- <span data-ttu-id="862ba-110">Classi di transazione incluse</span><span class="sxs-lookup"><span data-stu-id="862ba-110">Included Transaction classes</span></span>
- <span data-ttu-id="862ba-111">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="862ba-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="862ba-112">Impostazione dell'esigibilità</span><span class="sxs-lookup"><span data-stu-id="862ba-112">Chargeability setup</span></span>
- <span data-ttu-id="862ba-113">Stima utilizzando i dettagli della riga dell'offerta</span><span class="sxs-lookup"><span data-stu-id="862ba-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="862ba-114">Clienti riga di offerta</span><span class="sxs-lookup"><span data-stu-id="862ba-114">Quote line Customers</span></span>

<span data-ttu-id="862ba-115">La tabella seguente fornisce informazioni sui campi nella scheda **Generale** della riga dell'offerta basata sul progetto.</span><span class="sxs-lookup"><span data-stu-id="862ba-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="862ba-116">Questi campi aiutano a creare le basi per una stima dettagliata e completa del lavoro del progetto.</span><span class="sxs-lookup"><span data-stu-id="862ba-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="862ba-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="862ba-117">**Field**</span></span> | <span data-ttu-id="862ba-118">**Pertinenza, scopo e indicazioni**</span><span class="sxs-lookup"><span data-stu-id="862ba-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="862ba-119">**Impatto downstream**</span><span class="sxs-lookup"><span data-stu-id="862ba-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="862ba-120">Nome</span><span class="sxs-lookup"><span data-stu-id="862ba-120">Name</span></span> | <span data-ttu-id="862ba-121">Il nome della riga dell'offerta che dovrebbe aiutarti a identificare il componente discreto dell'offerta che viene stimata.</span><span class="sxs-lookup"><span data-stu-id="862ba-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="862ba-122">Copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-123">Metodo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="862ba-123">Billing Method</span></span> | <span data-ttu-id="862ba-124">In un'offerta creata da un'opportunità, questo valore viene copiato dal campo corrispondente nella riga dell'opportunità.</span><span class="sxs-lookup"><span data-stu-id="862ba-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="862ba-125">Questo campo include i due principali modelli di contratto supportati da Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="862ba-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="862ba-126">- Prezzo fisso</span><span class="sxs-lookup"><span data-stu-id="862ba-126">- Fixed price</span></span></br><span data-ttu-id="862ba-127">- Tempistica e materiali.</span><span class="sxs-lookup"><span data-stu-id="862ba-127">- Time and material.</span></span>| <span data-ttu-id="862ba-128">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-129">Project</span><span class="sxs-lookup"><span data-stu-id="862ba-129">Project</span></span> | <span data-ttu-id="862ba-130">Utilizza questo campo facoltativo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno.</span><span class="sxs-lookup"><span data-stu-id="862ba-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="862ba-131">Quando un progetto viene mappato a una riga dell'offerta, viene semplificata l'impostazione delle attività addebitabili e anche l'inserimento di una stima basata sul progetto nella riga dell'offerta come dettagli della riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="862ba-132">Quando un progetto non è mappato a una riga dell'offerta basata sul progetto, la stima deve essere creata manualmente creando ogni dettaglio della riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="862ba-133">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="862ba-134">Attività incluse</span><span class="sxs-lookup"><span data-stu-id="862ba-134">Included Tasks</span></span> | <span data-ttu-id="862ba-135">Indica se questa riga dell'offerta viene utilizzata per tutte o alcune delle attività di progetto per il progetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="862ba-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="862ba-136">Di seguito sono riportati i valori possibili di questo campo:</span><span class="sxs-lookup"><span data-stu-id="862ba-136">This field has the following possible values:</span></span></br><span data-ttu-id="862ba-137">- Tutte le attività di progetto</span><span class="sxs-lookup"><span data-stu-id="862ba-137">- All project tasks</span></span></br><span data-ttu-id="862ba-138">- Solo le attività di progetto selezionate</span><span class="sxs-lookup"><span data-stu-id="862ba-138">- Selected project tasks only</span></span></br><span data-ttu-id="862ba-139">Un valore vuoto in questo campo equivale all'opzione **Tutte le attività di progetto**.</span><span class="sxs-lookup"><span data-stu-id="862ba-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="862ba-140">Quando **Solo le attività di progetto selezionate** viene selezionato nella pagina del progetto, la scheda **Impostazione fatturazione attività** consente di selezionare attività specifiche per associarle a questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="862ba-141">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-142">Includi tempo</span><span class="sxs-lookup"><span data-stu-id="862ba-142">Include Time</span></span> | <span data-ttu-id="862ba-143">Un contrassegno **Sì**/**No** indica se le transazioni temporali o i costi di manodopera sul progetto selezionato saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="862ba-144">Un valore **No** indica che le transazioni temporali o i costi di manodopera non saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="862ba-145">Un valore **Sì** indica che le transazioni temporali o i costi di manodopera saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="862ba-146">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-147">Includi spesa</span><span class="sxs-lookup"><span data-stu-id="862ba-147">Include Expense</span></span> | <span data-ttu-id="862ba-148">Un contrassegno **Sì**/**No** indica se i costi di spesa sul progetto selezionato saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="862ba-149">Un valore **No** indica che i costi di spesa non saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="862ba-150">Un valore **Sì** indica che i costi di spesa saranno inclusi nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="862ba-151">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-152">Includi commissione</span><span class="sxs-lookup"><span data-stu-id="862ba-152">Include Fee</span></span> | <span data-ttu-id="862ba-153">Un contrassegno **Sì**/**No** indica se le commissioni sul progetto selezionato saranno incluse nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="862ba-154">Un valore **No** indica che le commissioni non saranno incluse nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="862ba-155">Un valore **Sì** indica che le commissioni saranno incluse nella stima su questa riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="862ba-156">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-157">Importo offerto</span><span class="sxs-lookup"><span data-stu-id="862ba-157">Quoted Amount</span></span> | <span data-ttu-id="862ba-158">Questo è l'importo che verrà offerto al cliente per tutto il lavoro previsto in questa riga dell'offerta basata sul progetto.</span><span class="sxs-lookup"><span data-stu-id="862ba-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="862ba-159">In un'offerta creata da un'opportunità, questo valore viene copiato dal campo **Budget cliente** nella riga dell'opportunità.</span><span class="sxs-lookup"><span data-stu-id="862ba-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="862ba-160">Quando la riga dell'offerta basata sul progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="862ba-161">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-162">Imposta stimata</span><span class="sxs-lookup"><span data-stu-id="862ba-162">Estimated Tax</span></span> | <span data-ttu-id="862ba-163">Questo è un campo modificabile che consente all'utente di aggiungere l'importo delle imposte stimate nella riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="862ba-164">Quando una riga dell'offerta basata sul progetto contiene i dettagli della riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="862ba-165">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-166">Importo offerto al netto delle imposte</span><span class="sxs-lookup"><span data-stu-id="862ba-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="862ba-167">Questo campo rappresenta l'importo della riga dell'offerta al netto delle imposte ed è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="862ba-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="862ba-168">L'importo in questo campo viene calcolato come *Importo offerto + imposte*.</span><span class="sxs-lookup"><span data-stu-id="862ba-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="862ba-169">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-170">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="862ba-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="862ba-171">Questo campo è modificabile ed è disponibile solo per le righe dell'offerta basate su progetto che hanno un metodo di fatturazione **Tempistica e materiali**.</span><span class="sxs-lookup"><span data-stu-id="862ba-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="862ba-172">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="862ba-173">Budget cliente</span><span class="sxs-lookup"><span data-stu-id="862ba-173">Customer Budget</span></span> | <span data-ttu-id="862ba-174">Questo campo è modificabile e viene copiato dal campo corrispondente nella riga dell'opportunità se l'offerta è stata creata da un'opportunità.</span><span class="sxs-lookup"><span data-stu-id="862ba-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="862ba-175">Questo valore di campo viene copiato nella voce di contratto del progetto che viene creata da questa riga dell'offerta quando l'offerta viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="862ba-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="862ba-176">Regole di convalida per i campi nella scheda Generale delle righe dell'offerta basate sul progetto</span><span class="sxs-lookup"><span data-stu-id="862ba-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="862ba-177">**Regola 1** : se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto** , un progetto è incluso nella riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="862ba-178">**Regola 2** : se il campo **Attività incluse** è vuoto o se è impostato su **Tutte le attività di progetto** , un progetto e una determinata classe di transazione possono essere inclusi solo in una riga di offerta basata su progetto di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="862ba-179">**Regola 3** : se il campo **Attività incluse** è vuoto o se è impostato su **Solo le attività di progetto selezionate** , un progetto e una determinata classe di transazione possono essere inclusi in più righe di offerta basata su progetto di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="862ba-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="862ba-180">**Regola 4** : se un'opportunità ha più offerte, possono esserci righe di offerta da offerte diverse che fanno tutte riferimento allo stesso progetto e includono la stessa classe di transazione.</span><span class="sxs-lookup"><span data-stu-id="862ba-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="862ba-181">**Regola 5** : se le offerte non appartengono alla stessa opportunità, non possono includere lo stesso progetto e la stessa classe di transazione.</span><span class="sxs-lookup"><span data-stu-id="862ba-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="862ba-182">
                    <strong>Opportunità</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="862ba-183">
                    <strong>Offerta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="862ba-184">
                    <strong>Riga di offerta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="862ba-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="862ba-186">
                    <strong>Attività incluse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="862ba-187">
                    <strong>Includi tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="862ba-188">
                    <strong>Includi spesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="862ba-189">
                    <strong>Includi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="862ba-190">
                    <strong>Tariffa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="862ba-191">
                    <strong>Valido/Non valido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="862ba-192">
                    <strong>Motivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="862ba-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-193">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-194">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-195">QL1</span><span class="sxs-lookup"><span data-stu-id="862ba-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-196">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-197">Foglio bianco</span><span class="sxs-lookup"><span data-stu-id="862ba-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-198">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-199">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-200">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-201">Non valido</span><span class="sxs-lookup"><span data-stu-id="862ba-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-202">Violazione della regola n. 2.</span><span class="sxs-lookup"><span data-stu-id="862ba-202">Violation of Rule #2.</span></span> <span data-ttu-id="862ba-203">Tempistica, spesa e commissioni sul progetto P1 sono incluse nelle righe dell'offerta QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="862ba-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-204">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-205">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-206">QL2</span><span class="sxs-lookup"><span data-stu-id="862ba-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-207">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-208">Foglio bianco</span><span class="sxs-lookup"><span data-stu-id="862ba-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-209">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-210">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-211">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="862ba-212">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-213">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-214">QL1</span><span class="sxs-lookup"><span data-stu-id="862ba-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-215">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-216">Foglio bianco</span><span class="sxs-lookup"><span data-stu-id="862ba-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-217">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-218">No</span><span class="sxs-lookup"><span data-stu-id="862ba-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-219">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-220">Non valido</span><span class="sxs-lookup"><span data-stu-id="862ba-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-221">Violazione della regola n. 2.</span><span class="sxs-lookup"><span data-stu-id="862ba-221">Violation of Rule #2.</span></span> <span data-ttu-id="862ba-222">Tempistica e commissioni sul progetto P1 sono incluse nelle righe dell'offerta QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="862ba-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-223">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-224">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-225">QL2</span><span class="sxs-lookup"><span data-stu-id="862ba-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-226">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-227">Foglio bianco</span><span class="sxs-lookup"><span data-stu-id="862ba-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-228">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-229">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-230">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-231">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-232">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-233">QL1</span><span class="sxs-lookup"><span data-stu-id="862ba-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-234">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-235">Foglio bianco</span><span class="sxs-lookup"><span data-stu-id="862ba-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-236">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-237">No</span><span class="sxs-lookup"><span data-stu-id="862ba-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-238">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-239">Valido</span><span class="sxs-lookup"><span data-stu-id="862ba-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="862ba-240">Tempistica e commissioni sul progetto P1 sono incluse in QL1.</span><span class="sxs-lookup"><span data-stu-id="862ba-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="862ba-241">La spesa sul progetto P1 è inclusa in QL2.</span><span class="sxs-lookup"><span data-stu-id="862ba-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="862ba-242">Non c'è sovrapposizione tra gli elementi inclusi in ogni riga dell'offerta ed è valido.</span><span class="sxs-lookup"><span data-stu-id="862ba-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-243">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-244">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-245">QL2</span><span class="sxs-lookup"><span data-stu-id="862ba-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-246">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-247">Foglio bianco</span><span class="sxs-lookup"><span data-stu-id="862ba-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-248">No</span><span class="sxs-lookup"><span data-stu-id="862ba-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-249">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-250">No</span><span class="sxs-lookup"><span data-stu-id="862ba-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="862ba-251">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-252">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-253">QL1</span><span class="sxs-lookup"><span data-stu-id="862ba-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-254">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-255">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="862ba-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-256">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-257">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-258">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-259">Non valido</span><span class="sxs-lookup"><span data-stu-id="862ba-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-260">Violazione della regola n. 2 precedente</span><span class="sxs-lookup"><span data-stu-id="862ba-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="862ba-261">Q1 include tempistica, spese e commissioni per un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="862ba-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="862ba-262">QL2 include tempistica, spese e commissioni per l'intero progetto P1 e si sovrappone a quanto incluso in Q1.</span><span class="sxs-lookup"><span data-stu-id="862ba-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-263">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-264">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-265">QL2</span><span class="sxs-lookup"><span data-stu-id="862ba-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-266">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-267">Foglio bianco</span><span class="sxs-lookup"><span data-stu-id="862ba-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-268">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-269">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-270">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-271">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-272">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-273">QL1</span><span class="sxs-lookup"><span data-stu-id="862ba-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-274">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-275">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="862ba-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-276">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-277">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-278">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-279">Valido</span><span class="sxs-lookup"><span data-stu-id="862ba-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-280">In base alla regola n. 3 precedente,</span><span class="sxs-lookup"><span data-stu-id="862ba-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="862ba-281">Q1 include tempistica, spese e commissioni per un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="862ba-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="862ba-282">QL2 include tempistica, spese e commissioni per un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="862ba-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="862ba-283">L'unica convalida aggiuntiva riguarda il sottoinsieme di attività in QL1 che è diverso dal sottoinsieme di attività in QL2.</span><span class="sxs-lookup"><span data-stu-id="862ba-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="862ba-284">In questo modo si garantisce che non vi siano sovrapposizioni.</span><span class="sxs-lookup"><span data-stu-id="862ba-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="862ba-285">Ciò viene eseguito dal sistema quando vengono associate le attività.</span><span class="sxs-lookup"><span data-stu-id="862ba-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-286">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-287">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-288">QL2</span><span class="sxs-lookup"><span data-stu-id="862ba-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-289">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-290">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="862ba-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-291">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-292">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-293">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="862ba-294">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-295">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-296">QL1</span><span class="sxs-lookup"><span data-stu-id="862ba-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-297">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-298">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="862ba-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-299">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-300">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-301">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="862ba-302">Valido</span><span class="sxs-lookup"><span data-stu-id="862ba-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-303">In base alla regola n. 5, Q1 e Q2 sono due offerte della stessa opportunità, quindi possono entrambe eseguire una stima per gli stessi componenti di un progetto.</span><span class="sxs-lookup"><span data-stu-id="862ba-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-304">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-305">Secondo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-306">QL1</span><span class="sxs-lookup"><span data-stu-id="862ba-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-307">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-308">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="862ba-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-309">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-310">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-311">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="862ba-312">O1</span><span class="sxs-lookup"><span data-stu-id="862ba-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-313">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-314">QL1</span><span class="sxs-lookup"><span data-stu-id="862ba-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-315">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-316">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="862ba-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-317">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-318">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-319">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="862ba-320">Valido</span><span class="sxs-lookup"><span data-stu-id="862ba-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="862ba-321">In base alla regola n. 4, Q1 e Q2 sono due offerte di opportunità diverse, quindi non possono eseguire una stima per gli stessi componenti dello stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="862ba-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="862ba-322">O2</span><span class="sxs-lookup"><span data-stu-id="862ba-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="862ba-323">Primo trimestre</span><span class="sxs-lookup"><span data-stu-id="862ba-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-324">QL1</span><span class="sxs-lookup"><span data-stu-id="862ba-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-325">P1</span><span class="sxs-lookup"><span data-stu-id="862ba-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="862ba-326">Tutte le attività di progetto o vuoto</span><span class="sxs-lookup"><span data-stu-id="862ba-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-327">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="862ba-328">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="862ba-329">Sì</span><span class="sxs-lookup"><span data-stu-id="862ba-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="862ba-330">Non valido</span><span class="sxs-lookup"><span data-stu-id="862ba-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

