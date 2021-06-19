---
title: Utilizzare API di pianificazione per eseguire operazioni con le entità di pianificazione
description: Questo argomento fornisce informazioni ed esempi sull'utilizzo delle API di pianificazione.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116802"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="790fb-103">Utilizzare API di pianificazione per eseguire operazioni con le entità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="790fb-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="790fb-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="790fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="790fb-105">L'intera funzionalità, o una sua parte, descritta in questo articolo è disponibile nella versione di anteprima.</span><span class="sxs-lookup"><span data-stu-id="790fb-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="790fb-106">Il contenuto e la funzionalità sono soggetti a modifiche.</span><span class="sxs-lookup"><span data-stu-id="790fb-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="790fb-107">Entità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="790fb-107">Scheduling entities</span></span>

<span data-ttu-id="790fb-108">Le API di pianificazione consentono di eseguire operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="790fb-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="790fb-109">Queste entità vengono gestite tramite il motore di pianificazione in Project per il Web.</span><span class="sxs-lookup"><span data-stu-id="790fb-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="790fb-110">Le operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione** erano limitate nelle versioni precedenti di Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="790fb-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="790fb-111">La tabella seguente fornisce un elenco completo delle **Entità di pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="790fb-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="790fb-112">Nome dell'entità</span><span class="sxs-lookup"><span data-stu-id="790fb-112">Entity name</span></span>  | <span data-ttu-id="790fb-113">Nome logico entità</span><span class="sxs-lookup"><span data-stu-id="790fb-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="790fb-114">Project</span><span class="sxs-lookup"><span data-stu-id="790fb-114">Project</span></span> | <span data-ttu-id="790fb-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="790fb-115">msdyn_project</span></span> |
| <span data-ttu-id="790fb-116">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-116">Project Task</span></span>  | <span data-ttu-id="790fb-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="790fb-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="790fb-118">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-118">Project Task Dependency</span></span>  | <span data-ttu-id="790fb-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="790fb-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="790fb-120">Assegnazione risorse</span><span class="sxs-lookup"><span data-stu-id="790fb-120">Resource Assignment</span></span> | <span data-ttu-id="790fb-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="790fb-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="790fb-122">Bucket di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-122">Project Bucket</span></span>  | <span data-ttu-id="790fb-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="790fb-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="790fb-124">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-124">Project Team Member</span></span> | <span data-ttu-id="790fb-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="790fb-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="790fb-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="790fb-126">OperationSet</span></span>

<span data-ttu-id="790fb-127">OperationSet è un modello di unità di lavoro che può essere utilizzato quando in una transazione devono essere elaborate diverse richieste che influiscono sulla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="790fb-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="790fb-128">API di pianificazione</span><span class="sxs-lookup"><span data-stu-id="790fb-128">Schedule APIs</span></span>

<span data-ttu-id="790fb-129">Di seguito è riportato un elenco delle API di pianificazione correnti.</span><span class="sxs-lookup"><span data-stu-id="790fb-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="790fb-130">**msdyn_CreateProjectV1**: questa API può essere utilizzata per creare un progetto.</span><span class="sxs-lookup"><span data-stu-id="790fb-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="790fb-131">Il progetto e il bucket di progetto predefinito vengono creati immediatamente.</span><span class="sxs-lookup"><span data-stu-id="790fb-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="790fb-132">**msdyn_CreateTeamMemberV1**: questa API può essere utilizzata per creare un membro del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="790fb-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="790fb-133">Il record Membro del team viene creato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="790fb-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="790fb-134">**msdyn_CreateOperationSetV1**: questa API può essere utilizzata per pianificare diverse richieste che devono essere eseguite in una transazione.</span><span class="sxs-lookup"><span data-stu-id="790fb-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="790fb-135">**msdyn_PSSCreateV1**: questa API può essere utilizzata per creare un'entità.</span><span class="sxs-lookup"><span data-stu-id="790fb-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="790fb-136">L'entità può essere una qualsiasi delle entità di pianificazione che supportano l'operazione di creazione.</span><span class="sxs-lookup"><span data-stu-id="790fb-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="790fb-137">**msdyn_PSSUpdateV1**: questa API può essere utilizzata per aggiornare un'entità.</span><span class="sxs-lookup"><span data-stu-id="790fb-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="790fb-138">L'entità può essere una qualsiasi delle entità di pianificazione che supportano l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="790fb-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="790fb-139">**msdyn_PSSDeleteV1**: questa API può essere utilizzata per eliminare un'entità.</span><span class="sxs-lookup"><span data-stu-id="790fb-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="790fb-140">L'entità può essere una qualsiasi delle entità di pianificazione che supportano l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="790fb-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="790fb-141">**msdyn_ExecuteOperationSetV1**: questa API viene utilizzata per eseguire tutte le operazioni in un determinato set di operazioni.</span><span class="sxs-lookup"><span data-stu-id="790fb-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="790fb-142">Utilizzo delle API di pianificazione con OperationSet</span><span class="sxs-lookup"><span data-stu-id="790fb-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="790fb-143">Poiché i record con **CreateProjectV1** e **CreateTeamMemberV1** vengono creati immediatamente, queste API non possono essere utilizzate direttamente in **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="790fb-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="790fb-144">Tuttavia, puoi utilizzare l'API per creare i record necessari, creare un **OperationSet**, quindi utilizzare questi record predefiniti in **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="790fb-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="790fb-145">Operazioni supportate</span><span class="sxs-lookup"><span data-stu-id="790fb-145">Supported operations</span></span>

| <span data-ttu-id="790fb-146">Entità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="790fb-146">Scheduling entity</span></span> | <span data-ttu-id="790fb-147">Creazione di</span><span class="sxs-lookup"><span data-stu-id="790fb-147">Create</span></span> | <span data-ttu-id="790fb-148">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="790fb-148">Update</span></span> | <span data-ttu-id="790fb-149">CANC</span><span class="sxs-lookup"><span data-stu-id="790fb-149">Delete</span></span> | <span data-ttu-id="790fb-150">Considerazioni importanti</span><span class="sxs-lookup"><span data-stu-id="790fb-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="790fb-151">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-151">Project task</span></span> | <span data-ttu-id="790fb-152">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-152">Yes</span></span> | <span data-ttu-id="790fb-153">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-153">Yes</span></span> | <span data-ttu-id="790fb-154">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-154">Yes</span></span> | <span data-ttu-id="790fb-155">Nessuna</span><span class="sxs-lookup"><span data-stu-id="790fb-155">None</span></span> |
| <span data-ttu-id="790fb-156">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-156">Project task dependency</span></span> | <span data-ttu-id="790fb-157">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-157">Yes</span></span> | <span data-ttu-id="790fb-158">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-158">Yes</span></span> | | <span data-ttu-id="790fb-159">I record Dipendenza attività di progetto non vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="790fb-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="790fb-160">È invece possibile eliminare un vecchio record e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="790fb-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="790fb-161">Assegnazione risorse</span><span class="sxs-lookup"><span data-stu-id="790fb-161">Resource assignment</span></span> | <span data-ttu-id="790fb-162">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-162">Yes</span></span> | <span data-ttu-id="790fb-163">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-163">Yes</span></span> | | <span data-ttu-id="790fb-164">Le operazioni con i seguenti campi non sono supportate: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="790fb-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="790fb-165">I record Assegnazione risorse non vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="790fb-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="790fb-166">È invece possibile eliminare il vecchio record e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="790fb-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="790fb-167">Bucket di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-167">Project bucket</span></span> | <span data-ttu-id="790fb-168">N/D</span><span class="sxs-lookup"><span data-stu-id="790fb-168">N/A</span></span> | <span data-ttu-id="790fb-169">N/D</span><span class="sxs-lookup"><span data-stu-id="790fb-169">N/A</span></span> | <span data-ttu-id="790fb-170">N/D</span><span class="sxs-lookup"><span data-stu-id="790fb-170">N/A</span></span> | <span data-ttu-id="790fb-171">Il bucket predefinito viene creato utilizzando l'API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="790fb-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="790fb-172">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-172">Project team member</span></span> | <span data-ttu-id="790fb-173">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-173">Yes</span></span> | <span data-ttu-id="790fb-174">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-174">Yes</span></span> | <span data-ttu-id="790fb-175">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-175">Yes</span></span> | <span data-ttu-id="790fb-176">Per l'operazione di creazione, utilizza l'API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="790fb-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="790fb-177">Project</span><span class="sxs-lookup"><span data-stu-id="790fb-177">Project</span></span> | <span data-ttu-id="790fb-178">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-178">Yes</span></span> | <span data-ttu-id="790fb-179">Sì</span><span class="sxs-lookup"><span data-stu-id="790fb-179">Yes</span></span> | <span data-ttu-id="790fb-180">N/D</span><span class="sxs-lookup"><span data-stu-id="790fb-180">N/A</span></span> | <span data-ttu-id="790fb-181">Le operazioni con i seguenti campi non sono supportate: : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.</span><span class="sxs-lookup"><span data-stu-id="790fb-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="790fb-182">Queste API possono essere chiamate con oggetti entità che includono campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="790fb-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="790fb-183">La proprietà ID è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="790fb-183">The ID property is optional.</span></span> <span data-ttu-id="790fb-184">Se fornita, il sistema tenta di utilizzarla e genera un'eccezione se non può essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="790fb-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="790fb-185">Se non è fornita, il sistema la genererà.</span><span class="sxs-lookup"><span data-stu-id="790fb-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="790fb-186">Campi con limitazioni</span><span class="sxs-lookup"><span data-stu-id="790fb-186">Restricted fields</span></span>

