---
title: Panoramica delle dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni sulle dimensioni di determinazione dei prezzi in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898221"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="34de6-103">Panoramica delle dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="34de6-103">Pricing dimensions overview</span></span>

<span data-ttu-id="34de6-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="34de6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="34de6-105">Le dimensioni utilizzate nelle risorse umane per impostare prezzi e costi rientrano in due categorie:</span><span class="sxs-lookup"><span data-stu-id="34de6-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="34de6-106">Persone</span><span class="sxs-lookup"><span data-stu-id="34de6-106">People</span></span>
- <span data-ttu-id="34de6-107">Lavoro pianificato</span><span class="sxs-lookup"><span data-stu-id="34de6-107">Planned work</span></span>

<span data-ttu-id="34de6-108">Di conseguenza, sono disponibili due tipi di valori per le dimensioni di determinazione dei prezzi:</span><span class="sxs-lookup"><span data-stu-id="34de6-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="34de6-109">**Set di opzioni**: dimensioni che sono enumerazioni fisse per un set di valori.</span><span class="sxs-lookup"><span data-stu-id="34de6-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="34de6-110">**Valori basati su entità**: dimensioni che possono essere un set di valori differenti.</span><span class="sxs-lookup"><span data-stu-id="34de6-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="34de6-111">Dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="34de6-111">Pricing dimensions</span></span>

<span data-ttu-id="34de6-112">Dynamics 365 Project Operations viene fornito con un set predefinito di dimensioni dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="34de6-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="34de6-113">Puoi visualizzare queste dimensioni di determinazione dei prezzi in **Project Operations** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="34de6-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="34de6-114">Nel record del parametro, nella scheda **Dimensione di determinazione dei prezzi basata su importo**, verifica che i campi **Vendite applicabili a** e **Costo applicabile a** del ruolo **msdyn_resourcecategory** e dell'unità organizzativa di gestione risorse **msdyn_organizationalunit** siano impostati su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="34de6-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="34de6-115">Con questi campi abilitati puoi impostare il prezzo e il costo di ogni combinazione di unità organizzativa e ruolo.</span><span class="sxs-lookup"><span data-stu-id="34de6-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="34de6-116">Se devi determinare il prezzo o il costo delle risorse utilizzando ulteriori attributi, puoi creare entità, dimensioni e campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="34de6-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="34de6-117">Determinare il prezzo del tempo delle risorse umane</span><span class="sxs-lookup"><span data-stu-id="34de6-117">Pricing human resource time</span></span>
<span data-ttu-id="34de6-118">Il modo in cui un'organizzazione determina il prezzo del tempo delle risorse umane è spesso un fattore strategico importante che influenza direttamente la redditività dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="34de6-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="34de6-119">Collabora con i team finanziari e i responsabili delle procedure quando l'organizzazione è pronta per identificare il modo in cui configurare tassi di fatturazione e di costo per il tempo delle risorse umane.</span><span class="sxs-lookup"><span data-stu-id="34de6-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="34de6-120">Altre considerazioni per la determinazione dei prezzi includono se riutilizzare campi o entità che non sono al momento dimensioni di determinazione dei prezzi, ma che vengono applicate come tali per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="34de6-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="34de6-121">I campi come **Categoria di transazione** (**msdyn_transactioncategory**) e **Risorsa prenotabile** (**bookableresource**) sono esempi di possibili dimensioni.</span><span class="sxs-lookup"><span data-stu-id="34de6-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="34de6-122">Considera se la dimensione di determinazione dei prezzi deve essere una tabella o un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="34de6-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="34de6-123">Se prevedi modifiche ai valori di una dimensione superiori a 10 o 12 e necessiti di ulteriori attributi per questi valori, puoi creare un'entità anziché un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="34de6-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="34de6-124">La gestione di un set di opzioni, ad esempio l'aggiunta o la rimozione di valori, richiede un amministratore o uno sviluppatore mentre l'aggiunta di nuove righe a una tabella può essere eseguita dalla maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="34de6-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="34de6-125">L'esempio seguente presenta tassi di fatturazione configurati in base al ruolo e all'unità organizzativa di gestione risorse a cui la risorsa appartiene.</span><span class="sxs-lookup"><span data-stu-id="34de6-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="34de6-126">I tassi di costo sono in genere basati sulla fascia tariffaria del dipendente e sull'unità organizzativa a cui appartiene.</span><span class="sxs-lookup"><span data-stu-id="34de6-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="34de6-127">In questo esempio, le tabelle di tassi di fatturazione e costo saranno simili a quanto segue.</span><span class="sxs-lookup"><span data-stu-id="34de6-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="34de6-128">**Tassi di fatturazione di esempio**</span><span class="sxs-lookup"><span data-stu-id="34de6-128">**Sample bill rates**</span></span>

