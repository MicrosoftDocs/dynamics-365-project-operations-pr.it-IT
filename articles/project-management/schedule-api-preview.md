---
title: Utilizzare API di pianificazione per eseguire operazioni con le entità di pianificazione
description: Questo argomento fornisce informazioni ed esempi sull'utilizzo delle API di pianificazione.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868134"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="8b130-103">Utilizzare API di pianificazione per eseguire operazioni con le entità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8b130-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="8b130-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="8b130-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="8b130-105">L'intera funzionalità, o una sua parte, descritta in questo articolo è disponibile nella versione di anteprima.</span><span class="sxs-lookup"><span data-stu-id="8b130-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="8b130-106">Il contenuto e la funzionalità sono soggetti a modifiche.</span><span class="sxs-lookup"><span data-stu-id="8b130-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="8b130-107">Entità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8b130-107">Scheduling entities</span></span>

<span data-ttu-id="8b130-108">Le API di pianificazione consentono di eseguire operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="8b130-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="8b130-109">Queste entità vengono gestite tramite il motore di pianificazione in Project per il Web.</span><span class="sxs-lookup"><span data-stu-id="8b130-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="8b130-110">Le operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione** erano limitate nelle versioni precedenti di Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8b130-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="8b130-111">La tabella seguente fornisce un elenco completo delle **Entità di pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="8b130-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="8b130-112">Nome dell'entità</span><span class="sxs-lookup"><span data-stu-id="8b130-112">Entity name</span></span>  | <span data-ttu-id="8b130-113">Nome logico entità</span><span class="sxs-lookup"><span data-stu-id="8b130-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="8b130-114">Project</span><span class="sxs-lookup"><span data-stu-id="8b130-114">Project</span></span> | <span data-ttu-id="8b130-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="8b130-115">msdyn_project</span></span> |
| <span data-ttu-id="8b130-116">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="8b130-116">Project Task</span></span>  | <span data-ttu-id="8b130-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="8b130-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="8b130-118">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="8b130-118">Project Task Dependency</span></span>  | <span data-ttu-id="8b130-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="8b130-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="8b130-120">Assegnazione risorse</span><span class="sxs-lookup"><span data-stu-id="8b130-120">Resource Assignment</span></span> | <span data-ttu-id="8b130-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="8b130-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="8b130-122">Bucket di progetto</span><span class="sxs-lookup"><span data-stu-id="8b130-122">Project Bucket</span></span>  | <span data-ttu-id="8b130-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="8b130-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="8b130-124">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="8b130-124">Project Team Member</span></span> | <span data-ttu-id="8b130-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="8b130-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="8b130-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="8b130-126">OperationSet</span></span>

<span data-ttu-id="8b130-127">OperationSet è un modello di unità di lavoro che può essere utilizzato quando in una transazione devono essere elaborate diverse richieste che influiscono sulla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="8b130-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="8b130-128">API di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8b130-128">Schedule APIs</span></span>

