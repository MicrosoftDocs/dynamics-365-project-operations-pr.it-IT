---
title: Applicare i dati di configurazione e la configurazione dimostrativa - semplice
description: Questo argomento fornisce informazioni su come applicare la configurazione dimostrativa i dati di configurazione in Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089124"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="4c96b-103">Applicare i dati di configurazione e la configurazione dimostrativa per Project Operations - semplice</span><span class="sxs-lookup"><span data-stu-id="4c96b-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="4c96b-104">_\*\*Distribuzione semplice: accordo per la fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="4c96b-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="4c96b-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4c96b-105">Prerequisites</span></span>

<span data-ttu-id="4c96b-106">Prima di iniziare la configurazione, è necessario disporre di un ambiente Common Data Service (CDS) con provisioning per Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4c96b-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="4c96b-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="4c96b-107">Instructions</span></span>

1. <span data-ttu-id="4c96b-108">Scarica il [Pacchetto dati master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="4c96b-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="4c96b-109">Vai alla cartella *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ed esegui il file eseguibile *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="4c96b-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="4c96b-110">A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.</span><span class="sxs-lookup"><span data-stu-id="4c96b-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="4c96b-112">A pagina 2 della procedura guidata CMT, seleziona **Microsoft 365** come **Tipo di distribuzione**.</span><span class="sxs-lookup"><span data-stu-id="4c96b-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="4c96b-113">Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.</span><span class="sxs-lookup"><span data-stu-id="4c96b-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="4c96b-114">Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="4c96b-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Accesso alla configurazione](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="4c96b-116">A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="4c96b-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="4c96b-117">A pagina 4, seleziona il file zip, *MasterAndSetupData* dalla cartella decompressa, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="4c96b-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![File ZIP](./media/3ZipFile.png)

   ![Selezionare un file](./media/4SelectAFile.png)

9. <span data-ttu-id="4c96b-120">Dopo aver selezionato il file zip, seleziona **Importa dati**.</span><span class="sxs-lookup"><span data-stu-id="4c96b-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importa dati](./media/5ImportData.png)

10. <span data-ttu-id="4c96b-122">L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete.</span><span class="sxs-lookup"><span data-stu-id="4c96b-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="4c96b-123">Al termine dell'operazione, esci dalla procedura guidata CMT.</span><span class="sxs-lookup"><span data-stu-id="4c96b-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="4c96b-124">Nella tua organizzazione controlla i dati nelle seguenti 20 entità:</span><span class="sxs-lookup"><span data-stu-id="4c96b-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="4c96b-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="4c96b-125">Currency</span></span>
    -   <span data-ttu-id="4c96b-126">Conto</span><span class="sxs-lookup"><span data-stu-id="4c96b-126">Account</span></span>
    -   <span data-ttu-id="4c96b-127">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="4c96b-127">Organizational Unit</span></span>
    -   <span data-ttu-id="4c96b-128">Contatto</span><span class="sxs-lookup"><span data-stu-id="4c96b-128">Contact</span></span>
    -   <span data-ttu-id="4c96b-129">Unità</span><span class="sxs-lookup"><span data-stu-id="4c96b-129">Unit</span></span>
    -   <span data-ttu-id="4c96b-130">Unità di vendita</span><span class="sxs-lookup"><span data-stu-id="4c96b-130">Unit Group</span></span>
    -   <span data-ttu-id="4c96b-131">Listino prezzi</span><span class="sxs-lookup"><span data-stu-id="4c96b-131">Price List</span></span>
    -   <span data-ttu-id="4c96b-132">Listino prezzi di parametro progetto</span><span class="sxs-lookup"><span data-stu-id="4c96b-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="4c96b-133">Frequenza di fatturazione</span><span class="sxs-lookup"><span data-stu-id="4c96b-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="4c96b-134">Categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4c96b-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="4c96b-135">Categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="4c96b-135">Transaction Category</span></span>
    -   <span data-ttu-id="4c96b-136">Categoria di spesa</span><span class="sxs-lookup"><span data-stu-id="4c96b-136">Expense Category</span></span>
    -   <span data-ttu-id="4c96b-137">Prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="4c96b-137">Role Price</span></span>
    -   <span data-ttu-id="4c96b-138">Prezzo categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="4c96b-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="4c96b-139">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="4c96b-139">Characteristic</span></span>
    -   <span data-ttu-id="4c96b-140">Risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4c96b-140">Bookable Resource</span></span>
    -   <span data-ttu-id="4c96b-141">Associazione categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4c96b-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="4c96b-142">Caratteristica di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4c96b-142">Bookable Resource Characteristic</span></span>

    ![Completare l'importazione](./media/6CompleteImport.png)
