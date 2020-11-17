---
title: Abbinare la ricevuta a una spesa utilizzando OCR
description: Questo argomento fornisce informazioni sull'elaborazione del riconoscimento ottico dei caratteri (OCR) per le ricevute.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124328"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="5cd66-103">Abbinare la ricevuta a una spesa utilizzando OCR</span><span class="sxs-lookup"><span data-stu-id="5cd66-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="5cd66-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="5cd66-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5cd66-105">L'immissione delle spese è stata migliorata grazie all'introduzione dell'elaborazione del riconoscimento ottico dei caratteri (OCR) per le ricevute.</span><span class="sxs-lookup"><span data-stu-id="5cd66-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="5cd66-106">Questa funzionalità è progettata per migliorare l'esperienza dell'utente durante la creazione di note spese.</span><span class="sxs-lookup"><span data-stu-id="5cd66-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="5cd66-107">Funzionalità chiave</span><span class="sxs-lookup"><span data-stu-id="5cd66-107">Key features</span></span>

- <span data-ttu-id="5cd66-108">Il sistema estrae il nome, la data e l'importo totale del commerciante dalle ricevute.</span><span class="sxs-lookup"><span data-stu-id="5cd66-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="5cd66-109">Il sistema tenterà di abbinare le ricevute non allegate alle transazioni di spesa non associate.</span><span class="sxs-lookup"><span data-stu-id="5cd66-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="5cd66-110">Puoi creare transazioni di spesa inserite manualmente dalle ricevute.</span><span class="sxs-lookup"><span data-stu-id="5cd66-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="5cd66-111">Allegare le ricevute a una nota spese</span><span class="sxs-lookup"><span data-stu-id="5cd66-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="5cd66-112">Per allegare automaticamente le ricevute che includono transazioni con carta di credito quando viene creata una nota spese, completa i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="5cd66-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="5cd66-113">Apri l'area di lavoro **Gestione delle spese**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="5cd66-114">Nella scheda **Ricevute** verifica che esistano ricevute non allegate.</span><span class="sxs-lookup"><span data-stu-id="5cd66-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="5cd66-115">Puoi anche caricare le ricevute nella scheda **Ricevute**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="5cd66-116">Nella scheda **Spese** verifica che esistano spese non allegate.</span><span class="sxs-lookup"><span data-stu-id="5cd66-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="5cd66-117">In genere, l'amministratore importa queste spese dal fornitore della carta di credito.</span><span class="sxs-lookup"><span data-stu-id="5cd66-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="5cd66-118">Seleziona **Nuova nota spese**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-118">Select **New expense report**.</span></span> <span data-ttu-id="5cd66-119">Nota che ora puoi includere anche spese e ricevute quando crei una nota spese.</span><span class="sxs-lookup"><span data-stu-id="5cd66-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="5cd66-120">Se aggiungi sia le spese che le ricevute, viene attivato l'abbinamento automatico delle ricevute rispetto alle spese.</span><span class="sxs-lookup"><span data-stu-id="5cd66-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="5cd66-121">Creare o abbinare le ricevute a una nota spese</span><span class="sxs-lookup"><span data-stu-id="5cd66-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="5cd66-122">Per creare una spesa o abbinare una spesa da una ricevuta, completa i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="5cd66-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="5cd66-123">In una nota spese, nella scheda **Ricevute**, allega una ricevuta selezionando **Aggiungi ricevute**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="5cd66-124">Sotto l'immagine caricata della ricevuta, nota le opzioni **Crea** e **Abbina**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="5cd66-125">Seleziona **Crea** per creare una transazione di spesa inserita manualmente e compilare i valori estratti dalla ricevuta.</span><span class="sxs-lookup"><span data-stu-id="5cd66-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="5cd66-126">Se selezioni **Abbina**, il sistema cerca di abbinare una spesa esistente alla ricevuta.</span><span class="sxs-lookup"><span data-stu-id="5cd66-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="5cd66-127">Installazione</span><span class="sxs-lookup"><span data-stu-id="5cd66-127">Installation</span></span>

