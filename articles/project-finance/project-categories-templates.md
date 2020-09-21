---
title: Sincronizzare le categorie di spesa del progetto tra Finance and Operations e Project Service Automation
description: Questo argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare le categorie di spesa del progetto tra Microsoft Dynamics 365 Finance e Dynamics 365 Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 7dd914dc-1913-45eb-8a67-e897b00089fa
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 757fe1dbc804b986fc3334ebae7254a3f0491f59
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752674"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="a98cc-103">Sincronizzare le categorie di spesa del progetto tra Finance and Operations e Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a98cc-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a98cc-104">Questo argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare le categorie di spesa del progetto tra Dynamics 365 Finance e Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a98cc-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="a98cc-105">L'integrazione delle attività di progetto, le categorie delle transazioni di spesa, le stime delle ore, le stime delle spese e il blocco delle funzionalità sono disponibili nella versione 8.0.</span><span class="sxs-lookup"><span data-stu-id="a98cc-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="a98cc-106">L'integrazione dei dati effettivi è disponibile nella versione 8.0.1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a98cc-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="a98cc-107">Se stai utilizzando Enterprise Edition 7.3.0 dopo aver installato KB 4132657 e KB 4132660, potrai utilizzare i modelli per integrare attività di progetto, categorie di transazioni di spesa, stime di ore, stime di spesa e valori effettivi e per configurare il blocco delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a98cc-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="a98cc-108">Se devi reimpostare le distribuzioni contabili, è consigliabile installare anche KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="a98cc-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="a98cc-109">Flusso di dati per Project Service Automation e Finance</span><span class="sxs-lookup"><span data-stu-id="a98cc-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="a98cc-110">La soluzione di integrazione tra Project Service Automation e Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="a98cc-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="a98cc-111">I modelli di integrazione disponibili con la funzionalità Integrazione dati consentono il flusso di dati sulle categorie di transazione di spesa del progetto tra Finance e Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a98cc-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="a98cc-112">Se le categorie di spesa del progetto vengono gestite in Finance, il flusso di integrazione viene prima da Finance a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a98cc-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="a98cc-113">Gli ID integrazione delle categorie di spesa del progetto vengono quindi aggiornati tramite la sincronizzazione da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="a98cc-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a98cc-114">Se le categorie di spesa del progetto vengono gestite in Project Service Automation, il flusso di integrazione viene prima da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="a98cc-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="a98cc-115">Le categorie di progetto devono essere già configurate in Finance prima della sincronizzazione da Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a98cc-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="a98cc-116">Quindi sincronizza di nuovo da Finance a Project Service Automation e quindi da Project Service Automation di nuovo a Finance.</span><span class="sxs-lookup"><span data-stu-id="a98cc-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="a98cc-117">In questo modo, contribuisci a garantire che le categorie siano collegate e che non vengano creati duplicati.</span><span class="sxs-lookup"><span data-stu-id="a98cc-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="a98cc-118">In genere, le categorie di spesa del progetto vengono gestite in Finance.</span><span class="sxs-lookup"><span data-stu-id="a98cc-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="a98cc-119">Tuttavia, se non lo sono o se le categorie di spesa sono già state create in Project Service Automation, è necessario prima sincronizzare utilizzando il modello Categorie di transazione di spesa del progetto (da PSA a Fin e Ops).</span><span class="sxs-lookup"><span data-stu-id="a98cc-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="a98cc-120">Quindi sincronizza utilizzando il modello delle categorie di transazioni di spesa del progetto (Da Fin e Ops a PSA).</span><span class="sxs-lookup"><span data-stu-id="a98cc-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="a98cc-121">È consiglibile quindi eseguire ancora una volta la sincronizzazione da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="a98cc-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="a98cc-122">Se esegui la sincronizzazione prima da Project Service Automation, è necessario soddisfare i seguenti requisiti in Finance prima di eseguire la sincronizzazione:</span><span class="sxs-lookup"><span data-stu-id="a98cc-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="a98cc-123">La categoria condivisa che corrisponde alla categoria di progetto configurata in Project Service Automation deve esistere e deve essere abilitata per entrambi **Progetto** e **Spesa**.</span><span class="sxs-lookup"><span data-stu-id="a98cc-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="a98cc-124">Per ogni persona giuridica Finance con cui deve essere effettuata l'integrazione, devono esistere le seguenti categorie di progetto:</span><span class="sxs-lookup"><span data-stu-id="a98cc-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="a98cc-125">**Categoria progetto** esiste.</span><span class="sxs-lookup"><span data-stu-id="a98cc-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="a98cc-126">**Usa in Gestione spese** è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a98cc-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="a98cc-127">**Attivo nella giornale di registrazione** è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a98cc-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="a98cc-128">**Tipo di transazione** è impostata su **Gerstione spese**.</span><span class="sxs-lookup"><span data-stu-id="a98cc-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="a98cc-129">La figura seguente mostra come i dati vengono sincronizzati tra Project Service Automation e Finance.</span><span class="sxs-lookup"><span data-stu-id="a98cc-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="a98cc-130">[![Flusso di dati per l'integrazione di Project Service Automation con Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a98cc-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="a98cc-131">Sincronizzazione delle categorie di spesa del progetto tra Finance e Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a98cc-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="a98cc-132">Modello e attività</span><span class="sxs-lookup"><span data-stu-id="a98cc-132">Template and task</span></span>

