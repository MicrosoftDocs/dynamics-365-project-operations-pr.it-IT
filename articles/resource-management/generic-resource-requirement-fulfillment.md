---
title: Soddisfare i requisiti generici delle risorse
description: In questo argomento vengono fornite informazioni sulla prenotazione di risorse denominate per un requisito di risorsa generica.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897591"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="40a16-103">Soddisfare i requisiti generici delle risorse</span><span class="sxs-lookup"><span data-stu-id="40a16-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="40a16-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="40a16-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="40a16-105">Puoi prenotare una risorsa denominata per sostituire una risorsa generica che ha un requisito di risorsa.</span><span class="sxs-lookup"><span data-stu-id="40a16-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="40a16-106">Nella pagina **Progetti**, seleziona la scheda **Team**.</span><span class="sxs-lookup"><span data-stu-id="40a16-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="40a16-107">Seleziona la risorsa generica che ha un requisito di risorsa nell'elenco e seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="40a16-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="40a16-108">Oppure apri il requisito di risorsa e seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="40a16-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="40a16-109">Nella pagina **Assistente di pianificazione**, seleziona una risorsa denominata per prenotarla per il team di progetto e seleziona **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="40a16-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="40a16-110">Al termine della prenotazione di una risorsa denominata, questa sostituisce la risorsa generica.</span><span class="sxs-lookup"><span data-stu-id="40a16-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="40a16-111">Anche le assegnazioni nella pianificazione vengono aggiornate con la risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="40a16-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="40a16-112">Soddisfare un requisito di risorsa generica con molteplici risorse denominate</span><span class="sxs-lookup"><span data-stu-id="40a16-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="40a16-113">Soddisfare un requisito di risorsa generica con molteplici risorse denominate è simile ad assegnare una singola risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="40a16-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="40a16-114">Ad esempio, supponiamo di avere un'attività di una durata di cinque giorni con 120 ore di lavoro richiesto.</span><span class="sxs-lookup"><span data-stu-id="40a16-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="40a16-115">Questa attività non può essere completata da una risorsa che ha un orario di lavoro tipico di otto ore al giorno per cinque giorni alla settimana.</span><span class="sxs-lookup"><span data-stu-id="40a16-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="40a16-116">Il requisito è di 120 ore di ingegneria robotica durante cinque giorni, ovvero 24 ore al giorno.</span><span class="sxs-lookup"><span data-stu-id="40a16-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="40a16-117">Questo è un esempio di quando più risorse denominate sono necessarie per soddisfare una richiesta di risorse generiche.</span><span class="sxs-lookup"><span data-stu-id="40a16-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="40a16-118">Devi quindi prenotare più risorse per soddisfare il requisito.</span><span class="sxs-lookup"><span data-stu-id="40a16-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="40a16-119">La differenza principale in questo scenario è che la risorsa generica rimane nel team assegnato all'attività e i membri del team di risorse denominate prenotate non sono assegnati come parte della posizione.</span><span class="sxs-lookup"><span data-stu-id="40a16-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="40a16-120">Il responsabile di progetto può assegnare il lavoro come appropriato alle risorse denominate.</span><span class="sxs-lookup"><span data-stu-id="40a16-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="40a16-121">La vista **Riconciliazione** può consentire a un responsabile di progetto di suddividere le prenotazioni tra molteplici risorse per le assegnazioni delle attività.</span><span class="sxs-lookup"><span data-stu-id="40a16-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="40a16-122">Questa operazione non viene eseguita automaticamente in quanto negli scenari più complessi, come nel caso in cui il requisito è costituito da un gruppo di attività, il sistema deve supporre l'intenzione con la quale il responsabile di progetto desidera eseguire le assegnazioni.</span><span class="sxs-lookup"><span data-stu-id="40a16-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="40a16-123">Poiché il sistema non può comprendere l'intenzione, è probabile che quanto supposto sia differente da quanto previsto e quindi si avrà un risultato incorretto o imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="40a16-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="40a16-124">Il risultato prevedibile è che la risorsa generica rimane assegnata fino a che il responsabile di progetto non crea deliberatamente assegnazioni mediante la vista **Riconciliazione**.</span><span class="sxs-lookup"><span data-stu-id="40a16-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


