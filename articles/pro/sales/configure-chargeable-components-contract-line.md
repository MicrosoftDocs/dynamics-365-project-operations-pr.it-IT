---
title: Configurare i componenti addebitabili di una voce di contratto basata su progetto
description: Questo argomento fornisce informazioni su come aggiungere componenti addebitabili alle voci di contratto in Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003726"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="1693f-103">Configurare i componenti addebitabili di una voce di contratto basata su progetto</span><span class="sxs-lookup"><span data-stu-id="1693f-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="1693f-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="1693f-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1693f-105">Una voce di contratto basata su progetto ha i componenti *inclusi* e *addebitabili*.</span><span class="sxs-lookup"><span data-stu-id="1693f-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="1693f-106">I componenti inclusi sono componenti soggetti a:</span><span class="sxs-lookup"><span data-stu-id="1693f-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="1693f-107">Metodo di fatturazione e suddivisioni dei clienti</span><span class="sxs-lookup"><span data-stu-id="1693f-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="1693f-108">Limite da non superare</span><span class="sxs-lookup"><span data-stu-id="1693f-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="1693f-109">Impostazioni della frequenza della fattura definite nella voce di contratto basata su progetto</span><span class="sxs-lookup"><span data-stu-id="1693f-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="1693f-110">Un sottoinsieme dei componenti inclusi può essere contrassegnato come addebitabile usando il campo **Tipo di fatturazione**.</span><span class="sxs-lookup"><span data-stu-id="1693f-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="1693f-111">Il campo **Tipo di fatturazione** è un set di opzioni che consente i seguenti valori nel contesto di una voce di contratto:</span><span class="sxs-lookup"><span data-stu-id="1693f-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="1693f-112">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-112">Chargeable</span></span>
  - <span data-ttu-id="1693f-113">Non addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-113">Non-chargeable</span></span>

<span data-ttu-id="1693f-114">I componenti addebitabili possono essere definiti sulle attività, sui ruoli e sulle categorie di transazioni.</span><span class="sxs-lookup"><span data-stu-id="1693f-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="1693f-115">L'esigibilità è definita nelle attività per una voce di contratto di progetto e si applica a tutte le classi di transazione incluse in quella riga.</span><span class="sxs-lookup"><span data-stu-id="1693f-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="1693f-116">Se il campo **Includi attività** di una voce di contratto è vuoto o impostato su **Intero progetto**, la scheda **Attività addebitabili** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1693f-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="1693f-117">L'esigibilità definita nei ruoli per una voce di contratto di progetto si applica solo alla classe di transazione **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="1693f-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="1693f-118">Se il campo **Includi tempo** di una voce di contratto è impostato su **No**, la scheda **Ruoli addebitabili** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1693f-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="1693f-119">L'esigibilità è definita nelle categorie di transazione per una voce di contratto di progetto e si applica solo alla classe di transazione **Spesa**.</span><span class="sxs-lookup"><span data-stu-id="1693f-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="1693f-120">Se il campo **Includi spese** è impostato su **No**, la scheda **Categorie addebitabili** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1693f-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="1693f-121">Aggiornare un'attività di progetto in modo che sia addebitabile o non addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="1693f-122">Un'attività di progetto può essere addebitabile o non addebitabile in una specifica voce di contratto, il che rende possibile la seguente configurazione:</span><span class="sxs-lookup"><span data-stu-id="1693f-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="1693f-123">Se una voce di contratto basata su progetto include **Tempo** e l'attività **T1** è associata ad essa come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="1693f-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="1693f-124">Se è presente una seconda voce di contratto che include **Spesa**, puoi associare l'attività T1 nella voce di contratto come non addebitabile.</span><span class="sxs-lookup"><span data-stu-id="1693f-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="1693f-125">Il risultato è che tutto il tempo registrato sull'attività è addebitabile e tutte le spese non sono addebitabili.</span><span class="sxs-lookup"><span data-stu-id="1693f-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="1693f-126">Il tipo di fatturazione di un'attività può essere configurato nella scheda **Attività addebitabili** di una voce di contratto aggiornando il campo **Tipo di fatturazione** nella griglia secondaria delle attività voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="1693f-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="1693f-127">In alternativa, puoi aggiornare il campo **Tipo di fatturazione** nella griglia secondaria dell'impostazione fatturazione attività di un progetto che mostra le voci di contratto associate a un'attività.</span><span class="sxs-lookup"><span data-stu-id="1693f-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="1693f-128">Aggiornare un ruolo come addebitabile o non addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="1693f-129">Un ruolo può essere addebitabile o non addebitabile su una specifica voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="1693f-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="1693f-130">Il tipo di fatturazione di un ruolo può essere configurato nella scheda **Ruoli addebitabili** di una voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="1693f-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="1693f-131">Per fare ciò, aggiorna il campo **Tipo di fatturazione** nella griglia secondaria **Ruoli addebitabili**.</span><span class="sxs-lookup"><span data-stu-id="1693f-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="1693f-132">Aggiornare una categoria di transazione come addebitabile o non addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="1693f-133">Una categoria di transazione può essere addebitabile o non addebitabile su una specifica voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="1693f-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="1693f-134">Il tipo di fatturazione di una transazione può essere configurato nella scheda **Categorie addebitabili** di una voce di contratto basata di progetto.</span><span class="sxs-lookup"><span data-stu-id="1693f-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="1693f-135">Per fare ciò, aggiorna il campo **Tipo di fatturazione** nella griglia secondaria **Categorie addebitabili**.</span><span class="sxs-lookup"><span data-stu-id="1693f-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="1693f-136">Risolvere l'esigibilità</span><span class="sxs-lookup"><span data-stu-id="1693f-136">Resolve chargeability</span></span>

