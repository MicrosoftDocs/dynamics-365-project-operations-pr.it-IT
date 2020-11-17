---
title: Creare un modello di progetto
description: Come creare un modello di progetto in Project Service
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
ms.openlocfilehash: 78d25183aad8d86593d3f2582295db59eb84cf14
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133193"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="fb7a6-103">Creare un modello di progetto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fb7a6-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fb7a6-104">I modelli di progetto consentono di risparmiare tempo se la società esegue regolarmente offerte per tipi di progetti simili.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="fb7a6-105">Tali modelli forniscono un set standard di ruoli e di ore previste per tipo di progetto.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="fb7a6-106">I responsabili di gestione account e di progetto possono creare i progetti in base a un modello di progetto o possono copiare il modello ed eseguirne di personalizzati.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="fb7a6-107">Componenti del modello di progetto</span><span class="sxs-lookup"><span data-stu-id="fb7a6-107">Components of project template</span></span>
 <span data-ttu-id="fb7a6-108">Un modello di progetto è composto da tre componenti:</span><span class="sxs-lookup"><span data-stu-id="fb7a6-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="fb7a6-109">**Struttura di suddivisione del lavoro**: una struttura di suddivisione del lavoro nel modello di progetto ha lo stesso set di elementi del progetto.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="fb7a6-110">È possibile creare una gerarchia di attività, associare ruoli all'attività, definire gli attributi di pianificazione, impostare dipendenze e visualizzare i dati nel diagramma di Gantt.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="fb7a6-111">La struttura di suddivisione del lavoro in modelli di progetto supporta anche modalità di attività per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="fb7a6-112">Non esiste una differenza tra un modello di progetto e un progetto quando si crea una pianificazione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="fb7a6-113">**Stime di progetto**: e stime di progetto nei modelli funzionano nello stesso modo in cui funzionano nei progetti, ad eccezione del fatto che i costi e i prezzi di vendita specificati sono sempre i costi e i listini prezzi di vendita predefiniti indicati nei parametri di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fb7a6-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="fb7a6-114">Per il resto, il funzionamento è analogo a quello del progetto.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="fb7a6-115">**Formazione del team di progetto**: quando si crea un team di progettazione per un modello di progetto, non puoi prenotare una risorsa denominata nel modello.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="fb7a6-116">Puoi utilizzare **Genera team progetto** nella struttura di suddivisione del lavoro per creare un gruppo di risorse generiche.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="fb7a6-117">Puoi anche specificare le attività e le competenze necessarie per risorse generiche.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="fb7a6-118">Non puoi sostituire una risorsa generica a una risorsa prenotabile in modelli di progetto.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="fb7a6-119">Crea un progetto da un modello</span><span class="sxs-lookup"><span data-stu-id="fb7a6-119">Create a project from a template</span></span>  
 <span data-ttu-id="fb7a6-120">Puoi creare un progetto da un modello nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb7a6-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="fb7a6-121">Quando si crea un progetto dall'offerta, puoi scegliere un modello di progetto nel modulo di creazione rapida del progetto stesso.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="fb7a6-122">Quando si crea un progetto facendo clic su **Nuovo progetto**, viene visualizzato il modulo del progetto prima di salvare il record.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="fb7a6-123">Qui puoi fare clic sul campo **Seleziona un modello** per scegliere un modello nell'elenco dei modelli predefiniti nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="fb7a6-124">Fai clic su **Crea progetto da un modello** nella pagina **Modello di progetto** per creare un progetto dal modello.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="fb7a6-125">Copia di componenti di un modello in un progetto</span><span class="sxs-lookup"><span data-stu-id="fb7a6-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="fb7a6-126">Quando si copiano i componenti di un modello in un progetto, è necessario tenere in considerazione alcuni aspetti.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="fb7a6-127">**Copia di una struttura di suddivisione del lavoro**: quando si copia la struttura di suddivisione del lavoro utilizzando un modello di progetto, se il progetto ha un calendario diverso dal progetto, le ore lavorative nel calendario di progetto verranno applicate alla pianificazione di attività.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="fb7a6-128">In questo modo viene modificata la pianificazione nel calendario di progetto di backup.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="fb7a6-129">Analogamente, la prima attività sulla struttura di suddivisione del lavoro ha come data quella di inizio del progetto, in modo che il resto della pianificazione della gerarchia di attività venga aggiornato in base alla durata e alle dipendenze specificate nella struttura di suddivisione del lavoro del modello.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="fb7a6-130">**Copia di stime di progetto**: quando si copia nelle righe di stima del progetto, i listini prezzi vengono aggiornati in base all'unità proprietaria del progetto per il listino prezzi di costo e in base al cliente per il listino prezzi di vendita.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="fb7a6-131">Il costo unitario e i prezzi di vendita vengono determinati da tali listini prezzi dei progetti associati a un'entità di vendita.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="fb7a6-132">**Copia di un team di progetto**: quando si copia il team di progetto dal modello in un progetto, le risorse generiche vengono copiate, insieme alle competenze definite nel modello.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="fb7a6-133">Le assegnazioni di risorse generiche vengono memorizzate come nel modello del progetto.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fb7a6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb7a6-134">See Also</span></span>  
 [<span data-ttu-id="fb7a6-135">Guida del responsabile di progetto</span><span class="sxs-lookup"><span data-stu-id="fb7a6-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
