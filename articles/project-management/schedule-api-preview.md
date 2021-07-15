---
title: Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione
description: Questo argomento fornisce informazioni ed esempi per l'utilizzo delle API di pianificazione del progetto.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293232"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="28bcb-103">Utilizzare le API di pianificazione del progetto per eseguire operazioni con entità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="28bcb-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="28bcb-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="28bcb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="28bcb-105">L'intera funzionalità, o una sua parte, descritta in questo articolo è disponibile nella versione di anteprima.</span><span class="sxs-lookup"><span data-stu-id="28bcb-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="28bcb-106">Il contenuto e la funzionalità sono soggetti a modifiche.</span><span class="sxs-lookup"><span data-stu-id="28bcb-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="28bcb-107">Entità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="28bcb-107">Scheduling entities</span></span>

<span data-ttu-id="28bcb-108">Le API di pianificazione del progetto offrono la possibilità di eseguire operazioni di creazione, aggiornamento ed eliminazione con **entità di pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="28bcb-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="28bcb-109">Queste entità vengono gestite tramite il motore di pianificazione in Project per il Web.</span><span class="sxs-lookup"><span data-stu-id="28bcb-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="28bcb-110">Le operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione** erano limitate nelle versioni precedenti di Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="28bcb-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="28bcb-111">La tabella seguente fornisce un elenco completo delle entità di pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="28bcb-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="28bcb-112">Nome dell'entità</span><span class="sxs-lookup"><span data-stu-id="28bcb-112">Entity name</span></span>  | <span data-ttu-id="28bcb-113">Nome logico entità</span><span class="sxs-lookup"><span data-stu-id="28bcb-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="28bcb-114">Project</span><span class="sxs-lookup"><span data-stu-id="28bcb-114">Project</span></span> | <span data-ttu-id="28bcb-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="28bcb-115">msdyn_project</span></span> |
| <span data-ttu-id="28bcb-116">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-116">Project Task</span></span>  | <span data-ttu-id="28bcb-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="28bcb-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="28bcb-118">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-118">Project Task Dependency</span></span>  | <span data-ttu-id="28bcb-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="28bcb-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="28bcb-120">Assegnazione risorse</span><span class="sxs-lookup"><span data-stu-id="28bcb-120">Resource Assignment</span></span> | <span data-ttu-id="28bcb-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="28bcb-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="28bcb-122">Bucket di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-122">Project Bucket</span></span>  | <span data-ttu-id="28bcb-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="28bcb-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="28bcb-124">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-124">Project Team Member</span></span> | <span data-ttu-id="28bcb-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="28bcb-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="28bcb-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="28bcb-126">OperationSet</span></span>

<span data-ttu-id="28bcb-127">OperationSet è un modello di unità di lavoro che può essere utilizzato quando in una transazione devono essere elaborate diverse richieste che influiscono sulla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="28bcb-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="28bcb-128">API di pianificazione di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-128">Project schedule APIs</span></span>

<span data-ttu-id="28bcb-129">Di seguito è riportato un elenco delle API di pianificazione del progetto correnti.</span><span class="sxs-lookup"><span data-stu-id="28bcb-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="28bcb-130">**msdyn_CreateProjectV1**: questa API può essere utilizzata per creare un progetto.</span><span class="sxs-lookup"><span data-stu-id="28bcb-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="28bcb-131">Il progetto e il bucket di progetto predefinito vengono creati immediatamente.</span><span class="sxs-lookup"><span data-stu-id="28bcb-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="28bcb-132">**msdyn_CreateTeamMemberV1**: questa API può essere utilizzata per creare un membro del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="28bcb-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="28bcb-133">Il record Membro del team viene creato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="28bcb-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="28bcb-134">**msdyn_CreateOperationSetV1**: questa API può essere utilizzata per pianificare diverse richieste che devono essere eseguite in una transazione.</span><span class="sxs-lookup"><span data-stu-id="28bcb-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="28bcb-135">**msdyn_PSSCreateV1**: questa API può essere utilizzata per creare un'entità.</span><span class="sxs-lookup"><span data-stu-id="28bcb-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="28bcb-136">L'entità può essere una qualsiasi delle entità di pianificazione del progetto che supportano l'operazione di creazione.</span><span class="sxs-lookup"><span data-stu-id="28bcb-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="28bcb-137">**msdyn_PSSUpdateV1**: questa API può essere utilizzata per aggiornare un'entità.</span><span class="sxs-lookup"><span data-stu-id="28bcb-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="28bcb-138">L'entità può essere una qualsiasi delle entità di pianificazione del progetto che supportano l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="28bcb-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="28bcb-139">**msdyn_PSSDeleteV1**: questa API può essere utilizzata per eliminare un'entità.</span><span class="sxs-lookup"><span data-stu-id="28bcb-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="28bcb-140">L'entità può essere una qualsiasi delle entità di pianificazione del progetto che supportano l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="28bcb-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="28bcb-141">**msdyn_ExecuteOperationSetV1**: questa API viene utilizzata per eseguire tutte le operazioni in un determinato set di operazioni.</span><span class="sxs-lookup"><span data-stu-id="28bcb-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="28bcb-142">Utilizzo delle API di pianificazione del progetto con OperationSet</span><span class="sxs-lookup"><span data-stu-id="28bcb-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="28bcb-143">Poiché i record con **CreateProjectV1** e **CreateTeamMemberV1** vengono creati immediatamente, queste API non possono essere utilizzate direttamente in **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="28bcb-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="28bcb-144">Tuttavia, puoi utilizzare l'API per creare i record necessari, creare un **OperationSet**, quindi utilizzare questi record predefiniti in **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="28bcb-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="28bcb-145">Operazioni supportate</span><span class="sxs-lookup"><span data-stu-id="28bcb-145">Supported operations</span></span>

