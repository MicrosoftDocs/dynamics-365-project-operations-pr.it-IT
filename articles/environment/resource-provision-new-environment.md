---
title: Effettuare il provisioning di un nuovo ambiente
description: Questo argomento fornisce informazioni su come effettuare il provisioning di un nuovo ambiente Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950539"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="5dae1-103">Effettuare il provisioning di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="5dae1-103">Provision a new environment</span></span>

<span data-ttu-id="5dae1-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="5dae1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5dae1-105">Questo argomento fornisce informazioni su come eseguire il provisioning di un nuovo ambiente Dynamics 365 Project Operations per scenari basati risorse/materiali non stoccati.</span><span class="sxs-lookup"><span data-stu-id="5dae1-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="5dae1-106">Abilitare il provisioning automatizzato di Project Operations in un progetto LCS</span><span class="sxs-lookup"><span data-stu-id="5dae1-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="5dae1-107">Utilizza i passaggi seguenti per abilitare il flusso di provisioning automatizzato di Project Operations per il progetto LCS.</span><span class="sxs-lookup"><span data-stu-id="5dae1-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="5dae1-108">Vai a [LCS](https://lcs.dynamics.com/v2) e seleziona il riquadro **Gestione funzionalità di anteprima**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="5dae1-109">Nell'elenco **Funzionalità di anteprima** seleziona **Funzionalità Project Operations**, quindi seleziona **Funzionalità di anteprima abilitata** per abilitare Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5dae1-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="5dae1-110">Questo passaggio viene eseguito solo una volta per progetto LCS.</span><span class="sxs-lookup"><span data-stu-id="5dae1-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="5dae1-111">Effettuare il provisioning di un ambiente Project Operations</span><span class="sxs-lookup"><span data-stu-id="5dae1-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="5dae1-112">Apri una nuova distribuzione di [ambiente demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [ambiente di produzione/sandbox](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) di Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="5dae1-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="5dae1-113">Segui la procedura guidata **Provisioning ambiente**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="5dae1-114">Assicurati che la versione dell'applicazione selezionata sia 10.0.13 o successiva.</span><span class="sxs-lookup"><span data-stu-id="5dae1-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="5dae1-115">Per effettuare il provisioning di Project Operations, in **Impostazioni avanzate** seleziona **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="5dae1-116">Abilita l'**Impostazione Common Data Service** selezionando **Sì** e quindi inserisci le informazioni nei campi obbligatori:</span><span class="sxs-lookup"><span data-stu-id="5dae1-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="5dae1-117">Nome</span><span class="sxs-lookup"><span data-stu-id="5dae1-117">Name</span></span>
  - <span data-ttu-id="5dae1-118">Area geografica</span><span class="sxs-lookup"><span data-stu-id="5dae1-118">Region</span></span>
  - <span data-ttu-id="5dae1-119">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="5dae1-119">Language</span></span>
  - <span data-ttu-id="5dae1-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="5dae1-120">Currency</span></span>
 
5. <span data-ttu-id="5dae1-121">Nel campo **Modello Common Data Service**, seleziona **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="5dae1-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="5dae1-122">Seleziona il tipo di ambiente per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5dae1-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="5dae1-123">Una versione di valutazione basata su abbonamento ti consentirà di distribuire un ambiente CDS per 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="5dae1-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Impostazioni di distribuzione](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="5dae1-125">Seleziona **Accetto** per accettare le condizioni d'uso e quindi seleziona **Fatto** per tornare alle impostazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5dae1-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consenso distribuzione](./media/2DeploymentConsent.png)

7. <span data-ttu-id="5dae1-127">Facoltativo: applica i dati demo all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="5dae1-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="5dae1-128">Vai a **Impostazioni avanzate** seleziona **Personalizza configurazione database SQL** e imposta **Specificare un set di dati per il database dell'applicazione** su **Demo**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="5dae1-129">Completa i restanti campi obbligatori nella procedura guidata e conferma la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5dae1-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="5dae1-130">Il tempo per il provisioning dell'ambiente varia in base al tipo di ambiente.</span><span class="sxs-lookup"><span data-stu-id="5dae1-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="5dae1-131">Il provisioning potrebbe richiedere fino a sei ore.</span><span class="sxs-lookup"><span data-stu-id="5dae1-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="5dae1-132">Dopo il completamento della distribuzione, l'ambiente verrà visualizzato come **Distribuito**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="5dae1-133">Per confermare che l'ambiente è stato distribuito correttamente, seleziona **Accesso** e accedi all'ambiente per confermare.</span><span class="sxs-lookup"><span data-stu-id="5dae1-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Dettagli degli ambienti ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="5dae1-135">Applicare gli aggiornamenti all'ambiente Finance</span><span class="sxs-lookup"><span data-stu-id="5dae1-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="5dae1-136">Project Operations richiede un ambiente Finance con la versione dell'applicazione **10.0.13 (10.0.569.20009)** o superiore.</span><span class="sxs-lookup"><span data-stu-id="5dae1-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="5dae1-137">Potrebbe essere necessario applicare aggiornamenti di qualità all'ambiente Finance per ricevere questa versione.</span><span class="sxs-lookup"><span data-stu-id="5dae1-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="5dae1-138">In LCS, nella pagina **Dettagli ambiente**, nella sezione **Aggiornamenti disponibili**, seleziona **Visualizza aggiornamento**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Visualizzare gli aggiornamenti](./media/5ViewUpdates.png)

