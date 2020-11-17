---
title: Panoramica delle modalità di gestione delle risorse
description: Questo argomento fornisce informazioni sulla funzionalità Gestione delle risorse in Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118523"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="4a7f2-103">Panoramica delle modalità di gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="4a7f2-103">Resource management modes overview</span></span>

<span data-ttu-id="4a7f2-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="4a7f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4a7f2-105">Dynamics 365 Project Operations supporta due modalità per eseguire il flusso di prenotazione complessivo.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="4a7f2-106">La modalità di gestione è definita come un parametro del progetto e può essere modificata se le esigenze aziendali cambiano.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="4a7f2-107">Modalità centrale</span><span class="sxs-lookup"><span data-stu-id="4a7f2-107">Central mode</span></span>
<span data-ttu-id="4a7f2-108">Per le organizzazioni che centralizzano l'allocazione delle risorse ai progetti, la modalità centrale fornisce un modo per garantire che i responsabili di progetto possano definire i requisiti di risorsa a livello di progetto.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="4a7f2-109">L'evasione dei requisiti di risorsa è delegato a un responsabile delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="4a7f2-110">I responsabili di progetto possono accettare o rifiutare le risorse proposte dal responsabile delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Modalità centrale](./media/resource-management-central.png)

<span data-ttu-id="4a7f2-112">Per gestire le risorse con la modalità centrale, vedi:</span><span class="sxs-lookup"><span data-stu-id="4a7f2-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="4a7f2-113">Assegnare risorse prenotabili generiche a un'attività e generare requisiti di risorsa</span><span class="sxs-lookup"><span data-stu-id="4a7f2-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="4a7f2-114">Prenotare risorse denominate da requisiti di risorsa</span><span class="sxs-lookup"><span data-stu-id="4a7f2-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="4a7f2-115">Inviare una richiesta di risorsa</span><span class="sxs-lookup"><span data-stu-id="4a7f2-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="4a7f2-116">Soddisfare una richiesta di risorse</span><span class="sxs-lookup"><span data-stu-id="4a7f2-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="4a7f2-117">Accettare o rifiutare una risorsa di progetto proposta da una richiesta di risorsa</span><span class="sxs-lookup"><span data-stu-id="4a7f2-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="4a7f2-118">Modalità ibrida</span><span class="sxs-lookup"><span data-stu-id="4a7f2-118">Hybrid mode</span></span>
<span data-ttu-id="4a7f2-119">Per le organizzazioni che richiedono flessibilità nell'allocazione delle risorse, la modalità ibrida consente sia ai responsabili di progetto che ai responsabili delle risorse di prenotare le risorse.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Modalità ibrida](./media/resource-management-hybrid.png)

<span data-ttu-id="4a7f2-121">Oltre al processo in modalità centrale supportato, vedi i seguenti argomenti per gestire tutti gli altri flussi di prenotazione supportati in modalità ibrida:</span><span class="sxs-lookup"><span data-stu-id="4a7f2-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="4a7f2-122">Prenota una risorsa direttamente per un progetto:</span><span class="sxs-lookup"><span data-stu-id="4a7f2-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="4a7f2-123">Prenotare risorse prenotabili denominate per un team di progetto e assegnarvi attività</span><span class="sxs-lookup"><span data-stu-id="4a7f2-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="4a7f2-124">Prenota una risorsa da un requisito di risorsa:</span><span class="sxs-lookup"><span data-stu-id="4a7f2-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="4a7f2-125">Assegnare risorse prenotabili generiche a un'attività e generare requisiti di risorsa</span><span class="sxs-lookup"><span data-stu-id="4a7f2-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="4a7f2-126">Prenotare risorse denominate da requisiti di risorsa</span><span class="sxs-lookup"><span data-stu-id="4a7f2-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
