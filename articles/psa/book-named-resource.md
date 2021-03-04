---
title: Prenotare risorse denominate da requisiti di risorsa
description: In questo argomento vengono fornite informazioni sulla prenotazione di risorse denominate per un requisito di risorsa generica.
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145098"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="c5f4c-103">Prenotare risorse denominate da requisiti di risorsa</span><span class="sxs-lookup"><span data-stu-id="c5f4c-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c5f4c-104">Puoi prenotare una risorsa denominata per sostituire una risorsa generica che ha un requisito di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="c5f4c-105">In Project Service Automation (PSA), nella pagina **Progetti**, fai clic sulla scheda **Team**.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="c5f4c-106">Seleziona la risorsa generica che ha un requisito di risorsa nell'elenco e fai clic su **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="c5f4c-107">Oppure apri il requisito di risorsa e fai clic su **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-107">Or, open the resource requirement and then click **Book**.</span></span>


![Prenotare un membro del team generico](media/RM-how-to-14.png)


3. <span data-ttu-id="c5f4c-109">Nella pagina **Assistente di pianificazione**, seleziona una risorsa denominata per prenotarla per il team di progetto e fai clic su **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Prenotare un membro del team generico utilizzando l'assistente di pianificazione](media/RM-how-to-15.png)

<span data-ttu-id="c5f4c-111">Al termine della prenotazione di una risorsa denominata, questa sostituisce la risorsa generica.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Membro del team denominato che sostituisce un membro del team generico](media/RM-how-to-16.png)

<span data-ttu-id="c5f4c-113">Anche le assegnazioni nella pianificazione vengono aggiornate con la risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Membro del team denominato assegnato ad attività di progetto](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="c5f4c-115">Soddisfare un requisito di risorsa generica con molteplici risorse denominate</span><span class="sxs-lookup"><span data-stu-id="c5f4c-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="c5f4c-116">Soddisfare un requisito di risorsa generica con molteplici risorse denominate è simile ad assegnare una singola risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="c5f4c-117">Ad esempio, supponiamo di avere un'attività di una durata di cinque giorni con 120 ore di lavoro richiesto.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="c5f4c-118">Questa attività non può essere completata da una risorsa che ha un orario di lavoro tipico di otto ore al giorno per cinque giorni alla settimana.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Un'attività che necessita di 120 ore di lavoro in cinque giorni](media/RM-how-to-21.png)

<span data-ttu-id="c5f4c-120">Il requisito è di 120 ore di ingegneria robotica durante cinque giorni, ovvero 24 ore al giorno.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Requisito giornaliero](media/RM-how-to-22.png)

<span data-ttu-id="c5f4c-122">Questo è un esempio di quando più risorse denominate sono necessarie per soddisfare una richiesta di risorse generiche.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="c5f4c-123">Devi quindi prenotare più risorse per soddisfare il requisito.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Prenotare molteplici risorse per soddisfare il requisito](media/RM-how-to-23.png)

<span data-ttu-id="c5f4c-125">La differenza principale in questo scenario è che la risorsa generica rimane nel team assegnato all'attività e i membri del team di risorse denominate prenotate non sono assegnati come parte della posizione.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="c5f4c-126">Il responsabile di progetto può assegnare il lavoro come appropriato alle risorse denominate.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="c5f4c-127">La vista **Riconciliazione** può consentire a un responsabile di progetto di suddividere le prenotazioni tra molteplici risorse per le assegnazioni delle attività.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="c5f4c-128">Questa operazione non viene eseguita automaticamente in quanto negli scenari più complessi, come nel caso in cui il requisito è costituito da un gruppo di attività, il sistema deve supporre l'intenzione con la quale il responsabile di progetto desidera eseguire le assegnazioni.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="c5f4c-129">Poiché il sistema non può comprendere l'intenzione, è probabile che quanto supposto sia differente da quanto previsto e che si abbia quindi un risultato incorretto o imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="c5f4c-130">Il risultato prevedibile è che la risorsa generica rimane assegnata fino a che il responsabile di progetto non crea deliberatamente assegnazioni mediante la vista **Riconciliazione**.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


