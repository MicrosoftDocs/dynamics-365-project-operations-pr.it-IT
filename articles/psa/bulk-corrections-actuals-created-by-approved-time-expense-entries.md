---
title: Correzioni in blocco di valori effettivi creati tramite voci di spesa e inserimenti ore approvati
description: In questo argomento viene indicato in che modo un amministratore può apportare correzioni singole o in blocco a voci di spesa e inserimenti ore precedentemente approvati, se la fatturazione non è completa.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: c6d849e4be9e3687396cd6a0c4158d92f25c7879
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012051"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="15cf2-103">Correzioni in blocco di valori effettivi creati tramite voci di spesa e inserimenti ore approvati</span><span class="sxs-lookup"><span data-stu-id="15cf2-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="15cf2-104">In alcuni casi, è possibile che l'immissione di voci di spesa e inserimenti ore avvenga in modo errato.</span><span class="sxs-lookup"><span data-stu-id="15cf2-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="15cf2-105">È ad esempio possibile che un consulente selezioni la data errata durante la creazione di un inserimento ora o che trasponga i numeri quando inserisce una spesa.</span><span class="sxs-lookup"><span data-stu-id="15cf2-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="15cf2-106">Sebbene un consulente non possa effettuare aggiornamenti alle voci inviate, un amministratore può correggere direttamente la voce per un progetto.</span><span class="sxs-lookup"><span data-stu-id="15cf2-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="15cf2-107">Per completare le procedure in questo argomento, devi disporre delle autorizzazioni amministratore.</span><span class="sxs-lookup"><span data-stu-id="15cf2-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="15cf2-108">Correggere gli inserimenti ore approvati</span><span class="sxs-lookup"><span data-stu-id="15cf2-108">Correct approved time entries</span></span>     

<span data-ttu-id="15cf2-109">Completa i seguenti passaggi per correggere uno o più inserimenti ore per un progetto.</span><span class="sxs-lookup"><span data-stu-id="15cf2-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="15cf2-110">Nell'area **Vendite** seleziona **Transazioni**, quindi **Ora approvata**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="15cf2-111">In **Ora approvata** elenca, individua e seleziona uno o più inserimenti ore approvate da correggere.</span><span class="sxs-lookup"><span data-stu-id="15cf2-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="15cf2-112">Puoi utilizzare il filtro per individuare voci correlate.</span><span class="sxs-lookup"><span data-stu-id="15cf2-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="15cf2-113">Ad esempio, puoi filtrare in base a un ID progetto e selezionare tutti gli inserimenti ore approvati con tale ID progetto.</span><span class="sxs-lookup"><span data-stu-id="15cf2-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="15cf2-114">Seleziona **Voci corrette**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-114">Select **Correct entries**.</span></span> <span data-ttu-id="15cf2-115">Viene automaticamente creato un nuovo giornale di registrazione correzione, con il tipo **Correzione dell'ora** assegnato.</span><span class="sxs-lookup"><span data-stu-id="15cf2-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="15cf2-116">Le voci selezionate vengono aggiunte al giornale di registrazione.</span><span class="sxs-lookup"><span data-stu-id="15cf2-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="15cf2-117">Nella pagina **Nuovo giornale di registrazione** immetti in **Descrizione** del testo per il giornale di registrazione correzione, quindi seleziona la scheda **Correzioni di inserimenti ore**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="15cf2-118">Nella sezione **Nuovi valori per gli inserimenti ore** aggiorna i campi con le informazioni corrette, come necessario.</span><span class="sxs-lookup"><span data-stu-id="15cf2-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="15cf2-119">Puoi ad esempio modificare il progetto assegnato o la risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="15cf2-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="15cf2-120">Seleziona **Anteprima**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-120">Select **Preview**.</span></span> <span data-ttu-id="15cf2-121">Nella finestra di dialogo seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="15cf2-122">Nella scheda **Righe giornale di registrazione** è visualizzato un elenco dei valori effettivi originali correlati agli inserimenti ore selezionati che sono stati ripristinati, con le righe corrispondenti corrette che sono state create.</span><span class="sxs-lookup"><span data-stu-id="15cf2-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="15cf2-123">Se è necessario apportare ulteriori correzioni, ripeti i passaggi 5 e 6.</span><span class="sxs-lookup"><span data-stu-id="15cf2-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="15cf2-124">Tutti i valori effettivi corretti avranno gli stessi valori che hai selezionato nella sezione **Nuovi valori per gli inserimenti ore**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="15cf2-125">Se le correzioni vengono visualizzate come previsto, seleziona **Conferma**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="15cf2-126">Nella finestra di dialogo seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="15cf2-127">Torna all'area **Vendite**, seleziona **Progetti** e quindi apri il progetto per il quale hai appena aggiornato gli inserimenti ore.</span><span class="sxs-lookup"><span data-stu-id="15cf2-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="15cf2-128">Nella pagina **Progetti** visualizza le modifiche che hai apportato nella scheda **Valori effettivi**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="15cf2-129">Se la scheda **Valori effettivi** non è visibile, seleziona **Elementi correlati** > **Valori effettivi**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="15cf2-130">Nell'elenco **Visualizzazione associata valore effettivo** potrai vedere che gli inserimenti ore originali che sono stati ripristinati risultano ancora elencati, così come gli inserimenti ore corrette.</span><span class="sxs-lookup"><span data-stu-id="15cf2-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="15cf2-131">Il grafico seguente contiene ad esempio due voci con una quantità pari a 8,00, con i relativi addebiti elencati nella colonna Importo.</span><span class="sxs-lookup"><span data-stu-id="15cf2-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="15cf2-132">Sono inoltre presenti due voci con una quantità pari a -8,00, i cui importi accreditati sono mostrati nella colonna Importo.</span><span class="sxs-lookup"><span data-stu-id="15cf2-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="15cf2-133">Il risultato di queste correzioni è una quantità pari a zero.</span><span class="sxs-lookup"><span data-stu-id="15cf2-133">These corrections bring the quantity to zero.</span></span>

