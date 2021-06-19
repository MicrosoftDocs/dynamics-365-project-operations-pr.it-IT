---
title: Novità o modifiche nella versione di aggiornamento 32 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 32 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129671"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="f0ff5-103">Novità o modifiche nella versione di aggiornamento 32 di Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="f0ff5-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f0ff5-104">Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="f0ff5-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f0ff5-106">È compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f0ff5-107">Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="f0ff5-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f0ff5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f0ff5-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 32 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="f0ff5-110">Questa versione ha un numero di build di V3.10.53.108 ed è generalmente disponibile tramite un aggiornamento automatico di giugno 2021.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="f0ff5-111">Rilascio 32 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f0ff5-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f0ff5-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="f0ff5-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="f0ff5-113">Generali</span><span class="sxs-lookup"><span data-stu-id="f0ff5-113">General</span></span>

- <span data-ttu-id="f0ff5-114">Quando un aggiornamento importante non riesce, devono essere bloccati solo i punti di ingresso dell'applicazione principale, per garantire che le entità condivise siano ancora accessibili.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="f0ff5-115">Ore e spesa</span><span class="sxs-lookup"><span data-stu-id="f0ff5-115">Time and Expense</span></span>

<span data-ttu-id="f0ff5-116">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="f0ff5-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="f0ff5-117">**TimeEntriesImportFromResourceAssignment** non mantiene l'ora di inizio e l'ora di fine della sezione del profilo di assegnazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="f0ff5-118">Quando selezioni **Apri inserimento** nella griglia **Inserimento ore**, potresti non essere in grado di selezionare altri moduli.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="f0ff5-119">Durante l'importazione delle assegnazioni agli inserimenti delle ore, la query del codice client potrebbe generare un URL lungo che non risolve la query.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="f0ff5-120">Nella griglia **Inserimento ore**, dopo che un valore è stato eliminato da una cella, lo stato attivo non rimane nella griglia.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="f0ff5-121">Il pulsante **Rifiuta** è stato rimosso dalla vista **Approvazioni in elaborazione** per le omologazioni moderne.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="f0ff5-122">La stabilità e le prestazioni dell'approvazione in blocco dell'inserimento ore sono influenzate da deadlock e dalla mancata gestione appropriata delle personalizzazioni relative all'entità **Inserimento ore**.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="f0ff5-123">Pianificazione di progetti</span><span class="sxs-lookup"><span data-stu-id="f0ff5-123">Project Planning</span></span>

- <span data-ttu-id="f0ff5-124">Un'eccezione di riferimento null viene generata quando si aggiorna un progetto che ha un valore null nel campo **Unità contratto**.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="f0ff5-125">**Aggiorna totali progetto** non calcola correttamente il costo rimanente e le vendite rimanenti su un progetto.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="f0ff5-126">I calcoli dei prezzi ridondanti influiscono sulle prestazioni correlate agli aggiornamenti sui contorni dell'assegnazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="f0ff5-127">Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="f0ff5-127">Resource Management</span></span>

<span data-ttu-id="f0ff5-128">Il problema seguente è stato risolto:</span><span class="sxs-lookup"><span data-stu-id="f0ff5-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="f0ff5-129">Quando la capacità di calendario di una risorsa prenotabile è maggiore di 1, Project Service Automation riconosce erroneamente la capacità come 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f0ff5-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="f0ff5-130">Pertanto, si verifica un ciclo infinito nella visualizzazione della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="f0ff5-131">Vendite</span><span class="sxs-lookup"><span data-stu-id="f0ff5-131">Sales</span></span>

<span data-ttu-id="f0ff5-132">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="f0ff5-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="f0ff5-133">Quando viene creata una riga del giornale di registrazione con un tipo di transazione personalizzato, si verifica la seguente eccezione di riferimento null: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="f0ff5-134">I ruoli e le categorie disattivati prima della copia di un'offerta non devono essere aggiunti ai ruoli e alle categorie addebitabili dell'offerta appena copiata.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="f0ff5-135">La data del documento e la data contabile non sono allineate con la data di inizio fornita in un dettaglio della riga della fattura creato direttamente in una bozza di fattura.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="f0ff5-136">Le eccezioni di riferimento null vengono generate negli scenari correlati alla disattivazione di ruoli e categorie prima che venga copiata un'offerta.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="f0ff5-137">L'azione **Aggiorna prezzi** nella pagina **Progetti** non aggiorna le stime di spesa e le stime dei materiali.</span><span class="sxs-lookup"><span data-stu-id="f0ff5-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