<span data-ttu-id="790fb-187">Le seguenti tabelle definiscono i campi con limitazioni **Crea** e **Modifica.**</span><span class="sxs-lookup"><span data-stu-id="790fb-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="790fb-188">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-188">Project task</span></span>

| <span data-ttu-id="790fb-189">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="790fb-189">**Logical name**</span></span>                       | <span data-ttu-id="790fb-190">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-190">**Can create**</span></span> | <span data-ttu-id="790fb-191">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="790fb-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="790fb-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="790fb-193">no</span><span class="sxs-lookup"><span data-stu-id="790fb-193">no</span></span>             | <span data-ttu-id="790fb-194">no</span><span class="sxs-lookup"><span data-stu-id="790fb-194">no</span></span>               |
| <span data-ttu-id="790fb-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="790fb-196">no</span><span class="sxs-lookup"><span data-stu-id="790fb-196">no</span></span>             | <span data-ttu-id="790fb-197">no</span><span class="sxs-lookup"><span data-stu-id="790fb-197">no</span></span>               |
| <span data-ttu-id="790fb-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="790fb-198">msdyn_actualend</span></span>                        | <span data-ttu-id="790fb-199">no</span><span class="sxs-lookup"><span data-stu-id="790fb-199">no</span></span>             | <span data-ttu-id="790fb-200">no</span><span class="sxs-lookup"><span data-stu-id="790fb-200">no</span></span>               |
| <span data-ttu-id="790fb-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="790fb-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="790fb-202">no</span><span class="sxs-lookup"><span data-stu-id="790fb-202">no</span></span>             | <span data-ttu-id="790fb-203">no</span><span class="sxs-lookup"><span data-stu-id="790fb-203">no</span></span>               |
| <span data-ttu-id="790fb-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="790fb-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="790fb-205">no</span><span class="sxs-lookup"><span data-stu-id="790fb-205">no</span></span>             | <span data-ttu-id="790fb-206">no</span><span class="sxs-lookup"><span data-stu-id="790fb-206">no</span></span>               |
| <span data-ttu-id="790fb-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="790fb-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="790fb-208">no</span><span class="sxs-lookup"><span data-stu-id="790fb-208">no</span></span>             | <span data-ttu-id="790fb-209">no</span><span class="sxs-lookup"><span data-stu-id="790fb-209">no</span></span>               |
| <span data-ttu-id="790fb-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="790fb-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="790fb-211">no</span><span class="sxs-lookup"><span data-stu-id="790fb-211">no</span></span>             | <span data-ttu-id="790fb-212">no</span><span class="sxs-lookup"><span data-stu-id="790fb-212">no</span></span>               |
| <span data-ttu-id="790fb-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="790fb-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="790fb-214">no</span><span class="sxs-lookup"><span data-stu-id="790fb-214">no</span></span>             | <span data-ttu-id="790fb-215">no</span><span class="sxs-lookup"><span data-stu-id="790fb-215">no</span></span>               |
| <span data-ttu-id="790fb-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="790fb-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="790fb-217">no</span><span class="sxs-lookup"><span data-stu-id="790fb-217">no</span></span>             | <span data-ttu-id="790fb-218">no</span><span class="sxs-lookup"><span data-stu-id="790fb-218">no</span></span>               |
| <span data-ttu-id="790fb-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="790fb-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="790fb-220">no</span><span class="sxs-lookup"><span data-stu-id="790fb-220">no</span></span>             | <span data-ttu-id="790fb-221">no</span><span class="sxs-lookup"><span data-stu-id="790fb-221">no</span></span>               |
| <span data-ttu-id="790fb-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="790fb-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="790fb-223">no</span><span class="sxs-lookup"><span data-stu-id="790fb-223">no</span></span>             | <span data-ttu-id="790fb-224">no</span><span class="sxs-lookup"><span data-stu-id="790fb-224">no</span></span>               |
| <span data-ttu-id="790fb-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="790fb-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="790fb-226">no</span><span class="sxs-lookup"><span data-stu-id="790fb-226">no</span></span>             | <span data-ttu-id="790fb-227">no</span><span class="sxs-lookup"><span data-stu-id="790fb-227">no</span></span>               |
| <span data-ttu-id="790fb-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="790fb-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="790fb-229">no</span><span class="sxs-lookup"><span data-stu-id="790fb-229">no</span></span>             | <span data-ttu-id="790fb-230">no</span><span class="sxs-lookup"><span data-stu-id="790fb-230">no</span></span>               |
| <span data-ttu-id="790fb-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="790fb-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="790fb-232">no</span><span class="sxs-lookup"><span data-stu-id="790fb-232">no</span></span>             | <span data-ttu-id="790fb-233">no</span><span class="sxs-lookup"><span data-stu-id="790fb-233">no</span></span>               |
| <span data-ttu-id="790fb-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="790fb-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="790fb-235">no</span><span class="sxs-lookup"><span data-stu-id="790fb-235">no</span></span>             | <span data-ttu-id="790fb-236">no</span><span class="sxs-lookup"><span data-stu-id="790fb-236">no</span></span>               |
| <span data-ttu-id="790fb-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="790fb-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="790fb-238">no</span><span class="sxs-lookup"><span data-stu-id="790fb-238">no</span></span>             | <span data-ttu-id="790fb-239">no</span><span class="sxs-lookup"><span data-stu-id="790fb-239">no</span></span>               |
| <span data-ttu-id="790fb-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="790fb-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="790fb-241">no</span><span class="sxs-lookup"><span data-stu-id="790fb-241">no</span></span>             | <span data-ttu-id="790fb-242">no</span><span class="sxs-lookup"><span data-stu-id="790fb-242">no</span></span>               |
| <span data-ttu-id="790fb-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="790fb-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="790fb-244">no</span><span class="sxs-lookup"><span data-stu-id="790fb-244">no</span></span>             | <span data-ttu-id="790fb-245">no</span><span class="sxs-lookup"><span data-stu-id="790fb-245">no</span></span>               |
| <span data-ttu-id="790fb-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="790fb-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="790fb-247">no</span><span class="sxs-lookup"><span data-stu-id="790fb-247">no</span></span>             | <span data-ttu-id="790fb-248">no</span><span class="sxs-lookup"><span data-stu-id="790fb-248">no</span></span>               |
| <span data-ttu-id="790fb-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="790fb-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="790fb-250">no</span><span class="sxs-lookup"><span data-stu-id="790fb-250">no</span></span>             | <span data-ttu-id="790fb-251">no</span><span class="sxs-lookup"><span data-stu-id="790fb-251">no</span></span>               |
| <span data-ttu-id="790fb-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="790fb-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="790fb-253">no</span><span class="sxs-lookup"><span data-stu-id="790fb-253">no</span></span>             | <span data-ttu-id="790fb-254">no</span><span class="sxs-lookup"><span data-stu-id="790fb-254">no</span></span>               |
| <span data-ttu-id="790fb-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="790fb-256">no</span><span class="sxs-lookup"><span data-stu-id="790fb-256">no</span></span>             | <span data-ttu-id="790fb-257">no</span><span class="sxs-lookup"><span data-stu-id="790fb-257">no</span></span>               |
| <span data-ttu-id="790fb-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="790fb-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="790fb-259">no</span><span class="sxs-lookup"><span data-stu-id="790fb-259">no</span></span>             | <span data-ttu-id="790fb-260">no</span><span class="sxs-lookup"><span data-stu-id="790fb-260">no</span></span>               |
| <span data-ttu-id="790fb-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="790fb-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="790fb-262">no</span><span class="sxs-lookup"><span data-stu-id="790fb-262">no</span></span>             | <span data-ttu-id="790fb-263">no</span><span class="sxs-lookup"><span data-stu-id="790fb-263">no</span></span>               |
| <span data-ttu-id="790fb-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="790fb-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="790fb-265">no</span><span class="sxs-lookup"><span data-stu-id="790fb-265">no</span></span>             | <span data-ttu-id="790fb-266">no</span><span class="sxs-lookup"><span data-stu-id="790fb-266">no</span></span>               |
| <span data-ttu-id="790fb-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="790fb-267">msdyn_progress</span></span>                         | <span data-ttu-id="790fb-268">no</span><span class="sxs-lookup"><span data-stu-id="790fb-268">no</span></span>             | <span data-ttu-id="790fb-269">no (sì per P4W)</span><span class="sxs-lookup"><span data-stu-id="790fb-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="790fb-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="790fb-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="790fb-271">no</span><span class="sxs-lookup"><span data-stu-id="790fb-271">no</span></span>             | <span data-ttu-id="790fb-272">no</span><span class="sxs-lookup"><span data-stu-id="790fb-272">no</span></span>               |
| <span data-ttu-id="790fb-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="790fb-274">no</span><span class="sxs-lookup"><span data-stu-id="790fb-274">no</span></span>             | <span data-ttu-id="790fb-275">no</span><span class="sxs-lookup"><span data-stu-id="790fb-275">no</span></span>               |
| <span data-ttu-id="790fb-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="790fb-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="790fb-277">no</span><span class="sxs-lookup"><span data-stu-id="790fb-277">no</span></span>             | <span data-ttu-id="790fb-278">no</span><span class="sxs-lookup"><span data-stu-id="790fb-278">no</span></span>               |
| <span data-ttu-id="790fb-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="790fb-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="790fb-280">no</span><span class="sxs-lookup"><span data-stu-id="790fb-280">no</span></span>             | <span data-ttu-id="790fb-281">no</span><span class="sxs-lookup"><span data-stu-id="790fb-281">no</span></span>               |
| <span data-ttu-id="790fb-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="790fb-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="790fb-283">no</span><span class="sxs-lookup"><span data-stu-id="790fb-283">no</span></span>             | <span data-ttu-id="790fb-284">no</span><span class="sxs-lookup"><span data-stu-id="790fb-284">no</span></span>               |
| <span data-ttu-id="790fb-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="790fb-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="790fb-286">no</span><span class="sxs-lookup"><span data-stu-id="790fb-286">no</span></span>             | <span data-ttu-id="790fb-287">no</span><span class="sxs-lookup"><span data-stu-id="790fb-287">no</span></span>               |
| <span data-ttu-id="790fb-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="790fb-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="790fb-289">no</span><span class="sxs-lookup"><span data-stu-id="790fb-289">no</span></span>             | <span data-ttu-id="790fb-290">no</span><span class="sxs-lookup"><span data-stu-id="790fb-290">no</span></span>               |
| <span data-ttu-id="790fb-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="790fb-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="790fb-292">no</span><span class="sxs-lookup"><span data-stu-id="790fb-292">no</span></span>             | <span data-ttu-id="790fb-293">no</span><span class="sxs-lookup"><span data-stu-id="790fb-293">no</span></span>               |
| <span data-ttu-id="790fb-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="790fb-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="790fb-295">no</span><span class="sxs-lookup"><span data-stu-id="790fb-295">no</span></span>             | <span data-ttu-id="790fb-296">no</span><span class="sxs-lookup"><span data-stu-id="790fb-296">no</span></span>               |
| <span data-ttu-id="790fb-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="790fb-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="790fb-298">no</span><span class="sxs-lookup"><span data-stu-id="790fb-298">no</span></span>             | <span data-ttu-id="790fb-299">no</span><span class="sxs-lookup"><span data-stu-id="790fb-299">no</span></span>               |
| <span data-ttu-id="790fb-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="790fb-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="790fb-301">no</span><span class="sxs-lookup"><span data-stu-id="790fb-301">no</span></span>             | <span data-ttu-id="790fb-302">no</span><span class="sxs-lookup"><span data-stu-id="790fb-302">no</span></span>               |
| <span data-ttu-id="790fb-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="790fb-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="790fb-304">no</span><span class="sxs-lookup"><span data-stu-id="790fb-304">no</span></span>             | <span data-ttu-id="790fb-305">no</span><span class="sxs-lookup"><span data-stu-id="790fb-305">no</span></span>               |
| <span data-ttu-id="790fb-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="790fb-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="790fb-307">no</span><span class="sxs-lookup"><span data-stu-id="790fb-307">no</span></span>             | <span data-ttu-id="790fb-308">no</span><span class="sxs-lookup"><span data-stu-id="790fb-308">no</span></span>               |
| <span data-ttu-id="790fb-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="790fb-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="790fb-310">no</span><span class="sxs-lookup"><span data-stu-id="790fb-310">no</span></span>             | <span data-ttu-id="790fb-311">no</span><span class="sxs-lookup"><span data-stu-id="790fb-311">no</span></span>               |
| <span data-ttu-id="790fb-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="790fb-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="790fb-313">no</span><span class="sxs-lookup"><span data-stu-id="790fb-313">no</span></span>             | <span data-ttu-id="790fb-314">no</span><span class="sxs-lookup"><span data-stu-id="790fb-314">no</span></span>               |
| <span data-ttu-id="790fb-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="790fb-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="790fb-316">no</span><span class="sxs-lookup"><span data-stu-id="790fb-316">no</span></span>             | <span data-ttu-id="790fb-317">no</span><span class="sxs-lookup"><span data-stu-id="790fb-317">no</span></span>               |
| <span data-ttu-id="790fb-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="790fb-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="790fb-319">no</span><span class="sxs-lookup"><span data-stu-id="790fb-319">no</span></span>             | <span data-ttu-id="790fb-320">no</span><span class="sxs-lookup"><span data-stu-id="790fb-320">no</span></span>               |
| <span data-ttu-id="790fb-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="790fb-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="790fb-322">no</span><span class="sxs-lookup"><span data-stu-id="790fb-322">no</span></span>             | <span data-ttu-id="790fb-323">no</span><span class="sxs-lookup"><span data-stu-id="790fb-323">no</span></span>               |
| <span data-ttu-id="790fb-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="790fb-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="790fb-325">no</span><span class="sxs-lookup"><span data-stu-id="790fb-325">no</span></span>             | <span data-ttu-id="790fb-326">no</span><span class="sxs-lookup"><span data-stu-id="790fb-326">no</span></span>               |
| <span data-ttu-id="790fb-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="790fb-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="790fb-328">no</span><span class="sxs-lookup"><span data-stu-id="790fb-328">no</span></span>             | <span data-ttu-id="790fb-329">no</span><span class="sxs-lookup"><span data-stu-id="790fb-329">no</span></span>               |
| <span data-ttu-id="790fb-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="790fb-330">msdyn_summary</span></span>                          | <span data-ttu-id="790fb-331">no</span><span class="sxs-lookup"><span data-stu-id="790fb-331">no</span></span>             | <span data-ttu-id="790fb-332">no</span><span class="sxs-lookup"><span data-stu-id="790fb-332">no</span></span>               |
| <span data-ttu-id="790fb-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="790fb-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="790fb-334">no</span><span class="sxs-lookup"><span data-stu-id="790fb-334">no</span></span>             | <span data-ttu-id="790fb-335">no</span><span class="sxs-lookup"><span data-stu-id="790fb-335">no</span></span>               |
| <span data-ttu-id="790fb-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="790fb-337">no</span><span class="sxs-lookup"><span data-stu-id="790fb-337">no</span></span>             | <span data-ttu-id="790fb-338">no</span><span class="sxs-lookup"><span data-stu-id="790fb-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="790fb-339">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-339">Project task dependency</span></span>

