---
title: Novità o modifiche nella versione di aggiornamento 19 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 19 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949144"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="253bc-103">Versione di aggiornamento di Project Service Automation 19, V3</span><span class="sxs-lookup"><span data-stu-id="253bc-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="253bc-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="253bc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="253bc-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="253bc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="253bc-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="253bc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="253bc-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="253bc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="253bc-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="253bc-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="253bc-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 19 di PSA V3.</span><span class="sxs-lookup"><span data-stu-id="253bc-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="253bc-110">Questa versione ha il numero di build V3.10.30.41 ed è generalmente disponibile tramite un aggiornamento automatico a maggio 2020.</span><span class="sxs-lookup"><span data-stu-id="253bc-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="253bc-111">Rilascio 19 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="253bc-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="253bc-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="253bc-112">Bug fixes</span></span>

<span data-ttu-id="253bc-113">**Tempo e spesa**</span><span class="sxs-lookup"><span data-stu-id="253bc-113">**Time and Expense**</span></span>

<span data-ttu-id="253bc-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="253bc-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="253bc-115">Gli errori derivati dalle importazioni dell'inserimento ore non vengono visualizzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="253bc-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="253bc-116">La griglia Inserimento ore non supporta il comportamento del campo **Solo data**.</span><span class="sxs-lookup"><span data-stu-id="253bc-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="253bc-117">Le risorse del progetto non sono in grado di creare una spesa con un progetto.</span><span class="sxs-lookup"><span data-stu-id="253bc-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="253bc-118">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="253bc-118">**Project Management**</span></span>

<span data-ttu-id="253bc-119">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="253bc-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="253bc-120">L'attività del nipote provoca una stima dello sforzo errata durante il calcolo del completamento (EAC).</span><span class="sxs-lookup"><span data-stu-id="253bc-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="253bc-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="253bc-121">**Sales**</span></span>

<span data-ttu-id="253bc-122">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="253bc-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="253bc-123">L'azione **Ricalcola** non funzione con i dettagli della voce di contratto delle spese o con i dettagli della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="253bc-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="253bc-124">**Aggiorna prezzi** mancante per stime di spesa.</span><span class="sxs-lookup"><span data-stu-id="253bc-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="253bc-125">I clienti non sono in grado di selezionare le ragioni dello stato del contratto personalizzato dalla pagina **Contratto di progetto**.</span><span class="sxs-lookup"><span data-stu-id="253bc-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="253bc-126">Prestazioni compromesse dell'esperienza cliente durante la creazione del listino prezzi personalizzato da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="253bc-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="253bc-127">I clienti rilevano incoerenze nei valori predefiniti di **unità** nelle pagine **Dettagli riga di offerta** e **Dettagli voce di contratto**.</span><span class="sxs-lookup"><span data-stu-id="253bc-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="253bc-128">L'aggiunta di elementi della categoria di transazioni non addebitabili a una voce di contratto addebitabile non rispetterà il tipo di fatturazione **Non addebitabile** della categoria di transazione.</span><span class="sxs-lookup"><span data-stu-id="253bc-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="253bc-129">I clienti non possono utilizzare i ruoli e la categoria appena aggiunti nei contratti precedentemente creati.</span><span class="sxs-lookup"><span data-stu-id="253bc-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="253bc-130">I clienti riscontrano prestazioni compromesse per Recupero non necessario in PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="253bc-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="253bc-131">I ruoli configurati come non addebitabili nell'elenco **Categorie di risorse** devono essere aggiunti alla scheda **Ruoli addebitabili** come **Non0chargeable** sulla voce di contratto per un progetto.</span><span class="sxs-lookup"><span data-stu-id="253bc-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="253bc-132">I clienti possono riscontrare prestazioni compromesse durante la creazione di un progetto perché **GetBookableResourceIdFromUser** recupera tutte le colonne di risorse prenotabili anziché solo l'ID principale.</span><span class="sxs-lookup"><span data-stu-id="253bc-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="253bc-133">All'entità **TransactionType** manca il plug-in di aggiornamento preliminare per impedire agli utenti di accedere a **Unità** e **UnitGroups** che non sono validi per i tipi di transazione.</span><span class="sxs-lookup"><span data-stu-id="253bc-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="253bc-134">Il passaggio **Rimuovi** non funziona per l'importazione dell'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="253bc-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]