<span data-ttu-id="5cd66-128">Per utilizzare queste funzionalità avanzate di spesa, installa il componente aggiuntivo Servizio gestione delle spese per Microsoft Dynamics 365 Finance e attiva le funzionalità nella tua istanza.</span><span class="sxs-lookup"><span data-stu-id="5cd66-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="5cd66-129">Puoi accedere al componente aggiuntivo dal tuo progetto in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5cd66-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="5cd66-130">Accedi a LCS e apri l'ambiente desiderato.</span><span class="sxs-lookup"><span data-stu-id="5cd66-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="5cd66-131">Vai a **Dettagli completi**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="5cd66-132">Seleziona **Gestisci** o scorri verso il basso fino alla scheda dettaglio **Componenti aggiuntivi per l'ambiente**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="5cd66-133">Seleziona **Installa un nuovo componente aggiuntivo**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="5cd66-134">Seleziona **Servizio gestione delle spese**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="5cd66-135">Segui la guida all'installazione e accetta le condizioni.</span><span class="sxs-lookup"><span data-stu-id="5cd66-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="5cd66-136">Seleziona **Installa**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-136">Select **Install**.</span></span>

<span data-ttu-id="5cd66-137">Nell'area di lavoro **Gestione delle funzionalità**, attiva le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="5cd66-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="5cd66-138">Note spese riprogettate</span><span class="sxs-lookup"><span data-stu-id="5cd66-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="5cd66-139">Abbina automaticamente e crea spesa dalla ricevuta</span><span class="sxs-lookup"><span data-stu-id="5cd66-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="5cd66-140">Quando attivi queste funzionalità, si verificano le seguenti azioni:</span><span class="sxs-lookup"><span data-stu-id="5cd66-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="5cd66-141">L'area di lavoro esistente **Gestione delle spese** viene sostituita con la nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5cd66-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="5cd66-142">Viene aggiunta una nuova voce di menu per la visibilità del campo di spesa.</span><span class="sxs-lookup"><span data-stu-id="5cd66-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="5cd66-143">Puoi ancora aprire la pagina **Note spese** precedente andando a **Gestione delle spese > Le mie spese > Note spese**.</span><span class="sxs-lookup"><span data-stu-id="5cd66-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="5cd66-144">I flussi di lavoro e le eventuali approvazioni ti portano comunque alla pagina delle note spese esistenti.</span><span class="sxs-lookup"><span data-stu-id="5cd66-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="5cd66-145">Le ricevute verranno elaborate tramite Microsoft Azure Cognitive Services e i metadati verranno estratti e aggiunti.</span><span class="sxs-lookup"><span data-stu-id="5cd66-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="5cd66-146">Viene aggiunta un'opzione che consente di creare una nota spese che include ricevute non allegate abbinate.</span><span class="sxs-lookup"><span data-stu-id="5cd66-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="5cd66-147">Un'opzione aggiunta alle note spese consente di creare una riga di spesa da una ricevuta o di tentare di abbinare una ricevuta esistente a una riga di spesa esistente.</span><span class="sxs-lookup"><span data-stu-id="5cd66-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="5cd66-148">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="5cd66-148">Frequently asked questions</span></span>

<span data-ttu-id="5cd66-149">**Microsoft utilizza i miei dati per i suoi modelli?**</span><span class="sxs-lookup"><span data-stu-id="5cd66-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="5cd66-150">No, Microsoft ha creato un modello generale di apprendimento automatico per il suo servizio di elaborazione delle ricevute.</span><span class="sxs-lookup"><span data-stu-id="5cd66-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="5cd66-151">Questo modello non si basa sulle ricevute che carichi.</span><span class="sxs-lookup"><span data-stu-id="5cd66-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="5cd66-152">**Dove è disponibile e viene elaborata questa funzione?**</span><span class="sxs-lookup"><span data-stu-id="5cd66-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="5cd66-153">Attualmente sono supportati gli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="5cd66-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="5cd66-154">**Dove vanno le mie ricevute?**</span><span class="sxs-lookup"><span data-stu-id="5cd66-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="5cd66-155">Finance contatta Cognitive Services per estrarre i dati sul campo.</span><span class="sxs-lookup"><span data-stu-id="5cd66-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="5cd66-156">Cognitive Services conserveranno una copia della ricevuta per un massimo di 24 ore durante l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="5cd66-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="5cd66-157">Una volta completata l'elaborazione, Cognitive Services rimuoveranno la ricevuta.</span><span class="sxs-lookup"><span data-stu-id="5cd66-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="5cd66-158">Le ricevute sono ancora archiviate in Finance.</span><span class="sxs-lookup"><span data-stu-id="5cd66-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="5cd66-159">Per ulteriori informazioni, vedi [Abilitare la comprensione delle ricevute con la nuova funzionalità di riconoscimento modulo](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="5cd66-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
