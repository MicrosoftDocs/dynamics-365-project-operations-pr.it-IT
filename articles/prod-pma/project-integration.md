---
title: Integrazione con Microsoft Project Client
description: La pianificazione e la gestione di una pianificazione del progetto possono essere complesse, quindi i project manager devono utilizzare strumenti che li aiutino a gestire questa attività. L'integrazione con Microsoft Project Client fornisce supporto per aprire e gestire una struttura di suddivisione del lavoro di progetto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b312ec5b1f4e6a98a2cbf1667b2f55b758b2d613
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269840"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="19e0e-104">Integrazione con Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="19e0e-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19e0e-105">La pianificazione e la gestione di una pianificazione del progetto possono essere complesse, quindi i project manager devono utilizzare strumenti che li aiutino a gestire questa attività.</span><span class="sxs-lookup"><span data-stu-id="19e0e-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="19e0e-106">L'integrazione con Microsoft Project Client fornisce supporto per aprire e gestire una struttura di suddivisione del lavoro di progetto.</span><span class="sxs-lookup"><span data-stu-id="19e0e-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="19e0e-107">Il project manager può pubblicare eventuali modifiche nella struttura di suddivisione del lavoro del progetto Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="19e0e-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="19e0e-108">Se stai usando l'aggiornamento di luglio (versione 10.0.4), devi installare KB 4054797 e 4055884.</span><span class="sxs-lookup"><span data-stu-id="19e0e-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="19e0e-109">Configurare il componente aggiuntivo di Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="19e0e-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="19e0e-110">Per abilitare l'integrazione con Microsoft Project Client, è necessario installare un componente aggiuntivo di Microsoft Dynamics 365 nell'applicazione client Microsoft Project dell'utente.</span><span class="sxs-lookup"><span data-stu-id="19e0e-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="19e0e-111">Questo viene fatto aprendo l'**area di lavoro per la gestione dei progetti**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="19e0e-112">•   Fai clic su **Configura componente aggiuntivo client di progetto** dalla sezione **Collegamenti** > **Imposta** dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19e0e-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="19e0e-113">•   Fai clic su **Apri**, quindi fai clic su **Esegui** quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="19e0e-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="19e0e-114">Aprire e modificare una bozza di struttura di suddivisione del lavoro esistente in Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="19e0e-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="19e0e-115">Se un progetto in Dynamics 365 Finance ha già una struttura di suddivisione del lavoro creata, la struttura di suddivisione del lavoro può essere aperta nell'applicazione Microsoft Project Client se la struttura di suddivisione del lavoro è in uno stato di bozza.</span><span class="sxs-lookup"><span data-stu-id="19e0e-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="19e0e-116">Per aprire dalla pagina **Progetto**, fai clic sul collegamento **Apri in Microsoft Project** dalla scheda **Piano**. Questa pagina può essere aperta anche dall'interno dell'applicazione Microsoft Project Client facendo clic su **Apri** nella scheda **Microsoft Dynamics 365**. Seleziona **Persona giuridica** e **Progetto** dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="19e0e-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="19e0e-117">Se stai usando Internet Explorer come browser, dovrai fare clic su **Salva** per aprire manualmente dalla posizione in cui viene scaricato il file.</span><span class="sxs-lookup"><span data-stu-id="19e0e-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="19e0e-118">Oppure fai clic su **Salva e apri** per aprire il file in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="19e0e-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="19e0e-119">Non rinominare il nome del file durante il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="19e0e-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="19e0e-120">Prima di apportare modifiche al file utilizzando Microsoft Project Client, devi verificarlo. Fai clic su **Estrai** nella scheda **Microsoft Dynamics 365**. Ciò impedirà ad altri utenti di modificare contemporaneamente la struttura di suddivisione del lavoro da Finance.</span><span class="sxs-lookup"><span data-stu-id="19e0e-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="19e0e-121">Per pubblicare la struttura di suddivisione del lavoro dopo aver completato le modifiche, fai clic su **Registra** nella scheda **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="19e0e-122">Se un team di progetto è già stato aggiunto al progetto in Finance, l'elenco delle risorse verrà popolato con i membri del team.</span><span class="sxs-lookup"><span data-stu-id="19e0e-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="19e0e-123">Se un team di progetto non è stato ancora aggiunto al progetto, è possibile selezionare le risorse e creare il team all'interno di Microsoft Project Client facendo clic sul pulsante **Risorse** della scheda **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="19e0e-124">I seguenti dati verranno sincronizzati di nuovo con Finance come parte del processo di check-in:</span><span class="sxs-lookup"><span data-stu-id="19e0e-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="19e0e-125">•   Nome attività</span><span class="sxs-lookup"><span data-stu-id="19e0e-125">•   Task name</span></span>

<span data-ttu-id="19e0e-126">•   Data di inizio</span><span class="sxs-lookup"><span data-stu-id="19e0e-126">•   Start date</span></span>

<span data-ttu-id="19e0e-127">•   Data di fine</span><span class="sxs-lookup"><span data-stu-id="19e0e-127">•   Finish date</span></span>

