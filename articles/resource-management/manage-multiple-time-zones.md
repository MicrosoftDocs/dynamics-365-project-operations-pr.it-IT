---
title: Gestire i fusi orario
description: Quando viene creato un progetto, il fuso orario si basa sul fuso orario definito nel modello di ore lavorative applicato.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119828"
---
# <a name="manage-time-zones"></a><span data-ttu-id="112e8-103">Gestire i fusi orario</span><span class="sxs-lookup"><span data-stu-id="112e8-103">Manage time zones</span></span>

<span data-ttu-id="112e8-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="112e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="112e8-105">Progetti</span><span class="sxs-lookup"><span data-stu-id="112e8-105">Projects</span></span>

<span data-ttu-id="112e8-106">Quando viene creato un progetto, il fuso orario si basa sul fuso orario definito nel modello di ore lavorative applicato.</span><span class="sxs-lookup"><span data-stu-id="112e8-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="112e8-107">Sul modulo **Progetto**, le date sono sempre relative al fuso orario dell'utente che ha effettuato l'accesso a ciascuna scheda, ad eccezione della scheda **Attività**. Quando visualizzi la struttura di suddivisione del lavoro, le date verranno sempre visualizzate nel fuso orario del progetto.</span><span class="sxs-lookup"><span data-stu-id="112e8-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="112e8-108">Attività</span><span class="sxs-lookup"><span data-stu-id="112e8-108">Tasks</span></span>

<span data-ttu-id="112e8-109">Quando viene creata un'attività, l'ora di inizio, l'ora di fine e le ore/giorno sono controllate dalle ore lavorative del progetto.</span><span class="sxs-lookup"><span data-stu-id="112e8-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="112e8-110">Ad esempio, se un'attività viene creata con un progetto il cui fuso orario è -8 PST e ha le seguenti ore lavorative: dalle 9:00 alle 17:00 dal lunedì al venerdì, qualsiasi attività creata senza un'assegnazione rispetterà l'ora di inizio e l'ora di fine del calendario del progetto.</span><span class="sxs-lookup"><span data-stu-id="112e8-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="112e8-111">Gestire le risorse con i fusi orari</span><span class="sxs-lookup"><span data-stu-id="112e8-111">Manage resources with time zones</span></span>

<span data-ttu-id="112e8-112">Per risultati accurati e prevedibili durante l'utilizzo di **Estendi prenotazione**, ci sono due prerequisiti chiave che devono essere soddisfatti:</span><span class="sxs-lookup"><span data-stu-id="112e8-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="112e8-113">L'utente deve configurare il fuso orario del proprio dispositivo in modo che corrisponda al fuso orario definito nelle **Impostazioni di personalizzazione** del sistema.</span><span class="sxs-lookup"><span data-stu-id="112e8-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Impostazioni di fuso orario in Windows 10](media/reconcile-assignments-03.png)

  ![Impostazioni di fuso orario nelle impostazioni di personalizzazione](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="112e8-116">La risorsa prenotabile deve avere almeno un minuto di orario di lavoro che si sovrappone ai profili utilizzati per definire l'estensione richiesta.</span><span class="sxs-lookup"><span data-stu-id="112e8-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="112e8-117">Ad esempio, le seguenti risorse con orari di lavoro compresi tra le 9:00 e le 19:00.</span><span class="sxs-lookup"><span data-stu-id="112e8-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Confronto dei profili delle risorse](media/reconcile-assignments-05.png)

<span data-ttu-id="112e8-119">La tabella seguente mostra:</span><span class="sxs-lookup"><span data-stu-id="112e8-119">The following table shows:</span></span>

- <span data-ttu-id="112e8-120">Un modello di calendario di progetto</span><span class="sxs-lookup"><span data-stu-id="112e8-120">A project calendar template</span></span>
- <span data-ttu-id="112e8-121">Risorsa A: questa risorsa ha lo stesso calendario ed è nello stesso fuso orario del progetto.</span><span class="sxs-lookup"><span data-stu-id="112e8-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="112e8-122">L'ora di inizio delle prenotazioni sarà alle 9:00.</span><span class="sxs-lookup"><span data-stu-id="112e8-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="112e8-123">Risorsa B: questa risorsa si trova in un fuso orario diverso da quello del progetto e inizia alle 7:00 del suo fuso orario.</span><span class="sxs-lookup"><span data-stu-id="112e8-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="112e8-124">Tuttavia, le prenotazioni inizieranno alle 9:00 in quanto è il primo orario di inizio del profilo dell'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="112e8-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="112e8-125">Risorse C e D: le risorse si trovano in fusi orari diversi, sia diversi l'uno dall'altro che dal progetto, e le loro prenotazioni iniziano non prima dei rispettivi orari di inizio disponibili.</span><span class="sxs-lookup"><span data-stu-id="112e8-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="112e8-126">Entità</span><span class="sxs-lookup"><span data-stu-id="112e8-126">Entity</span></span>  |<span data-ttu-id="112e8-127">Calendario</span><span class="sxs-lookup"><span data-stu-id="112e8-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="112e8-128">Modello di calendario di progetto</span><span class="sxs-lookup"><span data-stu-id="112e8-128">Project calendar template</span></span>   | ![calendario di progetto](media/reconcile-assignments-06.png) |
|<span data-ttu-id="112e8-130">Risorsa A</span><span class="sxs-lookup"><span data-stu-id="112e8-130">Resource A</span></span>  | ![Calendario della risorsa A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="112e8-132">Risorsa B</span><span class="sxs-lookup"><span data-stu-id="112e8-132">Resource B</span></span>  |  ![Calendario della risorsa B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="112e8-134">Risorsa C</span><span class="sxs-lookup"><span data-stu-id="112e8-134">Resource C</span></span>  |  ![Calendario della risorsa C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="112e8-136">Risorsa D</span><span class="sxs-lookup"><span data-stu-id="112e8-136">Resource D</span></span>  | ![Calendario della risorsa D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="112e8-138">Quando ti sposti nella vista **Riconciliazione**, vengono visualizzate le assegnazioni di risorse e le relative prenotazioni insufficienti.</span><span class="sxs-lookup"><span data-stu-id="112e8-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Visualizzazione di riconciliazione prima dell'estensione](media/reconcile-assignments-10.png)

<span data-ttu-id="112e8-140">Dopo che la funzionalità di estensione della prenotazione è stata utilizzata per ciascuna risorsa, le prenotazioni vengono estese per ogni risorsa perché le ore lavorative di ciascuna risorsa si sovrappongono ai profili dell'insufficienza.</span><span class="sxs-lookup"><span data-stu-id="112e8-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Visualizzazione di riconciliazione dopo l'estensione della prenotazione](media/reconcile-assignments-11.png) 

<span data-ttu-id="112e8-142">Tieni presente che esaminando attentamente i dettagli delle prenotazioni puoi visualizzare le differenze nell'orario di inizio delle prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="112e8-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="112e8-143">Le prenotazioni iniziano non prima dell'ora di inizio del profilo di assegnazione e non prima dell'ora di inizio disponibile della risorsa.</span><span class="sxs-lookup"><span data-stu-id="112e8-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nuove prenotazioni delle risorse nella scheda di pianificazione](media/reconcile-assignments-12.png)