| <span data-ttu-id="28bcb-146">Entità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="28bcb-146">Scheduling entity</span></span> | <span data-ttu-id="28bcb-147">Creazione di</span><span class="sxs-lookup"><span data-stu-id="28bcb-147">Create</span></span> | <span data-ttu-id="28bcb-148">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="28bcb-148">Update</span></span> | <span data-ttu-id="28bcb-149">CANC</span><span class="sxs-lookup"><span data-stu-id="28bcb-149">Delete</span></span> | <span data-ttu-id="28bcb-150">Considerazioni importanti</span><span class="sxs-lookup"><span data-stu-id="28bcb-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="28bcb-151">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-151">Project task</span></span> | <span data-ttu-id="28bcb-152">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-152">Yes</span></span> | <span data-ttu-id="28bcb-153">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-153">Yes</span></span> | <span data-ttu-id="28bcb-154">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-154">Yes</span></span> | <span data-ttu-id="28bcb-155">Nessuna</span><span class="sxs-lookup"><span data-stu-id="28bcb-155">None</span></span> |
| <span data-ttu-id="28bcb-156">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-156">Project task dependency</span></span> | <span data-ttu-id="28bcb-157">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-157">Yes</span></span> | <span data-ttu-id="28bcb-158">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-158">Yes</span></span> | | <span data-ttu-id="28bcb-159">I record Dipendenza attività di progetto non vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="28bcb-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="28bcb-160">È invece possibile eliminare un vecchio record e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="28bcb-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="28bcb-161">Assegnazione risorse</span><span class="sxs-lookup"><span data-stu-id="28bcb-161">Resource assignment</span></span> | <span data-ttu-id="28bcb-162">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-162">Yes</span></span> | <span data-ttu-id="28bcb-163">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-163">Yes</span></span> | | <span data-ttu-id="28bcb-164">Le operazioni con i seguenti campi non sono supportate: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="28bcb-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="28bcb-165">I record Assegnazione risorse non vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="28bcb-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="28bcb-166">È invece possibile eliminare il vecchio record e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="28bcb-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="28bcb-167">Bucket di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-167">Project bucket</span></span> | <span data-ttu-id="28bcb-168">N/D</span><span class="sxs-lookup"><span data-stu-id="28bcb-168">N/A</span></span> | <span data-ttu-id="28bcb-169">N/D</span><span class="sxs-lookup"><span data-stu-id="28bcb-169">N/A</span></span> | <span data-ttu-id="28bcb-170">N/D</span><span class="sxs-lookup"><span data-stu-id="28bcb-170">N/A</span></span> | <span data-ttu-id="28bcb-171">Il bucket predefinito viene creato utilizzando l'API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="28bcb-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="28bcb-172">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-172">Project team member</span></span> | <span data-ttu-id="28bcb-173">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-173">Yes</span></span> | <span data-ttu-id="28bcb-174">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-174">Yes</span></span> | <span data-ttu-id="28bcb-175">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-175">Yes</span></span> | <span data-ttu-id="28bcb-176">Per l'operazione di creazione, utilizza l'API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="28bcb-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="28bcb-177">Project</span><span class="sxs-lookup"><span data-stu-id="28bcb-177">Project</span></span> | <span data-ttu-id="28bcb-178">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-178">Yes</span></span> | <span data-ttu-id="28bcb-179">Sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-179">Yes</span></span> | <span data-ttu-id="28bcb-180">N/D</span><span class="sxs-lookup"><span data-stu-id="28bcb-180">N/A</span></span> | <span data-ttu-id="28bcb-181">Le operazioni con i seguenti campi non sono supportate: : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.</span><span class="sxs-lookup"><span data-stu-id="28bcb-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="28bcb-182">Queste API possono essere chiamate con oggetti entità che includono campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="28bcb-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="28bcb-183">La proprietà ID è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="28bcb-183">The ID property is optional.</span></span> <span data-ttu-id="28bcb-184">Se fornita, il sistema tenta di utilizzarla e genera un'eccezione se non può essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="28bcb-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="28bcb-185">Se non è fornita, il sistema la genererà.</span><span class="sxs-lookup"><span data-stu-id="28bcb-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="28bcb-186">Campi con limitazioni</span><span class="sxs-lookup"><span data-stu-id="28bcb-186">Restricted fields</span></span>

<span data-ttu-id="28bcb-187">Le seguenti tabelle definiscono i campi con limitazioni **Crea** e **Modifica.**</span><span class="sxs-lookup"><span data-stu-id="28bcb-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="28bcb-188">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-188">Project task</span></span>

