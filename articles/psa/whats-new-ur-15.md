---
title: Novità o modifiche nella versione di aggiornamento 15 di Project Service Automation V3
description: Questo argomento fornisce informazioni sulle novità dell'aggiornamento rilascio 15 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: fe1e2b2046faeee4e4c71484a976d70e8722e090
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949324"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="40609-103">Versione di aggiornamento di Project Service Automation 15, V3</span><span class="sxs-lookup"><span data-stu-id="40609-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="40609-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="40609-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="40609-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="40609-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="40609-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="40609-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="40609-107">Per aggiornare a questa versione, visitare l'interfaccia di amministrazione di Dynamics 365 online e andare alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="40609-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="40609-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="40609-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="40609-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 15 di PSA V3.</span><span class="sxs-lookup"><span data-stu-id="40609-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="40609-110">Questa versione ha il numero di build V3.10.5.28 ed è generalmente disponibile tramite un aggiornamento automatico in gennaio 2020.</span><span class="sxs-lookup"><span data-stu-id="40609-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="40609-111">Rilascio 15 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="40609-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="40609-112">Miglioramenti</span><span class="sxs-lookup"><span data-stu-id="40609-112">Enhancements</span></span>

- <span data-ttu-id="40609-113">Gestione progetti</span><span class="sxs-lookup"><span data-stu-id="40609-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="40609-114">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="40609-114">Bug fixes</span></span>

- <span data-ttu-id="40609-115">Tempo e spesa</span><span class="sxs-lookup"><span data-stu-id="40609-115">Time and Expense</span></span>

  - <span data-ttu-id="40609-116">Risolto: Aggiungere la gestione degli errori al caricamento nella visualizzazione di riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="40609-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="40609-117">Risolto: Hub risorse di progetto: Rinominare **Importo** per ridurre l'ambiguità.</span><span class="sxs-lookup"><span data-stu-id="40609-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="40609-118">Risolto: Modificare la visualizzazione **Copia colonne inserimenti ore** per includere il tipo.</span><span class="sxs-lookup"><span data-stu-id="40609-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="40609-119">Risolto: La modifica della durata per l'inserimento ore nella visualizzazione griglia utilizzando i numeri decimali comporta errori sconosciuti per alcuni numeri.</span><span class="sxs-lookup"><span data-stu-id="40609-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="40609-120">Gestione progetti</span><span class="sxs-lookup"><span data-stu-id="40609-120">Project Management</span></span>

  - <span data-ttu-id="40609-121">Risolto: Il menu a discesa per **Utilizza in visualizzazione tracciabilità** ora si espande in base alla larghezza delle opzioni.</span><span class="sxs-lookup"><span data-stu-id="40609-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="40609-122">Risolto: Durante la gestione dei progetti nel fuso orario +13, i calcoli delle attività possono visualizzare risultati imprecisi.</span><span class="sxs-lookup"><span data-stu-id="40609-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="40609-123">Risolto: **Ora di fine membro del team** è stato corretto quando si utilizza un calendario a 24 ore.</span><span class="sxs-lookup"><span data-stu-id="40609-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="40609-124">Risolto: Riattivato il **processo aziendale** nel modulo principale **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="40609-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="40609-125">Risolto: Il calcolo delle assegnazioni non ignora più un giorno.</span><span class="sxs-lookup"><span data-stu-id="40609-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="40609-126">Risolto: un nuovo banner di notifica è stato aggiunto al modulo del progetto quando il fuso orario differisce tra utente e progetto.</span><span class="sxs-lookup"><span data-stu-id="40609-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="40609-127">Sales</span><span class="sxs-lookup"><span data-stu-id="40609-127">Sales</span></span>

  - <span data-ttu-id="40609-128">Risolto: la ricerca della categoria di stima delle spese può essere utilizzata per filtrare i duplicati.</span><span class="sxs-lookup"><span data-stu-id="40609-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="40609-129">Risolto: il codice in **PluginDomain.ExecuteInTryCatchBlock(..)** non nasconde più l'origine dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="40609-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="40609-130">Risolto: non viene più visualizzato un messaggio di errore **Ricerca progetto** nel modulo **Riga di offerta** quando ci sono più di 1000 progetti.</span><span class="sxs-lookup"><span data-stu-id="40609-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="40609-131">Risolto: la griglia **Stime** per le stime della manodopera e delle spese ora mostra il simbolo di valuta corretto.</span><span class="sxs-lookup"><span data-stu-id="40609-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="40609-132">Risolto: dopo che un'organizzazione aggiorna PSA dall'aggiornamento rilascio 14 all'aggiornamento rilascio 15, la scheda **Pianifica** non viene più visualizzata come vuota sul modulo **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="40609-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]