| <span data-ttu-id="790fb-340">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="790fb-340">**Logical name**</span></span>              | <span data-ttu-id="790fb-341">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-341">**Can create**</span></span> | <span data-ttu-id="790fb-342">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="790fb-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="790fb-343">msdyn_linktype</span></span>                | <span data-ttu-id="790fb-344">no</span><span class="sxs-lookup"><span data-stu-id="790fb-344">no</span></span>             | <span data-ttu-id="790fb-345">no</span><span class="sxs-lookup"><span data-stu-id="790fb-345">no</span></span>           |
| <span data-ttu-id="790fb-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="790fb-346">msdyn_linktypename</span></span>            | <span data-ttu-id="790fb-347">no</span><span class="sxs-lookup"><span data-stu-id="790fb-347">no</span></span>             | <span data-ttu-id="790fb-348">no</span><span class="sxs-lookup"><span data-stu-id="790fb-348">no</span></span>           |
| <span data-ttu-id="790fb-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="790fb-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="790fb-350">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-350">yes</span></span>            | <span data-ttu-id="790fb-351">no</span><span class="sxs-lookup"><span data-stu-id="790fb-351">no</span></span>           |
| <span data-ttu-id="790fb-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="790fb-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="790fb-353">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-353">yes</span></span>            | <span data-ttu-id="790fb-354">no</span><span class="sxs-lookup"><span data-stu-id="790fb-354">no</span></span>           |
| <span data-ttu-id="790fb-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="790fb-355">msdyn_project</span></span>                 | <span data-ttu-id="790fb-356">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-356">yes</span></span>            | <span data-ttu-id="790fb-357">no</span><span class="sxs-lookup"><span data-stu-id="790fb-357">no</span></span>           |
| <span data-ttu-id="790fb-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="790fb-358">msdyn_projectname</span></span>             | <span data-ttu-id="790fb-359">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-359">yes</span></span>            | <span data-ttu-id="790fb-360">no</span><span class="sxs-lookup"><span data-stu-id="790fb-360">no</span></span>           |
| <span data-ttu-id="790fb-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="790fb-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="790fb-362">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-362">yes</span></span>            | <span data-ttu-id="790fb-363">no</span><span class="sxs-lookup"><span data-stu-id="790fb-363">no</span></span>           |
| <span data-ttu-id="790fb-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="790fb-364">msdyn_successortask</span></span>           | <span data-ttu-id="790fb-365">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-365">yes</span></span>            | <span data-ttu-id="790fb-366">no</span><span class="sxs-lookup"><span data-stu-id="790fb-366">no</span></span>           |
| <span data-ttu-id="790fb-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="790fb-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="790fb-368">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-368">yes</span></span>            | <span data-ttu-id="790fb-369">no</span><span class="sxs-lookup"><span data-stu-id="790fb-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="790fb-370">Assegnazione risorse</span><span class="sxs-lookup"><span data-stu-id="790fb-370">Resource assignment</span></span>

