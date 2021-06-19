---
title: Set di approvazioni
description: Questo argomento fornisce informazioni sul set di approvazioni, le richieste e i sottoinsiemi di tali operazioni.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116876"
---
# <a name="approval-sets"></a><span data-ttu-id="e3761-103">Set di approvazioni</span><span class="sxs-lookup"><span data-stu-id="e3761-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e3761-104">L'approvazione consente di configurare le richieste di approvazione in sottoinsiemi di operazioni più piccoli.</span><span class="sxs-lookup"><span data-stu-id="e3761-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="e3761-105">Questo raggruppamento consente di elaborare le approvazioni in ordine per Progetto e consente di ripristinare e mettere in sequenza.</span><span class="sxs-lookup"><span data-stu-id="e3761-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="e3761-106">Il raggruppamento migliora l'affidabilità e la tracciabilità del processo di approvazione per grandi volumi di approvazioni.</span><span class="sxs-lookup"><span data-stu-id="e3761-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="e3761-107">I set di approvazione indicano lo stato di elaborazione complessivo dei relativi record.</span><span class="sxs-lookup"><span data-stu-id="e3761-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="e3761-108">Quando un record di approvazione viene elaborato utilizzando un set di approvazione, il record si sposta da **Inviato** in **Approvato** e viene scollegato dal set di approvazioni.</span><span class="sxs-lookup"><span data-stu-id="e3761-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="e3761-109">Se un record restituisce un errore quando viene presentato per l'approvazione, il record rimane in uno stato di **Inviato** e il set di approvazione è contrassegnato come non riuscito.</span><span class="sxs-lookup"><span data-stu-id="e3761-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="e3761-110">Il set di approvazioni registra il messaggio dell'errore.</span><span class="sxs-lookup"><span data-stu-id="e3761-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="e3761-111">Elaborazione di approvazioni e set di approvazioni</span><span class="sxs-lookup"><span data-stu-id="e3761-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="e3761-112">Le approvazioni in coda per l'elaborazione sono visibili nella vista **Approvazioni in elaborazione**.</span><span class="sxs-lookup"><span data-stu-id="e3761-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="e3761-113">Il sistema tenta di elaborare tutte le voci più volte in modo asincrono, incluso un nuovo tentativo di approvazione se i tentativi precedenti non sono riusciti.</span><span class="sxs-lookup"><span data-stu-id="e3761-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="e3761-114">Il campo **Durata del set di approvazioni** registra il numero di tentativi rimasti per elaborare il set prima che venga contrassegnato come fallito.</span><span class="sxs-lookup"><span data-stu-id="e3761-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="e3761-115">Approvazioni non riuscite e set di approvazioni</span><span class="sxs-lookup"><span data-stu-id="e3761-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="e3761-116">La vista **Approvazioni non riuscite** elenca tutte le approvazioni che richiedono l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e3761-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="e3761-117">Apri i registri dei set di approvazioni associati per identificare la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="e3761-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="e3761-118">Se selezioni **Riprova** viene aggiunto al conteggio della durata del set di approvazioni, riporta il set di approvazioni allo stato **Elaborazione** e tenta di elaborare i record rimanenti.</span><span class="sxs-lookup"><span data-stu-id="e3761-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="e3761-119">Configurazione dei set di approvazione</span><span class="sxs-lookup"><span data-stu-id="e3761-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="e3761-120">Abilita la funzione Set di approvazioni</span><span class="sxs-lookup"><span data-stu-id="e3761-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="e3761-121">Prima di abilitare la funzione Set di approvazioni, verifica che non vi siano approvazioni in corso di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e3761-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="e3761-122">Vai alla pagina **Parametri progetto** e seleziona **Controllo funzionalità** > **Abilita approvazioni moderne**.</span><span class="sxs-lookup"><span data-stu-id="e3761-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="e3761-123">Disabilita la funzione Set di approvazioni</span><span class="sxs-lookup"><span data-stu-id="e3761-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="e3761-124">Prima di disabilitare la funzione Set di approvazioni, verifica che non vi siano approvazioni in corso di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e3761-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="e3761-125">Vai alla pagina **Parametri progetto** e seleziona **Controllo funzionalità** > **Disabilita approvazioni moderne**.</span><span class="sxs-lookup"><span data-stu-id="e3761-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="e3761-126">Configurazione della soglia asincrona</span><span class="sxs-lookup"><span data-stu-id="e3761-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="e3761-127">Quando vengono creati i set di approvazioni, l'elaborazione passa in background quando il numero selezionato di record per l'approvazione supera la soglia indicata.</span><span class="sxs-lookup"><span data-stu-id="e3761-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="e3761-128">Usa il campo **Soglia asincrona** per configurare quando l'elaborazione dell'approvazione deve essere eseguita in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="e3761-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="e3761-129">Valori validi:</span><span class="sxs-lookup"><span data-stu-id="e3761-129">Valid values are:</span></span>

  - <span data-ttu-id="e3761-130">Zero: tutte le richieste devono essere elaborate in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e3761-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="e3761-131">Numeri maggiori di zero: le approvazioni vengono elaborate in modo asincrono solo quando il numero di approvazioni inviato supera questo valore.</span><span class="sxs-lookup"><span data-stu-id="e3761-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
