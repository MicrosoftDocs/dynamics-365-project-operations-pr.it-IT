---
title: Risolvere i problemi relativi alla griglia delle attività
description: Questo argomento fornisce le informazioni sulla risoluzione dei problemi necessaria quando si utilizza la griglia delle attività.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031542"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="99725-103">Risolvere i problemi relativi alla griglia delle attività</span><span class="sxs-lookup"><span data-stu-id="99725-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="99725-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="99725-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="99725-105">Questa argomento descrive come risolvere i problemi che potresti riscontrare mentre utilizzi la gestione dei costi.</span><span class="sxs-lookup"><span data-stu-id="99725-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="99725-106">Abilitare i cookie</span><span class="sxs-lookup"><span data-stu-id="99725-106">Enable cookies</span></span>

<span data-ttu-id="99725-107">Project Operations richiede che i cookie di terze parti siano abilitati per eseguire il rendering della struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="99725-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="99725-108">Quando i cookie di terze parti non sono abilitati, invece di visualizzare le attività, vedrai una pagina vuota quando selezioni la scheda **Attività** nella pagina **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="99725-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Scheda vuota quando i cookie di terze parti non sono abilitati](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="99725-110">Soluzione alternativa</span><span class="sxs-lookup"><span data-stu-id="99725-110">Workaround</span></span>
<span data-ttu-id="99725-111">Per Microsoft Edge o Google Chrome, le seguenti procedure delineano come aggiornare le impostazioni del browser per abilitare i cookie di terze parti.</span><span class="sxs-lookup"><span data-stu-id="99725-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="99725-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="99725-112">Microsoft Edge</span></span>

1. <span data-ttu-id="99725-113">Apri il browser Edge.</span><span class="sxs-lookup"><span data-stu-id="99725-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="99725-114">Nell'angolo superiore destro seleziona i **puntini di sospensione** (...) e quindi **Impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="99725-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="99725-115">Sotto **Cookie e autorizzazioni del sito** seleziona **Cookie e dati dei siti**.</span><span class="sxs-lookup"><span data-stu-id="99725-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="99725-116">Disattiva **Blocca cookie di terze parti**.</span><span class="sxs-lookup"><span data-stu-id="99725-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="99725-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="99725-117">Google Chrome</span></span>

1. <span data-ttu-id="99725-118">Aprire il browser Chrome.</span><span class="sxs-lookup"><span data-stu-id="99725-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="99725-119">Nell'angolo superiore destro, seleziona i tre puntini verticali e quindi seleziona **Impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="99725-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="99725-120">Sotto **Privacy e sicurezza** seleziona **Cookie e altri dati dei siti**.</span><span class="sxs-lookup"><span data-stu-id="99725-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="99725-121">Seleziona **Consenti tutti i cookie**.</span><span class="sxs-lookup"><span data-stu-id="99725-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99725-122">Se blocchi i cookie di terze parti, tutti i cookie e i dati di altri siti verranno bloccati, anche se il sito è consentito nell'elenco delle eccezioni.</span><span class="sxs-lookup"><span data-stu-id="99725-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="99725-123">Endpoint PEX</span><span class="sxs-lookup"><span data-stu-id="99725-123">PEX Endpoint</span></span>

<span data-ttu-id="99725-124">Project Operations richiede che un parametro di progetto faccia riferimento all'endpoint PEX.</span><span class="sxs-lookup"><span data-stu-id="99725-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="99725-125">Questo endpoint è necessario per comunicare con il servizio utilizzato per il rendering della struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="99725-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="99725-126">Se il parametro non è abilitato, riceverai l'errore "Il parametro del progetto non è valido".</span><span class="sxs-lookup"><span data-stu-id="99725-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="99725-127">Soluzione alternativa</span><span class="sxs-lookup"><span data-stu-id="99725-127">Workaround</span></span>
 ![Campo Endpoint PEX nel parametro di progetto](media/projectparameter.png)

1. <span data-ttu-id="99725-129">Aggiungi il campo **Endpoint PEX** alla pagina **Parametri di progetto**.</span><span class="sxs-lookup"><span data-stu-id="99725-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="99725-130">Aggiorna il campo con il seguente valore: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="99725-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="99725-131">Rimuovi il campo dalla pagina **Parametri di progetto**.</span><span class="sxs-lookup"><span data-stu-id="99725-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="99725-132">Privilegi per progetto per il Web</span><span class="sxs-lookup"><span data-stu-id="99725-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="99725-133">Project Operations si basa su un servizio di pianificazione esterno.</span><span class="sxs-lookup"><span data-stu-id="99725-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="99725-134">Il servizio richiede che un utente abbia diversi ruoli assegnati per leggere e scrivere nelle entità correlate alla struttura di suddivisione del lavoro.</span><span class="sxs-lookup"><span data-stu-id="99725-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="99725-135">Queste entità includono attività di progetto, assegnazioni di risorse e dipendenze tra attività.</span><span class="sxs-lookup"><span data-stu-id="99725-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="99725-136">Se un utente non può eseguire il rendering della struttura di suddivisione del lavoro quando accede alla scheda **Attività** probabilmente è perché Progetto per Project Operations non è stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="99725-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="99725-137">Un utente potrebbe ricevere un errore relativo al ruolo di sicurezza o un errore relativo a un rifiuto di accesso.</span><span class="sxs-lookup"><span data-stu-id="99725-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="99725-138">Soluzione alternativa</span><span class="sxs-lookup"><span data-stu-id="99725-138">Workaround</span></span>

1. <span data-ttu-id="99725-139">Vai a **Impostazioni > Sicurezza > Utenti > Utenti dell'applicazione**.</span><span class="sxs-lookup"><span data-stu-id="99725-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Lettore dell'applicazione](media/applicationuser.jpg)
   
