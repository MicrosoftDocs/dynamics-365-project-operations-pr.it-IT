---
title: Contratti di progetto
description: Questo argomento fornisce esempi dei contratti di progetto che puoi creare per vari tipi di progetti e fonti di finanziamento, e come puoi gestire i contratti e inviare fattura ai clienti del progetto.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752676"
---
# <a name="project-contracts"></a><span data-ttu-id="5a185-103">Contratti di progetto</span><span class="sxs-lookup"><span data-stu-id="5a185-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a185-104">Questo articolo fornisce esempi dei contratti di progetto che puoi creare per vari tipi di progetti e fonti di finanziamento, e come puoi gestire i contratti e inviare fattura ai clienti del progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="5a185-105">Il tipo di progetto creato per un contratto di progetto determina il metodo utilizzato per fatturare i clienti del progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="5a185-106">Puoi modificare un contratto di progetto e il progetto correlato, ma non puoi modificare il tipo di progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="5a185-107">Utilizzando un contratto di progetto, puoi fatturare uno o più progetti contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="5a185-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="5a185-108">Il contratto di progetto aiuta anche a garantire una procedura di fatturazione coerente per ogni sottoprogetto in una struttura di progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="5a185-109">Ogni progetto che verrà fatturato deve essere associato a un contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="5a185-110">Le impostazioni per un contratto di progetto si applicano a tutti i progetti e sottoprogetti associati a quel contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="5a185-111">Un contratto di progetto può specificare una o più fonti di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="5a185-112">Pertanto, è possibile suddividere la fatturazione tra più finanziatori, impostare limiti di finanziamento in modo che le fonti di finanziamento non vengano fatturate per più di un importo specificato e configurare le regole di finanziamento per l'addebito delle spese.</span><span class="sxs-lookup"><span data-stu-id="5a185-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="5a185-113">Finanziamenti per contratti a progetto</span><span class="sxs-lookup"><span data-stu-id="5a185-113">Funding for project contracts</span></span>
<span data-ttu-id="5a185-114">Alcuni contratti di progetto specificano che più parti condividono la responsabilità del finanziamento dei costi del progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="5a185-115">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="5a185-115">Here are some examples:</span></span>

