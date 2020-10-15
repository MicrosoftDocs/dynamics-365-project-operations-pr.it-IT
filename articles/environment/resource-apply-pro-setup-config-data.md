---
title: Impostare e applicare i dati di configurazione in Common Data Service per Project Operations
description: Questo argomento fornisce informazioni sull'impostazione e l'applicazione dei dati di configurazione in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948930"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="4a7d6-103">Impostare e applicare i dati di configurazione in Common Data Service per Project Operations</span><span class="sxs-lookup"><span data-stu-id="4a7d6-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="4a7d6-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="4a7d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="4a7d6-105">Installare i dati di impostazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="4a7d6-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="4a7d6-106">Scarica, sblocca e decomprimi il [pacchetto dati di impostazione e configurazione](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="4a7d6-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="4a7d6-107">Vai alla cartella decompressa ed esegui il file eseguibile *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="4a7d6-108">A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="4a7d6-110">A pagina 2 della procedura guidata CMT, seleziona **Office 365** come **Tipo di distribuzione**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="4a7d6-111">Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="4a7d6-112">Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Accesso alla configurazione](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="4a7d6-114">A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="4a7d6-115">A pagina 4, seleziona il file zip *SampleSetupAndConfigData* dalla cartella decompressa.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selezione del file zip](./media/3ZipFile.png)

![Selezionare un file](./media/4SelectAFile.png)

9. <span data-ttu-id="4a7d6-118">Dopo aver selezionato il file zip, seleziona **Importa dati**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-118">After the zip file is selected, select **Import Data**.</span></span>

![Importa dati](./media/5ImportData.png)

10. <span data-ttu-id="4a7d6-120">L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="4a7d6-121">Al termine dell'importazione, esci dalla procedura guidata CMT.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="4a7d6-122">Nella tua organizzazione controlla i dati nelle seguenti 19 entità:</span><span class="sxs-lookup"><span data-stu-id="4a7d6-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="4a7d6-123">Valuta</span><span class="sxs-lookup"><span data-stu-id="4a7d6-123">Currency</span></span>
  - <span data-ttu-id="4a7d6-124">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="4a7d6-124">Organizational Unit</span></span>
  - <span data-ttu-id="4a7d6-125">Contatto</span><span class="sxs-lookup"><span data-stu-id="4a7d6-125">Contact</span></span>
  - <span data-ttu-id="4a7d6-126">Gruppo imposte</span><span class="sxs-lookup"><span data-stu-id="4a7d6-126">Tax Group</span></span>
  - <span data-ttu-id="4a7d6-127">Gruppo clienti</span><span class="sxs-lookup"><span data-stu-id="4a7d6-127">Customer Group</span></span>
  - <span data-ttu-id="4a7d6-128">Unità</span><span class="sxs-lookup"><span data-stu-id="4a7d6-128">Unit</span></span>
  - <span data-ttu-id="4a7d6-129">Unità di vendita</span><span class="sxs-lookup"><span data-stu-id="4a7d6-129">Unit Group</span></span>
  - <span data-ttu-id="4a7d6-130">Listino prezzi</span><span class="sxs-lookup"><span data-stu-id="4a7d6-130">Price List</span></span>
  - <span data-ttu-id="4a7d6-131">Listino prezzi di parametro progetto</span><span class="sxs-lookup"><span data-stu-id="4a7d6-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="4a7d6-132">Frequenza di fatturazione</span><span class="sxs-lookup"><span data-stu-id="4a7d6-132">Invoice Frequency</span></span>
  - <span data-ttu-id="4a7d6-133">Categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4a7d6-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="4a7d6-134">Categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="4a7d6-134">Transaction Category</span></span>
  - <span data-ttu-id="4a7d6-135">Categoria di spesa</span><span class="sxs-lookup"><span data-stu-id="4a7d6-135">Expense Category</span></span>
  - <span data-ttu-id="4a7d6-136">Prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="4a7d6-136">Role Price</span></span>
  - <span data-ttu-id="4a7d6-137">Prezzo categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="4a7d6-137">Transaction Category Price</span></span>
  - <span data-ttu-id="4a7d6-138">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="4a7d6-138">Characteristic</span></span>
  - <span data-ttu-id="4a7d6-139">Risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4a7d6-139">Bookable Resource</span></span>
  - <span data-ttu-id="4a7d6-140">Associazione categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4a7d6-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="4a7d6-141">Caratteristica di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4a7d6-141">Bookable Resource Characteristic</span></span>

