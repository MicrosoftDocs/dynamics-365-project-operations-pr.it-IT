---
title: Visualizzare l‘utilizzo addebitabile per le risorse
description: In questo argomento vengono fornite informazioni sulla vista utilizzo risorse.
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
ms.openlocfilehash: a1d1db532c65b2a13f3cf4e1281a5987490b96df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122168"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="be8e0-103">Visualizzare l‘utilizzo addebitabile per le risorse</span><span class="sxs-lookup"><span data-stu-id="be8e0-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="be8e0-104">La **vista utilizzo** nella pagina **Utilizzo risorse di Project Service** mostra l'utilizzo addebitabile per ogni risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="be8e0-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="be8e0-105">Poiché la vista è basata sulla scheda di pianificazione, include molte delle funzionalità di quella scheda.</span><span class="sxs-lookup"><span data-stu-id="be8e0-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Vista Utilizzo](media/FAQ-utilization-1.png)
 

<span data-ttu-id="be8e0-107">Il calcolo dell'utilizzo addebitabile viene eseguito in questo modo:</span><span class="sxs-lookup"><span data-stu-id="be8e0-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="be8e0-108">Utilizzo addebitabile = (ore effettive addebitabili)/(capacità della risorsa).</span><span class="sxs-lookup"><span data-stu-id="be8e0-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="be8e0-109">Le celle rappresentano l'utilizzo addebitabile calcolato per il periodo selezionato (giorni, settimane, o mesi).</span><span class="sxs-lookup"><span data-stu-id="be8e0-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="be8e0-110">I colori in ogni cella mostrano l'utilizzo addebitabile per una risorsa rispetto al relativo utilizzo addebitabile di destinazione.</span><span class="sxs-lookup"><span data-stu-id="be8e0-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="be8e0-111">L'utilizzo di destinazione può essere impostato nel ruolo predefinito della risorsa o nella singola risorsa stessa.</span><span class="sxs-lookup"><span data-stu-id="be8e0-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="be8e0-112">Il calcolo considera dapprima la persona per la destinazione e quindi il ruolo predefinito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="be8e0-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="be8e0-113">Impostare la destinazione in una risorsa</span><span class="sxs-lookup"><span data-stu-id="be8e0-113">Set target on a resource</span></span>

1. <span data-ttu-id="be8e0-114">Seleziona **Risorse** \> **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="be8e0-115">Selezionare una risorsa per aprire il record.</span><span class="sxs-lookup"><span data-stu-id="be8e0-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="be8e0-116">Nella scheda **Project Service**, è possibile impostare l'utilizzo di destinazione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="be8e0-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Utilizzo della scheda Project Service per impostare l'utilizzo di destinazione](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="be8e0-118">Impostare l'utilizzo di destinazione in un ruolo</span><span class="sxs-lookup"><span data-stu-id="be8e0-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="be8e0-119">Selezionare **Risorse** \> **Ruoli risorsa**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="be8e0-120">Selezionare un ruolo e aprire il record.</span><span class="sxs-lookup"><span data-stu-id="be8e0-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="be8e0-121">Impostare l'utilizzo di destinazione per il ruolo.</span><span class="sxs-lookup"><span data-stu-id="be8e0-121">Set the target utilization for the role.</span></span>

