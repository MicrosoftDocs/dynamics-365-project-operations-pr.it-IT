---
title: Elaborazione della ricevuta spesa
description: Questo argomento fornisce informazioni sull'elaborazione del riconoscimento ottico dei caratteri (OCR) per le ricevute. Questa funzionalità è progettata per migliorare l'esperienza dell'utente durante la creazione di ricevute spesa in Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 64901610144f9dfe274bd4c2294ab32659743a1a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960297"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="8b923-104">Elaborazione della ricevuta spesa</span><span class="sxs-lookup"><span data-stu-id="8b923-104">Expense receipt processing</span></span>

<span data-ttu-id="8b923-105">L'immissione delle spese è stata migliorata grazie all'introduzione dell'elaborazione del riconoscimento ottico dei caratteri (OCR) per le ricevute.</span><span class="sxs-lookup"><span data-stu-id="8b923-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="8b923-106">Questa funzionalità è progettata per migliorare l'esperienza dell'utente durante la creazione di ricevute spesa.</span><span class="sxs-lookup"><span data-stu-id="8b923-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="8b923-107">Funzionalità chiave</span><span class="sxs-lookup"><span data-stu-id="8b923-107">Key features</span></span>

- <span data-ttu-id="8b923-108">Il nome, la data e l'importo totale del commerciante vengono estratti dalle ricevute.</span><span class="sxs-lookup"><span data-stu-id="8b923-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="8b923-109">Il sistema tenta di abbinare le ricevute non allegate alle transazioni di spesa non associate.</span><span class="sxs-lookup"><span data-stu-id="8b923-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="8b923-110">Gli utenti possono creare transazioni di spesa inserite manualmente dalle ricevute.</span><span class="sxs-lookup"><span data-stu-id="8b923-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="8b923-111">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="8b923-111">Usage examples</span></span>

<span data-ttu-id="8b923-112">Per allegare automaticamente le ricevute che includono transazioni con carta di credito quando viene creata una nota spese, esegui i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="8b923-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="8b923-113">Apri l'area di lavoro **Gestione delle spese**.</span><span class="sxs-lookup"><span data-stu-id="8b923-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="8b923-114">Nella scheda **Ricevute** verifica che esistano ricevute non allegate.</span><span class="sxs-lookup"><span data-stu-id="8b923-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="8b923-115">Puoi anche caricare le ricevute nella scheda **Ricevute**.</span><span class="sxs-lookup"><span data-stu-id="8b923-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="8b923-116">Nella scheda **Spese** verifica che esistano spese non allegate.</span><span class="sxs-lookup"><span data-stu-id="8b923-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="8b923-117">In genere, l'amministratore importa queste spese dal fornitore della carta di credito.</span><span class="sxs-lookup"><span data-stu-id="8b923-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="8b923-118">Seleziona **Nuova nota spese**.</span><span class="sxs-lookup"><span data-stu-id="8b923-118">Select **New expense report**.</span></span> <span data-ttu-id="8b923-119">Nota che ora puoi includere anche spese e ricevute quando crei una nota spese.</span><span class="sxs-lookup"><span data-stu-id="8b923-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="8b923-120">Se aggiungi sia le spese che le ricevute, viene attivato l'abbinamento automatico delle ricevute rispetto alle spese.</span><span class="sxs-lookup"><span data-stu-id="8b923-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="8b923-121">Per creare una spesa o abbinare una spesa da una ricevuta, esegui i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="8b923-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="8b923-122">In una nota spese, nella scheda **Ricevute**, allega una ricevuta selezionando **Aggiungi ricevute**.</span><span class="sxs-lookup"><span data-stu-id="8b923-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="8b923-123">Sotto l'immagine caricata della ricevuta, nota le opzioni **Crea** e **Abbina**.</span><span class="sxs-lookup"><span data-stu-id="8b923-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="8b923-124">Seleziona **Crea** per creare una transazione di spesa inserita manualmente e compilare i valori estratti dalla ricevuta.</span><span class="sxs-lookup"><span data-stu-id="8b923-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="8b923-125">Se selezioni **Abbina**, il sistema cerca di abbinare una spesa esistente alla ricevuta.</span><span class="sxs-lookup"><span data-stu-id="8b923-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="8b923-126">Installazione</span><span class="sxs-lookup"><span data-stu-id="8b923-126">Installation</span></span>

