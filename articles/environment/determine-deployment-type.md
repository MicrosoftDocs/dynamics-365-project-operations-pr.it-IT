---
title: Determinare il tipo di distribuzione
description: Questo argomento fornisce informazioni per determina il tipo di distribuzione di Project Operations giusto per la tua azienda.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401223"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="a30ff-103">Determinare il tipo di distribuzione</span><span class="sxs-lookup"><span data-stu-id="a30ff-103">Determine your deployment type</span></span>

<span data-ttu-id="a30ff-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="a30ff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a30ff-105">Dopo aver acquistato la licenza, inizia qui per determinare il miglior modello di distribuzione di Dynamics 365 Project Operations utilizzando il [flusso di installazione guidata](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a30ff-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="a30ff-106">Dopo aver completato il flusso di installazione guidata, verrai indirizzato al portale di gestione corretto per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a30ff-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="a30ff-107">Vedi i dettagli di distribuzione per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a30ff-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="a30ff-108">Clienti esistenti di Dynamics che utilizzano Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a30ff-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="a30ff-109">Project Operations include le funzionalità fornite con Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a30ff-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="a30ff-110">Un percorso di aggiornamento verrà rilasciato per questi clienti nel primo ciclo di rilascio del 2021.</span><span class="sxs-lookup"><span data-stu-id="a30ff-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="a30ff-111">Clienti esistenti di Dynamics 365 Finance che utilizzando Gestione progetti e contabilità</span><span class="sxs-lookup"><span data-stu-id="a30ff-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="a30ff-112">I clienti esistenti di Finance che utilizzano la funzionalità Gestione progetti e contabilità possono continuare a utilizzarlo così com'è.</span><span class="sxs-lookup"><span data-stu-id="a30ff-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="a30ff-113">Vedi [Project Operations per scenari di materiali stoccati/ordini di produzione](#pma).</span><span class="sxs-lookup"><span data-stu-id="a30ff-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="a30ff-114">Tipi di distribuzione</span><span class="sxs-lookup"><span data-stu-id="a30ff-114">Deployment types</span></span>
<span data-ttu-id="a30ff-115">Project Operations supporta più opzioni di distribuzione per soddisfare le tue esigenze.</span><span class="sxs-lookup"><span data-stu-id="a30ff-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="a30ff-116">Che tu sia un cliente Dynamics 365 nuovo o esistente, Project Operations può supportare le tue esigenze.</span><span class="sxs-lookup"><span data-stu-id="a30ff-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="a30ff-117">Il nostro [Questionario sulla distribuzione](https://aka.ms/provisionprojectoperations) ti aiuterà a determinare la giusta distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a30ff-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="a30ff-118">I risultati ti guideranno verso uno dei seguenti tipi di distribuzione:</span><span class="sxs-lookup"><span data-stu-id="a30ff-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="a30ff-119">Distribuzione semplice: dalla transazione alla fatturazione proforma</span><span class="sxs-lookup"><span data-stu-id="a30ff-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="a30ff-120">Project Operations per scenari di risorse/materiali non stoccati</span><span class="sxs-lookup"><span data-stu-id="a30ff-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="a30ff-121">Project Operations per scenari di materiali stoccati/ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="a30ff-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="a30ff-122">Project Operations supporta scenari di materiali stoccati/ordini di produzione e scenari basati su risorse/materiali non stoccati nello stesso ambiente tramite configurazioni a livello di persona giuridica.</span><span class="sxs-lookup"><span data-stu-id="a30ff-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="a30ff-123">Ad esempio, Contoso può utilizzare le funzionalità di materiali stoccati/ordini di produzione nel proprio stabilimento di produzione negli Stati Uniti (persona giuridica = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="a30ff-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="a30ff-124">Contoso può utilizzare le funzionalità basate su risorse/materiali non stoccati nella struttura di assistenza Contoso Robotics Arms nel Regno Unito (persona giuridica = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="a30ff-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="a30ff-125">Distribuzione semplice: dalla transazione alla fatturazione proforma</span><span class="sxs-lookup"><span data-stu-id="a30ff-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="a30ff-126">La distribuzione semplice include le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="a30ff-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="a30ff-127">Processo di vendita per progetti che estendono le esperienze delle applicazioni Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a30ff-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="a30ff-128">Pianificazione del progetto utilizzando Microsoft Project per il Web</span><span class="sxs-lookup"><span data-stu-id="a30ff-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a30ff-129">Determinazione dei prezzi multidimensionale</span><span class="sxs-lookup"><span data-stu-id="a30ff-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a30ff-130">Gestione delle risorse unificata</span><span class="sxs-lookup"><span data-stu-id="a30ff-130">Unified resource management</span></span>
- <span data-ttu-id="a30ff-131">Registrazione del tempo</span><span class="sxs-lookup"><span data-stu-id="a30ff-131">Time tracking</span></span>
- <span data-ttu-id="a30ff-132">Spesa di base</span><span class="sxs-lookup"><span data-stu-id="a30ff-132">Basic expense</span></span>
- <span data-ttu-id="a30ff-133">Fatturazione proforma e per il cliente</span><span class="sxs-lookup"><span data-stu-id="a30ff-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="a30ff-134">Passaggi per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="a30ff-134">Deployment steps</span></span>
<span data-ttu-id="a30ff-135">Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a30ff-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a30ff-136">Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](lite-preview-subscription-sign-up.md) e [Eseguire il provisioning di un nuovo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="a30ff-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="a30ff-137">Project Operations per scenari di risorse/materiali non stoccati</span><span class="sxs-lookup"><span data-stu-id="a30ff-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="a30ff-138">Project Operations per scenari di risorse/materiali non stoccati includono le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="a30ff-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="a30ff-139">Processo di vendita per progetti che estendono l'applicazione Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a30ff-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="a30ff-140">Pianificazione del progetto utilizzando Microsoft Project per il Web</span><span class="sxs-lookup"><span data-stu-id="a30ff-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a30ff-141">Determinazione dei prezzi multidimensionale</span><span class="sxs-lookup"><span data-stu-id="a30ff-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a30ff-142">Gestione delle risorse unificata</span><span class="sxs-lookup"><span data-stu-id="a30ff-142">Unified resource management</span></span>
- <span data-ttu-id="a30ff-143">Registrazione del tempo</span><span class="sxs-lookup"><span data-stu-id="a30ff-143">Time tracking</span></span>
- <span data-ttu-id="a30ff-144">Spesa di base</span><span class="sxs-lookup"><span data-stu-id="a30ff-144">Basic expense</span></span>
- <span data-ttu-id="a30ff-145">Spesa completa</span><span class="sxs-lookup"><span data-stu-id="a30ff-145">Full expense</span></span>
- <span data-ttu-id="a30ff-146">OCR ricevuta</span><span class="sxs-lookup"><span data-stu-id="a30ff-146">Receipt OCR</span></span>
- <span data-ttu-id="a30ff-147">Fatturazione proforma e per il cliente</span><span class="sxs-lookup"><span data-stu-id="a30ff-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="a30ff-148">Riconoscimento dei ricavi per progetti</span><span class="sxs-lookup"><span data-stu-id="a30ff-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="a30ff-149">Passaggi per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="a30ff-149">Deployment steps</span></span>
<span data-ttu-id="a30ff-150">Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a30ff-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a30ff-151">Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](resource-sign-up-preview-subscription.md) e [Eseguire il provisioning di un nuovo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a30ff-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="a30ff-152">Project Operations per scenari di materiali stoccati/ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="a30ff-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="a30ff-153">Pianificazione di un progetto tramite la struttura di suddivisione del lavoro</span><span class="sxs-lookup"><span data-stu-id="a30ff-153">Project planning using WBS</span></span>
- <span data-ttu-id="a30ff-154">Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="a30ff-154">Resource Management</span></span>
- <span data-ttu-id="a30ff-155">Registrazione del tempo</span><span class="sxs-lookup"><span data-stu-id="a30ff-155">Time Tracking</span></span>
- <span data-ttu-id="a30ff-156">Spesa completa</span><span class="sxs-lookup"><span data-stu-id="a30ff-156">Full Expense</span></span>
- <span data-ttu-id="a30ff-157">OCR ricevuta</span><span class="sxs-lookup"><span data-stu-id="a30ff-157">Receipt OCR</span></span>
- <span data-ttu-id="a30ff-158">Fattura completa</span><span class="sxs-lookup"><span data-stu-id="a30ff-158">Full Invoicing</span></span>
- <span data-ttu-id="a30ff-159">Riconoscimento ricavi</span><span class="sxs-lookup"><span data-stu-id="a30ff-159">Revenue Recognition</span></span>
- <span data-ttu-id="a30ff-160">Ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="a30ff-160">Production Orders</span></span>
- <span data-ttu-id="a30ff-161">Supporto materiali</span><span class="sxs-lookup"><span data-stu-id="a30ff-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="a30ff-162">Passaggi per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="a30ff-162">Deployment steps</span></span>
<span data-ttu-id="a30ff-163">Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a30ff-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a30ff-164">Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Eseguire il provisioning di un nuovo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="a30ff-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

