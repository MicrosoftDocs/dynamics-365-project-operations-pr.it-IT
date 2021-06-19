---
title: Aggiornare Project Operations nel tuo ambiente Finance
description: Questo argomento fornisce informazioni su come aggiornare Project Operations nell'ambiente Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011061"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="657e1-103">Aggiornare Project Operations nel tuo ambiente Finance</span><span class="sxs-lookup"><span data-stu-id="657e1-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="657e1-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="657e1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="657e1-105">Questo argomento fornisce informazioni su come aggiornare Dynamics 365 Project Operations nell'ambiente Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="657e1-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="657e1-106">Sono disponibili tre procedure richieste per aggiornare Project Operations all'aggiornamento 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="657e1-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="657e1-107">Importare il pacchetto nel progetto di anteprima</span><span class="sxs-lookup"><span data-stu-id="657e1-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="657e1-108">Applicare l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="657e1-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="657e1-109">Aggiornare l'ambiente Dataverse</span><span class="sxs-lookup"><span data-stu-id="657e1-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="657e1-110">Importare il pacchetto nel progetto LCS</span><span class="sxs-lookup"><span data-stu-id="657e1-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="657e1-111">Accedi a [Lifecycle Services (LCS)](https://lcs.dynamics.com/) come proprietario del progetto o responsabile dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="657e1-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="657e1-112">Nell'elenco dei progetti seleziona il progetto LCS.</span><span class="sxs-lookup"><span data-stu-id="657e1-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="657e1-113">Nella pagina **Progetto** nel gruppo **Ambienti** apri l'ambiente che desideri aggiornare.</span><span class="sxs-lookup"><span data-stu-id="657e1-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="657e1-114">Verifica che l'ambiente sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="657e1-114">Verify that the environment is running.</span></span> <span data-ttu-id="657e1-115">Se non è avviato, avvia l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="657e1-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="657e1-116">Nella sezione **Nuova versione** sotto **Aggiornamenti disponibili**, seleziona **Visualizza aggiornamento** per 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="657e1-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Pulsante Visualizza aggiornamento](media/view-update.png)

6. <span data-ttu-id="657e1-118">Nella pagina **Aggiornamenti binari** seleziona **Salva pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="657e1-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="657e1-119">Nella pagina **Esamina e salva aggiornamenti** seleziona **Salva pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="657e1-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="657e1-120">Nel riquadro **Salva pacchetto nella raccolta cespiti** che si apre, immetti il nome del pacchetto e quindi seleziona **Salva pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="657e1-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="657e1-121">Quando LCS ha terminato di salvare il pacchetto, il pulsate **Fatto** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="657e1-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="657e1-122">Seleziona **Fatto**.</span><span class="sxs-lookup"><span data-stu-id="657e1-122">Select **Done**.</span></span> <span data-ttu-id="657e1-123">LCS verificherà il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="657e1-123">LCS will verify the package.</span></span> <span data-ttu-id="657e1-124">La verifica può richiedere alcuni minuti o fino a un'ora.</span><span class="sxs-lookup"><span data-stu-id="657e1-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="657e1-125">Applicare l'aggiornamento del pacchetto</span><span class="sxs-lookup"><span data-stu-id="657e1-125">Apply the package update</span></span>

1. <span data-ttu-id="657e1-126">In LCS, sulla pagina **Dettagli ambiente** seleziona **Gestisci** > **Applica aggiornamenti**.</span><span class="sxs-lookup"><span data-stu-id="657e1-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="657e1-127">Dall'elenco, seleziona il pacchetto che hai salvato in precedenza, quindi seleziona **Applica**.</span><span class="sxs-lookup"><span data-stu-id="657e1-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="657e1-128">Seleziona **Sì** per confermare che desideri distribuire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="657e1-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Finestra di dialogo Conferma distribuzione del pacchetto](media/confirm-package-deployment.png)

4. <span data-ttu-id="657e1-130">Seleziona **Sì** per confermare che desideri aggiornare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="657e1-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Finestra di dialogo Conferma aggiornamento dell'applicazione](media/confirm-application-update.png)

