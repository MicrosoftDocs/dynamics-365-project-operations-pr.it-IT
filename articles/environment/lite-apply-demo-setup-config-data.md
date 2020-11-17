---
title: Applicare i dati di configurazione e la configurazione dimostrativa - semplice
description: Questo argomento fornisce informazioni su come applicare la configurazione dimostrativa i dati di configurazione in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401268"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="79e8a-103">Applicare i dati di configurazione e la configurazione dimostrativa per Project Operations - semplice</span><span class="sxs-lookup"><span data-stu-id="79e8a-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="79e8a-104">_\*\*Distribuzione semplice: accordo per la fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="79e8a-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="79e8a-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="79e8a-105">Prerequisites</span></span>

<span data-ttu-id="79e8a-106">Prima di iniziare la configurazione, è necessario disporre di un ambiente Common Data Service (CDS) con provisioning per Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="79e8a-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="79e8a-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="79e8a-107">Instructions</span></span>

1. <span data-ttu-id="79e8a-108">Scarica il [Pacchetto dati master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="79e8a-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="79e8a-109">Vai alla cartella *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ed esegui il file eseguibile *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="79e8a-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="79e8a-110">A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.</span><span class="sxs-lookup"><span data-stu-id="79e8a-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="79e8a-112">A pagina 2 della procedura guidata CMT, seleziona **Microsoft 365** come **Tipo di distribuzione**.</span><span class="sxs-lookup"><span data-stu-id="79e8a-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="79e8a-113">Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.</span><span class="sxs-lookup"><span data-stu-id="79e8a-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="79e8a-114">Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="79e8a-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Accesso alla configurazione](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="79e8a-116">A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="79e8a-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="79e8a-117">A pagina 4, seleziona il file zip, *MasterAndSetupData* dalla cartella decompressa, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="79e8a-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![File ZIP](./media/3ZipFile.png)

![Selezionare un file](./media/4SelectAFile.png)

9. <span data-ttu-id="79e8a-120">Dopo aver selezionato il file zip, seleziona **Importa dati**.</span><span class="sxs-lookup"><span data-stu-id="79e8a-120">After the zip file is selected, select **Import Data**.</span></span>

![Importa dati](./media/5ImportData.png)

10. <span data-ttu-id="79e8a-122">L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete.</span><span class="sxs-lookup"><span data-stu-id="79e8a-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="79e8a-123">Al termine dell'operazione, esci dalla procedura guidata CMT.</span><span class="sxs-lookup"><span data-stu-id="79e8a-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="79e8a-124">Nella tua organizzazione controlla i dati nelle seguenti 20 entità:</span><span class="sxs-lookup"><span data-stu-id="79e8a-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="79e8a-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="79e8a-125">Currency</span></span>
-   <span data-ttu-id="79e8a-126">Conto</span><span class="sxs-lookup"><span data-stu-id="79e8a-126">Account</span></span>
-   <span data-ttu-id="79e8a-127">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="79e8a-127">Organizational Unit</span></span>
-   <span data-ttu-id="79e8a-128">Contatto</span><span class="sxs-lookup"><span data-stu-id="79e8a-128">Contact</span></span>
-   <span data-ttu-id="79e8a-129">Gruppo imposte</span><span class="sxs-lookup"><span data-stu-id="79e8a-129">Tax Group</span></span>
-   <span data-ttu-id="79e8a-130">Gruppo clienti</span><span class="sxs-lookup"><span data-stu-id="79e8a-130">Customer Group</span></span>
-   <span data-ttu-id="79e8a-131">Unità</span><span class="sxs-lookup"><span data-stu-id="79e8a-131">Unit</span></span>
-   <span data-ttu-id="79e8a-132">Unità di vendita</span><span class="sxs-lookup"><span data-stu-id="79e8a-132">Unit Group</span></span>
-   <span data-ttu-id="79e8a-133">Listino prezzi</span><span class="sxs-lookup"><span data-stu-id="79e8a-133">Price List</span></span>
-   <span data-ttu-id="79e8a-134">Listino prezzi di parametro progetto</span><span class="sxs-lookup"><span data-stu-id="79e8a-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="79e8a-135">Frequenza di fatturazione</span><span class="sxs-lookup"><span data-stu-id="79e8a-135">Invoice Frequency</span></span>
-   <span data-ttu-id="79e8a-136">Categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="79e8a-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="79e8a-137">Categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="79e8a-137">Transaction Category</span></span>
-   <span data-ttu-id="79e8a-138">Categoria di spesa</span><span class="sxs-lookup"><span data-stu-id="79e8a-138">Expense Category</span></span>
-   <span data-ttu-id="79e8a-139">Prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="79e8a-139">Role Price</span></span>
-   <span data-ttu-id="79e8a-140">Prezzo categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="79e8a-140">Transaction Category Price</span></span>
-   <span data-ttu-id="79e8a-141">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="79e8a-141">Characteristic</span></span>
-   <span data-ttu-id="79e8a-142">Risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="79e8a-142">Bookable Resource</span></span>
-   <span data-ttu-id="79e8a-143">Associazione categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="79e8a-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="79e8a-144">Caratteristica di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="79e8a-144">Bookable Resource Characteristic</span></span>

![Completare l'importazione](./media/6CompleteImport.png)
