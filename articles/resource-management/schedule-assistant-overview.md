---
title: Panoramica dell'assistente di pianificazione
description: Questo argomento fornisce informazioni su utilizzare l'assistente di pianificazione per prenotare le risorse.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078732"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="3100d-103">Panoramica dell'assistente di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3100d-103">Schedule assistant overview</span></span>

<span data-ttu-id="3100d-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="3100d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3100d-105">L'assistente di pianificazione viene utilizzato per prenotare le risorse in base ai requisiti definiti dal responsabile di progetto.</span><span class="sxs-lookup"><span data-stu-id="3100d-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="3100d-106">L'assistente di pianificazione si basa sui parametri forniti nel requisito di risorsa per trovare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3100d-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="3100d-107">L'assistente di pianificazione consiglia risorse che soddisfano i requisiti pertinenti, come finestre temporali o competenze necessarie.</span><span class="sxs-lookup"><span data-stu-id="3100d-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="3100d-108">Dopo aver identificato le risorse appropriate, il responsabile delle risorse o del progetto può prenotare la risorsa per il lavoro.</span><span class="sxs-lookup"><span data-stu-id="3100d-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3100d-109">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="3100d-109">Prerequisites</span></span>

<span data-ttu-id="3100d-110">L'assistente di pianificazione fa parte della soluzione Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="3100d-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="3100d-111">Questa soluzione è inclusa e installata con Dynamics 365 Project Operations, Dynamics 365 Field Service e Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="3100d-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="3100d-112">Requisiti e risorse corrispondenti</span><span class="sxs-lookup"><span data-stu-id="3100d-112">Matching requirements and resources</span></span>

<span data-ttu-id="3100d-113">Un requisito di risorsa generato si basa su dettagli quali:</span><span class="sxs-lookup"><span data-stu-id="3100d-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="3100d-114">Caratteristiche</span><span class="sxs-lookup"><span data-stu-id="3100d-114">Characteristics</span></span>
-   <span data-ttu-id="3100d-115">Ruoli</span><span class="sxs-lookup"><span data-stu-id="3100d-115">Roles</span></span>
-   <span data-ttu-id="3100d-116">Business Unit</span><span class="sxs-lookup"><span data-stu-id="3100d-116">Business units</span></span>
-   <span data-ttu-id="3100d-117">Preferenze di risorsa</span><span class="sxs-lookup"><span data-stu-id="3100d-117">Resource preferences</span></span>
-   <span data-ttu-id="3100d-118">Profili del lavoro richiesto</span><span class="sxs-lookup"><span data-stu-id="3100d-118">Effort contours</span></span>
-   <span data-ttu-id="3100d-119">Fuso orario</span><span class="sxs-lookup"><span data-stu-id="3100d-119">Time zone</span></span>

<span data-ttu-id="3100d-120">L'assistente di pianificazione utilizza questi dettagli per filtrare le risorse.</span><span class="sxs-lookup"><span data-stu-id="3100d-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="3100d-121">Avviare l'assistente di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3100d-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="3100d-122">Sono disponibili due modi per avviare l'assistente di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3100d-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="3100d-123">Se stai utilizzando la modalità ibrida, nella griglia dei membri del team puoi selezionare qualsiasi membro del team con un requisito di risorsa non soddisfatto e quindi selezionare **Prenota**.</span><span class="sxs-lookup"><span data-stu-id="3100d-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="3100d-124">Se stai utilizzando la modalità centrale, il responsabile delle risorse trova e seleziona la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3100d-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="3100d-125">Filtri dell'assistente di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3100d-125">Schedule assistant filters</span></span>

<span data-ttu-id="3100d-126">Dopo l'esecuzione dell'assistente di pianificazione, i dettagli del requisito di risorsa vengono visualizzati come valori filtrati nel riquadro di sinistra.</span><span class="sxs-lookup"><span data-stu-id="3100d-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="3100d-127">Il responsabile delle risorse o il responsabile del progetto possono ottimizzare i risultati regolando i filtri per soddisfare le esigenze di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3100d-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="3100d-128">Il riquadro dei filtri mostra le opzioni relative al lavoro, tra cui:</span><span class="sxs-lookup"><span data-stu-id="3100d-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="3100d-129">Inizio e fine lavoro</span><span class="sxs-lookup"><span data-stu-id="3100d-129">Work start and end</span></span>
-   <span data-ttu-id="3100d-130">Caratteristiche</span><span class="sxs-lookup"><span data-stu-id="3100d-130">Characteristics</span></span>
-   <span data-ttu-id="3100d-131">Ruoli</span><span class="sxs-lookup"><span data-stu-id="3100d-131">Roles</span></span>
-   <span data-ttu-id="3100d-132">Unità organizzative</span><span class="sxs-lookup"><span data-stu-id="3100d-132">Organizational units</span></span>
-   <span data-ttu-id="3100d-133">Società di gestione risorse</span><span class="sxs-lookup"><span data-stu-id="3100d-133">Resourcing company</span></span>
-   <span data-ttu-id="3100d-134">Tipi di risorsa</span><span class="sxs-lookup"><span data-stu-id="3100d-134">Resource types</span></span>
-   <span data-ttu-id="3100d-135">Risorse preferite</span><span class="sxs-lookup"><span data-stu-id="3100d-135">Preferred resources</span></span>
