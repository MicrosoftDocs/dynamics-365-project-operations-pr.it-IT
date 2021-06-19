---
title: Prestazioni della pianificazione delle risorse di progetto
description: Questo argomento fornisce informazioni su come migliorare le prestazioni della pianificazione delle risorse per un gran numero di progetti.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010026"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="894f9-103">Prestazioni della pianificazione delle risorse di progetto</span><span class="sxs-lookup"><span data-stu-id="894f9-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="894f9-104">I problemi di prestazioni relativi alla pianificazione delle risorse possono verificarsi quando il numero di progetti raggiunge le migliaia.</span><span class="sxs-lookup"><span data-stu-id="894f9-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="894f9-105">Per migliorare le prestazioni della pianificazione delle risorse, è disponibile una funzione che consente agli utenti di ridurre il tempo necessario per aprire il modulo di disponibilità delle risorse.</span><span class="sxs-lookup"><span data-stu-id="894f9-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="894f9-106">In particolare, viene rimosso il processo di sincronizzazione di roll-up della capacità delle risorse e viene utilizzata la tabella **ResProjectResource** per velocizzare la ricerca delle risorse.</span><span class="sxs-lookup"><span data-stu-id="894f9-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="894f9-107">Nota che la tabella **ResRollup** non verrà più utilizzata.</span><span class="sxs-lookup"><span data-stu-id="894f9-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="894f9-108">Se esiste una dipendenza dal processo di sincronizzazione di roll-up della capacità delle risorse o dalla tabella **ResProjectResource**, non utilizzare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="894f9-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="894f9-109">Abilitare il miglioramento delle prestazioni della pianificazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="894f9-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="894f9-110">Per abilitare il miglioramento delle prestazioni della pianificazione delle risorse, completa i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="894f9-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="894f9-111">Vai a **Gestione funzionalità** > **Tutto** e nell'elenco delle funzionalità individua **Abilita la funzione di miglioramento delle prestazioni della pianificazione delle risorse di progetto**.</span><span class="sxs-lookup"><span data-stu-id="894f9-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="894f9-112">Seleziona **Abilita ora**.</span><span class="sxs-lookup"><span data-stu-id="894f9-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="894f9-113">Se non riesci a trovare la funzione nell'elenco, seleziona **Controlla aggiornamenti** per aggiornare l'elenco.</span><span class="sxs-lookup"><span data-stu-id="894f9-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="894f9-114">Aggiorna il browser, quindi vai a **Gestione progetti e contabilità** > **Periodico** > **Risorse di progetto** > **Sincronizza la capacità dei calendari delle risorse in tutte le società**.</span><span class="sxs-lookup"><span data-stu-id="894f9-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="894f9-115">Imposta **Rimuovi record di capacità esistenti** su **Sì** per rimuovere i dati precedenti.</span><span class="sxs-lookup"><span data-stu-id="894f9-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="894f9-116">Se desideri generare dati incrementali, imposta su **No**.</span><span class="sxs-lookup"><span data-stu-id="894f9-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="894f9-117">Nel campo **Codice periodo** seleziona il periodo in cui generare i dati.</span><span class="sxs-lookup"><span data-stu-id="894f9-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="894f9-118">Se selezioni un codice periodo, non è necessario definire una data di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="894f9-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="894f9-119">Se lasci il campo **Codice periodo** vuoto, seleziona le date di inizio e fine specifiche per generare i dati.</span><span class="sxs-lookup"><span data-stu-id="894f9-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="894f9-120">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="894f9-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="894f9-121">Verranno distribuiti i dati generali della tabella **ResCalendarCapacity** in tutte le società nel tuo ambiente, quindi il processo batch deve essere eseguito solo in una persona giuridica.</span><span class="sxs-lookup"><span data-stu-id="894f9-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="894f9-122">I dati in questo processo batch sono necessari per calcolare la capacità delle risorse tramite il calendario associato.</span><span class="sxs-lookup"><span data-stu-id="894f9-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="894f9-123">Vai a **Gestione progetti e contabilità** > **Periodico** > **Risorse di progetto** > **Popola risorse di progetto in tutte le società** e poi seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="894f9-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="894f9-124">Questo è lo script di aggiornamento dei dati per i dati generali nelle tabelle **ResProjectResource**, **ResCalendarDateTimeRange** e **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="894f9-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="894f9-125">Anche i valori per il campo **PSAPRojSchedRole.RootActivity** vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="894f9-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="894f9-126">Se lo script non viene eseguito, riceverai un avviso quando proverai a eseguire le operazioni di pianificazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="894f9-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="894f9-127">Disattivare il miglioramento delle prestazioni della pianificazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="894f9-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="894f9-128">Vai a **Gestione funzionalità** > **Tutto** e cerca **Abilita la funzione di miglioramento delle prestazioni della pianificazione delle risorse di progetto**.</span><span class="sxs-lookup"><span data-stu-id="894f9-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="894f9-129">Seleziona la funzione, quindi seleziona il pulsante **Disabilita**.</span><span class="sxs-lookup"><span data-stu-id="894f9-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="894f9-130">Aggiorna il browser.</span><span class="sxs-lookup"><span data-stu-id="894f9-130">Refresh your browser.</span></span>
4. <span data-ttu-id="894f9-131">Vai a **Gestione progetti e contabilità** > **Periodico** > **Sincronizzazione capacità** > **Sincronizza i roll-up della capacità delle risorse**.</span><span class="sxs-lookup"><span data-stu-id="894f9-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="894f9-132">Nella pagina **Sincronizzazione roll-up della capacità** imposta **Rimuovi record di capacità esistenti** su **Sì** per rimuovere i dati precedenti.</span><span class="sxs-lookup"><span data-stu-id="894f9-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="894f9-133">Se desideri generare dati incrementali, imposta su **No**.</span><span class="sxs-lookup"><span data-stu-id="894f9-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="894f9-134">Nel campo **Codice periodo** seleziona il periodo in cui generare i dati.</span><span class="sxs-lookup"><span data-stu-id="894f9-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="894f9-135">Se selezioni un codice periodo, non è necessario definire una data di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="894f9-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="894f9-136">Se lasci il campo **Codice periodo** vuoto, seleziona le date di inizio e fine specifiche per generare i dati.</span><span class="sxs-lookup"><span data-stu-id="894f9-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="894f9-137">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="894f9-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="894f9-138">Verranno distribuiti i dati generali della tabella **ResRollup** in tutte le società nel tuo ambiente, quindi il processo batch deve essere eseguito solo in una persona giuridica.</span><span class="sxs-lookup"><span data-stu-id="894f9-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="894f9-139">Questo processo batch è necessario per tutte le visualizzazioni **Disponibilità delle risorse**.</span><span class="sxs-lookup"><span data-stu-id="894f9-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="894f9-140">Se questo processo batch non viene eseguito, i dati **ResRollup** verranno generati istantaneamente, il che può richiedere tempo.</span><span class="sxs-lookup"><span data-stu-id="894f9-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]