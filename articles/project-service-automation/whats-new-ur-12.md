---
title: Novità dell'aggiornamento rilascio 12 di Project Service Automation V3
description: Questo argomento fornisce informazioni sulle novità dell'aggiornamento rilascio 12 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752646"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="54a3d-103">Aggiornamento rilascio 12 di Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="54a3d-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="54a3d-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="54a3d-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="54a3d-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="54a3d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="54a3d-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="54a3d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="54a3d-107">Per aggiornare a questa versione, visitare l'interfaccia di amministrazione di Dynamics 365 online e andare alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="54a3d-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="54a3d-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="54a3d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="54a3d-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 12 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="54a3d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="54a3d-110">Questa versione ha il numero di build V3.10.2.34 ed è generalmente disponibile tramite un aggiornamento automatico in ottobre 2019.</span><span class="sxs-lookup"><span data-stu-id="54a3d-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="54a3d-111">Rilascio 12 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="54a3d-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="54a3d-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="54a3d-112">Bug fixes</span></span>

- <span data-ttu-id="54a3d-113">Tempo e spesa</span><span class="sxs-lookup"><span data-stu-id="54a3d-113">Time and Expense</span></span>

    - <span data-ttu-id="54a3d-114">Risolto: la messaggistica degli errori di immissione dell'ora è stata aggiornata con un contesto più pertinente.</span><span class="sxs-lookup"><span data-stu-id="54a3d-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="54a3d-115">Risolto: la pianificazione e la griglia di immissione dell'ora visualizzano correttamente la barra di scorrimento verticale quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="54a3d-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="54a3d-116">Risolto: Gli inserimenti ore e spese inviati possono essere approvati.</span><span class="sxs-lookup"><span data-stu-id="54a3d-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="54a3d-117">Risolto: il messaggio di annullamento della finestra di dialogo di conferma dell'approvazione è stato corretto per riflettere lo stato dell'approvazione quando cambia da **Approvato** in **Inviato**.</span><span class="sxs-lookup"><span data-stu-id="54a3d-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="54a3d-118">Risolto: i campi **Prezzo**, **Unità** e **Quantità** sono ora bloccati sul record Spese dopo che è stato approvato.</span><span class="sxs-lookup"><span data-stu-id="54a3d-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="54a3d-119">Gestione progetti</span><span class="sxs-lookup"><span data-stu-id="54a3d-119">Project Management</span></span>

    - <span data-ttu-id="54a3d-120">Risolto: l'azione **Nuovo** nel modulo principale **Membro del team** è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="54a3d-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="54a3d-121">Risolto: le assegnazioni delle risorse sono state aggiornate per tenere conto degli errori di arrotondamento non accurati, che portano a uno spostamento nella data di fine di un'attività.</span><span class="sxs-lookup"><span data-stu-id="54a3d-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="54a3d-122">Risolto: nella griglia delle attività, all'utente vengono visualizzati errori sul lato server.</span><span class="sxs-lookup"><span data-stu-id="54a3d-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="54a3d-123">Risolto: il nome del membro del team ora viene visualizzato nel selettore di persone dell'attività anziché nel nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="54a3d-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="54a3d-124">Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="54a3d-124">Resource Management</span></span>

    - <span data-ttu-id="54a3d-125">Risolto: i dettagli sui requisiti delle risorse per i progetti creati da un modello ora utilizzano il calendario del progetto.</span><span class="sxs-lookup"><span data-stu-id="54a3d-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="54a3d-126">Risolto: le abilità e le competenze ora vengono automaticamente impostate dai dati master del ruolo nel requisito della risorsa creato per quel ruolo.</span><span class="sxs-lookup"><span data-stu-id="54a3d-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="54a3d-127">Sales</span><span class="sxs-lookup"><span data-stu-id="54a3d-127">Sales</span></span>

    - <span data-ttu-id="54a3d-128">Risolto: ID oggetto duplicato trovato nel modulo **Contratto principale**.</span><span class="sxs-lookup"><span data-stu-id="54a3d-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="54a3d-129">Risolto: la logica è stata aggiornata per rendere la scheda **Analisi offerta** visibile in modo da visualizzare l'impostazione dei metadati della scheda.</span><span class="sxs-lookup"><span data-stu-id="54a3d-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="54a3d-130">Risolto: la data contabile sul record effettivo ora proviene dalla data di registrazione ora/spesa e non dalla data dell'approvazione.</span><span class="sxs-lookup"><span data-stu-id="54a3d-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