| <span data-ttu-id="34de6-129">Ruolo</span><span class="sxs-lookup"><span data-stu-id="34de6-129">Role</span></span>        | <span data-ttu-id="34de6-130">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="34de6-130">Org Unit</span></span>    |<span data-ttu-id="34de6-131">Unità</span><span class="sxs-lookup"><span data-stu-id="34de6-131">Unit</span></span>      |<span data-ttu-id="34de6-132">Prezzo</span><span class="sxs-lookup"><span data-stu-id="34de6-132">Price</span></span>      |<span data-ttu-id="34de6-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="34de6-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="34de6-134">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="34de6-134">Developer</span></span>   | <span data-ttu-id="34de6-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="34de6-135">Contoso US</span></span>  |<span data-ttu-id="34de6-136">Hour</span><span class="sxs-lookup"><span data-stu-id="34de6-136">Hour</span></span> | <span data-ttu-id="34de6-137">200</span><span class="sxs-lookup"><span data-stu-id="34de6-137">200</span></span>|<span data-ttu-id="34de6-138">USD</span><span class="sxs-lookup"><span data-stu-id="34de6-138">USD</span></span>     |
| <span data-ttu-id="34de6-139">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="34de6-139">Developer</span></span>   | <span data-ttu-id="34de6-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="34de6-140">Contoso India</span></span> |<span data-ttu-id="34de6-141">Hour</span><span class="sxs-lookup"><span data-stu-id="34de6-141">Hour</span></span>|   <span data-ttu-id="34de6-142">112</span><span class="sxs-lookup"><span data-stu-id="34de6-142">112</span></span>|<span data-ttu-id="34de6-143">USD</span><span class="sxs-lookup"><span data-stu-id="34de6-143">USD</span></span>     |


<span data-ttu-id="34de6-144">**Tassi di costo di esempio**</span><span class="sxs-lookup"><span data-stu-id="34de6-144">**Sample cost rates**</span></span>

| <span data-ttu-id="34de6-145">Fascia salariale</span><span class="sxs-lookup"><span data-stu-id="34de6-145">Salary Band</span></span>     | <span data-ttu-id="34de6-146">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="34de6-146">Org Unit</span></span>    |<span data-ttu-id="34de6-147">Unità</span><span class="sxs-lookup"><span data-stu-id="34de6-147">Unit</span></span>      |<span data-ttu-id="34de6-148">Prezzo</span><span class="sxs-lookup"><span data-stu-id="34de6-148">Price</span></span>      |<span data-ttu-id="34de6-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="34de6-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="34de6-150">Mia società_Fascia1</span><span class="sxs-lookup"><span data-stu-id="34de6-150">My company_Band1</span></span> | <span data-ttu-id="34de6-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="34de6-151">Contoso US</span></span>  |<span data-ttu-id="34de6-152">Hour</span><span class="sxs-lookup"><span data-stu-id="34de6-152">Hour</span></span> | <span data-ttu-id="34de6-153">145</span><span class="sxs-lookup"><span data-stu-id="34de6-153">145</span></span>|<span data-ttu-id="34de6-154">USD</span><span class="sxs-lookup"><span data-stu-id="34de6-154">USD</span></span>     |
| <span data-ttu-id="34de6-155">Mia società_Fascia2</span><span class="sxs-lookup"><span data-stu-id="34de6-155">My company_Band2</span></span> | <span data-ttu-id="34de6-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="34de6-156">Contoso India</span></span> |<span data-ttu-id="34de6-157">Hour</span><span class="sxs-lookup"><span data-stu-id="34de6-157">Hour</span></span>|   <span data-ttu-id="34de6-158">67</span><span class="sxs-lookup"><span data-stu-id="34de6-158">67</span></span>|<span data-ttu-id="34de6-159">USD</span><span class="sxs-lookup"><span data-stu-id="34de6-159">USD</span></span>     |
