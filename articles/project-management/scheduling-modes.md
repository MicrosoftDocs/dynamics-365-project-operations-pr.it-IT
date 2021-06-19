---
title: Modalità di pianificazione
description: In questo argomento vengono fornite informazioni sulle modalità di pianificazione.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116712"
---
# <a name="scheduling-modes"></a><span data-ttu-id="4d560-103">Modalità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4d560-103">Scheduling modes</span></span>

<span data-ttu-id="4d560-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="4d560-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4d560-105">Dynamics 365 Project Operations fornisce la possibilità alle organizzazioni di definire come gestire le modifiche alle variabili chiave nelle attività all'interno della struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="4d560-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="4d560-106">In base alle esigenze specifiche dell'organizzazione, i responsabili di progetto possono apportare modifiche alla modalità di pianificazione quando viene creato un progetto.</span><span class="sxs-lookup"><span data-stu-id="4d560-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="4d560-107">Sono disponibili tre modalità di pianificazione in Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4d560-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="4d560-108">Durata fissa (questa è la modalità predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d560-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="4d560-109">Lavoro fisso (*Lavoro*)</span><span class="sxs-lookup"><span data-stu-id="4d560-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="4d560-110">Unità fisse</span><span class="sxs-lookup"><span data-stu-id="4d560-110">Fixed units</span></span>

<span data-ttu-id="4d560-111">I valori influenzati dalla definizione di una specifica modalità di pianificazione sono determinati dalla seguente formula:</span><span class="sxs-lookup"><span data-stu-id="4d560-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="4d560-112">Lavoro = Durata x Unità</span><span class="sxs-lookup"><span data-stu-id="4d560-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="4d560-113">Quando definisci la modalità di pianificazione di un progetto, imposti uno di questi valori che poi non può più essere modificato.</span><span class="sxs-lookup"><span data-stu-id="4d560-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="4d560-114">Mantenere questo valore come costante pone una priorità su quel valore, che notifica al sistema di non cambiarlo quando cambiano gli altri due valori.</span><span class="sxs-lookup"><span data-stu-id="4d560-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="4d560-115">La tabella seguente fornisce informazioni sugli impatti della selezione di una modalità specifica.</span><span class="sxs-lookup"><span data-stu-id="4d560-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="4d560-116">**In questa attività**</span><span class="sxs-lookup"><span data-stu-id="4d560-116">**In this task**</span></span>             | <span data-ttu-id="4d560-117">**Se rivedi le unità**</span><span class="sxs-lookup"><span data-stu-id="4d560-117">**If you revise units**</span></span>   | <span data-ttu-id="4d560-118">**Se rivedi la durata**</span><span class="sxs-lookup"><span data-stu-id="4d560-118">**If you revise duration**</span></span> | <span data-ttu-id="4d560-119">**Se rivedi il lavoro**</span><span class="sxs-lookup"><span data-stu-id="4d560-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="4d560-120">Attività unità fisse</span><span class="sxs-lookup"><span data-stu-id="4d560-120">Fixed units task</span></span>     | <span data-ttu-id="4d560-121">La durata viene ricalcolata.</span><span class="sxs-lookup"><span data-stu-id="4d560-121">Duration is recalculated.</span></span> | <span data-ttu-id="4d560-122">Il lavoro viene ricalcolato.</span><span class="sxs-lookup"><span data-stu-id="4d560-122">Effort is recalculated.</span></span>    | <span data-ttu-id="4d560-123">La durata viene ricalcolata.</span><span class="sxs-lookup"><span data-stu-id="4d560-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="4d560-124">Attività lavoro fisso</span><span class="sxs-lookup"><span data-stu-id="4d560-124">Fixed effort task</span></span>    | <span data-ttu-id="4d560-125">La durata viene ricalcolata.</span><span class="sxs-lookup"><span data-stu-id="4d560-125">Duration is recalculated.</span></span> | <span data-ttu-id="4d560-126">Le unità vengono ricalcolate.</span><span class="sxs-lookup"><span data-stu-id="4d560-126">Units are recalculated.</span></span>    | <span data-ttu-id="4d560-127">La durata viene ricalcolata.</span><span class="sxs-lookup"><span data-stu-id="4d560-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="4d560-128">Attività durata fissa</span><span class="sxs-lookup"><span data-stu-id="4d560-128">Fixed duration task</span></span>  | <span data-ttu-id="4d560-129">Il lavoro viene ricalcolato.</span><span class="sxs-lookup"><span data-stu-id="4d560-129">Effort is recalculated.</span></span>   | <span data-ttu-id="4d560-130">Il lavoro viene ricalcolato.</span><span class="sxs-lookup"><span data-stu-id="4d560-130">Effort is recalculated.</span></span>    | <span data-ttu-id="4d560-131">Le unità vengono ricalcolate.</span><span class="sxs-lookup"><span data-stu-id="4d560-131">Units are recalculated.</span></span>   |

<span data-ttu-id="4d560-132">Per ulteriori informazioni sulle implicazioni di una determinata modalità, vedi [Modificare il tipo di attività per una pianificazione più accurata](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="4d560-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="4d560-133">In argomento, il termine **lavoro** viene utilizzato al posto di **risorse**.</span><span class="sxs-lookup"><span data-stu-id="4d560-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="4d560-134">Modificare la modalità di pianificazione dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="4d560-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="4d560-135">Completa i seguenti passaggi per definire la modalità di pianificazione di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="4d560-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="4d560-136">Vai a **Impostazioni** \> **Generale** \> **Parametri** e quindi seleziona il parametro del progetto.</span><span class="sxs-lookup"><span data-stu-id="4d560-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="4d560-137">Nella pagina **Parametri di progetto** seleziona la modalità di pianificazione predefinita per l'organizzazione, quindi definisci la possibilità per il responsabile di progetto di sovrascrivere l'impostazione durante la creazione di un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="4d560-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="4d560-138">Modificare l'impostazione della modalità di pianificazione in un progetto</span><span class="sxs-lookup"><span data-stu-id="4d560-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="4d560-139">Se un'organizzazione consente al responsabile di progetto di sovrascrivere la modalità di pianificazione predefinita, il responsabile di progetto può apportare questa modifica quando crea un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="4d560-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="4d560-140">Tuttavia, dopo che il progetto è stato salvato, la modalità di pianificazione non può più essere modificata.</span><span class="sxs-lookup"><span data-stu-id="4d560-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="4d560-141">Progetti copiati</span><span class="sxs-lookup"><span data-stu-id="4d560-141">Copied projects</span></span>

<span data-ttu-id="4d560-142">Poiché un progetto viene creato quando viene eseguita l'azione di copia progetto, il responsabile di progetto non può impostare la modalità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4d560-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="4d560-143">Il progetto di destinazione sarà sempre predefinito nella modalità definita a livello organizzativo.</span><span class="sxs-lookup"><span data-stu-id="4d560-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="4d560-144">Attività copiate</span><span class="sxs-lookup"><span data-stu-id="4d560-144">Copied tasks</span></span>

<span data-ttu-id="4d560-145">Quando un'attività viene copiata da un progetto a un altro, l'attività eredita la modalità di pianificazione del progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4d560-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