<span data-ttu-id="a98cc-133">Per accedere al modello, nell'interfaccia di amministrazione di Microsoft Power Apps, seleziona **Progetti**, quindi, nell'angolo in alto a destra, seleziona **Nuovo progetto** per selezionare modelli pubblici.</span><span class="sxs-lookup"><span data-stu-id="a98cc-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a98cc-134">Il modello seguente e l'attività sottostante vengono utilizzati per sincronizzare le categorie di spesa del progetto da Finance a Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="a98cc-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="a98cc-135">**Nome del modello in Integrazione dati:** categorie di transazioni di spesa del progetto (da Fin e Ops a PSA)</span><span class="sxs-lookup"><span data-stu-id="a98cc-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="a98cc-136">**Nome dell'attività nel progetto:** sincronizza le categorie con PSA</span><span class="sxs-lookup"><span data-stu-id="a98cc-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="a98cc-137">Set di entità</span><span class="sxs-lookup"><span data-stu-id="a98cc-137">Entity set</span></span>

| <span data-ttu-id="a98cc-138">Finanza</span><span class="sxs-lookup"><span data-stu-id="a98cc-138">Finance</span></span>                           | <span data-ttu-id="a98cc-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a98cc-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="a98cc-140">Entità di integrazione per le categorie</span><span class="sxs-lookup"><span data-stu-id="a98cc-140">Integration entity for categories</span></span> | <span data-ttu-id="a98cc-141">Categorie di transazioni</span><span class="sxs-lookup"><span data-stu-id="a98cc-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="a98cc-142">Flusso di entità</span><span class="sxs-lookup"><span data-stu-id="a98cc-142">Entity flow</span></span>

<span data-ttu-id="a98cc-143">Le categorie di spesa del progetto vengono gestite in Finance e vengono sincronizzate con Project Service Automation come categorie di transazioni.</span><span class="sxs-lookup"><span data-stu-id="a98cc-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a98cc-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="a98cc-144">Power Query</span></span>

<span data-ttu-id="a98cc-145">Quando esegui la sincronizzazione con Project Service Automation, devi utilizzare Microsoft Power Query per Excel per impostare il tipo di fatturazione nella categoria della transazione.</span><span class="sxs-lookup"><span data-stu-id="a98cc-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="a98cc-146">Il modello delle categorie di transazioni di spesa del progetto (da Fin e Ops a PSA) fornisce una colonna e una mappatura predefinite.</span><span class="sxs-lookup"><span data-stu-id="a98cc-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="a98cc-147">Se crei il tuo modello, devi aggiungere una colonna aggiuntiva in Power Query.</span><span class="sxs-lookup"><span data-stu-id="a98cc-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="a98cc-148">Effettuare i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a98cc-148">Follow these steps.</span></span>

