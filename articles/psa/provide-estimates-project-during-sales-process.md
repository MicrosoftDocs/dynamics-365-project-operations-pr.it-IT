---
title: Fornire stime di lavoro per un progetto durante il processo di vendita
description: Come fornire stime di lavoro per un progetto durante il processo di vendita in Project Service
author: ruhercul
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120593"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="84f99-103">Fornire stime di lavoro per un progetto durante il processo di vendita (Project Service)</span><span class="sxs-lookup"><span data-stu-id="84f99-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="84f99-104">Durante il processo di vendita, puoi eseguire le stime di vendita dal basso fino alle voci di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="84f99-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="84f99-105">Le funzionalità [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] offrono un modo più scientifico e deterministico per fornire le stime di vendita suddividendo gli elementi di lavoro e associando gli attributi pertinenti che contribuiscono alle stime del progetto nella struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="84f99-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="84f99-106">Dopo aver acquisito la vendita, puoi utilizzare la struttura di suddivisione del lavoro associata al piano di progetto, ridefinendolo come necessario per il buon completamento del progetto.</span><span class="sxs-lookup"><span data-stu-id="84f99-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="84f99-107">Collega un progetto a una riga di offerta</span><span class="sxs-lookup"><span data-stu-id="84f99-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="84f99-108">Quando si crea una riga di offerta basata sul progetto offerta, puoi creare un nuovo progetto dalla riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="84f99-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="84f99-109">Puoi quindi utilizzare i modelli di progetto, che sono piani di progetto standard preconfigurati e stime finanziarie comuni all'organizzazione, o una copia di un piano di progetto e stime da un progetto passato.</span><span class="sxs-lookup"><span data-stu-id="84f99-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="84f99-110">Quando crei un progetto, la scelta di un modello di progetto offre una base per ridefinire il piano di progetto, le stime e i requisiti del ruolo.</span><span class="sxs-lookup"><span data-stu-id="84f99-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="84f99-111">Creando il progetto dall'offerta, questo viene automaticamente associato alla riga dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="84f99-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="84f99-112">Componenti della stima del progetto</span><span class="sxs-lookup"><span data-stu-id="84f99-112">Project estimate components</span></span>  
 <span data-ttu-id="84f99-113">La struttura di suddivisione del lavoro in un progetto offre un modo per suddividere il lavoro in attività, di gestire una gerarchia di attività e assegnare una stima del lavoro richiesto per completare ogni attività.</span><span class="sxs-lookup"><span data-stu-id="84f99-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="84f99-114">Puoi associare i ruoli a un'attività per indicare una stima del tipo di risorsa richiesto per completare un'attività e una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="84f99-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="84f99-115">La struttura di suddivisione del lavoro consente di determinare le stime di lavoro e di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="84f99-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="84f99-116">Per impostazione predefinita, il progetto utilizza i listini prezzi definiti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="84f99-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="84f99-117">I prezzi di costo e di vendita definiti nei listini prezzi consentono di determinare le stime finanziarie per la suddivisione del lavoro del progetto.</span><span class="sxs-lookup"><span data-stu-id="84f99-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="84f99-118">Se il progetto è associato a un'offerta e l'offerta ha un listino prezzi diverso da quello predefiniti, il listino prezzi dell'offerta viene utilizzato per stime finanziarie.</span><span class="sxs-lookup"><span data-stu-id="84f99-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="84f99-119">Importa le stime da un progetto a un'offerta</span><span class="sxs-lookup"><span data-stu-id="84f99-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="84f99-120">Con le stime di progetto nel progetto, puoi importarle nella riga dell'offerta:</span><span class="sxs-lookup"><span data-stu-id="84f99-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="84f99-121">In **Dettagli riga di offerta** fai clic su **Importa da stime**.</span><span class="sxs-lookup"><span data-stu-id="84f99-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="84f99-122">Seleziona se importare le stime di progetto riepilogate dal tipo delle transazioni, ruolo, o livello del nodo della struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="84f99-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="84f99-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84f99-123">See Also</span></span>  
 [<span data-ttu-id="84f99-124">Guida del responsabile di progetto</span><span class="sxs-lookup"><span data-stu-id="84f99-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
