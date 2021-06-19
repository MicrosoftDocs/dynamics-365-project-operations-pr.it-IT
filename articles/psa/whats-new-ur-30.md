---
title: Novità o modifiche nella versione di aggiornamento 30 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 30 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010431"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="39b31-103">Novità o modifiche nella versione di aggiornamento 30 di Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="39b31-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="39b31-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="39b31-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="39b31-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="39b31-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="39b31-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="39b31-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="39b31-107">Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="39b31-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="39b31-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="39b31-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="39b31-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 30 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="39b31-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="39b31-110">Questa versione ha il numero di build V3.10.51.61 ed è generalmente disponibile tramite un aggiornamento automatico nell'aprile 2021.</span><span class="sxs-lookup"><span data-stu-id="39b31-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="39b31-111">Rilascio 30 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="39b31-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="39b31-112">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="39b31-112">Bug fixes</span></span>

<span data-ttu-id="39b31-113">**Ore e spesa**</span><span class="sxs-lookup"><span data-stu-id="39b31-113">**Time and Expense**</span></span>

<span data-ttu-id="39b31-114">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="39b31-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="39b31-115">Si verifica un errore quando si crea e si salva un inserimento ore nella pagina **Creazione rapida** se il campo **Ruolo** viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="39b31-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="39b31-116">Il filtro Inserimento ora applica l'operatore di filtro errato.</span><span class="sxs-lookup"><span data-stu-id="39b31-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="39b31-117">I fogli presenze copiati non sono visualizzati automaticamente quando selezioni **Copia settimana** nel controllo dell'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="39b31-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="39b31-118">**Gestione risorse**</span><span class="sxs-lookup"><span data-stu-id="39b31-118">**Resource Management**</span></span>

<span data-ttu-id="39b31-119">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="39b31-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="39b31-120">Quando estendi una prenotazione, lo stato di prenotazione assegnato alla prenotazione definitiva non è corretto.</span><span class="sxs-lookup"><span data-stu-id="39b31-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="39b31-121">L'estensione di una prenotazione rispetta lo stato di prenotazione definito come **Confermato** nei metadati di configurazione della prenotazione.</span><span class="sxs-lookup"><span data-stu-id="39b31-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="39b31-122">Quando non viene specificato uno stato di prenotazione valido, il messaggio di errore non viene localizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="39b31-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="39b31-123">**Gestione progetti**</span><span class="sxs-lookup"><span data-stu-id="39b31-123">**Project Management**</span></span>

<span data-ttu-id="39b31-124">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="39b31-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="39b31-125">I progetti non possono essere creati in una valuta e includere attività correlate in un'altra valuta.</span><span class="sxs-lookup"><span data-stu-id="39b31-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="39b31-126">**Vendite**</span><span class="sxs-lookup"><span data-stu-id="39b31-126">**Sales**</span></span>

<span data-ttu-id="39b31-127">Sono stati risolti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="39b31-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="39b31-128">Quando un listino prezzi viene copiato, i prezzi non vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="39b31-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="39b31-129">La chiusura di un'offerta come acquisita non riesce quando il dettaglio del costo comporta un valore per l'origine.</span><span class="sxs-lookup"><span data-stu-id="39b31-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="39b31-130">Nell'entità **Attività di progetto**, **Costo stimato** è stato rinominato in **Costo pianificato (base)**.</span><span class="sxs-lookup"><span data-stu-id="39b31-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="39b31-131">Quando vengono create o eliminate fatture, viene generata un'eccezione di riferimento nulla.</span><span class="sxs-lookup"><span data-stu-id="39b31-131">A null reference exception is generated when invoices are created or deleted.</span></span>
