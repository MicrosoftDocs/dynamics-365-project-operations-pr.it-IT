---
title: Importare e gestire le transazioni con carta di credito
description: Questo argomento spiega come importare e gestire le transazioni con carta di credito relative alle spese. Queste transazioni possono essere impostate in modo che vengano importate automaticamente in base a una pianificazione ricorrente oppure possono essere importate manualmente in base alle esigenze.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079029"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="84359-104">Importare e gestire le transazioni con carta di credito</span><span class="sxs-lookup"><span data-stu-id="84359-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84359-105">Le transazioni con carta di credito relative alle spese possono essere impostate in modo che vengano importate automaticamente in base a una pianificazione ricorrente.</span><span class="sxs-lookup"><span data-stu-id="84359-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="84359-106">In alternativa, le transazioni possono essere importate manualmente in base alle necessità.</span><span class="sxs-lookup"><span data-stu-id="84359-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="84359-107">Le transazioni con carta di credito vengono importate tramite l'entità di dati Transazioni con carta di credito.</span><span class="sxs-lookup"><span data-stu-id="84359-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="84359-108">Per ulteriori informazioni sulle entità dati vedi [Entità dati](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="84359-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="84359-109">Importare le transazioni con carta di credito</span><span class="sxs-lookup"><span data-stu-id="84359-109">Import credit card transactions</span></span>

1. <span data-ttu-id="84359-110">Nella pagina **Transazioni con carta di credito** seleziona **Importa transazioni**.</span><span class="sxs-lookup"><span data-stu-id="84359-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="84359-111">Se stai aprendo la gestione dei dati per la prima volta, il sistema deve aggiornare l'elenco delle entità di dati prima di poter continuare.</span><span class="sxs-lookup"><span data-stu-id="84359-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="84359-112">Nella campo **Nome** immetti una descrizione univoca per il processo di importazione.</span><span class="sxs-lookup"><span data-stu-id="84359-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="84359-113">Nel campo **Formato dei dati di origine** seleziona il formato del file che contiene le transazioni della carta di credito da importare.</span><span class="sxs-lookup"><span data-stu-id="84359-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="84359-114">Seleziona **Carica** , quindi trova e seleziona il file da importare.</span><span class="sxs-lookup"><span data-stu-id="84359-114">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="84359-115">Dopo che il file è stato caricato, convalida la mappatura del file di transazione della carta di credito e le colonne dell'entità di dati delle transazioni della carta di credito selezionando il collegamento **Visualizza mappa** sul riquadro.</span><span class="sxs-lookup"><span data-stu-id="84359-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="84359-116">Se sono presenti errori di mappatura o se è necessario modificare la mappatura, apporta le modifiche alla mappatura dalla scheda **Visualizzazione della mappatura** o dalla scheda **Dettagli della mappatura**.</span><span class="sxs-lookup"><span data-stu-id="84359-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="84359-117">Per automatizzare le transazioni con carta di credito, seleziona **Crea processo dati ricorrente**.</span><span class="sxs-lookup"><span data-stu-id="84359-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="84359-118">Quindi puoi impostare la ricorrenza che definisce la frequenza con cui devono essere importate le transazioni con carta di credito.</span><span class="sxs-lookup"><span data-stu-id="84359-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="84359-119">Al termine, seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="84359-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="84359-120">Per importare ora il file selezionato, seleziona **Importa**.</span><span class="sxs-lookup"><span data-stu-id="84359-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="84359-121">Se si verificano errori durante l'importazione, puoi visualizzare il log di esecuzione o i dati di gestione temporanea per vedere gli errori che è necessario correggere per garantire una corretta importazione.</span><span class="sxs-lookup"><span data-stu-id="84359-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="84359-122">Se devi importare più di un formato di file, è necessario creare processi di importazione separati per ogni tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="84359-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="84359-123">Riassegnare le transazioni con carta di credito per i dipendenti licenziati</span><span class="sxs-lookup"><span data-stu-id="84359-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="84359-124">Dopo che un record di dipendente viene terminato, l'account Active Directory Domain Services (AD DS) del dipendente viene disabilitato.</span><span class="sxs-lookup"><span data-stu-id="84359-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="84359-125">Tuttavia, potrebbero essere attive transazioni con carta di credito che devono ancora essere spesate e rimborsate.</span><span class="sxs-lookup"><span data-stu-id="84359-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="84359-126">Dalla pagina **Transazioni con carta di credito** puoi riassegnare il dipendente per qualsiasi transazione con carta di credito in cui il dipendente associato è stato licenziato.</span><span class="sxs-lookup"><span data-stu-id="84359-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="84359-127">Seleziona una o più transazioni con carta di credito, quindi seleziona **Riassegna transazioni**.</span><span class="sxs-lookup"><span data-stu-id="84359-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="84359-128">È quindi possibile selezionare un altro dipendente a cui assegnare le transazioni con carta di credito.</span><span class="sxs-lookup"><span data-stu-id="84359-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="84359-129">Dopo che le transazioni con carta di credito sono state riassegnate, possono essere selezionate per una nota spese e pagate attraverso il normale processo di rimborso della nota spese.</span><span class="sxs-lookup"><span data-stu-id="84359-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
