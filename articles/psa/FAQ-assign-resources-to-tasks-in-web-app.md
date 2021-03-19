---
title: Come si assegna una risorsa prenotabile a un'attività nell'app Web
description: Una panoramica dei modi in cui è possibile assegnare risorse prenotabili.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286298"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="c84b7-103">Come si assegna una risorsa prenotabile a un'attività nell'app Web (app Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="c84b7-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c84b7-104">Vi sono due modi per assegnare una risorsa a un'attività in Project Service.</span><span class="sxs-lookup"><span data-stu-id="c84b7-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="c84b7-105">È possibile prenotare una risorsa come membro del team e quindi assegnarla a un'attività.</span><span class="sxs-lookup"><span data-stu-id="c84b7-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="c84b7-106">Oppure, è possibile creare un membro del team generico mediante l'assegnazione di ruoli nelle attività, generare un team e quindi soddisfare i requisiti di supporto con una risorsa con nome.</span><span class="sxs-lookup"><span data-stu-id="c84b7-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="c84b7-107">Si noti che se si desidera assegnare una risorsa prenotabile a un'attività, il membro del team della risorsa prenotabile deve avere prenotazioni disponibili sufficienti.</span><span class="sxs-lookup"><span data-stu-id="c84b7-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="c84b7-108">Il tipo di esecuzione della prenotazione deve essere Prenota definitivamente e lo stato Impegnato.</span><span class="sxs-lookup"><span data-stu-id="c84b7-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="c84b7-109">Se non vi sono prenotazioni sufficienti per la risorsa, Project Service rimuove l'assegnazione e visualizza il messaggio di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="c84b7-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="c84b7-110">*Impossibile assegnare la risorsa all'attività - le risorse seguenti non hanno ore prenotate sufficienti per il progetto*</span><span class="sxs-lookup"><span data-stu-id="c84b7-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="c84b7-111">Prenotare una risorsa come membro del team e quindi assegnarla a un'attività</span><span class="sxs-lookup"><span data-stu-id="c84b7-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="c84b7-112">Con questo metodo si aggiunge una risorsa al team di progetto e quindi si assegnano le attività alla risorsa nella pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="c84b7-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="c84b7-113">Di seguito viene descritto come procedere:</span><span class="sxs-lookup"><span data-stu-id="c84b7-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="c84b7-114">Nella griglia dei membri del team, aggiungere un nuovo membro del team selezionando **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="c84b7-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="c84b7-115">Nella schermata per la creazione rapida di membri del team, selezionare il nome della risorsa prenotabile e impostare un ruolo.</span><span class="sxs-lookup"><span data-stu-id="c84b7-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="c84b7-116">Selezionare le date **Da** e **A**.</span><span class="sxs-lookup"><span data-stu-id="c84b7-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="c84b7-117">![Screenshot dell'aggiunta di un membro del team](media/FAQ-Resources-to-Tasks2-1.png "Screenshot dell'aggiunta di un membro del team")</span><span class="sxs-lookup"><span data-stu-id="c84b7-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="c84b7-118">Selezionare uno dei seguenti metodi di allocazione per la prenotazione della risorsa:</span><span class="sxs-lookup"><span data-stu-id="c84b7-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="c84b7-119">**Piena capacità** prenota l'intera capacità della risorsa per le date di inizio e fine specificate.</span><span class="sxs-lookup"><span data-stu-id="c84b7-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="c84b7-120">**Percentuale capacità** prenota la risorsa per una percentuale della capacità della risorsa per le date di inizio e di fine specificate.</span><span class="sxs-lookup"><span data-stu-id="c84b7-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="c84b7-121">**Per ore - Distribuzione uniforme** prenota la risorsa per un determinato numero di ore, con una distribuzione giornaliera uniforme durante il periodo tra la data di inizio e quella di fine specificate.</span><span class="sxs-lookup"><span data-stu-id="c84b7-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="c84b7-122">**Per ore - Spese iniziali** prenota la risorsa per un determinato numero di ore, applicando spese iniziali alle ore giornaliere durante il periodo tra la data di inizio e quella di fine specificate.</span><span class="sxs-lookup"><span data-stu-id="c84b7-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="c84b7-123">Non selezionare **Nessuno** in quanto aggiunge la risorsa al team ma non crea prenotazioni che assorbano la capacità della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c84b7-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="c84b7-124">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="c84b7-124">Select **Save**.</span></span>

    <span data-ttu-id="c84b7-125">Si noti che le ore della prenotazione devono essere sufficienti per coprire le ore di lavoro e gli intervalli di date delle attività a cui si assegna la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c84b7-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="c84b7-126">Se non sono allineate, non è possibile assegnare la risorsa all'attività.</span><span class="sxs-lookup"><span data-stu-id="c84b7-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="c84b7-127">Nella struttura di suddivisione del lavoro per l'attività, fare clic sull'elenco a discesa della cella della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c84b7-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="c84b7-128">Eseguire quindi le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c84b7-128">Then:</span></span> 

    1. <span data-ttu-id="c84b7-129">Seleziona **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="c84b7-129">Select **Add**.</span></span>
    2. <span data-ttu-id="c84b7-130">Selezionare l'elenco a discesa in **Risorse** e selezionare il membro del team aggiunto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c84b7-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="c84b7-131">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="c84b7-131">Select **OK**.</span></span> <span data-ttu-id="c84b7-132">Il membro del team è ora assegnato all'attività.</span><span class="sxs-lookup"><span data-stu-id="c84b7-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="c84b7-133">![Screenshot dell'aggiunta di risorse con la struttura di suddivisione del lavoro](media/FAQ-Resources-to-Tasks2-2.png "Screenshot dell'aggiunta di risorse con la struttura di suddivisione del lavoro")</span><span class="sxs-lookup"><span data-stu-id="c84b7-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="c84b7-134">Nella griglia dei membri del team, viene visualizzata l'aggregazione delle ore assegnate alla risorsa in Ore assegnate.</span><span class="sxs-lookup"><span data-stu-id="c84b7-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="c84b7-135">È inferiore o uguale alle ore prenotate per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c84b7-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="c84b7-136">![Screenshot delle ore assegnate per una risorsa](media/FAQ-Resources-to-Tasks2-3.png "Screenshot delle ore assegnate per una risorsa")</span><span class="sxs-lookup"><span data-stu-id="c84b7-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="c84b7-137">Se l'attività che si tenta di assegnare alla risorsa inizia dopo la data di fine delle prenotazioni delle risorse, la risorsa non sarà visualizzata nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="c84b7-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="c84b7-138">Da notare che è possibile assegnare una risorsa a un numero di ore maggiore delle relative ore prenotate se la risorsa ha della capacità non assegnata.</span><span class="sxs-lookup"><span data-stu-id="c84b7-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="c84b7-139">In questo caso, la risorsa sarà assegnata solo parzialmente in base alle relative prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="c84b7-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="c84b7-140">È possibile visualizzare queste ore di attività non assegnate aggiungendo la colonna Ore senza personale alla struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="c84b7-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="c84b7-141">Se le risorse sono assegnate alle relative ore prenotate (uguali alle relative ore assegnate), verrà visualizzato il messaggio di errore seguente quando si tenta di assegnare ulteriori attività:</span><span class="sxs-lookup"><span data-stu-id="c84b7-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="c84b7-142">*Impossibile assegnare la risorsa all'attività - le risorse seguenti non hanno ore prenotate sufficienti per il progetto.*</span><span class="sxs-lookup"><span data-stu-id="c84b7-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="c84b7-143">Inoltre, il membro del team responsabile di progetto predefinito che viene aggiunto al team quando si crea il progetto viene aggiunto senza prenotazioni e non può essere assegnato ad alcuna attività.</span><span class="sxs-lookup"><span data-stu-id="c84b7-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="c84b7-144">Non sarà quindi visualizzato nell'elenco a discesa per le attività.</span><span class="sxs-lookup"><span data-stu-id="c84b7-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="c84b7-145">Per assegnare questa risorsa, è necessario rimuoverla dal team e aggiungerla nuovamente con un metodo di allocazione diverso da Nessuno.</span><span class="sxs-lookup"><span data-stu-id="c84b7-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="c84b7-146">Il motivo per cui viene aggiunta al team alla creazione del progetto è che in questo modo un progetto ha almeno un responsabile approvazione di progetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="c84b7-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="c84b7-147">Creare un membro del team generico mediante l'assegnazione di ruoli nelle attività</span><span class="sxs-lookup"><span data-stu-id="c84b7-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="c84b7-148">Questo metodo assicura che le risorse hanno prenotazioni sufficienti per le attività.</span><span class="sxs-lookup"><span data-stu-id="c84b7-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="c84b7-149">Innanzitutto, si crea una risorsa segnaposto o generica che descrive le caratteristiche della risorsa con nome che si desidera utilizzare per le attività generando un team dopo aver assegnato ruoli alle attività.</span><span class="sxs-lookup"><span data-stu-id="c84b7-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="c84b7-150">Di seguito viene descritto come procedere:</span><span class="sxs-lookup"><span data-stu-id="c84b7-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="c84b7-151">Nella struttura di suddivisione del lavoro, selezionare un'attività.</span><span class="sxs-lookup"><span data-stu-id="c84b7-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="c84b7-152">Selezionare l'icona a discesa **Ruolo assegnato** nella cella della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c84b7-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="c84b7-153">Selezionare l'elenco a discesa **Ruolo** e selezionare il ruolo per la risorsa generica.</span><span class="sxs-lookup"><span data-stu-id="c84b7-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="c84b7-154">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="c84b7-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="c84b7-155">![Screenshot dell'uso della struttura di suddivisione del lavoro per aggiungere una risorsa](media/FAQ-Resources-to-Tasks2-4.png "Screenshot dell'uso della struttura di suddivisione del lavoro per aggiungere una risorsa")</span><span class="sxs-lookup"><span data-stu-id="c84b7-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="c84b7-156">Dopo aver completato l'assegnazione dei ruoli alle attività nella struttura di suddivisione del lavoro, selezionare **Genera team di progetto**.</span><span class="sxs-lookup"><span data-stu-id="c84b7-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="c84b7-157">Project Service crea il numero minimo di membri del team generici in base ai ruoli, alle unità gestione risorse dell'organizzazione e al calendario del progetto aggregando le assegnazioni delle attività.</span><span class="sxs-lookup"><span data-stu-id="c84b7-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="c84b7-158">![Screenshot della generazione del team di progetto](media/FAQ-Resources-to-Tasks2-5.png "Screenshot della generazione del team di progetto")</span><span class="sxs-lookup"><span data-stu-id="c84b7-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="c84b7-159">Nella griglia dei membri del team, saranno visualizzate le risorse di tipo Risorsa generica con il ruolo e il nome posizione.</span><span class="sxs-lookup"><span data-stu-id="c84b7-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="c84b7-160">Se due risorse sono necessarie affinché un ruolo completi il lavoro, la funzionalità Genera team crea due membri del team e utilizza il nome posizione per distinguerli.</span><span class="sxs-lookup"><span data-stu-id="c84b7-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="c84b7-161">![Screenshot dell'aggiunta di due risorse generiche](media/FAQ-Resources-to-Tasks2-6.png "Screenshot dell'aggiunta di due risorse generiche")</span><span class="sxs-lookup"><span data-stu-id="c84b7-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="c84b7-162">È possibile aprire il requisito di risorsa di supporto per il membro del team generico selezionando il collegamento sotto Requisito di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c84b7-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="c84b7-163">![Screenshot dell'apertura del requisito di risorsa di supporto](media/FAQ-Resources-to-Tasks2-7.png "Screenshot dell'apertura del requisito di risorsa di supporto")</span><span class="sxs-lookup"><span data-stu-id="c84b7-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="c84b7-164">Selezionare **Prenota** per la risorsa generica e utilizzare la scheda di pianificazione per trovare e prenotare una risorsa reale.</span><span class="sxs-lookup"><span data-stu-id="c84b7-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="c84b7-165">È anche possibile inviare il requisito che deve essere soddisfatto da un responsabile delle risorse selezionando **Invia richiesta**.</span><span class="sxs-lookup"><span data-stu-id="c84b7-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="c84b7-166">Quando la risorsa generica viene soddisfatta con una risorsa denominata, la risorsa generica viene rimossa dal team e le assegnazioni delle attività per la risorsa generica sono assegnate alla risorsa denominata che ha soddisfatto il requisito di risorsa della risorsa generica.</span><span class="sxs-lookup"><span data-stu-id="c84b7-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]