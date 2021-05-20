---
title: Prestazioni delle proposte di fatturazione progetto
description: Questo argomento fornisce informazioni sui miglioramenti delle prestazioni delle proposte di fatturazione progetto.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
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
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920307"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="2ea5d-103">Prestazioni delle proposte di fatturazione progetto</span><span class="sxs-lookup"><span data-stu-id="2ea5d-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ea5d-104">Quando crei una nuova proposta di fatturazione, potresti riscontrare problemi di prestazioni con l'aumento del numero di progetti e sottoprogetti.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="2ea5d-105">Per migliorare le prestazioni, è disponibile una funzione che riduce il tempo necessario per creare una nuova proposta di fatturazione per le transazioni di progetto registrate.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="2ea5d-106">Abilitare il miglioramento delle prestazioni delle proposte di fatturazione progetto</span><span class="sxs-lookup"><span data-stu-id="2ea5d-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="2ea5d-107">Per abilitare la funzionalità di miglioramento delle prestazioni delle proposte di fatturazione progetto, completa i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="2ea5d-108">Vai a **Gestione funzionalità** > **Tutte**.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="2ea5d-109">Nell'elenco delle funzionalità, individua **Miglioramento delle prestazioni delle proposte di fatturazione progetto**.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="2ea5d-110">Seleziona **Abilita ora**.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="2ea5d-111">Aggiorna il browser, quindi crea una nuova proposta di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="2ea5d-112">Disabilitare il miglioramento delle prestazioni delle proposte di fatturazione progetto</span><span class="sxs-lookup"><span data-stu-id="2ea5d-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="2ea5d-113">Per disabilitare la funzionalità di miglioramento delle prestazioni delle proposte di fatturazione progetto, completa i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="2ea5d-114">Vai a **Gestione funzionalità** > **Tutte**.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="2ea5d-115">Nell'elenco delle funzionalità, individua **Miglioramento delle prestazioni delle proposte di fatturazione progetto**.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="2ea5d-116">Seleziona **Disabilita**.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="2ea5d-117">Aggiorna il browser.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="2ea5d-118">Le prestazioni delle proposte di fatturazione non possono essere applicate quando le regole di fatturazione sono abilitate o sono in esecuzione processi batch.</span><span class="sxs-lookup"><span data-stu-id="2ea5d-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
