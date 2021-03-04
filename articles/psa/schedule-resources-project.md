---
title: Pianificare risorse per un progetto
description: Come pianificare le risorse per un progetto in Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150448"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="d7fb1-103">Pianificare le risorse per un progetto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d7fb1-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d7fb1-104">Puoi verificare la disponibilità di una risorsa per ottenere una visione globale di come sono prenotate le risorse, oppure puoi filtrare la in base alle competenze, il team, la posizione e altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="d7fb1-105">Nella scheda di pianificazione sono visualizzati l'elenco di risorse e le relative disponibilità.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="d7fb1-106">Seleziona la modalità di visualizzazione per vedere la disponibilità in base a **Ore**, **Giorno**, **Settimana** o **Mese**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="d7fb1-107">Prima di utilizzare la scheda di pianificazione, è importante configurarla.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="d7fb1-108">Per ulteriori informazioni, vedi [Configurare la scheda di pianificazione (Field Service, Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="d7fb1-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="d7fb1-109">Se utilizzi una versione precedente, per la disponibilità delle risorse, vedi [Visualizzare la disponibilità delle risorse](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="d7fb1-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="d7fb1-110">Per utilizzare la funzionalità di prenotazione della scheda di pianificazione, la geocodifica e i servizi di localizzazione, è necessario abilitare le mappe.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="d7fb1-111">Nel menu principale seleziona **Pianificazione risorse** > **Amministrazione**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="d7fb1-112">Fai clic su **Parametri di pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="d7fb1-113">Apri il record e scorri verso il basso fino alla sezione **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="d7fb1-114">Nel campo **Connetti a Mappe** scegli **Sì**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="d7fb1-115">Accettare le condizioni e salvare il record.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="d7fb1-116">Nel menu principale seleziona **Project Service** > **Scheda di pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="d7fb1-117">Da qui, esistono diversi modi per pianificare manualmente un requisito di prenotazione.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="d7fb1-118">Seleziona il metodo più adatto per te.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="d7fb1-119">Trovare le risorse disponibili</span><span class="sxs-lookup"><span data-stu-id="d7fb1-119">Find available resources</span></span>

1.  <span data-ttu-id="d7fb1-120">Nell'elenco **Requisiti di prenotazione** fai clic con il pulsante destro del mouse sulla prenotazione non pianificata e scegli una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7fb1-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="d7fb1-121">Scegli **Trova disponibilità - risorse correnti** per individuare una risorsa disponibile nell'elenco nella scheda di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="d7fb1-122">Scegli **Trova disponibilità - Tutte le risorse** per individuare una risorsa disponibile nelle risorse del sistema</span><span class="sxs-lookup"><span data-stu-id="d7fb1-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="d7fb1-123">Se esegui tale operazione, i filtri mostreranno le opzioni per il requisito di prenotazione selezionato.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="d7fb1-124">Quando viene visualizzato uno slot disponibile, fai clic con il pulsante destro del mouse sull'intervallo di tempo nella scheda di pianificazione e scegli **Prenota qui**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="d7fb1-125">In alternativa, trascina e rilascia il requisito della prenotazione sull'intervallo di tempo disponibile.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="d7fb1-126">Prenota una risorsa mediante la visualizzazione giornaliera e trova chi è prenotato sotto la disponibilità</span><span class="sxs-lookup"><span data-stu-id="d7fb1-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="d7fb1-127">Nella scheda di pianificazione seleziona **Modalità di visualizzazione**, quindi **Giorni**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="d7fb1-128">Questo diagramma illustra la visualizzazione griglia del numero di ore che una risorsa è prenotata al giorno e i quali giorni sono liberi.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="d7fb1-129">Fai clic sul nome della risorsa che desideri prenotare, quindi seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="d7fb1-130">Nella finestra dialogo **Crea prenotazione risorsa** scegli il progetto per cui desideri prenotare la risorsa con il metodo di prenotazione e gli orari di inizio e fine.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="d7fb1-131">Al termine, seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="d7fb1-132">Visualizzare la scheda di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d7fb1-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="d7fb1-133">Seleziona un requisito di pianificazione non pianificato nell'elenco nella parte inferiore.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="d7fb1-134">Trascina il requisito di prenotazione in una risorsa/intervallo di tempo disponibile nella scheda di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="d7fb1-135">Al termine, seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="d7fb1-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="d7fb1-136">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="d7fb1-136">Additional resources</span></span>  
 [<span data-ttu-id="d7fb1-137">Guida di Resource Manager</span><span class="sxs-lookup"><span data-stu-id="d7fb1-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