| <span data-ttu-id="790fb-371">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="790fb-371">**Logical name**</span></span>             | <span data-ttu-id="790fb-372">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-372">**Can create**</span></span> | <span data-ttu-id="790fb-373">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="790fb-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="790fb-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="790fb-375">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-375">yes</span></span>            | <span data-ttu-id="790fb-376">no</span><span class="sxs-lookup"><span data-stu-id="790fb-376">no</span></span>           |
| <span data-ttu-id="790fb-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="790fb-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="790fb-378">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-378">yes</span></span>            | <span data-ttu-id="790fb-379">no</span><span class="sxs-lookup"><span data-stu-id="790fb-379">no</span></span>           |
| <span data-ttu-id="790fb-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="790fb-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="790fb-381">no</span><span class="sxs-lookup"><span data-stu-id="790fb-381">no</span></span>             | <span data-ttu-id="790fb-382">no</span><span class="sxs-lookup"><span data-stu-id="790fb-382">no</span></span>           |
| <span data-ttu-id="790fb-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="790fb-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="790fb-384">no</span><span class="sxs-lookup"><span data-stu-id="790fb-384">no</span></span>             | <span data-ttu-id="790fb-385">no</span><span class="sxs-lookup"><span data-stu-id="790fb-385">no</span></span>           |
| <span data-ttu-id="790fb-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="790fb-386">msdyn_committype</span></span>             | <span data-ttu-id="790fb-387">no</span><span class="sxs-lookup"><span data-stu-id="790fb-387">no</span></span>             | <span data-ttu-id="790fb-388">no</span><span class="sxs-lookup"><span data-stu-id="790fb-388">no</span></span>           |
| <span data-ttu-id="790fb-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="790fb-389">msdyn_committypename</span></span>         | <span data-ttu-id="790fb-390">no</span><span class="sxs-lookup"><span data-stu-id="790fb-390">no</span></span>             | <span data-ttu-id="790fb-391">no</span><span class="sxs-lookup"><span data-stu-id="790fb-391">no</span></span>           |
| <span data-ttu-id="790fb-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="790fb-392">msdyn_effort</span></span>                 | <span data-ttu-id="790fb-393">no</span><span class="sxs-lookup"><span data-stu-id="790fb-393">no</span></span>             | <span data-ttu-id="790fb-394">no</span><span class="sxs-lookup"><span data-stu-id="790fb-394">no</span></span>           |
| <span data-ttu-id="790fb-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="790fb-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="790fb-396">no</span><span class="sxs-lookup"><span data-stu-id="790fb-396">no</span></span>             | <span data-ttu-id="790fb-397">no</span><span class="sxs-lookup"><span data-stu-id="790fb-397">no</span></span>           |
| <span data-ttu-id="790fb-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="790fb-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="790fb-399">no</span><span class="sxs-lookup"><span data-stu-id="790fb-399">no</span></span>             | <span data-ttu-id="790fb-400">no</span><span class="sxs-lookup"><span data-stu-id="790fb-400">no</span></span>           |
| <span data-ttu-id="790fb-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="790fb-401">msdyn_finish</span></span>                 | <span data-ttu-id="790fb-402">no</span><span class="sxs-lookup"><span data-stu-id="790fb-402">no</span></span>             | <span data-ttu-id="790fb-403">no</span><span class="sxs-lookup"><span data-stu-id="790fb-403">no</span></span>           |
| <span data-ttu-id="790fb-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="790fb-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="790fb-405">no</span><span class="sxs-lookup"><span data-stu-id="790fb-405">no</span></span>             | <span data-ttu-id="790fb-406">no</span><span class="sxs-lookup"><span data-stu-id="790fb-406">no</span></span>           |
| <span data-ttu-id="790fb-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="790fb-408">no</span><span class="sxs-lookup"><span data-stu-id="790fb-408">no</span></span>             | <span data-ttu-id="790fb-409">no</span><span class="sxs-lookup"><span data-stu-id="790fb-409">no</span></span>           |
| <span data-ttu-id="790fb-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="790fb-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="790fb-411">no</span><span class="sxs-lookup"><span data-stu-id="790fb-411">no</span></span>             | <span data-ttu-id="790fb-412">no</span><span class="sxs-lookup"><span data-stu-id="790fb-412">no</span></span>           |
| <span data-ttu-id="790fb-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="790fb-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="790fb-414">no</span><span class="sxs-lookup"><span data-stu-id="790fb-414">no</span></span>             | <span data-ttu-id="790fb-415">no</span><span class="sxs-lookup"><span data-stu-id="790fb-415">no</span></span>           |
| <span data-ttu-id="790fb-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="790fb-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="790fb-417">no</span><span class="sxs-lookup"><span data-stu-id="790fb-417">no</span></span>             | <span data-ttu-id="790fb-418">no</span><span class="sxs-lookup"><span data-stu-id="790fb-418">no</span></span>           |
| <span data-ttu-id="790fb-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="790fb-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="790fb-420">no</span><span class="sxs-lookup"><span data-stu-id="790fb-420">no</span></span>             | <span data-ttu-id="790fb-421">no</span><span class="sxs-lookup"><span data-stu-id="790fb-421">no</span></span>           |
| <span data-ttu-id="790fb-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="790fb-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="790fb-423">no</span><span class="sxs-lookup"><span data-stu-id="790fb-423">no</span></span>             | <span data-ttu-id="790fb-424">no</span><span class="sxs-lookup"><span data-stu-id="790fb-424">no</span></span>           |
| <span data-ttu-id="790fb-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="790fb-425">msdyn_projectid</span></span>              | <span data-ttu-id="790fb-426">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-426">yes</span></span>            | <span data-ttu-id="790fb-427">no</span><span class="sxs-lookup"><span data-stu-id="790fb-427">no</span></span>           |
| <span data-ttu-id="790fb-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="790fb-428">msdyn_projectidname</span></span>          | <span data-ttu-id="790fb-429">no</span><span class="sxs-lookup"><span data-stu-id="790fb-429">no</span></span>             | <span data-ttu-id="790fb-430">no</span><span class="sxs-lookup"><span data-stu-id="790fb-430">no</span></span>           |
| <span data-ttu-id="790fb-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="790fb-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="790fb-432">no</span><span class="sxs-lookup"><span data-stu-id="790fb-432">no</span></span>             | <span data-ttu-id="790fb-433">no</span><span class="sxs-lookup"><span data-stu-id="790fb-433">no</span></span>           |
| <span data-ttu-id="790fb-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="790fb-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="790fb-435">no</span><span class="sxs-lookup"><span data-stu-id="790fb-435">no</span></span>             | <span data-ttu-id="790fb-436">no</span><span class="sxs-lookup"><span data-stu-id="790fb-436">no</span></span>           |
| <span data-ttu-id="790fb-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="790fb-437">msdyn_start</span></span>                  | <span data-ttu-id="790fb-438">no</span><span class="sxs-lookup"><span data-stu-id="790fb-438">no</span></span>             | <span data-ttu-id="790fb-439">no</span><span class="sxs-lookup"><span data-stu-id="790fb-439">no</span></span>           |
| <span data-ttu-id="790fb-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="790fb-440">msdyn_taskid</span></span>                 | <span data-ttu-id="790fb-441">no</span><span class="sxs-lookup"><span data-stu-id="790fb-441">no</span></span>             | <span data-ttu-id="790fb-442">no</span><span class="sxs-lookup"><span data-stu-id="790fb-442">no</span></span>           |
| <span data-ttu-id="790fb-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="790fb-443">msdyn_taskidname</span></span>             | <span data-ttu-id="790fb-444">no</span><span class="sxs-lookup"><span data-stu-id="790fb-444">no</span></span>             | <span data-ttu-id="790fb-445">no</span><span class="sxs-lookup"><span data-stu-id="790fb-445">no</span></span>           |
| <span data-ttu-id="790fb-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="790fb-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="790fb-447">no</span><span class="sxs-lookup"><span data-stu-id="790fb-447">no</span></span>             | <span data-ttu-id="790fb-448">no</span><span class="sxs-lookup"><span data-stu-id="790fb-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="790fb-449">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="790fb-449">Project team member</span></span>

