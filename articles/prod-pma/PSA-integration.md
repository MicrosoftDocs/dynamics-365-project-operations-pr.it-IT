---
title: Panoramica di Project Service Automation
description: Questo argomento fornisce informazioni sulla soluzione di integrazione tra Dynamics 365 Project Service Automation e Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ca459b99881b612e4656be112c8a2e420b4196e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005886"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="778a5-103">Panoramica di Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="778a5-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="778a5-104">La soluzione di integrazione da Project Service Automation a Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Dynamics 365 Finance e Dynamics 365 Project Service Automation tramite Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="778a5-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="778a5-105">I modelli di integrazione disponibili con la funzionalità Integrazione dati consentono il flusso di progetti, contratti di progetto, voci di contratto di progetto, fasi delle voci di contratto di progetto, attività di progetto, categorie di transazione di spesa, stime delle ore e stime delle spese da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="778a5-106">Se utilizzi la versione 7.3.0, devi installare KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="778a5-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="778a5-107">Potrai quindi integrare progetti a prezzo fisso.</span><span class="sxs-lookup"><span data-stu-id="778a5-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="778a5-108">Se stai utilizzando la versione 7.3.0 e stai trasferendo le transazioni delle commissioni da Project Service Automation, devi installare KB 4345320 per includere tali commissioni nella fattura del progetto.</span><span class="sxs-lookup"><span data-stu-id="778a5-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="778a5-109">Se stai utilizzando la versione 8.0, sarai in grado di utilizzare l'integrazione delle attività di progetto, le categorie delle transazioni di spesa, le stime delle ore, le stime delle spese e il blocco delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="778a5-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="778a5-110">Se stai utilizzando la versione 8.0.1 o successiva, sarai in grado di sincronizzare i valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="778a5-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="778a5-111">Prima di poter integrare Project Service Automation Finance, è necessario configurare i parametri di integrazione di Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="778a5-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="778a5-112">Per altre informazioni, vedi [Parametri di integrazione di Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="778a5-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="778a5-113">Questa soluzione di integrazione consente la sincronizzazione diretta nei seguenti scenari:</span><span class="sxs-lookup"><span data-stu-id="778a5-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="778a5-114">Gestisci i contratti di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="778a5-115">Crea progetti in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="778a5-116">Gestisci le voci dei contratti di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="778a5-117">Gestisci le fasi delle voci dei contratti di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="778a5-118">Gestisci le attività di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="778a5-119">Gestisci le categorie delle transazioni di spesa in Finance e sincronizzale direttamente da Finance a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="778a5-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="778a5-120">Crea le stime delle ore di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="778a5-121">Crea le stime di spesa del progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="778a5-122">Creare i tempi, le spese e le commissioni effettive del progetto in Project Service Automation e crea transazioni di progetto nel giornale di registrazione dell'integrazione di Project Service Automation in modo che possano essere registrate in Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="778a5-123">Sincronizzazione dati</span><span class="sxs-lookup"><span data-stu-id="778a5-123">Data synchronization</span></span>

<span data-ttu-id="778a5-124">La figura seguente mostra come i dati vengono sincronizzati come parte dell'integrazione tra Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="778a5-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="778a5-125">Non tutti i modelli sono attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="778a5-125">Not all templates are currently available.</span></span> <span data-ttu-id="778a5-126">I modelli verranno rilasciati non appena saranno completati.</span><span class="sxs-lookup"><span data-stu-id="778a5-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="778a5-127">[![Integrazione di Project Service Automation con Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="778a5-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="778a5-128">Requisiti di sistema per Finance</span><span class="sxs-lookup"><span data-stu-id="778a5-128">System requirements for Finance</span></span>

<span data-ttu-id="778a5-129">Per utilizzare la soluzione di integrazione da Project Service Automation a Finance, è necessario installare Enterprise Edition 7.3 con Platform update 12 o successiva.</span><span class="sxs-lookup"><span data-stu-id="778a5-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="778a5-130">Requisiti di sistema per Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="778a5-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="778a5-131">Per utilizzare la soluzione di integrazione da Project Service Automation a Finance, è necessario installare i seguenti componenti:</span><span class="sxs-lookup"><span data-stu-id="778a5-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="778a5-132">Dynamics 365 Project Service Automation 9.0.0.0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="778a5-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="778a5-133">Soluzione da prospect a cassa per Dynamics 365 Sales, versione 1.14.0.0 (v14) o successiva</span><span class="sxs-lookup"><span data-stu-id="778a5-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="778a5-134">Soluzione da Project Service Automation a Finance per Dynamics 365 Project Service Automation versione 1.0.0.0 o successiva</span><span class="sxs-lookup"><span data-stu-id="778a5-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="778a5-135">Installa la soluzione di integrazione da Project Service Automation a Finance nell'istanza di Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="778a5-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="778a5-136">Scarica la soluzione di integrazione da Project Service Automation a Finance dal [Centro download Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) e segui le istruzioni incluse con la soluzione.</span><span class="sxs-lookup"><span data-stu-id="778a5-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]