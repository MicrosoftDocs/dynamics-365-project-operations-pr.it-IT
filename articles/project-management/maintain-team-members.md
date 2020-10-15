---
title: Gestire membri del team
description: In questo argomento vengono fornite informazioni sulla prenotazione di risorse denominate per team di progetto e sull'assegnazione delle risorse ad attività.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961889"
---
# <a name="maintain-team-members"></a><span data-ttu-id="36540-103">Gestire membri del team</span><span class="sxs-lookup"><span data-stu-id="36540-103">Maintain team members</span></span>

<span data-ttu-id="36540-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="36540-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="36540-105">Puoi aggiungere una risorsa denominata a un team di progetto prenotandole direttamente nel team.</span><span class="sxs-lookup"><span data-stu-id="36540-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="36540-106">In Dynamics 365 Project Operations, vai a **Progetti** e apri il progetto per cui esegui le prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="36540-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="36540-107">Nella pagina **Progetto**, nella scheda **Team**, seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="36540-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="36540-108">Nella finestra di dialogo **Creazione rapida: Membro del team di progetto**, seleziona la risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="36540-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="36540-109">Il campo **Ruolo** verrà popolato con il ruolo predefinito della risorsa, se a questa ne è stato assegnato uno.</span><span class="sxs-lookup"><span data-stu-id="36540-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="36540-110">È possibile modificare il ruolo.</span><span class="sxs-lookup"><span data-stu-id="36540-110">You can change the role.</span></span> 
4. <span data-ttu-id="36540-111">Seleziona le date di inizio e di fine per la risorsa e quindi il metodo di allocazione della capacità della risorsa.</span><span class="sxs-lookup"><span data-stu-id="36540-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="36540-112">Se il membro del team deve essere un responsabile approvazione di progetto, seleziona **Sì** nel campo **Responsabile approvazione di progetto**.</span><span class="sxs-lookup"><span data-stu-id="36540-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="36540-113">Il membro del team può approvare voci di spesa e inserimenti ore inviati per il progetto.</span><span class="sxs-lookup"><span data-stu-id="36540-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="36540-114">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="36540-114">Select **Save**.</span></span>

<span data-ttu-id="36540-115">Ora puoi assegnare la risorsa prenotata ad attività nel progetto.</span><span class="sxs-lookup"><span data-stu-id="36540-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="36540-116">Nella pagina **Progetto**, fai clic sulla scheda **Pianifica** per assegnare attività alla nuova risorsa.</span><span class="sxs-lookup"><span data-stu-id="36540-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="36540-117">Il selettore di risorse eseguito dal campo **Risorse** nella griglia delle attività indicherà i membri del team che è possibile selezionare.</span><span class="sxs-lookup"><span data-stu-id="36540-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="36540-118">In Project Operations, le prenotazioni di risorse e le assegnazioni di attività non sono strettamente collegate.</span><span class="sxs-lookup"><span data-stu-id="36540-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="36540-119">Quando utilizzi il selettore di risorse nella pianificazione, puoi assegnare attività a membri del team per più ore di quelle che le relative prenotazioni coprono nel progetto.</span><span class="sxs-lookup"><span data-stu-id="36540-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="36540-120">Le differenze tra le prenotazioni dei membri del team e le assegnazioni sono mostrate nelle schede **Team** e **Riconciliazione risorse**.</span><span class="sxs-lookup"><span data-stu-id="36540-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="36540-121">Puoi anche riconciliare le differenze tra le prenotazioni e le assegnazioni per le risorse a un livello più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="36540-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="36540-122">Utilizza il selettore di risorse nella scheda **Pianifica** per cercare e selezionare le risorse prenotabili che non fanno ancora parte del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="36540-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="36540-123">Queste risorse sono visualizzate nel selettore di risorse come **Altre risorse**.</span><span class="sxs-lookup"><span data-stu-id="36540-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="36540-124">Quando si effettua una selezione, la risorsa viene aggiunta al team di progetto e assegnata all'attività, ma non viene generata alcuna prenotazione.</span><span class="sxs-lookup"><span data-stu-id="36540-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="36540-125">Puoi utilizzare la funzionalità di prenotazione estesa della scheda **Riconciliazione** o la **Scheda di pianificazione** per prenotare la capacità della risorsa per il progetto.</span><span class="sxs-lookup"><span data-stu-id="36540-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="36540-126">Dopo la prenotazione di un membro del team nel progetto, puoi utilizzare **Gestisci prenotazioni** o la **scheda di pianificazione** direttamente per gestire le tue prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="36540-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
