---
title: Richiesta Schedule of Expenditures of Federal Awards
description: Questo argomento fornisce informazioni sulla richiesta Schedule of Expenditures of Federal Awards.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010071"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="c1cf5-103">Richiesta Schedule of Expenditures of Federal Awards</span><span class="sxs-lookup"><span data-stu-id="c1cf5-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1cf5-104">Ai sensi dell'Office of Management and Budget Circular A-133, le agenzie che ricevono fondi federali sono soggette sono soggetti a requisiti di controllo, noti anche come controlli singoli.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="c1cf5-105">Il processo di controllo viene utilizzato per segnalare le entrate e le spese relative a sovvenzioni federali su base ricorrente.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="c1cf5-106">Parte del report del controllo singolo include la richiesta Schedule of Expenditures of Federal Awards (SEFA).</span><span class="sxs-lookup"><span data-stu-id="c1cf5-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="c1cf5-107">La richiesta Schedule of Expenditures of Federal Awards include il titolo e il numero del Catalog of Federal Domestic Assistance (CFDA), il numero della sovvenzione, l'anno della sovvenzione, il nome dell'agenzia federale che fornisce i fondi e il nome dell'entità pass-through.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="c1cf5-108">La richiesta è per un periodo specifico.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="c1cf5-109">In genere, il periodo corrisponde al periodo del rendiconto finanziario, ovvero un anno fiscale.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="c1cf5-110">La richiesta include le sovvenzioni con le date di proiezione comprese nell'intervallo di date selezionato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="c1cf5-111">La colonna **Agenzia concedente** della richiesta mostra il cliente della sovvenzione o, per una sovvenzione pass-through, l'agenzia concedente.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="c1cf5-112">Per una sovvenzione pass-through, la colonna **Agenzia pass-through** mostra il cliente della sovvenzione.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="c1cf5-113">Se la sovvenzione non è pass-through, la colonna **Agenzia pass-through** è vuota.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="c1cf5-114">Impostare i cluster CFDA</span><span class="sxs-lookup"><span data-stu-id="c1cf5-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="c1cf5-115">È necessario impostare i cluster CFDA che possono essere associati ai numeri CFDA nella richiesta Schedule of Expenditures of Federal Awards.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="c1cf5-116">Vai a **Gestione progetti e contabilità \> Imposta \> Sovvenzioni \> Cluster Catalog of Federal Domestic Assistance**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="c1cf5-117">Seleziona **Nuovo** per creare un cluster CFDA.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="c1cf5-118">Immetti il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="c1cf5-119">Selezionare **Salva** per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="c1cf5-120">Impostare i numeri CFDA</span><span class="sxs-lookup"><span data-stu-id="c1cf5-120">Set up CFDA numbers</span></span>

