---
title: Pianificare un progetto con una struttura di suddivisione del lavoro
description: Come pianificare un progetto con una struttura di suddivisione del lavoro in Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079058"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="54515-103">Pianificare un progetto con una struttura di suddivisione del lavoro (Project Service)</span><span class="sxs-lookup"><span data-stu-id="54515-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="54515-104">Una pianificazione del progetto comunica il lavoro da eseguire, le risorse che realizzeranno il lavoro e il calendario in cui il lavoro dovrà essere ultimato.</span><span class="sxs-lookup"><span data-stu-id="54515-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="54515-105">La pianificazione del progetto riflette il lavoro associato alla consegna puntuale del progetto.</span><span class="sxs-lookup"><span data-stu-id="54515-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="54515-106">Uno dei primi passaggi nella fase di inizializzazione del progetto è di realizzare una pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="54515-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="54515-107">Per stabilire una pianificazione del progetto, è necessario creare una struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="54515-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="54515-108">Crea una struttura del progetto con una struttura di suddivisione del lavoro che consente di:</span><span class="sxs-lookup"><span data-stu-id="54515-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="54515-109">Suddividere il lavoro in attività gestibili</span><span class="sxs-lookup"><span data-stu-id="54515-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="54515-110">Stimare il tempo necessario per completare un'attività</span><span class="sxs-lookup"><span data-stu-id="54515-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="54515-111">Impostare le relazioni tra attività e la durata dell'attività</span><span class="sxs-lookup"><span data-stu-id="54515-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="54515-112">Determinare i ruoli richiesti per completare ogni attività</span><span class="sxs-lookup"><span data-stu-id="54515-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="54515-113">La pianificazione del progetto nella struttura di suddivisione del lavoro ha un aspetto comune, completo di un diagramma di Gantt interattivo.</span><span class="sxs-lookup"><span data-stu-id="54515-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="54515-114">Crea una struttura di suddivisione del lavoro per un progetto</span><span class="sxs-lookup"><span data-stu-id="54515-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="54515-115">Crea una struttura di suddivisione del lavoro per rappresentare la sequenza di attività in un progetto.</span><span class="sxs-lookup"><span data-stu-id="54515-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="54515-116">La struttura di suddivisione del lavoro include le attività, i requisiti per ogni attività e le informazioni sui ricavi e i costi.</span><span class="sxs-lookup"><span data-stu-id="54515-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="54515-117">Nella struttura di suddivisione del lavoro, puoi aggiungere:</span><span class="sxs-lookup"><span data-stu-id="54515-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="54515-118">La sequenza di attività in una gerarchia</span><span class="sxs-lookup"><span data-stu-id="54515-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="54515-119">Eventuali altre attività che devono essere completate prima che possa essere avviata un'attività</span><span class="sxs-lookup"><span data-stu-id="54515-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="54515-120">La data di inizio, la data di fine e la durata di un'attività</span><span class="sxs-lookup"><span data-stu-id="54515-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="54515-121">Il numero di ore necessarie per un'attività</span><span class="sxs-lookup"><span data-stu-id="54515-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="54515-122">Qualsiasi competenza e formazione del lavoro richiesta</span><span class="sxs-lookup"><span data-stu-id="54515-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="54515-123">I lavoratori a cui è assegnata un'attività</span><span class="sxs-lookup"><span data-stu-id="54515-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="54515-124">Costi e ricavi stimati</span><span class="sxs-lookup"><span data-stu-id="54515-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="54515-125">Tipi di attività</span><span class="sxs-lookup"><span data-stu-id="54515-125">Task types</span></span>  
<span data-ttu-id="54515-126">Utilizzerai i seguenti tipi di attività quando si crea la struttura di suddivisione del lavoro:</span><span class="sxs-lookup"><span data-stu-id="54515-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="54515-127">**Nodo radice di progetto**</span><span class="sxs-lookup"><span data-stu-id="54515-127">**Project root node**</span></span> | <span data-ttu-id="54515-128">L'attività di riepilogo di livello superiore per il progetto.</span><span class="sxs-lookup"><span data-stu-id="54515-128">The top-level summary task for the project.</span></span> <span data-ttu-id="54515-129">Tutte le altra attività di progetto vengono create al di sotto.</span><span class="sxs-lookup"><span data-stu-id="54515-129">All other project tasks are created under it.</span></span> <span data-ttu-id="54515-130">Il nome dell'attività principale è il nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="54515-130">The name of the root task is the project name.</span></span> <span data-ttu-id="54515-131">Il lavoro, le date e la durata del nodo radice sono basati sui valori nella gerarchia sottostante.</span><span class="sxs-lookup"><span data-stu-id="54515-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="54515-132">Non puoi modificare le proprietà del nodo radice o eliminare il nodo radice.</span><span class="sxs-lookup"><span data-stu-id="54515-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="54515-133">**Attività di riepilogo o del contenitore**</span><span class="sxs-lookup"><span data-stu-id="54515-133">**Summary or container tasks**</span></span> | <span data-ttu-id="54515-134">Un'attività di riepilogo ha un'attività secondaria sottostante.</span><span class="sxs-lookup"><span data-stu-id="54515-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="54515-135">Un'attività di riepilogo non ha alcun lavoro o costo proprio.</span><span class="sxs-lookup"><span data-stu-id="54515-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="54515-136">Il suo lavoro e il suo costo sono un rollup delle attività secondarie.</span><span class="sxs-lookup"><span data-stu-id="54515-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="54515-137">Puoi modificare il nome di un'attività di riepilogo, ma non puoi modificare il lavoro, le date o la durata, perché vengono calcolate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="54515-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="54515-138">L'eliminazione di un'attività di riepilogo elimina l'attività stessa e le attività secondarie.</span><span class="sxs-lookup"><span data-stu-id="54515-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="54515-139">**Attività del nodo foglia**</span><span class="sxs-lookup"><span data-stu-id="54515-139">**Leaf node tasks**</span></span> | <span data-ttu-id="54515-140">Un'attività del nodo foglia rappresenta il lavoro più dettagliato del progetto.</span><span class="sxs-lookup"><span data-stu-id="54515-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="54515-141">Ha un lavoro stimato, un numero pianificato di risorse, date di inizio e fine pianificate e una durata.</span><span class="sxs-lookup"><span data-stu-id="54515-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="54515-142">Gerarchia attività</span><span class="sxs-lookup"><span data-stu-id="54515-142">Task hierarchy</span></span>  
 <span data-ttu-id="54515-143">Sono disponibili le opzioni seguenti quando si crea una gerarchia dell'attività:</span><span class="sxs-lookup"><span data-stu-id="54515-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="54515-144">**Aggiungi attività**.</span><span class="sxs-lookup"><span data-stu-id="54515-144">**Add task**.</span></span>   <span data-ttu-id="54515-145">Puoi aggiungere un'attività a una posizione scelta nella gerarchia dell'attività.</span><span class="sxs-lookup"><span data-stu-id="54515-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="54515-146">Se non selezioni una posizione, la nuova attività viene visualizzata alla fine.</span><span class="sxs-lookup"><span data-stu-id="54515-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="54515-147">**Rientro attività**.</span><span class="sxs-lookup"><span data-stu-id="54515-147">**Indent task**.</span></span>   <span data-ttu-id="54515-148">Rientra un'attività per fare in modo che sia figlia dell'attività direttamente al di sopra.</span><span class="sxs-lookup"><span data-stu-id="54515-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="54515-149">**Rientro negativo attività**.</span><span class="sxs-lookup"><span data-stu-id="54515-149">**Outdent task**.</span></span>   <span data-ttu-id="54515-150">Imposti un rientro negativo di un'attività in modo che non sia più un'attività secondaria dell'attività padre originale.</span><span class="sxs-lookup"><span data-stu-id="54515-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="54515-151">**Sposta su e sposta giù**.</span><span class="sxs-lookup"><span data-stu-id="54515-151">**Move up and Move down**.</span></span>   <span data-ttu-id="54515-152">Sposta le attività in alto e in basso nella gerarchia dell'attività padre.</span><span class="sxs-lookup"><span data-stu-id="54515-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="54515-153">Se si sposta un'attività in alto o in basso non ci sono conseguenze sul lavoro, il costo, le date o la durata.</span><span class="sxs-lookup"><span data-stu-id="54515-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="54515-154">Attributi attività</span><span class="sxs-lookup"><span data-stu-id="54515-154">Task attributes</span></span>  
 <span data-ttu-id="54515-155">Un nome dell'attività descrive il lavoro che deve essere completato.</span><span class="sxs-lookup"><span data-stu-id="54515-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="54515-156">Utilizza vari attributi dell'attività per descrivere i requisiti di pianificazione e assegnazione del personale per l'attività.</span><span class="sxs-lookup"><span data-stu-id="54515-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="54515-157">Attributi di pianificazione</span><span class="sxs-lookup"><span data-stu-id="54515-157">Schedule attributes</span></span>

 - <span data-ttu-id="54515-158">Assegna i valori a **Ore di lavoro** , **Numero di risorse** , **Data di inizio** , **Data di fine** e **Durata** per determinare la pianificazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="54515-158">Assign values to **Effort hours** , **Number of resources** , **Start date** , **End date** , and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="54515-159">**Lavoro** è una stima delle ore necessarie per completare l'attività.</span><span class="sxs-lookup"><span data-stu-id="54515-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="54515-160">**Numero di risorse** è una stima che il responsabile di progetto inserisce nell'attività per ottenere la migliore pianificazione possibile.</span><span class="sxs-lookup"><span data-stu-id="54515-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="54515-161">**Durata** (in giorni) indica il numero di giorni lavorativi che ci vorranno per completare l'attività.</span><span class="sxs-lookup"><span data-stu-id="54515-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="54515-162">Attributi di assegnazione del personale</span><span class="sxs-lookup"><span data-stu-id="54515-162">Staffing attributes</span></span>

 - <span data-ttu-id="54515-163">**Ruolo** , **Unità organizzativa risorsa** , **Numero di risorse** e **Risorse** descrivono i requisiti di assegnazione del personale per l'attività.</span><span class="sxs-lookup"><span data-stu-id="54515-163">**Role** , **Resource organizational unit** , **Number of resources** , and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="54515-164">**Ruolo** descrive il tipo di risorsa necessario per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="54515-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="54515-165">**Unità organizzativa risorsa** indica l'unità organizzativa da cui le risorse devono avere assegnato del personale per questa attività, influisce inoltre sulla stima di costo e vendite dell'attività, poiché viene contabilizzata quando si determina il prezzo di vendita dell'unità per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="54515-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="54515-166">**Risorse** include una risorsa generica o una risorsa denominata quando ne viene trovata una.</span><span class="sxs-lookup"><span data-stu-id="54515-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="54515-167">Dipendenze attività</span><span class="sxs-lookup"><span data-stu-id="54515-167">Task dependencies</span></span>  
 <span data-ttu-id="54515-168">Puoi creare relazioni di predecessore tra una o più attività nella struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="54515-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="54515-169">Puoi impostare uno o più valori per il campo di predecessore nelle attività per indicare le attività da cui sarà dipendente.</span><span class="sxs-lookup"><span data-stu-id="54515-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="54515-170">Quando assegni un valore di predecessore a un'attività, l'attività può iniziare solo quando tutte le attività predecessore sono state completate.</span><span class="sxs-lookup"><span data-stu-id="54515-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="54515-171">Impostando questa dipendenza in un'attività darà come risultato il ricalcolo della data di inizio pianificata dell'attività come l'ultima fine di tutti i predecessori.</span><span class="sxs-lookup"><span data-stu-id="54515-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="54515-172">Le conseguenze correlate ai predecessori in una pianificazione non sono limitate dalla modalità dell'attività definita nell'attività.</span><span class="sxs-lookup"><span data-stu-id="54515-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="54515-173">Modalità attività</span><span class="sxs-lookup"><span data-stu-id="54515-173">Task mode</span></span>  
 <span data-ttu-id="54515-174">La modalità attività è uno dei fattori importanti che determinano la pianificazione attività del nodo foglia.</span><span class="sxs-lookup"><span data-stu-id="54515-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="54515-175">Esistono due diverse modalità di attività per ogni attività: la modalità di pianificazione automatica e la modalità di pianificazione manuale.</span><span class="sxs-lookup"><span data-stu-id="54515-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="54515-176">**Pianificazione automatica**.</span><span class="sxs-lookup"><span data-stu-id="54515-176">**Auto scheduling**.</span></span>   <span data-ttu-id="54515-177">Quando imposti la modalità di attività su Pianificata automaticamente, il motore di pianificazione dell'attività utilizza le regole di pianificazione nei seguenti attributi di attività per determinare la pianificazione per l'attività:</span><span class="sxs-lookup"><span data-stu-id="54515-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="54515-178">Attività precedenti</span><span class="sxs-lookup"><span data-stu-id="54515-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="54515-179">Risorse</span><span class="sxs-lookup"><span data-stu-id="54515-179">Effort</span></span>  
  
    -   <span data-ttu-id="54515-180">Numero di risorse</span><span class="sxs-lookup"><span data-stu-id="54515-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="54515-181">Date di inizio e fine</span><span class="sxs-lookup"><span data-stu-id="54515-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="54515-182">**Regole di pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="54515-182">**Scheduling rules**.</span></span>   <span data-ttu-id="54515-183">La data di inizio di un'attività del nodo foglia privo di impostazioni predefinite dei predecessori alla data di inizio della pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="54515-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="54515-184">La durata di un'attività del nodo foglia viene sempre calcolata come il numero dei giorni lavorativi tra le date di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="54515-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="54515-185">Quando un'attività viene pianificata automaticamente, il motore di pianificazione segue le regole riportate di seguito:</span><span class="sxs-lookup"><span data-stu-id="54515-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="54515-186">Le date di inizio e fine di un'attività devono sempre essere giorni lavorativi in base al calendario della pianificazione del progetto</span><span class="sxs-lookup"><span data-stu-id="54515-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="54515-187">La data di inizio di un'attività con impostazioni predefinite dei predecessori sull'ultima data di fine dei predecessori</span><span class="sxs-lookup"><span data-stu-id="54515-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="54515-188">Lavoro = Numero delle persone \* Durata \* Ore in un giorno lavorativo standard del calendario di progetto</span><span class="sxs-lookup"><span data-stu-id="54515-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="54515-189">**Responsabile pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="54515-189">**Manual scheduling**.</span></span>   <span data-ttu-id="54515-190">In alcuni casi, può essere utile deviare dalle regole.</span><span class="sxs-lookup"><span data-stu-id="54515-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="54515-191">In questi casi, puoi impostare la modalità di attività per l'attività da pianificare manualmente.</span><span class="sxs-lookup"><span data-stu-id="54515-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="54515-192">Ciò interrompe il calcolo dei valori da parte del motore di pianificazione per gli attributi di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="54515-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="54515-193">L'impostazione dei predecessori nelle attività influenza sempre la data di inizio dell'attività dipendente.</span><span class="sxs-lookup"><span data-stu-id="54515-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="54515-194">Crea una struttura di suddivisione del lavoro</span><span class="sxs-lookup"><span data-stu-id="54515-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="54515-195">Passa a **Project Service > Progetti**.</span><span class="sxs-lookup"><span data-stu-id="54515-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="54515-196">Fai clic sul progetto che desideri utilizzare.</span><span class="sxs-lookup"><span data-stu-id="54515-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="54515-197">Nella barra sulla parte superiore dello schermo, seleziona la freccia in giù accanto al nome del progetto e quindi fai clic sulla Struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="54515-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="54515-198">Per aggiungere un'attività, fai clic su **Aggiungi attività**.</span><span class="sxs-lookup"><span data-stu-id="54515-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="54515-199">Compila i campi per l'attività, quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="54515-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="54515-200">Continua ad aggiungere attività fino a che la struttura di suddivisione del lavoro non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="54515-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="54515-201">Durante la creazione della struttura di suddivisione del lavoro, puoi eseguire le operazioni seguenti per organizzare le seguenti:</span><span class="sxs-lookup"><span data-stu-id="54515-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="54515-202">Seleziona un'attività e fai clic su **Rientro** per spostarla in un'altra attività oppure fai clic su Rientro negativo per spostarlo di un livello.</span><span class="sxs-lookup"><span data-stu-id="54515-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="54515-203">Seleziona un'attività e fai clic su **Sposta su** o **Sposta giù** per spostarla in alto o in basso nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="54515-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="54515-204">Fai clic su **Nascondi Gantt** per nascondere il diagramma di Gantt e fai clic su **Mostra Gantt** per visualizzarlo di nuovo.</span><span class="sxs-lookup"><span data-stu-id="54515-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="54515-205">Seleziona un periodo di tempo diverso per il diagramma di Gantt in **Scala temporale**.</span><span class="sxs-lookup"><span data-stu-id="54515-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="54515-206">Per aggiungere i ruoli specificati nella struttura di suddivisione del lavoro ai membri del team del progetto, fai clic su **Genera team di progetto**.</span><span class="sxs-lookup"><span data-stu-id="54515-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="54515-207">Una volta terminato di apportare modifiche, fai clic su **Salva** nell'angolo in basso a destra dello schermo.</span><span class="sxs-lookup"><span data-stu-id="54515-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="54515-208">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54515-208">See Also</span></span>  
 [<span data-ttu-id="54515-209">Guida del responsabile di progetto</span><span class="sxs-lookup"><span data-stu-id="54515-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