| <span data-ttu-id="28bcb-189">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="28bcb-189">**Logical name**</span></span>                       | <span data-ttu-id="28bcb-190">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-190">**Can create**</span></span> | <span data-ttu-id="28bcb-191">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="28bcb-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="28bcb-193">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-193">no</span></span>             | <span data-ttu-id="28bcb-194">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-194">no</span></span>               |
| <span data-ttu-id="28bcb-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="28bcb-196">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-196">no</span></span>             | <span data-ttu-id="28bcb-197">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-197">no</span></span>               |
| <span data-ttu-id="28bcb-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="28bcb-198">msdyn_actualend</span></span>                        | <span data-ttu-id="28bcb-199">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-199">no</span></span>             | <span data-ttu-id="28bcb-200">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-200">no</span></span>               |
| <span data-ttu-id="28bcb-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="28bcb-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="28bcb-202">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-202">no</span></span>             | <span data-ttu-id="28bcb-203">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-203">no</span></span>               |
| <span data-ttu-id="28bcb-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="28bcb-205">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-205">no</span></span>             | <span data-ttu-id="28bcb-206">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-206">no</span></span>               |
| <span data-ttu-id="28bcb-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="28bcb-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="28bcb-208">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-208">no</span></span>             | <span data-ttu-id="28bcb-209">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-209">no</span></span>               |
| <span data-ttu-id="28bcb-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="28bcb-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="28bcb-211">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-211">no</span></span>             | <span data-ttu-id="28bcb-212">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-212">no</span></span>               |
| <span data-ttu-id="28bcb-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="28bcb-214">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-214">no</span></span>             | <span data-ttu-id="28bcb-215">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-215">no</span></span>               |
| <span data-ttu-id="28bcb-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="28bcb-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="28bcb-217">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-217">no</span></span>             | <span data-ttu-id="28bcb-218">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-218">no</span></span>               |
| <span data-ttu-id="28bcb-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="28bcb-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="28bcb-220">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-220">no</span></span>             | <span data-ttu-id="28bcb-221">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-221">no</span></span>               |
| <span data-ttu-id="28bcb-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="28bcb-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="28bcb-223">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-223">no</span></span>             | <span data-ttu-id="28bcb-224">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-224">no</span></span>               |
| <span data-ttu-id="28bcb-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="28bcb-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="28bcb-226">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-226">no</span></span>             | <span data-ttu-id="28bcb-227">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-227">no</span></span>               |
| <span data-ttu-id="28bcb-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="28bcb-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="28bcb-229">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-229">no</span></span>             | <span data-ttu-id="28bcb-230">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-230">no</span></span>               |
| <span data-ttu-id="28bcb-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="28bcb-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="28bcb-232">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-232">no</span></span>             | <span data-ttu-id="28bcb-233">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-233">no</span></span>               |
| <span data-ttu-id="28bcb-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="28bcb-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="28bcb-235">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-235">no</span></span>             | <span data-ttu-id="28bcb-236">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-236">no</span></span>               |
| <span data-ttu-id="28bcb-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="28bcb-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="28bcb-238">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-238">no</span></span>             | <span data-ttu-id="28bcb-239">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-239">no</span></span>               |
| <span data-ttu-id="28bcb-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="28bcb-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="28bcb-241">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-241">no</span></span>             | <span data-ttu-id="28bcb-242">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-242">no</span></span>               |
| <span data-ttu-id="28bcb-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="28bcb-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="28bcb-244">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-244">no</span></span>             | <span data-ttu-id="28bcb-245">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-245">no</span></span>               |
| <span data-ttu-id="28bcb-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="28bcb-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="28bcb-247">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-247">no</span></span>             | <span data-ttu-id="28bcb-248">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-248">no</span></span>               |
| <span data-ttu-id="28bcb-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="28bcb-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="28bcb-250">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-250">no</span></span>             | <span data-ttu-id="28bcb-251">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-251">no</span></span>               |
| <span data-ttu-id="28bcb-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="28bcb-253">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-253">no</span></span>             | <span data-ttu-id="28bcb-254">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-254">no</span></span>               |
| <span data-ttu-id="28bcb-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="28bcb-256">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-256">no</span></span>             | <span data-ttu-id="28bcb-257">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-257">no</span></span>               |
| <span data-ttu-id="28bcb-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="28bcb-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="28bcb-259">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-259">no</span></span>             | <span data-ttu-id="28bcb-260">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-260">no</span></span>               |
| <span data-ttu-id="28bcb-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="28bcb-262">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-262">no</span></span>             | <span data-ttu-id="28bcb-263">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-263">no</span></span>               |
| <span data-ttu-id="28bcb-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="28bcb-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="28bcb-265">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-265">no</span></span>             | <span data-ttu-id="28bcb-266">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-266">no</span></span>               |
| <span data-ttu-id="28bcb-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="28bcb-267">msdyn_progress</span></span>                         | <span data-ttu-id="28bcb-268">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-268">no</span></span>             | <span data-ttu-id="28bcb-269">no (sì per P4W)</span><span class="sxs-lookup"><span data-stu-id="28bcb-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="28bcb-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="28bcb-271">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-271">no</span></span>             | <span data-ttu-id="28bcb-272">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-272">no</span></span>               |
| <span data-ttu-id="28bcb-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="28bcb-274">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-274">no</span></span>             | <span data-ttu-id="28bcb-275">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-275">no</span></span>               |
| <span data-ttu-id="28bcb-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="28bcb-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="28bcb-277">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-277">no</span></span>             | <span data-ttu-id="28bcb-278">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-278">no</span></span>               |
| <span data-ttu-id="28bcb-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="28bcb-280">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-280">no</span></span>             | <span data-ttu-id="28bcb-281">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-281">no</span></span>               |
| <span data-ttu-id="28bcb-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="28bcb-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="28bcb-283">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-283">no</span></span>             | <span data-ttu-id="28bcb-284">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-284">no</span></span>               |
| <span data-ttu-id="28bcb-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="28bcb-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="28bcb-286">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-286">no</span></span>             | <span data-ttu-id="28bcb-287">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-287">no</span></span>               |
| <span data-ttu-id="28bcb-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="28bcb-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="28bcb-289">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-289">no</span></span>             | <span data-ttu-id="28bcb-290">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-290">no</span></span>               |
| <span data-ttu-id="28bcb-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="28bcb-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="28bcb-292">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-292">no</span></span>             | <span data-ttu-id="28bcb-293">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-293">no</span></span>               |
| <span data-ttu-id="28bcb-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="28bcb-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="28bcb-295">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-295">no</span></span>             | <span data-ttu-id="28bcb-296">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-296">no</span></span>               |
| <span data-ttu-id="28bcb-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="28bcb-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="28bcb-298">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-298">no</span></span>             | <span data-ttu-id="28bcb-299">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-299">no</span></span>               |
| <span data-ttu-id="28bcb-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="28bcb-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="28bcb-301">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-301">no</span></span>             | <span data-ttu-id="28bcb-302">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-302">no</span></span>               |
| <span data-ttu-id="28bcb-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="28bcb-304">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-304">no</span></span>             | <span data-ttu-id="28bcb-305">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-305">no</span></span>               |
| <span data-ttu-id="28bcb-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="28bcb-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="28bcb-307">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-307">no</span></span>             | <span data-ttu-id="28bcb-308">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-308">no</span></span>               |
| <span data-ttu-id="28bcb-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="28bcb-310">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-310">no</span></span>             | <span data-ttu-id="28bcb-311">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-311">no</span></span>               |
| <span data-ttu-id="28bcb-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="28bcb-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="28bcb-313">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-313">no</span></span>             | <span data-ttu-id="28bcb-314">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-314">no</span></span>               |
| <span data-ttu-id="28bcb-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="28bcb-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="28bcb-316">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-316">no</span></span>             | <span data-ttu-id="28bcb-317">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-317">no</span></span>               |
| <span data-ttu-id="28bcb-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="28bcb-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="28bcb-319">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-319">no</span></span>             | <span data-ttu-id="28bcb-320">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-320">no</span></span>               |
| <span data-ttu-id="28bcb-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="28bcb-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="28bcb-322">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-322">no</span></span>             | <span data-ttu-id="28bcb-323">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-323">no</span></span>               |
| <span data-ttu-id="28bcb-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="28bcb-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="28bcb-325">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-325">no</span></span>             | <span data-ttu-id="28bcb-326">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-326">no</span></span>               |
| <span data-ttu-id="28bcb-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="28bcb-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="28bcb-328">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-328">no</span></span>             | <span data-ttu-id="28bcb-329">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-329">no</span></span>               |
| <span data-ttu-id="28bcb-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="28bcb-330">msdyn_summary</span></span>                          | <span data-ttu-id="28bcb-331">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-331">no</span></span>             | <span data-ttu-id="28bcb-332">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-332">no</span></span>               |
| <span data-ttu-id="28bcb-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="28bcb-334">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-334">no</span></span>             | <span data-ttu-id="28bcb-335">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-335">no</span></span>               |
| <span data-ttu-id="28bcb-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="28bcb-337">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-337">no</span></span>             | <span data-ttu-id="28bcb-338">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="28bcb-339">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-339">Project task dependency</span></span>