<span data-ttu-id="8b923-127">Questa funzione utilizza in combinazione la funzione **Note spese riprogettate** per semplificare l'esperienza di spesa.</span><span class="sxs-lookup"><span data-stu-id="8b923-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="8b923-128">Questa funzione è disponibile solo per gli ambienti superiori al livello 2 che sono sandbox e di produzione.</span><span class="sxs-lookup"><span data-stu-id="8b923-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="8b923-129">Per utilizzare queste funzionalità avanzate di spesa, installa il componente aggiuntivo Servizio gestione delle spese per Microsoft Dynamics 365 Finance e attiva le funzionalità nella tua istanza.</span><span class="sxs-lookup"><span data-stu-id="8b923-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="8b923-130">Puoi accedere al componente aggiuntivo dal tuo progetto in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8b923-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="8b923-131">Accedi a LCS e apri l'ambiente desiderato.</span><span class="sxs-lookup"><span data-stu-id="8b923-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="8b923-132">Vai a **Dettagli completi**.</span><span class="sxs-lookup"><span data-stu-id="8b923-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="8b923-133">Seleziona **Gestisci** o scorri verso il basso fino alla scheda dettaglio **Componenti aggiuntivi per l'ambiente**.</span><span class="sxs-lookup"><span data-stu-id="8b923-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="8b923-134">Seleziona **Installa un nuovo componente aggiuntivo**.</span><span class="sxs-lookup"><span data-stu-id="8b923-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="8b923-135">Seleziona **Servizio gestione delle spese**.</span><span class="sxs-lookup"><span data-stu-id="8b923-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="8b923-136">Segui la guida all'installazione e accetta le condizioni.</span><span class="sxs-lookup"><span data-stu-id="8b923-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="8b923-137">Seleziona **Installa**.</span><span class="sxs-lookup"><span data-stu-id="8b923-137">Select **Install**.</span></span>

<span data-ttu-id="8b923-138">Nell'area di lavoro **Gestione delle funzionalità**, attiva le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="8b923-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="8b923-139">Note spese riprogettate</span><span class="sxs-lookup"><span data-stu-id="8b923-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="8b923-140">Abbina automaticamente e crea spesa dalla ricevuta</span><span class="sxs-lookup"><span data-stu-id="8b923-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="8b923-141">Quando attivi queste funzionalità, si verificano le seguenti azioni:</span><span class="sxs-lookup"><span data-stu-id="8b923-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="8b923-142">L'area di lavoro esistente **Gestione delle spese** viene sostituita con la nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8b923-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="8b923-143">Viene aggiunta una nuova voce di menu per la visibilità del campo di spesa.</span><span class="sxs-lookup"><span data-stu-id="8b923-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="8b923-144">Puoi ancora aprire la pagina **Note spese** precedente andando a **Gestione delle spese > Le mie spese > Note spese**.</span><span class="sxs-lookup"><span data-stu-id="8b923-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="8b923-145">I flussi di lavoro e le eventuali approvazioni ti portano comunque alla pagina delle note spese esistenti.</span><span class="sxs-lookup"><span data-stu-id="8b923-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="8b923-146">Le ricevute verranno elaborate tramite Microsoft Azure Cognitive Services e i metadati verranno estratti e aggiunti.</span><span class="sxs-lookup"><span data-stu-id="8b923-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="8b923-147">Viene aggiunta un'opzione che consente di creare una nota spese che include ricevute non allegate abbinate.</span><span class="sxs-lookup"><span data-stu-id="8b923-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="8b923-148">Un'opzione aggiunta alle note spese consente di creare una riga di spesa da una ricevuta o di tentare di abbinare una ricevuta esistente a una riga di spesa esistente.</span><span class="sxs-lookup"><span data-stu-id="8b923-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="8b923-149">Per ulteriori informazioni sulla funzione Note spese riprogettate, vedi [Note spese riprogettate](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="8b923-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8b923-150">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="8b923-150">Frequently asked questions</span></span>

<span data-ttu-id="8b923-151">**Microsoft utilizza i miei dati per i suoi modelli?**</span><span class="sxs-lookup"><span data-stu-id="8b923-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="8b923-152">No, Microsoft ha creato un modello generale di apprendimento automatico per il suo servizio di elaborazione delle ricevute.</span><span class="sxs-lookup"><span data-stu-id="8b923-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="8b923-153">Questo modello non si basa sulle ricevute che carichi.</span><span class="sxs-lookup"><span data-stu-id="8b923-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="8b923-154">**Dove è disponibile e viene elaborata questa funzione?**</span><span class="sxs-lookup"><span data-stu-id="8b923-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="8b923-155">Attualmente sono supportati gli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="8b923-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="8b923-156">**Dove vanno le mie ricevute?**</span><span class="sxs-lookup"><span data-stu-id="8b923-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="8b923-157">Finance contatta Cognitive Services per estrarre i dati sul campo.</span><span class="sxs-lookup"><span data-stu-id="8b923-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="8b923-158">Cognitive Services conserveranno una copia della ricevuta per un massimo di 24 ore durante l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="8b923-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="8b923-159">Una volta completata l'elaborazione, Cognitive Services rimuoveranno la ricevuta.</span><span class="sxs-lookup"><span data-stu-id="8b923-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="8b923-160">Le ricevute sono ancora archiviate in Finance.</span><span class="sxs-lookup"><span data-stu-id="8b923-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="8b923-161">Per ulteriori informazioni, vedi [Abilitare la comprensione delle ricevute con la nuova funzionalità di riconoscimento modulo](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="8b923-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
