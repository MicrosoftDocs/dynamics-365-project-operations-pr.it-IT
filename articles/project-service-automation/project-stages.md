---
title: Fasi di progetto
description: In questo argomento vengono fornite informazioni sulle fasi di progetto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752620"
---
# <a name="project-stages"></a><span data-ttu-id="80194-103">Fasi di progetto</span><span class="sxs-lookup"><span data-stu-id="80194-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="80194-104">Le fasi di progetto vengono aggiornate per riflettere lo stato del progetto durante l'esecuzione dello stesso.</span><span class="sxs-lookup"><span data-stu-id="80194-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="80194-105">Il processo aziendale predefinito aggiorna automaticamente alcune fasi del progetto mentre altre vengono aggiornate manualmente dal responsabile di progetto.</span><span class="sxs-lookup"><span data-stu-id="80194-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="80194-106">Le fasi seguenti sono definite nel processo aziendale predefinito:</span><span class="sxs-lookup"><span data-stu-id="80194-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="80194-107">Nuovo</span><span class="sxs-lookup"><span data-stu-id="80194-107">New</span></span>
- <span data-ttu-id="80194-108">Offerta</span><span class="sxs-lookup"><span data-stu-id="80194-108">Quote</span></span>
- <span data-ttu-id="80194-109">Piano</span><span class="sxs-lookup"><span data-stu-id="80194-109">Plan</span></span>
- <span data-ttu-id="80194-110">Consegna</span><span class="sxs-lookup"><span data-stu-id="80194-110">Deliver</span></span>
- <span data-ttu-id="80194-111">Completo</span><span class="sxs-lookup"><span data-stu-id="80194-111">Complete</span></span>
- <span data-ttu-id="80194-112">Chiusura</span><span class="sxs-lookup"><span data-stu-id="80194-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="80194-113">Nuovo</span><span class="sxs-lookup"><span data-stu-id="80194-113">New</span></span>

<span data-ttu-id="80194-114">Quando crei un progetto, la fase di progetto è impostata su **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="80194-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="80194-115">Se il progetto è stato creato a partire da un modello, potrebbe includere dati relativi a pianificazione, stime e team.</span><span class="sxs-lookup"><span data-stu-id="80194-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="80194-116">In caso contrario, è solo un abbozzo di progetto ed è necessario immettere gli altri componenti.</span><span class="sxs-lookup"><span data-stu-id="80194-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="80194-117">Offerta</span><span class="sxs-lookup"><span data-stu-id="80194-117">Quote</span></span>

<span data-ttu-id="80194-118">Quando associ un progetto a un'offerta o quando crei un progetto da un'offerta, la fase di progetto diventa **Offerta** e le date di inizio e di fine stimate vengono aggiornate.</span><span class="sxs-lookup"><span data-stu-id="80194-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="80194-119">Sebbene il progetto sia nella fase **Offerta**, nella scheda **Vendita** della pagina **Entità progetto** vengono visualizzati i dettagli dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="80194-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="80194-120">Piano</span><span class="sxs-lookup"><span data-stu-id="80194-120">Plan</span></span>

<span data-ttu-id="80194-121">Quando acquisisci un'offerta associata a un progetto e il progetto passa alla fase **Contratto**, la fase di progetto diventa **Piano**.</span><span class="sxs-lookup"><span data-stu-id="80194-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="80194-122">Quando il progetto è nella fase **Piano**, la pagina **Entità progetto** visualizza i dettagli del contratto.</span><span class="sxs-lookup"><span data-stu-id="80194-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="80194-123">Consegna</span><span class="sxs-lookup"><span data-stu-id="80194-123">Deliver</span></span>

<span data-ttu-id="80194-124">Quando il piano di progetto viene completato e sei pronto a iniziare il progetto, il responsabile di progetto deve aggiornare la fase di progetto a **Consegna** per indicare che il progetto è stato iniziato.</span><span class="sxs-lookup"><span data-stu-id="80194-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="80194-125">Completo</span><span class="sxs-lookup"><span data-stu-id="80194-125">Complete</span></span> 

<span data-ttu-id="80194-126">Quando il lavoro del progetto viene completato, il responsabile di progetto può aggiornare la fase a **Completo**.</span><span class="sxs-lookup"><span data-stu-id="80194-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="80194-127">Aggiornando la fase di progetto a **Completo**, il responsabile di progetto indica che il lavoro è completato al 100 per cento, ma che rimane aperto di modo che sia possibile registrare qualsiasi inserimento ore o voce di spesa in sospeso.</span><span class="sxs-lookup"><span data-stu-id="80194-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="80194-128">Chiusura</span><span class="sxs-lookup"><span data-stu-id="80194-128">Close</span></span>

<span data-ttu-id="80194-129">Quando tutte le registrazioni sono registrate per il progetto, il responsabile di progetto può aggiornare la fase a **Chiusura**.</span><span class="sxs-lookup"><span data-stu-id="80194-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="80194-130">A quel punto, nessuna transazione può essere registrata e il progetto diventa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="80194-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
