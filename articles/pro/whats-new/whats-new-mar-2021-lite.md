---
title: Novità di marzo 2021 - Distribuzione semplice di Project Operations
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di marzo 2021 di Distribuzione semplice di Project Operations.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: efddb96b2cb428b9dc0488c32eb5670d01322bcb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993871"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="4043f-103">Novità di marzo 2021 - Distribuzione semplice di Project Operations</span><span class="sxs-lookup"><span data-stu-id="4043f-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="4043f-104">_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="4043f-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4043f-105">Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4043f-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="4043f-106">Project Operations in ambiente Dataverse versione 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="4043f-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="4043f-107">Aggiornamenti di qualità</span><span class="sxs-lookup"><span data-stu-id="4043f-107">Quality updates</span></span>

| <span data-ttu-id="4043f-108">**Area funzionalità**</span><span class="sxs-lookup"><span data-stu-id="4043f-108">**Feature area**</span></span> | <span data-ttu-id="4043f-109">**Numero di riferimento**</span><span class="sxs-lookup"><span data-stu-id="4043f-109">**Reference number**</span></span> | <span data-ttu-id="4043f-110">**Aggiornamento di qualità**</span><span class="sxs-lookup"><span data-stu-id="4043f-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4043f-111">Determinazione dei prezzi e fatturazione</span><span class="sxs-lookup"><span data-stu-id="4043f-111">Billing and pricing</span></span> | <span data-ttu-id="4043f-112">2133873</span><span class="sxs-lookup"><span data-stu-id="4043f-112">2133873</span></span> | <span data-ttu-id="4043f-113">Risolto il problema della visualizzazione del simbolo di valuta **Prezzo di vendita unitario** nella griglia **Stime di spesa**.</span><span class="sxs-lookup"><span data-stu-id="4043f-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="4043f-114">Determinazione dei prezzi e fatturazione</span><span class="sxs-lookup"><span data-stu-id="4043f-114">Billing and pricing</span></span> | <span data-ttu-id="4043f-115">2174616</span><span class="sxs-lookup"><span data-stu-id="4043f-115">2174616</span></span> | <span data-ttu-id="4043f-116">Quando si chiude un'offerta, il listino prezzi personalizzato del contratto viene implementato nei dettagli della riga del contratto che vengono copiati dall'offerta.</span><span class="sxs-lookup"><span data-stu-id="4043f-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="4043f-117">Gestione delle opportunità</span><span class="sxs-lookup"><span data-stu-id="4043f-117">Opportunity Management</span></span> | <span data-ttu-id="4043f-118">2167475</span><span class="sxs-lookup"><span data-stu-id="4043f-118">2167475</span></span> | <span data-ttu-id="4043f-119">Importo fisso dell'imposta nella fattura di rettifica che ha originato un movimento effettivo non fatturato.</span><span class="sxs-lookup"><span data-stu-id="4043f-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="4043f-120">Gestione delle opportunità</span><span class="sxs-lookup"><span data-stu-id="4043f-120">Opportunity Management</span></span> | <span data-ttu-id="4043f-121">2176285</span><span class="sxs-lookup"><span data-stu-id="4043f-121">2176285</span></span> | <span data-ttu-id="4043f-122">L'importo dell'imposta non deve essere copiato dai dettagli della riga di offerta/contratto di vendita nei dettagli della riga di offerta/contratto di costo.</span><span class="sxs-lookup"><span data-stu-id="4043f-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="4043f-123">Gestione delle opportunità</span><span class="sxs-lookup"><span data-stu-id="4043f-123">Opportunity Management</span></span> | <span data-ttu-id="4043f-124">2188079</span><span class="sxs-lookup"><span data-stu-id="4043f-124">2188079</span></span> | <span data-ttu-id="4043f-125">La regola di fatturazione suddivisa non deve essere creata per i contratti che non sono basati su lavoro.</span><span class="sxs-lookup"><span data-stu-id="4043f-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="4043f-126">Pianificazione e rilevamento</span><span class="sxs-lookup"><span data-stu-id="4043f-126">Planning and Tracking</span></span> | <span data-ttu-id="4043f-127">2138853</span><span class="sxs-lookup"><span data-stu-id="4043f-127">2138853</span></span> | <span data-ttu-id="4043f-128">Funzione di copia del progetto aggiornata per garantire che le righe di stima delle spese che fanno riferimento alle attività vengano copiate nel progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4043f-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="4043f-129">Pianificazione e rilevamento</span><span class="sxs-lookup"><span data-stu-id="4043f-129">Planning and Tracking</span></span> | <span data-ttu-id="4043f-130">2173259</span><span class="sxs-lookup"><span data-stu-id="4043f-130">2173259</span></span> | <span data-ttu-id="4043f-131">Funzione di copia del progetto aggiornata per garantire che non visualizzi il messaggio di errore **Copia di WBS** in determinati scenari.</span><span class="sxs-lookup"><span data-stu-id="4043f-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="4043f-132">Ore e spesa</span><span class="sxs-lookup"><span data-stu-id="4043f-132">Time and Expense</span></span> | <span data-ttu-id="4043f-133">2148910</span><span class="sxs-lookup"><span data-stu-id="4043f-133">2148910</span></span> | <span data-ttu-id="4043f-134">Risolto il problema di visualizzazione con la pagina **Modifica inserimento** nella griglia **Inserimento ore**.</span><span class="sxs-lookup"><span data-stu-id="4043f-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="4043f-135">Ore e spesa</span><span class="sxs-lookup"><span data-stu-id="4043f-135">Time and Expense</span></span> | <span data-ttu-id="4043f-136">2159798</span><span class="sxs-lookup"><span data-stu-id="4043f-136">2159798</span></span> | <span data-ttu-id="4043f-137">Controlli rafforzati per garantire che le voci di spesa approvate non possano essere modificate.</span><span class="sxs-lookup"><span data-stu-id="4043f-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