<span data-ttu-id="19e0e-128">•   Attività precedenti</span><span class="sxs-lookup"><span data-stu-id="19e0e-128">•   Predecessors</span></span>

<span data-ttu-id="19e0e-129">•   Nomi risorse</span><span class="sxs-lookup"><span data-stu-id="19e0e-129">•   Resource names</span></span>

<span data-ttu-id="19e0e-130">•   Categoria</span><span class="sxs-lookup"><span data-stu-id="19e0e-130">•   Category</span></span>

<span data-ttu-id="19e0e-131">•   Categoria di risorsa</span><span class="sxs-lookup"><span data-stu-id="19e0e-131">•   Resource category</span></span>

<span data-ttu-id="19e0e-132">•   Orario di lavoro</span><span class="sxs-lookup"><span data-stu-id="19e0e-132">•   Work hours</span></span>

<span data-ttu-id="19e0e-133">•   Note</span><span class="sxs-lookup"><span data-stu-id="19e0e-133">•   Notes</span></span>

<span data-ttu-id="19e0e-134">•   Priorità</span><span class="sxs-lookup"><span data-stu-id="19e0e-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="19e0e-135">Se aggiungi altre colonne al file di Microsoft Project Client, non verranno salvate nel file e non verranno visualizzate quando il file viene aperto di nuovo.</span><span class="sxs-lookup"><span data-stu-id="19e0e-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="19e0e-136">Creare la struttura di suddivisione del lavoro per un progetto esistente utilizzando Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="19e0e-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="19e0e-137">Per creare una nuova struttura di suddivisione del lavoro utilizzando Microsoft Project Client, segui questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="19e0e-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="19e0e-138">Apri Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="19e0e-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="19e0e-139">Nella scheda **Microsoft Dynamics 365** fai clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="19e0e-140">Selezionare la **persona giuridica** per il progetto.</span><span class="sxs-lookup"><span data-stu-id="19e0e-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="19e0e-141">Seleziona il **progetto**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="19e0e-142">Fai clic su **Estrai** nella scheda **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="19e0e-143">Quando sei pronto per pubblicare su Finance, fai clic su **Registra** nella scheda **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="19e0e-144">Sostituisci la struttura di suddivisione del lavoro per un progetto esistente utilizzando Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="19e0e-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="19e0e-145">Per creare una nuova struttura di suddivisione del lavoro utilizzando Microsoft Project Client e sostituire una struttura di suddivisione del lavoro esistente per un progetto esistente, attieniti alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="19e0e-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="19e0e-146">Apri Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="19e0e-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="19e0e-147">Crea la pianificazione in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="19e0e-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="19e0e-148">Nella scheda **Microsoft Dynamics 365**, fai clic su **Salva modifiche** > **Sostituisci progetto esistente**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="19e0e-149">Selezionare la **persona giuridica** per il progetto.</span><span class="sxs-lookup"><span data-stu-id="19e0e-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="19e0e-150">Seleziona il **progetto**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="19e0e-151">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="19e0e-152">Creare un nuovo progetto dall'interno di Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="19e0e-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="19e0e-153">Apri Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="19e0e-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="19e0e-154">Crea la pianificazione in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="19e0e-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="19e0e-155">Nella scheda **Microsoft Dynamics 365**, fai clic su **Salva modifiche** > **Salva su nuovo progetto**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="19e0e-156">Selezionare la **persona giuridica** per il progetto.</span><span class="sxs-lookup"><span data-stu-id="19e0e-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="19e0e-157">Immetti l'**ID progetto**, se necessario.</span><span class="sxs-lookup"><span data-stu-id="19e0e-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="19e0e-158">Immetti il **Nome progetto**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="19e0e-159">Seleziona un valore per **Tipo di progetto**, **Gruppo di progetto** e **ID contratto di progetto**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="19e0e-160">In alternativa, puoi creare un nuovo contratto di progetto facendo clic su **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="19e0e-161">Seleziona il **Calendario** da utilizzare per le risorse.</span><span class="sxs-lookup"><span data-stu-id="19e0e-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="19e0e-162">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="19e0e-162">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="19e0e-163">Il componente aggiuntivo Project Client non supporta i seguenti caratteri nel formato dell'ID progetto:</span><span class="sxs-lookup"><span data-stu-id="19e0e-163">The Project Client add-in doesn’t support the following characters in the project ID format:</span></span>
> 
>   - <span data-ttu-id="19e0e-164">Carattere di sottolineatura</span><span class="sxs-lookup"><span data-stu-id="19e0e-164">Underscore</span></span>
>   - <span data-ttu-id="19e0e-165">Periodo</span><span class="sxs-lookup"><span data-stu-id="19e0e-165">Period</span></span>
>   - <span data-ttu-id="19e0e-166">BARRA SPAZIATRICE</span><span class="sxs-lookup"><span data-stu-id="19e0e-166">Space</span></span>
>   - <span data-ttu-id="19e0e-167">Barra</span><span class="sxs-lookup"><span data-stu-id="19e0e-167">Slash</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