| <span data-ttu-id="28bcb-340">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="28bcb-340">**Logical name**</span></span>              | <span data-ttu-id="28bcb-341">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-341">**Can create**</span></span> | <span data-ttu-id="28bcb-342">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="28bcb-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="28bcb-343">msdyn_linktype</span></span>                | <span data-ttu-id="28bcb-344">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-344">no</span></span>             | <span data-ttu-id="28bcb-345">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-345">no</span></span>           |
| <span data-ttu-id="28bcb-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="28bcb-346">msdyn_linktypename</span></span>            | <span data-ttu-id="28bcb-347">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-347">no</span></span>             | <span data-ttu-id="28bcb-348">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-348">no</span></span>           |
| <span data-ttu-id="28bcb-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="28bcb-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="28bcb-350">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-350">yes</span></span>            | <span data-ttu-id="28bcb-351">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-351">no</span></span>           |
| <span data-ttu-id="28bcb-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="28bcb-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="28bcb-353">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-353">yes</span></span>            | <span data-ttu-id="28bcb-354">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-354">no</span></span>           |
| <span data-ttu-id="28bcb-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="28bcb-355">msdyn_project</span></span>                 | <span data-ttu-id="28bcb-356">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-356">yes</span></span>            | <span data-ttu-id="28bcb-357">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-357">no</span></span>           |
| <span data-ttu-id="28bcb-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="28bcb-358">msdyn_projectname</span></span>             | <span data-ttu-id="28bcb-359">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-359">yes</span></span>            | <span data-ttu-id="28bcb-360">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-360">no</span></span>           |
| <span data-ttu-id="28bcb-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="28bcb-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="28bcb-362">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-362">yes</span></span>            | <span data-ttu-id="28bcb-363">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-363">no</span></span>           |
| <span data-ttu-id="28bcb-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="28bcb-364">msdyn_successortask</span></span>           | <span data-ttu-id="28bcb-365">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-365">yes</span></span>            | <span data-ttu-id="28bcb-366">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-366">no</span></span>           |
| <span data-ttu-id="28bcb-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="28bcb-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="28bcb-368">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-368">yes</span></span>            | <span data-ttu-id="28bcb-369">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="28bcb-370">Assegnazione risorse</span><span class="sxs-lookup"><span data-stu-id="28bcb-370">Resource assignment</span></span>

