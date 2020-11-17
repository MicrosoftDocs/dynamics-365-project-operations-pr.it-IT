---
title: Novità o modifiche nella versione di aggiornamento 23 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 23 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131123"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="a2610-103">Versione di aggiornamento di Project Service Automation 23, V3</span><span class="sxs-lookup"><span data-stu-id="a2610-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="a2610-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a2610-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a2610-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="a2610-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a2610-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a2610-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a2610-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a2610-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a2610-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a2610-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a2610-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 23 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="a2610-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="a2610-110">Questa versione ha il numero di build V 3.10.34.30 ed è generalmente disponibile tramite un aggiornamento automatico in agosto 2020</span><span class="sxs-lookup"><span data-stu-id="a2610-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="a2610-111">Rilascio 23 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a2610-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a2610-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="a2610-112">Bug fixes</span></span>

<span data-ttu-id="a2610-113">**Tempo e spesa**</span><span class="sxs-lookup"><span data-stu-id="a2610-113">**Time and Expense**</span></span>

<span data-ttu-id="a2610-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="a2610-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="a2610-115">Gestisci il caso limite in **Eliminazione membro del team di progetto** per fornire un'eccezione significativa.</span><span class="sxs-lookup"><span data-stu-id="a2610-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="a2610-116">L'importazione dell'assegnazione risulta in una schermata di rimozione vuota.</span><span class="sxs-lookup"><span data-stu-id="a2610-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="a2610-117">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="a2610-117">**Resource Management**</span></span>

<span data-ttu-id="a2610-118">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="a2610-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a2610-119">La **Scheda risorsa griglia di utilizzo delle risorse** mostra dati errati quando la scala temporale è superiore a cinque giorni.</span><span class="sxs-lookup"><span data-stu-id="a2610-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="a2610-120">Quando i clienti creano una risorsa prenotabile, il plug-in non riesce ad aggiungere automaticamente la risorsa a un gruppo Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="a2610-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="a2610-121">La visualizzazione **Riconciliazione** mostra i contorni manuali in modo errato nella visualizzzione **Settimana** o **Mese**.</span><span class="sxs-lookup"><span data-stu-id="a2610-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="a2610-122">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="a2610-122">**Project Management**</span></span>

<span data-ttu-id="a2610-123">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="a2610-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="a2610-124">Un numero eccessivo di entità **RetrieveMultiple per usersettings** stanno causando una riduzione delle prestazioni per le approvazioni dei progetti e altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="a2610-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="a2610-125">La ricerca delle risorse della griglia **Pianificazione delle attività** è limitata per mostrare solo fino a cinque membri del team di progetto.</span><span class="sxs-lookup"><span data-stu-id="a2610-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="a2610-126">La ricerca delle risorse della griglia **Pianificazione delle attività** non filtra le risorse inattive.</span><span class="sxs-lookup"><span data-stu-id="a2610-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="a2610-127">La modalità manuale non funziona come previsto nella struttura di suddivisione del lavoro di pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="a2610-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="a2610-128">La griglia **Pianificazione delle attività** mostra **Categorie di transazioni inattive**.</span><span class="sxs-lookup"><span data-stu-id="a2610-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="a2610-129">La griglia **Assegnazione delle risorse** viene arrotondata in modo errato quando un'attività ha più assegnazioni.</span><span class="sxs-lookup"><span data-stu-id="a2610-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="a2610-130">I valori di arrotondamento sono diversi tra il costo pianificato e il costo effettivo per una singola attività.</span><span class="sxs-lookup"><span data-stu-id="a2610-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="a2610-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a2610-131">**Sales**</span></span>

<span data-ttu-id="a2610-132">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="a2610-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="a2610-133">Il doppio clic su **Recupera tutte le categorie di transazioni** crea più righe.</span><span class="sxs-lookup"><span data-stu-id="a2610-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
