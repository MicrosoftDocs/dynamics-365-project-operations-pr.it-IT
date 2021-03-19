---
title: Configurare Project Service Automation
description: Passaggi per configurare Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 06a29f67040cd7da583bdeae85d6a0f6a3684c52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290589"
---
# <a name="configure-project-service"></a><span data-ttu-id="a14c8-103">Configurare Project Service</span><span class="sxs-lookup"><span data-stu-id="a14c8-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a14c8-104">Prima di usare le funzionalità di automazione di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] per gestire gli account, i progetti e le risorse, devi completare alcuni passaggi di configurazione per garantire che la soluzione [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] soddisfi le esigenze aziendali.</span><span class="sxs-lookup"><span data-stu-id="a14c8-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="a14c8-105">Nei passaggi seguenti è incluso:</span><span class="sxs-lookup"><span data-stu-id="a14c8-105">These steps include:</span></span>  
  
-   <span data-ttu-id="a14c8-106">[Configurare le unità di tempo](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="a14c8-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="a14c8-107">Configura le unità di tempo nel catalogo di prodotti che utilizzerai come base per la pianificazione e la fatturazione dei progetti.</span><span class="sxs-lookup"><span data-stu-id="a14c8-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="a14c8-108">[Configurare valute e tassi di cambio](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="a14c8-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="a14c8-109">Imposta le valute da utilizzare per i progetti.</span><span class="sxs-lookup"><span data-stu-id="a14c8-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="a14c8-110">[Creare unità organizzative](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="a14c8-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="a14c8-111">Imposta i gruppi che la società utilizza per suddividere la propria attività, per area geografica, funzionalità aziendale o un'altra divisione logica.</span><span class="sxs-lookup"><span data-stu-id="a14c8-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="a14c8-112">[Configurare le frequenze di fatturazione](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="a14c8-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="a14c8-113">Imposta i periodi di tempo che desideri utilizzare per la fatturazione dei clienti.</span><span class="sxs-lookup"><span data-stu-id="a14c8-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="a14c8-114">[Configurare categorie di transazioni](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="a14c8-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="a14c8-115">Imposta le categorie di transazione a cui i commerciali possono addebitare le spese fatturabili e non fatturabili.</span><span class="sxs-lookup"><span data-stu-id="a14c8-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="a14c8-116">[Configurare categorie di spesa](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="a14c8-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="a14c8-117">Imposta le categorie a cui i commerciali possono addebitare le spese fatturabili e non fatturabili.</span><span class="sxs-lookup"><span data-stu-id="a14c8-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="a14c8-118">[Creare voci del catalogo prodotti](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="a14c8-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="a14c8-119">Aggiungi i prodotti che vendi, come licenze software, al catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="a14c8-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="a14c8-120">[Creare un listino prezzi](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="a14c8-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="a14c8-121">Configura listini prezzi diversi a seconda di quanto si desidera addebitare ai clienti per ogni ruolo che il progetto richiede.</span><span class="sxs-lookup"><span data-stu-id="a14c8-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="a14c8-122">[Configurare le risorse](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="a14c8-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="a14c8-123">Aggiungi le competenze, le capacità, i ruoli risorse e altre informazioni sulle risorse necessarie per i progetti.</span><span class="sxs-lookup"><span data-stu-id="a14c8-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a14c8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a14c8-124">See Also</span></span>  
 <span data-ttu-id="a14c8-125">[Panoramica di Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="a14c8-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="a14c8-126">[Configurare Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="a14c8-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="a14c8-127">[Guida per la gestione dell'account](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a14c8-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="a14c8-128">[Guida del responsabile di progetto](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a14c8-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="a14c8-129">[Guida di Resource Manager](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a14c8-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="a14c8-130">Guida per tempo, spese e collaborazione</span><span class="sxs-lookup"><span data-stu-id="a14c8-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]