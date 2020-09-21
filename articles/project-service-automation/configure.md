---
title: Configurare Project Service Automation
description: Passaggi per configurare Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752629"
---
# <a name="configure-project-service"></a><span data-ttu-id="74e55-103">Configurare Project Service</span><span class="sxs-lookup"><span data-stu-id="74e55-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="74e55-104">Prima di usare le funzionalità di automazione di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] per gestire gli account, i progetti e le risorse, devi completare alcuni passaggi di configurazione per garantire che la soluzione [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] soddisfi le esigenze aziendali.</span><span class="sxs-lookup"><span data-stu-id="74e55-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="74e55-105">Nei passaggi seguenti è incluso:</span><span class="sxs-lookup"><span data-stu-id="74e55-105">These steps include:</span></span>  
  
-   <span data-ttu-id="74e55-106">[Configurare le unità di tempo](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="74e55-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="74e55-107">Configura le unità di tempo nel catalogo di prodotti che utilizzerai come base per la pianificazione e la fatturazione dei progetti.</span><span class="sxs-lookup"><span data-stu-id="74e55-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="74e55-108">[Configurare valute e tassi di cambio](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="74e55-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="74e55-109">Imposta le valute da utilizzare per i progetti.</span><span class="sxs-lookup"><span data-stu-id="74e55-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="74e55-110">[Creare unità organizzative](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="74e55-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="74e55-111">Imposta i gruppi che la società utilizza per suddividere la propria attività, per area geografica, funzionalità aziendale o un'altra divisione logica.</span><span class="sxs-lookup"><span data-stu-id="74e55-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="74e55-112">[Configurare le frequenze di fatturazione](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="74e55-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="74e55-113">Imposta i periodi di tempo che desideri utilizzare per la fatturazione dei clienti.</span><span class="sxs-lookup"><span data-stu-id="74e55-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="74e55-114">[Configurare categorie di transazioni](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="74e55-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="74e55-115">Imposta le categorie di transazione a cui i commerciali possono addebitare le spese fatturabili e non fatturabili.</span><span class="sxs-lookup"><span data-stu-id="74e55-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="74e55-116">[Configurare categorie di spesa](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="74e55-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="74e55-117">Imposta le categorie a cui i commerciali possono addebitare le spese fatturabili e non fatturabili.</span><span class="sxs-lookup"><span data-stu-id="74e55-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="74e55-118">[Creare voci del catalogo prodotti](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="74e55-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="74e55-119">Aggiungi i prodotti che vendi, come licenze software, al catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="74e55-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="74e55-120">[Creare un listino prezzi](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="74e55-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="74e55-121">Configura listini prezzi diversi a seconda di quanto si desidera addebitare ai clienti per ogni ruolo che il progetto richiede.</span><span class="sxs-lookup"><span data-stu-id="74e55-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="74e55-122">[Configurare le risorse](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="74e55-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="74e55-123">Aggiungi le competenze, le capacità, i ruoli risorse e altre informazioni sulle risorse necessarie per i progetti.</span><span class="sxs-lookup"><span data-stu-id="74e55-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="74e55-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74e55-124">See Also</span></span>  
 <span data-ttu-id="74e55-125">[Panoramica di Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="74e55-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="74e55-126">[Configurare Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="74e55-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="74e55-127">[Guida per la gestione dell'account](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="74e55-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="74e55-128">[Guida del responsabile di progetto](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="74e55-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="74e55-129">[Guida di Resource Manager](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="74e55-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="74e55-130">Guida per tempo, spese e collaborazione</span><span class="sxs-lookup"><span data-stu-id="74e55-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
