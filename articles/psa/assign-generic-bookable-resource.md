---
title: Assegnare risorse prenotabili generiche a un'attività e a un team di progetto
description: In questo argomento vengono fornite informazioni sulla prenotazione di risorse generiche per attività e team di progetto.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127073"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="889ca-103">Assegnare risorse prenotabili generiche a un'attività e generare requisiti di risorsa</span><span class="sxs-lookup"><span data-stu-id="889ca-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="889ca-104">Oltre a prenotare e assegnare risorse denominate o reali al tuo progetto, puoi assegnare risorse generiche ad attività di progetto.</span><span class="sxs-lookup"><span data-stu-id="889ca-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="889ca-105">Queste risorse possono essere utilizzate come segnaposto per le risorse denominate fino a che non si è pronti ad assegnare risorse denominate al progetto.</span><span class="sxs-lookup"><span data-stu-id="889ca-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="889ca-106">In Project Service Automation (PSA), apri la pagina **Progetto** e nella scheda **Pianifica**, immetti il nome posizione della risorsa generica nella cella **Risorsa** della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="889ca-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="889ca-107">In alternativa, fai clic sull'icona **Risorsa** nella cella per aprire il selettore di risorse e quindi immetti il nome della risorsa generica che intendi creare.</span><span class="sxs-lookup"><span data-stu-id="889ca-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Creare e assegnare un membro del team generico](media/RM-how-to-9.png)

<span data-ttu-id="889ca-109">Viene aperto il pannello **Creazione rapida: Membro del team di progetto**.</span><span class="sxs-lookup"><span data-stu-id="889ca-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="889ca-110">Immetti il ruolo e l'unità organizzativa del membro del team di risorse generiche e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="889ca-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Creazione rapida di un membro del team generico](media/RM-how-to-10.png)

3. <span data-ttu-id="889ca-112">Dopo aver creato il nuovo membro del team di risorse generiche, questo viene assegnato all'attività.</span><span class="sxs-lookup"><span data-stu-id="889ca-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="889ca-113">Puoi continuare ad assegnare quella risorsa generica ad altre attività nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="889ca-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Assegnare un membro del team generico esistente ad attività](media/RM-how-to-11.png)

4. <span data-ttu-id="889ca-115">Dopo aver assegnato la risorsa generica, puoi generare un requisito di risorsa e soddisfarlo prenotando direttamente o inviando una richiesta di risorsa a un responsabile delle risorse.</span><span class="sxs-lookup"><span data-stu-id="889ca-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generare un requisito per un membro del team generico](media/RM-how-to-12.png)

<span data-ttu-id="889ca-117">Nella griglia dei membri del team, oltre a poter utilizzare il selettore di risorse come indicato in precedenza, puoi aggiungere risorse generiche direttamente.</span><span class="sxs-lookup"><span data-stu-id="889ca-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="889ca-118">Le risorse sono aggiunte con un requisito di risorsa basato sulle date di inizio/fine e sul metodo di allocazione specificati nel pannello **Creazione rapida: Membro del team di progetto**.</span><span class="sxs-lookup"><span data-stu-id="889ca-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="889ca-119">Puoi osservare una differenza se aggiungi il membro del team generico direttamente e quindi assegni più attività alla risorsa generica delle ore richieste che deve coprire.</span><span class="sxs-lookup"><span data-stu-id="889ca-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="889ca-120">Fai clic su **Genera requisito** per rigenerare il requisito ed equilibrare le ore richieste rispetto alle assegnazioni.</span><span class="sxs-lookup"><span data-stu-id="889ca-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="889ca-121">Puoi anche fare clic sul collegamento **Requisito di risorsa** nella griglia del team per aprire il requisito e aggiungere competenze, risorse preferite e così via.</span><span class="sxs-lookup"><span data-stu-id="889ca-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Requisito di risorsa](media/RM-how-to-13.png)

