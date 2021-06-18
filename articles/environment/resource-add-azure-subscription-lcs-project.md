---
title: Aggiungere una sottoscrizione di Azure a un progetto LCS
description: Questo argomento fornisce informazioni su come connettere la sottoscrizione di Azure a un progetto LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000621"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="1c4c1-103">Aggiungere una sottoscrizione di Azure a un progetto LCS</span><span class="sxs-lookup"><span data-stu-id="1c4c1-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="1c4c1-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="1c4c1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1c4c1-105">Gli ambienti ospitati su cloud devono essere distribuiti utilizzando una sottoscrizione di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="1c4c1-106">Questo argomento descrive come connettere la sottoscrizione di Azure esistente a un progetto LCS.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="1c4c1-107">Concedere il consenso amministratore</span><span class="sxs-lookup"><span data-stu-id="1c4c1-107">Grant admin consent</span></span>

1. <span data-ttu-id="1c4c1-108">Nel progetto LCS, nella sezione **Ambienti**, seleziona **Impostazioni di Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Impostazioni Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="1c4c1-110">Nella pagina **Impostazioni progetto**, nella scheda **Connettori di Azure**, seleziona **Autorizza**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="1c4c1-111">Ciò consente di distribuire gli ambienti a questo progetto.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-111">This allows environments to be deployed to this project.</span></span>

![Connettori di Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="1c4c1-113">Seleziona **Autorizza** di nuovo per fornire il consenso amministratore.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-113">Select **Authorize** again to provide admin consent.</span></span>

![Concedi consenso amministratore](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="1c4c1-115">Accetta la richiesta di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-115">Accept the permissions request.</span></span>

![Accetta richiesta di autorizzazione](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="1c4c1-117">L'autorizzazione è ora completa.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-117">The authorization is now complete.</span></span> 

![Autorizzazione completata](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="1c4c1-119">Fornire l'accesso a Servizi di distribuzione Dynamics alla sottoscrizione di Azure</span><span class="sxs-lookup"><span data-stu-id="1c4c1-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="1c4c1-120">Vai a [Fatturazione di Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e seleziona la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="1c4c1-121">Servizi di distribuzione Dynamics deve accedere a questa sottoscrizione per poter distribuire gli ambienti.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Dettagli sottoscrizione di Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="1c4c1-123">Seleziona **Controllo di accesso (IAM)** nel riquadro di spostamento, quindi seleziona **Aggiungi assegnazione di ruolo**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="1c4c1-124">Nel dispositivo di scorrimento sul lato destro, seleziona **Ruolo collaboratore** e nell'elenco fornito trova e seleziona **Servizi di distribuzione Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="1c4c1-125">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-125">Select **Save**.</span></span>

![Accesso sottoscrizione](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="1c4c1-127">Aggiungere un connettore di sottoscrizione a un progetto LCS</span><span class="sxs-lookup"><span data-stu-id="1c4c1-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="1c4c1-128">Nel progetto LCS, nella pagina **Impostazioni di Microsoft Azure**, seleziona **Aggiungi** per aggiungere un nuovo connettore.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="1c4c1-129">Immetti l'ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="1c4c1-130">È possibile trovare l'ID della sottoscrizione di Azure nel [portale di Azure](https://ms.portal.azure.com/), sotto **Impostazioni** in basso a sinistra dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="1c4c1-131">Nel campo **Configura per l'utilizzo di Azure Resource Manager**, seleziona **Sì**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="1c4c1-132">Assicurati che il dominio tenant AAD della sottoscrizione di Azure corrisponda alla sottoscrizione di Azure proprietaria del dominio che stai utilizzando e seleziona **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="1c4c1-133">Nella schermata **Impostazione di Microsoft Azure**, seleziona **Avanti** per confermare.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="1c4c1-134">Se ricevi un errore in questa schermata, torna alla sezione [Fornire l'accesso a Servizi di distribuzione Dynamics alla sottoscrizione di Azure](#provide) in questo argomento e assicurati di aver completato tutti i passaggi.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="1c4c1-135">Scarica il certificato di gestione di Azure in una cartella locale sul tuo computer.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="1c4c1-136">Chiedi all'amministratore della tua sottoscrizione di Azure di caricare il certificato nel portale di gestione di Azure selezionando la sottoscrizione e andando in **Impostazioni** > **Certificati di gestione**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="1c4c1-137">Questo certificato consente a LCS di comunicare con Azure per tuo conto.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="1c4c1-138">Puoi saltare questo passaggio se il tuo utente ha accesso alla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="1c4c1-139">Seleziona **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-139">Select  **Next**.</span></span>
8. <span data-ttu-id="1c4c1-140">Seleziona l'area di Azure in cui eseguire la distribuzione e seleziona un data center vicino al luogo in cui prevedi di utilizzare questo sistema.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="1c4c1-141">Seleziona **Connetti**.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-141">Select  **Connect**.</span></span>

<span data-ttu-id="1c4c1-142">La sottoscrizione di Azure è stata connessa in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="1c4c1-143">Ora puoi distribuire ambienti ospitati su cloud di Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
