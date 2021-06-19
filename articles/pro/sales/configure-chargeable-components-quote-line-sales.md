---
title: Configurare i componenti addebitabili di una riga di offerta
description: Questo argomento fornisce informazioni sulla configurazione dei componenti addebitabili e non addebitabili di una riga di offerta basata su progetto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003771"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="948fd-103">Configurare i componenti addebitabili di una riga di offerta</span><span class="sxs-lookup"><span data-stu-id="948fd-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="948fd-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="948fd-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="948fd-105">Una riga di offerta basata su progetto ha il concetto di componenti *inclusi* e *addebitabili*.</span><span class="sxs-lookup"><span data-stu-id="948fd-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="948fd-106">I componenti inclusi sono soggetti a:</span><span class="sxs-lookup"><span data-stu-id="948fd-106">Included components are subject to:</span></span>

  - <span data-ttu-id="948fd-107">Metodo di fatturazione e suddivisioni dei clienti</span><span class="sxs-lookup"><span data-stu-id="948fd-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="948fd-108">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="948fd-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="948fd-109">Impostazioni della frequenza della fattura definite nella riga di offerta basata su progetto</span><span class="sxs-lookup"><span data-stu-id="948fd-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="948fd-110">Un sottoinsieme dei componenti inclusi può essere contrassegnato come addebitabile usando il campo **Tipo di fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="948fd-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="948fd-111">Il campo **Tipo di fatturazione** è un set di opzioni che consente i seguenti valori nel contesto di una riga di offerta:</span><span class="sxs-lookup"><span data-stu-id="948fd-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="948fd-112">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-112">Chargeable</span></span>
  - <span data-ttu-id="948fd-113">Non addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-113">Non-chargeable</span></span>