2. <span data-ttu-id="99725-141">Fai doppio clic sul record dell'utente dell'applicazione per verificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="99725-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="99725-142">L'utente ha accesso al progetto:</span><span class="sxs-lookup"><span data-stu-id="99725-142">The user has access to the project.</span></span> <span data-ttu-id="99725-143">Questa verifica viene in genere eseguita assicurando che l'utente abbia il ruolo di sicurezza **Responsabile di progetto**.</span><span class="sxs-lookup"><span data-stu-id="99725-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="99725-144">L'utente dell'applicazione Microsoft Project esiste ed è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="99725-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="99725-145">Se l'utente non esiste, puoi crearne un nuovo record utente.</span><span class="sxs-lookup"><span data-stu-id="99725-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="99725-146">Seleziona **Nuovi utenti**.</span><span class="sxs-lookup"><span data-stu-id="99725-146">Select **New Users**.</span></span> <span data-ttu-id="99725-147">Modifica il modulo di immissione su **Utente dell'applicazione**, quindi aggiungi l'**ID applicazione**.</span><span class="sxs-lookup"><span data-stu-id="99725-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Dettagli utente dell'applicazione](media/applicationuserdetails.jpg)

4. <span data-ttu-id="99725-149">Verifica che all'utente sia stata assegnata la licenza corretta e che il servizio sia abilitato nei dettagli dei piani di servizio della licenza.</span><span class="sxs-lookup"><span data-stu-id="99725-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="99725-150">Verifica che l'utente possa aprire project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="99725-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="99725-151">Verifica tramite i parametri di progetto che il sistema stia puntando all'endpoint di progetto corretto.</span><span class="sxs-lookup"><span data-stu-id="99725-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="99725-152">Verifica che l'utente dell'applicazione di progetto sia stato creato.</span><span class="sxs-lookup"><span data-stu-id="99725-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="99725-153">Applica i seguenti ruoli di sicurezza all'utente:</span><span class="sxs-lookup"><span data-stu-id="99725-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="99725-154">Utente di Dataverse</span><span class="sxs-lookup"><span data-stu-id="99725-154">Dataverse User</span></span>
  - <span data-ttu-id="99725-155">Sistema Project Operations</span><span class="sxs-lookup"><span data-stu-id="99725-155">Project Operations System</span></span>
  - <span data-ttu-id="99725-156">Sistema di progetto</span><span class="sxs-lookup"><span data-stu-id="99725-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="99725-157">Errore durante l'aggiornamento della struttura di suddivisione del lavoro</span><span class="sxs-lookup"><span data-stu-id="99725-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="99725-158">Quando vengono apportati uno o più aggiornamenti alla struttura di suddivisione del lavoro, le modifiche non riescono e non vengono salvate.</span><span class="sxs-lookup"><span data-stu-id="99725-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="99725-159">Si verifica un errore nella griglia di pianificazione indicante che "Impossibile salvare la modifica recente apportata".</span><span class="sxs-lookup"><span data-stu-id="99725-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="99725-160">Soluzione alternativa</span><span class="sxs-lookup"><span data-stu-id="99725-160">Workaround</span></span>

1. <span data-ttu-id="99725-161">Verifica che all'utente sia stata assegnata la licenza corretta e che il servizio sia abilitato nei dettagli dei piani di servizio della licenza.</span><span class="sxs-lookup"><span data-stu-id="99725-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="99725-162">Verifica che l'utente possa aprire project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="99725-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="99725-163">Verifica che il sistema stia puntando all'endpoint di progetto corretto.</span><span class="sxs-lookup"><span data-stu-id="99725-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="99725-164">Verifica che l'utente dell'applicazione di progetto sia stato creato.</span><span class="sxs-lookup"><span data-stu-id="99725-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="99725-165">Applica i seguenti ruoli di sicurezza all'utente:</span><span class="sxs-lookup"><span data-stu-id="99725-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="99725-166">Utente Dataverse o utente di base</span><span class="sxs-lookup"><span data-stu-id="99725-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="99725-167">Sistema Project Operations</span><span class="sxs-lookup"><span data-stu-id="99725-167">Project Operations System</span></span>
  - <span data-ttu-id="99725-168">Sistema di progetto</span><span class="sxs-lookup"><span data-stu-id="99725-168">Project System</span></span>
  - <span data-ttu-id="99725-169">Sistema di doppia scrittura di Project Operations (questo ruolo è richiesto se distribuisci lo scenario basato su risorse/materiali non stoccati di operazioni di progetto).</span><span class="sxs-lookup"><span data-stu-id="99725-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
