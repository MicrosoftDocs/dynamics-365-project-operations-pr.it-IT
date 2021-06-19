---
title: Prenotare risorse prenotabili denominate per un team di progetto e assegnarvi attività
description: In questo argomento vengono fornite informazioni sulla modalità di prenotazione di risorse denominate per team di progetto e sull'assegnazione delle risorse ad attività.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009351"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="79d7f-103">Prenotare risorse prenotabili denominate per un team di progetto e assegnarvi attività</span><span class="sxs-lookup"><span data-stu-id="79d7f-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="79d7f-104">Puoi aggiungere una risorsa denominata a un team di progetto prenotandole direttamente nel team.</span><span class="sxs-lookup"><span data-stu-id="79d7f-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="79d7f-105">A tale scopo, eseguire la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="79d7f-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="79d7f-106">In Project Service Automation, seleziona **Progetti** e apri il progetto per cui esegui le prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="79d7f-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="79d7f-107">Nella pagina **Progetto**, nella scheda **Team**, fai clic su **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="79d7f-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Aggiungere un membro del team dalla scheda Team](media/RM-how-to-1.png)

3. <span data-ttu-id="79d7f-109">Nella finestra di dialogo **Creazione rapida: Membro del team di progetto**, seleziona la risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="79d7f-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="79d7f-110">Il campo **Ruolo** verrà popolato con il ruolo predefinito della risorsa, se a questa ne è stato assegnato uno.</span><span class="sxs-lookup"><span data-stu-id="79d7f-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="79d7f-111">Se necessario, puoi cambiare il ruolo.</span><span class="sxs-lookup"><span data-stu-id="79d7f-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="79d7f-112">Seleziona le date di inizio e di fine per la risorsa e quindi il metodo di allocazione della capacità della risorsa.</span><span class="sxs-lookup"><span data-stu-id="79d7f-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="79d7f-113">Se il membro del team deve essere un responsabile approvazione di progetto, seleziona **Sì** nel campo **Responsabile approvazione di progetto**.</span><span class="sxs-lookup"><span data-stu-id="79d7f-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="79d7f-114">Ciò significa che il membro del team può approvare voci di spesa e inserimenti ore inviati per il progetto.</span><span class="sxs-lookup"><span data-stu-id="79d7f-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="79d7f-115">Fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="79d7f-115">Click **Save**.</span></span>

![Aggiungere un membro del team nel modulo di creazione rapida](media/RM-how-to-2.png)


<span data-ttu-id="79d7f-117">Ora puoi assegnare la risorsa prenotata ad attività nel progetto.</span><span class="sxs-lookup"><span data-stu-id="79d7f-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="79d7f-118">Nella pagina **Progetto**, fai clic sulla scheda **Pianifica** per assegnare attività alla nuova risorsa.</span><span class="sxs-lookup"><span data-stu-id="79d7f-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="79d7f-119">Il selettore di risorse eseguito dal campo **Risorse** nella griglia delle attività indicherà i membri del team che è possibile selezionare.</span><span class="sxs-lookup"><span data-stu-id="79d7f-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Assegnare un membro del team ad un'attività nella scheda Pianifica](media/RM-how-to-3.png)

<span data-ttu-id="79d7f-121">Nella versione 3 di Project Service Automation (PSA), le prenotazioni delle risorse e le assegnazioni di attività non sono strettamente correlate.</span><span class="sxs-lookup"><span data-stu-id="79d7f-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="79d7f-122">Ciò significa che quando utilizzi il selettore di risorse nella pianificazione, puoi assegnare attività a membri del team per più ore di quelle che le relative prenotazioni coprono nel progetto.</span><span class="sxs-lookup"><span data-stu-id="79d7f-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="79d7f-123">Puoi vedere le differenze tra le prenotazioni dei membri del team e le assegnazioni nella scheda **Team** o nella scheda **Riconciliazione risorse**. Puoi inoltre riconciliare le differenze tra prenotazioni e assegnazioni delle risorse a un livello più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="79d7f-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Scheda Riconciliazione risorse](media/RM-how-to-4.png)

<span data-ttu-id="79d7f-125">Puoi anche utilizzare il selettore di risorse nella scheda **Pianifica** per cercare e selezionare le risorse prenotabili che non fanno ancora parte del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="79d7f-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="79d7f-126">Queste sono visualizzate nel selettore di risorse come **Altre risorse**.</span><span class="sxs-lookup"><span data-stu-id="79d7f-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Assegnare una risorsa non membro del team ad un'attività](media/RM-how-to-5.png)

<span data-ttu-id="79d7f-128">Quando si esegue tale operazione, la risorsa viene aggiunta al team di progetto e assegnata all'attività, ma non viene generata alcuna prenotazione.</span><span class="sxs-lookup"><span data-stu-id="79d7f-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Membro del team con assegnazioni e nessuna prenotazione](media/RM-how-to-6.png)

<span data-ttu-id="79d7f-130">Puoi utilizzare la funzionalità di prenotazione estesa della scheda **Riconciliazione** o la **Scheda di pianificazione** per prenotare la capacità della risorsa per il progetto.</span><span class="sxs-lookup"><span data-stu-id="79d7f-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Estendere le prenotazioni per un membro del team nella scheda Riconciliazione risorse](media/RM-how-to-7.png)

<span data-ttu-id="79d7f-132">Dopo la prenotazione di un membro del team nel progetto, puoi utilizzare Gestisci prenotazioni o la scheda di pianificazione direttamente per gestire le tue prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="79d7f-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]