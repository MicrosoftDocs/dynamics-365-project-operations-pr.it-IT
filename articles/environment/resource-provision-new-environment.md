---
title: Effettuare il provisioning di un nuovo ambiente
description: Questo argomento fornisce informazioni su come effettuare il provisioning di un nuovo ambiente Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949367"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="5ddc7-103">Effettuare il provisioning di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="5ddc7-103">Provision a new environment</span></span>

<span data-ttu-id="5ddc7-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="5ddc7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5ddc7-105">Questo argomento fornisce informazioni su come effettuare il provisioning di un nuovo ambiente Dynamics 365 Project Operations per scenari basati su risorse/non stoccate.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="5ddc7-106">Abilitare il provisioning automatizzato di Project Operations in un progetto LCS</span><span class="sxs-lookup"><span data-stu-id="5ddc7-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="5ddc7-107">Utilizza i passaggi seguenti per abilitare il flusso di provisioning automatizzato di Project Operations per il progetto LCS.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="5ddc7-108">Vai a [LCS](https://lcs.dynamics.com/v2) e seleziona il riquadro **Gestione funzionalità di anteprima**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="5ddc7-109">Nell'elenco **Funzionalità di anteprima** seleziona **Project Operations**, quindi seleziona **Funzionalità di anteprima abilitata** per abilitare Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="5ddc7-110">Questo passaggio viene eseguito solo una volta per progetto LCS.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="5ddc7-111">Effettuare il provisioning di un ambiente Project Operations</span><span class="sxs-lookup"><span data-stu-id="5ddc7-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="5ddc7-112">Apri una nuova distribuzione di [ambiente demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [ambiente di produzione/sandbox](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) di Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="5ddc7-113">Segui la procedura guidata **Provisioning ambiente**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="5ddc7-114">Assicurati che la versione dell'applicazione selezionata sia 10.0.13 o successiva.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="5ddc7-115">Per effettuare il provisioning di Project Operations, in **Impostazioni avanzate** seleziona **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="5ddc7-116">Abilita l'**Impostazione Common Data Service** selezionando **Sì** e quindi inserisci le informazioni nei campi obbligatori:</span><span class="sxs-lookup"><span data-stu-id="5ddc7-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="5ddc7-117">Nome</span><span class="sxs-lookup"><span data-stu-id="5ddc7-117">Name</span></span>
  - <span data-ttu-id="5ddc7-118">Area geografica</span><span class="sxs-lookup"><span data-stu-id="5ddc7-118">Region</span></span>
  - <span data-ttu-id="5ddc7-119">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="5ddc7-119">Language</span></span>
  - <span data-ttu-id="5ddc7-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="5ddc7-120">Currency</span></span>
 
5. <span data-ttu-id="5ddc7-121">Nel campo **Modello Common Data Service**, seleziona **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="5ddc7-122">Seleziona il tipo di ambiente per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="5ddc7-123">Una versione di valutazione basata su abbonamento ti consentirà di distribuire un ambiente CDS per 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Impostazioni di distribuzione](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="5ddc7-125">Seleziona **Accetto** per accettare le condizioni d'uso e quindi seleziona **Fatto** per tornare alle impostazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consenso distribuzione](./media/2DeploymentConsent.png)

7. <span data-ttu-id="5ddc7-127">Completa i restanti campi obbligatori nella procedura guidata e conferma la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="5ddc7-128">Il tempo di provisioning dell'ambiente varia in base al tipo di ambiente.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="5ddc7-129">Il provisioning potrebbe richiedere fino a sei ore.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="5ddc7-130">Dopo il completamento della distribuzione, l'ambiente verrà visualizzato come **Distribuito**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="5ddc7-131">Per confermare che l'ambiente è stato distribuito correttamente, seleziona **Accedi** e accedi all'ambiente per confermare.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Dettagli degli ambienti ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="5ddc7-133">Applicare i dati dimostrativi di Project Operations Finance (passaggio facoltativo)</span><span class="sxs-lookup"><span data-stu-id="5ddc7-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="5ddc7-134">Applica i dati dimostrativi di Project Operations Finance all'ambiente ospitato su cloud versione del servizio 10.0.13 come descritto in [questo articolo](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="5ddc7-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="5ddc7-135">Applicare gli aggiornamenti all'ambiente Finance</span><span class="sxs-lookup"><span data-stu-id="5ddc7-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="5ddc7-136">Project Operations richiede un ambiente Finance con la versione dell'applicazione **10.0.13 (10.0.569.20009)** o superiore.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="5ddc7-137">Potrebbe essere necessario applicare aggiornamenti di qualità all'ambiente Finance per ricevere questa versione.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="5ddc7-138">In LCS, nella pagina **Dettagli ambiente**, nella sezione **Aggiornamenti disponibili**, seleziona **Visualizza aggiornamento**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Visualizzare gli aggiornamenti](./media/5ViewUpdates.png)

2. <span data-ttu-id="5ddc7-140">Nella pagina **Aggiornamenti binari**, seleziona **Salva pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-140">On the **Binary updates** page, select **Save package.**</span></span>

![Salvare il pacchetto](./media/6SavePackage.png)

3. <span data-ttu-id="5ddc7-142">Fai clic su **Seleziona tutto** e quindi seleziona **Salva pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-142">Click **Select all** and then select **Save package**.</span></span>

![Verificare e salvare gli aggiornamenti](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="5ddc7-144">Immetti un nome e una descrizione del pacchetto, quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="5ddc7-145">A seconda della connessione Internet, questo processo potrebbe richiedere del tempo.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-145">Depending on the internet connection, this process might take some time.</span></span>

![Caricare il pacchetto nella raccolta di risorse](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="5ddc7-147">Dopo aver salvato il pacchetto, seleziona **Fatto** e salva questo pacchetto nella raccolta di risorse nel progetto LCS.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="5ddc7-148">Il salvataggio e la convalida del pacchetto potrebbero richiedere circa 15 minuti.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="5ddc7-149">Per applicare l'aggiornamento, passa alla pagina **Dettagli ambiente** in LCS e seleziona **Gestisci** > **Applica aggiornamenti**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Gestire gli ambienti](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="5ddc7-151">Nell'elenco degli aggiornamenti seleziona il pacchetto che hai creato e seleziona **Applica**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Applicare gli aggiornamenti](./media/10ApplyUpdates.png)

<span data-ttu-id="5ddc7-153">La manutenzione dell'ambiente richiederà del tempo.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-153">Environment servicing will take some time.</span></span> <span data-ttu-id="5ddc7-154">Al termine, l'ambiente tornerà a uno stato distribuito.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ambiente distribuito](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="5ddc7-156">Stabilire una connessione a Doppia scrittura</span><span class="sxs-lookup"><span data-stu-id="5ddc7-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="5ddc7-157">Nel progetto LCS, vai alla pagina **Dettagli ambiente**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="5ddc7-158">In **Informazioni sull'ambiente Common Data Service**, seleziona **Collega a CDS per app**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="5ddc7-159">Dopo aver completato il collegamento, seleziona di nuovo **Collega a CDS per app**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="5ddc7-160">Verrai reindirizzato a Doppia scrittura in Finance.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-160">You will be redirected to Dual Write in Finance.</span></span>

![Collegamento a CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="5ddc7-162">Seleziona **Applica soluzione** per accedere alle entità che verranno mappate nell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Applica soluzioni](./media/13ApplySolutions.png)

5. <span data-ttu-id="5ddc7-164">Seleziona entrambe le soluzioni, **Mapping entità doppia scrittura Dynamics 365 Finance and Operations** e **Mapping entità doppia scrittura Dynamics 365 Project Operations**, quindi seleziona **Applica**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confermare le soluzioni](./media/14ConfirmSolutions.png)

<span data-ttu-id="5ddc7-166">Dopo aver applicato le soluzioni, le entità doppia scrittura vengono applicate all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Applicazione delle soluzioni](./media/15ApplyingSolutions.png)

