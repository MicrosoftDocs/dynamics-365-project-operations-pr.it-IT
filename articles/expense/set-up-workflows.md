---
title: Impostare flussi di lavoro per la gestione delle spese
description: È possibile impostare un processo del flusso di lavoro utilizzato per esaminare e approvare i documenti di viaggio e di spesa.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127703"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="8cfc4-103">Impostare flussi di lavoro per la gestione delle spese</span><span class="sxs-lookup"><span data-stu-id="8cfc4-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="8cfc4-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="8cfc4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8cfc4-105">È possibile impostare un processo del flusso di lavoro per esaminare e approvare i documenti di viaggio e di spesa.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="8cfc4-106">Puoi definire flussi di lavoro per note spese, richieste di viaggio e richieste di anticipo in contanti.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="8cfc4-107">Un flusso di lavoro rappresenta un processo aziendale e definisce il modo in cui un documento scorre attraverso il sistema.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="8cfc4-108">Il flusso di lavoro indica anche chi deve completare un'attività o approvare un documento.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="8cfc4-109">Ci sono diversi vantaggi nell'utilizzo del sistema di flusso di lavoro nella tua organizzazione:</span><span class="sxs-lookup"><span data-stu-id="8cfc4-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="8cfc4-110">**Processi coerenti**: puoi definire il processo di approvazione per documenti specifici, come richieste di acquisto e note spese.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="8cfc4-111">L'utilizzo del sistema del flusso di lavoro aiuta a garantire che i documenti vengano elaborati e approvati in modo coerente ed efficiente.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="8cfc4-112">**Visibilità del processo**: puoi tenere traccia dello stato, della cronologia e delle metriche delle prestazioni di una specifica istanza del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="8cfc4-113">Ciò ti consente di determinare se è necessario apportare modifiche al flusso di lavoro per migliorare l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="8cfc4-114">**Elenco di lavoro centralizzato**: gli utenti possono visualizzare un elenco di lavoro centralizzato per vedere le attività del flusso di lavoro e le approvazioni loro assegnate.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="8cfc4-115">Tipi di flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="8cfc4-115">Workflow types</span></span>

<span data-ttu-id="8cfc4-116">Nella tabella seguente sono elencati i tipi di flusso di lavoro che puoi creare in **Gestione delle spese**.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="8cfc4-117"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="8cfc4-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="8cfc4-118"><strong>Usa questo tipo per</strong></span><span class="sxs-lookup"><span data-stu-id="8cfc4-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="8cfc4-119"><strong>Approvazione automatica di note spese</strong></span><span class="sxs-lookup"><span data-stu-id="8cfc4-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="8cfc4-120">Creare flussi di lavoro di approvazione per le note spese.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="8cfc4-121"><strong>Registrazione automatica di note spese</strong></span><span class="sxs-lookup"><span data-stu-id="8cfc4-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="8cfc4-122">Creare flussi di lavoro di registrazione automatica per le note spese.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="8cfc4-123"><strong>Voce di spesa</strong></span><span class="sxs-lookup"><span data-stu-id="8cfc4-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="8cfc4-124">Creare flussi di lavoro di approvazione per le voci di spesa nelle note spese.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="8cfc4-125"><strong>Registrazione automatica delle voci di spesa</strong></span><span class="sxs-lookup"><span data-stu-id="8cfc4-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="8cfc4-126">Creare flussi di lavoro di registrazione automatica per le voci di spesa nelle note spese.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="8cfc4-127"><strong>Richiesta di viaggio</strong></span><span class="sxs-lookup"><span data-stu-id="8cfc4-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="8cfc4-128">Creare flussi di lavoro di approvazione per le richieste di viaggio.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="8cfc4-129"><strong>Richiesta di anticipo in contanti</strong></span><span class="sxs-lookup"><span data-stu-id="8cfc4-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="8cfc4-130">Creare flussi di lavoro di approvazione per richieste di anticipo in contanti.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="8cfc4-131"><strong>Recupero dell'IVA</strong></span><span class="sxs-lookup"><span data-stu-id="8cfc4-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="8cfc4-132">Creare flussi di lavoro di approvazione per il recupero dell'IVA.</span><span class="sxs-lookup"><span data-stu-id="8cfc4-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