<span data-ttu-id="8b130-129">Di seguito è riportato un elenco delle API di pianificazione correnti.</span><span class="sxs-lookup"><span data-stu-id="8b130-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="8b130-130">**msdyn_CreateProjectV1**: questa API può essere utilizzata per creare un progetto.</span><span class="sxs-lookup"><span data-stu-id="8b130-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="8b130-131">Il progetto e il bucket di progetto predefinito vengono creati immediatamente.</span><span class="sxs-lookup"><span data-stu-id="8b130-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="8b130-132">**msdyn_CreateTeamMemberV1**: questa API può essere utilizzata per creare un membro del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="8b130-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="8b130-133">Il record Membro del team viene creato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="8b130-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="8b130-134">**msdyn_CreateOperationSetV1**: questa API può essere utilizzata per pianificare diverse richieste che devono essere eseguite in una transazione.</span><span class="sxs-lookup"><span data-stu-id="8b130-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="8b130-135">**msdyn_PSSCreateV1**: questa API può essere utilizzata per creare un'entità.</span><span class="sxs-lookup"><span data-stu-id="8b130-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="8b130-136">L'entità può essere una qualsiasi delle entità di pianificazione che supportano l'operazione di creazione.</span><span class="sxs-lookup"><span data-stu-id="8b130-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="8b130-137">**msdyn_PSSUpdateV1**: questa API può essere utilizzata per aggiornare un'entità.</span><span class="sxs-lookup"><span data-stu-id="8b130-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="8b130-138">L'entità può essere una qualsiasi delle entità di pianificazione che supportano l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8b130-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="8b130-139">**msdyn_PSSDeleteV1**: questa API può essere utilizzata per eliminare un'entità.</span><span class="sxs-lookup"><span data-stu-id="8b130-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="8b130-140">L'entità può essere una qualsiasi delle entità di pianificazione che supportano l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="8b130-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="8b130-141">**msdyn_ExecuteOperationSetV1**: questa API viene utilizzata per eseguire tutte le operazioni in un determinato set di operazioni.</span><span class="sxs-lookup"><span data-stu-id="8b130-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="8b130-142">Utilizzo delle API di pianificazione con OperationSet</span><span class="sxs-lookup"><span data-stu-id="8b130-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="8b130-143">Poiché i record con **CreateProjectV1** e **CreateTeamMemberV1** vengono creati immediatamente, queste API non possono essere utilizzate direttamente in **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="8b130-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="8b130-144">Tuttavia, puoi utilizzare l'API per creare i record necessari, creare un **OperationSet**, quindi utilizzare questi record predefiniti in **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="8b130-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="8b130-145">Operazioni supportate</span><span class="sxs-lookup"><span data-stu-id="8b130-145">Supported operations</span></span>

