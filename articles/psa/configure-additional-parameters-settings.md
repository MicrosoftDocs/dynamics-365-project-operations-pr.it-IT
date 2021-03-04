---
title: Configurare impostazioni di parametri aggiuntivi
description: Come configurare le impostazioni dei parametri aggiuntivi in Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 73264845808e12950a48eea2b79e54c393d9c024
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151573"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="9b8da-103">Configurare le impostazioni dei parametri aggiuntivi (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9b8da-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9b8da-104">Una volta configurati gli oggetti negli argomenti precedenti, devi impostare altri parametri aggiuntivi del progetto da usare per i progetti.</span><span class="sxs-lookup"><span data-stu-id="9b8da-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="9b8da-105">Quando hai installato per la prima volta [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] hai creato un'impostazione di parametri per creare prima tutti i record richiesti per [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="9b8da-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="9b8da-106">È ora di tornare indietro e configurare altri campi per queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="9b8da-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="9b8da-107">Dovrai configurare le seguenti impostazioni:</span><span class="sxs-lookup"><span data-stu-id="9b8da-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="9b8da-108">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="9b8da-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="9b8da-109">Frequenza di fatturazione</span><span class="sxs-lookup"><span data-stu-id="9b8da-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="9b8da-110">Modello di ore lavorative</span><span class="sxs-lookup"><span data-stu-id="9b8da-110">Work hours template</span></span>  
  
-   <span data-ttu-id="9b8da-111">Listino prezzi</span><span class="sxs-lookup"><span data-stu-id="9b8da-111">Price list</span></span>  
 
<span data-ttu-id="9b8da-112">In questo passaggio, dovrai indicare il tipo di assegnazione delle risorse desiderato:</span><span class="sxs-lookup"><span data-stu-id="9b8da-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="9b8da-113">**Centrale**.</span><span class="sxs-lookup"><span data-stu-id="9b8da-113">**Central**.</span></span> <span data-ttu-id="9b8da-114">Solo i responsabili delle risorse possono assegnare le risorse ai progetti.</span><span class="sxs-lookup"><span data-stu-id="9b8da-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="9b8da-115">**Ibrido**.</span><span class="sxs-lookup"><span data-stu-id="9b8da-115">**Hybrid**.</span></span> <span data-ttu-id="9b8da-116">I responsabili delle risorse i, responsabili di progetto e gli account manager possono assegnare le risorse ai progetti.</span><span class="sxs-lookup"><span data-stu-id="9b8da-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="9b8da-117">Per impostare i parametri di progetto:</span><span class="sxs-lookup"><span data-stu-id="9b8da-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="9b8da-118">Passa a **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="9b8da-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="9b8da-119">Fai clic sui parametri che desideri configurare (quello creato quando hai installato per la prima volta [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) oppure fai clic su **Nuovo** per crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="9b8da-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="9b8da-120">Nell'area **Generale**, imposta tutte le opzioni per i parametri del progetto.</span><span class="sxs-lookup"><span data-stu-id="9b8da-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="9b8da-121">Nell'area **Listino prezzi** fai clic su **+** per aggiungere un listino prezzi, seleziona un listino nell'elenco a discesa **Listino prezzi parametro di progetto**, quindi fai clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="9b8da-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="9b8da-122">Fai clic sul pulsante **Salva** nell'angolo in basso a destra dello schermo.</span><span class="sxs-lookup"><span data-stu-id="9b8da-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="9b8da-123">Il record di parametri del progetto deve essere mantenuto per il corretto funzionamento di Project Service.</span><span class="sxs-lookup"><span data-stu-id="9b8da-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="9b8da-124">Questo record non deve essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="9b8da-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="9b8da-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b8da-125">See Also</span></span>  
 [<span data-ttu-id="9b8da-126">Configurare le risorse</span><span class="sxs-lookup"><span data-stu-id="9b8da-126">Set up resources</span></span>](../psa/set-up-resources.md)
