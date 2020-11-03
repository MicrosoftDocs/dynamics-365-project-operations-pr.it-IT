---
title: Applicare i dati dimostrativi di Project Operations a un ambiente ospitato su cloud di Finance
description: Questo argomento spiega come applicare i dati dimostrativi da Project Operations a un ambiente ospitato su cloud di Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096627"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="2647e-103">Applicare i dati dimostrativi di Project Operations a un ambiente ospitato su cloud di Finance</span><span class="sxs-lookup"><span data-stu-id="2647e-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="2647e-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="2647e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2647e-105">Questo argomento si applica solo a Microsoft Dynamics 365 Finance versione 10.0.13 e può essere eseguito solo su un ambiente ospitato su cloud.</span><span class="sxs-lookup"><span data-stu-id="2647e-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="2647e-106">Completa i passaggi in questo argomento **PRIMA** di applicare aggiornamenti di qualità all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="2647e-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="2647e-107">Nel progetto LCS, apri la pagina **Dettagli ambiente**.</span><span class="sxs-lookup"><span data-stu-id="2647e-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="2647e-108">Questa include i dettagli necessari per connettersi all'ambiente utilizzando Remote Desktop Protocol (RDP).</span><span class="sxs-lookup"><span data-stu-id="2647e-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Dettagli degli ambienti ](./media/1EnvironmentDetails.png)

<span data-ttu-id="2647e-110">Il primo set di credenziali evidenziate sono le credenziali dell'account locale e contengono un collegamento ipertestuale alla connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="2647e-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="2647e-111">Le credenziali includono il nome utente e la password dell'amministratore dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="2647e-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="2647e-112">Il secondo set di credenziali viene utilizzato per accedere a SQL Server in questo ambiente.</span><span class="sxs-lookup"><span data-stu-id="2647e-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="2647e-113">Collegati in remoto all'ambiente tramite il collegamento ipertestuale in **Account locali** e utilizza le **Credenziali account locale** per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="2647e-113">Remote to the environment by the hyperlink in **Local Accounts** , and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="2647e-114">Vai a **Internet Information Services** > **Pool di applicazioni** > **AOSService** e arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="2647e-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="2647e-115">A questo punto arresta il servizio in modo da poter continuare a sostituire il database SQL.</span><span class="sxs-lookup"><span data-stu-id="2647e-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Arrestare AOS](./media/2StopAOS.png)

4. <span data-ttu-id="2647e-117">Vai a **Servizi** e arresta i seguenti due elementi:</span><span class="sxs-lookup"><span data-stu-id="2647e-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="2647e-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span><span class="sxs-lookup"><span data-stu-id="2647e-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="2647e-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span><span class="sxs-lookup"><span data-stu-id="2647e-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Arrestare i servizi](./media/3StopServices.png)

5. <span data-ttu-id="2647e-121">Apri Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="2647e-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="2647e-122">Accedi con le credenziali del server SQL e utilizza l'utente e la password di axdbadmin dalla pagina LCS **Dettagli ambienti**.</span><span class="sxs-lookup"><span data-stu-id="2647e-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="2647e-124">In Esplora oggetti, **Database** e individua **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="2647e-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="2647e-125">Sostituirai il database con un nuovo database che si trova nell'[Area download](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="2647e-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="2647e-126">Copia il file zip nella VM a cui sei collegato in remoto ed estrai il contenuto dello zip.</span><span class="sxs-lookup"><span data-stu-id="2647e-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="2647e-127">In SQL Server Management Studio, fai clic con il pulsante destro del mouse su **AxDB** e quindi seleziona **Attività** > **Ripristina** > **Database**.</span><span class="sxs-lookup"><span data-stu-id="2647e-127">In SQL Server Management Studio, right-click **AxDB** , and then select **Tasks** > **Restore** > **Database**.</span></span>

![Ripristina database](./media/5RestoreDatabase.png)

9. <span data-ttu-id="2647e-129">Seleziona **Dispositivo di origine** e vai al file estratto dallo zip che hai copiato.</span><span class="sxs-lookup"><span data-stu-id="2647e-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Dispositivi di origine](./media/6SourceDevice.png)

10. <span data-ttu-id="2647e-131">Seleziona **Opzioni** e quindi seleziona **Sovrascrivi database esistente** e **Chiudi connessioni esistenti al database di destinazione**.</span><span class="sxs-lookup"><span data-stu-id="2647e-131">Select **Options** , and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="2647e-132">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="2647e-132">Select **OK**.</span></span>

![Ripristinare le impostazioni](./media/7RestoreSetting.png)

<span data-ttu-id="2647e-134">Riceverai la conferma che il ripristino AXDB è andato a buon fine.</span><span class="sxs-lookup"><span data-stu-id="2647e-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="2647e-135">Dopo aver ricevuto questa conferma, puoi chiudere SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="2647e-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="2647e-136">Torna a **Internet Information Services** > **Pool di applicazioni** > **AOSService** e avvia AOSService.</span><span class="sxs-lookup"><span data-stu-id="2647e-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="2647e-137">Vai a **Servizi** e avvia i due servizi che hai arrestato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="2647e-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="2647e-138">Individua lo strumento AdminUserProvisioning su questa VM.</span><span class="sxs-lookup"><span data-stu-id="2647e-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="2647e-139">Guarda in K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="2647e-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="2647e-140">Esegui il file .ext utilizzando il tuo indirizzo utente nel campo **Indirizzo e-mail**.</span><span class="sxs-lookup"><span data-stu-id="2647e-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="2647e-141">Seleziona **Invia**.</span><span class="sxs-lookup"><span data-stu-id="2647e-141">Select **Submit**.</span></span>

![Provisioning utente amministratore](./media/8AdminUserProvisioning.png)

<span data-ttu-id="2647e-143">Questo processo richiede un paio di minuti per il completamento.</span><span class="sxs-lookup"><span data-stu-id="2647e-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="2647e-144">Dovresti ricevere un messaggio di conferma che l'utente amministratore è stato aggiornato correttamente.</span><span class="sxs-lookup"><span data-stu-id="2647e-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="2647e-145">Infine, esegui il prompt dei comandi come amministratore ed esegui iisreset</span><span class="sxs-lookup"><span data-stu-id="2647e-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Ripristino IIS](./media/9IISReset.png)

18. <span data-ttu-id="2647e-147">Chiudi la sessione Desktop remoto e utilizza la pagina **Dettagli ambiente** di LCS per accedere all'ambiente e confermare che funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="2647e-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
