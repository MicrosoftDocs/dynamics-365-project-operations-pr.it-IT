---
title: Fasi del progetto
description: Questo argomento fornisce informazioni sulle fasi di progetto disponibili in Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996931"
---
# <a name="project-stages"></a><span data-ttu-id="07d11-103">Fasi del progetto</span><span class="sxs-lookup"><span data-stu-id="07d11-103">Project stages</span></span>

<span data-ttu-id="07d11-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="07d11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="07d11-105">Le fasi del progetto sono ideate per riflettere lo stato del progetto durante l'esecuzione dello stesso.</span><span class="sxs-lookup"><span data-stu-id="07d11-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="07d11-106">Le personalizzazioni possono essere utilizzate per aggiornare automaticamente le fasi con i flussi di processi aziendali, Power Automate o estensioni plug-in.</span><span class="sxs-lookup"><span data-stu-id="07d11-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="07d11-107">Le fasi seguenti sono definite nel flusso del processo aziendale predefinito:</span><span class="sxs-lookup"><span data-stu-id="07d11-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="07d11-108">Nuovo elemento</span><span class="sxs-lookup"><span data-stu-id="07d11-108">New</span></span>
- <span data-ttu-id="07d11-109">Offerta</span><span class="sxs-lookup"><span data-stu-id="07d11-109">Quote</span></span>
- <span data-ttu-id="07d11-110">Piano</span><span class="sxs-lookup"><span data-stu-id="07d11-110">Plan</span></span>
- <span data-ttu-id="07d11-111">Consegna</span><span class="sxs-lookup"><span data-stu-id="07d11-111">Deliver</span></span>
- <span data-ttu-id="07d11-112">Completamento</span><span class="sxs-lookup"><span data-stu-id="07d11-112">Complete</span></span>
- <span data-ttu-id="07d11-113">Chiuso</span><span class="sxs-lookup"><span data-stu-id="07d11-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="07d11-114">Nuovo elemento</span><span class="sxs-lookup"><span data-stu-id="07d11-114">New</span></span>

<span data-ttu-id="07d11-115">Quando crei un progetto, la fase di progetto è impostata su **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="07d11-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="07d11-116">Se il progetto è stato creato a partire da un modello, potrebbe includere dati relativi a pianificazione, stime e team.</span><span class="sxs-lookup"><span data-stu-id="07d11-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="07d11-117">In caso contrario, è un abbozzo di progetto ed è necessario immettere gli altri componenti.</span><span class="sxs-lookup"><span data-stu-id="07d11-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="07d11-118">Offerta</span><span class="sxs-lookup"><span data-stu-id="07d11-118">Quote</span></span>

<span data-ttu-id="07d11-119">Quando associ un progetto a un'offerta o quando crei un progetto da un'offerta, la fase di progetto diventa **Offerta** e le date di inizio e di fine stimate vengono aggiornate.</span><span class="sxs-lookup"><span data-stu-id="07d11-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="07d11-120">Sebbene il progetto sia nella fase **Offerta**, nella scheda **Vendita** della pagina **Entità progetto** vengono visualizzati i dettagli dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="07d11-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="07d11-121">Piano</span><span class="sxs-lookup"><span data-stu-id="07d11-121">Plan</span></span>

<span data-ttu-id="07d11-122">Quando acquisisci un'offerta associata a un progetto e il progetto passa alla fase **Contratto**, la fase di progetto diventa **Piano**.</span><span class="sxs-lookup"><span data-stu-id="07d11-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="07d11-123">Quando il progetto è nella fase **Piano**, la pagina **Entità progetto** visualizza i dettagli del contratto.</span><span class="sxs-lookup"><span data-stu-id="07d11-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="07d11-124">Consegna</span><span class="sxs-lookup"><span data-stu-id="07d11-124">Deliver</span></span>

<span data-ttu-id="07d11-125">Quando il piano di progetto viene completato e sei pronto a iniziare il progetto, il responsabile di progetto deve aggiornare la fase di progetto a **Consegna** per indicare che il progetto è stato iniziato.</span><span class="sxs-lookup"><span data-stu-id="07d11-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="07d11-126">Completo</span><span class="sxs-lookup"><span data-stu-id="07d11-126">Complete</span></span> 

<span data-ttu-id="07d11-127">Quando il lavoro del progetto viene completato, il responsabile di progetto può aggiornare la fase a **Completo**.</span><span class="sxs-lookup"><span data-stu-id="07d11-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="07d11-128">Aggiornando la fase di progetto a **Completo**, il responsabile di progetto indica che il lavoro è completato al 100 per cento, ma che rimane aperto di modo che sia possibile registrare qualsiasi inserimento ore o voce di spesa in sospeso.</span><span class="sxs-lookup"><span data-stu-id="07d11-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="07d11-129">Chiusura</span><span class="sxs-lookup"><span data-stu-id="07d11-129">Close</span></span>

<span data-ttu-id="07d11-130">Quando tutte le registrazioni sono registrate per il progetto, il responsabile di progetto può aggiornare la fase a **Chiusura**.</span><span class="sxs-lookup"><span data-stu-id="07d11-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="07d11-131">A quel punto, nessuna transazione può essere registrata e il progetto diventa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="07d11-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]