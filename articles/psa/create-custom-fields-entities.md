---
title: Creare campi ed entità personalizzati
description: In questo argomento viene illustrato come creare set di opzioni ed entità nella soluzione utilizzata sulla piattaforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290541"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="3c3c0-103">Creare campi ed entità personalizzati</span><span class="sxs-lookup"><span data-stu-id="3c3c0-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3c3c0-104">Completa i passaggi seguenti ogni volta che intendi creare un set di opzioni o un'entità personalizzato nella piattaforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="3c3c0-105">Le procedure illustrate in questo argomento devono essere completate tramite l'interfaccia Web di Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="3c3c0-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c3c0-106">Ti consigliamo di apportare le modifiche alle dimensioni di determinazione dei prezzi personalizzate in una soluzione distinta.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="3c3c0-107">Questo procedura consigliata importante fornisce flessibilità per aggiornamenti o rimozioni future delle modifiche, agevola il riutilizzo del lavoro e semplifica il trasferimento di tali modifiche a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="3c3c0-108">Dopo aver apportato tutte le modifiche necessarie, esporta questa soluzione come **Soluzione gestita** e importala in altre istanze per riutilizzare la configurazione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="3c3c0-109">Creare campi e set di opzioni personalizzati nella soluzione per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="3c3c0-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="3c3c0-110">Una dimensione di determinazione dei prezzi può essere un set di opzioni o un'entità.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="3c3c0-111">Entrambi devono essere creati nella soluzione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="3c3c0-112">I passaggi in questa procedura illustrano il modo in cui creare dimensioni basate su entità e dimensioni basate su set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="3c3c0-113">Dimensioni basata su entità</span><span class="sxs-lookup"><span data-stu-id="3c3c0-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="3c3c0-114">In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="3c3c0-115">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="3c3c0-116">Fai clic su **Nuovo** per creare una nuova entità denominata **Titolo standard**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="3c3c0-117">Immetti le altre informazioni e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definizione dell'entità Titolo standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="3c3c0-119">Dimensioni basate su set di opzioni</span><span class="sxs-lookup"><span data-stu-id="3c3c0-119">Option set-based dimensions</span></span> 
<span data-ttu-id="3c3c0-120">Puoi creare due dimensioni basate su set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="3c3c0-121">Utilizza **Ubicazione lavoro risorsa** per tenere traccia del prezzo del lavoro nell'ubicazione **Abitazione** e del lavoro **In loco** e utilizza **Ore lavorative risorsa** con i valori **Normale** e **Straordinario** per applicare un ricarico quando il lavoro è ultimato.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="3c3c0-122">In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="3c3c0-123">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Set di opzioni**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="3c3c0-124">Fai clic su **Nuovo** per creare un nuovo set di opzioni, immetti le altre informazioni richieste e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="3c3c0-125">Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ubicazione lavoro risorsa</span><span class="sxs-lookup"><span data-stu-id="3c3c0-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="3c3c0-126">Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ore lavorative risorsa</span><span class="sxs-lookup"><span data-stu-id="3c3c0-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="3c3c0-127">Creare dati per le dimensioni basate su entità</span><span class="sxs-lookup"><span data-stu-id="3c3c0-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="3c3c0-128">Puoi creare dati per le dimensioni basate su entità manualmente oppure utilizzando le chiamate di importazione o di servizio di Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="3c3c0-129">Utilizza i passaggi in questa procedura per creare due titoli standard, **Sistemista** e **Sistemista esperto**, a partire dalla dimensione basata su entità **Titolo standard**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="3c3c0-130">Se intendi creare pochi dati, come illustrato nel seguente esempio, puoi utilizzare un modulo standard.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="3c3c0-131">In PSA fai clic su **Ricerca avanzata**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="3c3c0-132">Selezionar l'entità **Titolo standard**, quindi fai clic su **Risultati**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="3c3c0-133">Tutte le righe nell'entità **Titolo standard** verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="3c3c0-134">Fai clic su **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-134">Click **New**.</span></span> <span data-ttu-id="3c3c0-135">Nel campo **Nome** immetti "Sistemista" e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="3c3c0-136">Chiudere il modulo.</span><span class="sxs-lookup"><span data-stu-id="3c3c0-136">Close the form.</span></span> 
4. <span data-ttu-id="3c3c0-137">Ripeti i passaggi da 1 a 3 per creare un altro titolo standard, ovvero "Sistemista esperto".</span><span class="sxs-lookup"><span data-stu-id="3c3c0-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="3c3c0-138">Dati di esempio per l'entità Titolo standard</span><span class="sxs-lookup"><span data-stu-id="3c3c0-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]