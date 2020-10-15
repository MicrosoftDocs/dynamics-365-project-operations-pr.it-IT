---
title: Prenotazioni e assegnazioni
description: Questo argomento fornisce informazioni sulle differenze tra le prenotazioni delle risorse e le assegnazioni delle risorse.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896016"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="4c8ac-103">Prenotazioni e assegnazioni</span><span class="sxs-lookup"><span data-stu-id="4c8ac-103">Bookings vs assignments</span></span>

<span data-ttu-id="4c8ac-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="4c8ac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4c8ac-105">Le prenotazioni sono l'allocazione provvisoria o definitiva delle risorse a un progetto.</span><span class="sxs-lookup"><span data-stu-id="4c8ac-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="4c8ac-106">Le prenotazioni definitive consumano la capacità di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c8ac-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="4c8ac-107">Le assegnazioni sono l'assegnazione di risorse alle attività di progetto nella pianificazione di progetto.</span><span class="sxs-lookup"><span data-stu-id="4c8ac-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="4c8ac-108">Le risorse possono essere reali o generiche.</span><span class="sxs-lookup"><span data-stu-id="4c8ac-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="4c8ac-109">Idealmente, per le risorse reali, prenotazioni e assegnazioni dovrebbero corrispondere in quanto non differiscono.</span><span class="sxs-lookup"><span data-stu-id="4c8ac-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="4c8ac-110">Tuttavia, in Microsoft Dynamics Project Operations questa concordanza non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="4c8ac-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="4c8ac-111">La visualizzazione **Riconciliazione** mostra a un responsabile di progetto dove prenotazioni e assegnazioni non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="4c8ac-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
