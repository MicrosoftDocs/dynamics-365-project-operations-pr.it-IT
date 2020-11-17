---
title: Novità o modifiche nella versione di aggiornamento 14 di Project Service Automation V3
description: Questo argomento fornisce informazioni sulle novità dell'aggiornamento rilascio 14 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124823"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="1fcf1-103">Versione di aggiornamento di Project Service Automation 14, V3</span><span class="sxs-lookup"><span data-stu-id="1fcf1-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="1fcf1-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="1fcf1-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="1fcf1-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1fcf1-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1fcf1-107">Per aggiornare a questa versione, visitare l'interfaccia di amministrazione di Dynamics 365 online e andare alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="1fcf1-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1fcf1-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1fcf1-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 14 di PSA V3.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="1fcf1-110">Questa versione ha il numero di build V3.10.4.21 ed è disponibile secondo la seguente pianificazione:</span><span class="sxs-lookup"><span data-stu-id="1fcf1-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="1fcf1-111">**Disponibilità generale (aggiornamento automatico):** gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="1fcf1-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="1fcf1-112">**Aggiornamento automatico:** febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="1fcf1-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="1fcf1-113">Rilascio 14 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1fcf1-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="1fcf1-114">Miglioramenti</span><span class="sxs-lookup"><span data-stu-id="1fcf1-114">Enhancements</span></span>

- <span data-ttu-id="1fcf1-115">Sales</span><span class="sxs-lookup"><span data-stu-id="1fcf1-115">Sales</span></span>

     - <span data-ttu-id="1fcf1-116">I valori personalizzati del campo **Dettagli riga di offerta** vengono copiati in **Dettagli riga contratto di progetto** quando un'offerta viene aggiornata **come acquisita**.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="1fcf1-117">I progetti confermati possono essere **chiusi come persi**.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="1fcf1-118">Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="1fcf1-118">Resource Management</span></span>

     - <span data-ttu-id="1fcf1-119">Quando si estendono le prenotazioni, verrà visualizzata una finestra di dialogo per la conferma degli utenti con il riepilogo dei risultati della prenotazione e fornire un collegamento a Gestisci prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="1fcf1-120">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="1fcf1-120">Bug fixes</span></span>

- <span data-ttu-id="1fcf1-121">Tempo e spesa</span><span class="sxs-lookup"><span data-stu-id="1fcf1-121">Time and Expense</span></span>

     - <span data-ttu-id="1fcf1-122">Risolto: migliorata l'esperienza dell'utente quando l'utente non seleziona alcuna voce da correggere.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="1fcf1-123">Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="1fcf1-123">Resource Management</span></span>

     - <span data-ttu-id="1fcf1-124">Risolto: la prenotazione di una risorsa più volte crea l'overflow del nome della risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="1fcf1-125">Sales</span><span class="sxs-lookup"><span data-stu-id="1fcf1-125">Sales</span></span>

     - <span data-ttu-id="1fcf1-126">Risolto: il prezzo di vendita totale non viene calcolato fino a quando l'utente non inserisce anche un prezzo di costo per le stime di spesa in un progetto.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="1fcf1-127">Risolto: la chiusura di un'offerta come **acquisita** non riesce se il contratto di progetto associato non è in stato di **Bozza**.</span><span class="sxs-lookup"><span data-stu-id="1fcf1-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

