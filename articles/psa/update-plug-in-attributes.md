---
title: Aggiornare attributi di plug-in per includere nuove dimensioni di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni sull'aggiornamento degli attributi di plug-in per le dimensioni di determinazione dei prezzi.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b0d50733340f277453f4ef5b52bdd3ee089449cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012816"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="25c4f-103">Aggiornare attributi di plug-in per includere nuove dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="25c4f-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="25c4f-104">Se non utilizzi le funzionalità Offerte e Contratti di Project Service Automation (PSA) puoi ignorare questo argomento.</span><span class="sxs-lookup"><span data-stu-id="25c4f-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="25c4f-105">Questo argomento presuppone che tu abbia completato le procedure negli argomenti [Creare campi ed entità personalizzati](create-custom-fields-entities.md), [Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali](field-references.md) e [Impostare campi personalizzati come dimensioni di determinazione dei prezzi](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="25c4f-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="25c4f-106">Se non hai completato queste procedure, completale prima di leggere questo argomento.</span><span class="sxs-lookup"><span data-stu-id="25c4f-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="25c4f-107">Quando si creano i dettagli di una riga di offerta nella pagina **Riga di offerta** per una riga di offerta di progetto, il sistema crea due righe di stima in background: una riga per il lato costo della stima e una per il lato vendite.</span><span class="sxs-lookup"><span data-stu-id="25c4f-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="25c4f-108">Questo è ciò che avviene anche per le voci di contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="25c4f-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="25c4f-109">Quando modifichi la quantità o un campo nel lato costo, quella modifica viene propagata al lato vendite.</span><span class="sxs-lookup"><span data-stu-id="25c4f-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="25c4f-110">Ciò è possibile in quanto i seguenti plug-in devono essere registrati di nuovo dopo una modifica alle dimensioni di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="25c4f-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="25c4f-111">PreOperationContractLineDetailUpdate - Aggiorna **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="25c4f-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="25c4f-112">PreOperationQuoteLineDetailUpdate - Aggiorna **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="25c4f-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="25c4f-113">La procedura seguente consente di eseguire la registrazione dei plug-in.</span><span class="sxs-lookup"><span data-stu-id="25c4f-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="25c4f-114">Apri **PluginRegistrationTool** e connettiti all'istanza online.</span><span class="sxs-lookup"><span data-stu-id="25c4f-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="25c4f-115">Fai clic su **Cerca** e cerca il plug-in da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="25c4f-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Screenshot della struttura di ricerca](media/PRT-1.png)

3. <span data-ttu-id="25c4f-117">Una volta trovato il plug-in, selezionalo e fai clic su **Seleziona nel modulo principale**.</span><span class="sxs-lookup"><span data-stu-id="25c4f-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="25c4f-118">Seleziona il passaggio del plug-in da aggiornare, fai clic con il pulsante destro del mouse e quindi scegli **Aggiorna**.</span><span class="sxs-lookup"><span data-stu-id="25c4f-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Screenshot del plug-in da aggiornare](media/PRT-2.png)
 
5. <span data-ttu-id="25c4f-120">Nella finestra di aggiornamento, fai clic sui puntini di sospensione (**...**) negli attributi di filtro.</span><span class="sxs-lookup"><span data-stu-id="25c4f-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Screenshot delle informazioni di configurazione di Aggiorna passaggio esistente](media/PRT-3.png)
 
6. <span data-ttu-id="25c4f-122">Seleziona le caselle di controllo degli attributi di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="25c4f-122">Select the pricing attribute check boxes.</span></span>

 ![Screenshot che mostra la selezione delle caselle di controllo degli attributi di determinazione dei prezzi](media/PRT-4.png)

7. <span data-ttu-id="25c4f-124">Fai clic su **OK** per chiudere la pagina e quindi seleziona **Aggiorna passaggio**.</span><span class="sxs-lookup"><span data-stu-id="25c4f-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Screenshot con il pulsante "Aggiorna passaggio"](media/PRT-5.png)
 
8. <span data-ttu-id="25c4f-126">Ripeti questa procedura per il secondo plug-in. **PreOperationQuoteLineDetail - Aggiornamento di msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="25c4f-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="25c4f-127">Chiudi lo strumento per la registrazione di plug-in.</span><span class="sxs-lookup"><span data-stu-id="25c4f-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]