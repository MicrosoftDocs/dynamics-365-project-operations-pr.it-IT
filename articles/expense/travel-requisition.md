---
title: Richieste di viaggio
description: In questo argomento vengono fornite informazioni sulle richieste di viaggio.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906216"
---
# <a name="travel-requisitions"></a><span data-ttu-id="6160e-103">Richieste di viaggio</span><span class="sxs-lookup"><span data-stu-id="6160e-103">Travel requisitions</span></span>

<span data-ttu-id="6160e-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="6160e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6160e-105">Una richiesta di viaggio elenca le spese che saranno sostenute ai fini del viaggio.</span><span class="sxs-lookup"><span data-stu-id="6160e-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="6160e-106">Una richiesta di viaggio viene inviata per la revisione e può essere utilizzata per autorizzare le spese.</span><span class="sxs-lookup"><span data-stu-id="6160e-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="6160e-107">Potrebbe esserti richiesto di inviare una richiesta di viaggio prima di sostenere eventuali spese addebitate all'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="6160e-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="6160e-108">Questo requisito si applica indipendentemente dal fatto che addebiti le spese su una carta di credito aziendale, spendi denaro che hai ricevuto da un anticipo in contanti o sostieni spese vive che saranno rimborsate dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="6160e-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="6160e-109">Le richieste di viaggio e i criteri possono essere utilizzati per aiutare a gestire le spese dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="6160e-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="6160e-110">Ad esempio, se l'organizzazione sta lavorando a un progetto a prezzo fisso che richiede viaggi, le spese di viaggio dei membri del team del progetto devono rientrare nel budget del progetto.</span><span class="sxs-lookup"><span data-stu-id="6160e-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="6160e-111">Richiedendo che le spese di viaggio siano approvate prima che vengano sostenute, l'organizzazione può aiutare a garantire che il progetto rispetti il budget.</span><span class="sxs-lookup"><span data-stu-id="6160e-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="6160e-112">Configurazione</span><span class="sxs-lookup"><span data-stu-id="6160e-112">Configuration</span></span> 

<span data-ttu-id="6160e-113">Le richieste di viaggio possono essere configurate come "obbligatorie" abilitando il parametro "La preautorizzazione del viaggio è obbligatoria" nei parametri di Gestione spese.</span><span class="sxs-lookup"><span data-stu-id="6160e-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="6160e-114">Creare e inviare una richiesta di viaggio</span><span class="sxs-lookup"><span data-stu-id="6160e-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="6160e-115">Vai a **Spese personali: richiesta di viaggio** e seleziona **Nuova richiesta di viaggio**.</span><span class="sxs-lookup"><span data-stu-id="6160e-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="6160e-116">Immetti uno scopo e una destinazione per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6160e-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="6160e-117">Nel campo **Descrizione viaggio**, immetti eventuali informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="6160e-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="6160e-118">Per ciascuna delle spese previste, ad esempio volo, vitto o noleggio auto, crea una voce di spesa.</span><span class="sxs-lookup"><span data-stu-id="6160e-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="6160e-119">Includi la data stimata, l'importo stimato e la valuta per ciascuna spesa.</span><span class="sxs-lookup"><span data-stu-id="6160e-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="6160e-120">Quando hai finito di aggiungere le spese previste, seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="6160e-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="6160e-121">Quando sei pronto per inviare la richiesta di viaggio, seleziona **Flusso di lavoro** > **Invia**.</span><span class="sxs-lookup"><span data-stu-id="6160e-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="6160e-122">Puoi visualizzare le richieste di viaggio approvate in **Spese personali: richiesta di viaggio**.</span><span class="sxs-lookup"><span data-stu-id="6160e-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="6160e-123">Visualizzare le richieste di viaggio disponibili</span><span class="sxs-lookup"><span data-stu-id="6160e-123">View available travel requisitions</span></span>

<span data-ttu-id="6160e-124">Puoi visualizzare tutte le richieste di viaggio in **Spese personali: richieste di viaggio**.</span><span class="sxs-lookup"><span data-stu-id="6160e-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="6160e-125">Approvare le richieste di viaggio</span><span class="sxs-lookup"><span data-stu-id="6160e-125">Approve travel requisitions</span></span>

<span data-ttu-id="6160e-126">Seleziona la richiesta di viaggio da approvare, quindi seleziona **Flusso di lavoro** > **Approva**.</span><span class="sxs-lookup"><span data-stu-id="6160e-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="6160e-127">Inviare una nota spese utilizzando la richiesta di viaggio approvata</span><span class="sxs-lookup"><span data-stu-id="6160e-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="6160e-128">Crea una nuova nota spese e nell'intestazione della nota spese e dall'elenco delle richieste di viaggio approvate seleziona **Eseguire il mapping alla richiesta di viaggio**.</span><span class="sxs-lookup"><span data-stu-id="6160e-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="6160e-129">Il campo **Importo richiesta di viaggio** viene aggiornato automaticamente nell'intestazione della nota spese.</span><span class="sxs-lookup"><span data-stu-id="6160e-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="6160e-130">Aggiungi tutte le spese sostenute per il viaggio.</span><span class="sxs-lookup"><span data-stu-id="6160e-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="6160e-131">Se il campo **Preautorizzata** è abilitato, l'importo riconciliato e l'importo autorizzato per la categoria di spesa specifica verranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="6160e-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="6160e-132">Quando si esegue il mapping di una nota spese a una richiesta di viaggio approvata, l'importo della transazione non può essere maggiore dell'importo autorizzato.</span><span class="sxs-lookup"><span data-stu-id="6160e-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