<span data-ttu-id="5ddc7-168">Dopo l'applicazione delle entità, tutti i mapping disponibili vengono elencati nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapping doppia scrittura](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="5ddc7-170">Aggiornare le entità di dati dopo l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5ddc7-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="5ddc7-171">In Finance, vai all'area di lavoro **Gestione dati**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-171">In Finance, go to the **Data management** workspace.</span></span>

![Area di lavoro Gestione dati](./media/16DataManagement.png)

2. <span data-ttu-id="5ddc7-173">Seleziona il riquadro **Parametri framework**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-173">Select the **Framework parameters** tile.</span></span>

![Parametri framework](./media/17FrameworkParameters.png)

3. <span data-ttu-id="5ddc7-175">Nella pagina **Impostazioni entità**, seleziona **Aggiorna elenco di entità**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Aggiornare l'elenco di entità](./media/18RefreshEntityList.png)

<span data-ttu-id="5ddc7-177">L'aggiornamento richiederà circa 20 minuti.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="5ddc7-178">Riceverai un avviso quando sarà completo.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-178">You will receive an alert when it is complete.</span></span>

![Conferma dell'aggiornamento](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="5ddc7-180">Eseguire il mapping doppia scrittura di Project Operations</span><span class="sxs-lookup"><span data-stu-id="5ddc7-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="5ddc7-181">Nel progetto LCS, vai alla pagina **Dettagli ambiente**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="5ddc7-182">In **Informazioni sull'ambiente Common Data Service**, seleziona **Collega a CDS per app**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="5ddc7-183">Dopo aver selezionato il collegamento, verrai reindirizzato all'elenco delle entità nei mapping.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="5ddc7-184">Avvia il mapping come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="5ddc7-185">Assicurati di seguire la sequenza elencata.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="5ddc7-186">**Mapping entità**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-186">**Entity Map**</span></span> | <span data-ttu-id="5ddc7-187">**Aggiorna entità**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-187">**Refresh entity**</span></span> | <span data-ttu-id="5ddc7-188">**Sincronizzazione iniziale**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-188">**Initial sync**</span></span> | <span data-ttu-id="5ddc7-189">**Master per la sincronizzazione iniziale**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-189">**Master for initial sync**</span></span> | <span data-ttu-id="5ddc7-190">**Esegui prerequisiti**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-190">**Run prerequisites**</span></span> | <span data-ttu-id="5ddc7-191">**Sincronizzazione iniziale prerequisiti**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="5ddc7-192">**Ruoli delle risorse di progetto per tutte le aziende (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="5ddc7-193">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-193">No</span></span> | <span data-ttu-id="5ddc7-194">Sì</span><span class="sxs-lookup"><span data-stu-id="5ddc7-194">Yes</span></span> | <span data-ttu-id="5ddc7-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5ddc7-195">Common Data Service</span></span> | <span data-ttu-id="5ddc7-196">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-196">No</span></span> | <span data-ttu-id="5ddc7-197">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-197">N\A</span></span> |
| <span data-ttu-id="5ddc7-198">**Persone giuridiche (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="5ddc7-199">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-199">No</span></span> | <span data-ttu-id="5ddc7-200">Sì</span><span class="sxs-lookup"><span data-stu-id="5ddc7-200">Yes</span></span> | <span data-ttu-id="5ddc7-201">App Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5ddc7-201">Finance and Operations apps</span></span> | <span data-ttu-id="5ddc7-202">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-202">No</span></span> | <span data-ttu-id="5ddc7-203">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-203">N\A</span></span> |
| <span data-ttu-id="5ddc7-204">**Valori effettivi dell'integrazione di Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="5ddc7-205">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-205">No</span></span> | <span data-ttu-id="5ddc7-206">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-206">No</span></span> | <span data-ttu-id="5ddc7-207">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-207">N\A</span></span> | <span data-ttu-id="5ddc7-208">Sì</span><span class="sxs-lookup"><span data-stu-id="5ddc7-208">Yes</span></span> | <span data-ttu-id="5ddc7-209">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-209">No</span></span> |
| <span data-ttu-id="5ddc7-210">**Voci del contratto di progetto (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="5ddc7-211">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-211">No</span></span> | <span data-ttu-id="5ddc7-212">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-212">No</span></span> | <span data-ttu-id="5ddc7-213">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-213">N\A</span></span> | <span data-ttu-id="5ddc7-214">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-214">No</span></span> | <span data-ttu-id="5ddc7-215">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-215">No</span></span> |
| <span data-ttu-id="5ddc7-216">**Entità di integrazione per le relazioni di transazione del progetto (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="5ddc7-217">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-217">No</span></span> | <span data-ttu-id="5ddc7-218">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-218">No</span></span> | <span data-ttu-id="5ddc7-219">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-219">N\A</span></span> | <span data-ttu-id="5ddc7-220">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-220">No</span></span> | <span data-ttu-id="5ddc7-221">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-221">N\A</span></span> |
| <span data-ttu-id="5ddc7-222">**Passaggi fondamentali della voce di contratto dell'integrazione di Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="5ddc7-223">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-223">No</span></span> | <span data-ttu-id="5ddc7-224">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-224">No</span></span> | <span data-ttu-id="5ddc7-225">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-225">N\A</span></span> | <span data-ttu-id="5ddc7-226">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-226">No</span></span> | <span data-ttu-id="5ddc7-227">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-227">N\A</span></span> |
| <span data-ttu-id="5ddc7-228">**Entità di integrazione di Project Operations per le stime di spesa (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="5ddc7-229">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-229">No</span></span> | <span data-ttu-id="5ddc7-230">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-230">No</span></span> | <span data-ttu-id="5ddc7-231">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-231">N\A</span></span> | <span data-ttu-id="5ddc7-232">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-232">No</span></span> | <span data-ttu-id="5ddc7-233">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-233">N\A</span></span> |
| <span data-ttu-id="5ddc7-234">**Entità di integrazione di Project Operations per le stime delle ore (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="5ddc7-235">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-235">No</span></span> | <span data-ttu-id="5ddc7-236">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-236">No</span></span> | <span data-ttu-id="5ddc7-237">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-237">N\A</span></span> | <span data-ttu-id="5ddc7-238">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-238">No</span></span> | <span data-ttu-id="5ddc7-239">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-239">N\A</span></span> |
| <span data-ttu-id="5ddc7-240">**Entità di esportazione delle spese di progetto di integrazione di Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="5ddc7-241">Sì</span><span class="sxs-lookup"><span data-stu-id="5ddc7-241">Yes</span></span> | <span data-ttu-id="5ddc7-242">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-242">No</span></span> | <span data-ttu-id="5ddc7-243">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-243">N\A</span></span> | <span data-ttu-id="5ddc7-244">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-244">No</span></span> | <span data-ttu-id="5ddc7-245">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-245">N\A</span></span> |
| <span data-ttu-id="5ddc7-246">**Entità di integrazione di Project Operations per le stime delle ore (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="5ddc7-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="5ddc7-247">Sì</span><span class="sxs-lookup"><span data-stu-id="5ddc7-247">Yes</span></span> | <span data-ttu-id="5ddc7-248">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-248">No</span></span> | <span data-ttu-id="5ddc7-249">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-249">N\A</span></span> | <span data-ttu-id="5ddc7-250">No</span><span class="sxs-lookup"><span data-stu-id="5ddc7-250">No</span></span> | <span data-ttu-id="5ddc7-251">N/A</span><span class="sxs-lookup"><span data-stu-id="5ddc7-251">N\A</span></span> |

4. <span data-ttu-id="5ddc7-252">Per aggiornare l'entità, seleziona il nome del mapping, quindi seleziona **Aggiorna entità**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="5ddc7-253">Procedi con l'esecuzione del mapping al termine dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-253">Proceed with running the map after the refresh is complete.</span></span>

![Aggiornare il mapping](./media/20RefreshMapping.png)

<span data-ttu-id="5ddc7-255">Prima di abilitare il mapping successivo, verificare che il mapping nella tabella sia in uno stato **In esecuzione**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="5ddc7-256">L'esecuzione di mapping con un numero maggiore di prerequisiti potrebbe richiedere del tempo.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="5ddc7-257">Per eseguire un mapping con prerequisiti, abilita l'interruttore **Mostra mapping entità correlate**.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="5ddc7-258">Se la tabella indica che **Sincronizzazione iniziale prerequisiti** è **No**, verifica che il contrassegno **Sincronizzazione iniziale** sia **Disattivato** in tutti i mapping di prerequisiti prima di eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Eseguire il mapping](./media/21RunMap.png)

6. <span data-ttu-id="5ddc7-260">Conferma che tutti i mapping relativi al progetto siano in stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-260">Validate all project related maps are in the running state.</span></span>

![Tutti i mapping in esecuzione](./media/22AllMapsRunning.png)

<span data-ttu-id="5ddc7-262">Il provisioning e la configurazione dell'ambiente Project Operations sono stati ora completati.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-262">Your Project Operations environment is now provisioned and configured.</span></span>
