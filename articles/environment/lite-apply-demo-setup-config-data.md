---
title: Applicare i dati di configurazione e la configurazione dimostrativa
description: Questo argomento fornisce informazioni su come applicare la configurazione dimostrativa i dati di configurazione in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078741"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="10882-103">Applica la configurazione demo e i dati di configurazione per la distribuzione semplice di Project Operations: accordo per la fatturazione proforma</span><span class="sxs-lookup"><span data-stu-id="10882-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="10882-104">_\*\*Distribuzione semplice: accordo per la fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="10882-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="10882-105">Scarica il [Pacchetto dati master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="10882-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="10882-106">Vai alla cartella *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ed esegui il file eseguibile *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="10882-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="10882-107">A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.</span><span class="sxs-lookup"><span data-stu-id="10882-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="10882-109">A pagina 2 della procedura guidata CMT, seleziona **Microsoft 365** come **Tipo di distribuzione**.</span><span class="sxs-lookup"><span data-stu-id="10882-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="10882-110">Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.</span><span class="sxs-lookup"><span data-stu-id="10882-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="10882-111">Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="10882-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Accesso alla configurazione](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="10882-113">A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="10882-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="10882-114">A pagina 4, seleziona il file zip, *MasterAndSetupData* dalla cartella decompressa, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="10882-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![File ZIP](./media/3ZipFile.png)

![Selezionare un file](./media/4SelectAFile.png)

9. <span data-ttu-id="10882-117">Dopo aver selezionato il file zip, seleziona **Importa dati**.</span><span class="sxs-lookup"><span data-stu-id="10882-117">After the zip file is selected, select **Import Data**.</span></span>

![Importa dati](./media/5ImportData.png)

10. <span data-ttu-id="10882-119">L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete.</span><span class="sxs-lookup"><span data-stu-id="10882-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="10882-120">Al termine dell'operazione, esci dalla procedura guidata CMT.</span><span class="sxs-lookup"><span data-stu-id="10882-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="10882-121">Nella tua organizzazione controlla i dati nelle seguenti 20 entità:</span><span class="sxs-lookup"><span data-stu-id="10882-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="10882-122">Valuta</span><span class="sxs-lookup"><span data-stu-id="10882-122">Currency</span></span>
- <span data-ttu-id="10882-123">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="10882-123">Organizational Unit</span></span>
- <span data-ttu-id="10882-124">Contatto</span><span class="sxs-lookup"><span data-stu-id="10882-124">Contact</span></span>
- <span data-ttu-id="10882-125">Gruppo imposte</span><span class="sxs-lookup"><span data-stu-id="10882-125">Tax Group</span></span>
- <span data-ttu-id="10882-126">Gruppo clienti</span><span class="sxs-lookup"><span data-stu-id="10882-126">Customer Group</span></span>
- <span data-ttu-id="10882-127">Unità</span><span class="sxs-lookup"><span data-stu-id="10882-127">Unit</span></span>
- <span data-ttu-id="10882-128">Unità di vendita</span><span class="sxs-lookup"><span data-stu-id="10882-128">Unit Group</span></span>
- <span data-ttu-id="10882-129">Listino prezzi</span><span class="sxs-lookup"><span data-stu-id="10882-129">Price List</span></span>
- <span data-ttu-id="10882-130">Listino prezzi di parametro progetto</span><span class="sxs-lookup"><span data-stu-id="10882-130">Project Parameter Price List</span></span>
- <span data-ttu-id="10882-131">Frequenza di fatturazione</span><span class="sxs-lookup"><span data-stu-id="10882-131">Invoice Frequency</span></span>
- <span data-ttu-id="10882-132">Dettagli di frequenza di fatturazione</span><span class="sxs-lookup"><span data-stu-id="10882-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="10882-133">Categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="10882-133">Bookable Resource Category</span></span>
- <span data-ttu-id="10882-134">Categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="10882-134">Transaction Category</span></span>
- <span data-ttu-id="10882-135">Categoria di spesa</span><span class="sxs-lookup"><span data-stu-id="10882-135">Expense Category</span></span>
- <span data-ttu-id="10882-136">Prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="10882-136">Role Price</span></span>
- <span data-ttu-id="10882-137">Prezzo categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="10882-137">Transaction Category Price</span></span>
- <span data-ttu-id="10882-138">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="10882-138">Characteristic</span></span>
- <span data-ttu-id="10882-139">Risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="10882-139">Bookable Resource</span></span>
- <span data-ttu-id="10882-140">Associazione categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="10882-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="10882-141">Caratteristica di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="10882-141">Bookable Resource Characteristic</span></span>

![Completare l'importazione](./media/6CompleteImport.png)
