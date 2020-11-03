---
title: Aggiornare la stima al completamento
description: Questo argomento fornisce informazioni sull'aggiornamento della proiezione dell'impegno su un progetto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079059"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="f4d39-103">Aggiornare la stima al completamento</span><span class="sxs-lookup"><span data-stu-id="f4d39-103">Update estimate at completion</span></span>

<span data-ttu-id="f4d39-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="f4d39-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f4d39-105">È normale per un responsabile di progetto aggiornare le stime originali di un'attività.</span><span class="sxs-lookup"><span data-stu-id="f4d39-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="f4d39-106">Le nuove proiezioni di progetto sono la percezione delle stime di un responsabile di progetto, considerato lo stato corrente del progetto.</span><span class="sxs-lookup"><span data-stu-id="f4d39-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="f4d39-107">Tuttavia, non raccomandiamo la modifica delle cifre di riferimento da parte dei responsabili di progetto, poiché la linea di base del progetto rappresenta l'origine di riferimento stabilita per la pianificazione e la stima dei costi del progetto ed è stata concordata dalle parti interessate.</span><span class="sxs-lookup"><span data-stu-id="f4d39-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="f4d39-108">Vi sono due modi per un responsabile di progetto di eseguire una nuova proiezione del lavoro richiesto per le attività:</span><span class="sxs-lookup"><span data-stu-id="f4d39-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="f4d39-109">Sostituisci la stima predefinita di completamento con una nuova stima del lavoro richiesto rimanente effettivo per l'attività.</span><span class="sxs-lookup"><span data-stu-id="f4d39-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="f4d39-110">Sostituire la percentuale di avanzamento predefinita con una nuova stima dell'avanzamento effettivo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="f4d39-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="f4d39-111">Ognuno di questi approcci genera un nuovo calcolo di stima di completamento, stima al completamento, percentuale di avanzamento e scostamento risorse previsto dell'attività.</span><span class="sxs-lookup"><span data-stu-id="f4d39-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="f4d39-112">La stima di completamento, la stima al completamento e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento risorse.</span><span class="sxs-lookup"><span data-stu-id="f4d39-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
