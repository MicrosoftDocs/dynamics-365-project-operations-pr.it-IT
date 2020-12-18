---
title: Impostare e applicare i dati di configurazione in Common Data Service
description: Questo argomento fornisce informazioni sull'impostazione e l'applicazione dei dati di configurazione in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642233"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="4ca88-103">Impostare e applicare i dati di configurazione in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4ca88-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="4ca88-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="4ca88-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="4ca88-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4ca88-105">Prerequisites</span></span>

<span data-ttu-id="4ca88-106">Prima di iniziare a configurare i dati in Common Data Service (CDS), devono essere soddisfatti i seguenti prerequisiti:</span><span class="sxs-lookup"><span data-stu-id="4ca88-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="4ca88-107">Provisioning di un ambiente CDS e un ambiente Dynamics 365 Finance per Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4ca88-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="4ca88-108">Informazioni sulla persona giuridica di Dynamics 365 Finance condivise nell'ambiente CDS.</span><span class="sxs-lookup"><span data-stu-id="4ca88-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="4ca88-109">Ciò significa che l'entità **Società** in CDS ha i seguenti record aziendali:</span><span class="sxs-lookup"><span data-stu-id="4ca88-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="4ca88-110">THPM</span><span class="sxs-lookup"><span data-stu-id="4ca88-110">THPM</span></span>
  - <span data-ttu-id="4ca88-111">USPM</span><span class="sxs-lookup"><span data-stu-id="4ca88-111">USPM</span></span>
  - <span data-ttu-id="4ca88-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="4ca88-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="4ca88-113">Installare i dati di impostazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="4ca88-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="4ca88-114">Scarica, sblocca e decomprimi il [pacchetto dati di impostazione e configurazione](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="4ca88-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="4ca88-115">Vai alla cartella decompressa ed esegui il file eseguibile *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="4ca88-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="4ca88-116">A pagina 1 del Configurazione guidata della migrazione (CMT) di Common Data Service, seleziona **Importa dati** e poi seleziona **Continua**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrazione della configurazione](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="4ca88-118">A pagina 2 della procedura guidata CMT, seleziona **Microsoft 365** come **Tipo di distribuzione**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="4ca88-119">Seleziona le caselle di controllo **Visualizza l'elenco delle organizzazioni disponibili** e **Mostra avanzate**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="4ca88-120">Seleziona l'area del tenant, inserisci le tue credenziali e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Accesso alla configurazione](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="4ca88-122">A pagina 3, dall'elenco delle organizzazioni nel tenant, seleziona l'organizzazione in cui vuoi importare i dati dimostrativi e seleziona **Accedi**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="4ca88-123">A pagina 4, seleziona il file zip *SampleSetupAndConfigData* dalla cartella decompressa.</span><span class="sxs-lookup"><span data-stu-id="4ca88-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selezione del file zip](./media/3ZipFile.png)

![Selezionare un file](./media/4SelectAFile.png)

9. <span data-ttu-id="4ca88-126">Dopo aver selezionato il file zip, seleziona **Importa dati**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-126">After the zip file is selected, select **Import Data**.</span></span>

![Importa dati](./media/5ImportData.png)

10. <span data-ttu-id="4ca88-128">L'importazione verrà eseguita per circa due-dieci minuti a seconda della velocità della rete.</span><span class="sxs-lookup"><span data-stu-id="4ca88-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="4ca88-129">Al termine dell'importazione, esci dalla procedura guidata CMT.</span><span class="sxs-lookup"><span data-stu-id="4ca88-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="4ca88-130">Nella tua organizzazione controlla i dati nelle seguenti 19 entità:</span><span class="sxs-lookup"><span data-stu-id="4ca88-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="4ca88-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="4ca88-131">Currency</span></span>
  - <span data-ttu-id="4ca88-132">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="4ca88-132">Organizational Unit</span></span>
  - <span data-ttu-id="4ca88-133">Contatto</span><span class="sxs-lookup"><span data-stu-id="4ca88-133">Contact</span></span>
  - <span data-ttu-id="4ca88-134">Gruppo imposte</span><span class="sxs-lookup"><span data-stu-id="4ca88-134">Tax Group</span></span>
  - <span data-ttu-id="4ca88-135">Gruppo clienti</span><span class="sxs-lookup"><span data-stu-id="4ca88-135">Customer Group</span></span>
  - <span data-ttu-id="4ca88-136">Unità</span><span class="sxs-lookup"><span data-stu-id="4ca88-136">Unit</span></span>
  - <span data-ttu-id="4ca88-137">Unità di vendita</span><span class="sxs-lookup"><span data-stu-id="4ca88-137">Unit Group</span></span>
  - <span data-ttu-id="4ca88-138">Listino prezzi</span><span class="sxs-lookup"><span data-stu-id="4ca88-138">Price List</span></span>
  - <span data-ttu-id="4ca88-139">Listino prezzi di parametro progetto</span><span class="sxs-lookup"><span data-stu-id="4ca88-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="4ca88-140">Frequenza di fatturazione</span><span class="sxs-lookup"><span data-stu-id="4ca88-140">Invoice Frequency</span></span>
  - <span data-ttu-id="4ca88-141">Categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4ca88-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="4ca88-142">Categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="4ca88-142">Transaction Category</span></span>
  - <span data-ttu-id="4ca88-143">Categoria di spesa</span><span class="sxs-lookup"><span data-stu-id="4ca88-143">Expense Category</span></span>
  - <span data-ttu-id="4ca88-144">Prezzo ruolo</span><span class="sxs-lookup"><span data-stu-id="4ca88-144">Role Price</span></span>
  - <span data-ttu-id="4ca88-145">Prezzo categoria di transazione</span><span class="sxs-lookup"><span data-stu-id="4ca88-145">Transaction Category Price</span></span>
  - <span data-ttu-id="4ca88-146">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="4ca88-146">Characteristic</span></span>
  - <span data-ttu-id="4ca88-147">Risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4ca88-147">Bookable Resource</span></span>
  - <span data-ttu-id="4ca88-148">Associazione categoria di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4ca88-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="4ca88-149">Caratteristica di risorsa prenotabile</span><span class="sxs-lookup"><span data-stu-id="4ca88-149">Bookable Resource Characteristic</span></span>

