---
title: Novità o modifiche nella versione di aggiornamento 31 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 31 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999136"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="3fc7b-103">Novità o modifiche nella versione di aggiornamento 31 di Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="3fc7b-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3fc7b-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3fc7b-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3fc7b-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3fc7b-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3fc7b-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3fc7b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3fc7b-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 31 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="3fc7b-110">Questa versione ha il numero di build V3.10.52.77 ed è generalmente disponibile tramite un aggiornamento automatico a maggio 2021.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="3fc7b-111">Rilascio 31 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3fc7b-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3fc7b-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="3fc7b-112">Bug fixes</span></span>

<span data-ttu-id="3fc7b-113">**Ore e spesa**</span><span class="sxs-lookup"><span data-stu-id="3fc7b-113">**Time and Expense**</span></span>

<span data-ttu-id="3fc7b-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="3fc7b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3fc7b-115">I pulsanti di comando per il controllo dell'inserimento ore nella pagina **Risorsa prenotabile** erano confusi.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="3fc7b-116">Un'eccezione di riferimento nulla è stata generata in **Project.SetTrackingFields** quando si approva un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="3fc7b-117">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="3fc7b-117">**Resource Management**</span></span>

<span data-ttu-id="3fc7b-118">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="3fc7b-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="3fc7b-119">**Crea membro del team** non visualizza correttamente l'impostazione dei metadati di configurazione della prenotazione per **Stato Impegnato predefinito della prenotazione**.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="3fc7b-120">Quando si aggiorna da PSA 1.X a 3.X, il processo di aggiornamento non riesce per **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="3fc7b-121">**Vendite**</span><span class="sxs-lookup"><span data-stu-id="3fc7b-121">**Sales**</span></span>

<span data-ttu-id="3fc7b-122">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="3fc7b-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="3fc7b-123">Il ricavo effettivo converte gli importi nella valuta di progetto nella griglia di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="3fc7b-124">L'impostazione predefinita della valuta non è chiara quando si creano righe di giornale di registrazione, righe di preventivo e righe di contratto in scenari in cui la valuta di base di un'organizzazione è diversa dalla valuta di progetto.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="3fc7b-125">La query **In attesa di convalida del giornale di registrazione** non filtra per progetto.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="3fc7b-126">Le vendite rimanenti vengono calcolate in modo errato su un progetto.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="3fc7b-127">Le offerte basate su un contatto non riescono quando vengono create senza un listino prezzi.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="3fc7b-128">Non viene visualizzata alcuna casella di selezione di elaborazione quando selezioni **Conferma fattura**.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="3fc7b-129">Non viene visualizzata alcuna casella di selezione di elaborazione quando selezioni **Crea fattura**.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="3fc7b-130">La chiusura di un'offerta come persa non annulla le prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="3fc7b-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