<span data-ttu-id="657e1-132">La distribuzione e l'aggiornamento dell'applicazione verranno avviati.</span><span class="sxs-lookup"><span data-stu-id="657e1-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="657e1-133">Sulla pagina **Dettagli ambiente** nell'angolo in alto a destra, lo stato dell'ambiente verrà aggiornato su **Manutenzione**.</span><span class="sxs-lookup"><span data-stu-id="657e1-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="657e1-134">In circa due ore l'aggiornamento sarà completo.</span><span class="sxs-lookup"><span data-stu-id="657e1-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="657e1-135">Le informazioni sulla versione dell'applicazione verranno aggiornate su **Microsoft Dynamics 365 for Finance and Operations 10.0.15** e lo stato dell'ambiente verrà aggiornato su **Distribuito**.</span><span class="sxs-lookup"><span data-stu-id="657e1-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="657e1-136">Aggiornare l'ambiente Dataverse</span><span class="sxs-lookup"><span data-stu-id="657e1-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="657e1-137">Accedi all'[interfaccia di amministrazione di Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="657e1-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="657e1-138">Nell'elenco, trova e apri l'ambiente che hai utilizzato per installare Project Operations.</span><span class="sxs-lookup"><span data-stu-id="657e1-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="657e1-139">Sulla pagina **Ambienti** seleziona **Risorsa** > **App Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="657e1-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="657e1-140">Nell'elenco, individua **Microsoft Dynamics 365 Project Operations** e nella colonna **Stato** seleziona **Aggiornamento disponibile**.</span><span class="sxs-lookup"><span data-stu-id="657e1-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="657e1-141">Seleziona la casella di controllo **Accetto le condizioni d'uso**, quindi seleziona **Aggiorna**.</span><span class="sxs-lookup"><span data-stu-id="657e1-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="657e1-142">L'ultima versione della soluzione verrà installata.</span><span class="sxs-lookup"><span data-stu-id="657e1-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="657e1-143">Al termine dell'installazione, avrai la versione 4.5.0.134 installata.</span><span class="sxs-lookup"><span data-stu-id="657e1-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="657e1-144">Configurare le nuove funzionalità</span><span class="sxs-lookup"><span data-stu-id="657e1-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="657e1-145">Abilitare il mapping doppia scrittura</span><span class="sxs-lookup"><span data-stu-id="657e1-145">Enable dual-write mapping</span></span>

<span data-ttu-id="657e1-146">Dopo aver completato l'aggiornamento degli ambienti Finance e Dataverse puoi abilitare i mapping a doppia scrittura richiesti.</span><span class="sxs-lookup"><span data-stu-id="657e1-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="657e1-147">Completa le seguenti procedure per abilitare i mapping a doppia scrittura.</span><span class="sxs-lookup"><span data-stu-id="657e1-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="657e1-148">Aggiornare le impostazioni di sicurezza nell'ambiente Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="657e1-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="657e1-149">Aggiornare le entità di dati</span><span class="sxs-lookup"><span data-stu-id="657e1-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="657e1-150">Aggiornare ed eseguire i mapping a doppia scrittura</span><span class="sxs-lookup"><span data-stu-id="657e1-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="657e1-151">Aggiornare le impostazioni di sicurezza nell'ambiente Dataverse</span><span class="sxs-lookup"><span data-stu-id="657e1-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="657e1-152">I seguenti aggiornamenti ai privilegi di sicurezza per le entità sono richiesti come parte dell'aggiornamento a UR5.</span><span class="sxs-lookup"><span data-stu-id="657e1-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="657e1-153">Nell'ambiente Dataverse vai a **Impostazioni** e nel gruppo **Sistema** seleziona **Sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="657e1-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Impostazioni dell'ambiente Dataverse](media/Picture21.png)

