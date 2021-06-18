---
title: Sincronizzare le stime del progetto direttamente da Project Service Automation a Finance and Operations
description: Questo argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare le stime delle ore di progetto e le stime delle spese del progetto direttamente da Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
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
ms.openlocfilehash: a6955dcd1ebe494e0171c30ac4384089da6a8745
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999721"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="8ab11-103">Sincronizzare le stime del progetto direttamente da Project Service Automation a Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8ab11-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8ab11-104">Questo argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare le stime delle ore di progetto e le stime delle spese del progetto direttamente da Dynamics 365 Project Service Automation a Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8ab11-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="8ab11-105">L'integrazione delle attività di progetto, le categorie delle transazioni di spesa, le stime delle ore, le stime delle spese e il blocco delle funzionalità sono disponibili nella versione 8.0.</span><span class="sxs-lookup"><span data-stu-id="8ab11-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="8ab11-106">L'integrazione dei dati effettivi è disponibile nella versione 8.0.1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="8ab11-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="8ab11-107">Flusso di dati per Project Service Automation su Finance</span><span class="sxs-lookup"><span data-stu-id="8ab11-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="8ab11-108">La soluzione di integrazione da Project Service Automation a Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="8ab11-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="8ab11-109">I modelli di integrazione disponibili con la funzionalità Integrazione dati consentono il flusso di dati sulle stime delle ore di progetto e delle spese del progetto da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="8ab11-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="8ab11-110">La figura seguente mostra come i dati vengono sincronizzati tra Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="8ab11-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="8ab11-111">[![Flusso di dati per l'integrazione di Project Service Automation con Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="8ab11-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="8ab11-112">Stime delle ore di progetto</span><span class="sxs-lookup"><span data-stu-id="8ab11-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="8ab11-113">Modelli e attività</span><span class="sxs-lookup"><span data-stu-id="8ab11-113">Template and tasks</span></span>

<span data-ttu-id="8ab11-114">Per accedere ai modelli disponibili, nell'interfaccia di amministrazione di Microsoft Power Apps, seleziona **Progetti**, quindi, nell'angolo in alto a destra, seleziona **Nuovo progetto** per selezionare modelli pubblici.</span><span class="sxs-lookup"><span data-stu-id="8ab11-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="8ab11-115">Il modello seguente e le attività sottostanti vengono utilizzati per sincronizzare le stime delle ore di progetto da Project Service Automation a Finance:</span><span class="sxs-lookup"><span data-stu-id="8ab11-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="8ab11-116">**Nome del modello in Integrazione dati:** stime delle ore di progetto (da PSA a Fin e Ops)</span><span class="sxs-lookup"><span data-stu-id="8ab11-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="8ab11-117">**Nome delle attività nel progetto:**</span><span class="sxs-lookup"><span data-stu-id="8ab11-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="8ab11-118">Relazioni transazione</span><span class="sxs-lookup"><span data-stu-id="8ab11-118">Transaction relationships</span></span>
    - <span data-ttu-id="8ab11-119">Stime di spesa</span><span class="sxs-lookup"><span data-stu-id="8ab11-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="8ab11-120">Set di entità</span><span class="sxs-lookup"><span data-stu-id="8ab11-120">Entity set</span></span>

| <span data-ttu-id="8ab11-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8ab11-121">Project Service Automation</span></span> | <span data-ttu-id="8ab11-122">Finanza</span><span class="sxs-lookup"><span data-stu-id="8ab11-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="8ab11-123">Attività di progetto</span><span class="sxs-lookup"><span data-stu-id="8ab11-123">Project tasks</span></span>              | <span data-ttu-id="8ab11-124">Entità di integrazione per le stime delle ore di progetto</span><span class="sxs-lookup"><span data-stu-id="8ab11-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="8ab11-125">Flusso di entità</span><span class="sxs-lookup"><span data-stu-id="8ab11-125">Entity flow</span></span>

<span data-ttu-id="8ab11-126">Le stime delle ore di progetto vengono gestite in Project Service Automation e vengono sincronizzate con Finance come previsioni delle ore di progetto.</span><span class="sxs-lookup"><span data-stu-id="8ab11-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8ab11-127">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8ab11-127">Prerequisites</span></span>

<span data-ttu-id="8ab11-128">Prima di poter sincronizzare le stime delle ore di progetto, è necessario sincronizzare i progetti, le attività di progetto e le categorie di transazioni di spesa del progetto.</span><span class="sxs-lookup"><span data-stu-id="8ab11-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="8ab11-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="8ab11-129">Power Query</span></span>