![Completare l'importazione](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="4a7d6-143">Aggiornare le configurazioni di Project Operations</span><span class="sxs-lookup"><span data-stu-id="4a7d6-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="4a7d6-144">Passa all‘ambiente CE.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-144">Navigate to the CE environment.</span></span> <span data-ttu-id="4a7d6-145">Puoi trovarlo aprendo l'[interfaccia di amministrazione di Power Platform](https://admin.powerplatform.microsoft.com/environments), selezionando l'ambiente e quindi selezionando **Apri ambiente**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Aprire l'ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="4a7d6-147">Vai a **Progetti** > **Risorse** e seleziona **Nuovo** per creare una risorsa prenotabile per il tuo utente.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Risorse prenotabili](./media/8BookableResources.png)

3. <span data-ttu-id="4a7d6-149">Nella scheda **Generale**, seleziona l'utente amministratore.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="4a7d6-150">Verifica che il fuso orario corrisponda a quello in cui ti trovi.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-150">Verify that the time zone matches the one you are in.</span></span> 

![Nuova risorsa prenotabile](./media/9NewBookableResource.png)

4. <span data-ttu-id="4a7d6-152">Nella scheda **Pianificazione**, nel campo **Società**, seleziona la società **USPM**, quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Scheda Pianificazione](./media/10SchedulingTab.png)

5. <span data-ttu-id="4a7d6-154">Seleziona la scheda **Orario di lavoro**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-154">Select the **Work hours** tab.</span></span>  

![Orario di lavoro](./media/11WorkHours.png)

6. <span data-ttu-id="4a7d6-156">Fai doppio clic su qualsiasi valore nel calendario e seleziona **Modifica** > **Tutti gli eventi della serie**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendario lavorativo](./media/12WorkCalendar.png)

7. <span data-ttu-id="4a7d6-158">Cambia l'orario di lavoro in un giorno lavorativo di otto (8) ore, contrassegna i fine settimana come giorni non lavorativi e assicurati che il fuso orario corrisponda al tuo.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="4a7d6-159">Seleziona **Salva e chiudi**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-159">Select **Save and close**.</span></span>

![Aggiornare il calendario](./media/13UpdateCalendar.png)

9. <span data-ttu-id="4a7d6-161">Vai a **Impostazioni** > **Modelli calendario** e seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelli calendario](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="4a7d6-163">Immetti un nome, seleziona la risorsa del modello creata e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Salvare il modello calendario](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="4a7d6-165">Vai a **Parametri** e fai doppio clic sul record.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri progetto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="4a7d6-167">Aggiorna i seguenti campi:</span><span class="sxs-lookup"><span data-stu-id="4a7d6-167">Update the following fields:</span></span>

 - <span data-ttu-id="4a7d6-168">**Società predefinita**: USPM</span><span class="sxs-lookup"><span data-stu-id="4a7d6-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="4a7d6-169">**Unità organizzativa predefinita**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="4a7d6-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="4a7d6-170">**Frequenza di fatturazione**: settimo e ultimo giorno</span><span class="sxs-lookup"><span data-stu-id="4a7d6-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="4a7d6-171">**Modello di ore lavorative**: cambia nel modello che hai creato.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="4a7d6-172">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4a7d6-172">Select **Save**.</span></span> 

![Parametri progetto aggiornati](./media/17UpdatedProjectParameters.png)
