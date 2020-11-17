---
title: Prenotazioni e assegnazioni
description: Questo argomento fornisce informazioni sulle differenze tra le prenotazioni delle risorse e le assegnazioni delle risorse.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130223"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="5f006-103">Prenotazioni e assegnazioni</span><span class="sxs-lookup"><span data-stu-id="5f006-103">Bookings vs assignments</span></span>

<span data-ttu-id="5f006-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="5f006-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5f006-105">Le prenotazioni sono l'allocazione provvisoria o definitiva delle risorse a un progetto.</span><span class="sxs-lookup"><span data-stu-id="5f006-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="5f006-106">Le prenotazioni definitive consumano la capacità di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="5f006-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="5f006-107">Le prenotazioni rappresentano concetti organizzativi per i team per capire in che modo le risorse saranno impegnate nei vari progetti.</span><span class="sxs-lookup"><span data-stu-id="5f006-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="5f006-108">Dynamics 365 Project Operations considera le prenotazioni un concetto a livello di progetto.</span><span class="sxs-lookup"><span data-stu-id="5f006-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="5f006-109">Diversamente dalle prenotazioni, le assegnazioni sono l'impegno delle risorse per le attività di progetto nella pianificazione di progetto.</span><span class="sxs-lookup"><span data-stu-id="5f006-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="5f006-110">Le risorse possono essere denominate o generiche.</span><span class="sxs-lookup"><span data-stu-id="5f006-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="5f006-111">In genere, la somma delle prenotazioni per una risorsa sarà uguale alla somma delle assegnazioni della risorsa in una o più attività.</span><span class="sxs-lookup"><span data-stu-id="5f006-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="5f006-112">Tuttavia, in Project Operations questa concordanza non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="5f006-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="5f006-113">La vista **Riconciliazione** mostra a un responsabile di progetto dove prenotazioni e assegnazioni non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="5f006-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
