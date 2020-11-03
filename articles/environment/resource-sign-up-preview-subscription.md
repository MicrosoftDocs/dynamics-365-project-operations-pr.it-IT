---
title: Iscriversi per gli abbonamenti in anteprima a Project Operations per scenari basati su risorse/non stoccate
description: Questo argomento fornisce informazioni su come abbonarsi e distribuire Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078762"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="307e7-103">Iscriversi per gli abbonamenti in anteprima a Project Operations per scenari basati su risorse/non stoccate</span><span class="sxs-lookup"><span data-stu-id="307e7-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="307e7-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="307e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="307e7-105">Questo argomento spiega come abbonarsi all'offerta per i partner/anteprima e distribuire l'ambiente Project Operations per scenari basati su risorse/non stoccate.</span><span class="sxs-lookup"><span data-stu-id="307e7-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="307e7-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="307e7-106">Prerequisites</span></span>

- <span data-ttu-id="307e7-107">Riceverai un messaggio e-mail che ti invita a partecipare all'anteprima.</span><span class="sxs-lookup"><span data-stu-id="307e7-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="307e7-108">È possibile richiedere un'anteprima sul [sito Web di Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="307e7-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="307e7-109">L'utente che distribuisce l'anteprima deve disporre dei diritti di amministratore globale del tenant di Azure.</span><span class="sxs-lookup"><span data-stu-id="307e7-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="307e7-110">La distribuzione di un ambiente Finance richiede una sottoscrizione di Azure valida che verrà fatturata in base all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="307e7-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="307e7-111">Puoi utilizzare la sottoscrizione esistente della tua organizzazione o utilizzare una [versione di valutazione di Azure](https://azure.microsoft.com/en-us/free/) per iniziare.</span><span class="sxs-lookup"><span data-stu-id="307e7-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="307e7-112">L'ambiente CDS verrà fornito gratuitamente per un periodo limitato di 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="307e7-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="307e7-113">Sottoscrivi</span><span class="sxs-lookup"><span data-stu-id="307e7-113">Subscribe</span></span>

<span data-ttu-id="307e7-114">Quando la [richiesta di anteprima](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) viene approvata, riceverai tre offerte da Microsoft tramite e-mail.</span><span class="sxs-lookup"><span data-stu-id="307e7-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="307e7-115">Queste offerte consentono di distribuire l'anteprima di Project Operations:</span><span class="sxs-lookup"><span data-stu-id="307e7-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="307e7-116">Dynamics 365 Project Operations (CRM): versione di valutazione di anteprima</span><span class="sxs-lookup"><span data-stu-id="307e7-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="307e7-117">Office 365 Project Operations - Versione di valutazione di anteprima</span><span class="sxs-lookup"><span data-stu-id="307e7-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="307e7-118">Dynamics 365 Finance - Versione di valutazione di anteprima</span><span class="sxs-lookup"><span data-stu-id="307e7-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="307e7-119">Solo una persona, l'amministratore del tenant, in un'organizzazione deve eseguire questa attività.</span><span class="sxs-lookup"><span data-stu-id="307e7-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="307e7-120">Se non sei abbonato a questa versione, attendi fino a quando la tua organizzazione non è stata iscritta e hai ricevuto le credenziali utente.</span><span class="sxs-lookup"><span data-stu-id="307e7-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="307e7-121">Dynamics 365 Project Operations (CRM): versione di valutazione di anteprima</span><span class="sxs-lookup"><span data-stu-id="307e7-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="307e7-122">Prima di iniziare, assicurati di aver effettuato l'accesso a un browser con l'account utente di lavoro nel tenant in cui desideri l'anteprima di Project Operations.</span><span class="sxs-lookup"><span data-stu-id="307e7-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="307e7-123">Riscatta il primo codice dell'offerta, **Dynamics 365 Project Operations (CRM) - Versione di valutazione di anteprima** incollandolo nell'URL del browser.</span><span class="sxs-lookup"><span data-stu-id="307e7-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Riscattare l'offerta](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="307e7-125">Conferma l'ordine.</span><span class="sxs-lookup"><span data-stu-id="307e7-125">Confirm your order.</span></span>

![Conferma l'ordine](./media/17ConfirmOrderNew.png)

<span data-ttu-id="307e7-127">Vedrai la conferma che l'offerta è stata riscattata.</span><span class="sxs-lookup"><span data-stu-id="307e7-127">You will see confirmation offer was successfully redeemed.</span></span>

![Conferma](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="307e7-129">Office 365 Project Operations - Versione di valutazione di anteprima</span><span class="sxs-lookup"><span data-stu-id="307e7-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="307e7-130">Ripeti gli stessi passaggi del primo codice dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="307e7-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="307e7-131">Assicurati di aggiungere il secondo codice dell'offerta utilizzando lo stesso account utente utilizzato con il primo codice dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="307e7-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="307e7-132">Versione di valutazione di anteprima di Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="307e7-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="307e7-133">Ripeti gli stessi passaggi con l'ultima offerta dal messaggio e-mail di benvenuto.</span><span class="sxs-lookup"><span data-stu-id="307e7-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="307e7-134">Assegnare licenze</span><span class="sxs-lookup"><span data-stu-id="307e7-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="307e7-135">Avrai bisogno dell'accesso amministrativo al portale di Microsoft 365 dell'organizzazione per completare i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="307e7-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="307e7-136">Vai all'[interfaccia di amministrazione di Microsoft 365](https://portal.office.com/) per assegnare le licenze ai tuoi utenti.</span><span class="sxs-lookup"><span data-stu-id="307e7-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Home page dell'interfaccia di amministrazione](./media/14AdminPortal.png)

2. <span data-ttu-id="307e7-138">Nella pagina **Utenti attivi** seleziona gli utenti a cui assegnare una licenza.</span><span class="sxs-lookup"><span data-stu-id="307e7-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Assegnare licenze](./media/15AssignLicenses.png)

3. <span data-ttu-id="307e7-140">Verifica che le licenze **Anteprima di Dynamics 365 Project Operations (CRM)** e **Office 365 Project Operations - Anteprima** siano selezionate e seleziona **Salva le modifiche**.</span><span class="sxs-lookup"><span data-stu-id="307e7-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="307e7-141">Non è necessario assegnare l'offerta della versione di valutazione di Finance a un utente.</span><span class="sxs-lookup"><span data-stu-id="307e7-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="307e7-142">Avviare un nuovo progetto in LCS</span><span class="sxs-lookup"><span data-stu-id="307e7-142">Start a new project in LCS</span></span>

<span data-ttu-id="307e7-143">Creare un nuovo progetto LCS come descritto nell'argomento [Avviare un nuovo progetto in LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="307e7-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="307e7-144">Aggiungere una sottoscrizione di Azure a un progetto LCS</span><span class="sxs-lookup"><span data-stu-id="307e7-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="307e7-145">Per completare questa attività, segui i passaggi nell'argomento [Aggiungere una sottoscrizione di Azure al progetto LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="307e7-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="307e7-146">Distribuire l'ambiente demo di Finance con Project Operations per scenari basati su risorse/non stoccate</span><span class="sxs-lookup"><span data-stu-id="307e7-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="307e7-147">Segui le indicazioni nell'argomento [Effettuare il provisioning di un nuovo ambiente](resource-provision-new-environment.md) per completare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="307e7-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="307e7-148">Utilizza il tipo di distribuzione [ambiente demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) per l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="307e7-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="307e7-149">Installare i dati di impostazione e configurazione CDS</span><span class="sxs-lookup"><span data-stu-id="307e7-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="307e7-150">Installa i dati di installazione e configurazione CDS come descritto nell'argomento [Impostare e applicare i dati di configurazione in Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="307e7-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="307e7-151">Completa questo passaggio solo dopo che l'ambiente demo Finance è stato distribuito e i dati demo in FO sono pronti.</span><span class="sxs-lookup"><span data-stu-id="307e7-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>
