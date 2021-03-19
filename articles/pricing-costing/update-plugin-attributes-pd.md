---
title: Aggiornamento degli attributi dei plug-in con nuove dimensioni di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni su come aggiornare gli attributi di plug-in per le dimensioni di determinazione dei prezzi.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274688"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="9e3d8-103">Aggiornare gli attributi dei plug-in con nuove dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="9e3d8-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="9e3d8-104">In questo argomento vengono fornite informazioni su come aggiornare gli attributi di plug-in per le dimensioni di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="9e3d8-105">Questo argomento è applicabile solo alle funzionalità di preventivo e contratto in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9e3d8-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9e3d8-106">Prerequisites</span></span>
<span data-ttu-id="9e3d8-107">Prima di completare i passaggi in questo argomento, è necessario aver completato le procedure nei seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="9e3d8-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="9e3d8-108">Creazione di campi ed entità personalizzati</span><span class="sxs-lookup"><span data-stu-id="9e3d8-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="9e3d8-109">Aggiungere campi personalizzati all'impostazione e alle entità transazionali </span><span class="sxs-lookup"><span data-stu-id="9e3d8-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="9e3d8-110">[Configurare campi personalizzati come dimensioni di determinazione dei prezzi](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="9e3d8-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="9e3d8-111">Se non hai completato queste procedure, completale prima di leggere questo argomento.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="9e3d8-112">Registrare un plug-in</span><span class="sxs-lookup"><span data-stu-id="9e3d8-112">Register a plug-in</span></span>
<span data-ttu-id="9e3d8-113">Quando un dettaglio di una riga di preventivo viene creato nella pagina **Riga di offerta** per una riga di preventivo di progetto, il sistema crea due righe di preventivo.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="9e3d8-114">Una riga è per i costi della stima e l'altra è per le vendite.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="9e3d8-115">Questo è ciò che avviene anche per le voci di contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="9e3d8-116">Quando modifichi la quantità o un campo nel lato costo, quella modifica viene propagata al lato vendite.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="9e3d8-117">Ciò è possibile perché i plug-in PreOperation su Quotelinedetail e le entità di dettaglio della linea di contratto collegano attributi specifici dal lato dei costi al lato delle vendite della transazione.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="9e3d8-118">Se è necessario che le modifiche apportate ai valori della dimensione del prezzo sul lato delle vendite vengano apportate anche sul lato del costo, i seguenti plug-in devono essere registrati nuovamente dopo aver apportato le modifiche a una dimensione del prezzo.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="9e3d8-119">Questi sono i plug-in per aggiornare e registrare nuovamente:</span><span class="sxs-lookup"><span data-stu-id="9e3d8-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="9e3d8-120">PreOperationContractLineDetailUpdate: **Aggiorna msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="9e3d8-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="9e3d8-121">PreOperationQuoteLineDetailUpdate: **Aggiorna msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="9e3d8-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="9e3d8-122">Completare i seguenti passaggi per aggiornare e registrare nuovamente i plug-in.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="9e3d8-123">Apri **PluginRegistrationTool** e connettiti al tuo ambiente Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="9e3d8-124">Seleziona **Ricerca** e digita le prime lettere del plug-in da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="9e3d8-125">Una volta trovato il plug-in, selezionalo e fai clic su **Seleziona nel modulo principale**.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="9e3d8-126">Seleziona il passaggio **Aggiorna msdyn_orderlinetransaction**, fai clic con il pulsante destro del mouse e quindi scegli **Aggiorna**.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="9e3d8-127">Nella finestra di dialogo **Aggiorna**, fai clic sui puntini di sospensione (**...**) negli attributi di filtro.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="9e3d8-128">La finestra degli attributi di filtro viene aperta; fornisce un elenco di tutti gli attributi nell'entità e le dimensioni di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="9e3d8-129">Seleziona le caselle di controllo per gli attributi di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="9e3d8-130">Seleziona **OK** per chiudere la pagina, quindi seleziona **Aggiorna passaggio**.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="9e3d8-131">Ripeti i passaggi da 2 a 7 per il secondo plug-in, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="9e3d8-132">Per questo plug-in, devi aggiornare il passaggio **Aggiorna of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="9e3d8-133">Chiudi **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]