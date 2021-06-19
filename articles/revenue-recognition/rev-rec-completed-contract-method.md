---
title: Gestire le stime dei ricavi
description: Questo argomento fornisce informazioni su come gestire le stime dei ricavi per i progetti.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e3cbaff18d8bd4d6f6a7577bba25b3e843b1757e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013852"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="d01c2-103">Gestire le stime dei ricavi</span><span class="sxs-lookup"><span data-stu-id="d01c2-103">Manage revenue estimates</span></span>

<span data-ttu-id="d01c2-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="d01c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d01c2-105">Puoi creare, calcolare, registrare, stornare o eliminare le stime delle entrate.</span><span class="sxs-lookup"><span data-stu-id="d01c2-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="d01c2-106">Puoi farlo manualmente o utilizzando un processo periodico.</span><span class="sxs-lookup"><span data-stu-id="d01c2-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="d01c2-107">Questo argomento fornisce informazioni su come gestire le stime dei ricavi per i progetti.</span><span class="sxs-lookup"><span data-stu-id="d01c2-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="d01c2-108">Gestisci le stime dei ricavi manualmente</span><span class="sxs-lookup"><span data-stu-id="d01c2-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="d01c2-109">Nel progetto di stima dei ricavi a prezzo fisso o nella pagina **Richiesta di preventivo** (**Contabilità e gestione dei progetti** > **Report e richieste di informazioni** > **Richieste di informazioni sulle stime e report**), selezionare **Stime**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="d01c2-110">Gestire le stime dei ricavi utilizzando un processo periodico</span><span class="sxs-lookup"><span data-stu-id="d01c2-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="d01c2-111">Andare a **Gestione del progetto e contabilità** > **Periodico** > **Stime** e seleziona il processo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d01c2-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="d01c2-112">Creare una stima delle entrate</span><span class="sxs-lookup"><span data-stu-id="d01c2-112">Create a revenue estimate</span></span>

<span data-ttu-id="d01c2-113">Completare la seguente procedura per creare una stima dei ricavi.</span><span class="sxs-lookup"><span data-stu-id="d01c2-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="d01c2-114">Andare a **Contabilità e gestione progetti** > **Periodico** > **Stime**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="d01c2-115">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-115">Select **New**.</span></span> <span data-ttu-id="d01c2-116">Nella pagina **Creazione stima**, seleziona i seguenti parametri:</span><span class="sxs-lookup"><span data-stu-id="d01c2-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="d01c2-117">**Codice periodo**: questo codice determina la frequenza con cui vengono pubblicate le stime.</span><span class="sxs-lookup"><span data-stu-id="d01c2-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="d01c2-118">**Data di stima**: la data in cui viene elaborata la stima.</span><span class="sxs-lookup"><span data-stu-id="d01c2-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="d01c2-119">**Continuo**: selezionare questa casella di controllo per creare stime solo se le stime sono state registrate nel periodo precedente o se la stima è la prima stima che è stata creata.</span><span class="sxs-lookup"><span data-stu-id="d01c2-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="d01c2-120">Se l'opzione non è selezionata, le stime vengono create anche se non sono state registrate nel periodo precedente.</span><span class="sxs-lookup"><span data-stu-id="d01c2-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="d01c2-121">**Metodo Costo per il completamento**: definire come stimare il lavoro rimanente del progetto.</span><span class="sxs-lookup"><span data-stu-id="d01c2-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="d01c2-122">Per ulteriori informazioni, vedere [Costo per completare i metodi](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d01c2-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="d01c2-123">**Metodo di completamento**: selezionare un metodo di completamento dalle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="d01c2-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="d01c2-124">**Automatico**: la percentuale di completamento viene calcolata automaticamente e in base alle linee di costo incluse nel calcolo.</span><span class="sxs-lookup"><span data-stu-id="d01c2-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="d01c2-125">Il modello di costo definisce le righe di costo incluse.</span><span class="sxs-lookup"><span data-stu-id="d01c2-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="d01c2-126">**Manuale**: la percentuale di completamento è uguale alla percentuale di completamento dell'ultima stima.</span><span class="sxs-lookup"><span data-stu-id="d01c2-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="d01c2-127">Dopo aver creato il preventivo, puoi modificare l'opzione **Calcolo manuale** nella pagina **Stime**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="d01c2-128">**Dal modello di costo**: una combinazione dei metodi automatico e manuale.</span><span class="sxs-lookup"><span data-stu-id="d01c2-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="d01c2-129">Questa opzione viene impostata automaticamente o manualmente, a seconda del valore predefinito nel modello di costo.</span><span class="sxs-lookup"><span data-stu-id="d01c2-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="d01c2-130">**Modello di previsione**: selezionare un modello di previsione per la stima.</span><span class="sxs-lookup"><span data-stu-id="d01c2-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="d01c2-131">**Stampa elenco preventivo**: crea e mostra un elenco di preventivi.</span><span class="sxs-lookup"><span data-stu-id="d01c2-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="d01c2-132">L'elenco contiene lo stato della funzione corrente.</span><span class="sxs-lookup"><span data-stu-id="d01c2-132">The list contains the status of the current function.</span></span> <span data-ttu-id="d01c2-133">È possibile stampare eventuali avvisi sul preventivo sul report.</span><span class="sxs-lookup"><span data-stu-id="d01c2-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="d01c2-134">Le seguenti condizioni fanno apparire degli avvisi nell'elenco delle stime:</span><span class="sxs-lookup"><span data-stu-id="d01c2-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="d01c2-135">Una percentuale di completamento superiore al 100 percento.</span><span class="sxs-lookup"><span data-stu-id="d01c2-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="d01c2-136">Una percentuale di completamento inferiore allo 0 percento.</span><span class="sxs-lookup"><span data-stu-id="d01c2-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="d01c2-137">Un importo negativo nella colonna **Da completare**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="d01c2-138">Un preventivo senza importo del contratto corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d01c2-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="d01c2-139">Un preventivo senza stima dei prezzi allegato.</span><span class="sxs-lookup"><span data-stu-id="d01c2-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="d01c2-140">**Mostra Infolog**: selezionare questa opzione per ricevere un messaggio che contiene informazioni sui progetti di stima che sono stati elaborati durante l'esecuzione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="d01c2-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="d01c2-141">Pubblica WIP o ratei</span><span class="sxs-lookup"><span data-stu-id="d01c2-141">Post WIP or accruals</span></span>