2. <span data-ttu-id="657e1-155">Seleziona **Ruoli di sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="657e1-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="657e1-156">Seleziona **utente app a doppia scrittura** e seleziona la scheda **Entità personalizzate**.</span><span class="sxs-lookup"><span data-stu-id="657e1-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="657e1-157">Verifica che il ruolo abbia le autorizzazioni **Lettura** e **Aggiungi a** per:</span><span class="sxs-lookup"><span data-stu-id="657e1-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="657e1-158">**Tipo di tasso di cambio valuta**</span><span class="sxs-lookup"><span data-stu-id="657e1-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="657e1-159">**Piano dei conti**</span><span class="sxs-lookup"><span data-stu-id="657e1-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="657e1-160">**Calendario fiscale**</span><span class="sxs-lookup"><span data-stu-id="657e1-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="657e1-161">**Libro mastro**</span><span class="sxs-lookup"><span data-stu-id="657e1-161">**Ledger**</span></span>

5. <span data-ttu-id="657e1-162">Dopo aver aggiornato ruolo di sicurezza, vai a **Impostazioni** > **Sicurezza** > **Team**.</span><span class="sxs-lookup"><span data-stu-id="657e1-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="657e1-163">Verifica che il ruolo **utente app a doppia scrittura** sia stato applicato al team.</span><span class="sxs-lookup"><span data-stu-id="657e1-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="657e1-164">Aggiornare le entità di dati dall'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="657e1-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="657e1-165">Nel tuo ambiente Finance, apri l'area di lavoro **Gestione dati**, quindi apri la pagina **Parametri framework**.</span><span class="sxs-lookup"><span data-stu-id="657e1-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="657e1-166">Sulla scheda **Impostazioni entità** seleziona **Aggiorna elenco entità**.</span><span class="sxs-lookup"><span data-stu-id="657e1-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="657e1-167">Seleziona **Chiudi** per confermare l'aggiornamento dell'entità.</span><span class="sxs-lookup"><span data-stu-id="657e1-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="657e1-168">Questo processo richiederà circa 20 minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="657e1-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="657e1-169">Riceverai una notifica quando l'aggiornamento è completo.</span><span class="sxs-lookup"><span data-stu-id="657e1-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="657e1-170">Aggiornare i mapping doppia scrittura</span><span class="sxs-lookup"><span data-stu-id="657e1-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="657e1-171">Nell'area di lavoro **Gestione dati** seleziona **Doppia scrittura**.</span><span class="sxs-lookup"><span data-stu-id="657e1-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="657e1-172">Seleziona **Applicare soluzioni**, seleziona entrambe le soluzioni nell'elenco, quindi seleziona **Applica**.</span><span class="sxs-lookup"><span data-stu-id="657e1-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="657e1-173">Sulla pagina **Doppia scrittura** seleziona le seguenti mappe tabella, quindi seleziona **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="657e1-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="657e1-174">**Valori effettivi dell'integrazione di Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="657e1-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="657e1-175">**Categorie di spesa del progetto di integrazione di Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="657e1-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="657e1-176">**Entità di esportazione delle spese di progetto effettive di integrazione di Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="657e1-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="657e1-177">Sulla pagina **Versione del mapping di tabella**, applica una nuova versione della mappa a ciascuna delle tre entità.</span><span class="sxs-lookup"><span data-stu-id="657e1-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="657e1-178">Sulla pagina **Doppia scrittura** seleziona Esegui per riavviare i mapping.</span><span class="sxs-lookup"><span data-stu-id="657e1-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="657e1-179">Dall'elenco dei mapping, seleziona il mapping **Libro mastro (msdyn_ledgers)** con tutti i prerequisiti e seleziona la casella di controllo **Sincronizzazione iniziale**.</span><span class="sxs-lookup"><span data-stu-id="657e1-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="657e1-180">Nel campo **Master per la sincronizzazione iniziale** seleziona **App Finance and Operations** e poi seleziona **Esegui**.</span><span class="sxs-lookup"><span data-stu-id="657e1-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sincronizzazione dei mapping del libro mastro](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]