![Elenco Visualizzazione associata valore effettivo](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="15cf2-135">Correggere le voci di spesa approvate</span><span class="sxs-lookup"><span data-stu-id="15cf2-135">Correct approved expense entries</span></span>

<span data-ttu-id="15cf2-136">Completa i seguenti passaggi per correggere una o più voci di spesa.</span><span class="sxs-lookup"><span data-stu-id="15cf2-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="15cf2-137">Nel riquadro di navigazione a sinistra dell'area **Vendite** in **Transazioni** seleziona **Spese approvate**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="15cf2-138">Nell'elenco **Spese approvate** seleziona il progetto che desideri correggere, quindi seleziona **Voci corrette**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="15cf2-139">Verrà automaticamente creato un nuovo giornale di registrazione correzione, con il tipo **Correzione di spesa** assegnato.</span><span class="sxs-lookup"><span data-stu-id="15cf2-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="15cf2-140">Nella pagina **Nuovo giornale di registrazione** inserisci in **Descrizione** del testo per la correzione e nella scheda **Correzione di spese** seleziona in **Nuovi valori per le spese** i campi dati che desideri correggere per le righe di spesa selezionate.</span><span class="sxs-lookup"><span data-stu-id="15cf2-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="15cf2-141">Puoi ad esempio assegnare la spesa a un altro **Progetto** o correggere i valori di **Categoria di spesa**, **Data spesa** o **Risorsa prenotabile**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="15cf2-142">Seleziona **Anteprima**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-142">Select **Preview**.</span></span> <span data-ttu-id="15cf2-143">Nella finestra di dialogo seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="15cf2-144">Verifica le correzioni nella scheda **Righe giornale di registrazione**. Potrai visualizzare un elenco dei valori effettivi originali correlati alle voci di spesa selezionate che sono state ripristinate, con le righe corrispondenti corrette che sono state create.</span><span class="sxs-lookup"><span data-stu-id="15cf2-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="15cf2-145">Se i valori risultano corretti come previsto, seleziona **Conferma**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="15cf2-146">Nella finestra di dialogo seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="15cf2-147">Se non vengono visualizzati i valori previsti, seleziona **Annulla** per tornare all'elenco **Spese approvate**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="15cf2-148">Ripeti i passaggi da 2 a 5.</span><span class="sxs-lookup"><span data-stu-id="15cf2-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="15cf2-149">I valori effettivi corretti avranno gli stessi valori che hai selezionato nella sezione **Nuovi valori per le spese**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="15cf2-150">Dopo aver confermato il giornale di registrazione correzione, torna al progetto o ai progetti che hai aggiornato per visualizzare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="15cf2-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="15cf2-151">Nella pagina del progetto, nella scheda **Valori effettivi** controlla **Visualizzazione associata valore effettivo**.</span><span class="sxs-lookup"><span data-stu-id="15cf2-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="15cf2-152">Viene visualizzato un elenco delle voci originali e di quelle corrette.</span><span class="sxs-lookup"><span data-stu-id="15cf2-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="15cf2-153">Il grafico seguente mostra gli importi delle voci di spesa originali e gli importi delle voci di spesa corretti corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="15cf2-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Expense_actuals](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]