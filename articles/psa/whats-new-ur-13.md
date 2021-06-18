---
title: Novità o modifiche nella versione di aggiornamento 13 di Project Service Automation V3
description: Questo argomento fornisce informazioni sulle novità dell'aggiornamento rilascio 13 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: c328821064065e19938406856d327f690f577e7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000306"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="d198b-103">Versione di aggiornamento di Project Service Automation 13, V3</span><span class="sxs-lookup"><span data-stu-id="d198b-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d198b-104">Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="d198b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="d198b-105">Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="d198b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d198b-106">Questa versione è compatibile con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d198b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d198b-107">Per aggiornare a questa versione, visitare l'interfaccia di amministrazione di Dynamics 365 online e andare alla pagina delle soluzioni per installare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d198b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="d198b-108">Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d198b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d198b-109">Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 13 di Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="d198b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="d198b-110">Questa versione ha il numero di build V3.10.3.18 ed è disponibile secondo la seguente pianificazione:</span><span class="sxs-lookup"><span data-stu-id="d198b-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="d198b-111">**Disponibilità generale (aggiornamento automatico):** novembre 2019</span><span class="sxs-lookup"><span data-stu-id="d198b-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="d198b-112">**Aggiornamento automatico:** dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="d198b-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="d198b-113">Rilascio 13 dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d198b-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="d198b-114">Correzioni di bug</span><span class="sxs-lookup"><span data-stu-id="d198b-114">Bug fixes</span></span>

- <span data-ttu-id="d198b-115">Tempo e spesa</span><span class="sxs-lookup"><span data-stu-id="d198b-115">Time and Expense</span></span>

     - <span data-ttu-id="d198b-116">Risolto: la funzionalità di ricerca nella pagina **Approvazione delle spese** non funziona durante la ricerca per scopo della spesa.</span><span class="sxs-lookup"><span data-stu-id="d198b-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="d198b-117">Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="d198b-117">Resource Management</span></span>

     - <span data-ttu-id="d198b-118">Risolto: i numeri nella riconciliazione sono stati aggiornati per essere giustificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="d198b-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="d198b-119">Risolto: le risorse denominate non possono essere assegnate alle attività tramite la scheda **Pianifica**.</span><span class="sxs-lookup"><span data-stu-id="d198b-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="d198b-120">Gestione progetti</span><span class="sxs-lookup"><span data-stu-id="d198b-120">Project Management</span></span>

     - <span data-ttu-id="d198b-121">Risolto: l'eccezione di riferimento null durante l'assegnazione del membro del team quando in **TransactionType** mancano le informazioni di impostazione per **Unità** e **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="d198b-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="d198b-122">Sales</span><span class="sxs-lookup"><span data-stu-id="d198b-122">Sales</span></span>

     - <span data-ttu-id="d198b-123">Risolto: i record duplicati del tipo di transazione restituiscono un errore quando vengono creati i record del prezzo del ruolo.</span><span class="sxs-lookup"><span data-stu-id="d198b-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="d198b-124">Risolto: pulsanti aggiuntivi per **Nuova opportunità**, **Offerta**, **Riga ordine** e **Aggiungi prodotto** sono visibili nei comandi per Opportunità, Offerte, Prodotti ordine e nella griglia secondaria Righe basate su progetto.</span><span class="sxs-lookup"><span data-stu-id="d198b-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]