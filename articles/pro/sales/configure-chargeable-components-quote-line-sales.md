---
title: Configurare i componenti addebitabili di una riga di offerta
description: Questo argomento fornisce informazioni sulla configurazione dei componenti addebitabili e non addebitabili di una riga di offerta basata su progetto.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858298"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="3d759-103">Configurare i componenti addebitabili di una riga di offerta</span><span class="sxs-lookup"><span data-stu-id="3d759-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="3d759-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="3d759-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3d759-105">Una riga di offerta basata su progetto ha il concetto di componenti *inclusi* e *addebitabili*.</span><span class="sxs-lookup"><span data-stu-id="3d759-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="3d759-106">I componenti inclusi sono soggetti a:</span><span class="sxs-lookup"><span data-stu-id="3d759-106">Included components are subject to:</span></span>

  - <span data-ttu-id="3d759-107">Metodo di fatturazione e suddivisioni dei clienti</span><span class="sxs-lookup"><span data-stu-id="3d759-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="3d759-108">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="3d759-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="3d759-109">Impostazioni della frequenza della fattura definite nella riga di offerta basata su progetto</span><span class="sxs-lookup"><span data-stu-id="3d759-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="3d759-110">Un sottoinsieme dei componenti inclusi può essere contrassegnato come addebitabile usando il campo **Tipo di fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="3d759-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="3d759-111">Il campo **Tipo di fatturazione** è un set di opzioni che consente i seguenti valori nel contesto di una riga di offerta:</span><span class="sxs-lookup"><span data-stu-id="3d759-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="3d759-112">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-112">Chargeable</span></span>
  - <span data-ttu-id="3d759-113">Non addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-113">Non-chargeable</span></span>

