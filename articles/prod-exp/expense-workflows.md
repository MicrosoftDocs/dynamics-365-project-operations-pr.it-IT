---
title: Impostare flussi di lavoro per la gestione delle spese
description: È possibile impostare un processo del flusso di lavoro per esaminare e approvare i documenti di viaggio e di spesa.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005121"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="6ac26-103">Impostare flussi di lavoro per la gestione delle spese</span><span class="sxs-lookup"><span data-stu-id="6ac26-103">Set up Expense management workflows</span></span>

<span data-ttu-id="6ac26-104">È possibile impostare un processo del flusso di lavoro utilizzato per esaminare e approvare i documenti di viaggio e di spesa.</span><span class="sxs-lookup"><span data-stu-id="6ac26-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="6ac26-105">I documenti per cui puoi definire i flussi di lavoro includono note spese, richieste di viaggio e richieste di anticipo in contanti.</span><span class="sxs-lookup"><span data-stu-id="6ac26-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="6ac26-106">Un flusso di lavoro rappresenta un processo aziendale.</span><span class="sxs-lookup"><span data-stu-id="6ac26-106">A workflow represents a business process.</span></span> <span data-ttu-id="6ac26-107">Definisce il modo in cui un documento viene elaborato nel sistema e indica chi deve completare un'attività o approvare un documento.</span><span class="sxs-lookup"><span data-stu-id="6ac26-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="6ac26-108">Ci sono diversi vantaggi nell'utilizzo del sistema di flusso di lavoro nella tua organizzazione:</span><span class="sxs-lookup"><span data-stu-id="6ac26-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="6ac26-109">**Processi coerenti**: puoi definire il processo di approvazione per documenti specifici, come richieste di acquisto e note spese.</span><span class="sxs-lookup"><span data-stu-id="6ac26-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="6ac26-110">L'utilizzo del sistema del flusso di lavoro aiuta a garantire che i documenti vengano elaborati e approvati in modo coerente ed efficiente.</span><span class="sxs-lookup"><span data-stu-id="6ac26-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="6ac26-111">Visibilità del processo: puoi tenere traccia dello stato, della cronologia e delle metriche delle prestazioni di una specifica istanza del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6ac26-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="6ac26-112">Ciò ti consente di determinare se è necessario apportare modifiche al flusso di lavoro per migliorare l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="6ac26-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="6ac26-113">Elenco di lavoro centralizzato: gli utenti possono visualizzare un elenco di lavoro centralizzato per vedere le attività del flusso di lavoro e le approvazioni loro assegnate.</span><span class="sxs-lookup"><span data-stu-id="6ac26-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="6ac26-114">**Tipi di flusso di lavoro che è possibile creare**</span><span class="sxs-lookup"><span data-stu-id="6ac26-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="6ac26-115">Nella tabella seguente sono elencati i tipi di flusso di lavoro che puoi creare in **Spesa**.</span><span class="sxs-lookup"><span data-stu-id="6ac26-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="6ac26-116"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="6ac26-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="6ac26-117"><strong>Usa questo tipo per</strong></span><span class="sxs-lookup"><span data-stu-id="6ac26-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="6ac26-118"><strong>Report spese</strong></span><span class="sxs-lookup"><span data-stu-id="6ac26-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="6ac26-119">Creare flussi di lavoro di approvazione per le note spese.</span><span class="sxs-lookup"><span data-stu-id="6ac26-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="6ac26-120"><strong>Registrazione automatica di note spese</strong></span><span class="sxs-lookup"><span data-stu-id="6ac26-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="6ac26-121">Creare flussi di lavoro di registrazione automatica per le note spese.</span><span class="sxs-lookup"><span data-stu-id="6ac26-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="6ac26-122"><strong>Voce di spesa</strong></span><span class="sxs-lookup"><span data-stu-id="6ac26-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="6ac26-123">Creare flussi di lavoro di approvazione per le voci di spesa nelle note spese.</span><span class="sxs-lookup"><span data-stu-id="6ac26-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="6ac26-124"><strong>Registrazione automatica delle voci di spesa</strong></span><span class="sxs-lookup"><span data-stu-id="6ac26-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="6ac26-125">Creare flussi di lavoro di registrazione automatica per le voci di spesa nelle note spese.</span><span class="sxs-lookup"><span data-stu-id="6ac26-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="6ac26-126"><strong>Richiesta di viaggio</strong></span><span class="sxs-lookup"><span data-stu-id="6ac26-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="6ac26-127">Creare flussi di lavoro di approvazione per le richieste di viaggio.</span><span class="sxs-lookup"><span data-stu-id="6ac26-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="6ac26-128"><strong>Richiesta di anticipo in contanti</strong></span><span class="sxs-lookup"><span data-stu-id="6ac26-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="6ac26-129">Creare flussi di lavoro di approvazione per richieste di anticipo in contanti.</span><span class="sxs-lookup"><span data-stu-id="6ac26-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="6ac26-130"><strong>Recupero dell'IVA</strong></span><span class="sxs-lookup"><span data-stu-id="6ac26-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="6ac26-131">Creare flussi di lavoro di approvazione per il recupero dell'IVA.</span><span class="sxs-lookup"><span data-stu-id="6ac26-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]