<span data-ttu-id="c1cf5-121">È necessario impostare i numeri CFDA che possono essere aggiunti alle sovvenzioni e inclusi nella richiesta Schedule of Expenditures of Federal Awards.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="c1cf5-122">Vai a **Gestione progetti e contabilità \> Imposta \> Sovvenzioni \> Numeri Catalog of Federal Domestic Assistance**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="c1cf5-123">Seleziona **Nuovo** per creare un numero CFDA.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="c1cf5-124">Nella colonna **Numero** immettere il numero CFDA.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="c1cf5-125">Premi il tasto **Tabulazione**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="c1cf5-126">Nella colonna **Descrizione** immetti il titolo CFDA.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="c1cf5-127">Premi il tasto **Tabulazione**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="c1cf5-128">Facoltativo: nel campo **Cluster programma** aggiungi il cluster CFDA appropriato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="c1cf5-129">Selezionare **Salva** per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="c1cf5-130">Impostare sovvenzioni da dichiarare per la richiesta Schedule of Expenditures of Federal Awards</span><span class="sxs-lookup"><span data-stu-id="c1cf5-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="c1cf5-131">Vai a **Gestione progetti e contabilità \> Sovvenzioni \> Sovvenzioni** e seleziona una sovvenzione esistente.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="c1cf5-132">Nella scheda dettaglio **Impostazione** nel campo **Catalog of Federal Domestic Assistance** assegna il numero CFDA.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="c1cf5-133">Il numero CFDA sulla sovvenzione determina il cluster CFDA per la dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="c1cf5-134">Nella scheda dettaglio **Informazioni sul contatto** immetti le informazioni sul concedente procedendo nel seguente modo:</span><span class="sxs-lookup"><span data-stu-id="c1cf5-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="c1cf5-135">Nel campo **Cliente sovvenzione** inserisci il cliente responsabile della sovvenzione.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="c1cf5-136">Per una sovvenzione esistente, queste informazioni potrebbero essere già state inserite.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="c1cf5-137">Indicare se il cliente della sovvenzione è il finanziatore.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="c1cf5-138">Se il cliente della sovvenzione è il finanziatore, lascia la casella di controllo **Pass-through** deselezionata.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="c1cf5-139">Se il finanziatore è un altro cliente e il cliente della sovvenzione è responsabile della spesa e del monitoraggio del denaro, seleziona la casella di controllo **Pass-through**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="c1cf5-140">Se hai selezionato la casella di controllo **Pass-through** nel passaggio precedente, nel campo **Agenzia concedente** immetti il cliente che ha fornito la sovvenzione.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="c1cf5-141">L'agenzia concedente e il cliente della sovvenzione non possono essere lo stesso cliente.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="c1cf5-142">Ecco un esempio di sovvenzione pass-through:</span><span class="sxs-lookup"><span data-stu-id="c1cf5-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="c1cf5-143">Il governo federale ha finanziato un progetto infrastrutturale per uno stato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="c1cf5-144">Il governo federale ha dato i soldi allo stato da spendere.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="c1cf5-145">In questo caso, il governo federale è l'agenzia concedente e lo stato è il cliente della sovvenzione.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="c1cf5-146">Quando si attiva per la prima volta la funzione, i numeri CFDA iniziali verranno inseriti utilizzando i numeri esistenti sulle sovvenzioni.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="c1cf5-147">Escludere le sovvenzioni dalla dichiarazione SEFA in base al tipo di sovvenzione</span><span class="sxs-lookup"><span data-stu-id="c1cf5-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="c1cf5-148">Vai a **Gestione progetti e contabilità \> Imposta \> Concessioni \> Tipi di concessione**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="c1cf5-149">Nella scheda dettaglio **Informazioni predefinite** seleziona la casella di controllo **Escludi da Schedule of Expenditures of Federal Awards**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="c1cf5-150">Selezionare **Salva** per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="c1cf5-151">Eseguire la richiesta Schedule of Expenditures of Federal Awards</span><span class="sxs-lookup"><span data-stu-id="c1cf5-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="c1cf5-152">Vai a **Gestione progetti e contabilità \> Report e richieste di informazioni \> Richiesta di sovvenzione \> Schedule of Expenditures of Federal Awards**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="c1cf5-153">Nella sezione **Parametri** segui questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="c1cf5-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="c1cf5-154">Nel campo **Intervallo date** seleziona il codice per l'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="c1cf5-155">In alternativa, nei campi **Data iniziale** e **Data finale** definisci l'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="c1cf5-156">Facoltativo: per includere solo le transazioni fatturate come entrate nella richiesta, imposta l'opzione **Includi solo ricavi fatturati** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="c1cf5-157">Colonne</span><span class="sxs-lookup"><span data-stu-id="c1cf5-157">Columns</span></span>

<span data-ttu-id="c1cf5-158">La richiesta Schedule of Expenditures of Federal Awards include le seguenti colonne:</span><span class="sxs-lookup"><span data-stu-id="c1cf5-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="c1cf5-159">Nome del cluster Catalog of Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="c1cf5-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="c1cf5-160">Agenzia concedente</span><span class="sxs-lookup"><span data-stu-id="c1cf5-160">Grantor agency</span></span>
- <span data-ttu-id="c1cf5-161">Agenzia pass-through</span><span class="sxs-lookup"><span data-stu-id="c1cf5-161">Pass-through agency</span></span>
- <span data-ttu-id="c1cf5-162">Nome della sovvenzione</span><span class="sxs-lookup"><span data-stu-id="c1cf5-162">Grant name</span></span>
- <span data-ttu-id="c1cf5-163">ID sovvenzione</span><span class="sxs-lookup"><span data-stu-id="c1cf5-163">Grant ID</span></span>
- <span data-ttu-id="c1cf5-164">ID applicazione sovvenzione</span><span class="sxs-lookup"><span data-stu-id="c1cf5-164">Grant application ID</span></span>
- <span data-ttu-id="c1cf5-165">Catalog of Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="c1cf5-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="c1cf5-166">Ricevute</span><span class="sxs-lookup"><span data-stu-id="c1cf5-166">Receipts</span></span>
- <span data-ttu-id="c1cf5-167">Spese</span><span class="sxs-lookup"><span data-stu-id="c1cf5-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]