---
title: Sincronizzare la capacità delle risorse
description: Questo argomento fornisce informazioni su come sincronizzare la capacità di una risorsa tra calendari e progetti.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997516"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="6e336-103">Sincronizzare la capacità delle risorse</span><span class="sxs-lookup"><span data-stu-id="6e336-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e336-104">I processi per la sincronizzazione delle risorse aiutano a garantire che le informazioni per il calendario e il calendario di base si riflettano nella pianificazione delle risorse del progetto.</span><span class="sxs-lookup"><span data-stu-id="6e336-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="6e336-105">Se il calendario viene modificato, i processi apportano gli aggiornamenti richiesti alla pianificazione delle risorse del progetto.</span><span class="sxs-lookup"><span data-stu-id="6e336-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="6e336-106">I processi aiutano anche a migliorare le prestazioni, perché le informazioni sulle risorse del calendario vengono sincronizzate in anticipo.</span><span class="sxs-lookup"><span data-stu-id="6e336-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="6e336-107">Pertanto, gli aggiornamenti alle informazioni sulla pianificazione delle risorse avvengono più rapidamente.</span><span class="sxs-lookup"><span data-stu-id="6e336-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="6e336-108">Si consiglia di pianificare i processi come batch anziché uno alla volta.</span><span class="sxs-lookup"><span data-stu-id="6e336-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="6e336-109">In caso contrario, c'è il rischio che qualcuno dimentichi le date incluse in cui le informazioni sono state sincronizzate l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="6e336-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="6e336-110">Se le date incluse non vengono utilizzate, possono verificarsi degli intervalli durante la sincronizzazione della data.</span><span class="sxs-lookup"><span data-stu-id="6e336-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sincronizzazione del calendario](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="6e336-112">Sincronizzare il rollup della capacità delle risorse</span><span class="sxs-lookup"><span data-stu-id="6e336-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="6e336-113">Il processo di sincronizzazione è progettato per sincronizzare tutte le informazioni del calendario delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6e336-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="6e336-114">Queste informazioni includono le informazioni del calendario di base su eventuali modifiche alla tabella della capacità del calendario delle risorse del progetto.</span><span class="sxs-lookup"><span data-stu-id="6e336-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="6e336-115">Se vengono aggiunte nuove risorse al progetto, la sincronizzazione aiuta a garantire che le informazioni di calendario aggiornate siano disponibili.</span><span class="sxs-lookup"><span data-stu-id="6e336-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="6e336-116">Questa sincronizzazione può essere eseguita in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="6e336-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="6e336-117">Si consiglia di utilizzare un batch.</span><span class="sxs-lookup"><span data-stu-id="6e336-117">We recommend that you use a batch.</span></span> <span data-ttu-id="6e336-118">Le opzioni sono disponibili durante la sincronizzazione delle prenotazioni della capacità.</span><span class="sxs-lookup"><span data-stu-id="6e336-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="6e336-119">Seleziona **Gestione progetti e contabilità** &gt; **Periodico** &gt; **Sincronizzazione capacità** &gt; **Sincronizza i roll-up della capacità delle risorse**.</span><span class="sxs-lookup"><span data-stu-id="6e336-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="6e336-120">Imposta le opzioni nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6e336-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="6e336-121">Opzione</span><span class="sxs-lookup"><span data-stu-id="6e336-121">Option</span></span>      | <span data-ttu-id="6e336-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e336-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="6e336-123">Codice periodo</span><span class="sxs-lookup"><span data-stu-id="6e336-123">Period code</span></span> | <span data-ttu-id="6e336-124">Facoltativamente, seleziona il codice intervallo data di contabilità generale per impostare le date di inizio e fine per il processo di sincronizzazione per i roll-up della capacità delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6e336-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="6e336-125">Data di inizio</span><span class="sxs-lookup"><span data-stu-id="6e336-125">Start date</span></span>  | <span data-ttu-id="6e336-126">Immetti la data di inizio per il processo di sincronizzazione per i roll-up della capacità delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6e336-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="6e336-127">Data di fine</span><span class="sxs-lookup"><span data-stu-id="6e336-127">End date</span></span>    | <span data-ttu-id="6e336-128">Immetti la data di fine per il processo di sincronizzazione per i roll-up della capacità delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6e336-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="6e336-129">[![Processo di sincronizzazione](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="6e336-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]