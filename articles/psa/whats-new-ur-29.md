---
title: Novità o modifiche nella versione di aggiornamento 29 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 29 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664648"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="77906-103">Novità o modifiche nella versione di aggiornamento 29 di Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="77906-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="77906-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="77906-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="77906-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="77906-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="77906-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="77906-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="77906-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="77906-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="77906-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="77906-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="77906-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 29 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="77906-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="77906-110">Questa versione ha un numero di build di V3.10.47.7 ed è generalmente disponibile tramite un aggiornamento automatico a febbraio 2021.</span><span class="sxs-lookup"><span data-stu-id="77906-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="77906-111">Rilascio 29 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="77906-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="77906-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="77906-112">Bug fixes</span></span>

<span data-ttu-id="77906-113">**Ore e spesa**</span><span class="sxs-lookup"><span data-stu-id="77906-113">**Time and Expense**</span></span>

<span data-ttu-id="77906-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="77906-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="77906-115">Gli utenti non possono vedere le ore lavorative registrate nei giorni non lavorativi nella griglia di inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="77906-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="77906-116">Le voci di spesa approvate possono essere modificate nella griglia.</span><span class="sxs-lookup"><span data-stu-id="77906-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="77906-117">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="77906-117">**Project Management**</span></span>

<span data-ttu-id="77906-118">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="77906-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="77906-119">Logica di convalida mancante per garantire che le ore di lavoro per l'assegnazione delle risorse non possano essere negative.</span><span class="sxs-lookup"><span data-stu-id="77906-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="77906-120">L'azione personalizzata, **AssignResourcesForTask** aggiorna tutti i campi anziché solo i campi modificati.</span><span class="sxs-lookup"><span data-stu-id="77906-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="77906-121">Quando si copia un progetto in un ambiente con plug-in o flussi di lavoro registrati nell'evento **CreateProject**, l'attributo **msdyn_bulkgenerationstatus** non viene aggiornato se **CopyWBSToProject** non riesce.</span><span class="sxs-lookup"><span data-stu-id="77906-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="77906-122">Quando si espande il calendario del progetto, i giorni lavorativi non vengono ordinati in ordine crescente, causando il mancato aggiornamento di alcune attività del progetto.</span><span class="sxs-lookup"><span data-stu-id="77906-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="77906-123">La modifica del responsabile di progetto su un progetto esistente attiva la logica predefinita dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="77906-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="77906-124">**Vendite**</span><span class="sxs-lookup"><span data-stu-id="77906-124">**Sales**</span></span>

<span data-ttu-id="77906-125">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="77906-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="77906-126">La scheda **Esecuzione contratto** nella pagina **Contratto** non riesce silenziosamente durante l'inizializzazione quando non sono presenti righe di contratto.</span><span class="sxs-lookup"><span data-stu-id="77906-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
