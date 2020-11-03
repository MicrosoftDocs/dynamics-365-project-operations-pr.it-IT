---
title: Determinare il tipo di distribuzione
description: Questo argomento fornisce informazioni per determina il tipo di distribuzione di Project Operations giusto per la tua azienda.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078880"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="7cb0e-103">Determinare il tipo di distribuzione</span><span class="sxs-lookup"><span data-stu-id="7cb0e-103">Determine your deployment type</span></span>

<span data-ttu-id="7cb0e-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="7cb0e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7cb0e-105">Dopo aver acquistato la licenza, inizia qui per determinare il miglior modello di distribuzione di Dynamics 365 Project Operations utilizzando il [flusso di installazione guidata](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="7cb0e-106">Dopo aver completato il flusso di installazione guidata, verrai indirizzato al portale di gestione corretto per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="7cb0e-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="7cb0e-107">Vedi i dettagli di distribuzione per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="7cb0e-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="7cb0e-108">Clienti esistenti di Dynamics che utilizzano Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7cb0e-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="7cb0e-109">Project Operations include le funzionalità fornite con Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7cb0e-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="7cb0e-110">In futuro verrà rilasciato un percorso di aggiornamento per questi clienti.</span><span class="sxs-lookup"><span data-stu-id="7cb0e-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="7cb0e-111">Clienti esistenti di Dynamics 365 Finance che utilizzando Gestione progetti e contabilità</span><span class="sxs-lookup"><span data-stu-id="7cb0e-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="7cb0e-112">I clienti esistenti di Finance che utilizzano la funzionalità Gestione progetti e contabilità possono continuare a utilizzarla così com'è.</span><span class="sxs-lookup"><span data-stu-id="7cb0e-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="7cb0e-113">Vedi [Project Operations per scenari di materiali stoccati/ordini di produzione](#pma).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="7cb0e-114">Tipi di distribuzione</span><span class="sxs-lookup"><span data-stu-id="7cb0e-114">Deployment types</span></span>
<span data-ttu-id="7cb0e-115">Project Operations supporta più opzioni di distribuzione per soddisfare le tue esigenze.</span><span class="sxs-lookup"><span data-stu-id="7cb0e-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="7cb0e-116">Che tu sia un cliente Dynamics 365 nuovo o esistente, Project Operations può supportare le tue esigenze.</span><span class="sxs-lookup"><span data-stu-id="7cb0e-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="7cb0e-117">Il nostro [Questionario sulla distribuzione](https://aka.ms/provisionprojectoperations) ti aiuterà a determinare la giusta distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7cb0e-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="7cb0e-118">I risultati ti guideranno verso uno dei seguenti tipi di distribuzione:</span><span class="sxs-lookup"><span data-stu-id="7cb0e-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="7cb0e-119">Distribuzione semplice: dalla transazione alla fatturazione proforma</span><span class="sxs-lookup"><span data-stu-id="7cb0e-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="7cb0e-120">Project Operations per scenari di risorse/materiali non stoccati</span><span class="sxs-lookup"><span data-stu-id="7cb0e-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="7cb0e-121">Project Operations per scenari di materiali stoccati/ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="7cb0e-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="7cb0e-122">Project Operations supporta scenari di materiali stoccati/ordini di produzione e scenari basati su risorse/materiali non stoccati nello stesso ambiente tramite configurazioni a livello di persona giuridica.</span><span class="sxs-lookup"><span data-stu-id="7cb0e-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="7cb0e-123">Ad esempio, Contoso può utilizzare le funzionalità di materiali stoccati/ordini di produzione nel proprio stabilimento di produzione negli Stati Uniti (persona giuridica = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="7cb0e-124">Contoso può utilizzare le funzionalità basate su risorse/materiali non stoccati nella struttura di assistenza Contoso Robotics Arms nel Regno Unito (persona giuridica = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="7cb0e-125">Distribuzione semplice: dalla transazione alla fatturazione proforma</span><span class="sxs-lookup"><span data-stu-id="7cb0e-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="7cb0e-126">La distribuzione semplice include le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="7cb0e-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="7cb0e-127">Pianificazione del progetto utilizzando Microsoft Project per il Web</span><span class="sxs-lookup"><span data-stu-id="7cb0e-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7cb0e-128">Determinazione dei prezzi multidimensionale</span><span class="sxs-lookup"><span data-stu-id="7cb0e-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7cb0e-129">Gestione delle risorse unificata</span><span class="sxs-lookup"><span data-stu-id="7cb0e-129">Unified Resource Management</span></span>
- <span data-ttu-id="7cb0e-130">Registrazione del tempo</span><span class="sxs-lookup"><span data-stu-id="7cb0e-130">Time Tracking</span></span>
- <span data-ttu-id="7cb0e-131">Spesa di base</span><span class="sxs-lookup"><span data-stu-id="7cb0e-131">Basic Expense</span></span>
- <span data-ttu-id="7cb0e-132">Proposta di fattura</span><span class="sxs-lookup"><span data-stu-id="7cb0e-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7cb0e-133">Passaggi per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="7cb0e-133">Deployment steps</span></span>
<span data-ttu-id="7cb0e-134">Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7cb0e-135">Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](lite-preview-subscription-sign-up.md) e [Eseguire il provisioning di un nuovo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="7cb0e-136">Project Operations per scenari di risorse/materiali non stoccati</span><span class="sxs-lookup"><span data-stu-id="7cb0e-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="7cb0e-137">Project Operations per scenari di risorse/materiali non stoccati includono le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="7cb0e-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="7cb0e-138">Pianificazione del progetto utilizzando Microsoft Project per il Web</span><span class="sxs-lookup"><span data-stu-id="7cb0e-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7cb0e-139">Determinazione dei prezzi multidimensionale</span><span class="sxs-lookup"><span data-stu-id="7cb0e-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7cb0e-140">Gestione delle risorse unificata</span><span class="sxs-lookup"><span data-stu-id="7cb0e-140">Unified Resource Management</span></span>
- <span data-ttu-id="7cb0e-141">Registrazione del tempo</span><span class="sxs-lookup"><span data-stu-id="7cb0e-141">Time Tracking</span></span>
- <span data-ttu-id="7cb0e-142">Spesa di base</span><span class="sxs-lookup"><span data-stu-id="7cb0e-142">Basic Expense</span></span>
- <span data-ttu-id="7cb0e-143">Spesa completa</span><span class="sxs-lookup"><span data-stu-id="7cb0e-143">Full Expense</span></span>
- <span data-ttu-id="7cb0e-144">OCR ricevuta</span><span class="sxs-lookup"><span data-stu-id="7cb0e-144">Receipt OCR</span></span>
- <span data-ttu-id="7cb0e-145">Fattura completa</span><span class="sxs-lookup"><span data-stu-id="7cb0e-145">Full Invoicing</span></span>
- <span data-ttu-id="7cb0e-146">Riconoscimento ricavi</span><span class="sxs-lookup"><span data-stu-id="7cb0e-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7cb0e-147">Passaggi per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="7cb0e-147">Deployment steps</span></span>
<span data-ttu-id="7cb0e-148">Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7cb0e-149">Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](resource-sign-up-preview-subscription.md) e [Eseguire il provisioning di un nuovo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="7cb0e-150">Project Operations per scenari di materiali stoccati/ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="7cb0e-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="7cb0e-151">Pianificazione di un progetto tramite la struttura di suddivisione del lavoro</span><span class="sxs-lookup"><span data-stu-id="7cb0e-151">Project planning using WBS</span></span>
- <span data-ttu-id="7cb0e-152">Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="7cb0e-152">Resource Management</span></span>
- <span data-ttu-id="7cb0e-153">Registrazione del tempo</span><span class="sxs-lookup"><span data-stu-id="7cb0e-153">Time Tracking</span></span>
- <span data-ttu-id="7cb0e-154">Spesa completa</span><span class="sxs-lookup"><span data-stu-id="7cb0e-154">Full Expense</span></span>
- <span data-ttu-id="7cb0e-155">OCR ricevuta</span><span class="sxs-lookup"><span data-stu-id="7cb0e-155">Receipt OCR</span></span>
- <span data-ttu-id="7cb0e-156">Fattura completa</span><span class="sxs-lookup"><span data-stu-id="7cb0e-156">Full Invoicing</span></span>
- <span data-ttu-id="7cb0e-157">Riconoscimento ricavi</span><span class="sxs-lookup"><span data-stu-id="7cb0e-157">Revenue Recognition</span></span>
- <span data-ttu-id="7cb0e-158">Ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="7cb0e-158">Production Orders</span></span>
- <span data-ttu-id="7cb0e-159">Supporto materiali</span><span class="sxs-lookup"><span data-stu-id="7cb0e-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7cb0e-160">Passaggi per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="7cb0e-160">Deployment steps</span></span>
<span data-ttu-id="7cb0e-161">Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7cb0e-162">Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Eseguire il provisioning di un nuovo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7cb0e-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