| <span data-ttu-id="28bcb-371">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="28bcb-371">**Logical name**</span></span>             | <span data-ttu-id="28bcb-372">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-372">**Can create**</span></span> | <span data-ttu-id="28bcb-373">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="28bcb-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="28bcb-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="28bcb-375">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-375">yes</span></span>            | <span data-ttu-id="28bcb-376">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-376">no</span></span>           |
| <span data-ttu-id="28bcb-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="28bcb-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="28bcb-378">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-378">yes</span></span>            | <span data-ttu-id="28bcb-379">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-379">no</span></span>           |
| <span data-ttu-id="28bcb-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="28bcb-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="28bcb-381">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-381">no</span></span>             | <span data-ttu-id="28bcb-382">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-382">no</span></span>           |
| <span data-ttu-id="28bcb-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="28bcb-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="28bcb-384">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-384">no</span></span>             | <span data-ttu-id="28bcb-385">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-385">no</span></span>           |
| <span data-ttu-id="28bcb-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="28bcb-386">msdyn_committype</span></span>             | <span data-ttu-id="28bcb-387">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-387">no</span></span>             | <span data-ttu-id="28bcb-388">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-388">no</span></span>           |
| <span data-ttu-id="28bcb-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="28bcb-389">msdyn_committypename</span></span>         | <span data-ttu-id="28bcb-390">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-390">no</span></span>             | <span data-ttu-id="28bcb-391">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-391">no</span></span>           |
| <span data-ttu-id="28bcb-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="28bcb-392">msdyn_effort</span></span>                 | <span data-ttu-id="28bcb-393">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-393">no</span></span>             | <span data-ttu-id="28bcb-394">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-394">no</span></span>           |
| <span data-ttu-id="28bcb-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="28bcb-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="28bcb-396">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-396">no</span></span>             | <span data-ttu-id="28bcb-397">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-397">no</span></span>           |
| <span data-ttu-id="28bcb-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="28bcb-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="28bcb-399">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-399">no</span></span>             | <span data-ttu-id="28bcb-400">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-400">no</span></span>           |
| <span data-ttu-id="28bcb-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="28bcb-401">msdyn_finish</span></span>                 | <span data-ttu-id="28bcb-402">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-402">no</span></span>             | <span data-ttu-id="28bcb-403">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-403">no</span></span>           |
| <span data-ttu-id="28bcb-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="28bcb-405">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-405">no</span></span>             | <span data-ttu-id="28bcb-406">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-406">no</span></span>           |
| <span data-ttu-id="28bcb-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="28bcb-408">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-408">no</span></span>             | <span data-ttu-id="28bcb-409">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-409">no</span></span>           |
| <span data-ttu-id="28bcb-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="28bcb-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="28bcb-411">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-411">no</span></span>             | <span data-ttu-id="28bcb-412">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-412">no</span></span>           |
| <span data-ttu-id="28bcb-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="28bcb-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="28bcb-414">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-414">no</span></span>             | <span data-ttu-id="28bcb-415">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-415">no</span></span>           |
| <span data-ttu-id="28bcb-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="28bcb-417">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-417">no</span></span>             | <span data-ttu-id="28bcb-418">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-418">no</span></span>           |
| <span data-ttu-id="28bcb-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="28bcb-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="28bcb-420">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-420">no</span></span>             | <span data-ttu-id="28bcb-421">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-421">no</span></span>           |
| <span data-ttu-id="28bcb-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="28bcb-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="28bcb-423">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-423">no</span></span>             | <span data-ttu-id="28bcb-424">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-424">no</span></span>           |
| <span data-ttu-id="28bcb-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="28bcb-425">msdyn_projectid</span></span>              | <span data-ttu-id="28bcb-426">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-426">yes</span></span>            | <span data-ttu-id="28bcb-427">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-427">no</span></span>           |
| <span data-ttu-id="28bcb-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="28bcb-428">msdyn_projectidname</span></span>          | <span data-ttu-id="28bcb-429">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-429">no</span></span>             | <span data-ttu-id="28bcb-430">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-430">no</span></span>           |
| <span data-ttu-id="28bcb-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="28bcb-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="28bcb-432">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-432">no</span></span>             | <span data-ttu-id="28bcb-433">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-433">no</span></span>           |
| <span data-ttu-id="28bcb-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="28bcb-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="28bcb-435">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-435">no</span></span>             | <span data-ttu-id="28bcb-436">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-436">no</span></span>           |
| <span data-ttu-id="28bcb-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="28bcb-437">msdyn_start</span></span>                  | <span data-ttu-id="28bcb-438">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-438">no</span></span>             | <span data-ttu-id="28bcb-439">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-439">no</span></span>           |
| <span data-ttu-id="28bcb-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="28bcb-440">msdyn_taskid</span></span>                 | <span data-ttu-id="28bcb-441">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-441">no</span></span>             | <span data-ttu-id="28bcb-442">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-442">no</span></span>           |
| <span data-ttu-id="28bcb-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="28bcb-443">msdyn_taskidname</span></span>             | <span data-ttu-id="28bcb-444">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-444">no</span></span>             | <span data-ttu-id="28bcb-445">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-445">no</span></span>           |
| <span data-ttu-id="28bcb-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="28bcb-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="28bcb-447">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-447">no</span></span>             | <span data-ttu-id="28bcb-448">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="28bcb-449">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="28bcb-449">Project team member</span></span>

