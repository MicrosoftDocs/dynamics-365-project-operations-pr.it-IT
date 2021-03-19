---
title: Modifiche alla gestione delle risorse (Project Service Automation 3.x)
description: In questo argomento vengono fornite informazioni sulle modifiche all'area Gestione risorse.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284768"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="d2333-103">Modifiche alla gestione delle risorse (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="d2333-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="d2333-104">Le sezioni di questo argomento forniscono informazioni sulle modifiche apportate all'area Gestione risorse di Dynamics 365 Project Service Automation versione 3.x.</span><span class="sxs-lookup"><span data-stu-id="d2333-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="d2333-105">Stime di progetto</span><span class="sxs-lookup"><span data-stu-id="d2333-105">Project estimates</span></span>

<span data-ttu-id="d2333-106">Anziché essere basate sull'entità **msdyn\_projecttask** (**Attività di progetto**), le stime di progetto sono basate sull'entità **msdyn\_resourceassignment** (**Assegnazione risorse**).</span><span class="sxs-lookup"><span data-stu-id="d2333-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="d2333-107">Le assegnazioni delle risorse sono diventate un'"origine di riferimento" per la pianificazione delle attività e la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="d2333-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="d2333-108">Attività riga</span><span class="sxs-lookup"><span data-stu-id="d2333-108">Line tasks</span></span>

<span data-ttu-id="d2333-109">In PSA 3.x, le attività riga sono obsolete (deprecate).</span><span class="sxs-lookup"><span data-stu-id="d2333-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="d2333-110">Le assegnazioni ora puntano all'intera attività anziché alle righe attività.</span><span class="sxs-lookup"><span data-stu-id="d2333-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="d2333-111">Nell'esempio seguente viene illustrato come un'attività denominata "Attività di test" viene assegnata ai membri del team A e B nelle versioni precedenti di PSA e in PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="d2333-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="d2333-112">**Prima di PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="d2333-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="d2333-113">Attività di test</span><span class="sxs-lookup"><span data-stu-id="d2333-113">Test task</span></span>

        - <span data-ttu-id="d2333-114">Attività di test - Attività riga 1</span><span class="sxs-lookup"><span data-stu-id="d2333-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="d2333-115">Assegnazione a A</span><span class="sxs-lookup"><span data-stu-id="d2333-115">Assignment to A</span></span>

        - <span data-ttu-id="d2333-116">Attività di test - Attività riga 2</span><span class="sxs-lookup"><span data-stu-id="d2333-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="d2333-117">Assegnazione a B</span><span class="sxs-lookup"><span data-stu-id="d2333-117">Assignment to B</span></span>

- <span data-ttu-id="d2333-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="d2333-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="d2333-119">Attività di test</span><span class="sxs-lookup"><span data-stu-id="d2333-119">Test task</span></span>

        - <span data-ttu-id="d2333-120">Assegnazione a A</span><span class="sxs-lookup"><span data-stu-id="d2333-120">Assignment to A</span></span>
        - <span data-ttu-id="d2333-121">Assegnazione a B</span><span class="sxs-lookup"><span data-stu-id="d2333-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="d2333-122">Assegnazione non assegnata</span><span class="sxs-lookup"><span data-stu-id="d2333-122">Unassigned assignment</span></span>