![Completare l'importazione](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="4ca88-151">Aggiornare le configurazioni di Project Operations</span><span class="sxs-lookup"><span data-stu-id="4ca88-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="4ca88-152">Passa all‘ambiente CE.</span><span class="sxs-lookup"><span data-stu-id="4ca88-152">Navigate to the CE environment.</span></span> <span data-ttu-id="4ca88-153">Puoi trovarlo aprendo l'[interfaccia di amministrazione di Power Platform](https://admin.powerplatform.microsoft.com/environments), selezionando l'ambiente e quindi selezionando **Apri ambiente**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Aprire l'ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="4ca88-155">Vai a **Progetti** > **Risorse** e seleziona **Nuovo** per creare una risorsa prenotabile per il tuo utente.</span><span class="sxs-lookup"><span data-stu-id="4ca88-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Risorse prenotabili](./media/8BookableResources.png)

3. <span data-ttu-id="4ca88-157">Nella scheda **Generale**, seleziona l'utente amministratore.</span><span class="sxs-lookup"><span data-stu-id="4ca88-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="4ca88-158">Verifica che il fuso orario corrisponda a quello in cui ti trovi.</span><span class="sxs-lookup"><span data-stu-id="4ca88-158">Verify that the time zone matches the one you are in.</span></span> 

![Nuova risorsa prenotabile](./media/9NewBookableResource.png)

4. <span data-ttu-id="4ca88-160">Nella scheda **Pianificazione**, nel campo **Società**, seleziona la società **USPM**, quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Scheda Pianificazione](./media/10SchedulingTab.png)

5. <span data-ttu-id="4ca88-162">Seleziona la scheda **Orario di lavoro**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-162">Select the **Work hours** tab.</span></span>  

![Orario di lavoro](./media/11WorkHours.png)

6. <span data-ttu-id="4ca88-164">Fai doppio clic su qualsiasi valore nel calendario e seleziona **Modifica** > **Tutti gli eventi della serie**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendario lavorativo](./media/12WorkCalendar.png)

7. <span data-ttu-id="4ca88-166">Cambia l'orario di lavoro in un giorno lavorativo di otto (8) ore, contrassegna i fine settimana come giorni non lavorativi e assicurati che il fuso orario corrisponda al tuo.</span><span class="sxs-lookup"><span data-stu-id="4ca88-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="4ca88-167">Seleziona **Salva e chiudi**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-167">Select **Save and close**.</span></span>

![Aggiornare il calendario](./media/13UpdateCalendar.png)

9. <span data-ttu-id="4ca88-169">Vai a **Impostazioni** > **Modelli calendario** e seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelli calendario](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="4ca88-171">Immetti un nome, seleziona la risorsa del modello creata e quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Salvare il modello calendario](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="4ca88-173">Vai a **Parametri** e fai doppio clic sul record.</span><span class="sxs-lookup"><span data-stu-id="4ca88-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri progetto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="4ca88-175">Aggiorna i seguenti campi:</span><span class="sxs-lookup"><span data-stu-id="4ca88-175">Update the following fields:</span></span>

 - <span data-ttu-id="4ca88-176">**Società predefinita**: USPM</span><span class="sxs-lookup"><span data-stu-id="4ca88-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="4ca88-177">**Unità organizzativa predefinita**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="4ca88-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="4ca88-178">**Frequenza di fatturazione**: settimo e ultimo giorno</span><span class="sxs-lookup"><span data-stu-id="4ca88-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="4ca88-179">**Modello di ore lavorative**: cambia nel modello che hai creato.</span><span class="sxs-lookup"><span data-stu-id="4ca88-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="4ca88-180">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="4ca88-180">Select **Save**.</span></span> 

![Parametri progetto aggiornati](./media/17UpdatedProjectParameters.png)