| <span data-ttu-id="28bcb-450">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="28bcb-450">**Logical name**</span></span>                                 | <span data-ttu-id="28bcb-451">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-451">**Can create**</span></span> | <span data-ttu-id="28bcb-452">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="28bcb-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="28bcb-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="28bcb-454">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-454">no</span></span>             | <span data-ttu-id="28bcb-455">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-455">no</span></span>           |
| <span data-ttu-id="28bcb-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="28bcb-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="28bcb-457">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-457">no</span></span>             | <span data-ttu-id="28bcb-458">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-458">no</span></span>           |
| <span data-ttu-id="28bcb-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="28bcb-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="28bcb-460">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-460">no</span></span>             | <span data-ttu-id="28bcb-461">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-461">no</span></span>           |
| <span data-ttu-id="28bcb-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="28bcb-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="28bcb-463">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-463">no</span></span>             | <span data-ttu-id="28bcb-464">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-464">no</span></span>           |
| <span data-ttu-id="28bcb-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="28bcb-465">msdyn_effort</span></span>                                     | <span data-ttu-id="28bcb-466">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-466">no</span></span>             | <span data-ttu-id="28bcb-467">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-467">no</span></span>           |
| <span data-ttu-id="28bcb-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="28bcb-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="28bcb-469">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-469">no</span></span>             | <span data-ttu-id="28bcb-470">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-470">no</span></span>           |
| <span data-ttu-id="28bcb-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="28bcb-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="28bcb-472">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-472">no</span></span>             | <span data-ttu-id="28bcb-473">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-473">no</span></span>           |
| <span data-ttu-id="28bcb-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="28bcb-474">msdyn_finish</span></span>                                     | <span data-ttu-id="28bcb-475">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-475">no</span></span>             | <span data-ttu-id="28bcb-476">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-476">no</span></span>           |
| <span data-ttu-id="28bcb-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="28bcb-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="28bcb-478">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-478">no</span></span>             | <span data-ttu-id="28bcb-479">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-479">no</span></span>           |
| <span data-ttu-id="28bcb-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="28bcb-480">msdyn_hours</span></span>                                      | <span data-ttu-id="28bcb-481">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-481">no</span></span>             | <span data-ttu-id="28bcb-482">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-482">no</span></span>           |
| <span data-ttu-id="28bcb-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="28bcb-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="28bcb-484">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-484">no</span></span>             | <span data-ttu-id="28bcb-485">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-485">no</span></span>           |
| <span data-ttu-id="28bcb-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="28bcb-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="28bcb-487">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-487">no</span></span>             | <span data-ttu-id="28bcb-488">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-488">no</span></span>           |
| <span data-ttu-id="28bcb-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="28bcb-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="28bcb-490">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-490">no</span></span>             | <span data-ttu-id="28bcb-491">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-491">no</span></span>           |
| <span data-ttu-id="28bcb-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="28bcb-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="28bcb-493">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-493">no</span></span>             | <span data-ttu-id="28bcb-494">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-494">no</span></span>           |
| <span data-ttu-id="28bcb-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="28bcb-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="28bcb-496">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-496">no</span></span>             | <span data-ttu-id="28bcb-497">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-497">no</span></span>           |
| <span data-ttu-id="28bcb-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="28bcb-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="28bcb-499">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-499">no</span></span>             | <span data-ttu-id="28bcb-500">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-500">no</span></span>           |
| <span data-ttu-id="28bcb-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="28bcb-501">msdyn_start</span></span>                                      | <span data-ttu-id="28bcb-502">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-502">no</span></span>             | <span data-ttu-id="28bcb-503">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="28bcb-504">Project</span><span class="sxs-lookup"><span data-stu-id="28bcb-504">Project</span></span>

