---
title: Configurare la creazione automatica della fattura
description: Questo argomento fornisce informazioni su come configurare il sistema per generare fatture automaticamente.
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898131"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="36166-103">Configurare la creazione automatica della fattura</span><span class="sxs-lookup"><span data-stu-id="36166-103">Configure automated invoice creation</span></span>

<span data-ttu-id="36166-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="36166-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="36166-105">Completa i passaggi seguenti per configurare l'esecuzione automatica della fattura in Project Operations.</span><span class="sxs-lookup"><span data-stu-id="36166-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="36166-106">Passa a **Impostazioni** \> **Processi batch**.</span><span class="sxs-lookup"><span data-stu-id="36166-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="36166-107">Crea un processo batch e denominalo **Project Operations - Creazione di fatture**.</span><span class="sxs-lookup"><span data-stu-id="36166-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="36166-108">Il nome del processo batch deve includere il termine "creazione di fatture".</span><span class="sxs-lookup"><span data-stu-id="36166-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="36166-109">Nel campo **Tipo di processo** seleziona **Nome**.</span><span class="sxs-lookup"><span data-stu-id="36166-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="36166-110">Per impostazione predefinita, le opzioni **Frequenza giornaliera** e **Attivo** sono impostate su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="36166-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="36166-111">Seleziona **Esegui flusso di lavoro**.</span><span class="sxs-lookup"><span data-stu-id="36166-111">Select **Run Workflow**.</span></span> <span data-ttu-id="36166-112">Nella finestra di dialogo **Cerca record**, vengono visualizzati tre flussi di lavoro:</span><span class="sxs-lookup"><span data-stu-id="36166-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="36166-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="36166-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="36166-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="36166-114">ProcessRunner</span></span>
    - <span data-ttu-id="36166-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="36166-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="36166-116">Seleziona **ProcessRunCaller** e quindi **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="36166-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="36166-117">Nella finestra di dialogo successiva, seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="36166-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="36166-118">Un flusso di lavoro **Sospendi** è seguito da un flusso di lavoro **Elabora**.</span><span class="sxs-lookup"><span data-stu-id="36166-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="36166-119">Puoi anche selezionare **ProcessRunner** nel passaggio 5.</span><span class="sxs-lookup"><span data-stu-id="36166-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="36166-120">Successivamente, quando selezioni **OK**, un flusso di lavoro **Elabora** è seguito da un flusso di lavoro **Sospendi**.</span><span class="sxs-lookup"><span data-stu-id="36166-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="36166-121">I flussi di lavoro **ProcessRunCaller** e **ProcessRunner** creano le fatture.</span><span class="sxs-lookup"><span data-stu-id="36166-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="36166-122">**ProcessRunCaller** chiama **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="36166-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="36166-123">**ProcessRunner** è il flusso di lavoro che crea le fatture.</span><span class="sxs-lookup"><span data-stu-id="36166-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="36166-124">Esamina tutte le voci di contratto per le quali devono essere create le fatture e crea le fatture per tali voci.</span><span class="sxs-lookup"><span data-stu-id="36166-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="36166-125">Per determinare le voci di contratto per le quali creare le fatture, il processo analizza le date di esecuzione delle fatture per le voci di contratto.</span><span class="sxs-lookup"><span data-stu-id="36166-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="36166-126">Se le voci di contratto appartenenti a un contratto hanno la stessa data di esecuzione delle fatture, le transazioni sono combinate in una fattura con due righe fattura.</span><span class="sxs-lookup"><span data-stu-id="36166-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="36166-127">Se non sono presenti transazioni per le quali creare fatture, il processo ignora la creazione delle fatture.</span><span class="sxs-lookup"><span data-stu-id="36166-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="36166-128">Dopo il termine dell'esecuzione di **ProcessRunner**, questo flusso di lavoro chiama **ProcessRunCaller**, fornisce l'ora di fine e viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="36166-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="36166-129">**ProcessRunCaller** avvia quindi un timer che viene eseguito per 24 ore a partire dall'ora di fine specificata.</span><span class="sxs-lookup"><span data-stu-id="36166-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="36166-130">Alla fine dell'esecuzione del timer, **ProcessRunCaller** viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="36166-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="36166-131">Il processo batch per la creazione di fatture è un processo ricorrente.</span><span class="sxs-lookup"><span data-stu-id="36166-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="36166-132">Se questo processo batch viene eseguito molte volte, vengono create molteplici istanze del processo che causano errori.</span><span class="sxs-lookup"><span data-stu-id="36166-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="36166-133">Pertanto, devi avviare il processo batch una sola volta e riavviarlo solo se viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="36166-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="36166-134">La fatturazione batch viene eseguita solo per le righe di contratto di progetto configurate dalle pianificazioni fatture.</span><span class="sxs-lookup"><span data-stu-id="36166-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="36166-135">Una riga di contratto con un metodo di fatturazione a prezzo fisso deve avere i passaggi fondamentali configurati.</span><span class="sxs-lookup"><span data-stu-id="36166-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="36166-136">Una riga di contratto di progetto con un metodo di fatturazione di tempo e materiali richiederà una pianificazione fatturazione basata sulla data.</span><span class="sxs-lookup"><span data-stu-id="36166-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="36166-137">Lo stesso vale per una riga di contratto basato su progetto.</span><span class="sxs-lookup"><span data-stu-id="36166-137">The same applies to a project-based contract line.</span></span>     
