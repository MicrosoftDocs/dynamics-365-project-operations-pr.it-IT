---
title: Panoramica delle dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni sulle dimensioni di determinazione dei prezzi in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078983"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="2e8fb-103">Panoramica delle dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="2e8fb-103">Pricing dimensions overview</span></span>

<span data-ttu-id="2e8fb-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="2e8fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2e8fb-105">Le dimensioni utilizzate nelle risorse umane per impostare prezzi e costi rientrano in due categorie:</span><span class="sxs-lookup"><span data-stu-id="2e8fb-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="2e8fb-106">Persone</span><span class="sxs-lookup"><span data-stu-id="2e8fb-106">People</span></span>
- <span data-ttu-id="2e8fb-107">Lavoro pianificato</span><span class="sxs-lookup"><span data-stu-id="2e8fb-107">Planned work</span></span>

<span data-ttu-id="2e8fb-108">Di conseguenza, sono disponibili due tipi di valori per le dimensioni di determinazione dei prezzi:</span><span class="sxs-lookup"><span data-stu-id="2e8fb-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="2e8fb-109">**Set di opzioni** : dimensioni che sono enumerazioni fisse per un set di valori.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="2e8fb-110">**Valori basati su entità** : dimensioni che possono essere un set di valori differenti.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="2e8fb-111">Dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="2e8fb-111">Pricing dimensions</span></span>

<span data-ttu-id="2e8fb-112">Dynamics 365 Project Operations viene fornito con un set predefinito di dimensioni dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="2e8fb-113">Puoi visualizzare queste dimensioni di determinazione dei prezzi in **Project Operations** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="2e8fb-114">Nel record del parametro, nella scheda **Dimensione di determinazione dei prezzi basata su importo** , verifica che i campi **Vendite applicabili a** e **Costo applicabile a** del ruolo **msdyn_resourcecategory** e dell'unità organizzativa di gestione risorse **msdyn_organizationalunit** siano impostati su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="2e8fb-115">Con questi campi abilitati puoi impostare il prezzo e il costo di ogni combinazione di unità organizzativa e ruolo.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="2e8fb-116">Se devi determinare il prezzo o il costo delle risorse utilizzando ulteriori attributi, puoi creare entità, dimensioni e campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="2e8fb-117">Determinare il prezzo del tempo delle risorse umane</span><span class="sxs-lookup"><span data-stu-id="2e8fb-117">Pricing human resource time</span></span>
<span data-ttu-id="2e8fb-118">Il modo in cui un'organizzazione determina il prezzo del tempo delle risorse umane è spesso un fattore strategico importante che influenza direttamente la redditività dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="2e8fb-119">Collabora con i team finanziari e i responsabili delle procedure quando l'organizzazione è pronta per identificare il modo in cui configurare tassi di fatturazione e di costo per il tempo delle risorse umane.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="2e8fb-120">Altre considerazioni per la determinazione dei prezzi includono se riutilizzare campi o entità che non sono al momento dimensioni di determinazione dei prezzi, ma che vengono applicate come tali per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="2e8fb-121">I campi come **Categoria di transazione** ( **msdyn_transactioncategory** ) e **Risorsa prenotabile** ( **bookableresource** ) sono esempi di possibili dimensioni.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="2e8fb-122">Considera se la dimensione di determinazione dei prezzi deve essere una tabella o un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="2e8fb-123">Se prevedi modifiche ai valori di una dimensione superiori a 10 o 12 e necessiti di ulteriori attributi per questi valori, puoi creare un'entità anziché un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="2e8fb-124">La gestione di un set di opzioni, ad esempio l'aggiunta o la rimozione di valori, richiede un amministratore o uno sviluppatore mentre l'aggiunta di nuove righe a una tabella può essere eseguita dalla maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="2e8fb-125">L'esempio seguente presenta tassi di fatturazione configurati in base al ruolo e all'unità organizzativa di gestione risorse a cui la risorsa appartiene.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="2e8fb-126">I tassi di costo sono in genere basati sulla fascia tariffaria del dipendente e sull'unità organizzativa a cui appartiene.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="2e8fb-127">In questo esempio, le tabelle di tassi di fatturazione e costo saranno simili a quanto segue.</span><span class="sxs-lookup"><span data-stu-id="2e8fb-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="2e8fb-128">**Tassi di fatturazione di esempio**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-128">**Sample bill rates**</span></span>