<span data-ttu-id="d2333-123">In PSA 3.x, un'assegnazione non assegnata è un'assegnazione che viene assegnata a un membro del team **NULL** e a una risorsa **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d2333-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="d2333-124">È possibile avere assegnazioni non assegnate in un paio di scenari:</span><span class="sxs-lookup"><span data-stu-id="d2333-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="d2333-125">Se un'attività è stata creata, ma non è ancora stata assegnata a un membro del team, viene sempre creata un'assegnazione non assegnata.</span><span class="sxs-lookup"><span data-stu-id="d2333-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="d2333-126">Se tutti gli assegnatari di un'attività vengono rimossi, un'attività non assegnata viene ricreata per quell'attività.</span><span class="sxs-lookup"><span data-stu-id="d2333-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="d2333-127">Pianificare campi nell'entità Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="d2333-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="d2333-128">I campi dell'entità **msdyn\_projecttask** sono stati deprecati o spostati nell'entità **msdyn\_resourceassignment**, oppure vi si fa riferimento dall'entità **msdyn\_projectteam** entity (**Membro del team di progetto**).</span><span class="sxs-lookup"><span data-stu-id="d2333-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="d2333-129">Campo deprecato in msdyn\_projecttask (Attività di progetto)</span><span class="sxs-lookup"><span data-stu-id="d2333-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="d2333-130">Nuovo campo in msdyn\_resourceassignment (Assegnazione risorse)</span><span class="sxs-lookup"><span data-stu-id="d2333-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="d2333-131">Commento</span><span class="sxs-lookup"><span data-stu-id="d2333-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="d2333-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="d2333-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="d2333-133">Nessuna</span><span class="sxs-lookup"><span data-stu-id="d2333-133">None</span></span> | |
| <span data-ttu-id="d2333-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="d2333-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="d2333-135">Nessuna</span><span class="sxs-lookup"><span data-stu-id="d2333-135">None</span></span> | |
| <span data-ttu-id="d2333-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="d2333-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="d2333-137">Nessuna</span><span class="sxs-lookup"><span data-stu-id="d2333-137">None</span></span> | |
| <span data-ttu-id="d2333-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="d2333-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="d2333-139">Nessuna</span><span class="sxs-lookup"><span data-stu-id="d2333-139">None</span></span> | |
| <span data-ttu-id="d2333-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="d2333-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="d2333-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="d2333-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="d2333-142">Il formato di una struttura di dati JavaScript Object Notation (JSON) archiviato nel campo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="d2333-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="d2333-143">Profilo di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d2333-143">Schedule contour</span></span>

<span data-ttu-id="d2333-144">Il profilo di pianificazione è archiviato nel campo **Lavoro pianificato** (**msdyn\_plannedwork**) di ogni entità **Assegnazione risorse** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="d2333-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="d2333-145">Struttura</span><span class="sxs-lookup"><span data-stu-id="d2333-145">Structure</span></span>

<span data-ttu-id="d2333-146">La nuova struttura del profilo di pianificazione presenta periodi di tempo flessibili definiti per ogni giorno della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d2333-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="d2333-147">Ogni periodo di tempo ha le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2333-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="d2333-148">**Inizio** - L'inizio delle ore lavorative del giorno, a seconda del calendario di progetto.</span><span class="sxs-lookup"><span data-stu-id="d2333-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="d2333-149">**Fine** - La fine delle ore lavorative del giorno, a seconda del calendario di progetto.</span><span class="sxs-lookup"><span data-stu-id="d2333-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="d2333-150">**Ore** - Il numero di ore assegnate in un giorno.</span><span class="sxs-lookup"><span data-stu-id="d2333-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="d2333-151">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d2333-151">**Example**</span></span>

<span data-ttu-id="d2333-152">In questo esempio viene utilizzato un calendario di progetto in cui il giorno lavorativo è dalle 9 alle 17 nel fuso orario UTC-8.</span><span class="sxs-lookup"><span data-stu-id="d2333-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="d2333-153">Pianificazione automatica e pianificazione manuale</span><span class="sxs-lookup"><span data-stu-id="d2333-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="d2333-154">Se un'attività viene pianificata automaticamente, le ore sono caricate in anticipo e la durata dell'attività potrebbe essere ridotta.</span><span class="sxs-lookup"><span data-stu-id="d2333-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="d2333-155">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d2333-155">**Example**</span></span>

<span data-ttu-id="d2333-156">L'attività seguente è pianificata automaticamente per 18 ore su tre giorni (dal 3 dicembre 2018 al 5 dicembre 2018).</span><span class="sxs-lookup"><span data-stu-id="d2333-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="d2333-157">Se un'attività viene pianificata manualmente, le ore sono distribuite uniformemente a tutte le date.</span><span class="sxs-lookup"><span data-stu-id="d2333-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="d2333-158">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d2333-158">**Example**</span></span>

