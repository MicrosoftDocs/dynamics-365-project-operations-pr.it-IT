---
title: Creare soluzioni personalizzate per le dimensioni di determinazione dei prezzi
description: Questo argomento spiega come creare una soluzione personalizzata quando si creano dimensioni di determinazione dei prezzi personalizzate.
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
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144644"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="c690a-103">Creare soluzioni personalizzate per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="c690a-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="c690a-104">Tutte le modifiche alle dimensioni di determinazione dei prezzi personalizzate devono essere contenute in una soluzione separata.</span><span class="sxs-lookup"><span data-stu-id="c690a-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="c690a-105">Questo procedura consigliata importante fornisce flessibilità per aggiornamenti o rimozioni future delle modifiche, agevola il riutilizzo del lavoro e semplifica il trasferimento di tali modifiche a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="c690a-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c690a-106">Dopo aver apportato tutte le modifiche necessarie, esporta la soluzione come **Soluzione gestita** e importala in altre istanze per riutilizzare la configurazione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="c690a-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="c690a-107">Seleziona **Impostazioni** > **Soluzioni** e quindi seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="c690a-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="c690a-108">Assegna un nome alla soluzione, **dimensioni di determinazione dei prezzi di \<your organization name>**, immetti le informazioni richieste e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="c690a-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Creare una soluzione personalizzata per le dimensioni di determinazione dei prezzi](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="c690a-110">Aggiungere tutte le entità necessarie e i componenti correlati alla soluzione per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="c690a-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="c690a-111">Devi aggiungere le seguenti entità di Project Service alla soluzione per la determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="c690a-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="c690a-112">Completa i passaggi in questa procedura per apportare alcune importanti modifiche allo schema nella soluzione per la determinazione dei prezzi di modo che le entità siano consapevoli delle nuove dimensioni di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="c690a-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="c690a-113">Seleziona **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="c690a-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c690a-114">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Aggiungi record esistente** > **Entità**.</span><span class="sxs-lookup"><span data-stu-id="c690a-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="c690a-115">Nella finestra di dialogo **Componenti della soluzione**, seleziona le seguenti entità:</span><span class="sxs-lookup"><span data-stu-id="c690a-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="c690a-116">Effettiva</span><span class="sxs-lookup"><span data-stu-id="c690a-116">Actual</span></span>
- <span data-ttu-id="c690a-117">Risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="c690a-117">Bookable Resource</span></span>
- <span data-ttu-id="c690a-118">Riga di stima</span><span class="sxs-lookup"><span data-stu-id="c690a-118">Estimate Line</span></span>
- <span data-ttu-id="c690a-119">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="c690a-119">Project Task</span></span>
- <span data-ttu-id="c690a-120">Dettagli di riga fattura</span><span class="sxs-lookup"><span data-stu-id="c690a-120">Invoice Line Detail</span></span>
- <span data-ttu-id="c690a-121">Riga giornale di registrazione</span><span class="sxs-lookup"><span data-stu-id="c690a-121">Journal Line</span></span>
- <span data-ttu-id="c690a-122">Dettagli di voce di contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="c690a-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="c690a-123">Membro del team di progetto</span><span class="sxs-lookup"><span data-stu-id="c690a-123">Project Team Member</span></span>
- <span data-ttu-id="c690a-124">Dettagli riga di offerta</span><span class="sxs-lookup"><span data-stu-id="c690a-124">Quote Line Detail</span></span>
- <span data-ttu-id="c690a-125">Ricarico prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="c690a-125">Role Price Markup</span></span>
- <span data-ttu-id="c690a-126">Prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="c690a-126">Role Price</span></span> 
- <span data-ttu-id="c690a-127">Inserimento ore</span><span class="sxs-lookup"><span data-stu-id="c690a-127">Time Entry</span></span> 

> ![Aggiungere entità esistenti alla soluzione per le dimensioni di determinazione dei prezzi](media/Existing-entities-to-PD-solution.png)

> ![Selezionare componenti di soluzione](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="c690a-130">Assicurati di includere tutti i moduli e tutte le viste per ogni entità selezionata.</span><span class="sxs-lookup"><span data-stu-id="c690a-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="c690a-131">Quando viene richiesto di includere le entità dipendenti per le entità selezionate, seleziona **No**.</span><span class="sxs-lookup"><span data-stu-id="c690a-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Non includere i componenti correlati.](media/Do-not-include-required.png)