| <span data-ttu-id="8b130-146">Entità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8b130-146">Scheduling entity</span></span> | <span data-ttu-id="8b130-147">Creazione di</span><span class="sxs-lookup"><span data-stu-id="8b130-147">Create</span></span> | <span data-ttu-id="8b130-148">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8b130-148">Update</span></span> | <span data-ttu-id="8b130-149">CANC</span><span class="sxs-lookup"><span data-stu-id="8b130-149">Delete</span></span> | <span data-ttu-id="8b130-150">Considerazioni importanti</span><span class="sxs-lookup"><span data-stu-id="8b130-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="8b130-151">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="8b130-151">Project task</span></span> | <span data-ttu-id="8b130-152">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-152">Yes</span></span> | <span data-ttu-id="8b130-153">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-153">Yes</span></span> | <span data-ttu-id="8b130-154">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-154">Yes</span></span> | <span data-ttu-id="8b130-155">Nessuna</span><span class="sxs-lookup"><span data-stu-id="8b130-155">None</span></span> |
| <span data-ttu-id="8b130-156">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="8b130-156">Project task dependency</span></span> | <span data-ttu-id="8b130-157">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-157">Yes</span></span> | <span data-ttu-id="8b130-158">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-158">Yes</span></span> | | <span data-ttu-id="8b130-159">I record Dipendenza attività di progetto non vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="8b130-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="8b130-160">È invece possibile eliminare un vecchio record e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="8b130-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8b130-161">Assegnazione risorse</span><span class="sxs-lookup"><span data-stu-id="8b130-161">Resource assignment</span></span> | <span data-ttu-id="8b130-162">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-162">Yes</span></span> | <span data-ttu-id="8b130-163">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-163">Yes</span></span> | | <span data-ttu-id="8b130-164">Le operazioni con i seguenti campi non sono supportate: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="8b130-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="8b130-165">I record Assegnazione risorse non vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="8b130-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="8b130-166">È invece possibile eliminare il vecchio record e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="8b130-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8b130-167">Bucket di progetto</span><span class="sxs-lookup"><span data-stu-id="8b130-167">Project bucket</span></span> | <span data-ttu-id="8b130-168">N/D</span><span class="sxs-lookup"><span data-stu-id="8b130-168">N/A</span></span> | <span data-ttu-id="8b130-169">N/D</span><span class="sxs-lookup"><span data-stu-id="8b130-169">N/A</span></span> | <span data-ttu-id="8b130-170">N/D</span><span class="sxs-lookup"><span data-stu-id="8b130-170">N/A</span></span> | <span data-ttu-id="8b130-171">Il bucket predefinito viene creato utilizzando l'API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="8b130-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="8b130-172">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="8b130-172">Project team member</span></span> | <span data-ttu-id="8b130-173">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-173">Yes</span></span> | <span data-ttu-id="8b130-174">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-174">Yes</span></span> | <span data-ttu-id="8b130-175">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-175">Yes</span></span> | <span data-ttu-id="8b130-176">Per l'operazione di creazione, utilizza l'API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="8b130-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="8b130-177">Project</span><span class="sxs-lookup"><span data-stu-id="8b130-177">Project</span></span> | <span data-ttu-id="8b130-178">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-178">Yes</span></span> | <span data-ttu-id="8b130-179">Sì</span><span class="sxs-lookup"><span data-stu-id="8b130-179">Yes</span></span> | <span data-ttu-id="8b130-180">N/D</span><span class="sxs-lookup"><span data-stu-id="8b130-180">N/A</span></span> | <span data-ttu-id="8b130-181">Le operazioni con i seguenti campi non sono supportate: : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.</span><span class="sxs-lookup"><span data-stu-id="8b130-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="8b130-182">Queste API possono essere chiamate con oggetti entità che includono campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="8b130-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="8b130-183">La proprietà ID è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="8b130-183">The ID property is optional.</span></span> <span data-ttu-id="8b130-184">Se fornita, il sistema tenta di utilizzarla e genera un'eccezione se non può essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8b130-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="8b130-185">Se non è fornita, il sistema la genererà.</span><span class="sxs-lookup"><span data-stu-id="8b130-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="8b130-186">Limitazioni e problemi noti</span><span class="sxs-lookup"><span data-stu-id="8b130-186">Limitations and known issues</span></span>
<span data-ttu-id="8b130-187">Di seguito è riportato un elenco di limitazioni e problemi noti:</span><span class="sxs-lookup"><span data-stu-id="8b130-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="8b130-188">Le API di pianificazione possono essere utilizzate solo da **utenti con licenza Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="8b130-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="8b130-189">Non possono essere utilizzate da:</span><span class="sxs-lookup"><span data-stu-id="8b130-189">They can't be used by:</span></span>
    - <span data-ttu-id="8b130-190">Utenti dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="8b130-190">Application users</span></span>
    - <span data-ttu-id="8b130-191">Utenti di sistema</span><span class="sxs-lookup"><span data-stu-id="8b130-191">System users</span></span>
    - <span data-ttu-id="8b130-192">Utenti integrazione</span><span class="sxs-lookup"><span data-stu-id="8b130-192">Integration users</span></span>
    - <span data-ttu-id="8b130-193">Altri utenti che non dispongono della licenza richiesta</span><span class="sxs-lookup"><span data-stu-id="8b130-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="8b130-194">Ogni **OperationSet** può avere un massimo di 100 operazioni.</span><span class="sxs-lookup"><span data-stu-id="8b130-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="8b130-195">Ogni utente può avere un massimo di 10 **OperationSets** aperti.</span><span class="sxs-lookup"><span data-stu-id="8b130-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="8b130-196">Project Operations attualmente supporta un massimo di 500 attività totali in un progetto.</span><span class="sxs-lookup"><span data-stu-id="8b130-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="8b130-197">Lo stato di errore e i registri degli errori di **OperationSet** non sono attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="8b130-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="8b130-198">Le API di pianificazione sono in anteprima pubblica.</span><span class="sxs-lookup"><span data-stu-id="8b130-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="8b130-199">L'utilizzo di queste API in un ambiente di produzione non è supportato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b130-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="8b130-200">Scenario di esempio</span><span class="sxs-lookup"><span data-stu-id="8b130-200">Sample scenario</span></span>

<span data-ttu-id="8b130-201">In questo scenario, creerai un progetto, un membro del team, quattro attività e due assegnazioni di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b130-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="8b130-202">Successivamente, aggiornerai un'attività e il progetto, eliminerai un'attività e un'assegnazione di risorse e creerai una dipendenza attività.</span><span class="sxs-lookup"><span data-stu-id="8b130-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="8b130-203">Esempi aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="8b130-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
