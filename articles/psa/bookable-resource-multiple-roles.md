---
title: Stimare le vendite e i costi del progetto quando una risorsa prenotabile ricopre più ruoli per un progetto
description: Questo argomento fornisce informazioni su come utilizzare le dimensioni dei prezzi per supportare la determinazione di prezzi e costi per una risorsa che ricopre più ruoli in un progetto.
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
ms.openlocfilehash: 0f779cf7e247157d6cae2ae7c4c5644201cb7714
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290994"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="81782-103">Stimare le vendite e i costi del progetto quando una risorsa prenotabile ricopre più ruoli per un progetto</span><span class="sxs-lookup"><span data-stu-id="81782-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="81782-104">Le aziende basate su progetti hanno spesso la necessità di una risorsa che esegua più ruoli in un progetto.</span><span class="sxs-lookup"><span data-stu-id="81782-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="81782-105">Ognuno di questi ruoli potrebbe avere un prezzo e un costo diverso, il che significa che il tempo della stessa risorsa sul progetto potrebbe ottenere una stima finanziaria diversa a seconda del costo e delle tariffe per ciascuno dei ruoli.</span><span class="sxs-lookup"><span data-stu-id="81782-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="81782-106">Project Service Automation consente l'impostazione dei valori nel record del membro del team per la risorsa denominata e consente sostituzioni diverse su ciascuna delle attività a cui è assegnato il membro del team.</span><span class="sxs-lookup"><span data-stu-id="81782-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="81782-107">L'esempio seguente spiega come la semplice sostituzione di questo valore consenta a una risorsa di avere più ruoli in un progetto con costi e tariffe di fatturazione differenti.</span><span class="sxs-lookup"><span data-stu-id="81782-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="81782-108">Creare attività</span><span class="sxs-lookup"><span data-stu-id="81782-108">Create tasks</span></span>
<span data-ttu-id="81782-109">Crea due attività di progetto per 40 ore ciascuna, Attività A e Attività B. Seleziona Attività A come predecessore dell'Attività B.</span><span class="sxs-lookup"><span data-stu-id="81782-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="81782-110">Impostazione di ruolo e unità organizzativa per un membro del team di progetto generico</span><span class="sxs-lookup"><span data-stu-id="81782-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="81782-111">Nella pagina **Pianifica** seleziona la riga **Attività** per l'attività A.</span><span class="sxs-lookup"><span data-stu-id="81782-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="81782-112">Nel campo **Risorse** seleziona **Crea** nel menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="81782-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="81782-113">Nella pagina **Creazione rapida dei membri del team** specifica gli attributi del membro del team generico che può eseguire questa attività.</span><span class="sxs-lookup"><span data-stu-id="81782-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="81782-114">Seleziona il ruolo e l'unità organizzativa appropriati, quindi seleziona **Salva e chiudi**.</span><span class="sxs-lookup"><span data-stu-id="81782-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="81782-115">Un membro del team generico viene creato e assegnato a questa attività.</span><span class="sxs-lookup"><span data-stu-id="81782-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="81782-116">Ripeti questi passaggi per l'attività B e assicurati che il ruolo e l'unità organizzativa del membro del team generico creato per l'attività B sia diverso dall'attività A.</span><span class="sxs-lookup"><span data-stu-id="81782-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="81782-117">Impostazione di ruolo e unità organizzativa per un'attività di progetto</span><span class="sxs-lookup"><span data-stu-id="81782-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="81782-118">Dopo aver creato l'attività A, seleziona l'attività e quindi seleziona **Modifica attività**.</span><span class="sxs-lookup"><span data-stu-id="81782-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="81782-119">Nella pagina **Dettagli attività** trova i campi **Ruolo** e **Unità organizzativa**, aggiungi i valori di una risorsa che eseguirà questa attività.</span><span class="sxs-lookup"><span data-stu-id="81782-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="81782-120">Se stai completando questi scenari utilizzando i dati demo di Project Service Automation, seleziona **Consulting Lead** per il ruolo e **Fabrikam US** come unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="81782-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="81782-121">Seleziona l'attività B, quindi seleziona **Modifica attività**.</span><span class="sxs-lookup"><span data-stu-id="81782-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="81782-122">Nella pagina **Dettagli attività** trova i campi **Ruolo** e **Unità organizzativa**, aggiungi i valori di una risorsa che eseguirà questa attività.</span><span class="sxs-lookup"><span data-stu-id="81782-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="81782-123">Assicurati che i valori nei campi **Ruolo** e **Unità organizzativa** per l'attività B siano diversi dai valori per l'attività A.</span><span class="sxs-lookup"><span data-stu-id="81782-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="81782-124">Se stai completando questi scenari utilizzando i dati demo di Project Service Automation, seleziona **Network Technician** per il ruolo e **Fabrikam US** come unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="81782-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="81782-125">Salva e chiudi la pagina **Dettagli attività**.</span><span class="sxs-lookup"><span data-stu-id="81782-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="81782-126">Membro del team e stima del comportamento</span><span class="sxs-lookup"><span data-stu-id="81782-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="81782-127">Nella pagina **Dettagli attività** seleziona in **Membro del team** i due membri del team generici e quindi seleziona **Genera requisiti**.</span><span class="sxs-lookup"><span data-stu-id="81782-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="81782-128">Seleziona la riga del membro del team per **Consulting Lead** e poi seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="81782-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="81782-129">Viene visualizzata la scheda di pianificazione e viene prenotata una risorsa per quel requisito.</span><span class="sxs-lookup"><span data-stu-id="81782-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="81782-130">Seleziona la riga del membro del team per **Network Technician** e poi seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="81782-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="81782-131">Viene visualizzata la scheda di pianificazione e viene prenotata la stessa risorsa per quel requisito.</span><span class="sxs-lookup"><span data-stu-id="81782-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="81782-132">Griglia del membro del team</span><span class="sxs-lookup"><span data-stu-id="81782-132">Team Member grid</span></span> 
<span data-ttu-id="81782-133">Nella griglia **Membro del team** nota che i due record dei membri del team generici sono stati eliminati e sostituiti da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="81782-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="81782-134">Esiste un set di valori per quella risorsa che mostra un set di valori predefinito per **Ruolo** e **Unità organizzativa**.</span><span class="sxs-lookup"><span data-stu-id="81782-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="81782-135">Quando espandi la riga del record del membro del team puoi visualizzare assegnazioni distinte del record del membro del team per entrambe le attività.</span><span class="sxs-lookup"><span data-stu-id="81782-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="81782-136">Ogni riga di assegnazione ha valori specifici dell'attività per **Ruolo** e **Unità organizzativa**.</span><span class="sxs-lookup"><span data-stu-id="81782-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="81782-137">Griglia delle stime</span><span class="sxs-lookup"><span data-stu-id="81782-137">Estimates grid</span></span> 
<span data-ttu-id="81782-138">Quando passi alla griglia **Stime** puoi notare che entrambe le assegnazioni per la stessa risorsa hanno un prezzo diverso.</span><span class="sxs-lookup"><span data-stu-id="81782-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="81782-139">Il prezzo dell'assegnazione per la risorsa nell'attività A viene calcolato utilizzando il valore dell'attributo **Ruolo** di **Consulting Lead**.</span><span class="sxs-lookup"><span data-stu-id="81782-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="81782-140">Il prezzo dell'assegnazione per la stessa risorsa nell'attività B viene calcolato utilizzando il valore dell'attributo **Ruolo** di **Network Technician**.</span><span class="sxs-lookup"><span data-stu-id="81782-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]