-   <span data-ttu-id="5a185-116">Un grande cliente che ha più divisioni richiede che il finanziamento di un progetto sia suddiviso per divisione.</span><span class="sxs-lookup"><span data-stu-id="5a185-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="5a185-117">La tua azienda condivide i costi di un grande progetto con un'organizzazione esterna.</span><span class="sxs-lookup"><span data-stu-id="5a185-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="5a185-118">Un progetto stradale è cofinanziato da due comuni.</span><span class="sxs-lookup"><span data-stu-id="5a185-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="5a185-119">Un progetto per un ponte è finanziato da una sovvenzione governativa e da una società privata.</span><span class="sxs-lookup"><span data-stu-id="5a185-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="5a185-120">In Dynamics 365 Finance, puoi suddividere la fatturazione per una singola transazione o un intero progetto tra più clienti, sovvenzioni o organizzazioni.</span><span class="sxs-lookup"><span data-stu-id="5a185-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="5a185-121">Nei progetti che hanno più finanziatori, tutte le parti che contribuiscono al finanziamento di un progetto di finanziamento avanzato sono chiamate fonti di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="5a185-122">Dopo che un cliente, un'organizzazione o una sovvenzione è stata definita come fonte di finanziamento, può essere assegnata a una o più regole di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="5a185-123">Le regole di finanziamento contengono i criteri che determinano il modo in cui gli addebiti vengono assegnati alle varie fonti di finanziamento per un progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="5a185-124">Poiché gli articoli in magazzino, come quelli che compaiono nelle richieste di acquisto e negli ordini di acquisto, non possono essere suddivisi, l'importo del costo non può essere suddiviso tra più fonti di finanziamento al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5a185-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="5a185-125">Pertanto, il valore della fonte di finanziamento rimane 0 (zero) fino a quando non viene registrata l'uscita di magazzino.</span><span class="sxs-lookup"><span data-stu-id="5a185-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="5a185-126">Quando viene registrata l'uscita di magazzino, l'importo del costo viene distribuito in base alle regole di distribuzione del conto per il progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="5a185-127">Di seguito sono riportati alcuni passaggi che puoi eseguire per semplificare la suddivisione della fatturazione tra più fonti di finanziamento:</span><span class="sxs-lookup"><span data-stu-id="5a185-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="5a185-128">Specifica che tutte le transazioni immesse per un progetto utilizzano la stessa valuta di vendita del contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="5a185-129">Configura i limiti di finanziamento, in modo che a una fonte di finanziamento non venga fatturato più di un importo specificato per un progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="5a185-130">Configura le regole di finanziamento e i limiti di finanziamento per ogni ruolo di lavoro, articolo, categoria, gruppo di categorie e tipo di transazione (o per tutti i tipi di transazione).</span><span class="sxs-lookup"><span data-stu-id="5a185-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="5a185-131">Seleziona le date di inizio e di fine facoltative per definire il periodo di validità di ciascuna regola di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="5a185-132">Specifica la percentuale di cui è responsabile ciascuna fonte di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="5a185-133">Specifica quale fonte di finanziamento è responsabile dell'arrotondamento delle differenze causate dai calcoli di allocazione dei finanziamenti.</span><span class="sxs-lookup"><span data-stu-id="5a185-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="5a185-134">Configura le regole che determinano il modo in cui i costi del progetto vengono fatturati ai clienti esterni e addebitati alle organizzazioni interne.</span><span class="sxs-lookup"><span data-stu-id="5a185-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="5a185-135">Registra le transazioni in un conto di finanziamento sospeso fino a quando non è possibile ottenere finanziamenti aggiuntivi o finché non decidi di sostenere i costi internamente.</span><span class="sxs-lookup"><span data-stu-id="5a185-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="5a185-136">Per determinare quale gruppo fiscale associare a una transazione, nel progetto viene eseguita la ricerca di un'assegnazione di gruppo fiscale.</span><span class="sxs-lookup"><span data-stu-id="5a185-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="5a185-137">Se non è stata effettuata alcuna assegnazione di gruppo fiscale a livello di progetto, viene eseguita una ricerca nel contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="5a185-138">Esempio: più fonti di finanziamento (semplice)</span><span class="sxs-lookup"><span data-stu-id="5a185-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="5a185-139">La tabella seguente fornisce gli scenari per la gestione dell'allocazione dei finanziamenti tra più fonti di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="5a185-140">Questi scenari si basano sui seguenti presupposti:</span><span class="sxs-lookup"><span data-stu-id="5a185-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="5a185-141">Le impostazioni di priorità vengono prese in considerazione nell'allocazione dei fondi prima che vengano applicati altri criteri delle regole di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="5a185-142">Non è stato specificato alcun intervallo di date per definire il periodo in cui la regola di finanziamento è valida.</span><span class="sxs-lookup"><span data-stu-id="5a185-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a185-143"><strong>Scenario</strong></span><span class="sxs-lookup"><span data-stu-id="5a185-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="5a185-144"><strong>Fonte di finanziamento</strong></span><span class="sxs-lookup"><span data-stu-id="5a185-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="5a185-145"><strong>Percentuale di allocazione</strong></span><span class="sxs-lookup"><span data-stu-id="5a185-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="5a185-146"><strong>Priorità di allocazione</strong></span><span class="sxs-lookup"><span data-stu-id="5a185-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a185-147">Vuoi allocare i costi a una fonte di finanziamento finché i suoi fondi non sono esauriti, allocare i costi a una seconda fonte di finanziamento fino a quando i suoi fondi non sono esauriti e infine allocare i costi rimanenti a una terza fonte di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5a185-148">Fonte di　finanziamento　1</span><span class="sxs-lookup"><span data-stu-id="5a185-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="5a185-149">Fonte di　finanziamento　2</span><span class="sxs-lookup"><span data-stu-id="5a185-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="5a185-150">Fonte di　finanziamento　3</span><span class="sxs-lookup"><span data-stu-id="5a185-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a185-151">100%</span><span class="sxs-lookup"><span data-stu-id="5a185-151">100%</span></span></li>
<li><span data-ttu-id="5a185-152">100%</span><span class="sxs-lookup"><span data-stu-id="5a185-152">100%</span></span></li>
<li><span data-ttu-id="5a185-153">100%</span><span class="sxs-lookup"><span data-stu-id="5a185-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a185-154">1</span><span class="sxs-lookup"><span data-stu-id="5a185-154">1</span></span></li>
<li><span data-ttu-id="5a185-155">2</span><span class="sxs-lookup"><span data-stu-id="5a185-155">2</span></span></li>
<li><span data-ttu-id="5a185-156">3</span><span class="sxs-lookup"><span data-stu-id="5a185-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a185-157">Vuoi allocare il 75% dei costi a una fonte di finanziamento e il 25% a una seconda fonte di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="5a185-158">Quando una di queste fonti di finanziamento è esaurita, vuoi pagare i costi rimanenti da una terza fonte di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5a185-159">Fonte di　finanziamento　1</span><span class="sxs-lookup"><span data-stu-id="5a185-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="5a185-160">Fonte di　finanziamento　2</span><span class="sxs-lookup"><span data-stu-id="5a185-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="5a185-161">Fonte di　finanziamento　3</span><span class="sxs-lookup"><span data-stu-id="5a185-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a185-162">75%</span><span class="sxs-lookup"><span data-stu-id="5a185-162">75%</span></span></li>
<li><span data-ttu-id="5a185-163">25%</span><span class="sxs-lookup"><span data-stu-id="5a185-163">25%</span></span></li>
<li><span data-ttu-id="5a185-164">100%</span><span class="sxs-lookup"><span data-stu-id="5a185-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a185-165">1</span><span class="sxs-lookup"><span data-stu-id="5a185-165">1</span></span></li>
<li><span data-ttu-id="5a185-166">1</span><span class="sxs-lookup"><span data-stu-id="5a185-166">1</span></span></li>
<li><span data-ttu-id="5a185-167">2</span><span class="sxs-lookup"><span data-stu-id="5a185-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a185-168">Vuoi allocare il 75% dei costi a una fonte di finanziamento e il 25% a una seconda fonte di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="5a185-169">Quando una di queste fonti di finanziamento è esaurita, vuoi dividere i costi rimanenti tra una terza e una quarta fonte di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5a185-170">Fonte di　finanziamento　1</span><span class="sxs-lookup"><span data-stu-id="5a185-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="5a185-171">Fonte di　finanziamento　2</span><span class="sxs-lookup"><span data-stu-id="5a185-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="5a185-172">Fonte di　finanziamento　3</span><span class="sxs-lookup"><span data-stu-id="5a185-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="5a185-173">Fonte di　finanziamento　4</span><span class="sxs-lookup"><span data-stu-id="5a185-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a185-174">75%</span><span class="sxs-lookup"><span data-stu-id="5a185-174">75%</span></span></li>
<li><span data-ttu-id="5a185-175">25%</span><span class="sxs-lookup"><span data-stu-id="5a185-175">25%</span></span></li>
<li><span data-ttu-id="5a185-176">50%</span><span class="sxs-lookup"><span data-stu-id="5a185-176">50%</span></span></li>
<li><span data-ttu-id="5a185-177">50%</span><span class="sxs-lookup"><span data-stu-id="5a185-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a185-178">1</span><span class="sxs-lookup"><span data-stu-id="5a185-178">1</span></span></li>
<li><span data-ttu-id="5a185-179">1</span><span class="sxs-lookup"><span data-stu-id="5a185-179">1</span></span></li>
<li><span data-ttu-id="5a185-180">2</span><span class="sxs-lookup"><span data-stu-id="5a185-180">2</span></span></li>
<li><span data-ttu-id="5a185-181">2</span><span class="sxs-lookup"><span data-stu-id="5a185-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a185-182">Vuoi allocare il primo 25% dei costi a una fonte di finanziamento e il resto a una seconda fonte di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5a185-183">Fonte di　finanziamento　1</span><span class="sxs-lookup"><span data-stu-id="5a185-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="5a185-184">Fonte di　finanziamento　2</span><span class="sxs-lookup"><span data-stu-id="5a185-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a185-185">25%</span><span class="sxs-lookup"><span data-stu-id="5a185-185">25%</span></span></li>
<li><span data-ttu-id="5a185-186">100%</span><span class="sxs-lookup"><span data-stu-id="5a185-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a185-187">1</span><span class="sxs-lookup"><span data-stu-id="5a185-187">1</span></span></li>
<li><span data-ttu-id="5a185-188">2</span><span class="sxs-lookup"><span data-stu-id="5a185-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="5a185-189">Esempio: più fonti di finanziamento (complessa)</span><span class="sxs-lookup"><span data-stu-id="5a185-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="5a185-190">Hai tre fonti di finanziamento che desideri utilizzare nel seguente ordine:</span><span class="sxs-lookup"><span data-stu-id="5a185-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="5a185-191">Utilizza la fonte di finanziamento 2 e la fonte di finanziamento 3 allo stesso modo fino a quando la fonte di finanziamento 2 non è esaurita.</span><span class="sxs-lookup"><span data-stu-id="5a185-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="5a185-192">Continua a utilizzare la fonte di finanziamento 3 fino all'esaurimento.</span><span class="sxs-lookup"><span data-stu-id="5a185-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="5a185-193">Utilizza la fonte di finanziamento 1 dopo che la fonte di finanziamento 3 è esaurita.</span><span class="sxs-lookup"><span data-stu-id="5a185-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="5a185-194">Per realizzare questo obiettivo, devi fare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="5a185-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="5a185-195">Configura i limiti di finanziamento per la fonte di finanziamento 2 e la fonte di finanziamento 3, per i rispettivi importi.</span><span class="sxs-lookup"><span data-stu-id="5a185-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="5a185-196">Creare le regole di finanziamento seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a185-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="5a185-197">Regola 1 (Priorità 1): Assegna il 50% delle transazioni alla fonte di finanziamento 2 e il 50% alla fonte di finanziamento 3.</span><span class="sxs-lookup"><span data-stu-id="5a185-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="5a185-198">Regola 2 (Priorità 2): Assegna il 100% delle transazioni alla fonte di finanziamento 3.</span><span class="sxs-lookup"><span data-stu-id="5a185-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="5a185-199">Regola 3 (Priorità 3): Assegna il 100% delle transazioni alla fonte di finanziamento 1.</span><span class="sxs-lookup"><span data-stu-id="5a185-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="5a185-200">Questa configurazione funziona perché le transazioni vengono verificate a fronte di regole e limiti per determinare se qualcuno di essi si applica alla transazione.</span><span class="sxs-lookup"><span data-stu-id="5a185-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="5a185-201">Se alla transazione non si applicano regole o limiti specifici, si applica la regola Tutte le transazioni.</span><span class="sxs-lookup"><span data-stu-id="5a185-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="5a185-202">La regola Tutte le transazioni corrisponde a tutte le transazioni.</span><span class="sxs-lookup"><span data-stu-id="5a185-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="5a185-203">Se viene trovata una regola che corrisponde a una transazione, la percentuale che è stata assegnata in quella regola viene applicata per prima, ma solo dopo che le corrispondenze sono state verificate rispetto ai limiti impostati.</span><span class="sxs-lookup"><span data-stu-id="5a185-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="5a185-204">Se è stato raggiunto un limite e i fondi di una fonte di finanziamento sono esauriti, la regola di finanziamento associata al limite di finanziamento viene ignorata e il programma verifica la regola successiva che si applica.</span><span class="sxs-lookup"><span data-stu-id="5a185-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="5a185-205">In alcuni casi, solo una parte di una transazione può essere allocata in base a una regola.</span><span class="sxs-lookup"><span data-stu-id="5a185-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="5a185-206">Ciò potrebbe accadere perché viene raggiunto un limite quando la transazione viene allocata.</span><span class="sxs-lookup"><span data-stu-id="5a185-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="5a185-207">In questo caso, in base a tale regola viene assegnato solo un determinato importo, ad esempio il 50 percento a ciascuna fonte di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="5a185-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="5a185-208">Questo è il caso della regola 1, descritta in precedenza in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="5a185-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="5a185-209">Il resto viene assegnato in base alla regola successiva nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="5a185-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="5a185-210">La tabella seguente esamina questo scenario in maggior dettaglio.</span><span class="sxs-lookup"><span data-stu-id="5a185-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a185-211"><strong>Obiettivo mirato</strong></span><span class="sxs-lookup"><span data-stu-id="5a185-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="5a185-212"><strong>Dettagli</strong></span><span class="sxs-lookup"><span data-stu-id="5a185-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a185-213">Regole di finanziamento</span><span class="sxs-lookup"><span data-stu-id="5a185-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="5a185-214">Regola 1 (priorità 1): tutte le transazioni.</span><span class="sxs-lookup"><span data-stu-id="5a185-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="5a185-215">Effettua l'allocazione alla fonte di finanziamento 2 al 50% e la fonte di finanziamento 3 al 50%.</span><span class="sxs-lookup"><span data-stu-id="5a185-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="5a185-216">Regola 2 (priorità 2): tutte le transazioni.</span><span class="sxs-lookup"><span data-stu-id="5a185-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="5a185-217">Assegna la fonte di finanziamento 3 al 100%.</span><span class="sxs-lookup"><span data-stu-id="5a185-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="5a185-218">Regola 3 (priorità 2): tutte le transazioni.</span><span class="sxs-lookup"><span data-stu-id="5a185-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="5a185-219">Assegna la fonte di finanziamento 1 al 100%.</span><span class="sxs-lookup"><span data-stu-id="5a185-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a185-220">Limiti di finanziamento</span><span class="sxs-lookup"><span data-stu-id="5a185-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="5a185-221">Limite fonte di finanziamento 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="5a185-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="5a185-222">Limite fonte di finanziamento 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="5a185-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="5a185-223">Limite fonte di finanziamento 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="5a185-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a185-224">Transazione 1</span><span class="sxs-lookup"><span data-stu-id="5a185-224">Transaction 1</span></span></td>
<td><span data-ttu-id="5a185-225"><strong>Importo transazione:</strong> 100,00 <strong>Finanziamento:</strong> la transazione viene pagata solo in base alla regola 1, perché la transazione è completamente pagata dopo l'applicazione della regola 1.</span><span class="sxs-lookup"><span data-stu-id="5a185-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="5a185-226">La transazione è finanziata equamente tra la fonte di finanziamento 2 e la fonte di finanziamento 3.</span><span class="sxs-lookup"><span data-stu-id="5a185-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="5a185-227">Fonte di finanziamento 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="5a185-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="5a185-228">Fonte di finanziamento 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="5a185-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a185-229">Transazione 2</span><span class="sxs-lookup"><span data-stu-id="5a185-229">Transaction 2</span></span></td>
<td><span data-ttu-id="5a185-230"><strong>Importo transazione:</strong> 5.000,00 <strong>Finanziamento:</strong> la transazione viene pagata secondo tutte e tre le regole.</span><span class="sxs-lookup"><span data-stu-id="5a185-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="5a185-231"><strong>Regola 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="5a185-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="5a185-232">Fonte di finanziamento 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="5a185-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="5a185-233">Fonte di finanziamento 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="5a185-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="5a185-234">
<strong>Regola 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="5a185-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="5a185-235">Fonte di finanziamento 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="5a185-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="5a185-236">
<strong>Regola 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="5a185-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="5a185-237">Fonte di finanziamento 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="5a185-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a185-238">Fondi totali distribuiti per ciascuna fonte di finanziamento</span><span class="sxs-lookup"><span data-stu-id="5a185-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="5a185-239">Fonte di finanziamento 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="5a185-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="5a185-240">Fonte di finanziamento 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="5a185-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="5a185-241">Fonte di finanziamento 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="5a185-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="5a185-242">Regole di fatturazione</span><span class="sxs-lookup"><span data-stu-id="5a185-242">Billing rules</span></span>
<span data-ttu-id="5a185-243">Quando negozi un contratto di progetto con un cliente, definisci come e quando puoi fatturare al cliente il lavoro su un progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="5a185-244">Dopo aver configurato il contratto di progetto e il progetto, puoi configurare le regole di fatturazione per il progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="5a185-245">Le regole di fatturazione si basano sui termini del progetto specificati nel contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="5a185-246">Le regole di fatturazione che puoi creare dipendono dai termini del contratto di progetto e dal tipo di progetto, ad esempio Tempo e materiale o Prezzo fisso, che associ alla regola di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="5a185-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="5a185-247">Puoi creare più di una regola di fatturazione per un contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="5a185-248">Puoi anche assegnare una regola di fatturazione a più progetti associati allo stesso contratto di progetto e con termini di fatturazione simili.</span><span class="sxs-lookup"><span data-stu-id="5a185-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="5a185-249">Puoi configurare i seguenti tipi di regole di fatturazione:</span><span class="sxs-lookup"><span data-stu-id="5a185-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="5a185-250">**Unità di consegna**: fattura un cliente quando completi un'unità di consegna.</span><span class="sxs-lookup"><span data-stu-id="5a185-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="5a185-251">Le unità di consegna vengono definite nel contratto.</span><span class="sxs-lookup"><span data-stu-id="5a185-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="5a185-252">**Progresso**: fattura un cliente quando completi una determinata percentuale del progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="5a185-253">Puoi configurare una regola di fatturazione per calcolare automaticamente la percentuale di lavoro completato oppure è possibile calcolare manualmente la percentuale di lavoro completato e l'importo da fatturare al cliente.</span><span class="sxs-lookup"><span data-stu-id="5a185-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="5a185-254">**A fasi**: fattura a un cliente l'intero importo di una fase del progetto quando viene raggiunta.</span><span class="sxs-lookup"><span data-stu-id="5a185-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="5a185-255">**Commissione**: fattura un cliente per i tuoi servizi più una commissione di gestione, che in genere è una percentuale del costo dei servizi.</span><span class="sxs-lookup"><span data-stu-id="5a185-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="5a185-256">**Tempo e materiale**: fattura a un cliente il valore del tempo e dei materiali utilizzati in un progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="5a185-257">Per tutti i tipi di regole di fatturazione, puoi specificare una percentuale di conservazione che viene detratta dalle fatture del cliente fino a quando un progetto non raggiunge una fase concordata.</span><span class="sxs-lookup"><span data-stu-id="5a185-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="5a185-258">La percentuale di trattenuta del pagamento è specificata nel contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="5a185-259">L'importo viene calcolato in base al e sottratto dal valore totale delle righe in una fattura cliente.</span><span class="sxs-lookup"><span data-stu-id="5a185-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="5a185-260">Per le regole di fatturazione **Tempo e materiale** e **Progresso**, puoi assegnare categorie addebitabili.</span><span class="sxs-lookup"><span data-stu-id="5a185-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="5a185-261">Le categorie addebitabili indicano le transazioni che dovrebbero essere incluse nelle fatture dei clienti.</span><span class="sxs-lookup"><span data-stu-id="5a185-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="5a185-262">Quando sei pronto per fatturare al cliente, l'importo da fatturare per il progetto viene calcolato in base alle regole di fatturazione e viene generata una proposta di fattura progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="5a185-263">Le sezioni seguenti forniscono esempi che mostrano come configurare e gestire le regole di fatturazione per un progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="5a185-264">Esempio: crea una regola di fatturazione basata sul numero di unità consegnate</span><span class="sxs-lookup"><span data-stu-id="5a185-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="5a185-265">La tua organizzazione stipula un accordo per fornire un totale di cinque sessioni di formazione ai dipendenti di un cliente al costo di 10.000 per sessione di formazione.</span><span class="sxs-lookup"><span data-stu-id="5a185-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="5a185-266">Fatturi al cliente dopo ogni sessione di formazione.</span><span class="sxs-lookup"><span data-stu-id="5a185-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="5a185-267">Quando configuri le regole di fatturazione per il contratto, utilizzi i seguenti valori:</span><span class="sxs-lookup"><span data-stu-id="5a185-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="5a185-268">L'unità di consegna è una sessione di formazione.</span><span class="sxs-lookup"><span data-stu-id="5a185-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="5a185-269">Il prezzo unitario è 10.000 per sessione di formazione.</span><span class="sxs-lookup"><span data-stu-id="5a185-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="5a185-270">Il numero totale di unità è di cinque sessioni di formazione.</span><span class="sxs-lookup"><span data-stu-id="5a185-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="5a185-271">Dopo aver completato una sessione di formazione, puoi creare una fattura per 10.000, per la prima unità consegnata, e inviare la fattura al cliente.</span><span class="sxs-lookup"><span data-stu-id="5a185-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="5a185-272">Esempio: crea una regola di fatturazione basata su una percentuale specificata di completamento del progetto (calcolo manuale)</span><span class="sxs-lookup"><span data-stu-id="5a185-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="5a185-273">La tua organizzazione, una società di consulenza software, stipula un accordo con un cliente per sviluppare parte di un prodotto che il cliente sta sviluppando.</span><span class="sxs-lookup"><span data-stu-id="5a185-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="5a185-274">La tua organizzazione accetta di fornire il codice software per un periodo di sei mesi.</span><span class="sxs-lookup"><span data-stu-id="5a185-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="5a185-275">Il cliente accetta di pagare alla tua organizzazione un totale di 100.000 per il lavoro.</span><span class="sxs-lookup"><span data-stu-id="5a185-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="5a185-276">Crei una regola di fatturazione per fatturare al cliente in base alla percentuale di lavoro completata sul progetto, come specificato nel contratto.</span><span class="sxs-lookup"><span data-stu-id="5a185-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="5a185-277">Alla fine del primo mese, incontri il cliente per determinare la percentuale di lavoro completato.</span><span class="sxs-lookup"><span data-stu-id="5a185-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="5a185-278">Dopo che tu e il cliente avete esaminato il progetto, decidete che il progetto è stato completato al 15%.</span><span class="sxs-lookup"><span data-stu-id="5a185-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="5a185-279">Crei una fattura per 15.000 (15 percento di 100.000) e la invii al cliente.</span><span class="sxs-lookup"><span data-stu-id="5a185-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="5a185-280">Esempio: crea una regola di fatturazione basata su una percentuale specificata di completamento del progetto (calcolo automatico)</span><span class="sxs-lookup"><span data-stu-id="5a185-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="5a185-281">La tua organizzazione, una società di sviluppo software, accetta di sviluppare un pacchetto di contabilità salari per un cliente per 30.000.</span><span class="sxs-lookup"><span data-stu-id="5a185-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="5a185-282">Il cliente accetta di pagare alla tua organizzazione in base alla percentuale di lavoro completato.</span><span class="sxs-lookup"><span data-stu-id="5a185-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="5a185-283">Stimi che i costi del progetto siano 20.000.</span><span class="sxs-lookup"><span data-stu-id="5a185-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="5a185-284">Il contratto di progetto specifica le categorie di lavoro che utilizzi nel processo di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="5a185-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="5a185-285">Configuri regole di fatturazione che calcolano automaticamente gli importi delle fatture per la percentuale di lavoro completata per ciascuna categoria.</span><span class="sxs-lookup"><span data-stu-id="5a185-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="5a185-286">Hai configurato un budget per ogni categoria:</span><span class="sxs-lookup"><span data-stu-id="5a185-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="5a185-287">**Sviluppo**: costo di 15.000 e ricavi di 20.000</span><span class="sxs-lookup"><span data-stu-id="5a185-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="5a185-288">**Installazione**: costo di 5.000 e ricavi di 10.000</span><span class="sxs-lookup"><span data-stu-id="5a185-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="5a185-289">Quando crei una fattura cliente per la prima volta, l'importo della fattura viene calcolato automaticamente in base alle seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="5a185-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="5a185-290">Dopo un mese, il lavoratore del progetto invia una scheda attività per il progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="5a185-291">Il costo delle ore del lavoratore è di 5.000 per lo sviluppo e 1.000 per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="5a185-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="5a185-292">Il lavoro di sviluppo è completato al 33% (5.000 costi effettivi/15.000 costi a budget) e il lavoro di installazione è completato al 20% (1.000 costi effettivi/5.000 costi a budget).</span><span class="sxs-lookup"><span data-stu-id="5a185-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="5a185-293">L'importo della fattura di 8.667 viene calcolato automaticamente (33 percento di 20.000 + 20 percento di 10.000).</span><span class="sxs-lookup"><span data-stu-id="5a185-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="5a185-294">Crei una fattura per 8.667 e la invii al cliente.</span><span class="sxs-lookup"><span data-stu-id="5a185-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="5a185-295">Esempio: crea una regola di fatturazione basata su fasi concordate</span><span class="sxs-lookup"><span data-stu-id="5a185-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="5a185-296">La tua organizzazione, una società di consulenza gestionale, accetta di condurre ricerche di mercato per un prodotto di consumo che il cliente intende vendere.</span><span class="sxs-lookup"><span data-stu-id="5a185-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="5a185-297">Il cliente accetta di utilizzare i tuoi servizi per un periodo di tre mesi, a partire da marzo, e accetta di pagare alla tua organizzazione 50.000.</span><span class="sxs-lookup"><span data-stu-id="5a185-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="5a185-298">Il progetto ha tre fasi:</span><span class="sxs-lookup"><span data-stu-id="5a185-298">The project has three milestones:</span></span>

