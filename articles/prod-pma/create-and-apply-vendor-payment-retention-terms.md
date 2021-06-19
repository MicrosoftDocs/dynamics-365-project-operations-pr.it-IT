---
title: Creare e applicare le condizioni di trattenimento dei pagamenti del fornitore
description: Questo argomento fornisce informazioni su come impostare e mantenere le condizioni di trattenimento per i pagamenti dei fornitori.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006335"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="478a5-103">Creare e applicare le condizioni di trattenimento dei pagamenti del fornitore</span><span class="sxs-lookup"><span data-stu-id="478a5-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="478a5-104">L'impostazione delle condizioni di trattenimento dei pagamenti del fornitore per un progetto è utile quando l'organizzazione desidera trattenere parte dei pagamenti effettuati a un fornitore.</span><span class="sxs-lookup"><span data-stu-id="478a5-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="478a5-105">Ad esempio, quando desideri trattenere il pagamento a un fornitore finché i prodotti consegnati non soddisfano le tue aspettative.</span><span class="sxs-lookup"><span data-stu-id="478a5-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="478a5-106">Le condizioni di trattenimento del pagamento del fornitore possono essere specificate quando si negozia un contratto con il fornitore.</span><span class="sxs-lookup"><span data-stu-id="478a5-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="478a5-107">Creare le condizioni di trattenimento dei pagamenti del fornitore</span><span class="sxs-lookup"><span data-stu-id="478a5-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="478a5-108">Puoi inserire la percentuale del pagamento del fornitore da trattenere e la percentuale degli importi precedentemente trattenuti da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="478a5-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="478a5-109">Gli importi vengono automaticamente trattenuti sulle fatture fornitore fino a quando il contratto non raggiunge lo stato di completamento specificato.</span><span class="sxs-lookup"><span data-stu-id="478a5-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="478a5-110">Dopo aver impostato le condizioni di trattenimento, è possibile applicarle a qualsiasi progetto per quel fornitore.</span><span class="sxs-lookup"><span data-stu-id="478a5-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="478a5-111">Utilizza i passaggi seguenti per impostare e mantenere condizioni di trattenimento per i pagamenti del fornitore.</span><span class="sxs-lookup"><span data-stu-id="478a5-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="478a5-112">Vai a **Gestione progetti e contabilità** > **Trattenimento** > **Condizioni di trattenimento del pagamento del fornitore**.</span><span class="sxs-lookup"><span data-stu-id="478a5-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="478a5-113">Seleziona **Nuovo** per aggiungere una nuova condizione di trattenimento del fornitore.</span><span class="sxs-lookup"><span data-stu-id="478a5-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="478a5-114">Il valore **ID regola** per il nuovo termine viene inserito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="478a5-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="478a5-115">Immetti una breve descrizione nel campo **Descrizione** e nella scheda dettaglio **Condizioni** seleziona **Aggiungi riga** per inserire i valori delle condizioni per quanto segue:</span><span class="sxs-lookup"><span data-stu-id="478a5-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="478a5-116">**Percentuale di unità consegnate**: immetti una percentuale di completamento per la condizione.</span><span class="sxs-lookup"><span data-stu-id="478a5-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="478a5-117">Gli importi vengono automaticamente trattenuti sulle fatture fornitore fino a quando la fase di completamento del progetto è uguale alla percentuale specificata.</span><span class="sxs-lookup"><span data-stu-id="478a5-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="478a5-118">Ad esempio, se si immette 50,00, gli importi vengono trattenuti fino al completamento del 50% del progetto.</span><span class="sxs-lookup"><span data-stu-id="478a5-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="478a5-119">**Percentuale da trattenere**: immetti una percentuale dell'importo della fattura fornitore da trattenere.</span><span class="sxs-lookup"><span data-stu-id="478a5-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="478a5-120">Ad esempio, se immetti 10,00, viene trattenuto il 10 percento dell'importo su una fattura fornitore fino a quando il progetto non raggiunge la percentuale di completamento come impostato nel **campo Percentuale di unità consegnate**.</span><span class="sxs-lookup"><span data-stu-id="478a5-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="478a5-121">**Percentuale da rilasciare**: seleziona **Aggiungi riga** per immettere una percentuale di eventuali importi precedentemente trattenuti da rilasciare per il livello di completamento del progetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="478a5-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="478a5-122">Se hai più passaggi fondamentali per diversi livelli di completamento del progetto, immetti una riga della condizione di trattenimento del fornitore separata per ciascuna regola di trattenimento.</span><span class="sxs-lookup"><span data-stu-id="478a5-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="478a5-123">Ogni riga può specificare una percentuale di trattenimento diversa e una percentuale di rilascio diversa per ogni livello designato di completamento del progetto.</span><span class="sxs-lookup"><span data-stu-id="478a5-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="478a5-124">Dopo aver creato le condizioni di trattenimento per un fornitore, è possibile applicarle a un progetto.</span><span class="sxs-lookup"><span data-stu-id="478a5-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="478a5-125">Applicare le condizioni di trattenimento del fornitore a un progetto</span><span class="sxs-lookup"><span data-stu-id="478a5-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="478a5-126">Vai a **Gestione progetti e contabilità** > **Progetti** > **Tutti i progetti** e apri un progetto dalla pagina elenco dei progetti.</span><span class="sxs-lookup"><span data-stu-id="478a5-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="478a5-127">Nella scheda dettaglio **Contratti fornitori** seleziona **Aggiungi riga**.</span><span class="sxs-lookup"><span data-stu-id="478a5-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="478a5-128">Nel **campo Codice conto**, seleziona una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="478a5-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="478a5-129">**Tabella**: le condizioni di trattenimento per il fornitore si applicano a un singolo fornitore.</span><span class="sxs-lookup"><span data-stu-id="478a5-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="478a5-130">**Gruppo**: le condizioni di trattenimento per il fornitore si applicano a tutti i fornitori in un gruppo di fornitori.</span><span class="sxs-lookup"><span data-stu-id="478a5-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="478a5-131">**Tutto**: le condizioni di trattenimento per il fornitore si applicano a tutti i fornitori.</span><span class="sxs-lookup"><span data-stu-id="478a5-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="478a5-132">Nel **campo fornitore/gruppo di fornitori**, seleziona il fornitore o il gruppo di fornitori a cui si applicano le condizioni di trattenimento per il fornitore.</span><span class="sxs-lookup"><span data-stu-id="478a5-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="478a5-133">Se hai selezionato **Tutto** nel passaggio precedente, questo campo non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="478a5-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="478a5-134">Nel campo **Condizioni di trattenimento per il fornitore** seleziona le condizioni di trattenimento che hai creato nella procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="478a5-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="478a5-135">Se il progetto ha anche le condizioni di pagamento su pagamento impostati per il fornitore, immetti la percentuale di soglia per il progetto nel campo **Percentuale soglia pagamento su pagamento**.</span><span class="sxs-lookup"><span data-stu-id="478a5-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="478a5-136">Le condizioni di trattenimento per il fornitore vengono visualizzate anche negli ordini di acquisto creati per il fornitore.</span><span class="sxs-lookup"><span data-stu-id="478a5-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]