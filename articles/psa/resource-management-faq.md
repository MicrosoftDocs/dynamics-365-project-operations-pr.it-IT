---
title: Domande frequenti sulla gestione delle risorse
description: In questo argomento vengono illustrate le domande frequenti sulla gestione delle risorse.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079087"
---
# <a name="resource-management-faq"></a><span data-ttu-id="d5175-103">Domande frequenti sulla gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="d5175-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="d5175-104">Qual è la differenza tra un membro del team e un requisito di risorsa?</span><span class="sxs-lookup"><span data-stu-id="d5175-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="d5175-105">Un membro del team di progetto può essere assegnato ad attività, prenotato o sovraprenotato e impostato come revisore.</span><span class="sxs-lookup"><span data-stu-id="d5175-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="d5175-106">Un requisito di risorsa può esistere senza un membro del team di progetto, come bozza di nota della domanda.</span><span class="sxs-lookup"><span data-stu-id="d5175-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="d5175-107">Qual è la differenza tra ore proposte e ore prenotate provvisoriamente?</span><span class="sxs-lookup"><span data-stu-id="d5175-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="d5175-108">La differenza tra le ore proposte e le ore prenotate provvisoriamente è la visibilità.</span><span class="sxs-lookup"><span data-stu-id="d5175-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="d5175-109">Le ore proposte sono visibili solo ai responsabili delle risorse e al responsabile di progetto che ha avviato la domanda utilizzando una richiesta di risorse.</span><span class="sxs-lookup"><span data-stu-id="d5175-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="d5175-110">Le ore prenotate provvisoriamente sono visibili a tutti coloro che hanno accesso alla scheda di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d5175-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="d5175-111">Come è possibile visualizzare le ore prenotate provvisoriamente per le risorse in un team?</span><span class="sxs-lookup"><span data-stu-id="d5175-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="d5175-112">Le prenotazioni provvisorie possono essere eseguite quando si prenota un requisito di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d5175-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="d5175-113">Le risorse prenotate provvisoriamente in un team di progetto sono visualizzate come membri del team che hanno ore prenotate provvisoriamente.</span><span class="sxs-lookup"><span data-stu-id="d5175-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="d5175-114">Sono inoltre visualizzate anche nella scheda di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d5175-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="d5175-115">Come si modificano le ore richieste nonché le date di inizio e fine di una risorsa (generica o denominata) prenotata?</span><span class="sxs-lookup"><span data-stu-id="d5175-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="d5175-116">Dopo la prenotazione delle risorse, selezionare **Gestisci prenotazioni** per apportare le modifiche necessarie.</span><span class="sxs-lookup"><span data-stu-id="d5175-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="d5175-117">Quali sono i tipi di risorse supportati da Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="d5175-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="d5175-118">**Utente** e **Contatto** sono gli unici tipi di risorse supportati in Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d5175-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="d5175-119">Benché sia possibile creare altri tipi di risorse (ad esempio **Attrezzature** e **Gruppo** ), nessuno caso d'uso end-to-end è supportato per tali risorse.</span><span class="sxs-lookup"><span data-stu-id="d5175-119">Although you can create other types of resources (for example, **Equipment** and **Group** ), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="d5175-120">Qual è la differenza tra un'assegnazione e una prenotazione?</span><span class="sxs-lookup"><span data-stu-id="d5175-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="d5175-121">Le assegnazioni sono l'assegnazione di risorse alle attività di progetto nella pianificazione di progetto.</span><span class="sxs-lookup"><span data-stu-id="d5175-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="d5175-122">Le risorse possono essere reali o generiche.</span><span class="sxs-lookup"><span data-stu-id="d5175-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="d5175-123">Le prenotazioni sono l'allocazione provvisoria o definitiva delle risorse a un progetto.</span><span class="sxs-lookup"><span data-stu-id="d5175-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="d5175-124">Le prenotazioni definitive consumano la capacità di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="d5175-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="d5175-125">Idealmente, per le risorse reali, prenotazioni e assegnazioni dovrebbero corrispondere in quanto non differiscono.</span><span class="sxs-lookup"><span data-stu-id="d5175-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="d5175-126">Tuttavia, in PSA questa concordanza non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="d5175-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="d5175-127">La vista Riconciliazione mostra a un responsabile di progetto dove prenotazioni e assegnazioni non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="d5175-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
