---
title: Configurare l'integrazione della carta di credito
description: Questo argomento spiega come importare e gestire le transazioni con carta di credito relative alle spese.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 12c7971204b485ee7cb222cd9cffdfdfde93dcf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078839"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="36e2b-103">Configurare l'integrazione della carta di credito</span><span class="sxs-lookup"><span data-stu-id="36e2b-103">Set up credit card integration</span></span>

<span data-ttu-id="36e2b-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="36e2b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="36e2b-105">Le transazioni con carta di credito relative alle spese possono essere impostate in modo che vengano importate automaticamente in base a una pianificazione ricorrente.</span><span class="sxs-lookup"><span data-stu-id="36e2b-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="36e2b-106">In alternativa, le transazioni possono essere importate manualmente in base alle necessità.</span><span class="sxs-lookup"><span data-stu-id="36e2b-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="36e2b-107">Le transazioni con carta di credito vengono importate tramite l'entità di dati Transazioni con carta di credito.</span><span class="sxs-lookup"><span data-stu-id="36e2b-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="36e2b-108">Importare le transazioni con carta di credito</span><span class="sxs-lookup"><span data-stu-id="36e2b-108">Import credit card transactions</span></span>

1. <span data-ttu-id="36e2b-109">Nella pagina **Transazioni con carta di credito** seleziona **Importa transazioni**.</span><span class="sxs-lookup"><span data-stu-id="36e2b-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="36e2b-110">Se stai aprendo la gestione dei dati per la prima volta, il sistema deve aggiornare l'elenco delle entità di dati prima di poter continuare.</span><span class="sxs-lookup"><span data-stu-id="36e2b-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="36e2b-111">Nella campo **Nome** immetti una descrizione univoca per il processo di importazione.</span><span class="sxs-lookup"><span data-stu-id="36e2b-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="36e2b-112">Nel campo **Formato dei dati di origine** seleziona il formato del file che contiene le transazioni della carta di credito da importare.</span><span class="sxs-lookup"><span data-stu-id="36e2b-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="36e2b-113">Seleziona **Carica** , quindi trova e seleziona il file da importare.</span><span class="sxs-lookup"><span data-stu-id="36e2b-113">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="36e2b-114">Dopo che il file è stato caricato, convalida la mappatura del file di transazione della carta di credito e le colonne dell'entità di dati delle transazioni della carta di credito selezionando il collegamento **Visualizza mappa** sul riquadro.</span><span class="sxs-lookup"><span data-stu-id="36e2b-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="36e2b-115">Se sono presenti errori di mappatura o se è necessario modificare la mappatura, apporta le modifiche alla mappatura dalla scheda **Visualizzazione della mappatura** o dalla scheda **Dettagli della mappatura**.</span><span class="sxs-lookup"><span data-stu-id="36e2b-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="36e2b-116">Per automatizzare le transazioni con carta di credito, seleziona **Crea processo dati ricorrente**.</span><span class="sxs-lookup"><span data-stu-id="36e2b-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="36e2b-117">Quindi puoi impostare la ricorrenza che definisce la frequenza con cui devono essere importate le transazioni con carta di credito.</span><span class="sxs-lookup"><span data-stu-id="36e2b-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="36e2b-118">Al termine, seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="36e2b-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="36e2b-119">Per importare ora il file selezionato, seleziona **Importa**.</span><span class="sxs-lookup"><span data-stu-id="36e2b-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="36e2b-120">Se si verificano errori durante l'importazione, puoi visualizzare il log di esecuzione o i dati di gestione temporanea per vedere gli errori che è necessario correggere per garantire una corretta importazione.</span><span class="sxs-lookup"><span data-stu-id="36e2b-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="36e2b-121">Se devi importare più di un formato di file, è necessario creare processi di importazione separati per ogni tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="36e2b-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="36e2b-122">Riassegnare le transazioni con carta di credito per i dipendenti licenziati</span><span class="sxs-lookup"><span data-stu-id="36e2b-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="36e2b-123">Dopo che un record di dipendente viene terminato, l'account Active Directory Domain Services (AD DS) del dipendente viene disabilitato.</span><span class="sxs-lookup"><span data-stu-id="36e2b-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="36e2b-124">Tuttavia, potrebbero essere attive transazioni con carta di credito che devono ancora essere spesate e rimborsate.</span><span class="sxs-lookup"><span data-stu-id="36e2b-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="36e2b-125">Dalla pagina **Transazioni con carta di credito** puoi riassegnare il dipendente per qualsiasi transazione con carta di credito in cui il dipendente associato è stato licenziato.</span><span class="sxs-lookup"><span data-stu-id="36e2b-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="36e2b-126">Seleziona una o più transazioni con carta di credito, quindi seleziona **Riassegna transazioni**.</span><span class="sxs-lookup"><span data-stu-id="36e2b-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="36e2b-127">È quindi possibile selezionare un altro dipendente a cui assegnare le transazioni con carta di credito.</span><span class="sxs-lookup"><span data-stu-id="36e2b-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="36e2b-128">Dopo che le transazioni con carta di credito sono state riassegnate, possono essere selezionate per una nota spese e pagate attraverso il normale processo di rimborso della nota spese.</span><span class="sxs-lookup"><span data-stu-id="36e2b-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
