---
title: Prenotare provvisoriamente requisiti
description: In questo argomento vengono fornite informazioni su come prenotare provvisoriamente i requisiti.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124103"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="b0c25-103">Prenotare provvisoriamente requisiti</span><span class="sxs-lookup"><span data-stu-id="b0c25-103">Soft-book requirements</span></span>

<span data-ttu-id="b0c25-104">Un requisito di risorsa può essere prenotato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="b0c25-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="b0c25-105">Una prenotazione definitiva crea una proposta che consuma la capacità di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="b0c25-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="b0c25-106">La proposta viene quindi rispedita al richiedente per l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="b0c25-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="b0c25-107">Una prenotazione provvisoria aggiunge una risorsa a un team di progetto e ha uno stato differente nella scheda di pianificazione, ma non consuma la capacità della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b0c25-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="b0c25-108">Per prenotare provvisoriamente una risorsa nella scheda di pianificazione, imposta il campo **Stato di prenotazione** su **Provvisoria**.</span><span class="sxs-lookup"><span data-stu-id="b0c25-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Stato di prenotazione impostato su Provvisoria](media/Resource-Management-image77.png)

<span data-ttu-id="b0c25-110">Quando la scheda **Team** è visualizzata nella vista **Membri del team con nome**, la risorsa è visualizzata in quella scheda.</span><span class="sxs-lookup"><span data-stu-id="b0c25-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="b0c25-111">Le ore prenotate provvisoriamente sono indicate nella colonna **Ore prenotate provvisoriamente**.</span><span class="sxs-lookup"><span data-stu-id="b0c25-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Ore prenotate provvisoriamente nella vista Membri del team con nome](media/Resource-Management-image78.png)

<span data-ttu-id="b0c25-113">I membri del team prenotati provvisoriamente possono essere assegnati ad attività.</span><span class="sxs-lookup"><span data-stu-id="b0c25-113">Soft-booked team members can be assigned to tasks.</span></span>

![Membro del team prenotato provvisoriamente assegnato a un'attività](media/Resource-Management-image79.png)

<span data-ttu-id="b0c25-115">Nella scheda **Riconciliazione**, le prenotazioni di una risorsa prenotata provvisoriamente non sono visualizzate in quanto la scheda **Riconciliazione** considera solo le prenotazioni definitive.</span><span class="sxs-lookup"><span data-stu-id="b0c25-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Risorsa prenotata provvisoriamente senza prenotazioni nella scheda Riconciliazione](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="b0c25-117">Non è possibile prenotare provvisoriamente una risorsa a partire da un requisito generato da un membro del team generico.</span><span class="sxs-lookup"><span data-stu-id="b0c25-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="b0c25-118">Nella scheda di pianificazione, le prenotazioni provvisorie per una risorsa sono indicate con un colore differente.</span><span class="sxs-lookup"><span data-stu-id="b0c25-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Prenotazioni provvisorie nella scheda di pianificazione](media/Resource-Management-image81.png)

<span data-ttu-id="b0c25-120">Per convertire una prenotazione provvisoria in una definitiva, nella scheda di pianificazione fai clic con il pulsante destro del mouse sulla prenotazione provvisoria e quindi scegli **Cambia stato** \> **Prenota definitivamente** \> **Definitiva**.</span><span class="sxs-lookup"><span data-stu-id="b0c25-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Modificare lo stato della prenotazione in Definitiva](media/Resource-Management-image82.png)

<span data-ttu-id="b0c25-122">La prenotazione e lo stato vengono modificati nella scheda di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b0c25-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="b0c25-123">Poiché lo stato della prenotazione è ora **Definitiva**, la risorsa è visualizzata come prenotata e le relative capacità e disponibilità vengono rettificate.</span><span class="sxs-lookup"><span data-stu-id="b0c25-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="b0c25-124">Puoi utilizzare lo stesso metodo per annullare una prenotazione definitiva o provvisoria nella scheda di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b0c25-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="b0c25-125">Per convertire una risorsa prenotata provvisoriamente in una prenotata definitivamente nella scheda **Team** del progetto, seleziona la risorsa e quindi **Conferma**.</span><span class="sxs-lookup"><span data-stu-id="b0c25-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Comando Conferma](media/Resource-Management-image83.png)
