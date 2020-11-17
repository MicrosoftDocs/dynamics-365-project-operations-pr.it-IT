---
title: Panoramica delle dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni sulle dimensioni di determinazione dei prezzi in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128468"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="61e9a-103">Panoramica delle dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="61e9a-103">Pricing dimensions overview</span></span>

<span data-ttu-id="61e9a-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="61e9a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="61e9a-105">Le dimensioni utilizzate nelle risorse umane per impostare prezzi e costi rientrano in due categorie:</span><span class="sxs-lookup"><span data-stu-id="61e9a-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="61e9a-106">Persone</span><span class="sxs-lookup"><span data-stu-id="61e9a-106">People</span></span>
- <span data-ttu-id="61e9a-107">Lavoro pianificato</span><span class="sxs-lookup"><span data-stu-id="61e9a-107">Planned work</span></span>

<span data-ttu-id="61e9a-108">Di conseguenza, sono disponibili due tipi di valori per le dimensioni di determinazione dei prezzi:</span><span class="sxs-lookup"><span data-stu-id="61e9a-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="61e9a-109">**Set di opzioni**: dimensioni che sono enumerazioni fisse per un set di valori.</span><span class="sxs-lookup"><span data-stu-id="61e9a-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="61e9a-110">**Valori basati su entità**: dimensioni che possono essere un set di valori differenti.</span><span class="sxs-lookup"><span data-stu-id="61e9a-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="61e9a-111">Dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="61e9a-111">Pricing dimensions</span></span>

<span data-ttu-id="61e9a-112">Dynamics 365 Project Operations viene fornito con un set predefinito di dimensioni dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="61e9a-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="61e9a-113">Puoi visualizzare queste dimensioni di determinazione dei prezzi in **Project Operations** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="61e9a-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="61e9a-114">Nel record del parametro, nella scheda **Dimensione di determinazione dei prezzi basata su importo**, verifica che i campi **Vendite applicabili a** e **Costo applicabile a** del ruolo **msdyn_resourcecategory** e dell'unità organizzativa di gestione risorse **msdyn_organizationalunit** siano impostati su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="61e9a-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="61e9a-115">Con questi campi abilitati puoi impostare il prezzo e il costo di ogni combinazione di unità organizzativa e ruolo.</span><span class="sxs-lookup"><span data-stu-id="61e9a-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="61e9a-116">Se devi determinare il prezzo o il costo delle risorse utilizzando ulteriori attributi, puoi creare entità, dimensioni e campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="61e9a-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="61e9a-117">Determinare il prezzo del tempo delle risorse umane</span><span class="sxs-lookup"><span data-stu-id="61e9a-117">Pricing human resource time</span></span>
<span data-ttu-id="61e9a-118">Il modo in cui un'organizzazione determina il prezzo del tempo delle risorse umane è spesso un fattore strategico importante che influenza direttamente la redditività dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="61e9a-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="61e9a-119">Collabora con i team finanziari e i responsabili delle procedure quando l'organizzazione è pronta per identificare il modo in cui configurare tassi di fatturazione e di costo per il tempo delle risorse umane.</span><span class="sxs-lookup"><span data-stu-id="61e9a-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="61e9a-120">Altre considerazioni per la determinazione dei prezzi includono se riutilizzare campi o entità che non sono al momento dimensioni di determinazione dei prezzi, ma che vengono applicate come tali per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="61e9a-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="61e9a-121">I campi come **Categoria di transazione** (**msdyn_transactioncategory**) e **Risorsa prenotabile** (**bookableresource**) sono esempi di possibili dimensioni.</span><span class="sxs-lookup"><span data-stu-id="61e9a-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="61e9a-122">Considera se la dimensione di determinazione dei prezzi deve essere una tabella o un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="61e9a-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="61e9a-123">Se prevedi modifiche ai valori di una dimensione superiori a 10 o 12 e necessiti di ulteriori attributi per questi valori, puoi creare un'entità anziché un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="61e9a-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="61e9a-124">La gestione di un set di opzioni, ad esempio l'aggiunta o la rimozione di valori, richiede un amministratore o uno sviluppatore mentre l'aggiunta di nuove righe a una tabella può essere eseguita dalla maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="61e9a-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="61e9a-125">L'esempio seguente presenta tassi di fatturazione configurati in base al ruolo e all'unità organizzativa di gestione risorse a cui la risorsa appartiene.</span><span class="sxs-lookup"><span data-stu-id="61e9a-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="61e9a-126">I tassi di costo sono in genere basati sulla fascia tariffaria del dipendente e sull'unità organizzativa a cui appartiene.</span><span class="sxs-lookup"><span data-stu-id="61e9a-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="61e9a-127">In questo esempio, le tabelle di tassi di fatturazione e costo saranno simili a quanto segue.</span><span class="sxs-lookup"><span data-stu-id="61e9a-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="61e9a-128">**Tassi di fatturazione di esempio**</span><span class="sxs-lookup"><span data-stu-id="61e9a-128">**Sample bill rates**</span></span>