1. <span data-ttu-id="a98cc-149">Fai clic sulla freccia per aprire il mapping dell'attività delle categorie di spesa del progetto nel modello Categorie delle transazioni di spesa del progetto (da Fin e Ops a PSA).</span><span class="sxs-lookup"><span data-stu-id="a98cc-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="a98cc-150">Fai clic sul collegamento **Filtro e query avanzati** per aprire Power Query.</span><span class="sxs-lookup"><span data-stu-id="a98cc-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="a98cc-151">Seleziona **Aggiungi colonna condizionale**.</span><span class="sxs-lookup"><span data-stu-id="a98cc-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="a98cc-152">Immetti un nome per la nuova colonna, ad esempio **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="a98cc-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="a98cc-153">Immetti la seguente condizione: **Se CATEGORYID non è uguale a Null, allora 19235001, altrimenti null**.</span><span class="sxs-lookup"><span data-stu-id="a98cc-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="a98cc-154">Fai clic su **OK** nella colonna.</span><span class="sxs-lookup"><span data-stu-id="a98cc-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="a98cc-155">Assicurati di mappare questa nuova colonna nella pagina di mapping.</span><span class="sxs-lookup"><span data-stu-id="a98cc-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="a98cc-156">La figura seguente mostra un esempio del mapping delle attività del modello in Integrazione dati.</span><span class="sxs-lookup"><span data-stu-id="a98cc-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="a98cc-157">Il mapping mostra le informazioni sui campi che verranno sincronizzate da Finance a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a98cc-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="a98cc-158">[![Mapping dei modelli](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a98cc-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="a98cc-159">Sincronizzazione delle categorie di spesa del progetto tra Project Service Automation e Finance</span><span class="sxs-lookup"><span data-stu-id="a98cc-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="a98cc-160">Modello e attività</span><span class="sxs-lookup"><span data-stu-id="a98cc-160">Template and task</span></span>

<span data-ttu-id="a98cc-161">Il modello seguente e l'attività sottostante vengono utilizzati per sincronizzare le categorie di spesa del progetto da Project Service Automation a Finance:</span><span class="sxs-lookup"><span data-stu-id="a98cc-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a98cc-162">**Nome del modello in Integrazione dati:** categorie di transazioni di spesa del progetto (da PSA a Fin e Ops)</span><span class="sxs-lookup"><span data-stu-id="a98cc-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a98cc-163">**Nome dell'attività nel progetto:** sincronizza le categorie con Fin Ops</span><span class="sxs-lookup"><span data-stu-id="a98cc-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="a98cc-164">Set di entità</span><span class="sxs-lookup"><span data-stu-id="a98cc-164">Entity set</span></span>

| <span data-ttu-id="a98cc-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a98cc-165">Project Service Automation</span></span> | <span data-ttu-id="a98cc-166">Finanza</span><span class="sxs-lookup"><span data-stu-id="a98cc-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="a98cc-167">Categorie di transazioni</span><span class="sxs-lookup"><span data-stu-id="a98cc-167">Transaction categories</span></span>     | <span data-ttu-id="a98cc-168">Entità di integrazione per le categorie</span><span class="sxs-lookup"><span data-stu-id="a98cc-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="a98cc-169">Flusso di entità</span><span class="sxs-lookup"><span data-stu-id="a98cc-169">Entity flow</span></span>

<span data-ttu-id="a98cc-170">Le categorie di spesa del progetto vengono gestite in Finance e vengono sincronizzate con Project Service Automation come categorie di transazioni.</span><span class="sxs-lookup"><span data-stu-id="a98cc-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="a98cc-171">La sincronizzazione con gli aggiornamenti di Finance aggiorna la categoria di progetto in Finance con l'ID integrazione da Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a98cc-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a98cc-172">Mapping dei modelli nell'integrazione dei dati</span><span class="sxs-lookup"><span data-stu-id="a98cc-172">Template mapping in Data integration</span></span>

<span data-ttu-id="a98cc-173">La figura seguente mostra un esempio del mapping delle attività del modello in Integrazione dati.</span><span class="sxs-lookup"><span data-stu-id="a98cc-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="a98cc-174">Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="a98cc-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a98cc-175">[![Mapping dei modelli](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a98cc-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