| <span data-ttu-id="28bcb-505">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="28bcb-505">**Logical name**</span></span>                       | <span data-ttu-id="28bcb-506">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-506">**Can create**</span></span> | <span data-ttu-id="28bcb-507">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="28bcb-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="28bcb-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="28bcb-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="28bcb-509">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-509">no</span></span>             | <span data-ttu-id="28bcb-510">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-510">no</span></span>           |
| <span data-ttu-id="28bcb-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="28bcb-512">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-512">no</span></span>             | <span data-ttu-id="28bcb-513">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-513">no</span></span>           |
| <span data-ttu-id="28bcb-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="28bcb-515">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-515">no</span></span>             | <span data-ttu-id="28bcb-516">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-516">no</span></span>           |
| <span data-ttu-id="28bcb-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="28bcb-518">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-518">no</span></span>             | <span data-ttu-id="28bcb-519">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-519">no</span></span>           |
| <span data-ttu-id="28bcb-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="28bcb-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="28bcb-521">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-521">no</span></span>             | <span data-ttu-id="28bcb-522">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-522">no</span></span>           |
| <span data-ttu-id="28bcb-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="28bcb-524">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-524">no</span></span>             | <span data-ttu-id="28bcb-525">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-525">no</span></span>           |
| <span data-ttu-id="28bcb-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="28bcb-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="28bcb-527">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-527">yes</span></span>            | <span data-ttu-id="28bcb-528">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-528">no</span></span>           |
| <span data-ttu-id="28bcb-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="28bcb-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="28bcb-530">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-530">yes</span></span>            | <span data-ttu-id="28bcb-531">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-531">no</span></span>           |
| <span data-ttu-id="28bcb-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="28bcb-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="28bcb-533">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-533">yes</span></span>            | <span data-ttu-id="28bcb-534">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-534">no</span></span>           |
| <span data-ttu-id="28bcb-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="28bcb-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="28bcb-536">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-536">no</span></span>             | <span data-ttu-id="28bcb-537">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-537">no</span></span>           |
| <span data-ttu-id="28bcb-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="28bcb-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="28bcb-539">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-539">no</span></span>             | <span data-ttu-id="28bcb-540">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-540">no</span></span>           |
| <span data-ttu-id="28bcb-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="28bcb-542">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-542">no</span></span>             | <span data-ttu-id="28bcb-543">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-543">no</span></span>           |
| <span data-ttu-id="28bcb-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="28bcb-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="28bcb-545">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-545">no</span></span>             | <span data-ttu-id="28bcb-546">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-546">no</span></span>           |
| <span data-ttu-id="28bcb-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="28bcb-548">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-548">no</span></span>             | <span data-ttu-id="28bcb-549">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-549">no</span></span>           |
| <span data-ttu-id="28bcb-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="28bcb-550">msdyn_duration</span></span>                         | <span data-ttu-id="28bcb-551">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-551">no</span></span>             | <span data-ttu-id="28bcb-552">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-552">no</span></span>           |
| <span data-ttu-id="28bcb-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="28bcb-553">msdyn_effort</span></span>                           | <span data-ttu-id="28bcb-554">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-554">no</span></span>             | <span data-ttu-id="28bcb-555">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-555">no</span></span>           |
| <span data-ttu-id="28bcb-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="28bcb-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="28bcb-557">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-557">no</span></span>             | <span data-ttu-id="28bcb-558">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-558">no</span></span>           |
| <span data-ttu-id="28bcb-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="28bcb-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="28bcb-560">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-560">no</span></span>             | <span data-ttu-id="28bcb-561">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-561">no</span></span>           |
| <span data-ttu-id="28bcb-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="28bcb-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="28bcb-563">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-563">no</span></span>             | <span data-ttu-id="28bcb-564">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-564">no</span></span>           |
| <span data-ttu-id="28bcb-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="28bcb-565">msdyn_finish</span></span>                           | <span data-ttu-id="28bcb-566">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-566">yes</span></span>            | <span data-ttu-id="28bcb-567">sì</span><span class="sxs-lookup"><span data-stu-id="28bcb-567">yes</span></span>          |
| <span data-ttu-id="28bcb-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="28bcb-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="28bcb-569">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-569">no</span></span>             | <span data-ttu-id="28bcb-570">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-570">no</span></span>           |
| <span data-ttu-id="28bcb-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="28bcb-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="28bcb-572">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-572">no</span></span>             | <span data-ttu-id="28bcb-573">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-573">no</span></span>           |
| <span data-ttu-id="28bcb-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="28bcb-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="28bcb-575">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-575">no</span></span>             | <span data-ttu-id="28bcb-576">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-576">no</span></span>           |
| <span data-ttu-id="28bcb-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="28bcb-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="28bcb-578">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-578">no</span></span>             | <span data-ttu-id="28bcb-579">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-579">no</span></span>           |
| <span data-ttu-id="28bcb-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="28bcb-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="28bcb-581">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-581">no</span></span>             | <span data-ttu-id="28bcb-582">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-582">no</span></span>           |
| <span data-ttu-id="28bcb-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="28bcb-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="28bcb-584">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-584">no</span></span>             | <span data-ttu-id="28bcb-585">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-585">no</span></span>           |
| <span data-ttu-id="28bcb-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="28bcb-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="28bcb-587">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-587">no</span></span>             | <span data-ttu-id="28bcb-588">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-588">no</span></span>           |
| <span data-ttu-id="28bcb-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="28bcb-590">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-590">no</span></span>             | <span data-ttu-id="28bcb-591">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-591">no</span></span>           |
| <span data-ttu-id="28bcb-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="28bcb-593">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-593">no</span></span>             | <span data-ttu-id="28bcb-594">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-594">no</span></span>           |
| <span data-ttu-id="28bcb-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="28bcb-596">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-596">no</span></span>             | <span data-ttu-id="28bcb-597">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-597">no</span></span>           |
| <span data-ttu-id="28bcb-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="28bcb-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="28bcb-599">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-599">no</span></span>             | <span data-ttu-id="28bcb-600">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-600">no</span></span>           |
| <span data-ttu-id="28bcb-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="28bcb-602">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-602">no</span></span>             | <span data-ttu-id="28bcb-603">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-603">no</span></span>           |
| <span data-ttu-id="28bcb-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="28bcb-604">msdyn_progress</span></span>                         | <span data-ttu-id="28bcb-605">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-605">no</span></span>             | <span data-ttu-id="28bcb-606">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-606">no</span></span>           |
| <span data-ttu-id="28bcb-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="28bcb-608">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-608">no</span></span>             | <span data-ttu-id="28bcb-609">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-609">no</span></span>           |
| <span data-ttu-id="28bcb-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="28bcb-611">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-611">no</span></span>             | <span data-ttu-id="28bcb-612">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-612">no</span></span>           |
| <span data-ttu-id="28bcb-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="28bcb-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="28bcb-614">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-614">no</span></span>             | <span data-ttu-id="28bcb-615">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-615">no</span></span>           |
| <span data-ttu-id="28bcb-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="28bcb-617">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-617">no</span></span>             | <span data-ttu-id="28bcb-618">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-618">no</span></span>           |
| <span data-ttu-id="28bcb-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="28bcb-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="28bcb-620">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-620">no</span></span>             | <span data-ttu-id="28bcb-621">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-621">no</span></span>           |
| <span data-ttu-id="28bcb-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="28bcb-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="28bcb-623">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-623">no</span></span>             | <span data-ttu-id="28bcb-624">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-624">no</span></span>           |
| <span data-ttu-id="28bcb-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="28bcb-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="28bcb-626">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-626">no</span></span>             | <span data-ttu-id="28bcb-627">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-627">no</span></span>           |
| <span data-ttu-id="28bcb-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="28bcb-629">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-629">no</span></span>             | <span data-ttu-id="28bcb-630">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-630">no</span></span>           |
| <span data-ttu-id="28bcb-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="28bcb-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="28bcb-632">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-632">no</span></span>             | <span data-ttu-id="28bcb-633">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-633">no</span></span>           |
| <span data-ttu-id="28bcb-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="28bcb-635">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-635">no</span></span>             | <span data-ttu-id="28bcb-636">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-636">no</span></span>           |
| <span data-ttu-id="28bcb-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="28bcb-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="28bcb-638">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-638">no</span></span>             | <span data-ttu-id="28bcb-639">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-639">no</span></span>           |
| <span data-ttu-id="28bcb-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="28bcb-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="28bcb-641">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-641">no</span></span>             | <span data-ttu-id="28bcb-642">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-642">no</span></span>           |
| <span data-ttu-id="28bcb-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="28bcb-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="28bcb-644">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-644">no</span></span>             | <span data-ttu-id="28bcb-645">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-645">no</span></span>           |
| <span data-ttu-id="28bcb-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="28bcb-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="28bcb-647">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-647">no</span></span>             | <span data-ttu-id="28bcb-648">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-648">no</span></span>           |
| <span data-ttu-id="28bcb-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="28bcb-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="28bcb-650">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-650">no</span></span>             | <span data-ttu-id="28bcb-651">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-651">no</span></span>           |
| <span data-ttu-id="28bcb-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="28bcb-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="28bcb-653">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-653">no</span></span>             | <span data-ttu-id="28bcb-654">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-654">no</span></span>           |
| <span data-ttu-id="28bcb-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="28bcb-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="28bcb-656">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-656">no</span></span>             | <span data-ttu-id="28bcb-657">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-657">no</span></span>           |
| <span data-ttu-id="28bcb-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="28bcb-659">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-659">no</span></span>             | <span data-ttu-id="28bcb-660">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-660">no</span></span>           |
| <span data-ttu-id="28bcb-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="28bcb-662">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-662">no</span></span>             | <span data-ttu-id="28bcb-663">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-663">no</span></span>           |
| <span data-ttu-id="28bcb-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="28bcb-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="28bcb-665">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-665">no</span></span>             | <span data-ttu-id="28bcb-666">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-666">no</span></span>           |
| <span data-ttu-id="28bcb-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="28bcb-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="28bcb-668">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-668">no</span></span>             | <span data-ttu-id="28bcb-669">no</span><span class="sxs-lookup"><span data-stu-id="28bcb-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="28bcb-670">Limitazioni e problemi noti</span><span class="sxs-lookup"><span data-stu-id="28bcb-670">Limitations and known issues</span></span>
<span data-ttu-id="28bcb-671">Di seguito è riportato un elenco di limitazioni e problemi noti:</span><span class="sxs-lookup"><span data-stu-id="28bcb-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="28bcb-672">Le API di pianificazione del progetto possono essere utilizzate solo da **Utenti con licenza Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="28bcb-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="28bcb-673">Non possono essere utilizzate da:</span><span class="sxs-lookup"><span data-stu-id="28bcb-673">They can't be used by:</span></span>
    - <span data-ttu-id="28bcb-674">Utenti dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="28bcb-674">Application users</span></span>
    - <span data-ttu-id="28bcb-675">Utenti di sistema</span><span class="sxs-lookup"><span data-stu-id="28bcb-675">System users</span></span>
    - <span data-ttu-id="28bcb-676">Utenti integrazione</span><span class="sxs-lookup"><span data-stu-id="28bcb-676">Integration users</span></span>
    - <span data-ttu-id="28bcb-677">Altri utenti che non dispongono della licenza richiesta</span><span class="sxs-lookup"><span data-stu-id="28bcb-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="28bcb-678">Ogni **OperationSet** può avere un massimo di 100 operazioni.</span><span class="sxs-lookup"><span data-stu-id="28bcb-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="28bcb-679">Ogni utente può avere un massimo di 10 **OperationSets** aperti.</span><span class="sxs-lookup"><span data-stu-id="28bcb-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="28bcb-680">Project Operations attualmente supporta un massimo di 500 attività totali in un progetto.</span><span class="sxs-lookup"><span data-stu-id="28bcb-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="28bcb-681">Lo stato di errore e i registri degli errori di **OperationSet** non sono attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="28bcb-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="28bcb-682">Limiti e confini per progetti e attività</span><span class="sxs-lookup"><span data-stu-id="28bcb-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="28bcb-683">Gestione errori</span><span class="sxs-lookup"><span data-stu-id="28bcb-683">Error handling</span></span>

   - <span data-ttu-id="28bcb-684">Per rivedere gli errori generati dai set di operazioni, vai a **Impostazioni** \> **Pianifica integrazione** \> **Set di operazioni**.</span><span class="sxs-lookup"><span data-stu-id="28bcb-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="28bcb-685">Per rivedere gli errori generati dal servizio di pianificazione del progetto, vai a **Impostazioni** \> **Integrazione di pianificazione** \> **Registri errori PSS**.</span><span class="sxs-lookup"><span data-stu-id="28bcb-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="28bcb-686">Scenario di esempio</span><span class="sxs-lookup"><span data-stu-id="28bcb-686">Sample scenario</span></span>

<span data-ttu-id="28bcb-687">In questo scenario, creerai un progetto, un membro del team, quattro attività e due assegnazioni di risorse.</span><span class="sxs-lookup"><span data-stu-id="28bcb-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="28bcb-688">Successivamente, aggiornerai un'attività e il progetto, eliminerai un'attività e un'assegnazione di risorse e creerai una dipendenza attività.</span><span class="sxs-lookup"><span data-stu-id="28bcb-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="28bcb-689">Esempi aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="28bcb-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