<span data-ttu-id="3d759-114">I componenti addebitabili possono essere definiti sulle attività, sui ruoli e sulle categorie di transazioni.</span><span class="sxs-lookup"><span data-stu-id="3d759-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="3d759-115">L'esigibilità è definita nelle attività per una riga di offerta e si applica a tutte le classi di transazione incluse in quella riga.</span><span class="sxs-lookup"><span data-stu-id="3d759-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="3d759-116">Se il campo **Includi attività** è impostato su **Intero progetto** o viene lasciato vuoto, la scheda **Attività addebitabili** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3d759-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="3d759-117">L'esigibilità è definita nei ruoli di una riga di offerta e si applica solo alla classe di transazione **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="3d759-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="3d759-118">Se il campo **Includi tempo** è impostato su **No** su una riga di offerta di progetto, la scheda **Ruoli addebitabili** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3d759-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="3d759-119">L'esigibilità è definita nelle categorie di transazione per una riga di offerta e si applica solo alla classe di transazione **Spesa**.</span><span class="sxs-lookup"><span data-stu-id="3d759-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="3d759-120">Se il campo **Includi spese** è impostato su **No** su una riga di offerta di progetto, la scheda **Categorie addebitabili** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3d759-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="3d759-121">Aggiornare un'attività di progetto in modo che sia addebitabile o non addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="3d759-122">Un'attività di progetto può essere addebitabile o non addebitabile nel contesto di una specifica riga di offerta basata su progetto, il che rende possibile la seguente configurazione.</span><span class="sxs-lookup"><span data-stu-id="3d759-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="3d759-123">Se una riga di offerta basata su progetto include **Tempo** e l'attività **T1**, l'attività è associata alla riga di offerta come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="3d759-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="3d759-124">Se è presente una seconda riga di offerta che include **Spese**, puoi associare l'attività **T1** nella riga di offerta come non addebitabile.</span><span class="sxs-lookup"><span data-stu-id="3d759-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="3d759-125">Il risultato è che tutto il tempo registrato sull'attività è addebitabile e tutte le spese registrate sull'attività non sono addebitabili.</span><span class="sxs-lookup"><span data-stu-id="3d759-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="3d759-126">Il tipo di fatturazione di un'attività può essere configurato nella scheda **Attività addebitabili** di una riga di offerta basata su progetto aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Attività riga offerta**.</span><span class="sxs-lookup"><span data-stu-id="3d759-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="3d759-127">In alternativa, puoi aggiornare il tipo di fatturazione per un'attività di progetto nel campo **Tipo di fatturazione** nella griglia secondaria dell'impostazione fatturazione attività di un progetto che mostra le righe di offerta associate a un'attività.</span><span class="sxs-lookup"><span data-stu-id="3d759-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="3d759-128">Aggiornare un ruolo in modo che sia addebitabile o non addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="3d759-129">Un ruolo può essere addebitabile o non addebitabile nel contesto di una specifica riga di offerta basata su progetto.</span><span class="sxs-lookup"><span data-stu-id="3d759-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="3d759-130">Il tipo di fatturazione di un ruolo può essere configurato nella scheda **Ruoli addebitabili** di una riga di offerta aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Ruoli addebitabili**.</span><span class="sxs-lookup"><span data-stu-id="3d759-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="3d759-131">Aggiornare una categoria di transazione in modo che sia addebitabile o non addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="3d759-132">Una categoria di transazione può essere addebitabile o non addebitabile su una specifica riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="3d759-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="3d759-133">Il tipo di fatturazione di una transazione può essere configurato nella scheda **Categorie addebitabili** di una riga di offerta aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Categorie addebitabili**.</span><span class="sxs-lookup"><span data-stu-id="3d759-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="3d759-134">Risolvere l'esigibilità</span><span class="sxs-lookup"><span data-stu-id="3d759-134">Resolve chargeability</span></span>
<span data-ttu-id="3d759-135">Una stima o un valore effettivo creato per il tempo sarà considerato addebitabile solo se:</span><span class="sxs-lookup"><span data-stu-id="3d759-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="3d759-136">**Tempo** è incluso nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="3d759-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="3d759-137">**Ruolo** è configurato come addebitabile nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="3d759-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="3d759-138">**Attività incluse** è impostato su **Attività selezionate** nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="3d759-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="3d759-139">Se queste tre condizioni sono soddisfatte, anche l'**Attività** è configurata come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="3d759-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="3d759-140">Una stima o un valore effettivo creato per le spese è considerato addebitabile solo se:</span><span class="sxs-lookup"><span data-stu-id="3d759-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="3d759-141">**Spesa** è incluso nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="3d759-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="3d759-142">**Categoria di transazione** è configurato come addebitabile nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="3d759-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="3d759-143">**Attività incluse** è impostato su **Attività selezionate** nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="3d759-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="3d759-144">Se queste tre condizioni sono soddisfatte, anche l'**Attività** è configurata come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="3d759-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="3d759-145">Una stima o un valore effettivo creato per il materiale sarà considerato addebitabile solo se:</span><span class="sxs-lookup"><span data-stu-id="3d759-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="3d759-146">**Materiali** è incluso nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="3d759-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="3d759-147">**Attività incluse** è impostato su **Attività selezionate** nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="3d759-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="3d759-148">Se queste due condizioni sono soddisfatte, anche l'**Attività** deve essere configurata come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="3d759-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="3d759-149">
                    <strong>Include Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="3d759-150">
                    <strong>Include Spesa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="3d759-151">
                    <strong>Include Materiali</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="3d759-152">
                    <strong>Attività incluse</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3d759-153">
                    <strong>Ruolo</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3d759-154">
                    <strong>Categoria.</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3d759-155">
                    <strong>Attività</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="3d759-156">
                    <strong>Impatto esigibilità</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-157">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-158">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-159">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-160">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="3d759-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-161">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-162">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-163">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-164">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3d759-165">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3d759-166">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-167">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-168">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-169">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-170">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="3d759-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-171">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-172">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-173">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-174">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3d759-175">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3d759-176">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-177">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-178">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-179">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-180">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="3d759-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3d759-181">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-182">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-183">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-184">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-185">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3d759-186">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-187">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-188">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-189">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-190">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="3d759-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-191">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-192">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3d759-193">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-194">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-195">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-196">Tipo di fatturazione in base a valore effettivo materiale: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-197">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-198">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-199">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-200">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="3d759-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3d759-201">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-202">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3d759-203">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-204">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-205">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-206">Tipo di fatturazione in base a valore effettivo materiale: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-207">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-208">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-209">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-210">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="3d759-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3d759-211">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3d759-212">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-213">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-214">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-215">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-216">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="3d759-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-218">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-219">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-220">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="3d759-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-221">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3d759-222">
                    <strong>Addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-223">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-224">Fatturazione in base a valore effettivo tempo: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-225">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3d759-226">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="3d759-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-228">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-229">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-230">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="3d759-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-231">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3d759-232">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-233">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-234">Fatturazione in base a valore effettivo tempo: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-235">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-236">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-237">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="3d759-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-239">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-240">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="3d759-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-241">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-242">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-243">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-244">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3d759-245">Tipo di fatturazione in base a valore effettivo spesa: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-246">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-247">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="3d759-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3d759-249">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-250">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="3d759-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3d759-251">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-252">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-253">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-254">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-255">Tipo di fatturazione in base a valore effettivo spesa: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-256">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-257">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-258">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="3d759-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-260">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="3d759-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-261">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-262">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-263">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-264">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3d759-265">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="3d759-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3d759-266">Tipo di fatturazione in base a valore effettivo materiale: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3d759-267">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3d759-268">Sì</span><span class="sxs-lookup"><span data-stu-id="3d759-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="3d759-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3d759-270">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="3d759-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3d759-271">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3d759-272">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3d759-273">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="3d759-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3d759-274">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-275">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="3d759-276">Tipo di fatturazione in base a valore effettivo materiale: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3d759-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
