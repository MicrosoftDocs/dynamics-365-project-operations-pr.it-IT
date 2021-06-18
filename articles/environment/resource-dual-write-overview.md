---
title: Integrazione di doppia scrittura di Project Operations
description: Questo argomento fornisce una panoramica dell'integrazione della doppia scrittura di Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998686"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="71b49-103">Panoramica dell'integrazione di doppia scrittura di Project Operations</span><span class="sxs-lookup"><span data-stu-id="71b49-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="71b49-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="71b49-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="71b49-105">Project Operations usa le [capacità di doppia scrittura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) per sincronizzare i dati tra Microsoft Dataverse e Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="71b49-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="71b49-106">La seguente illustrazione mostra come i dati vengono sincronizzati come parte di questa integrazione tra Dataverse e Finance.</span><span class="sxs-lookup"><span data-stu-id="71b49-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Panoramica dei flussi di dati di Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="71b49-108">Project Operations in Dataverse fornisce una moderna interfaccia utente (UI) e una facile estensibilità senza codice/uso limitato di codice utilizzando le capacità Power Platform.</span><span class="sxs-lookup"><span data-stu-id="71b49-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="71b49-109">I responsabili di progetto, i responsabili delle risorse, i membri del team di progetto e altri personaggi del front-office svolgono le loro attività in Project Operations su Dataverse.</span><span class="sxs-lookup"><span data-stu-id="71b49-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="71b49-110">Project Operations in Finance fornisce supporto per la contabilità del progetto e il riconoscimento dei ricavi.</span><span class="sxs-lookup"><span data-stu-id="71b49-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="71b49-111">Project Operations si collega alla struttura finanziaria in Finance per il calcolo dell'IVA, i tassi di cambio valutari, i report sulle dimensioni finanziarie e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="71b49-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="71b49-112">Le esperienze dei contabili di progetto si svolgono principalmente in Finance.</span><span class="sxs-lookup"><span data-stu-id="71b49-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="71b49-113">L'integrazione di Project Operations consiste nella seguente integrazione di componenti:</span><span class="sxs-lookup"><span data-stu-id="71b49-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="71b49-114">Configurazione di Project Operations e integrazione dei dati di configurazione</span><span class="sxs-lookup"><span data-stu-id="71b49-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="71b49-115">Stime e valori effettivi di progetto</span><span class="sxs-lookup"><span data-stu-id="71b49-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="71b49-116">Fatture di progetto</span><span class="sxs-lookup"><span data-stu-id="71b49-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="71b49-117">Gestione spese</span><span class="sxs-lookup"><span data-stu-id="71b49-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="71b49-118">Fattura fornitore</span><span class="sxs-lookup"><span data-stu-id="71b49-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
