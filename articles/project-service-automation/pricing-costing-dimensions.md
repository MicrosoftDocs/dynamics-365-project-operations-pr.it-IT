---
title: Home page delle dimensioni di determinazione di prezzi e costi
description: In questo argomento viene fornita una panoramica delle dimensioni di determinazione dei prezzi.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752627"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="6e539-103">Home page delle dimensioni di determinazione di prezzi e costi</span><span class="sxs-lookup"><span data-stu-id="6e539-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="6e539-104">Le dimensioni utilizzate nelle risorse umane per impostare prezzi e costi rientrano in due categorie:</span><span class="sxs-lookup"><span data-stu-id="6e539-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="6e539-105">Persone</span><span class="sxs-lookup"><span data-stu-id="6e539-105">People</span></span>
- <span data-ttu-id="6e539-106">Lavoro pianificato</span><span class="sxs-lookup"><span data-stu-id="6e539-106">Planned work</span></span>

<span data-ttu-id="6e539-107">Di conseguenza, in Project Service Automation (PSA) sono disponibili due tipi di valori per le dimensioni di determinazione dei prezzi:</span><span class="sxs-lookup"><span data-stu-id="6e539-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="6e539-108">**Set di opzioni** - Dimensioni che sono enumerazioni fisse per un set di valori.</span><span class="sxs-lookup"><span data-stu-id="6e539-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="6e539-109">**Valori basati su entità** - Dimensioni che possono essere un set di valori differenti.</span><span class="sxs-lookup"><span data-stu-id="6e539-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="6e539-110">Dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="6e539-110">Pricing dimensions</span></span>

<span data-ttu-id="6e539-111">PSA include un set predefinito di dimensioni di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="6e539-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="6e539-112">Puoi visualizzare queste dimensioni selezionando **Project Service** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="6e539-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="6e539-113">Nel record del parametro, nella scheda **Dimensione di determinazione dei prezzi basata su importo**, verifica che i campi **Vendite applicabili a** e **Costo applicabile a** del ruolo **msdyn_resourcecategory** e dell'unità organizzativa di gestione risorse **msdyn_organizationalunit** siano impostati su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="6e539-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="6e539-114">Ciò ti consentirà di impostare il prezzo e il costo di ogni combinazione di unità organizzativa e ruolo.</span><span class="sxs-lookup"><span data-stu-id="6e539-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Screenshot dei parametri di Project Service con il campo "Vendite applicabili a" evidenziato](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="6e539-116">Se hai utilizzato i campi predefiniti di ruolo e unità organizzativa come dimensioni di determinazione dei prezzi prima della versione 3 di PSA, non vi sono differenze.</span><span class="sxs-lookup"><span data-stu-id="6e539-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="6e539-117">Puoi continuare a utilizzare Project Service come di consueto.</span><span class="sxs-lookup"><span data-stu-id="6e539-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="6e539-118">Se devi determinare il prezzo o il costo delle risorse utilizzando ulteriori attributi, puoi creare entità, dimensioni e campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="6e539-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="6e539-119">Per ulteriori informazioni, vedi gli argomenti seguenti, ma nota che devi completare le procedure nell'ordine indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6e539-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="6e539-120">Creare campi ed entità personalizzati</span><span class="sxs-lookup"><span data-stu-id="6e539-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="6e539-121">Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali</span><span class="sxs-lookup"><span data-stu-id="6e539-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="6e539-122">Impostare campi personalizzati come dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="6e539-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="6e539-123">Aggiornare attributi di plug-in per includere nuove dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="6e539-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="6e539-124">Determinare il prezzo del tempo delle risorse umane</span><span class="sxs-lookup"><span data-stu-id="6e539-124">Pricing human resource time</span></span>
<span data-ttu-id="6e539-125">Il modo in cui un'organizzazione determina il prezzo del tempo delle risorse umane è spesso un fattore strategico importante che influenza direttamente la redditività dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="6e539-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="6e539-126">Collabora con i team finanziari e i responsabili delle procedure quando l'organizzazione è pronta per identificare il modo in cui configurare tassi di fatturazione e di costo per il tempo delle risorse umane.</span><span class="sxs-lookup"><span data-stu-id="6e539-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="6e539-127">Altre considerazioni per la determinazione dei prezzi includono se riutilizzare campi o entità che non sono al momento dimensioni di determinazione dei prezzi, ma che vengono applicate come tali per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="6e539-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="6e539-128">I campi come **Categoria di transazione** (**msdyn_transactioncategory**) e **Risorsa prenotabile** (**bookableresource**) sono esempi di possibili dimensioni.</span><span class="sxs-lookup"><span data-stu-id="6e539-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="6e539-129">Devi inoltre considerare se la dimensione di determinazione dei prezzi deve essere una tabella o un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="6e539-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="6e539-130">Se prevedi modifiche ai valori di una dimensione superiori a 10 o 12 e necessiti di ulteriori attributi per questi valori, puoi creare un'entità anziché un set di opzioni.</span><span class="sxs-lookup"><span data-stu-id="6e539-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="6e539-131">La gestione di un set di opzioni, ad esempio l'aggiunta o la rimozione di valori, richiede un amministratore o uno sviluppatore mentre l'aggiunta di nuove righe a una tabella può essere eseguita dalla maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="6e539-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="6e539-132">L'esempio seguente presenta tassi di fatturazione configurati in base al ruolo e all'unità organizzativa di gestione risorse a cui la risorsa appartiene.</span><span class="sxs-lookup"><span data-stu-id="6e539-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="6e539-133">I tassi di costo sono in genere basati sulla fascia tariffaria del dipendente e sull'unità organizzativa a cui appartiene.</span><span class="sxs-lookup"><span data-stu-id="6e539-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="6e539-134">In questo esempio, le tabelle di tassi di fatturazione e costo saranno simili a quanto segue.</span><span class="sxs-lookup"><span data-stu-id="6e539-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="6e539-135">**Tassi di fatturazione di esempio**</span><span class="sxs-lookup"><span data-stu-id="6e539-135">**Sample bill rates**</span></span>

