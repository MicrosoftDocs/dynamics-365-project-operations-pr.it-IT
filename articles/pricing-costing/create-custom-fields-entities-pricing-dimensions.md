---
title: Creare campi ed entità personalizzati come dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni su come creare entità o set di opzioni personalizzati.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642818"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="4042c-103">Creare campi ed entità personalizzati come dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="4042c-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="4042c-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="4042c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4042c-105">Completa i passaggi seguenti quando intendi creare un set di opzioni o un'entità per usarla come dimensione di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="4042c-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="4042c-106">Per ulteriori informazioni, vedi [Panoramica delle dimensioni di determinazione dei prezzi](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4042c-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="4042c-107">Ti consigliamo di apportare le modifiche alle dimensioni di determinazione dei prezzi personalizzate in una soluzione distinta.</span><span class="sxs-lookup"><span data-stu-id="4042c-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="4042c-108">Questa importante best practice offre flessibilità in futuro per aggiornare o rimuovere le modifiche secondo necessità.</span><span class="sxs-lookup"><span data-stu-id="4042c-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="4042c-109">Ciò aiuterà anche il riutilizzo del tuo lavoro e renderà più facile trasferire queste modifiche su un'altra istanza. Dopo aver apportato tutte le modifiche richieste, esporta questa soluzione come **Soluzione gestita** e importala in altre istanze per riutilizzare la configurazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="4042c-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="4042c-110">Creare campi e set di opzioni personalizzati nella soluzione per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="4042c-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="4042c-111">Una dimensione di determinazione dei prezzi può essere un set di opzioni o un'entità.</span><span class="sxs-lookup"><span data-stu-id="4042c-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="4042c-112">Entrambi devono essere creati nella soluzione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="4042c-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="4042c-113">I passaggi in questa procedura illustrano il modo in cui creare dimensioni basate su entità e dimensioni basate su set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="4042c-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="4042c-114">Dimensioni basata su entità</span><span class="sxs-lookup"><span data-stu-id="4042c-114">Entity-based dimensions</span></span>
<span data-ttu-id="4042c-115">Per creare dimensioni basate su entità, segui questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="4042c-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="4042c-116">Vai a **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="4042c-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="4042c-117">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità**.</span><span class="sxs-lookup"><span data-stu-id="4042c-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="4042c-118">Seleziona **Nuovo** per creare una nuova entità denominata **Titolo standard**.</span><span class="sxs-lookup"><span data-stu-id="4042c-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="4042c-119">Immetti le altre informazioni e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4042c-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definizione dell'entità Titolo standard](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="4042c-121">Dimensioni basate su set di opzioni</span><span class="sxs-lookup"><span data-stu-id="4042c-121">Option set-based dimensions</span></span> 
<span data-ttu-id="4042c-122">Puoi creare due dimensioni basate su set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="4042c-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="4042c-123">Utilizzare **Ubicazione lavoro risorsa** per monitorare il prezzo della posizione del lavoro presso **Casa** o **In loco**.</span><span class="sxs-lookup"><span data-stu-id="4042c-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="4042c-124">Utilizzare **Ore lavorative della risorsa** con valori **Regolare** e **Straordinario** per applicare un markup quando il lavoro è completo.</span><span class="sxs-lookup"><span data-stu-id="4042c-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="4042c-125">Il grafico seguente fornisce una visualizzazione della dimensione **Ubicazione lavoro risorsa**.</span><span class="sxs-lookup"><span data-stu-id="4042c-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ubicazione lavoro risorsa](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="4042c-127">Il grafico seguente fornisce una visualizzazione della dimensione **Ore lavoro risorsa**.</span><span class="sxs-lookup"><span data-stu-id="4042c-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ore lavorative risorsa](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="4042c-129">Vai a **Impostazioni** > **Soluzioni** e fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="4042c-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="4042c-130">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Set di opzioni**.</span><span class="sxs-lookup"><span data-stu-id="4042c-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="4042c-131">Seleziona **Nuovo** per creare un nuovo set di opzioni, immetti le altre informazioni richieste e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4042c-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="4042c-132">Creare dati per le dimensioni basate su entità</span><span class="sxs-lookup"><span data-stu-id="4042c-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="4042c-133">Puoi creare dati per le dimensioni basate su entità manualmente oppure utilizzando le chiamate di importazione o di servizio di Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4042c-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="4042c-134">Utilizza i passaggi in questa procedura per creare due titoli standard, **Sistemista** e **Sistemista esperto**, a partire dalla dimensione basata su entità **Titolo standard**.</span><span class="sxs-lookup"><span data-stu-id="4042c-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="4042c-135">Se intendi creare pochi dati, come illustrato nel seguente esempio, puoi utilizzare un modulo standard.</span><span class="sxs-lookup"><span data-stu-id="4042c-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="4042c-136">Selezionare **Ricerca avanzata**.</span><span class="sxs-lookup"><span data-stu-id="4042c-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="4042c-137">Seleziona l'entità **Titolo standard**, quindi seleziona **Risultati**.</span><span class="sxs-lookup"><span data-stu-id="4042c-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="4042c-138">Tutte le righe nell'entità **Titolo standard** verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="4042c-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="4042c-139">Seleziona **Nuovo** e nel campo **Nome** immetti "Systems Engineer" e seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4042c-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="4042c-140">Chiudi la pagina.</span><span class="sxs-lookup"><span data-stu-id="4042c-140">Close the page.</span></span> 
5. <span data-ttu-id="4042c-141">Ripeti i passaggi da 1 a 3 per creare un altro titolo standard, ovvero "Sistemista esperto".</span><span class="sxs-lookup"><span data-stu-id="4042c-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Dati di esempio per l'entità Titolo standard](media/ST-data.png)
