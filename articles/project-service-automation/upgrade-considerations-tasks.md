---
title: Considerazioni sull'aggiornamento della struttura di suddivisione del lavoro
description: In questo argomento vengono fornite informazioni sull'aggiornamento della struttura di suddivisione del lavoro da Project Service Automation 2.x a 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752682"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="d1c30-103">Considerazioni sull'aggiornamento della struttura di suddivisione del lavoro</span><span class="sxs-lookup"><span data-stu-id="d1c30-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="d1c30-104">In questo argomento vengono fornite informazioni sull'aggiornamento della struttura di suddivisione del lavoro da Project Service Automation 2.x a 3.x.</span><span class="sxs-lookup"><span data-stu-id="d1c30-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="d1c30-105">In questo argomento viene definito lo stato di integrità di un progetto in Project Service Automation (PSA) che è necessario per un aggiornamento corretto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="d1c30-106">Sono inoltre fornite informazioni sulle condizioni di blocco comuni che rendono impossibile l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d1c30-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="d1c30-107">Per ulteriori informazioni sulla definizione delle attività di progetto e le relative funzioni in una pianificazione di progetto, vedi [Pianificazioni di progetto](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="d1c30-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="d1c30-108">Entità chiave</span><span class="sxs-lookup"><span data-stu-id="d1c30-108">Key entities</span></span>
<span data-ttu-id="d1c30-109">Per una struttura di suddivisione del lavoro accurata già caricata con le risorse, sono necessarie le entità seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1c30-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="d1c30-110">Progetto</span><span class="sxs-lookup"><span data-stu-id="d1c30-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="d1c30-111">Team di progetto</span><span class="sxs-lookup"><span data-stu-id="d1c30-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="d1c30-112">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="d1c30-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="d1c30-113">Assegnazioni di risorse</span><span class="sxs-lookup"><span data-stu-id="d1c30-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="d1c30-114">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="d1c30-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="d1c30-115">Risorse prenotabili</span><span class="sxs-lookup"><span data-stu-id="d1c30-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="d1c30-116">Per definire una struttura di suddivisione del lavoro caricata con risorse, devi completare i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1c30-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="d1c30-117">Creare un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-117">Create a new project.</span></span> <span data-ttu-id="d1c30-118">Per ulteriori informazioni su come creare un nuovo progetto, vedi [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="d1c30-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="d1c30-119">Creare una o più attività.</span><span class="sxs-lookup"><span data-stu-id="d1c30-119">Create one or more tasks.</span></span> <span data-ttu-id="d1c30-120">Per ulteriori informazioni su come creare un'attività, vedi [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="d1c30-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="d1c30-121">Definire le dipendenze delle attività.</span><span class="sxs-lookup"><span data-stu-id="d1c30-121">Define the task dependencies.</span></span> <span data-ttu-id="d1c30-122">Per ulteriori informazioni, vedere [Dipendenza attività di progetto](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="d1c30-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="d1c30-123">Assegnare membri del team di progetto al progetto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-123">Assign project team members to the project.</span></span> <span data-ttu-id="d1c30-124">Per ulteriori informazioni, vedi l'[msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="d1c30-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="d1c30-125">Assegnare membri del team di progetto alle attività.</span><span class="sxs-lookup"><span data-stu-id="d1c30-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="d1c30-126">Per ulteriori informazioni, vedi l'[msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d1c30-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="d1c30-127">Relazioni del team di progetto</span><span class="sxs-lookup"><span data-stu-id="d1c30-127">Project team relationships</span></span>

<span data-ttu-id="d1c30-128">Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:</span><span class="sxs-lookup"><span data-stu-id="d1c30-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="d1c30-129">Tutti i membri del team di progetto devono essere associati a una risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="d1c30-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="d1c30-130">Tutti i membri del team di progetto devono essere associati allo stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="d1c30-131">Relazioni delle attività di progetto</span><span class="sxs-lookup"><span data-stu-id="d1c30-131">Project task relationships</span></span>
<span data-ttu-id="d1c30-132">Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:</span><span class="sxs-lookup"><span data-stu-id="d1c30-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="d1c30-133">Tutte le attività correlate devono essere associate allo stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="d1c30-134">Ogni attività riga deve avere un'attività padre.</span><span class="sxs-lookup"><span data-stu-id="d1c30-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="d1c30-135">Ogni attività deve avere un progetto padre.</span><span class="sxs-lookup"><span data-stu-id="d1c30-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="d1c30-136">Condizioni valide</span><span class="sxs-lookup"><span data-stu-id="d1c30-136">Valid conditions</span></span>

- <span data-ttu-id="d1c30-137">Tutte le durate delle attività devono essere superiori o uguali a (>=) un'ora e inferiori a 1.800.000 minuti (1.250 giorni).\*</span><span class="sxs-lookup"><span data-stu-id="d1c30-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="d1c30-138">Tutte le attività devono avere una data di inizio successiva a 01/01/2000.\*</span><span class="sxs-lookup"><span data-stu-id="d1c30-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="d1c30-139">Tutte le attività devono avere una data di inizio che rientra in un periodo di 17 anni a partire dalla data odierna.\*</span><span class="sxs-lookup"><span data-stu-id="d1c30-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="d1c30-140">Tutte le attività devono avere una data di inizio antecedente o corrispondente alla data di fine.</span><span class="sxs-lookup"><span data-stu-id="d1c30-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="d1c30-141">Tutti i tipi di transazioni nelle classificazioni (Spese, Materiale, Imposta e Tempo) devono avere valori per **Unità predefinita** e **Unità di vendita**.</span><span class="sxs-lookup"><span data-stu-id="d1c30-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="d1c30-142">I formati delle date con lettere devono essere evitati.</span><span class="sxs-lookup"><span data-stu-id="d1c30-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="d1c30-143">Passaggi di mitigazione potenziali</span><span class="sxs-lookup"><span data-stu-id="d1c30-143">Potential mitigation steps</span></span>
- <span data-ttu-id="d1c30-144">Utilizzare la ricerca avanzata per identificare le attività del progetto che non contengono un ID progetto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="d1c30-145">Utilizzare la ricerca avanzata per identificare le attività del progetto in cui la durata pianificata è maggiore di >1.800.000.</span><span class="sxs-lookup"><span data-stu-id="d1c30-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="d1c30-146">Prima di apportare eventuali modifiche ai dati, è necessario esaminare le personalizzazioni associate all'entità che potrebbero aver danneggiato i dati.</span><span class="sxs-lookup"><span data-stu-id="d1c30-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="d1c30-147">Queste personalizzazioni devono essere risolte prima di procedere con eventuali aggiornamenti relativi ai dati.</span><span class="sxs-lookup"><span data-stu-id="d1c30-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="d1c30-148">Per le attività identificate che sono rimaste orfane, considerare la possibilità di eliminare queste attività se non sono necessarie o se devono essere associate al progetto padre corretto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="d1c30-149">Per qualsiasi attività in cui la durata è superiore a 1.250 giorni, prendere in considerazione l'aggiunta di più attività per rappresentare la durata totale, se possibile.</span><span class="sxs-lookup"><span data-stu-id="d1c30-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="d1c30-150">Le condizioni contrassegnate con un asterisco (\*) presentano limiti dovuti al fatto che Customer Relationship Management (CRM) supporta solo 7.320 espansioni di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="d1c30-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="d1c30-151">È necessario rimanere al di sotto di tale limite.</span><span class="sxs-lookup"><span data-stu-id="d1c30-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="d1c30-152">Relazioni delle assegnazioni di risorse</span><span class="sxs-lookup"><span data-stu-id="d1c30-152">Resource Assignment relationships</span></span>
<span data-ttu-id="d1c30-153">Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:</span><span class="sxs-lookup"><span data-stu-id="d1c30-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="d1c30-154">Tutte le assegnazioni di risorse in una struttura di suddivisione del lavoro devono essere correlate allo stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="d1c30-155">Tutte le assegnazioni di risorse in una struttura di suddivisione del lavoro devono essere associate ai membri del team di progetto nello stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="d1c30-156">Passaggi di mitigazione potenziali</span><span class="sxs-lookup"><span data-stu-id="d1c30-156">Potential mitigation steps</span></span>
- <span data-ttu-id="d1c30-157">Identificare tutte le attività che non rientrano nelle condizioni sopra descritte.</span><span class="sxs-lookup"><span data-stu-id="d1c30-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="d1c30-158">Eventuali assegnazioni di risorse non più valide devono essere eliminate.</span><span class="sxs-lookup"><span data-stu-id="d1c30-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="d1c30-159">Relazioni delle dipendenze delle attività di progetto</span><span class="sxs-lookup"><span data-stu-id="d1c30-159">Project task dependency relationships</span></span>
<span data-ttu-id="d1c30-160">Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:</span><span class="sxs-lookup"><span data-stu-id="d1c30-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="d1c30-161">Tutte le dipendenze delle attività di progetto devono essere correlate allo stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="d1c30-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="d1c30-162">Non è possibile avere più riferimenti alla stessa dipendenza di un'attività.</span><span class="sxs-lookup"><span data-stu-id="d1c30-162">A task can't have the same dependency referenced more than once.</span></span>
