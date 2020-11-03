---
title: Stima di vendite e costi del progetto quando una risorsa prenotabile ricopre più ruoli in un progetto
description: Questo argomento fornisce informazioni su come utilizzare le dimensioni di determinazione dei prezzi per supportare prezzi e costi per una risorsa che ricopre più ruoli in un progetto.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078928"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="109d0-103">Stima di vendite e costi del progetto quando una risorsa prenotabile ricopre più ruoli in un progetto</span><span class="sxs-lookup"><span data-stu-id="109d0-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="109d0-104">Le società basate su progetti hanno spesso la necessità di una risorsa per svolgere più ruoli in un progetto.</span><span class="sxs-lookup"><span data-stu-id="109d0-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="109d0-105">Ognuno di questi ruoli potrebbe avere un prezzo e un costo diverso, il che significa che il tempo della stessa risorsa sul progetto potrebbe ottenere una stima finanziaria diversa a seconda del costo e delle tariffe per ciascuno dei ruoli.</span><span class="sxs-lookup"><span data-stu-id="109d0-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="109d0-106">Project Service Automation consente l'impostazione dei valori nel record del membro del team per la risorsa denominata e consente sostituzioni diverse su ciascuna delle attività a cui è assegnato il membro del team.</span><span class="sxs-lookup"><span data-stu-id="109d0-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="109d0-107">L'esempio seguente spiega come la semplice sostituzione di questo valore consenta a una risorsa di avere più ruoli in un progetto con costi e tariffe di fatturazione differenti.</span><span class="sxs-lookup"><span data-stu-id="109d0-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="109d0-108">Creare attività</span><span class="sxs-lookup"><span data-stu-id="109d0-108">Create tasks</span></span>
<span data-ttu-id="109d0-109">Crea due attività di progetto per 40 ore ciascuna, Attività A e Attività B. Seleziona Attività A come predecessore dell'Attività B.</span><span class="sxs-lookup"><span data-stu-id="109d0-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="109d0-110">Impostazione di ruolo e unità organizzativa per un membro del team di progetto generico</span><span class="sxs-lookup"><span data-stu-id="109d0-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="109d0-111">Nella pagina **Pianifica** seleziona la riga **Attività** per l'attività A.</span><span class="sxs-lookup"><span data-stu-id="109d0-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="109d0-112">Nel campo **Risorse** seleziona **Crea** nel menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="109d0-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="109d0-113">Nella pagina **Creazione rapida dei membri del team** specifica gli attributi del membro del team generico che può eseguire questa attività.</span><span class="sxs-lookup"><span data-stu-id="109d0-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="109d0-114">Seleziona il ruolo e l'unità organizzativa appropriati, quindi seleziona **Salva e chiudi**.</span><span class="sxs-lookup"><span data-stu-id="109d0-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="109d0-115">Un membro del team generico viene creato e assegnato a questa attività.</span><span class="sxs-lookup"><span data-stu-id="109d0-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="109d0-116">Ripeti questi passaggi per l'attività B e assicurati che il ruolo e l'unità organizzativa del membro del team generico creato per l'attività B sia diverso dall'attività A.</span><span class="sxs-lookup"><span data-stu-id="109d0-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="109d0-117">Impostazione di ruolo e unità organizzativa per un'attività di progetto</span><span class="sxs-lookup"><span data-stu-id="109d0-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="109d0-118">Dopo aver creato l'attività A, seleziona l'attività e quindi seleziona **Modifica attività**.</span><span class="sxs-lookup"><span data-stu-id="109d0-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="109d0-119">Nella pagina **Dettagli attività** trova i campi **Ruolo** e **Unità organizzativa** , aggiungi i valori di una risorsa che eseguirà questa attività.</span><span class="sxs-lookup"><span data-stu-id="109d0-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="109d0-120">Se stai completando questi scenari utilizzando i dati demo di Project Service Automation, seleziona **Consulting Lead** per il ruolo e **Fabrikam US** come unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="109d0-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="109d0-121">Seleziona l'attività B, quindi seleziona **Modifica attività**.</span><span class="sxs-lookup"><span data-stu-id="109d0-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="109d0-122">Nella pagina **Dettagli attività** trova i campi **Ruolo** e **Unità organizzativa** , aggiungi i valori di una risorsa che eseguirà questa attività.</span><span class="sxs-lookup"><span data-stu-id="109d0-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="109d0-123">Assicurati che i valori nei campi **Ruolo** e **Unità organizzativa** siano diversi per l'attività B da quelli per l'attività A.</span><span class="sxs-lookup"><span data-stu-id="109d0-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="109d0-124">Se stai completando questi scenari utilizzando i dati demo di Project Service Automation, seleziona **Network Technician** per il ruolo e **Fabrikam US** come unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="109d0-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="109d0-125">Salva e chiudi la pagina **Dettagli attività**.</span><span class="sxs-lookup"><span data-stu-id="109d0-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="109d0-126">Membro del team e stima del comportamento</span><span class="sxs-lookup"><span data-stu-id="109d0-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="109d0-127">Nella pagina **Dettagli attività** seleziona in **Membro del team** i due membri del team generici e quindi seleziona **Genera requisiti**.</span><span class="sxs-lookup"><span data-stu-id="109d0-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="109d0-128">Vengono generati i requisiti della risorsa.</span><span class="sxs-lookup"><span data-stu-id="109d0-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="109d0-129">Seleziona la riga del membro del team per **Consulting Lead** e poi seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="109d0-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="109d0-130">Viene visualizzata la scheda di pianificazione e viene prenotata una risorsa per quel requisito.</span><span class="sxs-lookup"><span data-stu-id="109d0-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="109d0-131">Seleziona la riga del membro del team per **Network Technician** e poi seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="109d0-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="109d0-132">Viene visualizzata la scheda di pianificazione e viene prenotata la stessa risorsa per quel requisito.</span><span class="sxs-lookup"><span data-stu-id="109d0-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="109d0-133">Griglia del membro del team</span><span class="sxs-lookup"><span data-stu-id="109d0-133">Team Member grid</span></span> 
<span data-ttu-id="109d0-134">Nella griglia **Membro del team** nota che i due record dei membri del team generici sono stati eliminati e sostituiti da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="109d0-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="109d0-135">Esiste un set di valori per quella risorsa che mostra un set di valori predefinito per **Ruolo** e **Unità organizzativa**.</span><span class="sxs-lookup"><span data-stu-id="109d0-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="109d0-136">Quando espandi la riga del record del membro del team puoi visualizzare assegnazioni distinte del record del membro del team per entrambe le attività.</span><span class="sxs-lookup"><span data-stu-id="109d0-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="109d0-137">Ogni riga di assegnazione ha valori specifici dell'attività per **Ruolo** e **Unità organizzativa**.</span><span class="sxs-lookup"><span data-stu-id="109d0-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="109d0-138">Griglia delle stime</span><span class="sxs-lookup"><span data-stu-id="109d0-138">Estimates grid</span></span> 
<span data-ttu-id="109d0-139">Quando passi alla griglia **Stime** puoi notare che entrambe le assegnazioni per la stessa risorsa hanno un prezzo diverso.</span><span class="sxs-lookup"><span data-stu-id="109d0-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="109d0-140">Il prezzo dell'assegnazione per la risorsa nell'attività A viene calcolato utilizzando il valore dell'attributo **Ruolo** di **Consulting Lead**.</span><span class="sxs-lookup"><span data-stu-id="109d0-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="109d0-141">Il prezzo dell'assegnazione per la stessa risorsa nell'attività B viene calcolato utilizzando il valore dell'attributo **Ruolo** di **Network Technician**.</span><span class="sxs-lookup"><span data-stu-id="109d0-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