2. <span data-ttu-id="5dae1-140">Nella pagina **Aggiornamenti binari**, seleziona **Salva pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-140">On the **Binary updates** page, select **Save package.**</span></span>

![Salvare il pacchetto](./media/6SavePackage.png)

3. <span data-ttu-id="5dae1-142">Fai clic su **Seleziona tutto** e quindi seleziona **Salva pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-142">Click **Select all** and then select **Save package**.</span></span>

![Verificare e salvare gli aggiornamenti](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="5dae1-144">Immetti un nome e una descrizione del pacchetto, quindi seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="5dae1-145">A seconda della connessione Internet, questo processo potrebbe richiedere del tempo.</span><span class="sxs-lookup"><span data-stu-id="5dae1-145">Depending on the internet connection, this process might take some time.</span></span>

![Caricare il pacchetto nella raccolta di risorse](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="5dae1-147">Dopo aver salvato il pacchetto, seleziona **Fatto** e salva questo pacchetto nella raccolta di risorse nel progetto LCS.</span><span class="sxs-lookup"><span data-stu-id="5dae1-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="5dae1-148">Il salvataggio e la convalida del pacchetto potrebbero richiedere circa 15 minuti.</span><span class="sxs-lookup"><span data-stu-id="5dae1-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="5dae1-149">Per applicare l'aggiornamento, passa alla pagina **Dettagli ambiente** in LCS e seleziona **Gestisci** > **Applica aggiornamenti**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Gestire gli ambienti](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="5dae1-151">Nell'elenco degli aggiornamenti seleziona il pacchetto che hai creato e seleziona **Applica**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Applicare gli aggiornamenti](./media/10ApplyUpdates.png)

<span data-ttu-id="5dae1-153">La manutenzione dell'ambiente richiederà del tempo.</span><span class="sxs-lookup"><span data-stu-id="5dae1-153">Environment servicing will take some time.</span></span> <span data-ttu-id="5dae1-154">Al termine, l'ambiente tornerà a uno stato distribuito.</span><span class="sxs-lookup"><span data-stu-id="5dae1-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ambiente distribuito](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="5dae1-156">Stabilire una connessione a Doppia scrittura</span><span class="sxs-lookup"><span data-stu-id="5dae1-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="5dae1-157">Nel progetto LCS, vai alla pagina **Dettagli ambiente**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="5dae1-158">In **Informazioni sull'ambiente Common Data Service**, seleziona **Collega a CDS per app**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="5dae1-159">Dopo aver completato il collegamento, seleziona di nuovo **Collega a CDS per app**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="5dae1-160">Verrai reindirizzato a Doppia scrittura in Finance.</span><span class="sxs-lookup"><span data-stu-id="5dae1-160">You will be redirected to Dual Write in Finance.</span></span>

![Collegamento a CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="5dae1-162">Seleziona **Applica soluzione** per accedere alle entità che verranno mappate nell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dae1-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Applica soluzioni](./media/13ApplySolutions.png)

5. <span data-ttu-id="5dae1-164">Seleziona entrambe le soluzioni, **Dynamics 365 Finance and Operations Dual Write Entity Map** e **Dynamics 365 Project Operations Dual Write Entity Maps** e quindi seleziona **Applica**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confermare le soluzioni](./media/14ConfirmSolutions.png)

