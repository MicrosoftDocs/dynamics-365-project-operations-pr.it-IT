---
title: Considerazioni sull'aggiornamento della struttura di suddivisione del lavoro
description: In questo argomento vengono fornite informazioni sull'aggiornamento della struttura di suddivisione del lavoro da Project Service Automation 2.x a 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005616"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="7def9-103">Considerazioni sull'aggiornamento della struttura di suddivisione del lavoro</span><span class="sxs-lookup"><span data-stu-id="7def9-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7def9-104">In questo argomento vengono fornite informazioni sull'aggiornamento della struttura di suddivisione del lavoro da Project Service Automation 2.x a 3.x.</span><span class="sxs-lookup"><span data-stu-id="7def9-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="7def9-105">In questo argomento viene definito lo stato di integrità di un progetto in Project Service Automation (PSA) che è necessario per un aggiornamento corretto.</span><span class="sxs-lookup"><span data-stu-id="7def9-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="7def9-106">Sono inoltre fornite informazioni sulle condizioni di blocco comuni che rendono impossibile l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7def9-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="7def9-107">Per ulteriori informazioni sulla definizione delle attività di progetto e le relative funzioni in una pianificazione di progetto, vedi [Pianificazioni di progetto](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="7def9-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="7def9-108">Entità chiave</span><span class="sxs-lookup"><span data-stu-id="7def9-108">Key entities</span></span>
<span data-ttu-id="7def9-109">Per una struttura di suddivisione del lavoro accurata già caricata con le risorse, sono necessarie le entità seguenti:</span><span class="sxs-lookup"><span data-stu-id="7def9-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="7def9-110">Progetto</span><span class="sxs-lookup"><span data-stu-id="7def9-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="7def9-111">Team di progetto</span><span class="sxs-lookup"><span data-stu-id="7def9-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="7def9-112">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="7def9-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="7def9-113">Assegnazioni di risorse</span><span class="sxs-lookup"><span data-stu-id="7def9-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="7def9-114">Dipendenza attività di progetto</span><span class="sxs-lookup"><span data-stu-id="7def9-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="7def9-115">Risorse prenotabili</span><span class="sxs-lookup"><span data-stu-id="7def9-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="7def9-116">Per definire una struttura di suddivisione del lavoro caricata con risorse, devi completare i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7def9-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="7def9-117">Creare un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="7def9-117">Create a new project.</span></span> <span data-ttu-id="7def9-118">Per ulteriori informazioni su come creare un nuovo progetto, vedi [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="7def9-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="7def9-119">Creare una o più attività.</span><span class="sxs-lookup"><span data-stu-id="7def9-119">Create one or more tasks.</span></span> <span data-ttu-id="7def9-120">Per ulteriori informazioni su come creare un'attività, vedi [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="7def9-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="7def9-121">Definire le dipendenze delle attività.</span><span class="sxs-lookup"><span data-stu-id="7def9-121">Define the task dependencies.</span></span> <span data-ttu-id="7def9-122">Per ulteriori informazioni, vedere [Dipendenza attività di progetto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="7def9-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="7def9-123">Assegnare membri del team di progetto al progetto.</span><span class="sxs-lookup"><span data-stu-id="7def9-123">Assign project team members to the project.</span></span> <span data-ttu-id="7def9-124">Per ulteriori informazioni, vedi l'[msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="7def9-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="7def9-125">Assegnare membri del team di progetto alle attività.</span><span class="sxs-lookup"><span data-stu-id="7def9-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="7def9-126">Per ulteriori informazioni, vedi l'[msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="7def9-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="7def9-127">Relazioni del team di progetto</span><span class="sxs-lookup"><span data-stu-id="7def9-127">Project team relationships</span></span>

<span data-ttu-id="7def9-128">Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:</span><span class="sxs-lookup"><span data-stu-id="7def9-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="7def9-129">Tutti i membri del team di progetto devono essere associati a una risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="7def9-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="7def9-130">Tutti i membri del team di progetto devono essere associati allo stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="7def9-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="7def9-131">Relazioni delle attività di progetto</span><span class="sxs-lookup"><span data-stu-id="7def9-131">Project task relationships</span></span>
<span data-ttu-id="7def9-132">Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:</span><span class="sxs-lookup"><span data-stu-id="7def9-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="7def9-133">Tutte le attività correlate devono essere associate allo stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="7def9-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="7def9-134">Ogni attività riga deve avere un'attività padre.</span><span class="sxs-lookup"><span data-stu-id="7def9-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="7def9-135">Ogni attività deve avere un progetto padre.</span><span class="sxs-lookup"><span data-stu-id="7def9-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="7def9-136">Condizioni valide</span><span class="sxs-lookup"><span data-stu-id="7def9-136">Valid conditions</span></span>

- <span data-ttu-id="7def9-137">Tutte le durate delle attività devono essere superiori o uguali a (>=) un'ora e inferiori a 1.800.000 minuti (1.250 giorni).\*</span><span class="sxs-lookup"><span data-stu-id="7def9-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="7def9-138">Tutte le attività devono avere una data di inizio successiva a 01/01/2000.\*</span><span class="sxs-lookup"><span data-stu-id="7def9-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="7def9-139">Tutte le attività devono avere una data di inizio che rientra in un periodo di 17 anni a partire dalla data odierna.\*</span><span class="sxs-lookup"><span data-stu-id="7def9-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="7def9-140">Tutte le attività devono avere una data di inizio antecedente o corrispondente alla data di fine.</span><span class="sxs-lookup"><span data-stu-id="7def9-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="7def9-141">Tutti i tipi di transazioni nelle classificazioni (Spese, Materiale, Imposta e Tempo) devono avere valori per **Unità predefinita** e **Unità di vendita**.</span><span class="sxs-lookup"><span data-stu-id="7def9-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="7def9-142">I formati delle date con lettere devono essere evitati.</span><span class="sxs-lookup"><span data-stu-id="7def9-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="7def9-143">Passaggi di mitigazione potenziali</span><span class="sxs-lookup"><span data-stu-id="7def9-143">Potential mitigation steps</span></span>
- <span data-ttu-id="7def9-144">Utilizzare la ricerca avanzata per identificare le attività del progetto che non contengono un ID progetto.</span><span class="sxs-lookup"><span data-stu-id="7def9-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="7def9-145">Utilizzare la ricerca avanzata per identificare le attività del progetto in cui la durata pianificata è maggiore di >1.800.000.</span><span class="sxs-lookup"><span data-stu-id="7def9-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="7def9-146">Prima di apportare eventuali modifiche ai dati, è necessario esaminare le personalizzazioni associate all'entità che potrebbero aver danneggiato i dati.</span><span class="sxs-lookup"><span data-stu-id="7def9-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="7def9-147">Queste personalizzazioni devono essere risolte prima di procedere con eventuali aggiornamenti relativi ai dati.</span><span class="sxs-lookup"><span data-stu-id="7def9-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="7def9-148">Per le attività identificate che sono rimaste orfane, considerare la possibilità di eliminare queste attività se non sono necessarie o se devono essere associate al progetto padre corretto.</span><span class="sxs-lookup"><span data-stu-id="7def9-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="7def9-149">Per qualsiasi attività in cui la durata è superiore a 1.250 giorni, prendere in considerazione l'aggiunta di più attività per rappresentare la durata totale, se possibile.</span><span class="sxs-lookup"><span data-stu-id="7def9-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="7def9-150">Le condizioni contrassegnate con un asterisco (\*) presentano limiti dovuti al fatto che Customer Relationship Management (CRM) supporta solo 7.320 espansioni di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="7def9-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="7def9-151">È necessario rimanere al di sotto di tale limite.</span><span class="sxs-lookup"><span data-stu-id="7def9-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="7def9-152">Relazioni delle assegnazioni di risorse</span><span class="sxs-lookup"><span data-stu-id="7def9-152">Resource Assignment relationships</span></span>
<span data-ttu-id="7def9-153">Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:</span><span class="sxs-lookup"><span data-stu-id="7def9-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="7def9-154">Tutte le assegnazioni di risorse in una struttura di suddivisione del lavoro devono essere correlate allo stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="7def9-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="7def9-155">Tutte le assegnazioni di risorse in una struttura di suddivisione del lavoro devono essere associate ai membri del team di progetto nello stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="7def9-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="7def9-156">Passaggi di mitigazione potenziali</span><span class="sxs-lookup"><span data-stu-id="7def9-156">Potential mitigation steps</span></span>
- <span data-ttu-id="7def9-157">Identificare tutte le attività che non rientrano nelle condizioni sopra descritte.</span><span class="sxs-lookup"><span data-stu-id="7def9-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="7def9-158">Eventuali assegnazioni di risorse non più valide devono essere eliminate.</span><span class="sxs-lookup"><span data-stu-id="7def9-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="7def9-159">Relazioni delle dipendenze delle attività di progetto</span><span class="sxs-lookup"><span data-stu-id="7def9-159">Project task dependency relationships</span></span>
<span data-ttu-id="7def9-160">Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:</span><span class="sxs-lookup"><span data-stu-id="7def9-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="7def9-161">Tutte le dipendenze delle attività di progetto devono essere correlate allo stesso progetto.</span><span class="sxs-lookup"><span data-stu-id="7def9-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="7def9-162">Non è possibile avere più riferimenti alla stessa dipendenza di un'attività.</span><span class="sxs-lookup"><span data-stu-id="7def9-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]