---
title: Esaminare le risorse proposte
description: In questo argomento vengono fornite informazioni su come proporre risorse di progetto.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401178"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="89c39-103">Esaminare le risorse proposte</span><span class="sxs-lookup"><span data-stu-id="89c39-103">Review proposed resources</span></span>

<span data-ttu-id="89c39-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="89c39-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="89c39-105">I responsabili delle risorse possono proporre una risorsa al responsabile di progetto mediante una richiesta di risorsa.</span><span class="sxs-lookup"><span data-stu-id="89c39-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="89c39-106">Nella griglia delle richieste o nella richiesta stessa, seleziona **Cerca risorse**.</span><span class="sxs-lookup"><span data-stu-id="89c39-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="89c39-107">Nella pagina **Assistente di pianificazione**, seleziona la risorsa e quindi, nel riquadro **Crea prenotazione risorsa**, nel campo **Stato di prenotazione**, seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="89c39-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="89c39-108">Lo stato viene aggiornato come segue:</span><span class="sxs-lookup"><span data-stu-id="89c39-108">The following status updates occur:</span></span>

- <span data-ttu-id="89c39-109">Nella pagina **Assistente di pianificazione**, gli indicatori di stato vengono aggiornati per indicare che la prenotazione è stata proposta ma che non è definitiva.</span><span class="sxs-lookup"><span data-stu-id="89c39-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="89c39-110">Nella richiesta di risorsa, lo stato diventa **Revisione necessaria**.</span><span class="sxs-lookup"><span data-stu-id="89c39-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="89c39-111">Nella scheda **Team** del progetto, il valore **Stato richiesta** del membro del team generico diventa **Revisione necessaria**.</span><span class="sxs-lookup"><span data-stu-id="89c39-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="89c39-112">Il responsabile di progetto può accettare o rifiutare la proposta.</span><span class="sxs-lookup"><span data-stu-id="89c39-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="89c39-113">Quando i responsabili di progetto elaborano i requisiti di risorsa, possono utilizzare uno dei seguenti approcci:</span><span class="sxs-lookup"><span data-stu-id="89c39-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="89c39-114">Proporre molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare le ore richieste.</span><span class="sxs-lookup"><span data-stu-id="89c39-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="89c39-115">Le ore proposte vengono quindi suddivise tra molteplici risorse che possono soddisfare le ore richieste.</span><span class="sxs-lookup"><span data-stu-id="89c39-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="89c39-116">In questo scenario, le ore non possono sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="89c39-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="89c39-117">Proporre meno risorse del necessario.</span><span class="sxs-lookup"><span data-stu-id="89c39-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="89c39-118">In questo scenario, la capacità della risorsa proposta è inferiore alle ore necessarie specificate dal richiedente.</span><span class="sxs-lookup"><span data-stu-id="89c39-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="89c39-119">Pertanto, quando il richiedente accetta le risorse proposte, un requisito di risorsa non soddisfatto viene creato per acquisire la domanda restante.</span><span class="sxs-lookup"><span data-stu-id="89c39-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="89c39-120">Prenotare molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare il lavoro.</span><span class="sxs-lookup"><span data-stu-id="89c39-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="89c39-121">Prenotare meno risorse del necessario.</span><span class="sxs-lookup"><span data-stu-id="89c39-121">Book fewer resources than are required.</span></span> <span data-ttu-id="89c39-122">In questo scenario, le ore prenotate sono inferiori alle ore richieste.</span><span class="sxs-lookup"><span data-stu-id="89c39-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="89c39-123">Il sistema ti guida per proporre risorse anziché prenotazioni, di modo che il richiedente possa verificare e tenere traccia della domanda restante.</span><span class="sxs-lookup"><span data-stu-id="89c39-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="89c39-124">Disponibilità delle risorse</span><span class="sxs-lookup"><span data-stu-id="89c39-124">Resource availability</span></span>

<span data-ttu-id="89c39-125">È importante che i responsabili delle risorse siano in grado di visualizzare la disponibilità delle risorse e aggiornare le prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="89c39-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="89c39-126">In alcuni casi, non è necessaria una domanda formale (richiesta di risorsa), ma un responsabile delle risorse deve rispondere a una domanda non pianificata inviata tramite canali come un'e-mail, una telefonata o un sms.</span><span class="sxs-lookup"><span data-stu-id="89c39-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="89c39-127">I responsabili delle risorse utilizzano la scheda di pianificazione per aggiornare le risorse e le prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="89c39-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="89c39-128">Le ore lavorative di una risorsa sono utilizzate come base per il calcolo della disponibilità della risorsa.</span><span class="sxs-lookup"><span data-stu-id="89c39-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="89c39-129">Le prenotazioni di risorse consumano la capacità delle risorse.</span><span class="sxs-lookup"><span data-stu-id="89c39-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="89c39-130">Nella scheda di pianificazione sono utilizzati colori e ombreggiature per indicare prenotazioni, disponibilità e sovraprenotazioni nonché lo stato delle prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="89c39-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="89c39-131">Una delle impostazioni della scheda di pianificazione consente di visualizzare una legenda.</span><span class="sxs-lookup"><span data-stu-id="89c39-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="89c39-132">Se una freccia a destra viene visualizzata accanto a una singola risorsa prenotabile nella scheda di pianificazione, la risorsa può essere espansa per visualizzare i dettagli del lavoro per il quale la risorsa è prenotata.</span><span class="sxs-lookup"><span data-stu-id="89c39-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="89c39-133">Poiché Dynamics 365 Project Operations utilizza il motore Universal Resource Scheduling, se è installata anche la soluzione Dynamics 365 Field Service, puoi visualizzare i dettagli delle prenotazioni delle risorse per progetti, ordini di lavoro e qualsiasi altra entità a cui hai esteso la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="89c39-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="89c39-134">Per visualizzare ulteriori dettagli su una singola risorsa, fai clic con il pulsante destro del mouse sulla stessa per aprire la scheda della risorsa.</span><span class="sxs-lookup"><span data-stu-id="89c39-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

