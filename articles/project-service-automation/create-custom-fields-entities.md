---
title: Creare campi ed entità personalizzati
description: In questo argomento viene illustrato come creare set di opzioni ed entità nella soluzione utilizzata sulla piattaforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752711"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="78287-103">Creare campi ed entità personalizzati</span><span class="sxs-lookup"><span data-stu-id="78287-103">Create custom fields and entities</span></span> 

<span data-ttu-id="78287-104">Completa i passaggi seguenti ogni volta che intendi creare un set di opzioni o un'entità personalizzato nella piattaforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="78287-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="78287-105">Le procedure illustrate in questo argomento devono essere completate tramite l'interfaccia Web di Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="78287-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78287-106">Ti consigliamo di apportare le modifiche alle dimensioni di determinazione dei prezzi personalizzate in una soluzione distinta.</span><span class="sxs-lookup"><span data-stu-id="78287-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="78287-107">Questo procedura consigliata importante fornisce flessibilità per aggiornamenti o rimozioni future delle modifiche, agevola il riutilizzo del lavoro e semplifica il trasferimento di tali modifiche a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="78287-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="78287-108">Dopo aver apportato tutte le modifiche necessarie, esporta questa soluzione come **Soluzione gestita** e importala in altre istanze per riutilizzare la configurazione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="78287-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="78287-109">Creare una soluzione personalizzata per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="78287-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="78287-110">In PSA fai clic su **Impostazioni** > ,**Soluzioni** e quindi su **Nuovo** per creare una nuova soluzione.</span><span class="sxs-lookup"><span data-stu-id="78287-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="78287-111">Assegna un nome alla soluzione, **dimensioni di determinazione dei prezzi di \<nome dell'organizzazione>**, immetti le informazioni richieste e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="78287-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Creare una soluzione personalizzata per le dimensioni di determinazione dei prezzi](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="78287-113">Creare campi e set di opzioni personalizzati nella soluzione per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="78287-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="78287-114">Una dimensione di determinazione dei prezzi può essere un set di opzioni o un'entità.</span><span class="sxs-lookup"><span data-stu-id="78287-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="78287-115">Entrambi devono essere creati nella soluzione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="78287-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="78287-116">I passaggi in questa procedura illustrano il modo in cui creare dimensioni basate su entità e dimensioni basate su set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="78287-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="78287-117">Dimensioni basata su entità</span><span class="sxs-lookup"><span data-stu-id="78287-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="78287-118">In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<nome dell'organizzazione>**.</span><span class="sxs-lookup"><span data-stu-id="78287-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="78287-119">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità**.</span><span class="sxs-lookup"><span data-stu-id="78287-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="78287-120">Fai clic su **Nuovo** per creare una nuova entità denominata **Titolo standard**.</span><span class="sxs-lookup"><span data-stu-id="78287-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="78287-121">Immetti le altre informazioni e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="78287-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definizione dell'entità Titolo standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="78287-123">Dimensioni basate su set di opzioni</span><span class="sxs-lookup"><span data-stu-id="78287-123">Option set-based dimensions</span></span> 
<span data-ttu-id="78287-124">Puoi creare due dimensioni basate su set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="78287-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="78287-125">Utilizza **Ubicazione lavoro risorsa** per tenere traccia del prezzo del lavoro nell'ubicazione **Abitazione** e del lavoro **In loco** e utilizza **Ore lavorative risorsa** con i valori **Normale** e **Straordinario** per applicare un ricarico quando il lavoro è ultimato.</span><span class="sxs-lookup"><span data-stu-id="78287-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="78287-126">In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<nome dell'organizzazione>**.</span><span class="sxs-lookup"><span data-stu-id="78287-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="78287-127">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Set di opzioni**.</span><span class="sxs-lookup"><span data-stu-id="78287-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="78287-128">Fai clic su **Nuovo** per creare un nuovo set di opzioni, immetti le altre informazioni richieste e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="78287-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="78287-129">Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ubicazione lavoro risorsa</span><span class="sxs-lookup"><span data-stu-id="78287-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="78287-130">Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ore lavorative risorsa</span><span class="sxs-lookup"><span data-stu-id="78287-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="78287-131">Creare dati per le dimensioni basate su entità</span><span class="sxs-lookup"><span data-stu-id="78287-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="78287-132">Puoi creare dati per le dimensioni basate su entità manualmente oppure utilizzando le chiamate di importazione o di servizio di Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="78287-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="78287-133">Utilizza i passaggi in questa procedura per creare due titoli standard, **Sistemista** e **Sistemista esperto**, a partire dalla dimensione basata su entità **Titolo standard**.</span><span class="sxs-lookup"><span data-stu-id="78287-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="78287-134">Se intendi creare pochi dati, come illustrato nel seguente esempio, puoi utilizzare un modulo standard.</span><span class="sxs-lookup"><span data-stu-id="78287-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="78287-135">In PSA fai clic su **Ricerca avanzata**.</span><span class="sxs-lookup"><span data-stu-id="78287-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="78287-136">Selezionar l'entità **Titolo standard**, quindi fai clic su **Risultati**.</span><span class="sxs-lookup"><span data-stu-id="78287-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="78287-137">Tutte le righe nell'entità **Titolo standard** verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="78287-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="78287-138">Fai clic su **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="78287-138">Click **New**.</span></span> <span data-ttu-id="78287-139">Nel campo **Nome** immetti "Sistemista" e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="78287-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="78287-140">Chiudere il modulo.</span><span class="sxs-lookup"><span data-stu-id="78287-140">Close the form.</span></span> 
4. <span data-ttu-id="78287-141">Ripeti i passaggi da 1 a 3 per creare un altro titolo standard, ovvero "Sistemista esperto".</span><span class="sxs-lookup"><span data-stu-id="78287-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="78287-142">Dati di esempio per l'entità Titolo standard</span><span class="sxs-lookup"><span data-stu-id="78287-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="78287-143">Aggiungere tutte le entità PSA necessarie e i componenti correlati alla soluzione per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="78287-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="78287-144">Devi aggiungere le seguenti entità di Project Service alla soluzione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="78287-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="78287-145">Utilizza i passaggi in questa procedura per apportare alcune importanti modifiche allo schema nella soluzione per la determinazione dei prezzi di modo che le entità siano consapevoli delle nuove dimensioni di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="78287-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="78287-146">In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<nome dell'organizzazione>**.</span><span class="sxs-lookup"><span data-stu-id="78287-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="78287-147">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Aggiungi record esistente** > **Entità**.</span><span class="sxs-lookup"><span data-stu-id="78287-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="78287-148">Nella finestra di dialogo **Componenti della soluzione**, seleziona le seguenti entità:</span><span class="sxs-lookup"><span data-stu-id="78287-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="78287-149">Valore effettivo</span><span class="sxs-lookup"><span data-stu-id="78287-149">Actual</span></span>
- <span data-ttu-id="78287-150">Risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="78287-150">Bookable Resource</span></span>
- <span data-ttu-id="78287-151">Riga di stima</span><span class="sxs-lookup"><span data-stu-id="78287-151">Estimate Line</span></span>
- <span data-ttu-id="78287-152">Dettagli di riga fattura</span><span class="sxs-lookup"><span data-stu-id="78287-152">Invoice Line Detail</span></span>
- <span data-ttu-id="78287-153">Riga giornale di registrazione</span><span class="sxs-lookup"><span data-stu-id="78287-153">Journal Line</span></span>
- <span data-ttu-id="78287-154">Dettagli di voce di contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="78287-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="78287-155">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="78287-155">Project Team Member</span></span>
- <span data-ttu-id="78287-156">Dettagli riga di offerta</span><span class="sxs-lookup"><span data-stu-id="78287-156">Quote Line Detail</span></span>
- <span data-ttu-id="78287-157">Ricarico prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="78287-157">Role Price Markup</span></span>
- <span data-ttu-id="78287-158">Prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="78287-158">Role Price</span></span> 
- <span data-ttu-id="78287-159">Inserimento ore</span><span class="sxs-lookup"><span data-stu-id="78287-159">Time Entry</span></span> 

> ![Aggiungere entità esistenti alla soluzione per le dimensioni di determinazione dei prezzi](media/Existing-entities-to-PD-solution.png)

> ![Selezionare componenti di soluzione](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="78287-162">Assicurati di includere tutti i moduli e tutte le viste per ogni entità selezionata.</span><span class="sxs-lookup"><span data-stu-id="78287-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="78287-163">Quando viene richiesto di includere le entità dipendenti per le entità selezionate sopra, fai clic su **No**.</span><span class="sxs-lookup"><span data-stu-id="78287-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Non includere i componenti correlati.](media/Do-not-include-required.png)


