---
title: Crea un nuovo progetto
description: In questo argomento vengono fornite informazioni su come creare un nuovo progetto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270728"
---
# <a name="create-a-new-project"></a><span data-ttu-id="2e04e-103">Crea un nuovo progetto</span><span class="sxs-lookup"><span data-stu-id="2e04e-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e04e-104">Completa i passaggi seguenti per creare un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="2e04e-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="2e04e-105">Nella pagina **Gestione dei progetti**, seleziona **Nuovo progetto**, quindi immetti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e04e-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="2e04e-106">**Tipo di progetto:** tempo e materiale</span><span class="sxs-lookup"><span data-stu-id="2e04e-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="2e04e-107">**Nome progetto:** fase di aggiornamento XYZ 2</span><span class="sxs-lookup"><span data-stu-id="2e04e-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="2e04e-108">**Gruppo di progetto:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="2e04e-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="2e04e-109">**ID contratto di progetto:** 00000002</span><span class="sxs-lookup"><span data-stu-id="2e04e-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="2e04e-110">Seleziona **Crea progetto**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="2e04e-111">Assegnare una risorsa a un progetto</span><span class="sxs-lookup"><span data-stu-id="2e04e-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="2e04e-112">Nella pagina **Lavoratori** pagina, nell'elenco **Lavoratori**, seleziona il record per il lavoratore per cui hai impostato in precedenza le competenze e apri il record del lavoratore.</span><span class="sxs-lookup"><span data-stu-id="2e04e-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="2e04e-113">Nel riquadro azioni, nella scheda **Progetto**, nel gruppo **Imposta**, seleziona **Assegna progetti**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="2e04e-114">Nella pagina **Assegnazioni di progetti di convalida delle risorse**, nella scheda **Progetti**, nel campo **Aggiungi il progetto ai progetti selezionati**, filtra nel progetto **Fase di aggiornamento XYZ 2**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="2e04e-115">Nel riquadro **Progetti rimanenti**, seleziona un progetto, quindi seleziona il pulsante freccia per aggiungerlo al riquadro **Progetti selezionati**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="2e04e-116">Puoi inoltre assegnare categorie a una risorsa in base alle tue esigenze.</span><span class="sxs-lookup"><span data-stu-id="2e04e-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="2e04e-117">Il tipo di categoria è **Costo** o **Ricavi**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="2e04e-118">Il tipo di categoria è determinato dalla tua organizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e04e-118">The category type is determined by your organization.</span></span> <span data-ttu-id="2e04e-119">Se nessuna categoria è assegnata a una risorsa, Finance cerca la categoria predefinita sui prezzi orari per costi e ricavi.</span><span class="sxs-lookup"><span data-stu-id="2e04e-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="2e04e-120">Configurare le caratteristiche di ruolo e risorsa del progetto</span><span class="sxs-lookup"><span data-stu-id="2e04e-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="2e04e-121">Un project manager può utilizzare la funzionalità di assegnazione delle risorse del progetto per creare i ruoli richiesti per il progetto.</span><span class="sxs-lookup"><span data-stu-id="2e04e-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="2e04e-122">I ruoli possono essere utilizzati se le risorse confermate sono ancora sconosciute quando le risorse vengono prenotate.</span><span class="sxs-lookup"><span data-stu-id="2e04e-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="2e04e-123">I ruoli possono essere riservati temporaneamente come risorse pianificate, in modo da poter continuare le fasi di pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="2e04e-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="2e04e-124">[![Esempio di un ruolo](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="2e04e-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="2e04e-125">**Scenario:** Contoso è stato assunto per completare un progetto di tempistica e materiali con uno statuto progetto approvato.</span><span class="sxs-lookup"><span data-stu-id="2e04e-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="2e04e-126">Il project manager junior sta ancora completando l'ambito del progetto.</span><span class="sxs-lookup"><span data-stu-id="2e04e-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="2e04e-127">Il responsabile delle risorse sta attualmente individuando risorse specifiche che saranno prenotate per lavorare sul nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="2e04e-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="2e04e-128">A causa della natura critica del progetto, lo sponsor del progetto ha richiesto il Senior Project Manager come uno dei ruoli.</span><span class="sxs-lookup"><span data-stu-id="2e04e-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="2e04e-129">Il responsabile delle risorse deve acquisire la nuova risorsa e definire il ruolo nel sistema nel caso in cui il project manager junior richieda le informazioni sulla risorsa durante la pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="2e04e-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="2e04e-130">I passaggi seguenti mostrano come il responsabile delle risorse può configurare il ruolo di Senior project manager e associarvi le caratteristiche della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2e04e-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="2e04e-131">Successivamente, il ruolo può essere utilizzato per cercare le risorse disponibili che corrispondono alle competenze delle risorse richieste.</span><span class="sxs-lookup"><span data-stu-id="2e04e-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="2e04e-132">Nella pagina **Configura ruoli**, seleziona **Nuovo**, quindi immetti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e04e-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="2e04e-133">**ID ruolo:** Senior Project Manager</span><span class="sxs-lookup"><span data-stu-id="2e04e-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="2e04e-134">**Descrizione:** Senior Project Manager</span><span class="sxs-lookup"><span data-stu-id="2e04e-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="2e04e-135">Seleziona **Crea**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-135">Select **Create**.</span></span>
3. <span data-ttu-id="2e04e-136">Seleziona il ruolo **Senior Project Manager**, quindi seleziona **Configura caratteristiche**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="2e04e-137">Nel campo **Tipo di caratteristiche**, seleziona **Competenza**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="2e04e-138">Nel campo **Caratteristiche disponibili**, immetti la competenza da cercare.</span><span class="sxs-lookup"><span data-stu-id="2e04e-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="2e04e-139">Nel campo **Tipo di caratteristica**, seleziona **Certificato**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="2e04e-140">Nel campo **Caratteristiche disponibili**, immetti il tipo di certificato da cercare.</span><span class="sxs-lookup"><span data-stu-id="2e04e-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="2e04e-141">Assegnare una risorsa di progetto a un progetto</span><span class="sxs-lookup"><span data-stu-id="2e04e-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="2e04e-142">Nella pagina **Tutti i progetti**, seleziona il progetto **Fase di aggiornamento XYZ 2**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="2e04e-143">Nella scheda **Team progetto e programmazione**, seleziona **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="2e04e-144">Nel campo **Ruolo**, seleziona **Membro del team**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="2e04e-145">Seleziona **Prenota da calendario**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="2e04e-146">Nella pagina **Disponibilità risorse**, seleziona **Visualizza impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="2e04e-147">Nella pagina **Modifica impostazioni visualizzazione**, immetti i seguenti valori:</span><span class="sxs-lookup"><span data-stu-id="2e04e-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="2e04e-148">**Formato per la visualizzazione dell'intervallo di date:** giornaliero</span><span class="sxs-lookup"><span data-stu-id="2e04e-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="2e04e-149">**Visualizza descrizioni disponibili:** Sì</span><span class="sxs-lookup"><span data-stu-id="2e04e-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="2e04e-150">**Visualizza capacità rimanente:** Sì</span><span class="sxs-lookup"><span data-stu-id="2e04e-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="2e04e-151">Seleziona una risorsa dall'elenco delle risorse.</span><span class="sxs-lookup"><span data-stu-id="2e04e-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="2e04e-152">Seleziona **Prenota definitivamente** e **Piena capacità**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="2e04e-153">Assegnare una risorsa a un ruolo predefinito</span><span class="sxs-lookup"><span data-stu-id="2e04e-153">Assign a resource to a default role</span></span>

