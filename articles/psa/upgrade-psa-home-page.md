---
title: Home page degli aggiornamenti
description: In questo argomento viene indicato dove trovare informazioni importanti sulle funzionalità nuove e modificate di Dynamics 365 Project Service Automation nonché la procedura per eseguire l'aggiornamento alla versione più recente.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 838eecb1229ea20106c7d5487dc37a81e8df501b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281708"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="779e9-103">Home page degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="779e9-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="779e9-104">Aggiornamento da PSA versione 2.x o 1.x alla versione 3.x</span><span class="sxs-lookup"><span data-stu-id="779e9-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="779e9-105">Nuove istanze</span><span class="sxs-lookup"><span data-stu-id="779e9-105">New instances</span></span>

<span data-ttu-id="779e9-106">A partire dal 17 maggio 2019, quando Project Service Automation viene selezionato durante il provisioning di una nuova istanza, la versione 3.x viene installata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="779e9-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="779e9-107">Istanze esistenti</span><span class="sxs-lookup"><span data-stu-id="779e9-107">Existing instances</span></span>

<span data-ttu-id="779e9-108">In precedenza, i clienti che avevano un'istanza di PSA versione 2.x e dovevano eseguire l'aggiornamento alla versione 3.x, ovvero la versione basata sull'interfaccia client unificata di PSA, dovevano contattare il supporto e fornire i dettagli relativi all'istanza in modo da poter abilitare l'istanza per l'aggiornamento alla versione 3.x.</span><span class="sxs-lookup"><span data-stu-id="779e9-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="779e9-109">A partire dal 1° marzo 2020, i clienti che hanno un'istanza di PSA versione 2.x e devono eseguire l'aggiornamento alla versione 3.x, potranno aggiornare le istanze direttamente dal portale di amministrazione senza dover contattare il supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="779e9-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="779e9-110">PSA versione 3.x include modifiche importanti.</span><span class="sxs-lookup"><span data-stu-id="779e9-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="779e9-111">È basata sul framework Unified Interface per offrire un'esperienza utente migliorata.</span><span class="sxs-lookup"><span data-stu-id="779e9-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="779e9-112">L'app riprogettata fornisce un'interfaccia utente coerente e uniforme e segue i principi di progettazione interattiva per la visualizzazione ottimale su uno schermo o dispositivo di qualsiasi dimensione.</span><span class="sxs-lookup"><span data-stu-id="779e9-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="779e9-113">Altre modifiche sono state apportate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="779e9-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="779e9-114">Alcune delle aree che sono state modificate sono quelle relative a determinazione dei prezzi, prenotazione e assegnazione di risorse, tempo, spese e approvazioni.</span><span class="sxs-lookup"><span data-stu-id="779e9-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="779e9-115">Prima di iniziare la procedura di aggiornamento, ti consigliamo di completare le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="779e9-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="779e9-116">Verifica se Dynamics 365 Field Service e Project Service Automation sono entrambi installati nell'istanza identificata.</span><span class="sxs-lookup"><span data-stu-id="779e9-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="779e9-117">Se entrambe le soluzioni sono installate, devi pianificarne l'aggiornamento prima di ricominciare a utilizzare regolarmente l'istanza.</span><span class="sxs-lookup"><span data-stu-id="779e9-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="779e9-118">Leggi attentamente gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="779e9-118">Carefully review the following topics.</span></span> <span data-ttu-id="779e9-119">La conoscenza e la comprensione delle modifiche tra le diverse versioni renderanno più agevole la procedura di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="779e9-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="779e9-120">Questi argomenti forniscono informazioni sulle principali modifiche in PSA, nonché considerazioni e suggerimenti per la pianificazione dell'aggiornamento alla versione 3.x.</span><span class="sxs-lookup"><span data-stu-id="779e9-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="779e9-121">Novità o modifiche in Project Service Automation versione 3</span><span class="sxs-lookup"><span data-stu-id="779e9-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="779e9-122">Considerazioni sull'aggiornamento - Da Project Service Automation versione 2.x o 1.x alla versione 3.x</span><span class="sxs-lookup"><span data-stu-id="779e9-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="779e9-123">Aggiorna la tua istanza sandbox per valutare le modifiche nell'implementazione prima di eseguire l'aggiornamento dell'istanza di produzione.</span><span class="sxs-lookup"><span data-stu-id="779e9-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="779e9-124">Dopo aver letto gli argomenti indicati sopra e quando sei pronto ad eseguire l'aggiornamento a PSA versione 3.x o alla versione basata su UCI, invia una richiesta al supporto tecnico Microsoft per rendere l'aggiornamento disponibile nell'interfaccia di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="779e9-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="779e9-125">Nella richiesta, fornisci i dettagli sull'istanza.</span><span class="sxs-lookup"><span data-stu-id="779e9-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="779e9-126">Versioni precedenti di PSA (PSA versione 2.x) in un'istanza appena creata</span><span class="sxs-lookup"><span data-stu-id="779e9-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="779e9-127">A partire dal 17 maggio 2019, tutte le nuove istanze hanno UCI come client predefinito.</span><span class="sxs-lookup"><span data-stu-id="779e9-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="779e9-128">Per l'allineamento a questa modifica, il provisioning di PSA versione 3.x e Field Service versione 8.x viene eseguito per impostazione predefinita, in quanto tali versioni sono progettate per l'utilizzo con il client UCI.</span><span class="sxs-lookup"><span data-stu-id="779e9-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="779e9-129">A partire dal 1° marzo 2020, i clienti di Dynamics PSA non saranno più in grado di creare un nuovo ambiente con le versioni precedenti di PSA, ad esempio PSA versione 2.x o precedente.</span><span class="sxs-lookup"><span data-stu-id="779e9-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="779e9-130">Qualsiasi nuovo ambiente supporterà solo la versione 3.x di PSA.</span><span class="sxs-lookup"><span data-stu-id="779e9-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="779e9-131">Per la migliore esperienza quando utilizzi versioni precedenti delle applicazioni Field Service e PSA, vai alla pagina **Impostazioni di sistema** e imposta il campo **Utilizza solo la nuova Unified Interface (scelta consigliata)** su **No** in quanto queste versioni non sono progettate per essere caricate correttamente in UCI.</span><span class="sxs-lookup"><span data-stu-id="779e9-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="779e9-132">Dopo aver disattivato UCI, puoi aprire ed eseguire queste versioni di Field Service e PSA utilizzando il client Web precedente.</span><span class="sxs-lookup"><span data-stu-id="779e9-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]