| <span data-ttu-id="790fb-450">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="790fb-450">**Logical name**</span></span>                                 | <span data-ttu-id="790fb-451">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-451">**Can create**</span></span> | <span data-ttu-id="790fb-452">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="790fb-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="790fb-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="790fb-454">no</span><span class="sxs-lookup"><span data-stu-id="790fb-454">no</span></span>             | <span data-ttu-id="790fb-455">no</span><span class="sxs-lookup"><span data-stu-id="790fb-455">no</span></span>           |
| <span data-ttu-id="790fb-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="790fb-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="790fb-457">no</span><span class="sxs-lookup"><span data-stu-id="790fb-457">no</span></span>             | <span data-ttu-id="790fb-458">no</span><span class="sxs-lookup"><span data-stu-id="790fb-458">no</span></span>           |
| <span data-ttu-id="790fb-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="790fb-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="790fb-460">no</span><span class="sxs-lookup"><span data-stu-id="790fb-460">no</span></span>             | <span data-ttu-id="790fb-461">no</span><span class="sxs-lookup"><span data-stu-id="790fb-461">no</span></span>           |
| <span data-ttu-id="790fb-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="790fb-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="790fb-463">no</span><span class="sxs-lookup"><span data-stu-id="790fb-463">no</span></span>             | <span data-ttu-id="790fb-464">no</span><span class="sxs-lookup"><span data-stu-id="790fb-464">no</span></span>           |
| <span data-ttu-id="790fb-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="790fb-465">msdyn_effort</span></span>                                     | <span data-ttu-id="790fb-466">no</span><span class="sxs-lookup"><span data-stu-id="790fb-466">no</span></span>             | <span data-ttu-id="790fb-467">no</span><span class="sxs-lookup"><span data-stu-id="790fb-467">no</span></span>           |
| <span data-ttu-id="790fb-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="790fb-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="790fb-469">no</span><span class="sxs-lookup"><span data-stu-id="790fb-469">no</span></span>             | <span data-ttu-id="790fb-470">no</span><span class="sxs-lookup"><span data-stu-id="790fb-470">no</span></span>           |
| <span data-ttu-id="790fb-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="790fb-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="790fb-472">no</span><span class="sxs-lookup"><span data-stu-id="790fb-472">no</span></span>             | <span data-ttu-id="790fb-473">no</span><span class="sxs-lookup"><span data-stu-id="790fb-473">no</span></span>           |
| <span data-ttu-id="790fb-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="790fb-474">msdyn_finish</span></span>                                     | <span data-ttu-id="790fb-475">no</span><span class="sxs-lookup"><span data-stu-id="790fb-475">no</span></span>             | <span data-ttu-id="790fb-476">no</span><span class="sxs-lookup"><span data-stu-id="790fb-476">no</span></span>           |
| <span data-ttu-id="790fb-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="790fb-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="790fb-478">no</span><span class="sxs-lookup"><span data-stu-id="790fb-478">no</span></span>             | <span data-ttu-id="790fb-479">no</span><span class="sxs-lookup"><span data-stu-id="790fb-479">no</span></span>           |
| <span data-ttu-id="790fb-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="790fb-480">msdyn_hours</span></span>                                      | <span data-ttu-id="790fb-481">no</span><span class="sxs-lookup"><span data-stu-id="790fb-481">no</span></span>             | <span data-ttu-id="790fb-482">no</span><span class="sxs-lookup"><span data-stu-id="790fb-482">no</span></span>           |
| <span data-ttu-id="790fb-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="790fb-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="790fb-484">no</span><span class="sxs-lookup"><span data-stu-id="790fb-484">no</span></span>             | <span data-ttu-id="790fb-485">no</span><span class="sxs-lookup"><span data-stu-id="790fb-485">no</span></span>           |
| <span data-ttu-id="790fb-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="790fb-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="790fb-487">no</span><span class="sxs-lookup"><span data-stu-id="790fb-487">no</span></span>             | <span data-ttu-id="790fb-488">no</span><span class="sxs-lookup"><span data-stu-id="790fb-488">no</span></span>           |
| <span data-ttu-id="790fb-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="790fb-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="790fb-490">no</span><span class="sxs-lookup"><span data-stu-id="790fb-490">no</span></span>             | <span data-ttu-id="790fb-491">no</span><span class="sxs-lookup"><span data-stu-id="790fb-491">no</span></span>           |
| <span data-ttu-id="790fb-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="790fb-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="790fb-493">no</span><span class="sxs-lookup"><span data-stu-id="790fb-493">no</span></span>             | <span data-ttu-id="790fb-494">no</span><span class="sxs-lookup"><span data-stu-id="790fb-494">no</span></span>           |
| <span data-ttu-id="790fb-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="790fb-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="790fb-496">no</span><span class="sxs-lookup"><span data-stu-id="790fb-496">no</span></span>             | <span data-ttu-id="790fb-497">no</span><span class="sxs-lookup"><span data-stu-id="790fb-497">no</span></span>           |
| <span data-ttu-id="790fb-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="790fb-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="790fb-499">no</span><span class="sxs-lookup"><span data-stu-id="790fb-499">no</span></span>             | <span data-ttu-id="790fb-500">no</span><span class="sxs-lookup"><span data-stu-id="790fb-500">no</span></span>           |
| <span data-ttu-id="790fb-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="790fb-501">msdyn_start</span></span>                                      | <span data-ttu-id="790fb-502">no</span><span class="sxs-lookup"><span data-stu-id="790fb-502">no</span></span>             | <span data-ttu-id="790fb-503">no</span><span class="sxs-lookup"><span data-stu-id="790fb-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="790fb-504">Project</span><span class="sxs-lookup"><span data-stu-id="790fb-504">Project</span></span>