| <span data-ttu-id="2e8fb-129">Ruolo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-129">Role</span></span>        | <span data-ttu-id="2e8fb-130">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="2e8fb-130">Org Unit</span></span>    |<span data-ttu-id="2e8fb-131">Unità</span><span class="sxs-lookup"><span data-stu-id="2e8fb-131">Unit</span></span>      |<span data-ttu-id="2e8fb-132">Prezzo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-132">Price</span></span>      |<span data-ttu-id="2e8fb-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="2e8fb-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="2e8fb-134">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="2e8fb-134">Developer</span></span>   | <span data-ttu-id="2e8fb-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="2e8fb-135">Contoso US</span></span>  |<span data-ttu-id="2e8fb-136">Hour</span><span class="sxs-lookup"><span data-stu-id="2e8fb-136">Hour</span></span> | <span data-ttu-id="2e8fb-137">200</span><span class="sxs-lookup"><span data-stu-id="2e8fb-137">200</span></span>|<span data-ttu-id="2e8fb-138">USD</span><span class="sxs-lookup"><span data-stu-id="2e8fb-138">USD</span></span>     |
| <span data-ttu-id="2e8fb-139">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="2e8fb-139">Developer</span></span>   | <span data-ttu-id="2e8fb-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="2e8fb-140">Contoso India</span></span> |<span data-ttu-id="2e8fb-141">Hour</span><span class="sxs-lookup"><span data-stu-id="2e8fb-141">Hour</span></span>|   <span data-ttu-id="2e8fb-142">112</span><span class="sxs-lookup"><span data-stu-id="2e8fb-142">112</span></span>|<span data-ttu-id="2e8fb-143">USD</span><span class="sxs-lookup"><span data-stu-id="2e8fb-143">USD</span></span>     |


<span data-ttu-id="2e8fb-144">**Tassi di costo di esempio**</span><span class="sxs-lookup"><span data-stu-id="2e8fb-144">**Sample cost rates**</span></span>

| <span data-ttu-id="2e8fb-145">Fascia salariale</span><span class="sxs-lookup"><span data-stu-id="2e8fb-145">Salary Band</span></span>     | <span data-ttu-id="2e8fb-146">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="2e8fb-146">Org Unit</span></span>    |<span data-ttu-id="2e8fb-147">Unità</span><span class="sxs-lookup"><span data-stu-id="2e8fb-147">Unit</span></span>      |<span data-ttu-id="2e8fb-148">Prezzo</span><span class="sxs-lookup"><span data-stu-id="2e8fb-148">Price</span></span>      |<span data-ttu-id="2e8fb-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="2e8fb-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="2e8fb-150">Mia società_Fascia1</span><span class="sxs-lookup"><span data-stu-id="2e8fb-150">My company_Band1</span></span> | <span data-ttu-id="2e8fb-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="2e8fb-151">Contoso US</span></span>  |<span data-ttu-id="2e8fb-152">Hour</span><span class="sxs-lookup"><span data-stu-id="2e8fb-152">Hour</span></span> | <span data-ttu-id="2e8fb-153">145</span><span class="sxs-lookup"><span data-stu-id="2e8fb-153">145</span></span>|<span data-ttu-id="2e8fb-154">USD</span><span class="sxs-lookup"><span data-stu-id="2e8fb-154">USD</span></span>     |
| <span data-ttu-id="2e8fb-155">Mia società_Fascia2</span><span class="sxs-lookup"><span data-stu-id="2e8fb-155">My company_Band2</span></span> | <span data-ttu-id="2e8fb-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="2e8fb-156">Contoso India</span></span> |<span data-ttu-id="2e8fb-157">Hour</span><span class="sxs-lookup"><span data-stu-id="2e8fb-157">Hour</span></span>|   <span data-ttu-id="2e8fb-158">67</span><span class="sxs-lookup"><span data-stu-id="2e8fb-158">67</span></span>|<span data-ttu-id="2e8fb-159">USD</span><span class="sxs-lookup"><span data-stu-id="2e8fb-159">USD</span></span>     |
