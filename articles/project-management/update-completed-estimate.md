---
title: Aggiornare la stima al completamento
description: Questo argomento fornisce informazioni sull'aggiornamento della proiezione dell'impegno su un progetto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286433"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="c6416-103">Aggiornare la stima al completamento</span><span class="sxs-lookup"><span data-stu-id="c6416-103">Update estimate at completion</span></span>

<span data-ttu-id="c6416-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="c6416-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c6416-105">È normale per un responsabile di progetto aggiornare le stime originali di un'attività.</span><span class="sxs-lookup"><span data-stu-id="c6416-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="c6416-106">Le nuove proiezioni di progetto sono la percezione delle stime di un responsabile di progetto, considerato lo stato corrente del progetto.</span><span class="sxs-lookup"><span data-stu-id="c6416-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="c6416-107">Tuttavia, non raccomandiamo la modifica delle cifre di riferimento da parte dei responsabili di progetto, poiché la linea di base del progetto rappresenta l'origine di riferimento stabilita per la pianificazione e la stima dei costi del progetto ed è stata concordata dalle parti interessate.</span><span class="sxs-lookup"><span data-stu-id="c6416-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="c6416-108">Vi sono due modi per un responsabile di progetto di eseguire una nuova proiezione del lavoro richiesto per le attività:</span><span class="sxs-lookup"><span data-stu-id="c6416-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="c6416-109">Sostituisci la stima predefinita di completamento con una nuova stima del lavoro richiesto rimanente effettivo per l'attività.</span><span class="sxs-lookup"><span data-stu-id="c6416-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="c6416-110">Sostituire la percentuale di avanzamento predefinita con una nuova stima dell'avanzamento effettivo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c6416-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="c6416-111">Ognuno di questi approcci genera un nuovo calcolo di stima di completamento, stima al completamento, percentuale di avanzamento e scostamento risorse previsto dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c6416-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="c6416-112">La stima di completamento, la stima al completamento e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento risorse.</span><span class="sxs-lookup"><span data-stu-id="c6416-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]