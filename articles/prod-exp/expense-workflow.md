---
title: Flusso di lavoro per la gestione delle spese
description: Questo argomento spiega come utilizzare il sistema di flusso di lavoro in Microsoft Dynamics 365 Finance per impostare un processo di revisione per le note spese in Gestione spese.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960567"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="f684f-103">Flusso di lavoro per la gestione delle spese</span><span class="sxs-lookup"><span data-stu-id="f684f-103">Expense management workflow</span></span>

<span data-ttu-id="f684f-104">Puoi utilizzare il sistema di flusso di lavoro per impostare un processo di revisione per le note spese in Gestione spese.</span><span class="sxs-lookup"><span data-stu-id="f684f-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="f684f-105">Puoi impostare un flusso di lavoro che utilizza i seguenti criteri per determinare chi approva le note spese:</span><span class="sxs-lookup"><span data-stu-id="f684f-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="f684f-106">La gerarchia dei dipendenti e i limiti di approvazione predefiniti</span><span class="sxs-lookup"><span data-stu-id="f684f-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="f684f-107">Approvazione multilivello che supporta approvatori temporanei e un approvatore finale</span><span class="sxs-lookup"><span data-stu-id="f684f-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="f684f-108">Dimensioni finanziarie e responsabilità del progetto</span><span class="sxs-lookup"><span data-stu-id="f684f-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="f684f-109">Assegnazione a utenti o gruppi di utenti specifici</span><span class="sxs-lookup"><span data-stu-id="f684f-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="f684f-110">Puoi creare approvazioni del flusso di lavoro per note spese, richieste di viaggio, anticipi di cassa e recupero dell'IVA.</span><span class="sxs-lookup"><span data-stu-id="f684f-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="f684f-111">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="f684f-111">**Example**</span></span>

<span data-ttu-id="f684f-112">Il processo seguente è un esempio del flusso di lavoro di gestione delle spese per una nota spese.</span><span class="sxs-lookup"><span data-stu-id="f684f-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="f684f-113">Un dipendente crea e salva una nota spese.</span><span class="sxs-lookup"><span data-stu-id="f684f-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="f684f-114">Il dipendente invia la nota spese per l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="f684f-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="f684f-115">Il responsabile approvazione viene identificato in base alle regole definite durante l'impostazione del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f684f-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="f684f-116">Il responsabile approvatore riceve una notifica indicante che una nota spese è pronta per l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="f684f-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="f684f-117">Il responsabile approvatore esamina la nota spese e verifica che siano soddisfatte le seguenti condizioni:</span><span class="sxs-lookup"><span data-stu-id="f684f-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="f684f-118">Le spese non violano alcun criterio di spesa.</span><span class="sxs-lookup"><span data-stu-id="f684f-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="f684f-119">Se una spesa viola un criterio, il responsabile approvatore verifica che la nota spese includa una motivazione aziendale valida.</span><span class="sxs-lookup"><span data-stu-id="f684f-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="f684f-120">Le ricevute elettroniche sono collegate alla nota spese.</span><span class="sxs-lookup"><span data-stu-id="f684f-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="f684f-121">Il responsabile approvatore approva la nota spese.</span><span class="sxs-lookup"><span data-stu-id="f684f-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="f684f-122">La nota spese viene assegnata al coordinatore della contabilità fornitori per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="f684f-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="f684f-123">Si verifica uno dei seguenti passaggi, a seconda che la registrazione automatica sia configurata o meno:</span><span class="sxs-lookup"><span data-stu-id="f684f-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="f684f-124">Se è configurata la registrazione automatica, la nota spese viene elaborata per il pagamento e lo stato della nota spese viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f684f-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="f684f-125">Se la registrazione automatica non è configurata, il coordinatore della contabilità fornitori verifica che tutte le ricevute originali siano state inviate e che le ricevute siano corrispondenti alle spese nella nota spese.</span><span class="sxs-lookup"><span data-stu-id="f684f-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="f684f-126">Anche tutti i codici IVA inseriti nella nota spese devono essere verificati come corretti.</span><span class="sxs-lookup"><span data-stu-id="f684f-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="f684f-127">Dopo aver verificato questi requisiti, viene registrata la nota spese.</span><span class="sxs-lookup"><span data-stu-id="f684f-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="f684f-128">Dopo la registrazione della nota spese, il pagamento viene autorizzato per la nota spese e il dipendente viene rimborsato.</span><span class="sxs-lookup"><span data-stu-id="f684f-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
