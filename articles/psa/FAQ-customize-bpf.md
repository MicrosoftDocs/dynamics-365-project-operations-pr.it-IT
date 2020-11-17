---
title: Come si personalizza il processo aziendale Fasi del progetto?
description: Una panoramica su come personalizzare il processo aziendale Fasi del progetto.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125047"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="0410a-103">Come si personalizza il processo aziendale Fasi del progetto?</span><span class="sxs-lookup"><span data-stu-id="0410a-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="0410a-104">Le versioni precedenti dell'applicazione Project Service comportano un limite: i nomi delle fasi del processo aziendale Fasi del progetto devono corrispondere esattamente ai nomi inglesi previsti (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="0410a-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="0410a-105">In caso contrario, le regole business, che si basano sui nomi di fase inglesi, non funzionano come previsto.</span><span class="sxs-lookup"><span data-stu-id="0410a-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="0410a-106">Questo è il motivo per cui nel modulo di progetto non sono presenti azioni come **Cambia processo** o **Modifica processo** e la personalizzazione del processo aziendale non è incoraggiata.</span><span class="sxs-lookup"><span data-stu-id="0410a-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="0410a-107">Questo limite è stato superato con la versione 2.4.5.48 e successive.</span><span class="sxs-lookup"><span data-stu-id="0410a-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="0410a-108">Questo articolo fornisce soluzioni alternative nel caso sia necessario personalizzare il processo aziendale predefinito per le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="0410a-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="0410a-109">Le regole business richiedono una corrispondenza esatta con i nomi di fase inglesi</span><span class="sxs-lookup"><span data-stu-id="0410a-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="0410a-110">Il processo aziendale Fasi del progetto include regole business che determinano i seguenti comportamenti nell'app:</span><span class="sxs-lookup"><span data-stu-id="0410a-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="0410a-111">Quando il progetto è associato a un'offerta, il codice imposta il processo aziendale sulla fase **Quote**.</span><span class="sxs-lookup"><span data-stu-id="0410a-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="0410a-112">Quando il progetto è associato a un contratto, il codice imposta il processo aziendale sulla fase **Plan**.</span><span class="sxs-lookup"><span data-stu-id="0410a-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="0410a-113">Quando il processo aziendale è avanzato alla fase **Close**, il record del progetto viene disattivato.</span><span class="sxs-lookup"><span data-stu-id="0410a-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="0410a-114">Quando il progetto viene disattivato, il modulo di progetto e la struttura di suddivisione del lavoro vengono impostati in sola lettura, le prenotazioni delle risorse con nome vengono rilasciate e tutti i listini prezzi associati vengono disattivati.</span><span class="sxs-lookup"><span data-stu-id="0410a-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="0410a-115">Le regole business sono basate sui nomi inglesi per le fasi di progetto.</span><span class="sxs-lookup"><span data-stu-id="0410a-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="0410a-116">Questa dipendenza dai nomi di fase inglesi è il motivo principale per cui la personalizzazione del processo aziendale Fasi del progetto non è incoraggiata e per cui le azioni comuni del processo aziendale come **Cambia processo** o **Modifica processo** non sono presenti nell'entità di progetto.</span><span class="sxs-lookup"><span data-stu-id="0410a-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="0410a-117">Cosa succede se i nomi di fase non corrispondono ai nomi inglesi?</span><span class="sxs-lookup"><span data-stu-id="0410a-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="0410a-118">Nell'app Project Service versione 1.x sulla piattaforma 8.2, quando i nomi di fase nel processo aziendale non corrispondono esattamente ai nomi di fase inglesi, le regole business che impostano la fase appropriata per offerte o contratti o che chiudono il progetto sono ignorate.</span><span class="sxs-lookup"><span data-stu-id="0410a-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="0410a-119">Non vengono visualizzati messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="0410a-119">No error messages are displayed.</span></span> <span data-ttu-id="0410a-120">Di conseguenza, sembra possibile personalizzare il processo aziendale Fasi del progetto.</span><span class="sxs-lookup"><span data-stu-id="0410a-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="0410a-121">Tuttavia, i processi automatici per offerte, contratti e la chiusura del progetto non saranno visibili.</span><span class="sxs-lookup"><span data-stu-id="0410a-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="0410a-122">Nell'app Project Service versione 2.4.4.30 o precedente sulla piattaforma 9.0, è stata introdotta un'importante modifica architetturale dei processi aziendali che ha necessitato la riscrittura delle regole business dei processi aziendali.</span><span class="sxs-lookup"><span data-stu-id="0410a-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="0410a-123">Pertanto, se i nomi di fase di processo non corrispondono ai nomi inglesi previsti, non viene visualizzato alcun messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="0410a-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="0410a-124">Quindi se si desidera personalizzare il processo aziendale Fasi del progetto per l'entità di progetto, è possibile soltanto aggiungere fasi completamente nuove al processo aziendale predefinito per tale entità, mantenendo nel contempo inalterate le fasi **Quote**, **Plan** e **Close**.</span><span class="sxs-lookup"><span data-stu-id="0410a-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="0410a-125">Questa restrizione assicura che non si hanno errori inerenti alle regole business, le quali prevedono nomi di fasi inglesi nel processo aziendale.</span><span class="sxs-lookup"><span data-stu-id="0410a-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="0410a-126">Nella versione 2.4.5.48 o successive In una prossima versione, le regole business descritte in questo articolo sono state rimosse dal processo aziendale predefinito per l'entità di progetto.</span><span class="sxs-lookup"><span data-stu-id="0410a-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="0410a-127">L'aggiornamento a quella versione o a una versione successiva consentirà la personalizzazione del processo aziendale predefinito o la sostituzione delle stesso con quello personale.</span><span class="sxs-lookup"><span data-stu-id="0410a-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="0410a-128">Soluzioni per le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="0410a-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="0410a-129">Se l'aggiornamento non è possibile, è possibile personalizzare il processo aziendale Fasi del progetto per l'entità di progetto in uno dei due seguenti modi:</span><span class="sxs-lookup"><span data-stu-id="0410a-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="0410a-130">Aggiungere fasi supplementari alla configurazione predefinita, mantenendo nel contempo i nomi di fase inglesi per **Quote**, **Plan** e **Close**.</span><span class="sxs-lookup"><span data-stu-id="0410a-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Aggiunta di fasi alla configurazione predefinita](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="0410a-132">Creare il proprio processo aziendale e impostarlo come processo aziendale principale per l'entità di progetto, in modo da poter utilizzare i nomi di fase desiderati.</span><span class="sxs-lookup"><span data-stu-id="0410a-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="0410a-133">Tuttavia, se si intende utilizzare le fasi di progetto standard **Quote**, **Plan** e **Close**, è necessario effettuare alcune modifiche.</span><span class="sxs-lookup"><span data-stu-id="0410a-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="0410a-134">La logica più complessa è quella relativa alla chiusura del progetto, che è ancora possibile eseguire disattivando il record del progetto.</span><span class="sxs-lookup"><span data-stu-id="0410a-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Personalizzazione del flusso del processo aziendale](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="0410a-136">Ulteriori considerazioni per l'app Project Service versione 2.4.4.30 o precedente sulla piattaforma 9.0</span><span class="sxs-lookup"><span data-stu-id="0410a-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="0410a-137">In Project Service 2.4.4.30 o versione precedente sulla piattaforma 9.0, con un processo aziendale personalizzato, il campo **Nome fase** nell'entità di progetto utilizzata nel grafico **Progetto per fase** e le viste dell'elenco di progetti non verranno aggiornati in quanto associati al processo aziendale Fasi del progetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="0410a-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="0410a-138">È possibile risolvere questo problema come segue:</span><span class="sxs-lookup"><span data-stu-id="0410a-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="0410a-139">Aggiungere un campo personalizzato per acquisire la fase corrente del processo aziendale che viene aggiornata quando l'utente avanza nel processo aziendale personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0410a-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="0410a-140">Modificare il grafico **Progetto per fase** per utilizzare il campo personalizzato anziché la configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0410a-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="0410a-141">Procedura per creare un processo aziendale personalizzato per l'entità di progetto</span><span class="sxs-lookup"><span data-stu-id="0410a-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="0410a-142">Per creare un processo aziendale personalizzato per l'entità di progetto, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="0410a-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="0410a-143">Andare a **Impostazioni** > **Centro processi**.</span><span class="sxs-lookup"><span data-stu-id="0410a-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="0410a-144">Non copiare il processo aziendale Fasi del progetto in quanto vengono copiate anche le regole business di Project Service.</span><span class="sxs-lookup"><span data-stu-id="0410a-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Creare processi](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="0410a-146">Utilizzare lo strumento di progettazione dei processi per creare i nomi di fase desiderati.</span><span class="sxs-lookup"><span data-stu-id="0410a-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="0410a-147">Se si desidera la stessa funzionalità delle fasi predefinite **Quote**, **Plan** e **Close**, è necessario crearla in base ai nomi di fase del processo aziendale personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0410a-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Strumento di progettazione dei processi utilizzato per personalizzare il processo aziendale](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="0410a-149">Nello strumento di progettazione dei processi, fare clic su **Flusso di elaborazione ordine** e spostare il processo aziendale personalizzato sopra il processo aziendale Fasi del progetto affinché sia il processo aziendale principale.</span><span class="sxs-lookup"><span data-stu-id="0410a-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="0410a-150">Utilizzo di Flusso di elaborazione ordine</span><span class="sxs-lookup"><span data-stu-id="0410a-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="0410a-151">La procedura seguente si applica all'app Project Service 2.4.4.30 o versione precedente sulla piattaforma 9.0</span><span class="sxs-lookup"><span data-stu-id="0410a-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="0410a-152">Aggiungere un nuovo campo personalizzato all'entità di progetto per acquisire le fasi personalizzate nel processo aziendale personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0410a-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="0410a-153">Sarà necessario aggiungere delle regole business (plug-in/flusso di lavoro) per aggiornare questo campo quando la fase del processo aziendale personalizzato viene aggiornata.</span><span class="sxs-lookup"><span data-stu-id="0410a-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Personalizzazione dell'entità di progetto](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="0410a-155">Modificare il grafico **Progetto per fase** per utilizzare il nuovo campo personalizzato per le fasi.</span><span class="sxs-lookup"><span data-stu-id="0410a-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Utilizzo del grafico Progetto per fase](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="0410a-157">Modificare tutte le viste per l'entità di progetto per includere il campo personalizzato per le fasi.</span><span class="sxs-lookup"><span data-stu-id="0410a-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Modifica delle viste nell'entità di progetto](media/FAQ-Customize-BPF-8-720.png)

