---
title: Home page della creazione di report
description: In questo argomento vengono fornite informazioni sulla creazione di report in Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ee9bdfc6-123d-4146-8706-eab76fa37b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 42e24f42fd80b445718f81f4ff40e52c8cdaa7ba
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752698"
---
# <a name="reporting-home-page"></a><span data-ttu-id="916fd-103">Home page della creazione di report</span><span class="sxs-lookup"><span data-stu-id="916fd-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="916fd-104">Microsoft Dynamics 365 Project Service Automation consente alle organizzazioni basate su progetto di gestire efficacemente le operazioni inerenti alle proprie attività.</span><span class="sxs-lookup"><span data-stu-id="916fd-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="916fd-105">In qualsiasi progetto, i membri del team devono gestire le opportunità, le offerte e pianificare il lavoro, assegnare risorse ai progetti, gestire il lavoro a seconda del piano, fatturare il lavoro e quindi svolgere il lavoro per completare il progetto.</span><span class="sxs-lookup"><span data-stu-id="916fd-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="916fd-106">La capacità di generare report sulle operazioni è essenziale per determinare l'integrità dell'organizzazione e intraprendere qualsiasi azione correttiva necessaria.</span><span class="sxs-lookup"><span data-stu-id="916fd-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="916fd-107">PSA utilizza le tecnologie e i metodi di creazione di report di Microsoft Dynamics 365 per qualsiasi report.</span><span class="sxs-lookup"><span data-stu-id="916fd-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="916fd-108">Per ulteriori informazioni sulle opzioni per la creazione di report, consultare [Guida alla scrittura di report per Dynamics 365 Customer Engagement (on-premises), versione 9](../analytics/reporting-analytics-with-dynamics-365.md).</span><span class="sxs-lookup"><span data-stu-id="916fd-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](../analytics/reporting-analytics-with-dynamics-365.md).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="916fd-109">Creazione guidata report</span><span class="sxs-lookup"><span data-stu-id="916fd-109">Report Wizard</span></span>

<span data-ttu-id="916fd-110">La Creazione guidata report consente agli utenti non sviluppatori di creare semplici report.</span><span class="sxs-lookup"><span data-stu-id="916fd-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="916fd-111">Poiché l'app è integrata in una piattaforma esistente, l'esperienza è simile a quella documentata in [Creare o modificare un report con la Creazione guidata report](../basics/create-edit-copy-report-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="916fd-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](../basics/create-edit-copy-report-wizard.md).</span></span> <span data-ttu-id="916fd-112">Tuttavia, si utilizzeranno entità specifiche di Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="916fd-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="916fd-113">Report R Services per SQL Server personalizzati</span><span class="sxs-lookup"><span data-stu-id="916fd-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="916fd-114">Se è necessario generare un report specifico che non può essere creato utilizzando la Creazione guidata report, è possibile creare un report personalizzato.</span><span class="sxs-lookup"><span data-stu-id="916fd-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="916fd-115">Devi avere Microsoft Visual Studio installato insieme a Microsoft SQL Server Data Tools e alle estensioni per la modifica dei report.</span><span class="sxs-lookup"><span data-stu-id="916fd-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="916fd-116">Per ulteriori informazioni su strumenti e versioni, vedi [Ambiente di scrittura report utilizzando SQL Server Data Tools](../analytics/report-writing-environment-using-sql-server-data-tools.md).</span><span class="sxs-lookup"><span data-stu-id="916fd-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](../analytics/report-writing-environment-using-sql-server-data-tools.md).</span></span> <span data-ttu-id="916fd-117">Per informazioni su come creare un report personalizzato, vedi [Creare un nuovo report con SQL Server Data Tools](../analytics/create-a-new-report-using-sql-server-data-tools.md).</span><span class="sxs-lookup"><span data-stu-id="916fd-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](../analytics/create-a-new-report-using-sql-server-data-tools.md).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="916fd-118">App di dati analitici Power BI</span><span class="sxs-lookup"><span data-stu-id="916fd-118">Power BI insights apps</span></span>

<span data-ttu-id="916fd-119">L'utilizzo combinato di Microsoft Power BI e Dynamics 365 offre una potente soluzione di utilizzo dei dati sotto forma di app di dati analitici.</span><span class="sxs-lookup"><span data-stu-id="916fd-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="916fd-120">Per informazioni sulla disponibilità di app di analisi, vedi [Pagina delle app di analisi di Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="916fd-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="916fd-121">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="916fd-121">Additional resources</span></span>
<span data-ttu-id="916fd-122">Per ulteriori informazioni sulla creazione di report in PSA, vedi i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="916fd-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="916fd-123">Utilizzare il modello di dati di Project Service</span><span class="sxs-lookup"><span data-stu-id="916fd-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="916fd-124">Dashboard</span><span class="sxs-lookup"><span data-stu-id="916fd-124">Dashboards</span></span>](reports-dashboards.md)

