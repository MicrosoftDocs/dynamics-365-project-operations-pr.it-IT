---
title: Modalità di pianificazione
description: In questo argomento vengono fornite informazioni sulle modalità di pianificazione.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981440"
---
# <a name="scheduling-modes"></a><span data-ttu-id="dc1be-103">Modalità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="dc1be-103">Scheduling modes</span></span>

<span data-ttu-id="dc1be-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="dc1be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="dc1be-105">Dynamics 365 Project Operations fornisce la possibilità alle organizzazioni di definire come gestire le modifiche alle variabili chiave nelle attività all'interno della struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="dc1be-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="dc1be-106">In base alle esigenze specifiche dell'organizzazione, i responsabili di progetto possono apportare modifiche alla modalità di pianificazione quando viene creato un progetto.</span><span class="sxs-lookup"><span data-stu-id="dc1be-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="dc1be-107">Sono disponibili tre modalità di pianificazione in Project Operations:</span><span class="sxs-lookup"><span data-stu-id="dc1be-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="dc1be-108">Durata fissa (questa è la modalità predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc1be-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="dc1be-109">Lavoro fisso</span><span class="sxs-lookup"><span data-stu-id="dc1be-109">Fixed work</span></span>
  - <span data-ttu-id="dc1be-110">Unità fisse</span><span class="sxs-lookup"><span data-stu-id="dc1be-110">Fixed units</span></span>

<span data-ttu-id="dc1be-111">I valori influenzati dalla definizione di una specifica modalità di pianificazione sono determinati dalla seguente formula:</span><span class="sxs-lookup"><span data-stu-id="dc1be-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="dc1be-112">Risorse (*Lavoro*) = Durata x unità</span><span class="sxs-lookup"><span data-stu-id="dc1be-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="dc1be-113">Quando definisci la modalità di pianificazione di un progetto, imposti uno di questi valori che poi non può più essere modificato.</span><span class="sxs-lookup"><span data-stu-id="dc1be-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="dc1be-114">Mantenere questo valore come costante pone una priorità su quel valore, che notifica al sistema di non cambiarlo quando cambiano gli altri due valori.</span><span class="sxs-lookup"><span data-stu-id="dc1be-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="dc1be-115">La tabella seguente fornisce informazioni sugli impatti della selezione di una modalità specifica.</span><span class="sxs-lookup"><span data-stu-id="dc1be-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="dc1be-116">**In questa attività**</span><span class="sxs-lookup"><span data-stu-id="dc1be-116">**In this task**</span></span>             | <span data-ttu-id="dc1be-117">**Se rivedi le unità**</span><span class="sxs-lookup"><span data-stu-id="dc1be-117">**If you revise units**</span></span>   | <span data-ttu-id="dc1be-118">**Se rivedi la durata**</span><span class="sxs-lookup"><span data-stu-id="dc1be-118">**If you revise duration**</span></span> | <span data-ttu-id="dc1be-119">**Se rivedi il lavoro**</span><span class="sxs-lookup"><span data-stu-id="dc1be-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="dc1be-120">Attività unità fisse</span><span class="sxs-lookup"><span data-stu-id="dc1be-120">Fixed units task</span></span>     | <span data-ttu-id="dc1be-121">La durata viene ricalcolata.</span><span class="sxs-lookup"><span data-stu-id="dc1be-121">Duration is recalculated.</span></span> | <span data-ttu-id="dc1be-122">Il lavoro viene ricalcolato.</span><span class="sxs-lookup"><span data-stu-id="dc1be-122">Effort is recalculated.</span></span>    | <span data-ttu-id="dc1be-123">La durata viene ricalcolata.</span><span class="sxs-lookup"><span data-stu-id="dc1be-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="dc1be-124">Attività lavoro fisso</span><span class="sxs-lookup"><span data-stu-id="dc1be-124">Fixed effort task</span></span>    | <span data-ttu-id="dc1be-125">La durata viene ricalcolata.</span><span class="sxs-lookup"><span data-stu-id="dc1be-125">Duration is recalculated.</span></span> | <span data-ttu-id="dc1be-126">Le unità vengono ricalcolate.</span><span class="sxs-lookup"><span data-stu-id="dc1be-126">Units are recalculated.</span></span>    | <span data-ttu-id="dc1be-127">La durata viene ricalcolata.</span><span class="sxs-lookup"><span data-stu-id="dc1be-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="dc1be-128">Attività durata fissa</span><span class="sxs-lookup"><span data-stu-id="dc1be-128">Fixed duration task</span></span>  | <span data-ttu-id="dc1be-129">Il lavoro viene ricalcolato.</span><span class="sxs-lookup"><span data-stu-id="dc1be-129">Effort is recalculated.</span></span>   | <span data-ttu-id="dc1be-130">Il lavoro viene ricalcolato.</span><span class="sxs-lookup"><span data-stu-id="dc1be-130">Effort is recalculated.</span></span>    | <span data-ttu-id="dc1be-131">Le unità vengono ricalcolate.</span><span class="sxs-lookup"><span data-stu-id="dc1be-131">Units are recalculated.</span></span>   |

<span data-ttu-id="dc1be-132">Per ulteriori informazioni sulle implicazioni di una determinata modalità, vedi [Modificare il tipo di attività per una pianificazione più accurata](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="dc1be-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="dc1be-133">In argomento, il termine **lavoro** viene utilizzato al posto di **risorse**.</span><span class="sxs-lookup"><span data-stu-id="dc1be-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="dc1be-134">Modificare la modalità di pianificazione dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="dc1be-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="dc1be-135">Completa i seguenti passaggi per definire la modalità di pianificazione di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="dc1be-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="dc1be-136">Vai a **Impostazioni** \> **Generale** \> **Parametri** e quindi seleziona il parametro del progetto.</span><span class="sxs-lookup"><span data-stu-id="dc1be-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="dc1be-137">Nella pagina **Parametri di progetto** seleziona la modalità di pianificazione predefinita per l'organizzazione, quindi definisci la possibilità per il responsabile di progetto di sovrascrivere l'impostazione durante la creazione di un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="dc1be-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="dc1be-138">Modificare l'impostazione della modalità di pianificazione in un progetto</span><span class="sxs-lookup"><span data-stu-id="dc1be-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="dc1be-139">Se un'organizzazione consente al responsabile di progetto di sovrascrivere la modalità di pianificazione predefinita, il responsabile di progetto può apportare questa modifica quando crea un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="dc1be-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="dc1be-140">Tuttavia, dopo che il progetto è stato salvato, la modalità di pianificazione non può più essere modificata.</span><span class="sxs-lookup"><span data-stu-id="dc1be-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="dc1be-141">Progetti copiati</span><span class="sxs-lookup"><span data-stu-id="dc1be-141">Copied projects</span></span>

<span data-ttu-id="dc1be-142">Poiché un progetto viene creato quando viene eseguita l'azione di copia progetto, il responsabile di progetto non può impostare la modalità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="dc1be-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="dc1be-143">Il progetto di destinazione sarà sempre predefinito nella modalità definita a livello organizzativo.</span><span class="sxs-lookup"><span data-stu-id="dc1be-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="dc1be-144">Attività copiate</span><span class="sxs-lookup"><span data-stu-id="dc1be-144">Copied tasks</span></span>

<span data-ttu-id="dc1be-145">Quando un'attività viene copiata da un progetto a un altro, l'attività eredita la modalità di pianificazione del progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dc1be-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