<span data-ttu-id="8ab11-130">Nel modello delle stime delle ore di progetto, è necessario utilizzare Microsoft Power Query per Excel per completare queste attività:</span><span class="sxs-lookup"><span data-stu-id="8ab11-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="8ab11-131">Impostare l'ID modello di previsione predefinito che verrà utilizzato quando l'integrazione crea nuove previsioni orarie.</span><span class="sxs-lookup"><span data-stu-id="8ab11-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="8ab11-132">Filtrare tutti i record specifici della risorsa nell'attività che non riusciranno a integrare le previsioni orarie.</span><span class="sxs-lookup"><span data-stu-id="8ab11-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="8ab11-133">Filtrare tutte le righe di categorie di transazioni vuote.</span><span class="sxs-lookup"><span data-stu-id="8ab11-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="8ab11-134">Il mancato completamento di questa attività potrebbe causare previsioni orarie errate.</span><span class="sxs-lookup"><span data-stu-id="8ab11-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="8ab11-135">Impostare l'ID modello di previsione predefinito</span><span class="sxs-lookup"><span data-stu-id="8ab11-135">Set the default forecast model ID</span></span>

<span data-ttu-id="8ab11-136">Per aggiornare l'ID modello di previsione predefinito nel modello, fai clic sula freccia **Mappa** per aprire il mapping.</span><span class="sxs-lookup"><span data-stu-id="8ab11-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="8ab11-137">Quindi seleziona il collegamento **Filtro e query avanzati**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="8ab11-138">Se stai utilizzando il modello di stima delle ore di progetto predefinito (da PSA a Fin e Ops), seleziona **Condizione inserita** nell'elenco di **Passaggi applicati**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="8ab11-139">Nella voce **Funzione**, sostituisci **O\_previsione** con il nome dell'ID del modello di previsione da utilizzare con l'integrazione.</span><span class="sxs-lookup"><span data-stu-id="8ab11-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="8ab11-140">Il modello predefinito ha un ID modello di previsione dai dati demo.</span><span class="sxs-lookup"><span data-stu-id="8ab11-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="8ab11-141">Se stai creando un nuovo modello, devi aggiungere questa colonna.</span><span class="sxs-lookup"><span data-stu-id="8ab11-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="8ab11-142">In Power Query, seleziona **Aggiungi colonna condizionale** e inserisci un nome per la nuova colonna, ad esempio **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="8ab11-143">Immetti la condizione per la colonna, dove, se Project task è null, quindi \<enter the forecast model ID\>; in caso contrario null.</span><span class="sxs-lookup"><span data-stu-id="8ab11-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="8ab11-144">Filtrare i record specifici delle risorse</span><span class="sxs-lookup"><span data-stu-id="8ab11-144">Filter out resource-specific records</span></span>

<span data-ttu-id="8ab11-145">Il modello Stime delle ore di progetto (da PSA a Fin e Ops) ha un filtro predefinito che rimuove tutti i record specifici della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ab11-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="8ab11-146">Se crei il tuo modello, devi aggiungere questo filtro.</span><span class="sxs-lookup"><span data-stu-id="8ab11-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="8ab11-147">Seleziona il collegamento **Filtro e query avanzati** per filtrare la colonna **msdyn\_islinetask** in modo che solo i record **Falso** siano inclusi.</span><span class="sxs-lookup"><span data-stu-id="8ab11-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="8ab11-148">Filtrare le righe di categorie di transazioni vuote</span><span class="sxs-lookup"><span data-stu-id="8ab11-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="8ab11-149">Devi aggiungere un filtro per rimuovere tutte le righe con categorie di transazioni vuote.</span><span class="sxs-lookup"><span data-stu-id="8ab11-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="8ab11-150">Questa attività è obbligatoria, indipendentemente dal fatto che tu stia utilizzando il modello predefinito o creando il tuo modello.</span><span class="sxs-lookup"><span data-stu-id="8ab11-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="8ab11-151">Questo filtro rimuove le righe di riepilogo da Project Service Automation che potrebbero causare errori nelle previsioni orarie in Finance.</span><span class="sxs-lookup"><span data-stu-id="8ab11-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="8ab11-152">Seleziona il collegamento **Filtro e query avanzati** per filtrare i record Null nella colonna **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8ab11-153">Mapping dei modelli nell'integrazione dei dati</span><span class="sxs-lookup"><span data-stu-id="8ab11-153">Template mapping in Data integration</span></span>