-   <span data-ttu-id="5a185-299">Fase 1: raccolta dei dati sui consumatori - 31 marzo</span><span class="sxs-lookup"><span data-stu-id="5a185-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="5a185-300">Fase 2: analisi dei dati sui consumatori - 30 aprile</span><span class="sxs-lookup"><span data-stu-id="5a185-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="5a185-301">Fase 3: presentazione di una proposta di fattibilità del prodotto - 31 maggio</span><span class="sxs-lookup"><span data-stu-id="5a185-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="5a185-302">Il cliente accetta di pagare alla tua organizzazione 10.000 per la prima fase, 20.000 per la seconda e 20.000 per la terza.</span><span class="sxs-lookup"><span data-stu-id="5a185-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="5a185-303">Quando configuri il contratto di progetto, accetti di fatturare al cliente in base alla fase che hai completato.</span><span class="sxs-lookup"><span data-stu-id="5a185-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="5a185-304">La configurazione della regola di fatturazione include i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="5a185-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="5a185-305">Definisci le fasi del progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-305">Define the project milestones.</span></span>
-   <span data-ttu-id="5a185-306">Definisci l'importo da fatturare al cliente al completamento di ogni fase.</span><span class="sxs-lookup"><span data-stu-id="5a185-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="5a185-307">Quando la prima fase viene completata il 31 marzo, contrassegni la fase come completata, quindi crei una fattura per 10.000 e la invii al cliente.</span><span class="sxs-lookup"><span data-stu-id="5a185-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="5a185-308">Non puoi creare una fattura per una fase finché non è stata contrassegnata come completata.</span><span class="sxs-lookup"><span data-stu-id="5a185-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="5a185-309">Esempio: crea una regola di fatturazione basata sui servizi più una commissione di gestione</span><span class="sxs-lookup"><span data-stu-id="5a185-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="5a185-310">La tua organizzazione, una società di consulenza gestionale, accetta di condurre ricerche di mercato per valutare la fattibilità di un prodotto che il cliente, una società di vendita al dettaglio, sta sviluppando.</span><span class="sxs-lookup"><span data-stu-id="5a185-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="5a185-311">I termini dell'accordo specificano che fornirai i servizi dei tuoi primi tre consulenti di gestione, che condurranno la ricerca in base al tempo e ai materiali.</span><span class="sxs-lookup"><span data-stu-id="5a185-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="5a185-312">Il cliente accetta di pagare 100 all'ora, più una commissione di gestione del 10% per le ore di consulenza addebitate al progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="5a185-313">Quando configuri il contratto di progetto, crea una regola di fatturazione per aggiungere una commissione di gestione del 10% alle ore di consulenza addebitate al progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="5a185-314">Quando crei una fattura per il cliente, al cliente viene addebitata una commissione di gestione del 10% più il costo delle ore di consulenza.</span><span class="sxs-lookup"><span data-stu-id="5a185-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="5a185-315">Ad esempio, se i tre consulenti hanno lavorato un totale di 200 ore al progetto, viene creata una fattura per 22.000 in base al seguente calcolo:</span><span class="sxs-lookup"><span data-stu-id="5a185-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="5a185-316">200 ore a 100 all'ora = 20.000</span><span class="sxs-lookup"><span data-stu-id="5a185-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="5a185-317">Commissione di gestione del 10% = 2.000</span><span class="sxs-lookup"><span data-stu-id="5a185-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="5a185-318">Importo totale fattura = 22.000</span><span class="sxs-lookup"><span data-stu-id="5a185-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="5a185-319">Se le commissioni sono imponibili a un cliente e si seleziona una fascia IVA nel contratto di progetto, la fascia IVA viene inserita automaticamente in una regola di fatturazione per le commissioni.</span><span class="sxs-lookup"><span data-stu-id="5a185-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="5a185-320">Esempio: crea una regola di fatturazione per il valore del tempo e dei materiali</span><span class="sxs-lookup"><span data-stu-id="5a185-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="5a185-321">La tua organizzazione, una società di consulenza software, accetta di fornire cinque consulenti tecnici per lavorare su un progetto di sviluppo software per un cliente per i prossimi sei mesi.</span><span class="sxs-lookup"><span data-stu-id="5a185-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="5a185-322">Il cliente si impegna a pagare 150 per ogni ora di consulenza, più il costo delle forniture per ufficio.</span><span class="sxs-lookup"><span data-stu-id="5a185-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="5a185-323">La tua organizzazione invia una fattura al cliente alla fine di ogni mese.</span><span class="sxs-lookup"><span data-stu-id="5a185-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="5a185-324">Quando configuri il contratto di progetto, accetti di fatturare al cliente ogni mese il tempo e i materiali relativi al progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="5a185-325">Crei una regola di fatturazione che include le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="5a185-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="5a185-326">La durata del contratto è di sei mesi.</span><span class="sxs-lookup"><span data-stu-id="5a185-326">The contract period is six months.</span></span>
-   <span data-ttu-id="5a185-327">Il tempo di consulenza è calcolato a una tariffa di 150 all'ora.</span><span class="sxs-lookup"><span data-stu-id="5a185-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="5a185-328">Le forniture per ufficio vengono fatturate al costo e il costo totale del progetto non deve superare 10.000.</span><span class="sxs-lookup"><span data-stu-id="5a185-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="5a185-329">Crei una fattura cliente alla fine di ogni mese di calendario durante il progetto.</span><span class="sxs-lookup"><span data-stu-id="5a185-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="5a185-330">Durante il primo mese, i consulenti sul progetto registrano un totale di 800 ore.</span><span class="sxs-lookup"><span data-stu-id="5a185-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="5a185-331">Il costo delle forniture per ufficio addebitate al progetto è di 2.000.</span><span class="sxs-lookup"><span data-stu-id="5a185-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="5a185-332">Pertanto, alla fine del mese, crei una fattura per 122.000, che viene calcolata come 800 ore a 150 l'ora, più 2.000 per le forniture per ufficio.</span><span class="sxs-lookup"><span data-stu-id="5a185-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



