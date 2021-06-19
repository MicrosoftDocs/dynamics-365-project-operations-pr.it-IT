---
title: Prenotazioni e assegnazioni
description: Questo argomento fornisce informazioni sulle differenze tra le prenotazioni delle risorse e le assegnazioni delle risorse.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012771"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="20a9e-103">Prenotazioni e assegnazioni</span><span class="sxs-lookup"><span data-stu-id="20a9e-103">Bookings vs assignments</span></span>

<span data-ttu-id="20a9e-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="20a9e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="20a9e-105">Le prenotazioni sono l'allocazione provvisoria o definitiva delle risorse a un progetto.</span><span class="sxs-lookup"><span data-stu-id="20a9e-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="20a9e-106">Le prenotazioni definitive consumano la capacità di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="20a9e-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="20a9e-107">Le prenotazioni rappresentano concetti organizzativi per i team per capire in che modo le risorse saranno impegnate nei vari progetti.</span><span class="sxs-lookup"><span data-stu-id="20a9e-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="20a9e-108">Dynamics 365 Project Operations considera le prenotazioni un concetto a livello di progetto.</span><span class="sxs-lookup"><span data-stu-id="20a9e-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="20a9e-109">Diversamente dalle prenotazioni, le assegnazioni sono l'impegno delle risorse per le attività di progetto nella pianificazione di progetto.</span><span class="sxs-lookup"><span data-stu-id="20a9e-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="20a9e-110">Le risorse possono essere denominate o generiche.</span><span class="sxs-lookup"><span data-stu-id="20a9e-110">The resources can be named or generic.</span></span>  <span data-ttu-id="20a9e-111">Quando un requisito di risorsa viene ricavato dalle assegnazioni di attività del progetto, Project Operations utilizza i profili di lavoro dell'assegnazione delle risorse per creare i profili dei dettagli di requisito di risorsa.</span><span class="sxs-lookup"><span data-stu-id="20a9e-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="20a9e-112">Tuttavia, un riferimento alle assegnazioni di risorse non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="20a9e-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="20a9e-113">Gli aggiornamenti alle prenotazioni ricavate dal requisito di risorsa non aggiornano le assegnazioni delle risorse.</span><span class="sxs-lookup"><span data-stu-id="20a9e-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="20a9e-114">In genere, la somma delle prenotazioni per una risorsa sarà uguale alla somma delle assegnazioni della risorsa in una o più attività.</span><span class="sxs-lookup"><span data-stu-id="20a9e-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="20a9e-115">Tuttavia, in Project Operations questa concordanza non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="20a9e-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="20a9e-116">La vista **Riconciliazione** mostra a un responsabile di progetto dove prenotazioni e assegnazioni non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="20a9e-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]