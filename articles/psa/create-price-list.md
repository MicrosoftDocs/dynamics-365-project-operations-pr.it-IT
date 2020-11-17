---
title: Creare un listino prezzi
description: Come creare un listino prezzi in Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 08d93ad86d782922df6b22370749628ddbdc0718
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122033"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="6c666-103">Creare un listino prezzi (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6c666-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6c666-104">I listini prezzi offrono un modello che gli Account Manager possono utilizzare per la creazione di offerte e di progetti e per stabilire i costi di un progetto.</span><span class="sxs-lookup"><span data-stu-id="6c666-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="6c666-105">Questi offrono un elenco di voci dei ruoli e delle spese e il prezzo che verrà addebitato a ognuno.</span><span class="sxs-lookup"><span data-stu-id="6c666-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="6c666-106">È possibile creare più listini prezzi in modo da gestire strutture di prezzi diverse per diverse aree geografiche di vendita dei prodotti o per diversi canali di vendita.</span><span class="sxs-lookup"><span data-stu-id="6c666-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="6c666-107">È una buona idea creare almeno un listino prezzi per ogni valuta in cui si desidera fatturare ai clienti.</span><span class="sxs-lookup"><span data-stu-id="6c666-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="6c666-108">Per creare stime finanziarie per il lavoro da fornire, controlla che ogni progetto abbia un costo e un listino prezzi di vendita.</span><span class="sxs-lookup"><span data-stu-id="6c666-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="6c666-109">Impostare un costo predefinito e un listino prezzi di vendita valido per tutti i progetti creati nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="6c666-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="6c666-110">I listini prezzi si basano sui ruoli e le categorie di spesa, pertanto prima di creare un listino prezzi, verifica di aver già configurato i ruoli e le categorie di spesa che desideri utilizzare mentre si crea il listino prezzi.</span><span class="sxs-lookup"><span data-stu-id="6c666-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="6c666-111">Passa a **Project Service > Listini prezzi**.</span><span class="sxs-lookup"><span data-stu-id="6c666-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="6c666-112">Fare clic su **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="6c666-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="6c666-113">In **Contesto**, seleziona se questo listino prezzi è per **Costo**, **Acquisto** o **Vendite**.</span><span class="sxs-lookup"><span data-stu-id="6c666-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="6c666-114">In **Nome**, inserisci un nome per il listino prezzi.</span><span class="sxs-lookup"><span data-stu-id="6c666-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="6c666-115">In **Valuta**, seleziona la valuta che desideri utilizzare per la fatturazione o la determinazione dei costi.</span><span class="sxs-lookup"><span data-stu-id="6c666-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="6c666-116">In **Unità di tempo**, specifica il periodo di tempo a cui fa riferimento il prezzo, ad esempio giorno oppure ora.</span><span class="sxs-lookup"><span data-stu-id="6c666-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="6c666-117">Compila **Data di inizio**, **Data di fine** e **Descrizione** in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6c666-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="6c666-118">Fai clic su **Salva** per creare il record in modo da poter continuare a modificarlo.</span><span class="sxs-lookup"><span data-stu-id="6c666-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="6c666-119">Per aggiungere un prezzo del ruolo al listino prezzi, fai clic su **+** in **Prezzi ruolo**.</span><span class="sxs-lookup"><span data-stu-id="6c666-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="6c666-120">Nel riquadro **Prezzi ruolo**, compila i dettagli e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="6c666-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="6c666-121">Continua ad aggiungere i prezzi dei ruoli in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6c666-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="6c666-122">Una volta completato, fai clic su **Salva** nell'angolo in basso a destra dello schermo.</span><span class="sxs-lookup"><span data-stu-id="6c666-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="6c666-123">Per aggiungere un prezzo della categoria spesa, fai clic su **+** in **Prezzi categoria**.</span><span class="sxs-lookup"><span data-stu-id="6c666-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="6c666-124">Nel riquadro **Prezzo categoria di transazione**, compila i dettagli e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="6c666-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="6c666-125">Continua ad aggiungere i prezzi dei ruoli in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6c666-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="6c666-126">Una volta completato, fai clic su **Salva** nell'angolo in basso a destra dello schermo.</span><span class="sxs-lookup"><span data-stu-id="6c666-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="6c666-127">Per aggiungere le voci di listino prezzi al listino prezzi, fai clic su **+** in **Voci di listino**.</span><span class="sxs-lookup"><span data-stu-id="6c666-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="6c666-128">Nel riquadro **Voce di listino**, compila i dettagli e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="6c666-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="6c666-129">Continua ad aggiungere le voci listino in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6c666-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="6c666-130">Una volta completato, fai clic su **Salva** nell'angolo in basso a destra dello schermo.</span><span class="sxs-lookup"><span data-stu-id="6c666-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="6c666-131">Per aggiungere relazioni area al listino prezzi, fai clic su **+** in **Relazioni area**.</span><span class="sxs-lookup"><span data-stu-id="6c666-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="6c666-132">Nel riquadro **Nuova connessione**, compila i dettagli e quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="6c666-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="6c666-133">Continua ad aggiungere le relazioni area a seconda delle esigenze.</span><span class="sxs-lookup"><span data-stu-id="6c666-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="6c666-134">Una volta completato, fai clic su **Salva** nell'angolo in basso a destra dello schermo.</span><span class="sxs-lookup"><span data-stu-id="6c666-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6c666-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c666-135">See Also</span></span>  
 [<span data-ttu-id="6c666-136">Configurare Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6c666-136">Configure Project Service Automation</span></span>](../psa/configure.md)
