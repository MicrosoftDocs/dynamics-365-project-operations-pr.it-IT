---
title: Configurare l'integrazione della carta di credito
description: Questo argomento descrive come utilizzare le transazioni con carta di credito correlate alle spese.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001826"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="2a24e-103">Configurare l'integrazione della carta di credito</span><span class="sxs-lookup"><span data-stu-id="2a24e-103">Set up credit card integration</span></span>

<span data-ttu-id="2a24e-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="2a24e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2a24e-105">Le transazioni con carta di credito relative alle spese possono essere impostate in modo che vengano importate automaticamente in base a una pianificazione ricorrente.</span><span class="sxs-lookup"><span data-stu-id="2a24e-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="2a24e-106">In alternativa, le transazioni possono essere importate manualmente in base alle necessità.</span><span class="sxs-lookup"><span data-stu-id="2a24e-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="2a24e-107">Le transazioni con carta di credito vengono importate tramite l'entità di dati per le transazioni con carta di credito.</span><span class="sxs-lookup"><span data-stu-id="2a24e-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="2a24e-108">Importare le transazioni con carta di credito</span><span class="sxs-lookup"><span data-stu-id="2a24e-108">Import credit card transactions</span></span>

<span data-ttu-id="2a24e-109">Per importare transazioni con carta di credito, segui questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="2a24e-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="2a24e-110">Nella pagina **Transazioni con carta di credito** seleziona **Importa transazioni**.</span><span class="sxs-lookup"><span data-stu-id="2a24e-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="2a24e-111">Se stai aprendo la gestione dei dati per la prima volta, il sistema deve aggiornare l'elenco delle entità di dati prima di poter continuare.</span><span class="sxs-lookup"><span data-stu-id="2a24e-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="2a24e-112">Nel campo **Nome**, immetti una descrizione univoca per il processo di importazione.</span><span class="sxs-lookup"><span data-stu-id="2a24e-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="2a24e-113">Nel campo **Formato dei dati di origine** seleziona il formato del file che contiene le transazioni della carta di credito da importare.</span><span class="sxs-lookup"><span data-stu-id="2a24e-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="2a24e-114">Seleziona **Carica**, quindi trova e seleziona il file da importare.</span><span class="sxs-lookup"><span data-stu-id="2a24e-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="2a24e-115">Dopo che il file è stato caricato, convalida la mappatura del file di transazione della carta di credito e le colonne dell'entità di dati delle transazioni della carta di credito selezionando il collegamento **Visualizza mappa** nel riquadro.</span><span class="sxs-lookup"><span data-stu-id="2a24e-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="2a24e-116">Se sono presenti errori di mappatura o se è necessario modificare la mappatura, apporta le modifiche alla mappatura dalla scheda **Visualizzazione della mappatura** o dalla scheda **Dettagli della mappatura**.</span><span class="sxs-lookup"><span data-stu-id="2a24e-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="2a24e-117">Per automatizzare le transazioni con carta di credito, seleziona **Crea processo dati ricorrente**.</span><span class="sxs-lookup"><span data-stu-id="2a24e-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="2a24e-118">Quindi puoi impostare la ricorrenza che definisce la frequenza con cui devono essere importate le transazioni con carta di credito.</span><span class="sxs-lookup"><span data-stu-id="2a24e-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="2a24e-119">Al termine, seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a24e-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="2a24e-120">Per importare ora il file selezionato, seleziona **Importa**.</span><span class="sxs-lookup"><span data-stu-id="2a24e-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="2a24e-121">Se si verificano errori durante l'importazione, puoi visualizzare il registro di esecuzione o i dati di gestione temporanea per vedere gli errori che è necessario correggere per garantire un'importazione corretta.</span><span class="sxs-lookup"><span data-stu-id="2a24e-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="2a24e-122">Se è necessario importare più di un formato di file, devi creare processi di importazione distinti per ogni tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="2a24e-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="2a24e-123">Riassegnare le transazioni con carta di credito per i dipendenti licenziati</span><span class="sxs-lookup"><span data-stu-id="2a24e-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="2a24e-124">Dopo che un record di dipendente viene terminato, l'account Active Directory Domain Services (AD DS) del dipendente viene disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2a24e-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="2a24e-125">Tuttavia, potrebbero essere attive transazioni con carta di credito che devono ancora essere spesate e rimborsate.</span><span class="sxs-lookup"><span data-stu-id="2a24e-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="2a24e-126">Nella pagina **Transazioni con carta di credito** puoi riassegnare il dipendente per qualsiasi transazione con carta di credito in cui il dipendente associato è stato terminato.</span><span class="sxs-lookup"><span data-stu-id="2a24e-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="2a24e-127">Seleziona una o più transazioni con carta di credito, quindi seleziona **Riassegna transazioni**.</span><span class="sxs-lookup"><span data-stu-id="2a24e-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="2a24e-128">È quindi possibile selezionare un altro dipendente a cui assegnare le transazioni con carta di credito.</span><span class="sxs-lookup"><span data-stu-id="2a24e-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="2a24e-129">Dopo che le transazioni con carta di credito sono state riassegnate, possono essere selezionate per una nota spese e pagate attraverso il normale processo di rimborso della nota spese.</span><span class="sxs-lookup"><span data-stu-id="2a24e-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="2a24e-130">Eliminare transazioni con carta di credito</span><span class="sxs-lookup"><span data-stu-id="2a24e-130">Delete credit card transactions</span></span> 

<span data-ttu-id="2a24e-131">A volte, dopo l'importazione delle transazioni con carta di credito, potrebbe essere necessario eliminare alcune transazioni.</span><span class="sxs-lookup"><span data-stu-id="2a24e-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="2a24e-132">Questo perché le transazioni sono duplicati o perché i dati potrebbero non essere accurati.</span><span class="sxs-lookup"><span data-stu-id="2a24e-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="2a24e-133">Gli amministratori possono utilizzare la funzionalità **"Elimina transazioni con carta di credito"** per selezionare ed eliminare transazioni con carta di credito che **non sono associate** a una nota spese.</span><span class="sxs-lookup"><span data-stu-id="2a24e-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="2a24e-134">Vai a **Attività periodiche** > **Elimina le transazioni con carta di credito**.</span><span class="sxs-lookup"><span data-stu-id="2a24e-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="2a24e-135">Seleziona **Filtro** e fornisci informazioni per identificare i record da includere.</span><span class="sxs-lookup"><span data-stu-id="2a24e-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="2a24e-136">Seleziona **OK** per eliminare i record.</span><span class="sxs-lookup"><span data-stu-id="2a24e-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
