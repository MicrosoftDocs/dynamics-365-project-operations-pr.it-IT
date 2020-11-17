---
title: Proporre risorse di progetto
description: In questo argomento vengono fornite informazioni sulla proposta delle risorse di progetto.
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
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120188"
---
# <a name="propose-project-resources"></a><span data-ttu-id="4a5d5-103">Proporre risorse di progetto</span><span class="sxs-lookup"><span data-stu-id="4a5d5-103">Propose project resources</span></span>

<span data-ttu-id="4a5d5-104">I responsabili delle risorse possono proporre una risorsa al responsabile di progetto mediante una richiesta di risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="4a5d5-105">Nella griglia delle richieste o nella richiesta stessa, seleziona **Cerca risorse**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="4a5d5-106">Nella pagina **Assistente di pianificazione**, seleziona la risorsa e quindi, nel riquadro **Crea prenotazione risorsa**, nel campo **Stato di prenotazione**, seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Risorsa proposta selezionata.](media/Resource-Management-image62.png)

<span data-ttu-id="4a5d5-108">Lo stato viene aggiornato come segue:</span><span class="sxs-lookup"><span data-stu-id="4a5d5-108">The following status updates occur:</span></span>

- <span data-ttu-id="4a5d5-109">Nella pagina **Assistente di pianificazione**, gli indicatori di stato vengono aggiornati per indicare che la prenotazione è stata proposta ma che non è definitiva.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indicatori di stato per la prenotazione proposta nella pagina Assistente di pianificazione](media/Resource-Management-image63.png)

- <span data-ttu-id="4a5d5-111">Nella richiesta di risorsa, lo stato diventa **Revisione necessaria**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Stato della richiesta di risorsa aggiornato a Revisione necessaria](media/Resource-Management-image64.png)

- <span data-ttu-id="4a5d5-113">Nella scheda **Team** del progetto, il valore **Stato richiesta** del membro del team generico diventa **Revisione necessaria**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Stato della richiesta del membro del team generico aggiornato a Revisione necessaria nella scheda Team](media/Resource-Management-image48.png)

<span data-ttu-id="4a5d5-115">Il responsabile di progetto può accettare o rifiutare la proposta.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="4a5d5-116">Quando i responsabili di progetto elaborano i requisiti di risorsa, possono utilizzare uno dei seguenti approcci:</span><span class="sxs-lookup"><span data-stu-id="4a5d5-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="4a5d5-117">Proporre molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare le ore richieste.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="4a5d5-118">Le ore proposte vengono quindi suddivise tra molteplici risorse che possono soddisfare le ore richieste.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="4a5d5-119">In questo scenario, le ore non possono sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="4a5d5-120">Proporre meno risorse del necessario.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="4a5d5-121">In questo scenario, la capacità della risorsa proposta è inferiore alle ore necessarie specificate dal richiedente.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="4a5d5-122">Pertanto, quando il richiedente accetta le risorse proposte, un requisito di risorsa non soddisfatto viene creato per acquisire la domanda restante.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="4a5d5-123">Prenotare molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare il lavoro.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="4a5d5-124">Prenotare meno risorse del necessario.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-124">Book fewer resources than are required.</span></span> <span data-ttu-id="4a5d5-125">In questo scenario, le ore prenotate sono inferiori alle ore richieste.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="4a5d5-126">Il sistema ti guida per proporre risorse anziché prenotazioni, di modo che il richiedente possa verificare e tenere traccia della domanda restante.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="4a5d5-127">Utilizzo fatturabile</span><span class="sxs-lookup"><span data-stu-id="4a5d5-127">Billable utilization</span></span>

<span data-ttu-id="4a5d5-128">Le risorse possono avere un utilizzo di destinazione fatturabile.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="4a5d5-129">Questo utilizzo di destinazione è definito come attributo per il ruolo predefinito di una risorsa o impostato nel record della singola risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="4a5d5-130">I calcoli dell'utilizzo sono basati sulle ore effettive che le risorse hanno indicato utilizzando inserimenti ore approvati.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="4a5d5-131">Le seguenti formule vengono utilizzate per calcolare l'utilizzo:</span><span class="sxs-lookup"><span data-stu-id="4a5d5-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="4a5d5-132">Utilizzo fatturabile = Ore effettive addebitabili ÷ Capacità della risorsa</span><span class="sxs-lookup"><span data-stu-id="4a5d5-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="4a5d5-133">Utilizzo non fatturabile = Tempo effettivo con ID tipo di fatturazione = Non addebitabile, Complementare o Non disponibile ÷ Capacità della risorsa</span><span class="sxs-lookup"><span data-stu-id="4a5d5-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="4a5d5-134">Interno = Tempo effettivo senza contratto di vendita ÷ Capacità della risorsa</span><span class="sxs-lookup"><span data-stu-id="4a5d5-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="4a5d5-135">Capacità della risorsa = Ore lavorative della risorsa - Fuori sede - Giorni non lavorativi</span><span class="sxs-lookup"><span data-stu-id="4a5d5-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="4a5d5-136">La vista **Utilizzo risorsa** si trova nel riquadro **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Vista Utilizzo risorsa](media/Resource-Management-image65.png)

