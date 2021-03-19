---
title: Configurare le risorse di progetto
description: In questo argomento vengono fornite informazioni sull'impostazione o sulla richiesta di risorse di progetto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288744"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="b05b0-103">Configurare le risorse di progetto</span><span class="sxs-lookup"><span data-stu-id="b05b0-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b05b0-104">Devi configurare un calendario e associarlo a un dipendente o a un lavoratore.</span><span class="sxs-lookup"><span data-stu-id="b05b0-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="b05b0-105">Il calendario viene utilizzato per pianificare il progetto e l'orario di lavoro delle risorse riservate al progetto.</span><span class="sxs-lookup"><span data-stu-id="b05b0-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="b05b0-106">Durante la configurazione del calendario, i project manager possono eseguire il livellamento delle risorse come parte dell'ottimizzazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="b05b0-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="b05b0-107">In base alla pianificazione del calendario, è possibile applicare restrizioni alle risorse.</span><span class="sxs-lookup"><span data-stu-id="b05b0-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="b05b0-108">Puoi configurare un calendario nella pagina **Calendari**.</span><span class="sxs-lookup"><span data-stu-id="b05b0-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="b05b0-109">Quando configuri un lavoratore come risorsa del progetto, puoi selezionare tra i lavoratori che lavorano nell'azienda per cui stai configurando le risorse.</span><span class="sxs-lookup"><span data-stu-id="b05b0-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="b05b0-110">In alternativa, puoi selezionare lavoratori di altre società nella tua organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b05b0-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="b05b0-111">Questi lavoratori sono noti come risorse interaziendali.</span><span class="sxs-lookup"><span data-stu-id="b05b0-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="b05b0-112">Le seguenti procedure spiegano come configurare un lavoratore come risorsa di progetto nella propria azienda e come configurare una risorsa di progetto interaziendale.</span><span class="sxs-lookup"><span data-stu-id="b05b0-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="b05b0-113">Configurare un lavoratore come risorsa del progetto</span><span class="sxs-lookup"><span data-stu-id="b05b0-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="b05b0-114">Nella pagina **Lavoratori** pagina, nell'elenco **Lavoratori**, seleziona il lavoratore che stai aggiungendo come risorsa del progetto e apri il record del lavoratore.</span><span class="sxs-lookup"><span data-stu-id="b05b0-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="b05b0-115">Nel riquadro azioni seleziona **Progetto**&gt; **Imposta** &gt;**Impostazione progetto**.</span><span class="sxs-lookup"><span data-stu-id="b05b0-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="b05b0-116">Seleziona un calendario e quindi chiudi la pagina.</span><span class="sxs-lookup"><span data-stu-id="b05b0-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="b05b0-117">Puoi inoltre specificare progetti predefiniti per una risorsa come tipo di pre-assegnazione.</span><span class="sxs-lookup"><span data-stu-id="b05b0-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="b05b0-118">Le pre-assegnazioni possono essere utilizzate quando il responsabile delle risorse o il project manager sa in anticipo su quali progetti lavorerà la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b05b0-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="b05b0-119">Le pre-assegnazioni possono anche essere basate sulla richiesta di uno sponsor del progetto o di un cliente.</span><span class="sxs-lookup"><span data-stu-id="b05b0-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="b05b0-120">Per pre-assegnare un progetto, nella pagina **Assegna progetti**, nella scheda **Progetti**, nell'elenco **Progetti rimanenti**, seleziona il progetto appropriato.</span><span class="sxs-lookup"><span data-stu-id="b05b0-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="b05b0-121">Configurare una risorsa interaziendale</span><span class="sxs-lookup"><span data-stu-id="b05b0-121">Set up an intercompany resource</span></span>

<span data-ttu-id="b05b0-122">Quando si configura un lavoratore come risorsa interaziendale, devi completare la configurazione sia nella società mutuante che nella società mutuataria.</span><span class="sxs-lookup"><span data-stu-id="b05b0-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="b05b0-123">Nella società mutuante</span><span class="sxs-lookup"><span data-stu-id="b05b0-123">In the lending company</span></span>