<span data-ttu-id="5dae1-166">Dopo aver applicato le soluzioni, le entità doppia scrittura vengono applicate all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="5dae1-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Applicazione delle soluzioni](./media/15ApplyingSolutions.png)

<span data-ttu-id="5dae1-168">Dopo l'applicazione delle entità, tutti i mapping disponibili vengono elencati nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="5dae1-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapping doppia scrittura](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="5dae1-170">Aggiornare le entità di dati dopo l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5dae1-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="5dae1-171">In Finance, vai all'area di lavoro **Gestione dati**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-171">In Finance, go to the **Data management** workspace.</span></span>

![Area di lavoro Gestione dati](./media/16DataManagement.png)

2. <span data-ttu-id="5dae1-173">Seleziona il riquadro **Parametri framework**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-173">Select the **Framework parameters** tile.</span></span>

![Parametri framework](./media/17FrameworkParameters.png)

3. <span data-ttu-id="5dae1-175">Nella pagina **Impostazioni entità**, seleziona **Aggiorna elenco di entità**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Aggiornare l'elenco di entità](./media/18RefreshEntityList.png)

<span data-ttu-id="5dae1-177">L'aggiornamento richiederà circa 20 minuti.</span><span class="sxs-lookup"><span data-stu-id="5dae1-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="5dae1-178">Riceverai un avviso quando sarà completo.</span><span class="sxs-lookup"><span data-stu-id="5dae1-178">You will receive an alert when it is complete.</span></span>

