---
title: 'Distribuzione di Project Operations Lite: dalla transazione alla fatturazione proforma'
description: 'Questo argomento fornisce informazioni su come installare la distribuzione semplice di Project Operations: dalla transazione alla fatturazione proforma.'
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078740"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="b0692-103">Distribuzione di Project Operations Lite: dalla transazione alla fatturazione proforma</span><span class="sxs-lookup"><span data-stu-id="b0692-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="b0692-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="b0692-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b0692-105">Project Operations supporta più modelli di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b0692-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="b0692-106">Per determinare il miglior modello di distribuzione, vedi [Tipi di distribuzione](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="b0692-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="b0692-107">Questa distribuzione, Distribuzione semplice: dalla transazione alla fatturazione proforma, si traduce in una **Distribuzione solo su Common Data Service di Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="b0692-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="b0692-108">Installare Project Operations in un nuovo ambiente CDS</span><span class="sxs-lookup"><span data-stu-id="b0692-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="b0692-109">Installare in un ambiente CDS esistente</span><span class="sxs-lookup"><span data-stu-id="b0692-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="b0692-110">Installare Project Operations in un nuovo ambiente CDS</span><span class="sxs-lookup"><span data-stu-id="b0692-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="b0692-111">In quanto [amministratore globale o Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) con una licenza Project Operations, crea un nuovo ambiente CDS nell'[interfaccia di amministrazione di PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="b0692-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="b0692-112">Assicurati che **Database CDS** e **App Dynamics 365** siano abilitate.</span><span class="sxs-lookup"><span data-stu-id="b0692-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="b0692-113">Per altre informazioni, vedi [Creare e gestire ambienti nell'interfaccia di amministrazione di Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="b0692-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="b0692-114">Seleziona **Microsoft Dynamics 365 Project Operations** dall'elenco di distribuzione delle app Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b0692-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="b0692-115">Installare Project Operations in un ambiente CDS esistente</span><span class="sxs-lookup"><span data-stu-id="b0692-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="b0692-116">In quanto [amministratore globale o Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) con una licenza Project Operations, individuare l'ambiente nell'[interfaccia di amministrazione di PowerPlatform](https://admin.powerplatform.com) in cui desideri installare Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b0692-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="b0692-117">Installa **Microsoft Dynamics 365 Project Operations** dall'elenco di distribuzione delle app Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b0692-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="b0692-118">Per ulteriori informazioni, vedi [Gestire le app Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="b0692-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