<span data-ttu-id="2e04e-154">Per aiutare i responsabili di progetto o risorse possono eseguire il drill-down sulle risorse che possono essere prenotate per un progetto.</span><span class="sxs-lookup"><span data-stu-id="2e04e-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="2e04e-155">Puoi associare un ruolo predefinito a una risorsa esistente o a una risorsa appena acquisita.</span><span class="sxs-lookup"><span data-stu-id="2e04e-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="2e04e-156">Ad esempio, quando è stato assunto Daniel, aveva l'esperienza e le competenze per ricoprire il ruolo di analista aziendale.</span><span class="sxs-lookup"><span data-stu-id="2e04e-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="2e04e-157">Il responsabile delle risorse ha assegnato questo ruolo come ruolo predefinito di Daniel.</span><span class="sxs-lookup"><span data-stu-id="2e04e-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="2e04e-158">Pertanto, il responsabile delle risorse ha aggiunto Daniel a un pool di analisti aziendali disponibili a lavorare sui progetti.</span><span class="sxs-lookup"><span data-stu-id="2e04e-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="2e04e-159">Durante la prenotazione delle risorse, i project manager possono filtrare le risorse ruolo disponibili per lavorare sui progetti.</span><span class="sxs-lookup"><span data-stu-id="2e04e-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="2e04e-160">Possono utilizzare queste informazioni come un criterio quando eseguono l'analisi decisionale multicriterio durante l'evasione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="2e04e-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="2e04e-161">Possono anche aggiungere altre caratteristiche delle risorse al filtro per cercare risorse con competenze, istruzione ed esperienza specifiche per un determinato progetto.</span><span class="sxs-lookup"><span data-stu-id="2e04e-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="2e04e-162">**Scenario:** è stato avviato un progetto approvato e il ruolo di Senior project manager è stato riservato come risorsa pianificata durante la fase di pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="2e04e-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="2e04e-163">Il responsabile delle risorse ha ora acquisito una risorsa per svolgere il ruolo di Senior project manager.</span><span class="sxs-lookup"><span data-stu-id="2e04e-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="2e04e-164">Nella pagina **Elenco risorse**, seleziona **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="2e04e-165">Nella pagina **Ruolo risorsa**, seleziona **Nuovo**, quindi immetti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e04e-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="2e04e-166">**Validità:** immetti la data corrente.</span><span class="sxs-lookup"><span data-stu-id="2e04e-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="2e04e-167">**Scadenza:** immetti **Mai**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="2e04e-168">**Ruolo:** immetti **Senior Project Manager**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="2e04e-169">Seleziona **Salva** e quindi chiudi la pagina.</span><span class="sxs-lookup"><span data-stu-id="2e04e-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="2e04e-170">Nella scheda **Competenze**, aggiungi la competenza **ProjectMgmt** e il certificato **PMP**.</span><span class="sxs-lookup"><span data-stu-id="2e04e-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]