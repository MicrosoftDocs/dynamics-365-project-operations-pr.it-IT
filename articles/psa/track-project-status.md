---
title: Tener traccia dello stato di un progetto
description: Come registrare lo stato di un progetto in Project Service
author: ruhercul
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014391"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="f3ed8-103">Registrare lo stato di un progetto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f3ed8-104">Utilizzare [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] per registrare l'avanzamento di un progetto del cliente.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="f3ed8-105">Quando l'impegno avanza, le fasi del progetto si aggiornano per riflettere la fase dell'impegno:</span><span class="sxs-lookup"><span data-stu-id="f3ed8-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="f3ed8-106">**Nuovo**</span><span class="sxs-lookup"><span data-stu-id="f3ed8-106">**New**</span></span>    | <span data-ttu-id="f3ed8-107">Quando crei un progetto, la fase è impostata su **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="f3ed8-108">Se hai creato il progetto da un modello, in questa fase il progetto potrebbe avere una pianificazione, stime e dati del team.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="f3ed8-109">In caso contrario, sarà la struttura del progetto e sarà necessario immettere manualmente il resto dei componenti del progetto.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="f3ed8-110">**Offerta**</span><span class="sxs-lookup"><span data-stu-id="f3ed8-110">**Quote**</span></span>   |      <span data-ttu-id="f3ed8-111">Quando si associa un progetto a un'offerta o lo si crea da un'offerta, la fase del progetto è impostata su **Offerta** e anche le date di inizio e di fine stimate vengono aggiornate.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="f3ed8-112">Quando il progetto si trova nella fase di offerta, vengono visualizzati dettagli sull'offerta nella scheda **Vendite** della pagina **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="f3ed8-113">**Piano**</span><span class="sxs-lookup"><span data-stu-id="f3ed8-113">**Plan**</span></span>   |                                     <span data-ttu-id="f3ed8-114">Quando viene acquisita un'offerta associata a un progetto e quando l'impegno avanza alla fase contratto, la fase del progetto si aggiorna a **Piano**.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="f3ed8-115">I dettagli del contratto vengono visualizzati nella scheda **Vendite** nella pagina **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="f3ed8-116">**Completo**</span><span class="sxs-lookup"><span data-stu-id="f3ed8-116">**Complete**</span></span> |                    <span data-ttu-id="f3ed8-117">Quando il lavoro del progetto è completato, puoi passare la fase a **Completa**.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="f3ed8-118">Quando la fase del progetto è impostata su completo, è chiaro che il lavoro è completato al 100% ma viene tenuto aperto per tutte le voci di tempo e spesa da registrare.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="f3ed8-119">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="f3ed8-119">**Close**</span></span>   |           <span data-ttu-id="f3ed8-120">Quando tutte le transazioni sono state registrate nel progetto e non prevedi di registrarne altre, puoi impostare manualmente la fase su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="f3ed8-121">Quando il progetto è impostato su **Chiudi**, non è possibile registrare altre transazioni nel progetto e questo sarà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="f3ed8-122">Per registra lo stato del progetto</span><span class="sxs-lookup"><span data-stu-id="f3ed8-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="f3ed8-123">Passa a **Project Service > Progetti**.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="f3ed8-124">Fai clic sul progetto che desideri utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="f3ed8-125">Nella barra sulla parte superiore dello schermo, seleziona la freccia in giù accanto al nome del progetto e quindi fai clic su **Registrazione di progetto**.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="f3ed8-126">Seleziona **Registrazione lavoro richiesto** o **Registrazione costi** nell'elenco a discesa sull'elenco attività.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="f3ed8-127">Fai doppio clic sull'attività per modificarla.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-127">Double-click any task to edit it.</span></span> <span data-ttu-id="f3ed8-128">Puoi anche spostare o ridimensionare le barre nel diagramma di Gantt per modificare l'ora e l'avanzamento di un'attività.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="f3ed8-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3ed8-129">See Also</span></span>  
 [<span data-ttu-id="f3ed8-130">Guida del responsabile di progetto</span><span class="sxs-lookup"><span data-stu-id="f3ed8-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]