| <span data-ttu-id="61e9a-129">Ruolo</span><span class="sxs-lookup"><span data-stu-id="61e9a-129">Role</span></span>        | <span data-ttu-id="61e9a-130">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="61e9a-130">Org Unit</span></span>    |<span data-ttu-id="61e9a-131">Unità</span><span class="sxs-lookup"><span data-stu-id="61e9a-131">Unit</span></span>      |<span data-ttu-id="61e9a-132">Prezzo</span><span class="sxs-lookup"><span data-stu-id="61e9a-132">Price</span></span>      |<span data-ttu-id="61e9a-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="61e9a-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="61e9a-134">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="61e9a-134">Developer</span></span>   | <span data-ttu-id="61e9a-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="61e9a-135">Contoso US</span></span>  |<span data-ttu-id="61e9a-136">Hour</span><span class="sxs-lookup"><span data-stu-id="61e9a-136">Hour</span></span> | <span data-ttu-id="61e9a-137">200</span><span class="sxs-lookup"><span data-stu-id="61e9a-137">200</span></span>|<span data-ttu-id="61e9a-138">USD</span><span class="sxs-lookup"><span data-stu-id="61e9a-138">USD</span></span>     |
| <span data-ttu-id="61e9a-139">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="61e9a-139">Developer</span></span>   | <span data-ttu-id="61e9a-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="61e9a-140">Contoso India</span></span> |<span data-ttu-id="61e9a-141">Hour</span><span class="sxs-lookup"><span data-stu-id="61e9a-141">Hour</span></span>|   <span data-ttu-id="61e9a-142">112</span><span class="sxs-lookup"><span data-stu-id="61e9a-142">112</span></span>|<span data-ttu-id="61e9a-143">USD</span><span class="sxs-lookup"><span data-stu-id="61e9a-143">USD</span></span>     |


<span data-ttu-id="61e9a-144">**Tassi di costo di esempio**</span><span class="sxs-lookup"><span data-stu-id="61e9a-144">**Sample cost rates**</span></span>

| <span data-ttu-id="61e9a-145">Fascia salariale</span><span class="sxs-lookup"><span data-stu-id="61e9a-145">Salary Band</span></span>     | <span data-ttu-id="61e9a-146">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="61e9a-146">Org Unit</span></span>    |<span data-ttu-id="61e9a-147">Unità</span><span class="sxs-lookup"><span data-stu-id="61e9a-147">Unit</span></span>      |<span data-ttu-id="61e9a-148">Prezzo</span><span class="sxs-lookup"><span data-stu-id="61e9a-148">Price</span></span>      |<span data-ttu-id="61e9a-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="61e9a-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="61e9a-150">Mia società_Fascia1</span><span class="sxs-lookup"><span data-stu-id="61e9a-150">My company_Band1</span></span> | <span data-ttu-id="61e9a-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="61e9a-151">Contoso US</span></span>  |<span data-ttu-id="61e9a-152">Hour</span><span class="sxs-lookup"><span data-stu-id="61e9a-152">Hour</span></span> | <span data-ttu-id="61e9a-153">145</span><span class="sxs-lookup"><span data-stu-id="61e9a-153">145</span></span>|<span data-ttu-id="61e9a-154">USD</span><span class="sxs-lookup"><span data-stu-id="61e9a-154">USD</span></span>     |
| <span data-ttu-id="61e9a-155">Mia società_Fascia2</span><span class="sxs-lookup"><span data-stu-id="61e9a-155">My company_Band2</span></span> | <span data-ttu-id="61e9a-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="61e9a-156">Contoso India</span></span> |<span data-ttu-id="61e9a-157">Hour</span><span class="sxs-lookup"><span data-stu-id="61e9a-157">Hour</span></span>|   <span data-ttu-id="61e9a-158">67</span><span class="sxs-lookup"><span data-stu-id="61e9a-158">67</span></span>|<span data-ttu-id="61e9a-159">USD</span><span class="sxs-lookup"><span data-stu-id="61e9a-159">USD</span></span>     |
