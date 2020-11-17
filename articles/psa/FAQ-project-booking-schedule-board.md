---
title: Creare una prenotazione di progetto dalla scheda di pianificazione
description: In questo argomento vengono fornite informazioni su come creare una prenotazione di progetto dalla scheda di pianificazione.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: ccbfedec82b2d9035b51cf1b283ae5c441f1cbcc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122303"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="738a8-103">Creare una prenotazione di progetto dalla scheda di pianificazione</span><span class="sxs-lookup"><span data-stu-id="738a8-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="738a8-104">È possibile prenotare una risorsa in un progetto direttamente dalla scheda **Team** del progetto o generando un requisito di risorsa da un'assegnazione di membro del team generico e quindi soddisfacendo il requisito generato con un membro del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="738a8-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="738a8-105">È inoltre possibile prenotare una risorsa in un progetto direttamente dalla scheda di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="738a8-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="738a8-106">A questo scopo è possibile procedere in tre modi:</span><span class="sxs-lookup"><span data-stu-id="738a8-106">There are three ways to do this:</span></span>

- <span data-ttu-id="738a8-107">**Prenotare da un requisito di risorsa generato:** è possibile generare un requisito di risorsa dopo aver creato una risorsa generica e assegnare attività in un progetto.</span><span class="sxs-lookup"><span data-stu-id="738a8-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="738a8-108">**Prenotare dal requisito primario:** i requisiti principali sono visualizzati nella scheda di pianificazione nella scheda **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="738a8-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="738a8-109">**Prenotare da un nuovo requisito di risorsa:** è possibile creare un requisito di risorsa da zero e associarlo a un progetto.</span><span class="sxs-lookup"><span data-stu-id="738a8-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="738a8-110">Nella scheda di pianificazione, il requisito di risorsa è visualizzato nella scheda **Apri requisiti**.</span><span class="sxs-lookup"><span data-stu-id="738a8-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="738a8-111">Prenotare da un requisito di risorsa generato</span><span class="sxs-lookup"><span data-stu-id="738a8-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="738a8-112">È possibile creare una risorsa generica e assegnarla a una o più attività in un progetto.</span><span class="sxs-lookup"><span data-stu-id="738a8-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="738a8-113">Successivamente, è possibile generare un requisito di risorsa dal membro del team generico.</span><span class="sxs-lookup"><span data-stu-id="738a8-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="738a8-114">Nella scheda di pianificazione, questa risorsa sarà visualizzata nella scheda **Apri requisiti**. I filtri delle colonne nella griglia possono rivelarsi utili se vi sono molti requisiti aperti.</span><span class="sxs-lookup"><span data-stu-id="738a8-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="738a8-115">![Scheda Apri requisiti nella scheda di pianificazione](media/FAQ-Project-Booking-Schedule-Board-1.png "Tabella delle prenotazioni e delle assegnazioni")</span><span class="sxs-lookup"><span data-stu-id="738a8-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="738a8-116">Selezionare il requisito.</span><span class="sxs-lookup"><span data-stu-id="738a8-116">Select the requirement.</span></span> <span data-ttu-id="738a8-117">La scheda **Trova disponibilità** verrà visualizzata nella parte superiore della riga selezionata.</span><span class="sxs-lookup"><span data-stu-id="738a8-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="738a8-118">La selezione della scheda attiva la modalità Assistente di pianificazione della scheda di pianificazione e filtra le risorse disponibili che soddisfano il requisito di risorsa.</span><span class="sxs-lookup"><span data-stu-id="738a8-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="738a8-119">A questo punto è possibile prenotare una risorsa.</span><span class="sxs-lookup"><span data-stu-id="738a8-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="738a8-120">È inoltre possibile trascinare la riga selezionata dalla parte inferiore della scheda di pianificazione in una cella della risorsa nella griglia precedente.</span><span class="sxs-lookup"><span data-stu-id="738a8-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="738a8-121">Viene visualizzato il pannello **Crea prenotazione risorsa** a destra.</span><span class="sxs-lookup"><span data-stu-id="738a8-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="738a8-122">Se si seleziona **Prenota**, la risorsa viene prenotata nel team di progetto.</span><span class="sxs-lookup"><span data-stu-id="738a8-122">Selecting **Book** books the resource onto the project team.</span></span>

