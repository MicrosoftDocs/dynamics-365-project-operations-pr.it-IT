---
title: Prestazioni delle proposte di fatturazione progetto
description: Questo argomento fornisce informazioni sui miglioramenti delle prestazioni delle proposte di fatturazione progetto.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573564"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="c5cd8-103">Prestazioni delle proposte di fatturazione progetto</span><span class="sxs-lookup"><span data-stu-id="c5cd8-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c5cd8-104">Quando crei una nuova proposta di fatturazione, potresti riscontrare problemi di prestazioni con l'aumento del numero di progetti e sottoprogetti.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="c5cd8-105">Per migliorare le prestazioni, è disponibile una funzione che riduce il tempo necessario per creare una nuova proposta di fatturazione per le transazioni di progetto registrate.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="c5cd8-106">Abilitare il miglioramento delle prestazioni delle proposte di fatturazione progetto</span><span class="sxs-lookup"><span data-stu-id="c5cd8-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="c5cd8-107">Per abilitare la funzionalità di miglioramento delle prestazioni delle proposte di fatturazione progetto, completa i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="c5cd8-108">Vai a **Gestione funzionalità** > **Tutte**.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="c5cd8-109">Nell'elenco delle funzionalità, individua **Miglioramento delle prestazioni delle proposte di fatturazione progetto**.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="c5cd8-110">Seleziona **Abilita ora**.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="c5cd8-111">Aggiorna il browser, quindi crea una nuova proposta di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="c5cd8-112">Disabilitare il miglioramento delle prestazioni delle proposte di fatturazione progetto</span><span class="sxs-lookup"><span data-stu-id="c5cd8-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="c5cd8-113">Per disabilitare la funzionalità di miglioramento delle prestazioni delle proposte di fatturazione progetto, completa i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="c5cd8-114">Vai a **Gestione funzionalità** > **Tutte**.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="c5cd8-115">Nell'elenco delle funzionalità, individua **Miglioramento delle prestazioni delle proposte di fatturazione progetto**.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="c5cd8-116">Seleziona **Disabilita**.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="c5cd8-117">Aggiorna il browser.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="c5cd8-118">Le prestazioni delle proposte di fatturazione non possono essere applicate quando le regole di fatturazione sono abilitate o sono in esecuzione processi batch.</span><span class="sxs-lookup"><span data-stu-id="c5cd8-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