<span data-ttu-id="d2333-159">L'attività seguente è pianificata manualmente per 18 su tre giorni (dal 3 dicembre 2018 al 5 dicembre 2018).</span><span class="sxs-lookup"><span data-stu-id="d2333-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="d2333-160">Unità assegnazione</span><span class="sxs-lookup"><span data-stu-id="d2333-160">Assignment unit</span></span>

<span data-ttu-id="d2333-161">L'unità assegnazione è stata deprecata in PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="d2333-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="d2333-162">Le ore di lavoro richiesto dell'attività sono ora divise equamente, per giorno, tra tutte le risorse assegnate.</span><span class="sxs-lookup"><span data-stu-id="d2333-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="d2333-163">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d2333-163">**Example**</span></span>

<span data-ttu-id="d2333-164">In questo esempio, l'attività viene assegnata a due risorse e viene pianificata automaticamente per 36 ore su tre giorni (dal 3 dicembre 2018 al 5 dicembre 2018).</span><span class="sxs-lookup"><span data-stu-id="d2333-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="d2333-165">Assegnazione 1:</span><span class="sxs-lookup"><span data-stu-id="d2333-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="d2333-166">Assegnazione 2:</span><span class="sxs-lookup"><span data-stu-id="d2333-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="d2333-167">Dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="d2333-167">Pricing dimensions</span></span>

<span data-ttu-id="d2333-168">In PSA 3.x, i campi delle dimensioni di determinazione dei prezzi specifici delle risorse (come **Ruolo** e **Unità organizzativa**) sono stati rimossi dall'entità **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="d2333-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="d2333-169">Questi campi possono ora essere recuperati dal membro del team di progetto corrispondente (**msdyn\_projectteam**) dell'assegnazione delle risorse (**msdyn\_resourceassignment**) quando vengono generate le stime di progetto.</span><span class="sxs-lookup"><span data-stu-id="d2333-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="d2333-170">Un nuovo campo, **msdyn\_organizationalunit**, è stato aggiunto all'entità **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="d2333-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="d2333-171">Campo deprecato in msdyn\_projecttask (Attività di progetto)</span><span class="sxs-lookup"><span data-stu-id="d2333-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="d2333-172">Al suo posto viene utilizzato il campo msdyn\_projectteam (Membro del team di progetto)</span><span class="sxs-lookup"><span data-stu-id="d2333-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="d2333-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="d2333-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="d2333-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="d2333-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="d2333-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="d2333-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="d2333-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="d2333-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="d2333-177">Profili di distribuzione</span><span class="sxs-lookup"><span data-stu-id="d2333-177">Contours</span></span>

<span data-ttu-id="d2333-178">I campi del profilo di stima e di determinazione dei prezzi sono stati deprecati nell'entità **msdyn\_projecttask** .</span><span class="sxs-lookup"><span data-stu-id="d2333-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="d2333-179">Sono stati spostati nell'entità **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="d2333-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="d2333-180">Campo deprecato in msdyn\_projecttask (Attività di progetto)</span><span class="sxs-lookup"><span data-stu-id="d2333-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="d2333-181">Nuovo campo in msdyn\_resourceassignment (Assegnazione risorse)</span><span class="sxs-lookup"><span data-stu-id="d2333-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="d2333-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="d2333-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="d2333-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="d2333-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="d2333-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="d2333-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="d2333-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="d2333-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="d2333-186">I campi seguenti sono stati aggiunti all'entità **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="d2333-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="d2333-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d2333-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="d2333-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d2333-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="d2333-189">I campi seguenti per costi e vendite pianificati, effettivi e rimanenti rimangono invariati nell'entità **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="d2333-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="d2333-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d2333-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="d2333-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d2333-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="d2333-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="d2333-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="d2333-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="d2333-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="d2333-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="d2333-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="d2333-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="d2333-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]