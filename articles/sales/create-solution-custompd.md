---
title: Creare una soluzione per le dimensioni di determinazione dei prezzi personalizzate
description: In questo argomento vengono fornite informazioni sulla creazione di soluzioni per dimensioni di determinazione dei prezzi.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513995"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="78dc1-103">Creare una soluzione per le dimensioni di determinazione dei prezzi personalizzate</span><span class="sxs-lookup"><span data-stu-id="78dc1-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="78dc1-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="78dc1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="78dc1-105">Tutte le modifiche alle dimensioni di determinazione dei prezzi personalizzate devono essere contenute in una soluzione separata.</span><span class="sxs-lookup"><span data-stu-id="78dc1-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="78dc1-106">Questa procedura consigliata importante fornisce flessibilità per aggiornare o rimuovere modifiche come necessario, agevola il riutilizzo del lavoro e semplifica il trasferimento di tali modifiche ad altre istanze.</span><span class="sxs-lookup"><span data-stu-id="78dc1-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="78dc1-107">Dopo aver apportato tutte le modifiche necessarie, esporta questa soluzione come soluzione **Gestita** e importala in altre istanze per riutilizzarla.</span><span class="sxs-lookup"><span data-stu-id="78dc1-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="78dc1-108">Creare una soluzione per le dimensioni di determinazione dei prezzi personalizzate</span><span class="sxs-lookup"><span data-stu-id="78dc1-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="78dc1-109">Seleziona **Impostazioni** > **Soluzioni** e quindi seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="78dc1-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="78dc1-110">Assegna un nome alla soluzione, *dimensioni dei prezzi di <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="78dc1-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="78dc1-111">Immetti le altre informazioni e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="78dc1-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Creazione di una soluzione di determinazione dei prezzi personalizzata](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="78dc1-113">Aggiungere tutte le entità necessarie e i componenti correlati alla soluzione per le dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="78dc1-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="78dc1-114">Aggiungi le seguenti entità di Project Service alla tua soluzione tariffaria per apportare importanti modifiche allo schema nella soluzione tariffaria.</span><span class="sxs-lookup"><span data-stu-id="78dc1-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="78dc1-115">Dopo aver completato questa procedura, le entità riconosceranno le nuove dimensioni di prezzo.</span><span class="sxs-lookup"><span data-stu-id="78dc1-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="78dc1-116">Seleziona **Impostazioni** > **Soluzioni**, quindi fai doppio clic su **<*nome dell'organizzazione*> dimensioni di determinazione dei prezzi**.</span><span class="sxs-lookup"><span data-stu-id="78dc1-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="78dc1-117">In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Aggiungi record esistente** > **Entità**.</span><span class="sxs-lookup"><span data-stu-id="78dc1-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="78dc1-118">Nella finestra di dialogo **Componenti della soluzione**, seleziona le seguenti entità:</span><span class="sxs-lookup"><span data-stu-id="78dc1-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="78dc1-119">**Effettiva**</span><span class="sxs-lookup"><span data-stu-id="78dc1-119">**Actual**</span></span>
   - <span data-ttu-id="78dc1-120">**Risorsa prenotabile**</span><span class="sxs-lookup"><span data-stu-id="78dc1-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="78dc1-121">**Riga di stima**</span><span class="sxs-lookup"><span data-stu-id="78dc1-121">**Estimate Line**</span></span>
   - <span data-ttu-id="78dc1-122">**Attività di progetto**</span><span class="sxs-lookup"><span data-stu-id="78dc1-122">**Project Task**</span></span>
   - <span data-ttu-id="78dc1-123">**Dettagli di riga fattura**</span><span class="sxs-lookup"><span data-stu-id="78dc1-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="78dc1-124">**Riga giornale di registrazione**</span><span class="sxs-lookup"><span data-stu-id="78dc1-124">**Journal Line**</span></span>
   - <span data-ttu-id="78dc1-125">**Dettagli di voce di contratto di progetto**</span><span class="sxs-lookup"><span data-stu-id="78dc1-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="78dc1-126">**Membro del team di progetto**</span><span class="sxs-lookup"><span data-stu-id="78dc1-126">**Project Team Member**</span></span>
   - <span data-ttu-id="78dc1-127">**Dettagli riga di offerta**</span><span class="sxs-lookup"><span data-stu-id="78dc1-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="78dc1-128">**Ricarico prezzo ruolo**</span><span class="sxs-lookup"><span data-stu-id="78dc1-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="78dc1-129">**Prezzo ruolo**</span><span class="sxs-lookup"><span data-stu-id="78dc1-129">**Role Price**</span></span>
   - <span data-ttu-id="78dc1-130">**Inserimento ore**</span><span class="sxs-lookup"><span data-stu-id="78dc1-130">**Time Entry**</span></span>
 
   ![Aggiungi entità esistenti alla soluzione per le dimensioni di determinazione dei prezzi](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="78dc1-132">Per ciascuna entità, rivedere i componenti aggiunti e l'elenco finale delle risorse dell'entità per ciascuna entità.</span><span class="sxs-lookup"><span data-stu-id="78dc1-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="78dc1-133">Include tutti i moduli e tutte le viste per ogni entità selezionata.</span><span class="sxs-lookup"><span data-stu-id="78dc1-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entità aggiunta](./media/solution-component-selection.png)


5.  <span data-ttu-id="78dc1-135">Quando viene richiesto di includere eventuali entità dipendenti per le entità selezionate, seleziona **No, non includere i componenti richiesti.**</span><span class="sxs-lookup"><span data-stu-id="78dc1-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Comprese le entità dipendenti](./media/Do-not-include-required.png)