<span data-ttu-id="1693f-137">Una stima o un valore effettivo creato per il tempo è considerato addebitabile solo se:</span><span class="sxs-lookup"><span data-stu-id="1693f-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="1693f-138">**Tempo** è incluso nella voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="1693f-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="1693f-139">**Ruolo** è configurato come addebitabile nella voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="1693f-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="1693f-140">**Attività incluse** è impostato su **Attività selezionate** nella voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="1693f-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="1693f-141">Se queste tre condizioni sono soddisfatte, anche l'attività è configurata come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="1693f-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="1693f-142">Una stima o un valore effettivo creato per le spese è considerato addebitabile solo se:</span><span class="sxs-lookup"><span data-stu-id="1693f-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="1693f-143">**Spesa** è incluso nella voce di contratto</span><span class="sxs-lookup"><span data-stu-id="1693f-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="1693f-144">**Categoria di transazione** è configurato come addebitabile nella voce di contratto</span><span class="sxs-lookup"><span data-stu-id="1693f-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="1693f-145">**Attività incluse** è impostato su **Attività selezionata** nella voce di contratto</span><span class="sxs-lookup"><span data-stu-id="1693f-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="1693f-146">Se queste tre condizioni sono soddisfatte, l'**attività** è configurata come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="1693f-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="1693f-147">Una stima o un valore effettivo creato per il materiale è considerato addebitabile solo se:</span><span class="sxs-lookup"><span data-stu-id="1693f-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="1693f-148">**Materiali** è incluso nella voce di contratto</span><span class="sxs-lookup"><span data-stu-id="1693f-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="1693f-149">**Attività incluse** è impostato su **Attività selezionate** nella voce di contratto</span><span class="sxs-lookup"><span data-stu-id="1693f-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="1693f-150">Se queste due condizioni sono soddisfatte, l'**attività** è configurata come addebitabile.</span><span class="sxs-lookup"><span data-stu-id="1693f-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1693f-151">
                    <strong>Include il tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1693f-152">
                    <strong>Include la spesa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1693f-153">
                    <strong>Include Materiali</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="1693f-154">
                    <strong>Attività incluse</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1693f-155">
                    <strong>Ruolo</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1693f-156">
                    <strong>Categoria.</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1693f-157">
                    <strong>Attività</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="1693f-158">
                    <strong>Impatto esigibilità</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-159">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-160">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-161">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-162">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="1693f-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-163">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-164">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-165">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-166">Fatturazione in base a valore effettivo tempo: <strong>addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-167">Tipo di fatturazione in base a valore effettivo spesa: <strong>addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-168">Tipo di fatturazione in base a valore effettivo materiale: <strong>addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-169">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-170">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-171">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-172">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="1693f-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-173">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-174">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-175">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-176">Fatturazione in base a valore effettivo tempo: <strong>addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-177">Tipo di fatturazione in base a valore effettivo spesa: <strong>addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-178">Tipo di fatturazione in base a valore effettivo materiale: <strong>addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-179">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-180">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-181">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-182">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="1693f-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1693f-183">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-184">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-185">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-186">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-187">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1693f-188">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-189">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-190">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-191">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-192">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="1693f-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-193">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-194">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1693f-195">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-196">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-197">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-198">Tipo di fatturazione in base a valore effettivo materiale: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-199">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-200">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-201">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-202">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="1693f-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1693f-203">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-204">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1693f-205">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-206">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-207">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-208">Tipo di fatturazione in base a valore effettivo materiale: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-209">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-210">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-211">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-212">Solo le attività selezionate</span><span class="sxs-lookup"><span data-stu-id="1693f-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1693f-213">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1693f-214">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-215">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-216">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-217">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-218">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1693f-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-220">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-221">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-222">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="1693f-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-223">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1693f-224">
                    <strong>Addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-225">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-226">Fatturazione in base a valore effettivo tempo: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-227">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1693f-228">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1693f-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-230">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-231">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-232">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="1693f-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-233">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1693f-234">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-235">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-236">Fatturazione in base a valore effettivo tempo: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-237">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-238">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-239">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1693f-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-241">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-242">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="1693f-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-243">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-244">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-245">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-246">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1693f-247">Tipo di fatturazione in base a valore effettivo spesa: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-248">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-249">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1693f-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1693f-251">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-252">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="1693f-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1693f-253">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-254">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-255">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-256">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-257">Tipo di fatturazione in base a valore effettivo spesa: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-258">Tipo di fatturazione in base a valore effettivo materiale: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-259">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-260">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1693f-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-262">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="1693f-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-263">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-264">Addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-265">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-266">Fatturazione in base a valore effettivo tempo: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1693f-267">Tipo di fatturazione in base a valore effettivo spesa: addebitabile</span><span class="sxs-lookup"><span data-stu-id="1693f-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1693f-268">Tipo di fatturazione in base a valore effettivo materiale: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1693f-269">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1693f-270">Sì</span><span class="sxs-lookup"><span data-stu-id="1693f-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1693f-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1693f-272">Progetto intero</span><span class="sxs-lookup"><span data-stu-id="1693f-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1693f-273">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1693f-274">
                    <strong>Non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1693f-275">Non può essere impostato</span><span class="sxs-lookup"><span data-stu-id="1693f-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1693f-276">Fatturazione in base a valore effettivo tempo: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-277">Tipo di fatturazione in base a valore effettivo spesa: <strong>non addebitabile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1693f-278">Tipo di fatturazione in base a valore effettivo materiale: <strong>non disponibile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1693f-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
