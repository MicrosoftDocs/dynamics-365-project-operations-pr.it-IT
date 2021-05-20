---
title: Novità o modifiche nella versione di aggiornamento 25 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 25 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 3aa10e1d4b23fbe6c2743d71497bdef840776008
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948876"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="16cdc-103">Novità o modifiche nella versione di aggiornamento 25 di Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="16cdc-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="16cdc-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="16cdc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="16cdc-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="16cdc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="16cdc-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="16cdc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="16cdc-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="16cdc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="16cdc-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="16cdc-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="16cdc-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per Project Service Automation V3, rilascio di aggiornamento 25 Questa versione ha un numero di build di V 3.10.43.76 ed è generalmente disponibile tramite l'aggiornamento automatico di ottobre 2020.</span><span class="sxs-lookup"><span data-stu-id="16cdc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="16cdc-110">Rilascio 25 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="16cdc-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="16cdc-111">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="16cdc-111">Bug fixes</span></span>

<span data-ttu-id="16cdc-112">**Ore e spesa**</span><span class="sxs-lookup"><span data-stu-id="16cdc-112">**Time and Expense**</span></span>

<span data-ttu-id="16cdc-113">Il problema seguente è stato risolto:</span><span class="sxs-lookup"><span data-stu-id="16cdc-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="16cdc-114">Grafico di inserimenti ore che mostra dati aggiuntivi basati su un intervallo troppo grande per essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="16cdc-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="16cdc-115">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="16cdc-115">**Resource Management**</span></span>

<span data-ttu-id="16cdc-116">Il problema seguente è stato risolto:</span><span class="sxs-lookup"><span data-stu-id="16cdc-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="16cdc-117">Aggiunto il codice del Package Deployer per saltare l'importazione della patch Universal Resource Scheduling se esiste già una patch di versione successiva.</span><span class="sxs-lookup"><span data-stu-id="16cdc-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="16cdc-118">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="16cdc-118">**Project Management**</span></span>

<span data-ttu-id="16cdc-119">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="16cdc-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="16cdc-120">Corretti arrotondamenti e discrepanze nei tassi di cambio con conseguente costo pianificato errato nella griglia di tracciabilità del progetto.</span><span class="sxs-lookup"><span data-stu-id="16cdc-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="16cdc-121">Supporta la possibilità di visualizzare due o più griglie di reazione sul modulo **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="16cdc-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="16cdc-122">Convalida fornita per la possibilità di assegnare un'attività oltre la data di fine del calendario, che si traduce in un'assegnazione di risorse non riuscita.</span><span class="sxs-lookup"><span data-stu-id="16cdc-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="16cdc-123">Gestione degli errori migliorata per la risoluzione dell'eccezione di riferimento nullo generata da:</span><span class="sxs-lookup"><span data-stu-id="16cdc-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="16cdc-124">Plug-in **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="16cdc-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="16cdc-125">**PreValidateProjectTaskCreate** quando un'attività di progetto viene creata senza un progetto associato</span><span class="sxs-lookup"><span data-stu-id="16cdc-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="16cdc-126">Plug-in **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="16cdc-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="16cdc-127">Plug-in **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="16cdc-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="16cdc-128">Plug-in **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="16cdc-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="16cdc-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="16cdc-129">**Sales**</span></span>

<span data-ttu-id="16cdc-130">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="16cdc-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="16cdc-131">Gestione degli errori migliorata per risolvere le eccezioni di riferimento nullo generate da **Copia progetto: gestione stime HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="16cdc-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="16cdc-132">**Non pronto per la fatturazione** in un **Backlog di fatturazione tempo e materiale** non cancella lo stato di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="16cdc-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="16cdc-133">Corretto l'errore di etichettatura dei pulsanti **Prezzi** nella scheda **Prezzo ruolo** e **Articoli di catalogo**.</span><span class="sxs-lookup"><span data-stu-id="16cdc-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]