| <span data-ttu-id="790fb-505">**Nome logico**</span><span class="sxs-lookup"><span data-stu-id="790fb-505">**Logical name**</span></span>                       | <span data-ttu-id="790fb-506">**Creazione possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-506">**Can create**</span></span> | <span data-ttu-id="790fb-507">**Modifica possibile**</span><span class="sxs-lookup"><span data-stu-id="790fb-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="790fb-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="790fb-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="790fb-509">no</span><span class="sxs-lookup"><span data-stu-id="790fb-509">no</span></span>             | <span data-ttu-id="790fb-510">no</span><span class="sxs-lookup"><span data-stu-id="790fb-510">no</span></span>           |
| <span data-ttu-id="790fb-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="790fb-512">no</span><span class="sxs-lookup"><span data-stu-id="790fb-512">no</span></span>             | <span data-ttu-id="790fb-513">no</span><span class="sxs-lookup"><span data-stu-id="790fb-513">no</span></span>           |
| <span data-ttu-id="790fb-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="790fb-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="790fb-515">no</span><span class="sxs-lookup"><span data-stu-id="790fb-515">no</span></span>             | <span data-ttu-id="790fb-516">no</span><span class="sxs-lookup"><span data-stu-id="790fb-516">no</span></span>           |
| <span data-ttu-id="790fb-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="790fb-518">no</span><span class="sxs-lookup"><span data-stu-id="790fb-518">no</span></span>             | <span data-ttu-id="790fb-519">no</span><span class="sxs-lookup"><span data-stu-id="790fb-519">no</span></span>           |
| <span data-ttu-id="790fb-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="790fb-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="790fb-521">no</span><span class="sxs-lookup"><span data-stu-id="790fb-521">no</span></span>             | <span data-ttu-id="790fb-522">no</span><span class="sxs-lookup"><span data-stu-id="790fb-522">no</span></span>           |
| <span data-ttu-id="790fb-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="790fb-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="790fb-524">no</span><span class="sxs-lookup"><span data-stu-id="790fb-524">no</span></span>             | <span data-ttu-id="790fb-525">no</span><span class="sxs-lookup"><span data-stu-id="790fb-525">no</span></span>           |
| <span data-ttu-id="790fb-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="790fb-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="790fb-527">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-527">yes</span></span>            | <span data-ttu-id="790fb-528">no</span><span class="sxs-lookup"><span data-stu-id="790fb-528">no</span></span>           |
| <span data-ttu-id="790fb-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="790fb-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="790fb-530">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-530">yes</span></span>            | <span data-ttu-id="790fb-531">no</span><span class="sxs-lookup"><span data-stu-id="790fb-531">no</span></span>           |
| <span data-ttu-id="790fb-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="790fb-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="790fb-533">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-533">yes</span></span>            | <span data-ttu-id="790fb-534">no</span><span class="sxs-lookup"><span data-stu-id="790fb-534">no</span></span>           |
| <span data-ttu-id="790fb-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="790fb-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="790fb-536">no</span><span class="sxs-lookup"><span data-stu-id="790fb-536">no</span></span>             | <span data-ttu-id="790fb-537">no</span><span class="sxs-lookup"><span data-stu-id="790fb-537">no</span></span>           |
| <span data-ttu-id="790fb-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="790fb-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="790fb-539">no</span><span class="sxs-lookup"><span data-stu-id="790fb-539">no</span></span>             | <span data-ttu-id="790fb-540">no</span><span class="sxs-lookup"><span data-stu-id="790fb-540">no</span></span>           |
| <span data-ttu-id="790fb-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="790fb-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="790fb-542">no</span><span class="sxs-lookup"><span data-stu-id="790fb-542">no</span></span>             | <span data-ttu-id="790fb-543">no</span><span class="sxs-lookup"><span data-stu-id="790fb-543">no</span></span>           |
| <span data-ttu-id="790fb-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="790fb-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="790fb-545">no</span><span class="sxs-lookup"><span data-stu-id="790fb-545">no</span></span>             | <span data-ttu-id="790fb-546">no</span><span class="sxs-lookup"><span data-stu-id="790fb-546">no</span></span>           |
| <span data-ttu-id="790fb-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="790fb-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="790fb-548">no</span><span class="sxs-lookup"><span data-stu-id="790fb-548">no</span></span>             | <span data-ttu-id="790fb-549">no</span><span class="sxs-lookup"><span data-stu-id="790fb-549">no</span></span>           |
| <span data-ttu-id="790fb-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="790fb-550">msdyn_duration</span></span>                         | <span data-ttu-id="790fb-551">no</span><span class="sxs-lookup"><span data-stu-id="790fb-551">no</span></span>             | <span data-ttu-id="790fb-552">no</span><span class="sxs-lookup"><span data-stu-id="790fb-552">no</span></span>           |
| <span data-ttu-id="790fb-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="790fb-553">msdyn_effort</span></span>                           | <span data-ttu-id="790fb-554">no</span><span class="sxs-lookup"><span data-stu-id="790fb-554">no</span></span>             | <span data-ttu-id="790fb-555">no</span><span class="sxs-lookup"><span data-stu-id="790fb-555">no</span></span>           |
| <span data-ttu-id="790fb-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="790fb-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="790fb-557">no</span><span class="sxs-lookup"><span data-stu-id="790fb-557">no</span></span>             | <span data-ttu-id="790fb-558">no</span><span class="sxs-lookup"><span data-stu-id="790fb-558">no</span></span>           |
| <span data-ttu-id="790fb-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="790fb-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="790fb-560">no</span><span class="sxs-lookup"><span data-stu-id="790fb-560">no</span></span>             | <span data-ttu-id="790fb-561">no</span><span class="sxs-lookup"><span data-stu-id="790fb-561">no</span></span>           |
| <span data-ttu-id="790fb-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="790fb-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="790fb-563">no</span><span class="sxs-lookup"><span data-stu-id="790fb-563">no</span></span>             | <span data-ttu-id="790fb-564">no</span><span class="sxs-lookup"><span data-stu-id="790fb-564">no</span></span>           |
| <span data-ttu-id="790fb-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="790fb-565">msdyn_finish</span></span>                           | <span data-ttu-id="790fb-566">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-566">yes</span></span>            | <span data-ttu-id="790fb-567">sì</span><span class="sxs-lookup"><span data-stu-id="790fb-567">yes</span></span>          |
| <span data-ttu-id="790fb-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="790fb-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="790fb-569">no</span><span class="sxs-lookup"><span data-stu-id="790fb-569">no</span></span>             | <span data-ttu-id="790fb-570">no</span><span class="sxs-lookup"><span data-stu-id="790fb-570">no</span></span>           |
| <span data-ttu-id="790fb-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="790fb-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="790fb-572">no</span><span class="sxs-lookup"><span data-stu-id="790fb-572">no</span></span>             | <span data-ttu-id="790fb-573">no</span><span class="sxs-lookup"><span data-stu-id="790fb-573">no</span></span>           |
| <span data-ttu-id="790fb-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="790fb-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="790fb-575">no</span><span class="sxs-lookup"><span data-stu-id="790fb-575">no</span></span>             | <span data-ttu-id="790fb-576">no</span><span class="sxs-lookup"><span data-stu-id="790fb-576">no</span></span>           |
| <span data-ttu-id="790fb-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="790fb-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="790fb-578">no</span><span class="sxs-lookup"><span data-stu-id="790fb-578">no</span></span>             | <span data-ttu-id="790fb-579">no</span><span class="sxs-lookup"><span data-stu-id="790fb-579">no</span></span>           |
| <span data-ttu-id="790fb-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="790fb-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="790fb-581">no</span><span class="sxs-lookup"><span data-stu-id="790fb-581">no</span></span>             | <span data-ttu-id="790fb-582">no</span><span class="sxs-lookup"><span data-stu-id="790fb-582">no</span></span>           |
| <span data-ttu-id="790fb-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="790fb-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="790fb-584">no</span><span class="sxs-lookup"><span data-stu-id="790fb-584">no</span></span>             | <span data-ttu-id="790fb-585">no</span><span class="sxs-lookup"><span data-stu-id="790fb-585">no</span></span>           |
| <span data-ttu-id="790fb-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="790fb-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="790fb-587">no</span><span class="sxs-lookup"><span data-stu-id="790fb-587">no</span></span>             | <span data-ttu-id="790fb-588">no</span><span class="sxs-lookup"><span data-stu-id="790fb-588">no</span></span>           |
| <span data-ttu-id="790fb-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="790fb-590">no</span><span class="sxs-lookup"><span data-stu-id="790fb-590">no</span></span>             | <span data-ttu-id="790fb-591">no</span><span class="sxs-lookup"><span data-stu-id="790fb-591">no</span></span>           |
| <span data-ttu-id="790fb-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="790fb-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="790fb-593">no</span><span class="sxs-lookup"><span data-stu-id="790fb-593">no</span></span>             | <span data-ttu-id="790fb-594">no</span><span class="sxs-lookup"><span data-stu-id="790fb-594">no</span></span>           |
| <span data-ttu-id="790fb-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="790fb-596">no</span><span class="sxs-lookup"><span data-stu-id="790fb-596">no</span></span>             | <span data-ttu-id="790fb-597">no</span><span class="sxs-lookup"><span data-stu-id="790fb-597">no</span></span>           |
| <span data-ttu-id="790fb-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="790fb-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="790fb-599">no</span><span class="sxs-lookup"><span data-stu-id="790fb-599">no</span></span>             | <span data-ttu-id="790fb-600">no</span><span class="sxs-lookup"><span data-stu-id="790fb-600">no</span></span>           |
| <span data-ttu-id="790fb-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="790fb-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="790fb-602">no</span><span class="sxs-lookup"><span data-stu-id="790fb-602">no</span></span>             | <span data-ttu-id="790fb-603">no</span><span class="sxs-lookup"><span data-stu-id="790fb-603">no</span></span>           |
| <span data-ttu-id="790fb-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="790fb-604">msdyn_progress</span></span>                         | <span data-ttu-id="790fb-605">no</span><span class="sxs-lookup"><span data-stu-id="790fb-605">no</span></span>             | <span data-ttu-id="790fb-606">no</span><span class="sxs-lookup"><span data-stu-id="790fb-606">no</span></span>           |
| <span data-ttu-id="790fb-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="790fb-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="790fb-608">no</span><span class="sxs-lookup"><span data-stu-id="790fb-608">no</span></span>             | <span data-ttu-id="790fb-609">no</span><span class="sxs-lookup"><span data-stu-id="790fb-609">no</span></span>           |
| <span data-ttu-id="790fb-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="790fb-611">no</span><span class="sxs-lookup"><span data-stu-id="790fb-611">no</span></span>             | <span data-ttu-id="790fb-612">no</span><span class="sxs-lookup"><span data-stu-id="790fb-612">no</span></span>           |
| <span data-ttu-id="790fb-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="790fb-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="790fb-614">no</span><span class="sxs-lookup"><span data-stu-id="790fb-614">no</span></span>             | <span data-ttu-id="790fb-615">no</span><span class="sxs-lookup"><span data-stu-id="790fb-615">no</span></span>           |
| <span data-ttu-id="790fb-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="790fb-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="790fb-617">no</span><span class="sxs-lookup"><span data-stu-id="790fb-617">no</span></span>             | <span data-ttu-id="790fb-618">no</span><span class="sxs-lookup"><span data-stu-id="790fb-618">no</span></span>           |
| <span data-ttu-id="790fb-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="790fb-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="790fb-620">no</span><span class="sxs-lookup"><span data-stu-id="790fb-620">no</span></span>             | <span data-ttu-id="790fb-621">no</span><span class="sxs-lookup"><span data-stu-id="790fb-621">no</span></span>           |
| <span data-ttu-id="790fb-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="790fb-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="790fb-623">no</span><span class="sxs-lookup"><span data-stu-id="790fb-623">no</span></span>             | <span data-ttu-id="790fb-624">no</span><span class="sxs-lookup"><span data-stu-id="790fb-624">no</span></span>           |
| <span data-ttu-id="790fb-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="790fb-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="790fb-626">no</span><span class="sxs-lookup"><span data-stu-id="790fb-626">no</span></span>             | <span data-ttu-id="790fb-627">no</span><span class="sxs-lookup"><span data-stu-id="790fb-627">no</span></span>           |
| <span data-ttu-id="790fb-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="790fb-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="790fb-629">no</span><span class="sxs-lookup"><span data-stu-id="790fb-629">no</span></span>             | <span data-ttu-id="790fb-630">no</span><span class="sxs-lookup"><span data-stu-id="790fb-630">no</span></span>           |
| <span data-ttu-id="790fb-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="790fb-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="790fb-632">no</span><span class="sxs-lookup"><span data-stu-id="790fb-632">no</span></span>             | <span data-ttu-id="790fb-633">no</span><span class="sxs-lookup"><span data-stu-id="790fb-633">no</span></span>           |
| <span data-ttu-id="790fb-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="790fb-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="790fb-635">no</span><span class="sxs-lookup"><span data-stu-id="790fb-635">no</span></span>             | <span data-ttu-id="790fb-636">no</span><span class="sxs-lookup"><span data-stu-id="790fb-636">no</span></span>           |
| <span data-ttu-id="790fb-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="790fb-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="790fb-638">no</span><span class="sxs-lookup"><span data-stu-id="790fb-638">no</span></span>             | <span data-ttu-id="790fb-639">no</span><span class="sxs-lookup"><span data-stu-id="790fb-639">no</span></span>           |
| <span data-ttu-id="790fb-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="790fb-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="790fb-641">no</span><span class="sxs-lookup"><span data-stu-id="790fb-641">no</span></span>             | <span data-ttu-id="790fb-642">no</span><span class="sxs-lookup"><span data-stu-id="790fb-642">no</span></span>           |
| <span data-ttu-id="790fb-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="790fb-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="790fb-644">no</span><span class="sxs-lookup"><span data-stu-id="790fb-644">no</span></span>             | <span data-ttu-id="790fb-645">no</span><span class="sxs-lookup"><span data-stu-id="790fb-645">no</span></span>           |
| <span data-ttu-id="790fb-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="790fb-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="790fb-647">no</span><span class="sxs-lookup"><span data-stu-id="790fb-647">no</span></span>             | <span data-ttu-id="790fb-648">no</span><span class="sxs-lookup"><span data-stu-id="790fb-648">no</span></span>           |
| <span data-ttu-id="790fb-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="790fb-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="790fb-650">no</span><span class="sxs-lookup"><span data-stu-id="790fb-650">no</span></span>             | <span data-ttu-id="790fb-651">no</span><span class="sxs-lookup"><span data-stu-id="790fb-651">no</span></span>           |
| <span data-ttu-id="790fb-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="790fb-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="790fb-653">no</span><span class="sxs-lookup"><span data-stu-id="790fb-653">no</span></span>             | <span data-ttu-id="790fb-654">no</span><span class="sxs-lookup"><span data-stu-id="790fb-654">no</span></span>           |
| <span data-ttu-id="790fb-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="790fb-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="790fb-656">no</span><span class="sxs-lookup"><span data-stu-id="790fb-656">no</span></span>             | <span data-ttu-id="790fb-657">no</span><span class="sxs-lookup"><span data-stu-id="790fb-657">no</span></span>           |
| <span data-ttu-id="790fb-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="790fb-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="790fb-659">no</span><span class="sxs-lookup"><span data-stu-id="790fb-659">no</span></span>             | <span data-ttu-id="790fb-660">no</span><span class="sxs-lookup"><span data-stu-id="790fb-660">no</span></span>           |
| <span data-ttu-id="790fb-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="790fb-662">no</span><span class="sxs-lookup"><span data-stu-id="790fb-662">no</span></span>             | <span data-ttu-id="790fb-663">no</span><span class="sxs-lookup"><span data-stu-id="790fb-663">no</span></span>           |
| <span data-ttu-id="790fb-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="790fb-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="790fb-665">no</span><span class="sxs-lookup"><span data-stu-id="790fb-665">no</span></span>             | <span data-ttu-id="790fb-666">no</span><span class="sxs-lookup"><span data-stu-id="790fb-666">no</span></span>           |
| <span data-ttu-id="790fb-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="790fb-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="790fb-668">no</span><span class="sxs-lookup"><span data-stu-id="790fb-668">no</span></span>             | <span data-ttu-id="790fb-669">no</span><span class="sxs-lookup"><span data-stu-id="790fb-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="790fb-670">Limitazioni e problemi noti</span><span class="sxs-lookup"><span data-stu-id="790fb-670">Limitations and known issues</span></span>
<span data-ttu-id="790fb-671">Di seguito è riportato un elenco di limitazioni e problemi noti:</span><span class="sxs-lookup"><span data-stu-id="790fb-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="790fb-672">Le API di pianificazione possono essere utilizzate solo da **utenti con licenza Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="790fb-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="790fb-673">Non possono essere utilizzate da:</span><span class="sxs-lookup"><span data-stu-id="790fb-673">They can't be used by:</span></span>
    - <span data-ttu-id="790fb-674">Utenti dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="790fb-674">Application users</span></span>
    - <span data-ttu-id="790fb-675">Utenti di sistema</span><span class="sxs-lookup"><span data-stu-id="790fb-675">System users</span></span>
    - <span data-ttu-id="790fb-676">Utenti integrazione</span><span class="sxs-lookup"><span data-stu-id="790fb-676">Integration users</span></span>
    - <span data-ttu-id="790fb-677">Altri utenti che non dispongono della licenza richiesta</span><span class="sxs-lookup"><span data-stu-id="790fb-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="790fb-678">Ogni **OperationSet** può avere un massimo di 100 operazioni.</span><span class="sxs-lookup"><span data-stu-id="790fb-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="790fb-679">Ogni utente può avere un massimo di 10 **OperationSets** aperti.</span><span class="sxs-lookup"><span data-stu-id="790fb-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="790fb-680">Project Operations attualmente supporta un massimo di 500 attività totali in un progetto.</span><span class="sxs-lookup"><span data-stu-id="790fb-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="790fb-681">Lo stato di errore e i registri degli errori di **OperationSet** non sono attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="790fb-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="790fb-682">Limiti e confini per progetti e attività</span><span class="sxs-lookup"><span data-stu-id="790fb-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="790fb-683">Gestione errori</span><span class="sxs-lookup"><span data-stu-id="790fb-683">Error handling</span></span>

   - <span data-ttu-id="790fb-684">Per rivedere gli errori generati dai set di operazioni, vai a **Impostazioni** \> **Pianifica integrazione** \> **Set di operazioni**.</span><span class="sxs-lookup"><span data-stu-id="790fb-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="790fb-685">Per esaminare gli errori generati dal servizio di pianificazione del progetto, vai a **Impostazioni** \> **Pianifica integrazione** \> **Registri errori PSS**.</span><span class="sxs-lookup"><span data-stu-id="790fb-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="790fb-686">Scenario di esempio</span><span class="sxs-lookup"><span data-stu-id="790fb-686">Sample scenario</span></span>

<span data-ttu-id="790fb-687">In questo scenario, creerai un progetto, un membro del team, quattro attività e due assegnazioni di risorse.</span><span class="sxs-lookup"><span data-stu-id="790fb-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="790fb-688">Successivamente, aggiornerai un'attività e il progetto, eliminerai un'attività e un'assegnazione di risorse e creerai una dipendenza attività.</span><span class="sxs-lookup"><span data-stu-id="790fb-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="790fb-689">Esempi aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="790fb-689">Additional samples</span></span>

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