<span data-ttu-id="948fd-114">I componenti addebitabili possono essere definiti sulle attività, sui ruoli e sulle categorie di transazioni.</span><span class="sxs-lookup"><span data-stu-id="948fd-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="948fd-115">L'esigibilità è definita nelle attività per una riga di offerta e si applica a tutte le classi di transazione incluse in quella riga.</span><span class="sxs-lookup"><span data-stu-id="948fd-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="948fd-116">Se il campo **Includi attività** è impostato su **Intero progetto** o viene lasciato vuoto, la scheda **Attività addebitabili** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="948fd-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="948fd-117">L'esigibilità è definita nei ruoli di una riga di offerta e si applica solo alla classe di transazione **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="948fd-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="948fd-118">Se il campo **Includi tempo** è impostato su **No** su una riga di offerta di progetto, la scheda **Ruoli addebitabili** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="948fd-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="948fd-119">L'esigibilità è definita nelle categorie di transazione per una riga di offerta e si applica solo alla classe di transazione **Spesa**.</span><span class="sxs-lookup"><span data-stu-id="948fd-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="948fd-120">Se il campo **Includi spese** è impostato su **No** su una riga di offerta di progetto, la scheda **Categorie addebitabili** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="948fd-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="948fd-121">Aggiornare un'attività di progetto in modo che sia addebitabile o non addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="948fd-122">Un'attività di progetto può essere addebitabile o non addebitabile nel contesto di una specifica riga di offerta basata su progetto, il che rende possibile la seguente configurazione.</span><span class="sxs-lookup"><span data-stu-id="948fd-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="948fd-123">Se una riga di offerta basata su progetto include **Tempo** e l'attività **T1**, l'attività è associata alla riga di offerta come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="948fd-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="948fd-124">Se è presente una seconda riga di offerta che include **Spese**, puoi associare l'attività **T1** nella riga di offerta come non addebitabile.</span><span class="sxs-lookup"><span data-stu-id="948fd-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="948fd-125">Il risultato è che tutto il tempo registrato sull'attività è addebitabile e tutte le spese registrate sull'attività non sono addebitabili.</span><span class="sxs-lookup"><span data-stu-id="948fd-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="948fd-126">Il tipo di fatturazione di un'attività può essere configurato nella scheda **Attività addebitabili** di una riga di offerta basata su progetto aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Attività riga offerta**.</span><span class="sxs-lookup"><span data-stu-id="948fd-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="948fd-127">In alternativa, puoi aggiornare il tipo di fatturazione per un'attività di progetto nel campo **Tipo di fatturazione** nella griglia secondaria dell'impostazione fatturazione attività di un progetto che mostra le righe di offerta associate a un'attività.</span><span class="sxs-lookup"><span data-stu-id="948fd-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="948fd-128">Aggiornare un ruolo in modo che sia addebitabile o non addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="948fd-129">Un ruolo può essere addebitabile o non addebitabile nel contesto di una specifica riga di offerta basata su progetto.</span><span class="sxs-lookup"><span data-stu-id="948fd-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="948fd-130">Il tipo di fatturazione di un ruolo può essere configurato nella scheda **Ruoli addebitabili** di una riga di offerta aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Ruoli addebitabili**.</span><span class="sxs-lookup"><span data-stu-id="948fd-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="948fd-131">Aggiornare una categoria di transazione in modo che sia addebitabile o non addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="948fd-132">Una categoria di transazione può essere addebitabile o non addebitabile su una specifica riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="948fd-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="948fd-133">Il tipo di fatturazione di una transazione può essere configurato nella scheda **Categorie addebitabili** di una riga di offerta aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Categorie addebitabili**.</span><span class="sxs-lookup"><span data-stu-id="948fd-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="948fd-134">Risolvere l'esigibilità</span><span class="sxs-lookup"><span data-stu-id="948fd-134">Resolve chargeability</span></span>
<span data-ttu-id="948fd-135">Una stima o un valore effettivo creato per il tempo sarà considerato addebitabile solo se:</span><span class="sxs-lookup"><span data-stu-id="948fd-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="948fd-136">**Tempo** è incluso nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="948fd-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="948fd-137">**Ruolo** è configurato come addebitabile nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="948fd-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="948fd-138">**Attività incluse** è impostato su **Attività selezionate** nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="948fd-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="948fd-139">Se queste tre condizioni sono soddisfatte, anche l'**Attività** è configurata come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="948fd-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="948fd-140">Una stima o un valore effettivo creato per le spese è considerato addebitabile solo se:</span><span class="sxs-lookup"><span data-stu-id="948fd-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="948fd-141">**Spesa** è incluso nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="948fd-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="948fd-142">**Categoria di transazione** è configurato come addebitabile nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="948fd-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="948fd-143">**Attività incluse** è impostato su **Attività selezionate** nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="948fd-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="948fd-144">Se queste tre condizioni sono soddisfatte, anche l'**Attività** è configurata come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="948fd-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="948fd-145">Una stima o un valore effettivo creato per il materiale sarà considerato addebitabile solo se:</span><span class="sxs-lookup"><span data-stu-id="948fd-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="948fd-146">**Materiali** è incluso nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="948fd-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="948fd-147">**Attività incluse** è impostato su **Attività selezionate** nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="948fd-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="948fd-148">Se queste due condizioni sono soddisfatte, anche l'**Attività** deve essere configurata come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="948fd-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="948fd-149">
                    <strong>Include Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="948fd-150">
                    <strong>Include Spesa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="948fd-151">
                    <strong>Include Materiali</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="948fd-152">
                    <strong>Attività incluse</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="948fd-153">
                    <strong>Ruolo</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="948fd-154">
                    <strong>Categoria.</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="948fd-155">
                    <strong>Attività</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="948fd-156">
                    <strong>Impatto esigibilità</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-157">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-158">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-159">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-160">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="948fd-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-161">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-162">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-163">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-164">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="948fd-165">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="948fd-166">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-167">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-168">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-169">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-170">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="948fd-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-171">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-172">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-173">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-174">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="948fd-175">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="948fd-176">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-177">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-178">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-179">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-180">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="948fd-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="948fd-181">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-182">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-183">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-184">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-185">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="948fd-186">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-187">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-188">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-189">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-190">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="948fd-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-191">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-192">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="948fd-193">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-194">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-195">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-196">Tipo di fatturazione in base a valore effettivo materiale: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-197">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-198">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-199">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-200">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="948fd-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="948fd-201">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-202">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="948fd-203">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-204">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-205">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-206">Tipo di fatturazione in base a valore effettivo materiale: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-207">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-208">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-209">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-210">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="948fd-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="948fd-211">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="948fd-212">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-213">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-214">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-215">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-216">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="948fd-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-218">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-219">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-220">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="948fd-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-221">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="948fd-222">
                    <strong>Addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-223">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-224">Fatturazione in base a valore effettivo tempo: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-225">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="948fd-226">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="948fd-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-228">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-229">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-230">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="948fd-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-231">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="948fd-232">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-233">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-234">Fatturazione in base a valore effettivo tempo: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-235">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-236">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-237">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="948fd-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-239">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-240">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="948fd-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-241">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-242">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-243">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-244">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="948fd-245">Tipo di fatturazione in base a valore effettivo spesa: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-246">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-247">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="948fd-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="948fd-249">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-250">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="948fd-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="948fd-251">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-252">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-253">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-254">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-255">Tipo di fatturazione in base a valore effettivo spesa: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-256">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-257">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-258">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="948fd-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-260">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="948fd-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-261">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-262">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-263">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-264">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="948fd-265">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="948fd-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="948fd-266">Tipo di fatturazione in base a valore effettivo materiale: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="948fd-267">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="948fd-268">Sì</span><span class="sxs-lookup"><span data-stu-id="948fd-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="948fd-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="948fd-270">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="948fd-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="948fd-271">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="948fd-272">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="948fd-273">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="948fd-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="948fd-274">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-275">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="948fd-276">Tipo di fatturazione in base a valore effettivo materiale: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="948fd-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