![Conferma dell'aggiornamento](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="5dae1-180">Aggiornare le impostazioni di sicurezza su Project Operations su Dataverse</span><span class="sxs-lookup"><span data-stu-id="5dae1-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="5dae1-181">Vai Project Operations nell'ambiente Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5dae1-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="5dae1-182">Passa a **Impostazioni** > **Sicurezza** > **Ruoli di sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="5dae1-183">Nella pagina **Ruoli di sicurezza** nell'elenco dei ruoli, seleziona **utente app a doppia scrittura** e seleziona la scheda **Entità personalizzate**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="5dae1-184">Verifica che il ruolo abbia le autorizzazioni **Lettura** e **Aggiungi a** per:</span><span class="sxs-lookup"><span data-stu-id="5dae1-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="5dae1-185">**Tipo di tasso di cambio valuta**</span><span class="sxs-lookup"><span data-stu-id="5dae1-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="5dae1-186">**Piano dei conti**</span><span class="sxs-lookup"><span data-stu-id="5dae1-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="5dae1-187">**Calendario fiscale**</span><span class="sxs-lookup"><span data-stu-id="5dae1-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="5dae1-188">**Libro mastro**</span><span class="sxs-lookup"><span data-stu-id="5dae1-188">**Ledger**</span></span>

5. <span data-ttu-id="5dae1-189">Dopo aver aggiornato ruolo di sicurezza, vai a **Impostazioni** > **Sicurezza** > **Team** e seleziona il team predefinito nella visualizzazione team **Proprietario azienda locale**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="5dae1-190">Seleziona **Gestisci ruoli** e verifica che il privilegio di sicurezza **utente app a doppia scrittura** sia applicato a questo team.</span><span class="sxs-lookup"><span data-stu-id="5dae1-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="5dae1-191">Eseguire il mapping doppia scrittura di Project Operations</span><span class="sxs-lookup"><span data-stu-id="5dae1-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="5dae1-192">Nel progetto LCS, vai alla pagina **Dettagli ambiente**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="5dae1-193">In **Informazioni sull'ambiente Common Data Service**, seleziona **Collega a CDS per app**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="5dae1-194">Dopo aver selezionato il collegamento, verrai reindirizzato all'elenco delle entità nei mapping.</span><span class="sxs-lookup"><span data-stu-id="5dae1-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="5dae1-195">Avvia il mapping come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5dae1-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="5dae1-196">Assicurati di seguire la sequenza elencata.</span><span class="sxs-lookup"><span data-stu-id="5dae1-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="5dae1-197">**Mapping entità**</span><span class="sxs-lookup"><span data-stu-id="5dae1-197">**Entity Map**</span></span> | <span data-ttu-id="5dae1-198">**Aggiorna entità**</span><span class="sxs-lookup"><span data-stu-id="5dae1-198">**Refresh entity**</span></span> | <span data-ttu-id="5dae1-199">**Sincronizzazione iniziale**</span><span class="sxs-lookup"><span data-stu-id="5dae1-199">**Initial sync**</span></span> | <span data-ttu-id="5dae1-200">**Master per la sincronizzazione iniziale**</span><span class="sxs-lookup"><span data-stu-id="5dae1-200">**Master for initial sync**</span></span> | <span data-ttu-id="5dae1-201">**Esegui prerequisiti**</span><span class="sxs-lookup"><span data-stu-id="5dae1-201">**Run prerequisites**</span></span> | <span data-ttu-id="5dae1-202">**Sincronizzazione iniziale prerequisiti**</span><span class="sxs-lookup"><span data-stu-id="5dae1-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="5dae1-203">**Ruoli delle risorse di progetto per tutte le aziende (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="5dae1-204">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-204">No</span></span> | <span data-ttu-id="5dae1-205">Sì</span><span class="sxs-lookup"><span data-stu-id="5dae1-205">Yes</span></span> | <span data-ttu-id="5dae1-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5dae1-206">Common Data Service</span></span> | <span data-ttu-id="5dae1-207">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-207">No</span></span> | <span data-ttu-id="5dae1-208">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-208">N\A</span></span> |
| <span data-ttu-id="5dae1-209">**Persone giuridiche (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="5dae1-210">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-210">No</span></span> | <span data-ttu-id="5dae1-211">Sì</span><span class="sxs-lookup"><span data-stu-id="5dae1-211">Yes</span></span> | <span data-ttu-id="5dae1-212">App Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5dae1-212">Finance and Operations apps</span></span> | <span data-ttu-id="5dae1-213">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-213">No</span></span> | <span data-ttu-id="5dae1-214">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-214">N\A</span></span> |
| <span data-ttu-id="5dae1-215">**Libro mastro (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="5dae1-216">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-216">No</span></span> | <span data-ttu-id="5dae1-217">Sì</span><span class="sxs-lookup"><span data-stu-id="5dae1-217">Yes</span></span> | <span data-ttu-id="5dae1-218">App Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5dae1-218">Finance and Operations apps</span></span> | <span data-ttu-id="5dae1-219">Sì</span><span class="sxs-lookup"><span data-stu-id="5dae1-219">Yes</span></span> | <span data-ttu-id="5dae1-220">Sì, app Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5dae1-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="5dae1-221">**Valori effettivi dell'integrazione di Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="5dae1-222">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-222">No</span></span> | <span data-ttu-id="5dae1-223">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-223">No</span></span> | <span data-ttu-id="5dae1-224">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-224">N\A</span></span> | <span data-ttu-id="5dae1-225">Sì</span><span class="sxs-lookup"><span data-stu-id="5dae1-225">Yes</span></span> | <span data-ttu-id="5dae1-226">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-226">No</span></span> |
| <span data-ttu-id="5dae1-227">**Voci del contratto di progetto (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="5dae1-228">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-228">No</span></span> | <span data-ttu-id="5dae1-229">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-229">No</span></span> | <span data-ttu-id="5dae1-230">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-230">N\A</span></span> | <span data-ttu-id="5dae1-231">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-231">No</span></span> | <span data-ttu-id="5dae1-232">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-232">No</span></span> |
| <span data-ttu-id="5dae1-233">**Entità di integrazione per le relazioni di transazione del progetto (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="5dae1-234">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-234">No</span></span> | <span data-ttu-id="5dae1-235">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-235">No</span></span> | <span data-ttu-id="5dae1-236">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-236">N\A</span></span> | <span data-ttu-id="5dae1-237">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-237">No</span></span> | <span data-ttu-id="5dae1-238">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-238">N\A</span></span> |
| <span data-ttu-id="5dae1-239">**Passaggi fondamentali della voce di contratto dell'integrazione di Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="5dae1-240">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-240">No</span></span> | <span data-ttu-id="5dae1-241">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-241">No</span></span> | <span data-ttu-id="5dae1-242">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-242">N\A</span></span> | <span data-ttu-id="5dae1-243">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-243">No</span></span> | <span data-ttu-id="5dae1-244">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-244">N\A</span></span> |
| <span data-ttu-id="5dae1-245">**Entità di integrazione di Project Operations per le stime di spesa (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="5dae1-246">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-246">No</span></span> | <span data-ttu-id="5dae1-247">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-247">No</span></span> | <span data-ttu-id="5dae1-248">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-248">N\A</span></span> | <span data-ttu-id="5dae1-249">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-249">No</span></span> | <span data-ttu-id="5dae1-250">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-250">N\A</span></span> |
| <span data-ttu-id="5dae1-251">**Entità di esportazione categorie delle spese di progetto di integrazione di Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="5dae1-252">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-252">No</span></span> | <span data-ttu-id="5dae1-253">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-253">No</span></span> | <span data-ttu-id="5dae1-254">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-254">N\A</span></span> | <span data-ttu-id="5dae1-255">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-255">No</span></span> | <span data-ttu-id="5dae1-256">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-256">N\A</span></span> |
| <span data-ttu-id="5dae1-257">**Entità di esportazione delle spese di progetto di integrazione di Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="5dae1-258">Sì</span><span class="sxs-lookup"><span data-stu-id="5dae1-258">Yes</span></span> | <span data-ttu-id="5dae1-259">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-259">No</span></span> | <span data-ttu-id="5dae1-260">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-260">N\A</span></span> | <span data-ttu-id="5dae1-261">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-261">No</span></span> | <span data-ttu-id="5dae1-262">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-262">N\A</span></span> |
| <span data-ttu-id="5dae1-263">**Entità di integrazione di Project Operations per le stime delle ore (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="5dae1-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="5dae1-264">Sì</span><span class="sxs-lookup"><span data-stu-id="5dae1-264">Yes</span></span> | <span data-ttu-id="5dae1-265">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-265">No</span></span> | <span data-ttu-id="5dae1-266">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-266">N\A</span></span> | <span data-ttu-id="5dae1-267">No</span><span class="sxs-lookup"><span data-stu-id="5dae1-267">No</span></span> | <span data-ttu-id="5dae1-268">N/A</span><span class="sxs-lookup"><span data-stu-id="5dae1-268">N\A</span></span> |


4. <span data-ttu-id="5dae1-269">Per aggiornare l'entità, seleziona il nome del mapping, quindi seleziona **Aggiorna entità**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Aggiornare il mapping](./media/20RefreshMapping.png)

5. <span data-ttu-id="5dae1-271">Esegui il mapping al termine dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5dae1-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="5dae1-272">Prima di abilitare il mapping successivo, verificare che il mapping nella tabella sia in uno stato **In esecuzione**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="5dae1-273">L'esecuzione di mapping con un numero maggiore di prerequisiti potrebbe richiedere del tempo.</span><span class="sxs-lookup"><span data-stu-id="5dae1-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="5dae1-274">Per eseguire un mapping con prerequisiti, abilita l'interruttore **Mostra mapping entità correlate**.</span><span class="sxs-lookup"><span data-stu-id="5dae1-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="5dae1-275">Se la tabella indica che **Sincronizzazione iniziale prerequisiti** è **No**, verifica che il contrassegno **Sincronizzazione iniziale** sia **Disattivato** in tutti i mapping di prerequisiti prima di eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="5dae1-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Eseguire il mapping](./media/21RunMap.png)

6. <span data-ttu-id="5dae1-277">Conferma che tutti i mapping relativi al progetto siano in stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5dae1-277">Validate all project related maps are in the running state.</span></span>

![Tutti i mapping in esecuzione](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="5dae1-279">Applicare i dati di configurazione in CDS per Project Operations (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="5dae1-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="5dae1-280">Se hai applicato i dati demo all'ambiente Finance, vedi [Impostare e applicare i dati di configurazione in Common Data Service per Project Operations](resource-apply-pro-setup-config-data.md) per applicare i dati demo all'ambiente CDS.</span><span class="sxs-lookup"><span data-stu-id="5dae1-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="5dae1-281">Il provisioning e la configurazione dell'ambiente Project Operations sono stati ora completati.</span><span class="sxs-lookup"><span data-stu-id="5dae1-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]