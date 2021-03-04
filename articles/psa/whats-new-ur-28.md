---
title: Novità o modifiche nella versione di aggiornamento 28 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 28 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150628"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="af79c-103">Novità o modifiche nella versione di aggiornamento 28 di Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="af79c-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="af79c-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="af79c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="af79c-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="af79c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="af79c-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="af79c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="af79c-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="af79c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="af79c-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="af79c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="af79c-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per Project Service Automation V3, rilascio di aggiornamento 28. Questa versione ha un numero di build di V3.10.46.32 ed è generalmente disponibile tramite l'aggiornamento automatico di gennaio 2021.</span><span class="sxs-lookup"><span data-stu-id="af79c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="af79c-110">Rilascio 28 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="af79c-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="af79c-111">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="af79c-111">Bug fixes</span></span>

<span data-ttu-id="af79c-112">**Ore e spesa**</span><span class="sxs-lookup"><span data-stu-id="af79c-112">**Time and Expense**</span></span>

<span data-ttu-id="af79c-113">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="af79c-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="af79c-114">Gli utenti possono utilizzare **Modifica in blocco** per aggiornare gli inserimenti ore che sono stati approvati e inviati.</span><span class="sxs-lookup"><span data-stu-id="af79c-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="af79c-115">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="af79c-115">**Project Management**</span></span>

<span data-ttu-id="af79c-116">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="af79c-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="af79c-117">Nei casi in cui il GUID dell'attività viene interpretato come un numero, le attività non possono essere aperte per la modifica utilizzando **Modifica attività** nella barra multifunzione nella pagina **Struttura di suddivisione del lavoro**.</span><span class="sxs-lookup"><span data-stu-id="af79c-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="af79c-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="af79c-118">**Sales**</span></span>

<span data-ttu-id="af79c-119">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="af79c-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="af79c-120">Viene generata un'eccezione di riferimento null quando il plug-in **GetEstimatesForProject** viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="af79c-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="af79c-121">**Contrassegna come pronto per la fatturazione** sulla griglia passaggi fondamentali aggiorna solo parzialmente gli attributi, ad eccezione dell'attributo **InvoiceStatus** che viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="af79c-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

