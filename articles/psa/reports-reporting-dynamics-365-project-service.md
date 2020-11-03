---
title: Home page della creazione di report
description: In questo argomento vengono fornite informazioni sulla creazione di report in Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 30411818bdc1b370a71148cf79f743413167dab2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079103"
---
# <a name="reporting-home-page"></a><span data-ttu-id="8df42-103">Home page della creazione di report</span><span class="sxs-lookup"><span data-stu-id="8df42-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8df42-104">Microsoft Dynamics 365 Project Service Automation consente alle organizzazioni basate su progetto di gestire efficacemente le operazioni inerenti alle proprie attività.</span><span class="sxs-lookup"><span data-stu-id="8df42-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="8df42-105">In qualsiasi progetto, i membri del team devono gestire le opportunità, le offerte e pianificare il lavoro, assegnare risorse ai progetti, gestire il lavoro a seconda del piano, fatturare il lavoro e quindi svolgere il lavoro per completare il progetto.</span><span class="sxs-lookup"><span data-stu-id="8df42-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="8df42-106">La capacità di generare report sulle operazioni è essenziale per determinare l'integrità dell'organizzazione e intraprendere qualsiasi azione correttiva necessaria.</span><span class="sxs-lookup"><span data-stu-id="8df42-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="8df42-107">PSA utilizza le tecnologie e i metodi di creazione di report di Microsoft Dynamics 365 per qualsiasi report.</span><span class="sxs-lookup"><span data-stu-id="8df42-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="8df42-108">Per ulteriori informazioni sulle opzioni per la creazione di report, consultare [Guida alla scrittura di report per Dynamics 365 Customer Engagement (on-premises), versione 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="8df42-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="8df42-109">Creazione guidata report</span><span class="sxs-lookup"><span data-stu-id="8df42-109">Report Wizard</span></span>

<span data-ttu-id="8df42-110">La Creazione guidata report consente agli utenti non sviluppatori di creare semplici report.</span><span class="sxs-lookup"><span data-stu-id="8df42-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="8df42-111">Poiché l'app è integrata in una piattaforma esistente, l'esperienza è simile a quella documentata in [Creare o modificare un report con la Creazione guidata report](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="8df42-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="8df42-112">Tuttavia, si utilizzeranno entità specifiche di Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8df42-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="8df42-113">Report R Services per SQL Server personalizzati</span><span class="sxs-lookup"><span data-stu-id="8df42-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="8df42-114">Se è necessario generare un report specifico che non può essere creato utilizzando la Creazione guidata report, è possibile creare un report personalizzato.</span><span class="sxs-lookup"><span data-stu-id="8df42-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="8df42-115">Devi avere Microsoft Visual Studio installato insieme a Microsoft SQL Server Data Tools e alle estensioni per la modifica dei report.</span><span class="sxs-lookup"><span data-stu-id="8df42-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="8df42-116">Per ulteriori informazioni su strumenti e versioni, vedi [Ambiente di scrittura report utilizzando SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="8df42-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="8df42-117">Per informazioni su come creare un report personalizzato, vedi [Creare un nuovo report con SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="8df42-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="8df42-118">App di dati analitici Power BI</span><span class="sxs-lookup"><span data-stu-id="8df42-118">Power BI insights apps</span></span>

<span data-ttu-id="8df42-119">L'utilizzo combinato di Microsoft Power BI e Dynamics 365 offre una potente soluzione di utilizzo dei dati sotto forma di app di dati analitici.</span><span class="sxs-lookup"><span data-stu-id="8df42-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="8df42-120">Per informazioni sulla disponibilità di app di analisi, vedi [Pagina delle app di analisi di Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="8df42-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="8df42-121">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="8df42-121">Additional resources</span></span>
<span data-ttu-id="8df42-122">Per ulteriori informazioni sulla creazione di report in PSA, vedi i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="8df42-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="8df42-123">Utilizzare il modello di dati di Project Service</span><span class="sxs-lookup"><span data-stu-id="8df42-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="8df42-124">Dashboard</span><span class="sxs-lookup"><span data-stu-id="8df42-124">Dashboards</span></span>](reports-dashboards.md)