<span data-ttu-id="8ab11-154">La figura seguente mostra un esempio del mapping delle attività del modello in Integrazione dati.</span><span class="sxs-lookup"><span data-stu-id="8ab11-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="8ab11-155">Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="8ab11-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="8ab11-156">[![Mapping dei modelli di attività nell'integrazione dei dati](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ab11-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="8ab11-157">Stime di spesa del progetto</span><span class="sxs-lookup"><span data-stu-id="8ab11-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="8ab11-158">Modelli e attività</span><span class="sxs-lookup"><span data-stu-id="8ab11-158">Template and tasks</span></span>

<span data-ttu-id="8ab11-159">Il modello seguente e le attività sottostanti vengono utilizzati per sincronizzare le stime di spesa del progetto da Project Service Automation a Finance:</span><span class="sxs-lookup"><span data-stu-id="8ab11-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="8ab11-160">**Nome del modello in Integrazione dati:** stime di spesa del progetto (da PSA a Fin e Ops)</span><span class="sxs-lookup"><span data-stu-id="8ab11-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="8ab11-161">**Nome delle attività nel progetto:**</span><span class="sxs-lookup"><span data-stu-id="8ab11-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="8ab11-162">Relazioni transazione</span><span class="sxs-lookup"><span data-stu-id="8ab11-162">Transaction relationships</span></span> 
    - <span data-ttu-id="8ab11-163">Stime di spesa</span><span class="sxs-lookup"><span data-stu-id="8ab11-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="8ab11-164">Set di entità</span><span class="sxs-lookup"><span data-stu-id="8ab11-164">Entity set</span></span>

| <span data-ttu-id="8ab11-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8ab11-165">Project Service Automation</span></span> | <span data-ttu-id="8ab11-166">Finanza</span><span class="sxs-lookup"><span data-stu-id="8ab11-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="8ab11-167">Connessioni delle transazioni</span><span class="sxs-lookup"><span data-stu-id="8ab11-167">Transaction Connections</span></span>    | <span data-ttu-id="8ab11-168">Entità di integrazione per le relazioni di transazione del progetto</span><span class="sxs-lookup"><span data-stu-id="8ab11-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="8ab11-169">Righe di stima</span><span class="sxs-lookup"><span data-stu-id="8ab11-169">Estimate Lines</span></span>             | <span data-ttu-id="8ab11-170">Entità di integrazione per le stime di spesa del progetto</span><span class="sxs-lookup"><span data-stu-id="8ab11-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="8ab11-171">Flusso di entità</span><span class="sxs-lookup"><span data-stu-id="8ab11-171">Entity flow</span></span>

<span data-ttu-id="8ab11-172">Le stime di spesa del progetto vengono gestite in Project Service Automation e vengono sincronizzate con Finance come previsioni di spesa del progetto.</span><span class="sxs-lookup"><span data-stu-id="8ab11-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8ab11-173">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8ab11-173">Prerequisites</span></span>

<span data-ttu-id="8ab11-174">Prima di poter sincronizzare le stime di spesa del progetto, è necessario sincronizzare i progetti, le attività di progetto e le categorie di transazioni di spesa del progetto.</span><span class="sxs-lookup"><span data-stu-id="8ab11-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="8ab11-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="8ab11-175">Power Query</span></span>

<span data-ttu-id="8ab11-176">Nel modello delle stime di spesa del progetto, è necessario utilizzare Power Query per Excel per completare le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ab11-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="8ab11-177">Filtra per includere solo i record di riga di stima di spesa.</span><span class="sxs-lookup"><span data-stu-id="8ab11-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="8ab11-178">Impostare l'ID modello di previsione predefinito che verrà utilizzato quando l'integrazione crea nuove previsioni orarie.</span><span class="sxs-lookup"><span data-stu-id="8ab11-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="8ab11-179">Trasforma i tipi di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="8ab11-179">Transform the billing types.</span></span>
- <span data-ttu-id="8ab11-180">Trasforma i tipi di transazione.</span><span class="sxs-lookup"><span data-stu-id="8ab11-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="8ab11-181">Filtrare per includere solo le righe di stima di spesa</span><span class="sxs-lookup"><span data-stu-id="8ab11-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="8ab11-182">Il modello Stime di spesa del progetto (da PSA a Fin e Ops) ha un filtro predefinito che include solo le righe di spesa nell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="8ab11-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="8ab11-183">Se crei il tuo modello, devi aggiungere questo filtro.</span><span class="sxs-lookup"><span data-stu-id="8ab11-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="8ab11-184">Seleziona l'attività **Relazioni transazione**, quindi fai clic sulla freccia **Mapping** per aprire il mapping.</span><span class="sxs-lookup"><span data-stu-id="8ab11-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="8ab11-185">Seleziona il collegamento **Filtro e query avanzati**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="8ab11-186">Filtra la colonna **msdyn\_transactiontype1** in modo da includere solo **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="8ab11-187">Impostare l'ID modello di previsione predefinito</span><span class="sxs-lookup"><span data-stu-id="8ab11-187">Set the default forecast model ID</span></span>

<span data-ttu-id="8ab11-188">Per aggiornare l'ID modello di previsione predefinito nel modello, seleziona l'attività **Stime di spesa**, quindi fai clic sula freccia **Mappa** per aprire il mapping.</span><span class="sxs-lookup"><span data-stu-id="8ab11-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="8ab11-189">Seleziona il collegamento **Filtro e query avanzati**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="8ab11-190">Se stai utilizzando il modello di stima di spesa di progetto predefinito (da PSA a Fin e Ops), in Power Query seleziona la prima **Condizione inserita** dalla sezione **Passaggi applicati**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="8ab11-191">Nella voce **Funzione**, sostituisci **O\_previsione** con il nome dell'ID del modello di previsione da utilizzare con l'integrazione.</span><span class="sxs-lookup"><span data-stu-id="8ab11-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="8ab11-192">Il modello predefinito ha un ID modello di previsione dai dati demo.</span><span class="sxs-lookup"><span data-stu-id="8ab11-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="8ab11-193">Se stai creando un nuovo modello, devi aggiungere questa colonna.</span><span class="sxs-lookup"><span data-stu-id="8ab11-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="8ab11-194">In Power Query, seleziona **Aggiungi colonna condizionale** e inserisci un nome per la nuova colonna, ad esempio **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="8ab11-195">Immetti la condizione per la colonna, dove, se ID riga di stima è null, quindi \<enter the forecast model ID\>; in caso contrario null.</span><span class="sxs-lookup"><span data-stu-id="8ab11-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="8ab11-196">Trasformare i tipi di fatturazione</span><span class="sxs-lookup"><span data-stu-id="8ab11-196">Transform the billing types</span></span>

<span data-ttu-id="8ab11-197">Il modello Stime di spesa del progetto (da PSA a Fin e Ops) include una colonna condizionale utilizzata per trasformare i tipi di fatturazione ricevuti da Project Service Automation durante l'integrazione.</span><span class="sxs-lookup"><span data-stu-id="8ab11-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="8ab11-198">Se crei il tuo modello, devi aggiungere questa colonna condizionale.</span><span class="sxs-lookup"><span data-stu-id="8ab11-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="8ab11-199">Seleziona il collegamento **Filtro e query avanzati**, quindi seleziona **Aggiungi colonna condizionale**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="8ab11-200">Immetti un nome per la nuova colonna, ad esempio **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="8ab11-201">Quindi, immetti la condizione seguente:</span><span class="sxs-lookup"><span data-stu-id="8ab11-201">Then enter the following condition:</span></span>

<span data-ttu-id="8ab11-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="8ab11-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="8ab11-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="8ab11-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="8ab11-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="8ab11-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="8ab11-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="8ab11-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="8ab11-206">Trasformare i tipi di transazione</span><span class="sxs-lookup"><span data-stu-id="8ab11-206">Transform the transaction types</span></span>

<span data-ttu-id="8ab11-207">Il modello Stime di spesa del progetto (da PSA a Fin e Ops) include una colonna condizionale utilizzata per trasformare i tipi di transazione ricevuti da Project Service Automation durante l'integrazione.</span><span class="sxs-lookup"><span data-stu-id="8ab11-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="8ab11-208">Se crei il tuo modello, devi aggiungere questa colonna condizionale.</span><span class="sxs-lookup"><span data-stu-id="8ab11-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="8ab11-209">Seleziona il collegamento **Filtro e query avanzati**, quindi seleziona **Aggiungi colonna condizionale**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="8ab11-210">Immetti un nome per la nuova colonna, ad esempio **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="8ab11-211">Quindi, immetti la condizione seguente:</span><span class="sxs-lookup"><span data-stu-id="8ab11-211">Then enter the following condition:</span></span>

<span data-ttu-id="8ab11-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="8ab11-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="8ab11-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="8ab11-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="8ab11-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="8ab11-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8ab11-215">Mapping dei modelli nell'integrazione dei dati</span><span class="sxs-lookup"><span data-stu-id="8ab11-215">Template mapping in Data integration</span></span>

<span data-ttu-id="8ab11-216">La figura seguente mostra esempi di mapping delle attività del modello in Integrazione dati.</span><span class="sxs-lookup"><span data-stu-id="8ab11-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="8ab11-217">Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="8ab11-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="8ab11-218">[![Mappatura del modello delle transazioni di stima di spesa](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ab11-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="8ab11-219">[![Mappatura del modello delle stime di spesa](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ab11-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]