<span data-ttu-id="d01c2-142">Dopo che le stime sono state valutate, vengono mantenute, diminuite o aumentate.</span><span class="sxs-lookup"><span data-stu-id="d01c2-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="d01c2-143">Puoi quindi pubblicare la WIP quando lavori usando il principio di valutazione **Contratto completato** o registrare i ratei quando lavori utilizzando il principio di valutazione **Percentuale completata**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="d01c2-144">Lo stato del periodo di stima viene modificato da **Creato** a **Registrato**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="d01c2-145">WIP storni o ratei</span><span class="sxs-lookup"><span data-stu-id="d01c2-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="d01c2-146">Utilizzare l'opzione inversa per accreditare WIP o ratei già registrati, quindi creare stime per il periodo.</span><span class="sxs-lookup"><span data-stu-id="d01c2-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="d01c2-147">Per stornare un periodo che si trova tra altri periodi, invertire i periodi di stima necessari e quindi ripubblicarli.</span><span class="sxs-lookup"><span data-stu-id="d01c2-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="d01c2-148">Poiché tutti i periodi successivi dipendono dalle stime del periodo precedente, non saltare alcun periodo.</span><span class="sxs-lookup"><span data-stu-id="d01c2-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="d01c2-149">Elimina il progetto preventivo e finisci il progetto</span><span class="sxs-lookup"><span data-stu-id="d01c2-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="d01c2-150">Il passaggio finale del processo di stima consiste nell'eliminare il progetto di stima e terminare il progetto a prezzo fisso quando la percentuale di completamento raggiunge il 100 percento.</span><span class="sxs-lookup"><span data-stu-id="d01c2-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="d01c2-151">Quando si esegue l'eliminazione si verifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d01c2-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="d01c2-152">Per un progetto a prezzo fisso con un contratto completato, i valori WIP vengono cancellati dai conti collettivi e registrati nei conti profitti e perdite.</span><span class="sxs-lookup"><span data-stu-id="d01c2-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="d01c2-153">Per un progetto a prezzo fisso con una percentuale completata, i ratei vengono rimossi dal conto profitti e perdite.</span><span class="sxs-lookup"><span data-stu-id="d01c2-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="d01c2-154">La stima cambia lo stato in **Eliminato**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="d01c2-155">In casi speciali, la percentuale può estendersi oltre il 100 percento.</span><span class="sxs-lookup"><span data-stu-id="d01c2-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="d01c2-156">Quando ciò accade, ridurre la percentuale di completamento utilizzando il **metodo Imposta costo per il completamento su zero** per raggiungere il 100 percento.</span><span class="sxs-lookup"><span data-stu-id="d01c2-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="d01c2-157">Eliminazione inversa</span><span class="sxs-lookup"><span data-stu-id="d01c2-157">Reverse elimination</span></span>

1. <span data-ttu-id="d01c2-158">Vai a **Contabilità e gestione progetti** > **Periodico** > **Stime** > **Eliminazione inversa**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="d01c2-159">Nel riquadro azioni, nella scheda **Processo**, nel gruppo **Mantieni**, selezionare **Stima**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="d01c2-160">Selezionare **Eliminazione inversa**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="d01c2-161">Utilizzare questa pagina per annullare tutte le eliminazioni con una data di stima specificata e con uno stato di stima **Eliminato**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="d01c2-162">Lo stato della transazione cambia dopo aver selezionato i campi appropriati.</span><span class="sxs-lookup"><span data-stu-id="d01c2-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="d01c2-163">Questo cambia automaticamente anche lo stato del progetto in **In corso** se la fase del progetto è finita.</span><span class="sxs-lookup"><span data-stu-id="d01c2-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="d01c2-164">Lo stato della stima del periodo del progetto torna a **Inserito**.</span><span class="sxs-lookup"><span data-stu-id="d01c2-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]