> ![Utilizzo di Ruoli risorsa per impostare l'utilizzo di destinazione](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="be8e0-123">Calcolare un utilizzo addebitabile per una risorsa</span><span class="sxs-lookup"><span data-stu-id="be8e0-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="be8e0-124">Per calcolare l'utilizzo addebitabile per una risorsa, è necessario completare alcuni prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="be8e0-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="be8e0-125">Impostare il ruolo predefinito per una singola risorsa</span><span class="sxs-lookup"><span data-stu-id="be8e0-125">Set default role for individual resource</span></span>

<span data-ttu-id="be8e0-126">Innanzi tutto, l'utilizzo di destinazione deve essere impostato sulla singola risorsa o sui ruoli risorsa.</span><span class="sxs-lookup"><span data-stu-id="be8e0-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="be8e0-127">Se si utilizzano i ruoli delle risorse per le destinazioni, ogni singola risorsa deve avere un ruolo predefinito.</span><span class="sxs-lookup"><span data-stu-id="be8e0-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="be8e0-128">A questo proposito, selezionare **Risorse** \> **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="be8e0-129">Selezionare una risorsa, aprire il record e quindi selezionare la scheda **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="be8e0-130">Nella griglia **Ruolo risorsa**, assicurarsi che è presente un ruolo per la risorsa e che **Predefinito** è impostato su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="be8e0-131">Modificare il tipo di fatturazione per il ruolo risorsa</span><span class="sxs-lookup"><span data-stu-id="be8e0-131">Change billing type for resource role</span></span>

<span data-ttu-id="be8e0-132">I ruoli risorsa devono essere impostati per avere un tipo di fatturazione **Addebitabile**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="be8e0-133">Selezionare **Risorse** \> **Ruoli risorsa**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="be8e0-134">Aprire il record che si intende aggiornare e quindi impostare il tipo di fatturazione predefinito su **Addebitabile**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="be8e0-135">Impostare le ore lavorative per il ruolo risorsa</span><span class="sxs-lookup"><span data-stu-id="be8e0-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="be8e0-136">La risorsa deve avere delle ore lavorative per il calcolo della capacità.</span><span class="sxs-lookup"><span data-stu-id="be8e0-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="be8e0-137">Seleziona **Risorse** \> **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="be8e0-138">Selezionare una risorsa per aprire il record, quindi selezionare **Mostra ore lavorative**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="be8e0-139">È possibile aggiornare in blocco l'elenco delle risorse applicando un **modello di ore lavorative** dalla vista **Elenco risorse**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="be8e0-140">Risoluzione dei problemi relativi alle ore effettive addebitabili</span><span class="sxs-lookup"><span data-stu-id="be8e0-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="be8e0-141">Le ore effettive addebitabili provengono dall'entità **Valori effettivi**.</span><span class="sxs-lookup"><span data-stu-id="be8e0-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="be8e0-142">I valori effettivi con un tipo di fatturazione **Addebitabile** sono inclusi nel calcolo e per questo motivo è necessario avere progetti dove i valori effettivi sono addebitabili.</span><span class="sxs-lookup"><span data-stu-id="be8e0-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="be8e0-143">Se non si sta visualizzando l'utilizzo addebitabile, di seguito sono elencati alcuni punti da verificare:</span><span class="sxs-lookup"><span data-stu-id="be8e0-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="be8e0-144">La risorsa ha ore lavorative definite per la capacità.</span><span class="sxs-lookup"><span data-stu-id="be8e0-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="be8e0-145">La risorsa ha una destinazione di utilizzo definita singolarmente o un ruolo predefinito.</span><span class="sxs-lookup"><span data-stu-id="be8e0-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="be8e0-146">Il ruolo ha una destinazione di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="be8e0-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="be8e0-147">I valori effettivi hanno un tipo di fatturazione **Addebitabile** per il periodo per cui si prevede un calcolo dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="be8e0-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="be8e0-148">Verificare quanto segue se sono visualizzati valori effettivi con tipi di fatturazione differenti da Addebitabile:</span><span class="sxs-lookup"><span data-stu-id="be8e0-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="be8e0-149">Il ruolo utilizzato per il valore effettivo ha un tipo di fatturazione predefinito differente da Addebitabile.</span><span class="sxs-lookup"><span data-stu-id="be8e0-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="be8e0-150">Il ruolo nella voce di contratto di progetto che supporta il progetto è stato impostato come non addebitabile.</span><span class="sxs-lookup"><span data-stu-id="be8e0-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="be8e0-151">Il progetto non ha una voce di contratto associata.</span><span class="sxs-lookup"><span data-stu-id="be8e0-151">The project does not have an associated contract line.</span></span>