<span data-ttu-id="4a5d5-138">Ogni cella nella griglia rappresenta la percentuale di utilizzo fatturabile della risorsa in un periodo, ad esempio un giorno, una settimana o un mese.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="4a5d5-139">Le seguenti formule vengono utilizzate per colorare le celle:</span><span class="sxs-lookup"><span data-stu-id="4a5d5-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="4a5d5-140">**Verde:** utilizzo fatturabile \>= utilizzo di destinazione risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="4a5d5-141">**Giallo:** utilizzo di destinazione – 20 \<= utilizzo fatturabile \< utilizzo di destinazione</span><span class="sxs-lookup"><span data-stu-id="4a5d5-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="4a5d5-142">**Rosso:** utilizzo fatturabile \< utilizzo di destinazione – 20</span><span class="sxs-lookup"><span data-stu-id="4a5d5-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="4a5d5-143">Poiché la vista **Utilizzo risorsa** è basata sulla scheda di pianificazione, puoi utilizzare le funzionalità di filtro della scheda di pianificazione per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="4a5d5-144">La griglia richiede l'impostazione di un utilizzo di destinazione per il ruolo o la singola risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="4a5d5-145">A questo proposito, seleziona **Risorse** \> **Ruoli risorsa**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="4a5d5-146">Inoltre, un ruolo predefinito deve essere assegnato a ogni risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="4a5d5-147">Seleziona **Risorse** \> **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="4a5d5-148">Nella scheda **Project Service**, verifica che un ruolo risorsa sia definito e che il relativo campo **Predefinito** sia impostato su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="4a5d5-149">Puoi aggiungere ruoli aggiuntivi dove **Predefinito = No**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="4a5d5-150">Il ruolo dove **Predefinito = Sì** viene utilizzato per valutare l'utilizzo della risorsa in base alla destinazione di quel ruolo.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Ruolo predefinito impostato](media/Resource-Management-image67.png)

<span data-ttu-id="4a5d5-152">Nella scheda **Project Service**, puoi impostare un singolo utilizzo di destinazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="4a5d5-153">Per il calcolo dell'utilizzo viene quindi utilizzato l'utilizzo di destinazione allo scopo di valutare la destinazione della risorsa anziché la destinazione del ruolo predefinito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="4a5d5-154">L'utilizzo viene visualizzato per una risorsa solo se questa ha tempo addebitabile approvato durante il periodo visualizzato nella griglia.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="4a5d5-155">Disponibilità delle risorse</span><span class="sxs-lookup"><span data-stu-id="4a5d5-155">Resource availability</span></span>

<span data-ttu-id="4a5d5-156">È importante che i responsabili delle risorse siano in grado di visualizzare la disponibilità delle risorse e aggiornare le prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="4a5d5-157">In alcuni casi, non è necessaria una domanda formale (richiesta di risorsa), ma un responsabile delle risorse deve rispondere a una domanda non pianificata inviata tramite canali come un'e-mail, una telefonata o un sms.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="4a5d5-158">I responsabili delle risorse utilizzano la scheda di pianificazione per aggiornare le risorse e le prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="4a5d5-159">Le ore lavorative di una risorsa sono utilizzate come base per il calcolo della disponibilità della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="4a5d5-160">Le prenotazioni di risorse consumano la capacità delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-160">Resource bookings consume the capacity of the resources.</span></span>

![Scheda di pianificazione](media/Resource-Management-image68.png)

<span data-ttu-id="4a5d5-162">Nella scheda di pianificazione sono utilizzati colori e ombreggiature per indicare prenotazioni, disponibilità e sovraprenotazioni nonché lo stato delle prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="4a5d5-163">Una delle impostazioni della scheda di pianificazione consente di visualizzare una legenda.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="4a5d5-164">Se una freccia a destra viene visualizzata accanto a una singola risorsa prenotabile nella scheda di pianificazione, la risorsa può essere espansa per visualizzare i dettagli del lavoro per il quale la risorsa è prenotata.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Risorsa prenotabile espansa nella scheda di pianificazione](media/Resource-Management-image69.png)

<span data-ttu-id="4a5d5-166">Poiché Dynamics 365 Project Service Automation utilizza il motore Universal Resource Scheduling, se è installata anche la soluzione Dynamics 365 Field Service, puoi visualizzare i dettagli delle prenotazioni delle risorse per progetti, ordini di lavoro e qualsiasi altra entità a cui hai esteso la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Dettagli delle prenotazioni delle risorse per progetti e ordini di lavoro](media/Resource-Management-image70.png)

<span data-ttu-id="4a5d5-168">Per visualizzare ulteriori dettagli su una singola risorsa, fai clic con il pulsante destro del mouse sulla stessa per aprire la scheda della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Scheda della risorsa](media/Resource-Management-image71.png)