1. <span data-ttu-id="b05b0-124">In Finance, verifica che la società mutuante sia selezionata, quindi completa la procedura nella sezione precedente, "Configurare un lavoratore come risorsa di progetto".</span><span class="sxs-lookup"><span data-stu-id="b05b0-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="b05b0-125">Nella pagina **Contabilità interaziendale**, seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="b05b0-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="b05b0-126">Nel campo **ID persona giuridica**, seleziona la società mutuante.</span><span class="sxs-lookup"><span data-stu-id="b05b0-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="b05b0-127">Compila i campi rimanenti come necessario e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="b05b0-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="b05b0-128">Nella pagina **Prezzo di trasferimento**, seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="b05b0-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="b05b0-129">Nel campo **Persona giuridica richiedente**, seleziona la società appropriata.</span><span class="sxs-lookup"><span data-stu-id="b05b0-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="b05b0-130">Per prestare alla società mutuataria solo la risorsa che hai creato all'inizio di questa sezione, nel campo **Risorsa**, seleziona il nome della risorsa che hai creato.</span><span class="sxs-lookup"><span data-stu-id="b05b0-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="b05b0-131">Per rendere disponibili alla società mutuataria tutte le risorse della società mutuante, lascia vuoto il campo **Risorsa**.</span><span class="sxs-lookup"><span data-stu-id="b05b0-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="b05b0-132">Nella pagina **Parametri Gestione progetti e contabilità**, nella scheda **Interaziendale**, imposta l'opzione **Abilita programmazione risorse interaziendale e fogli presenze** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="b05b0-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="b05b0-133">Nella società mutuataria</span><span class="sxs-lookup"><span data-stu-id="b05b0-133">In the borrowing company</span></span>

- <span data-ttu-id="b05b0-134">Nella pagina **Elenco risorse**, nel filtro di ricerca, inserisci il nome della risorsa che hai creato per la società mutuante, per verificare che il nome sia incluso nell'elenco delle risorse per la società mutuataria.</span><span class="sxs-lookup"><span data-stu-id="b05b0-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="b05b0-135">Richiedere risorse di progetto</span><span class="sxs-lookup"><span data-stu-id="b05b0-135">Request project resources</span></span>
<span data-ttu-id="b05b0-136">La funzionalità per la pianificazione delle risorse di progetto consente solo ai responsabili delle risorse di distribuire le risorse con personale su impegni o progetti.</span><span class="sxs-lookup"><span data-stu-id="b05b0-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="b05b0-137">Per abilitare questa funzionalità, completa le seguenti attività o verifica che siano state completate:</span><span class="sxs-lookup"><span data-stu-id="b05b0-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="b05b0-138">Configura le sequenze numeriche.</span><span class="sxs-lookup"><span data-stu-id="b05b0-138">Set up number sequences.</span></span>
- <span data-ttu-id="b05b0-139">Configura i flussi di lavoro di gestione dei progetti e contabilità.</span><span class="sxs-lookup"><span data-stu-id="b05b0-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="b05b0-140">Abilita i flussi di lavoro delle richieste di risorse.</span><span class="sxs-lookup"><span data-stu-id="b05b0-140">Enable resource request workflows.</span></span>

<span data-ttu-id="b05b0-141">Dopo che le attività precedenti sono state completate, puoi completare le seguenti attività come richiesto:</span><span class="sxs-lookup"><span data-stu-id="b05b0-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="b05b0-142">Crea una richiesta di risorse da una risorsa con personale con prenotazione provvisoria.</span><span class="sxs-lookup"><span data-stu-id="b05b0-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="b05b0-143">Monitora le richieste di risorse.</span><span class="sxs-lookup"><span data-stu-id="b05b0-143">Monitor resource requests.</span></span>
- <span data-ttu-id="b05b0-144">Soddisfa richieste di risorse.</span><span class="sxs-lookup"><span data-stu-id="b05b0-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="b05b0-145">Richiedi una risorsa con personale da una struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="b05b0-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="b05b0-146">Prenota risorse per un progetto senza dover richiedere una risorsa con personale.</span><span class="sxs-lookup"><span data-stu-id="b05b0-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]