![Pannello Crea prenotazione risorsa](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="738a8-124">Prenotare dal requisito primario</span><span class="sxs-lookup"><span data-stu-id="738a8-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="738a8-125">La creazione di un progetto in Project Service crea automaticamente un requisito di risorsa definito requisito primario.</span><span class="sxs-lookup"><span data-stu-id="738a8-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="738a8-126">Si tratta di un requisito vuoto utilizzato per prenotare rapidamente una risorsa con la scheda di pianificazione senza generare un requisito o crearne uno da zero.</span><span class="sxs-lookup"><span data-stu-id="738a8-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="738a8-127">Poiché il requisito è vuoto, sarà necessario specificare le date nonché il metodo di allocazione e le ore se applicabile.</span><span class="sxs-lookup"><span data-stu-id="738a8-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="738a8-128">Per prenotare una risorsa con il requisito primario, nella scheda di pianificazione, selezionare la scheda **Progetto**. Se esistono più progetti, il filtro della colonna **Progetto** può consentire di trovare più facilmente il progetto desiderato.</span><span class="sxs-lookup"><span data-stu-id="738a8-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="738a8-129">![Filtri della colonna nella scheda di pianificazione](media/FAQ-Project-Booking-Schedule-Board-2.png "Tabella delle prenotazioni e delle assegnazioni")</span><span class="sxs-lookup"><span data-stu-id="738a8-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="738a8-130">Selezionare il requisito il cui nome è quello del progetto e la cui durata è zero (0).</span><span class="sxs-lookup"><span data-stu-id="738a8-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="738a8-131">Selezionare la scheda **Trova disponibilità** visualizzata nella riga selezionata.</span><span class="sxs-lookup"><span data-stu-id="738a8-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="738a8-132">In questo modo, viene attivata la modalità Assistente di pianificazione della scheda di pianificazione e vengono visualizzate le risorse disponibili che possono essere prenotate per il progetto.</span><span class="sxs-lookup"><span data-stu-id="738a8-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="738a8-133">Poiché un **requisito primario** è un requisito vuoto con durata zero (0), è necessario impostare la durata nel pannello **Crea prenotazione risorsa** quando si seleziona e prenota una risorsa.</span><span class="sxs-lookup"><span data-stu-id="738a8-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="738a8-134">È inoltre possibile selezionare il **requisito primario del progetto** nella parte inferiore della scheda di pianificazione e trascinarlo su una risorsa per prenotarla.</span><span class="sxs-lookup"><span data-stu-id="738a8-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="738a8-135">Poiché un **requisito primario** è un requisito vuoto con durata zero (0), è necessario impostare la durata nel pannello **Crea prenotazione risorsa** quando si seleziona e prenota una risorsa.</span><span class="sxs-lookup"><span data-stu-id="738a8-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="738a8-136">Quando si prenota una risorsa mediante il **requisito primario** nella scheda di pianificazione, lo si aggiunge al team del progetto senza alcuna attività.</span><span class="sxs-lookup"><span data-stu-id="738a8-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="738a8-137">Prenotare da un nuovo requisito di risorsa</span><span class="sxs-lookup"><span data-stu-id="738a8-137">Book from a new resource requirement</span></span>
<span data-ttu-id="738a8-138">Completare i passaggi seguenti per prenotare da un nuovo requisito di risorsa.</span><span class="sxs-lookup"><span data-stu-id="738a8-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="738a8-139">Accedere a **Requisiti di risorsa** e selezionare **Nuovo** per creare un nuovo requisito di risorsa.</span><span class="sxs-lookup"><span data-stu-id="738a8-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="738a8-140">Nella scheda **Progetto**, selezionare un progetto per associare il requisito al progetto.</span><span class="sxs-lookup"><span data-stu-id="738a8-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="738a8-141">Nella scheda di pianificazione, questo nuovo requisito è visualizzato come **requisito aperto** che è possibile soddisfare.</span><span class="sxs-lookup"><span data-stu-id="738a8-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="738a8-142">Prenotare la risorsa per aggiungerla al team di progetto.</span><span class="sxs-lookup"><span data-stu-id="738a8-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="738a8-143">Ora che la risorsa è prenotata, è necessario assegnare manualmente le attività.</span><span class="sxs-lookup"><span data-stu-id="738a8-143">Now that the resource is booked, you must assign tasks manually.</span></span>

