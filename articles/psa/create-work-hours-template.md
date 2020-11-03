---
title: Creare un modello di ore lavorative
description: Come creare un modello delle ore lavorative in Project Service
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
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078886"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="b837d-103">Creare un modello delle ore lavorative (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b837d-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b837d-104">Prima di creare le pianificazioni di progetto, devi impostare un calendario di progetto che definisce il numero di ore lavorative da sistemare ogni giorno nella pianificazione e in tutte le chiusure aziendali.</span><span class="sxs-lookup"><span data-stu-id="b837d-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="b837d-105">Questo si ottiene con un modello di ore lavorative, contenente dettagli sulle ore lavorative per giorni, giorni di ferie, e altre chiusure aziendali.</span><span class="sxs-lookup"><span data-stu-id="b837d-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="b837d-106">Quando crei un progetto, associa un modello di lavoro al calendario di progetto per applicare la pianificazione per il progetto.</span><span class="sxs-lookup"><span data-stu-id="b837d-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="b837d-107">Ci sono due modi per creare un modello delle ore lavorative:</span><span class="sxs-lookup"><span data-stu-id="b837d-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="b837d-108">Crea un modello delle ore lavorative in base al calendario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b837d-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="b837d-109">Crea un nuovo modello di ore lavorative.</span><span class="sxs-lookup"><span data-stu-id="b837d-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="b837d-110">Per creare un modello delle ore lavorative in base al calendario della risorsa</span><span class="sxs-lookup"><span data-stu-id="b837d-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="b837d-111">Passa a **Project Service > Risorse**.</span><span class="sxs-lookup"><span data-stu-id="b837d-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="b837d-112">Seleziona la risorsa su cui desideri basare le ore lavorative.</span><span class="sxs-lookup"><span data-stu-id="b837d-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="b837d-113">Fai clic su **Salva calendario con nome** , inserisci un nome per il modello delle ore lavorative e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="b837d-113">Click **Save Calendar As** , enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="b837d-114">Una volta completata la modifica delle opzioni, fai clic su **Salva e chiudi**.</span><span class="sxs-lookup"><span data-stu-id="b837d-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="b837d-115">Fai clic sul pulsante **Salva** nell'angolo in basso a destra dello schermo.</span><span class="sxs-lookup"><span data-stu-id="b837d-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="b837d-116">Per creare un nuovo modello di ore lavorative</span><span class="sxs-lookup"><span data-stu-id="b837d-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="b837d-117">Passa a **Project Service > Modelli ore lavorative**.</span><span class="sxs-lookup"><span data-stu-id="b837d-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="b837d-118">Fare clic su **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="b837d-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="b837d-119">Immetti un nome per il modello ore lavorative.</span><span class="sxs-lookup"><span data-stu-id="b837d-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="b837d-120">Seleziona una risorsa su cui basare le ore lavorative a e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="b837d-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b837d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b837d-121">See Also</span></span>  
 [<span data-ttu-id="b837d-122">Configurare le risorse</span><span class="sxs-lookup"><span data-stu-id="b837d-122">Set up resources</span></span>](../psa/set-up-resources.md)
