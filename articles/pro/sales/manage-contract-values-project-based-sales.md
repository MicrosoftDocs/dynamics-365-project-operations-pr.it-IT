---
title: Panoramica delle voci di contratto basate su progetto
description: Questo argomento fornisce informazioni sull'utilizzo delle voci di contratto basate su progetto.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003141"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="b6ee3-103">Panoramica delle voci di contratto basate su progetto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-103">Project-based contract lines overview</span></span>

<span data-ttu-id="b6ee3-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="b6ee3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b6ee3-105">Le voci di contratto basate su progetto in Dynamics 365 Project Operations sono progettate per contenere i contratti di stima e fatturazione per componenti specifici del lavoro di progetto su un impegno.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="b6ee3-106">La struttura di una voce di contratto basata su progetto viene estesa per le stime di progetto e gli scenari di fatturazione con i seguenti concetti:</span><span class="sxs-lookup"><span data-stu-id="b6ee3-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="b6ee3-107">Metodo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="b6ee3-107">Billing method</span></span>
- <span data-ttu-id="b6ee3-108">Mapping di progetti e attività</span><span class="sxs-lookup"><span data-stu-id="b6ee3-108">Project and task mapping</span></span>
- <span data-ttu-id="b6ee3-109">Classi di transazione incluse</span><span class="sxs-lookup"><span data-stu-id="b6ee3-109">Included transaction classes</span></span>
- <span data-ttu-id="b6ee3-110">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="b6ee3-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="b6ee3-111">Impostazione dell'esigibilità</span><span class="sxs-lookup"><span data-stu-id="b6ee3-111">Chargeability setup</span></span>
- <span data-ttu-id="b6ee3-112">Stime utilizzando i dettagli della voce di contratto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-112">Estimates using contract line details</span></span>
- <span data-ttu-id="b6ee3-113">Clienti voce di contratto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-113">Contract line customers</span></span>

