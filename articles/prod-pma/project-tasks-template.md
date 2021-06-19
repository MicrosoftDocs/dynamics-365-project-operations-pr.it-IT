---
title: Sincronizzare le attività di progetto direttamente da Project Service Automation a Finance and Operations
description: Questo argomento descrive il modello e l'attività sottostante utilizzati per sincronizzare le attività del progetto direttamente da Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 16cd38f2f190414d7be9c93e8ab90d55006f47e1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009981"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="41604-103">Sincronizzare le attività di progetto direttamente da Project Service Automation a Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="41604-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="41604-104">Questo argomento descrive il modello e l'attività sottostante utilizzati per sincronizzare le attività del progetto direttamente da Dynamics 365 Project Service Automation a Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="41604-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="41604-105">L'integrazione delle attività di progetto, le categorie delle transazioni di spesa, le stime delle ore, le stime delle spese e il blocco delle funzionalità sono disponibili nella versione 8.0.</span><span class="sxs-lookup"><span data-stu-id="41604-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="41604-106">Se stai utilizzando Enterprise Edition 7.3.0 dopo aver installato KB 4132657 e KB 4132660, potrai utilizzare i modelli per integrare attività di progetto, categorie di transazioni di spesa, stime di ore, stime di spesa e valori effettivi e per configurare il blocco delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="41604-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="41604-107">Se devi reimpostare le distribuzioni contabili, è consigliabile installare anche KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="41604-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="41604-108">L'integrazione dei dati effettivi è disponibile nella versione 8.0.1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="41604-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="41604-109">Flusso di dati per Project Service Automation su Finance</span><span class="sxs-lookup"><span data-stu-id="41604-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="41604-110">La soluzione di integrazione da Project Service Automation a Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="41604-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="41604-111">Il modello di integrazione disponibile con la funzionalità Integrazione dati consente il flusso di dati sulle attività del progetto da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="41604-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="41604-112">La figura seguente mostra come i dati vengono sincronizzati tra Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="41604-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="41604-113">[![Flusso di dati per l'integrazione di Project Service Automation con Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="41604-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="41604-114">Modello e attività</span><span class="sxs-lookup"><span data-stu-id="41604-114">Template and task</span></span>

<span data-ttu-id="41604-115">Per accedere al modello, nell'interfaccia di amministrazione di Microsoft Power Apps, seleziona **Progetti**, quindi, nell'angolo in alto a destra, seleziona **Nuovo progetto** per selezionare modelli pubblici.</span><span class="sxs-lookup"><span data-stu-id="41604-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="41604-116">Il modello seguente e l'attività sottostante vengono utilizzati per sincronizzare le attività di progetto da Project Service Automation a Finance:</span><span class="sxs-lookup"><span data-stu-id="41604-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="41604-117">**Nome del modello in Integrazione dati:** attività di progetto (da PSA a Fin e Ops)</span><span class="sxs-lookup"><span data-stu-id="41604-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="41604-118">**Nome dell'attività nel progetto:** attività di progetto</span><span class="sxs-lookup"><span data-stu-id="41604-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="41604-119">Prima di sincronizzare le attività di progetto , è necessario sincronizzare i contratti di progetto e i progetti.</span><span class="sxs-lookup"><span data-stu-id="41604-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="41604-120">Set di entità</span><span class="sxs-lookup"><span data-stu-id="41604-120">Entity set</span></span>

| <span data-ttu-id="41604-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="41604-121">Project Service Automation</span></span> | <span data-ttu-id="41604-122">Finanza</span><span class="sxs-lookup"><span data-stu-id="41604-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="41604-123">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="41604-123">Project Tasks</span></span>              | <span data-ttu-id="41604-124">Entità di integrazione per attività di progetto</span><span class="sxs-lookup"><span data-stu-id="41604-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="41604-125">Flusso di entità</span><span class="sxs-lookup"><span data-stu-id="41604-125">Entity flow</span></span>

<span data-ttu-id="41604-126">Le attività di progetto vengono gestiti in Project Service Automation e vengono sincronizzate con Finance come impegni di progetto.</span><span class="sxs-lookup"><span data-stu-id="41604-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="41604-127">Configurazione di prerequisiti e mapping</span><span class="sxs-lookup"><span data-stu-id="41604-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="41604-128">Prima di sincronizzare le attività di progetto , è necessario sincronizzare i contratti di progetto e i progetti.</span><span class="sxs-lookup"><span data-stu-id="41604-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="41604-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="41604-129">Power Query</span></span>

<span data-ttu-id="41604-130">Devi utilizzare Microsoft Power Query per Excel per filtrare i dati se viene soddisfatta la seguente condizione:</span><span class="sxs-lookup"><span data-stu-id="41604-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="41604-131">Hai record specifici della risorsa in un'attività di progetto.</span><span class="sxs-lookup"><span data-stu-id="41604-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="41604-132">Se devi utilizzare Power Query, segui queste linee guida:</span><span class="sxs-lookup"><span data-stu-id="41604-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="41604-133">Il modello Attività di progetto (da PSA a Fin e Ops) ha un filtro predefinito che esclude i record specifici della risorsa da un'attività di progetto impostando il filtro di **IsLineTask** su **Falso**.</span><span class="sxs-lookup"><span data-stu-id="41604-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="41604-134">Se crei il tuo modello, devi aggiungere questo filtro.</span><span class="sxs-lookup"><span data-stu-id="41604-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="41604-135">Mapping dei modelli nell'integrazione dei dati</span><span class="sxs-lookup"><span data-stu-id="41604-135">Template mapping in Data integration</span></span>

<span data-ttu-id="41604-136">La figura seguente mostra un esempio dei mapping delle attività del modello in Integrazione dati.</span><span class="sxs-lookup"><span data-stu-id="41604-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="41604-137">Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="41604-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="41604-138">[![Mapping dei modelli](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="41604-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]