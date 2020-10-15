---
title: Tipi di distribuzione
description: Questo argomento fornisce informazioni per determina il tipo di distribuzione di Project Operations giusto per la tua azienda.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948928"
---
# <a name="deployment-types"></a><span data-ttu-id="6a459-103">Tipi di distribuzione</span><span class="sxs-lookup"><span data-stu-id="6a459-103">Deployment types</span></span>

<span data-ttu-id="6a459-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="6a459-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a459-105">Dopo aver acquistato la licenza, inizia qui per determinare il miglior modello di distribuzione di Dynamics 365 Project Operations utilizzando il [flusso di installazione guidata](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6a459-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="6a459-106">Dopo aver completato il flusso di installazione guidata, verrai indirizzato al portale di gestione corretto per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="6a459-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="6a459-107">Vedi i dettagli di distribuzione di seguito per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="6a459-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="6a459-108">Clienti esistenti di Dynamics che utilizzano Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6a459-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="6a459-109">Project Operations include le funzionalità fornite con Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6a459-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="6a459-110">In futuro verrà rilasciato un percorso di aggiornamento per questi clienti.</span><span class="sxs-lookup"><span data-stu-id="6a459-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="6a459-111">Clienti esistenti di Dynamics 365 Finance che utilizzando Gestione progetti e contabilità</span><span class="sxs-lookup"><span data-stu-id="6a459-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="6a459-112">I clienti esistenti di Finance che utilizzano la funzionalità Gestione progetti e contabilità possono continuare a utilizzarla così com'è.</span><span class="sxs-lookup"><span data-stu-id="6a459-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="6a459-113">Vedi [Project Operations per scenari di materiali stoccati/ordini di produzione](#pma).</span><span class="sxs-lookup"><span data-stu-id="6a459-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="6a459-114">Project Operations supporta più opzioni di distribuzione per soddisfare le tue esigenze.</span><span class="sxs-lookup"><span data-stu-id="6a459-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="6a459-115">Che tu sia un cliente Dynamics 365 nuovo o esistente, Project Operations può supportare le tue esigenze.</span><span class="sxs-lookup"><span data-stu-id="6a459-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="6a459-116">Il nostro [Questionario sulla distribuzione](https://aka.ms/provisionprojectoperations) ti aiuterà a determinare la giusta distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6a459-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="6a459-117">I risultati ti guideranno verso uno dei seguenti tipi di distribuzione:</span><span class="sxs-lookup"><span data-stu-id="6a459-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="6a459-118">Distribuzione semplice: dalla transazione alla fatturazione proforma</span><span class="sxs-lookup"><span data-stu-id="6a459-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="6a459-119">Project Operations per scenari di risorse/materiali non stoccati</span><span class="sxs-lookup"><span data-stu-id="6a459-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="6a459-120">Project Operations per scenari di materiali stoccati/ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="6a459-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="6a459-121">Project Operations supporta scenari di materiali stoccati/ordini di produzione e scenari basati su risorse/materiali non stoccati nello stesso ambiente tramite configurazioni a livello di persona giuridica.</span><span class="sxs-lookup"><span data-stu-id="6a459-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="6a459-122">Ad esempio, Contoso può sfruttare le funzionalità di materiali stoccati/ordini di produzione nel proprio stabilimento di produzione negli Stati Uniti (Persona giuridica = Contoso Manufacturing Stati Uniti) e basati su risorse/materiali non stoccati nel proprio impianto di assistenza Contoso Robotics Arms nel Regno Unito (Persona giuridica = Contoso Robotics Regno Unito).</span><span class="sxs-lookup"><span data-stu-id="6a459-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="6a459-123"><a name="lite"><a/>Distribuzione semplice: dalla transazione alla fatturazione proforma</span><span class="sxs-lookup"><span data-stu-id="6a459-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="6a459-124">La distribuzione semplice include le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="6a459-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="6a459-125">Pianificazione del progetto utilizzando Microsoft Project per il Web</span><span class="sxs-lookup"><span data-stu-id="6a459-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6a459-126">Determinazione dei prezzi multidimensionale</span><span class="sxs-lookup"><span data-stu-id="6a459-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6a459-127">Gestione delle risorse unificata</span><span class="sxs-lookup"><span data-stu-id="6a459-127">Unified Resource Management</span></span>
- <span data-ttu-id="6a459-128">Registrazione del tempo</span><span class="sxs-lookup"><span data-stu-id="6a459-128">Time Tracking</span></span>
- <span data-ttu-id="6a459-129">Spesa di base</span><span class="sxs-lookup"><span data-stu-id="6a459-129">Basic Expense</span></span>
- <span data-ttu-id="6a459-130">Proposta di fattura</span><span class="sxs-lookup"><span data-stu-id="6a459-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6a459-131">Passaggi per la distribuzione:</span><span class="sxs-lookup"><span data-stu-id="6a459-131">Deployment steps:</span></span>
<span data-ttu-id="6a459-132">Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6a459-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6a459-133">Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](lite-preview-subscription-sign-up.md) e [Eseguire il provisioning di un nuovo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="6a459-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="6a459-134"><a name="integrated"><a/>Project Operations per scenari di risorse/materiali non stoccati</span><span class="sxs-lookup"><span data-stu-id="6a459-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="6a459-135">Project Operations per scenari di risorse/materiali non stoccati includono le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="6a459-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="6a459-136">Pianificazione del progetto utilizzando Microsoft Project per il Web</span><span class="sxs-lookup"><span data-stu-id="6a459-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6a459-137">Determinazione dei prezzi multidimensionale</span><span class="sxs-lookup"><span data-stu-id="6a459-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6a459-138">Gestione delle risorse unificata</span><span class="sxs-lookup"><span data-stu-id="6a459-138">Unified Resource Management</span></span>
- <span data-ttu-id="6a459-139">Registrazione del tempo</span><span class="sxs-lookup"><span data-stu-id="6a459-139">Time Tracking</span></span>
- <span data-ttu-id="6a459-140">Spesa di base</span><span class="sxs-lookup"><span data-stu-id="6a459-140">Basic Expense</span></span>
- <span data-ttu-id="6a459-141">Spesa completa</span><span class="sxs-lookup"><span data-stu-id="6a459-141">Full Expense</span></span>
- <span data-ttu-id="6a459-142">OCR ricevuta</span><span class="sxs-lookup"><span data-stu-id="6a459-142">Receipt OCR</span></span>
- <span data-ttu-id="6a459-143">Fattura completa</span><span class="sxs-lookup"><span data-stu-id="6a459-143">Full Invoicing</span></span>
- <span data-ttu-id="6a459-144">Riconoscimento ricavi</span><span class="sxs-lookup"><span data-stu-id="6a459-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6a459-145">Passaggi per la distribuzione:</span><span class="sxs-lookup"><span data-stu-id="6a459-145">Deployment steps:</span></span>
<span data-ttu-id="6a459-146">Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6a459-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6a459-147">Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](resource-sign-up-preview-subscription.md) e [Eseguire il provisioning di un nuovo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6a459-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="6a459-148">Project Operations per scenari di materiali stoccati/ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="6a459-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="6a459-149">Pianificazione di un progetto tramite la struttura di suddivisione del lavoro</span><span class="sxs-lookup"><span data-stu-id="6a459-149">Project planning using WBS</span></span>
- <span data-ttu-id="6a459-150">Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="6a459-150">Resource Management</span></span>
- <span data-ttu-id="6a459-151">Registrazione del tempo</span><span class="sxs-lookup"><span data-stu-id="6a459-151">Time Tracking</span></span>
- <span data-ttu-id="6a459-152">Spesa completa</span><span class="sxs-lookup"><span data-stu-id="6a459-152">Full Expense</span></span>
- <span data-ttu-id="6a459-153">OCR ricevuta</span><span class="sxs-lookup"><span data-stu-id="6a459-153">Receipt OCR</span></span>
- <span data-ttu-id="6a459-154">Fattura completa</span><span class="sxs-lookup"><span data-stu-id="6a459-154">Full Invoicing</span></span>
- <span data-ttu-id="6a459-155">Riconoscimento ricavi</span><span class="sxs-lookup"><span data-stu-id="6a459-155">Revenue Recognition</span></span>
- <span data-ttu-id="6a459-156">Ordini di produzione</span><span class="sxs-lookup"><span data-stu-id="6a459-156">Production Orders</span></span>
- <span data-ttu-id="6a459-157">Supporto materiali</span><span class="sxs-lookup"><span data-stu-id="6a459-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6a459-158">Passaggi per la distribuzione:</span><span class="sxs-lookup"><span data-stu-id="6a459-158">Deployment steps:</span></span>
<span data-ttu-id="6a459-159">Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6a459-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6a459-160">Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Eseguire il provisioning di un nuovo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6a459-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



