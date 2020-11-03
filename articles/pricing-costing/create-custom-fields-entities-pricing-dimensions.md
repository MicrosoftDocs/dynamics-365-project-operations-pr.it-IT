---
title: Creare campi ed entità personalizzati come dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni su come creare entità o set di opzioni personalizzati.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078914"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="567be-103">Creare campi ed entità personalizzati come dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="567be-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="567be-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="567be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="567be-105">Completa i passaggi seguenti ogni volta che intendi creare un set di opzioni o un'entità personalizzato.</span><span class="sxs-lookup"><span data-stu-id="567be-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="567be-106">Ti consigliamo di apportare le modifiche alle dimensioni di determinazione dei prezzi personalizzate in una soluzione distinta.</span><span class="sxs-lookup"><span data-stu-id="567be-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="567be-107">Questo procedura consigliata importante fornisce flessibilità per aggiornamenti o rimozioni future delle modifiche, agevola il riutilizzo del lavoro e semplifica il trasferimento di tali modifiche a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="567be-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="567be-108">Dopo aver apportato tutte le modifiche necessarie, esporta questa soluzione come **Soluzione gestita** e importala in altre istanze per riutilizzare la configurazione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="567be-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="567be-109">Creare una soluzione personalizzata per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="567be-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="567be-110">Vai in **Impostazioni** > , **Soluzioni** e quindi seleziona **Nuovo** per creare una nuova soluzione.</span><span class="sxs-lookup"><span data-stu-id="567be-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="567be-111">Assegna un nome alla soluzione, **dimensioni di determinazione dei prezzi di \<your organization name>** , immetti le informazioni richieste e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="567be-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="567be-112">Creare campi e set di opzioni personalizzati nella soluzione per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="567be-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="567be-113">Una dimensione di determinazione dei prezzi può essere un set di opzioni o un'entità.</span><span class="sxs-lookup"><span data-stu-id="567be-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="567be-114">Entrambi devono essere creati nella soluzione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="567be-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="567be-115">I passaggi in questa procedura illustrano il modo in cui creare dimensioni basate su entità e dimensioni basate su set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="567be-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="567be-116">Dimensioni basata su entità</span><span class="sxs-lookup"><span data-stu-id="567be-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="567be-117">Vai a **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="567be-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="567be-118">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità**.</span><span class="sxs-lookup"><span data-stu-id="567be-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="567be-119">Seleziona **Nuovo** per creare una nuova entità denominata **Titolo standard**.</span><span class="sxs-lookup"><span data-stu-id="567be-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="567be-120">Immetti le altre informazioni e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="567be-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="567be-121">Dimensioni basate su set di opzioni</span><span class="sxs-lookup"><span data-stu-id="567be-121">Option set-based dimensions</span></span> 
<span data-ttu-id="567be-122">Puoi creare due dimensioni basate su set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="567be-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="567be-123">Utilizza **Ubicazione lavoro risorsa** per tenere traccia del prezzo del lavoro nell'ubicazione **Abitazione** e del lavoro **In loco** e utilizza **Ore lavorative risorsa** con i valori **Normale** e **Straordinario** per applicare un ricarico quando il lavoro è ultimato.</span><span class="sxs-lookup"><span data-stu-id="567be-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="567be-124">Vai a **Impostazioni** > **Soluzioni** e fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="567be-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="567be-125">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Set di opzioni**.</span><span class="sxs-lookup"><span data-stu-id="567be-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="567be-126">Seleziona **Nuovo** per creare un nuovo set di opzioni, immetti le altre informazioni richieste e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="567be-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="567be-127">Creare dati per le dimensioni basate su entità</span><span class="sxs-lookup"><span data-stu-id="567be-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="567be-128">Puoi creare dati per le dimensioni basate su entità manualmente oppure utilizzando le chiamate di importazione o di servizio di Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="567be-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="567be-129">Utilizza i passaggi in questa procedura per creare due titoli standard, **Sistemista** e **Sistemista esperto** , a partire dalla dimensione basata su entità **Titolo standard**.</span><span class="sxs-lookup"><span data-stu-id="567be-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="567be-130">Se intendi creare pochi dati, come illustrato nel seguente esempio, puoi utilizzare un modulo standard.</span><span class="sxs-lookup"><span data-stu-id="567be-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="567be-131">Seleziona **Ricerca avanzata** , seleziona l'entità **Titolo standard** e quindi seleziona **Risultati**.</span><span class="sxs-lookup"><span data-stu-id="567be-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="567be-132">Tutte le righe nell'entità **Titolo standard** verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="567be-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="567be-133">Seleziona **Nuovo** e nel campo **Nome** immetti "Systems Engineer" e seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="567be-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="567be-134">Chiudi il modulo.</span><span class="sxs-lookup"><span data-stu-id="567be-134">Close the form.</span></span> 
4. <span data-ttu-id="567be-135">Ripeti i passaggi da 1 a 3 per creare un altro titolo standard, ovvero "Sistemista esperto".</span><span class="sxs-lookup"><span data-stu-id="567be-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="567be-136">Aggiungere tutte le entità necessarie e i componenti correlati alla soluzione per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="567be-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="567be-137">Devi aggiungere le seguenti entità alla soluzione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="567be-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="567be-138">Utilizza i passaggi in questa procedura per apportare alcune importanti modifiche allo schema nella soluzione per la determinazione dei prezzi di modo che le entità siano consapevoli delle nuove dimensioni di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="567be-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="567be-139">Seleziona **Impostazioni** > **Soluzioni** e fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="567be-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="567be-140">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Aggiungi record esistente** > **Entità**.</span><span class="sxs-lookup"><span data-stu-id="567be-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="567be-141">Nella finestra di dialogo **Componenti della soluzione** , seleziona le seguenti entità:</span><span class="sxs-lookup"><span data-stu-id="567be-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="567be-142">Valore effettivo</span><span class="sxs-lookup"><span data-stu-id="567be-142">Actual</span></span>
  - <span data-ttu-id="567be-143">Risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="567be-143">Bookable Resource</span></span>
  - <span data-ttu-id="567be-144">Riga di stima</span><span class="sxs-lookup"><span data-stu-id="567be-144">Estimate Line</span></span>
  - <span data-ttu-id="567be-145">Dettagli di riga fattura</span><span class="sxs-lookup"><span data-stu-id="567be-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="567be-146">Riga giornale di registrazione</span><span class="sxs-lookup"><span data-stu-id="567be-146">Journal Line</span></span>
  - <span data-ttu-id="567be-147">Dettagli di voce di contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="567be-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="567be-148">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="567be-148">Project Team Member</span></span>
  - <span data-ttu-id="567be-149">Dettagli riga di offerta</span><span class="sxs-lookup"><span data-stu-id="567be-149">Quote Line Detail</span></span>
  - <span data-ttu-id="567be-150">Ricarico prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="567be-150">Role Price Markup</span></span>
  - <span data-ttu-id="567be-151">Prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="567be-151">Role Price</span></span> 
  - <span data-ttu-id="567be-152">Inserimento ore</span><span class="sxs-lookup"><span data-stu-id="567be-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="567be-153">Assicurati di includere tutti i moduli e tutte le viste per ogni entità selezionata.</span><span class="sxs-lookup"><span data-stu-id="567be-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="567be-154">Quando viene richiesto di includere le entità dipendenti per le entità selezionate sopra, seleziona **No**.</span><span class="sxs-lookup"><span data-stu-id="567be-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

