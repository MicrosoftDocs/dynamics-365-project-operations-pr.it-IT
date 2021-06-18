---
title: Applicare i dati di configurazione e la configurazione dimostrativa - semplice
description: Questo argomento fornisce informazioni su come applicare la configurazione dimostrativa i dati di configurazione in Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997156"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="3fc50-103">Applicare i dati di configurazione e la configurazione dimostrativa per Project Operations - semplice</span><span class="sxs-lookup"><span data-stu-id="3fc50-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="3fc50-104">_\*\*Distribuzione semplice: accordo per la fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="3fc50-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="3fc50-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="3fc50-105">Prerequisites</span></span>

<span data-ttu-id="3fc50-106">Prima di iniziare la configurazione, è necessario disporre di un ambiente Common Data Service (CDS) con provisioning per Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3fc50-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="3fc50-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="3fc50-107">Instructions</span></span>

1. <span data-ttu-id="3fc50-108">Scarica il [Pacchetto dati master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="3fc50-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="3fc50-109">Vai alla cartella *ProjOpsSampleSetupData - solo CE CMT* ed esegui il file eseguibile, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="3fc50-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="3fc50-110">A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.</span><span class="sxs-lookup"><span data-stu-id="3fc50-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="3fc50-112">A pagina 2 della procedura guidata CMT, seleziona **Microsoft 365** come **Tipo di distribuzione**.</span><span class="sxs-lookup"><span data-stu-id="3fc50-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="3fc50-113">Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.</span><span class="sxs-lookup"><span data-stu-id="3fc50-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="3fc50-114">Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="3fc50-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Accesso alla configurazione](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="3fc50-116">A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="3fc50-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="3fc50-117">A pagina 4, seleziona il file zip, *SampleSetupAndConfigData* dalla cartella scompattata, *ProjOpsSampleSetupData - Solo CE CMT*.</span><span class="sxs-lookup"><span data-stu-id="3fc50-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![File ZIP](./media/3ZipFile.png)

   ![Seleziona un file](./media/4SelectAFile.png)

9. <span data-ttu-id="3fc50-120">Dopo aver selezionato il file zip, seleziona **Importa dati**.</span><span class="sxs-lookup"><span data-stu-id="3fc50-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importa dati](./media/5ImportData.png)

10. <span data-ttu-id="3fc50-122">L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete.</span><span class="sxs-lookup"><span data-stu-id="3fc50-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="3fc50-123">Al termine dell'operazione, esci dalla procedura guidata CMT.</span><span class="sxs-lookup"><span data-stu-id="3fc50-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="3fc50-124">Nella tua organizzazione controlla i dati nelle seguenti 18 entità:</span><span class="sxs-lookup"><span data-stu-id="3fc50-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="3fc50-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="3fc50-125">Currency</span></span>
    -   <span data-ttu-id="3fc50-126">Conto</span><span class="sxs-lookup"><span data-stu-id="3fc50-126">Account</span></span>
    -   <span data-ttu-id="3fc50-127">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="3fc50-127">Organizational Unit</span></span>
    -   <span data-ttu-id="3fc50-128">Contatto</span><span class="sxs-lookup"><span data-stu-id="3fc50-128">Contact</span></span>
    -   <span data-ttu-id="3fc50-129">Unità</span><span class="sxs-lookup"><span data-stu-id="3fc50-129">Unit</span></span>
    -   <span data-ttu-id="3fc50-130">Unità di vendita</span><span class="sxs-lookup"><span data-stu-id="3fc50-130">Unit Group</span></span>
    -   <span data-ttu-id="3fc50-131">Listino prezzi</span><span class="sxs-lookup"><span data-stu-id="3fc50-131">Price List</span></span>
    -   <span data-ttu-id="3fc50-132">Listino prezzi di parametro progetto</span><span class="sxs-lookup"><span data-stu-id="3fc50-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="3fc50-133">Frequenza di fatturazione</span><span class="sxs-lookup"><span data-stu-id="3fc50-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="3fc50-134">Categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="3fc50-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="3fc50-135">Categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="3fc50-135">Transaction Category</span></span>
    -   <span data-ttu-id="3fc50-136">Categoria di spesa</span><span class="sxs-lookup"><span data-stu-id="3fc50-136">Expense Category</span></span>
    -   <span data-ttu-id="3fc50-137">Prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="3fc50-137">Role Price</span></span>
    -   <span data-ttu-id="3fc50-138">Prezzo categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="3fc50-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="3fc50-139">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="3fc50-139">Characteristic</span></span>
    -   <span data-ttu-id="3fc50-140">Risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="3fc50-140">Bookable Resource</span></span>
    -   <span data-ttu-id="3fc50-141">Associazione categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="3fc50-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="3fc50-142">Caratteristica di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="3fc50-142">Bookable Resource Characteristic</span></span>

    ![Completare l'importazione](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
