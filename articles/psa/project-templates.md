---
title: Modelli di progetto
description: In questo argomento vengono fornite informazioni su come utilizzare modelli di progetto per una rapida configurazione dei progetti.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079038"
---
# <a name="project-templates"></a><span data-ttu-id="ba114-103">Modelli di progetto</span><span class="sxs-lookup"><span data-stu-id="ba114-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ba114-104">Un modello di progetto è un framework predefinito che consente di iniziare facilmente e velocemente un progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="ba114-105">Puoi utilizzare un modello predefinito per creare un nuovo progetto con un singolo clic.</span><span class="sxs-lookup"><span data-stu-id="ba114-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="ba114-106">Quanto ai progetti, devi definire i prerequisiti per i modelli di progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="ba114-107">Devi definire un calendario di progetto per ogni modello di progetto e ruoli e listini prezzi devono essere predefiniti nell'organizzazione, di modo che i componenti del modello abbiano dati utili.</span><span class="sxs-lookup"><span data-stu-id="ba114-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="ba114-108">Un modello di progetto include tre componenti: una pianificazione, stime di progetto e membri del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="ba114-109">Pianifica</span><span class="sxs-lookup"><span data-stu-id="ba114-109">Schedule</span></span>

<span data-ttu-id="ba114-110">Una pianificazione in un modello di progetto include lo stesso set di elementi di una pianificazione in un progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="ba114-111">Puoi creare una gerarchia di attività, associare ruoli ad attività, definire attributi di pianificazione e impostare dipendenze.</span><span class="sxs-lookup"><span data-stu-id="ba114-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="ba114-112">Una pianificazione in un modello di progetto supporta inoltre modalità di attività per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="ba114-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="ba114-113">Pertanto, supporta il motore di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ba114-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="ba114-114">Devi associare un calendario di progetto al progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="ba114-115">Quando crei una pianificazione del lavoro, non c'è differenza tra un modello di progetto e un progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="ba114-116">Stime di progetto</span><span class="sxs-lookup"><span data-stu-id="ba114-116">Project estimates</span></span>

<span data-ttu-id="ba114-117">Il funzionamento delle stime di progetto in un modello di progetto è uguale a quello delle stime di progetto in un progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="ba114-118">Tuttavia, i prezzi di costo e vendita sono estratti dai listini prezzi di costo e vendita predefiniti definiti nei parametri.</span><span class="sxs-lookup"><span data-stu-id="ba114-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="ba114-119">Creare un progetto da un modello</span><span class="sxs-lookup"><span data-stu-id="ba114-119">Creating a project from a template</span></span>
 
<span data-ttu-id="ba114-120">Esistono vari modi di creare un progetto da un modello di progetto:</span><span class="sxs-lookup"><span data-stu-id="ba114-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="ba114-121">Quando crei un progetto da un'offerta, puoi selezionare un modello di progetto nella finestra di dialogo **Creazione rapida: Progetto**.</span><span class="sxs-lookup"><span data-stu-id="ba114-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Finestra di dialogo Creazione rapida: Progetto](media/project-11.png)

- <span data-ttu-id="ba114-123">Quando crei un progetto selezionando **Nuovo progetto** , viene visualizzata la pagina **Progetto** prima del salvataggio del record.</span><span class="sxs-lookup"><span data-stu-id="ba114-123">When you create a project by selecting **New Project** , the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="ba114-124">Nel campo **Seleziona un modello** , seleziona uno dei modelli di progetto predefiniti nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ba114-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="ba114-125">Utilizza **Crea progetto da un modello** nella pagina **Entità modello**.</span><span class="sxs-lookup"><span data-stu-id="ba114-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="ba114-126">Copiare componenti di un modello in un progetto</span><span class="sxs-lookup"><span data-stu-id="ba114-126">Copying components of template to project</span></span>

<span data-ttu-id="ba114-127">Quando copi i componenti di un modello di progetto in un progetto, possono verificarsi alcune sostituzioni, a seconda delle impostazioni nel progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="ba114-128">Copiare la pianificazione</span><span class="sxs-lookup"><span data-stu-id="ba114-128">Copying the schedule</span></span>

<span data-ttu-id="ba114-129">Quando copi la pianificazione da un modello di progetto, se il progetto ha un calendario di progetto differente rispetto al modello, le ore lavorative nel calendario del progetto vengono applicate alla pianificazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="ba114-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="ba114-130">In questo modo la pianificazione viene modificata affinché corrisponda al calendario di progetto di backup.</span><span class="sxs-lookup"><span data-stu-id="ba114-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="ba114-131">Analogamente, la prima attività nella pianificazione acquisisce la data iniziale del progetto e la pianificazione del resto della gerarchia viene aggiornata in base alla durata e alle dipendenze specificate nel modello.</span><span class="sxs-lookup"><span data-stu-id="ba114-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="ba114-132">Copiare stime di progetto</span><span class="sxs-lookup"><span data-stu-id="ba114-132">Copying project estimates</span></span> 

<span data-ttu-id="ba114-133">Quando copi nelle righe di stima del progetto, i listini prezzi vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="ba114-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="ba114-134">Per il listino prezzi di costo, questi aggiornamenti sono basati sull'unità proprietaria del progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="ba114-135">Per il listino prezzi di vendita, sono basati sul cliente.</span><span class="sxs-lookup"><span data-stu-id="ba114-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="ba114-136">Per i progetti associati a un'entità Vendite, il costo unitario e i prezzi di vendita vengono determinati in base a questi listini prezzi.</span><span class="sxs-lookup"><span data-stu-id="ba114-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="ba114-137">Copiare un team di progetto</span><span class="sxs-lookup"><span data-stu-id="ba114-137">Copying a project team</span></span>

<span data-ttu-id="ba114-138">Quando un team di progetto viene copiato da un modello di progetto in un progetto, le risorse generiche vengono copiate insieme alle competenze e alle qualifiche definite nel modello.</span><span class="sxs-lookup"><span data-stu-id="ba114-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="ba114-139">Anche le assegnazioni di risorse generiche vengono gestite come se fossero nel modello di progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="ba114-140">Le risorse denominate non sono supportate nei modelli di progetto.</span><span class="sxs-lookup"><span data-stu-id="ba114-140">Named resources aren't supported in project templates.</span></span>