<span data-ttu-id="b6ee3-114">La tabella seguente include i campi nella scheda **Generale** delle voci di contratto basate su progetto che aiutano a creare le basi per una stima dettagliata e iniziale e le modalità di fatturazione per il lavoro basato su progetto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="b6ee3-115">Campo</span><span class="sxs-lookup"><span data-stu-id="b6ee3-115">Field</span></span> | <span data-ttu-id="b6ee3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6ee3-116">Description</span></span> | <span data-ttu-id="b6ee3-117">Impatto downstream</span><span class="sxs-lookup"><span data-stu-id="b6ee3-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b6ee3-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-118">**Name**</span></span> | <span data-ttu-id="b6ee3-119">Nome della voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-119">Name of the contract line.</span></span> <span data-ttu-id="b6ee3-120">Identifica il componente discreto del contratto che si sta stimando.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="b6ee3-121">Per un contratto di progetto creato da un'offerta, questo valore viene copiato da un valore corrispondente della riga di offerta basata su progetto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="b6ee3-122">Il nome copiato nella riga di fattura di progetto creata da questa voce di contratto quando viene creata la fattura.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="b6ee3-123">**Metodo di fatturazione**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-123">**Billing Method**</span></span> | <span data-ttu-id="b6ee3-124">In un contratto di progetto creato da un'offerta, questo valore viene copiato dal campo corrispondente della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="b6ee3-125">Questo è un set di opzioni che rappresenta i due principali modelli di contratto supportati da Project Operations:</span><span class="sxs-lookup"><span data-stu-id="b6ee3-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="b6ee3-126">- **Prezzo fisso**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-126">- **Fixed Price**</span></span></br><span data-ttu-id="b6ee3-127">- **Tempistica e materiali**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-127">- **Time and Material**</span></span> | <span data-ttu-id="b6ee3-128">In base al metodo di fatturazione della voce di contratto a cui si fa riferimento, verrà elaborata la transazione effettiva.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="b6ee3-129">Se la voce di contratto a cui fa riferimento il valore effettivo dispone di un metodo di fatturazione di tempo e materiale, vengono creati i record dei costi e delle vendite non fatturate.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="b6ee3-130">Se la voce di contratto a cui fa riferimento il valore effettivo ha un metodo di fatturazione a prezzo fisso, viene creato solo un costo effettivo.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="b6ee3-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-131">**Project**</span></span> | <span data-ttu-id="b6ee3-132">Utilizza questo campo per identificare il progetto che verrà utilizzato per fornire il lavoro su questo impegno.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="b6ee3-133">Questo valore verrà utilizzato insieme a **Attività incluse** e **Classi di transazione incluse** per risolvere il riferimento della voce di contratto in un record di riga effettivo o di stima.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="b6ee3-134">**Attività incluse**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-134">**Included Tasks**</span></span> | <span data-ttu-id="b6ee3-135">Indica se questa voce di contratto include tutte le attività di progetto per il progetto selezionato o solo un sottoinsieme delle attività.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="b6ee3-136">È un set di opzioni con i seguenti possibili valori:</span><span class="sxs-lookup"><span data-stu-id="b6ee3-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="b6ee3-137">- **Tutte le attività di progetto**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-137">- **All Project Tasks**</span></span></br><span data-ttu-id="b6ee3-138">- **Solo le attività di progetto selezionate**.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="b6ee3-139">Un valore vuoto in questo campo è uguale alla selezione di **Tutte le attività di progetto**.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="b6ee3-140">Se **Solo attività selezionate** è selezionato, puoi selezionare attività specifiche e associarle a questa voce di contratto nella scheda **Configurazione fatturazione attività** della pagina **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="b6ee3-141">Il valore verrà utilizzato insieme a **Progetto** e **Classi di transazione incluse** per risolvere il riferimento della voce di contratto in un record di riga effettivo o di stima.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b6ee3-142">**Includi tempo**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-142">**Include Time**</span></span> | <span data-ttu-id="b6ee3-143">Un valore **Sì**/**No** indica se le transazioni di tempo o i costi di manodopera nel progetto selezionato saranno inclusi in questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="b6ee3-144">Il valore **No** indica che le transazioni di tempo o i costi di manodopera non verranno inclusi in questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="b6ee3-145">Il valore **Sì** indica che verranno inclusi.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="b6ee3-146">Questo valore viene utilizzato insieme al progetto per risolvere il riferimento della voce di contratto in un record di riga effettiva o di stima.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b6ee3-147">**Includi spesa**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-147">**Include Expense**</span></span> | <span data-ttu-id="b6ee3-148">Un valore **Sì**/**No** indica se i costi di spesa nel progetto selezionato saranno inclusi in questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="b6ee3-149">Il valore **No** indica che i costi di spesa non verranno inclusi in questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="b6ee3-150">Il valore **Sì** indica che verranno inclusi.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="b6ee3-151">Questo valore viene utilizzato insieme al progetto per risolvere il riferimento della voce di contratto in un record di riga effettiva o di stima.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b6ee3-152">**Includi materiali**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-152">**Include Materials**</span></span> | <span data-ttu-id="b6ee3-153">Un valore **Sì**/**No** indica se i costi di materiale nel progetto selezionato saranno inclusi in questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="b6ee3-154">Un valore **No** indica che i costi materiale non saranno inclusi in questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="b6ee3-155">Il valore **Sì** indica che verranno inclusi.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="b6ee3-156">Questo valore viene utilizzato insieme al progetto per risolvere il riferimento della voce di contratto in un record di riga effettiva o di stima.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b6ee3-157">**Includi commissione**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-157">**Include Fee**</span></span> | <span data-ttu-id="b6ee3-158">Un valore **Sì**/**No** indica se le commissioni nel progetto selezionato saranno inclusi in questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="b6ee3-159">Il valore **No** indica che le commissioni non verranno incluse in questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="b6ee3-160">Il valore **Sì** indica che verranno inclusi.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="b6ee3-161">Questo valore viene utilizzato insieme al progetto per risolvere il riferimento della voce di contratto in un record di riga effettiva o di stima.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b6ee3-162">**Importo contratto**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-162">**Contracted Amount**</span></span> | <span data-ttu-id="b6ee3-163">In una voce di contratto a prezzo fisso, questo importo è il valore concordato che verrà fatturato al cliente per tutti i componenti di lavoro associati a questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="b6ee3-164">In una voce di contratto tempo e materiale, questo importo è il valore stimato che verrà fatturato al cliente per tutti i componenti di lavoro associati a questa voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="b6ee3-165">In un contratto di progetto creato da un'offerta, questo valore viene copiato dal campo corrispondente della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="b6ee3-166">Quando una voce di contratto basata su progetto include dettagli di riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo nei dettagli della voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="b6ee3-167">Quando la voce di contratto include i dettagli della riga, questo valore può essere modificato modificando gli importi dei dettagli della riga.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="b6ee3-168">In una voce di contratto a prezzo fisso, questo valore viene utilizzato per generare l'importo prima delle imposte sui passaggi fondamentali di fatturazione periodica.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="b6ee3-169">**Imposta stimata**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-169">**Estimated Tax**</span></span> | <span data-ttu-id="b6ee3-170">L'utente può modificare questo campo per inserire l'importo delle imposte stimato nella voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="b6ee3-171">Quando una voce di contratto basata su progetto include dettagli di riga, questo campo è bloccato per la modifica e viene riepilogato dall'importo delle imposte nei dettagli della voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="b6ee3-172">Quando la voce di contratto include i dettagli della riga, questo valore può essere modificato modificando gli importi delle imposte dei dettagli della riga.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="b6ee3-173">In una voce di contratto a prezzo fisso, questo valore viene utilizzato per generare le imposte sui passaggi fondamentali di fatturazione periodica.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="b6ee3-174">**Importo contratto al netto delle imposte**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="b6ee3-175">L'importo della voce di contratto al netto delle imposte.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-175">The contract line amount after tax.</span></span> <span data-ttu-id="b6ee3-176">Questo campo è di sola lettura e viene calcolato come **importo di contratto + imposte**.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="b6ee3-177">In una voce di contratto a prezzo fisso, questo valore viene utilizzato per generare i passaggi fondamentali di fatturazione periodica.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="b6ee3-178">**Limite da non superare**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="b6ee3-179">L'utente può modificare questo campo ed è disponibile solo sulle voci di contratto basate su progetto che hanno il metodo di fatturazione impostato come tempo e materiale.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="b6ee3-180">L'utente può modificare questo campo.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-180">The user can edit this field.</span></span> <span data-ttu-id="b6ee3-181">Quando un valore effettivo per tempo e materiale fa riferimento a questa voce di contratto per tempo e materiale, l'importo del valore effettivo viene valutato rispetto al limite da non superare della voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="b6ee3-182">Questa valutazione è completata dopo aver contabilizzato gli importi già spesi e impegnati.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="b6ee3-183">**Budget cliente**</span><span class="sxs-lookup"><span data-stu-id="b6ee3-183">**Customer Budget**</span></span> | <span data-ttu-id="b6ee3-184">Questo campo è modificabile e viene viene copiato dal campo corrispondente della riga di offerta se il contratto è stato creato da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="b6ee3-185">Questo campo è utilizzato solo per informazioni e non ha alcun significato downstream.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="b6ee3-186">Regole di convalida per le opzioni nella scheda Generale delle voci di contratto basate su progetto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="b6ee3-187">Regola 1: se il campo **Attività incluse** è vuoto o impostato su **Tutte le attività di progetto**, tutte le attività di progetto sono incluse nella voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="b6ee3-188">Regola 2: quando il campo **Attività incluse** è vuoto o impostato esplicitamente su **Tutte le attività di progetto**, un progetto e una determinata classe di transazione possono essere inclusi solo in una voce di contratto basata su progetto di un contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="b6ee3-189">Regola 3: quando il campo **Attività incluse** impostato esplicitamente su **Solo le attività di progetto selezionate**, un progetto e una determinata classe di transazione possono essere inclusi in più voci di contratto basata su progetto di un contratto.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="b6ee3-190">
                    <strong>Contratto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b6ee3-191">
                    <strong>Voce di contratto</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="b6ee3-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="b6ee3-193">
                    <strong>Attività incluse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="b6ee3-194">
                    <strong>Includi tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="b6ee3-195">
                    <strong>Includi spesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="b6ee3-196">
                    <strong>Includi materiali</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="b6ee3-197">
                    <strong>Includi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="b6ee3-198">
                    <strong>Commissione</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="b6ee3-199">
                    <strong>Valido/Non valido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="b6ee3-200">
                    <strong>Motivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6ee3-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-201">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-202">CL1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-203">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-204">Vuoto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-205">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-206">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-207">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-208">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-209">Non valido</span><span class="sxs-lookup"><span data-stu-id="b6ee3-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-210">Violazione della regola n. 2.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-210">Violation of Rule #2.</span></span> <span data-ttu-id="b6ee3-211">Tempo, spesa, materiali e commissioni nel progetto P1 sono inclusi nelle voci di contratto CL1 e CL2.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-212">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-213">CL2</span><span class="sxs-lookup"><span data-stu-id="b6ee3-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-214">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-215">Vuoto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-216">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-217">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-218">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-219">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-220">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-221">CL1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-222">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-223">Vuoto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-224">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-225">No</span><span class="sxs-lookup"><span data-stu-id="b6ee3-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-226">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-227">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-228">Non valido</span><span class="sxs-lookup"><span data-stu-id="b6ee3-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-229">Violazione della regola n. 2.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-229">Violation of Rule #2.</span></span> <span data-ttu-id="b6ee3-230">Tempo, materiali e commissioni nel progetto P1 sono inclusi nelle voci di contratto CL1 e CL2.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-231">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-232">CL2</span><span class="sxs-lookup"><span data-stu-id="b6ee3-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-233">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-234">Vuoto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-235">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-236">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-237">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-238">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-239">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-240">CL1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-241">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-242">Vuoto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-243">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-244">No</span><span class="sxs-lookup"><span data-stu-id="b6ee3-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-245">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-246">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-247">Valido</span><span class="sxs-lookup"><span data-stu-id="b6ee3-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-248">Tempo, materiali e commissioni nel progetto P1 sono incluse in CL1.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="b6ee3-249">La spesa sul progetto P1 è inclusa in CL2.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="b6ee3-250">Nessuna sovrapposizione in ciò che viene incluso in ogni voce di contratto e quindi valido.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-251">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-252">CL2</span><span class="sxs-lookup"><span data-stu-id="b6ee3-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-253">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-254">Vuoto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-255">No</span><span class="sxs-lookup"><span data-stu-id="b6ee3-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-256">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-257">No</span><span class="sxs-lookup"><span data-stu-id="b6ee3-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-258">No</span><span class="sxs-lookup"><span data-stu-id="b6ee3-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-259">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-260">CL1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-261">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-262">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="b6ee3-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-263">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-264">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-265">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-266">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-267">Non valido</span><span class="sxs-lookup"><span data-stu-id="b6ee3-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-268">Violazione della regola n. 2</span><span class="sxs-lookup"><span data-stu-id="b6ee3-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="b6ee3-269">C1 include tempo, materiali, spese e commissioni in un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="b6ee3-270">CL2 include tempo, materiali, spese e commissioni per l'intero progetto P1 e quindi si sovrappone a quanto incluso in C1.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-271">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-272">CL2</span><span class="sxs-lookup"><span data-stu-id="b6ee3-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-273">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-274">Vuoto</span><span class="sxs-lookup"><span data-stu-id="b6ee3-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-275">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-276">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-277">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-278">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-279">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-280">CL1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-281">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-282">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="b6ee3-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-283">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-284">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-285">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-286">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-287">Valido</span><span class="sxs-lookup"><span data-stu-id="b6ee3-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6ee3-288">Per la regola n. 3</span><span class="sxs-lookup"><span data-stu-id="b6ee3-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="b6ee3-289">C1 include tempo, spese, materiali e commissioni in un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="b6ee3-290">CL2 include tempo, spese, materiali e commissioni per un sottoinsieme di attività nel progetto P1.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="b6ee3-291">L'unica convalida aggiuntiva riguarda il sottoinsieme di attività in CL1 che è diverso dal sottoinsieme di attività in CL2 per garantire che non vi siano sovrapposizioni.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="b6ee3-292">Ciò viene eseguito dal sistema quando vengono associate le attività.</span><span class="sxs-lookup"><span data-stu-id="b6ee3-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6ee3-293">C1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b6ee3-294">CL2</span><span class="sxs-lookup"><span data-stu-id="b6ee3-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-295">P1</span><span class="sxs-lookup"><span data-stu-id="b6ee3-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b6ee3-296">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="b6ee3-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-297">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b6ee3-298">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-299">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b6ee3-300">Sì</span><span class="sxs-lookup"><span data-stu-id="b6ee3-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