| <span data-ttu-id="6e539-136">Ruolo</span><span class="sxs-lookup"><span data-stu-id="6e539-136">Role</span></span>        | <span data-ttu-id="6e539-137">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="6e539-137">Org Unit</span></span>    |<span data-ttu-id="6e539-138">Unità</span><span class="sxs-lookup"><span data-stu-id="6e539-138">Unit</span></span>      |<span data-ttu-id="6e539-139">Prezzo</span><span class="sxs-lookup"><span data-stu-id="6e539-139">Price</span></span>      |<span data-ttu-id="6e539-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="6e539-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="6e539-141">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="6e539-141">Developer</span></span>   | <span data-ttu-id="6e539-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="6e539-142">Contoso US</span></span>  |<span data-ttu-id="6e539-143">Hour</span><span class="sxs-lookup"><span data-stu-id="6e539-143">Hour</span></span> | <span data-ttu-id="6e539-144">200</span><span class="sxs-lookup"><span data-stu-id="6e539-144">200</span></span>|<span data-ttu-id="6e539-145">USD</span><span class="sxs-lookup"><span data-stu-id="6e539-145">USD</span></span>     |
| <span data-ttu-id="6e539-146">Sviluppatore</span><span class="sxs-lookup"><span data-stu-id="6e539-146">Developer</span></span>   | <span data-ttu-id="6e539-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="6e539-147">Contoso India</span></span> |<span data-ttu-id="6e539-148">Hour</span><span class="sxs-lookup"><span data-stu-id="6e539-148">Hour</span></span>|   <span data-ttu-id="6e539-149">112</span><span class="sxs-lookup"><span data-stu-id="6e539-149">112</span></span>|<span data-ttu-id="6e539-150">USD</span><span class="sxs-lookup"><span data-stu-id="6e539-150">USD</span></span>     |


<span data-ttu-id="6e539-151">**Tassi di costo di esempio**</span><span class="sxs-lookup"><span data-stu-id="6e539-151">**Sample cost rates**</span></span>

| <span data-ttu-id="6e539-152">Fascia salariale</span><span class="sxs-lookup"><span data-stu-id="6e539-152">Salary Band</span></span>     | <span data-ttu-id="6e539-153">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="6e539-153">Org Unit</span></span>    |<span data-ttu-id="6e539-154">Unità</span><span class="sxs-lookup"><span data-stu-id="6e539-154">Unit</span></span>      |<span data-ttu-id="6e539-155">Prezzo</span><span class="sxs-lookup"><span data-stu-id="6e539-155">Price</span></span>      |<span data-ttu-id="6e539-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="6e539-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="6e539-157">Mia società_Fascia1</span><span class="sxs-lookup"><span data-stu-id="6e539-157">My company_Band1</span></span> | <span data-ttu-id="6e539-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="6e539-158">Contoso US</span></span>  |<span data-ttu-id="6e539-159">Hour</span><span class="sxs-lookup"><span data-stu-id="6e539-159">Hour</span></span> | <span data-ttu-id="6e539-160">145</span><span class="sxs-lookup"><span data-stu-id="6e539-160">145</span></span>|<span data-ttu-id="6e539-161">USD</span><span class="sxs-lookup"><span data-stu-id="6e539-161">USD</span></span>     |
| <span data-ttu-id="6e539-162">Mia società_Fascia2</span><span class="sxs-lookup"><span data-stu-id="6e539-162">My company_Band2</span></span> | <span data-ttu-id="6e539-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="6e539-163">Contoso India</span></span> |<span data-ttu-id="6e539-164">Hour</span><span class="sxs-lookup"><span data-stu-id="6e539-164">Hour</span></span>|   <span data-ttu-id="6e539-165">67</span><span class="sxs-lookup"><span data-stu-id="6e539-165">67</span></span>|<span data-ttu-id="6e539-166">USD</span><span class="sxs-lookup"><span data-stu-id="6e539-166">USD</span></span>     |
