---
title: Abilitare le funzionalità dell'app Project Finder Mobile
description: Come abilitare le funzionalità dell'app Project Finder Mobile per Project Service
author: JohnPBurrows
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144553"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="236a1-103">Abilitare le funzionalità dell'app Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="236a1-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="236a1-104">Le risorse possono utilizzare l'app Project Finder Mobile nei telefoni con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per cercare nuovi progetti da utilizzare e per aggiornare il set di competenze.</span><span class="sxs-lookup"><span data-stu-id="236a1-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skillsets.</span></span>  
  
 <span data-ttu-id="236a1-105">L'app è disponibile per telefoni [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] e [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="236a1-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
    
 <span data-ttu-id="236a1-106">Per consentire agli utenti di visualizzare i requisiti delle risorse del progetto e aggiornare le competenze, devi selezionare le opzioni nelle impostazioni dei parametri per l'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="236a1-106">To allow users to view project resource requirements and update skills, options must be selected in the parameter settings for your organizational unit.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="236a1-107">L'app Project Finder Mobile funziona solo con [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (non con installazioni locali).</span><span class="sxs-lookup"><span data-stu-id="236a1-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="236a1-108">Passa a **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="236a1-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="236a1-109">Fai clic sulle impostazioni dei parametri da utilizzare per consentire le funzionalità dell'app Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="236a1-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="236a1-110">Nell'area **Generale** imposta **Requisiti di risorse visibili a risorse** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="236a1-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="236a1-111">Imposta **Consenti aggiornamento competenze da risorsa** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="236a1-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="236a1-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="236a1-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="236a1-113">Tale impostazione è globale.</span><span class="sxs-lookup"><span data-stu-id="236a1-113">This is a global setting.</span></span> <span data-ttu-id="236a1-114">I responsabili di progetto possono impostare se un progetto singolo sarà disponibile nella pagina **Team di progetto** del progetto.</span><span class="sxs-lookup"><span data-stu-id="236a1-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="236a1-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="236a1-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="236a1-116">Notifiche tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="236a1-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="236a1-117">invia i messaggi di posta elettronica relativi alle richieste di risorse ai destinatari seguenti nei momenti indicati:</span><span class="sxs-lookup"><span data-stu-id="236a1-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="236a1-118">Destinatario</span><span class="sxs-lookup"><span data-stu-id="236a1-118">Recipient</span></span>|<span data-ttu-id="236a1-119">Evento</span><span class="sxs-lookup"><span data-stu-id="236a1-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="236a1-120">Responsabile di progetto</span><span class="sxs-lookup"><span data-stu-id="236a1-120">Project manager</span></span>|<span data-ttu-id="236a1-121">- Una risorsa si iscrive a un progetto con l'app Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="236a1-121">- A resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="236a1-122">Risorsa</span><span class="sxs-lookup"><span data-stu-id="236a1-122">Resource</span></span>|<span data-ttu-id="236a1-123">- Il lavoro del progetto per cui la risorsa si è iscritta è già stato eseguito da un'altra risorsa.</span><span class="sxs-lookup"><span data-stu-id="236a1-123">- The project work that the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="236a1-124">- La propria richiesta di approvazione di competenze è stata approvata o rifiutata.</span><span class="sxs-lookup"><span data-stu-id="236a1-124">- The skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="236a1-125">- La richiesta di iscrizione al progetto è stata approvata o rifiutata.</span><span class="sxs-lookup"><span data-stu-id="236a1-125">- The project sign-up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="236a1-126">Informativa sulla privacy</span><span class="sxs-lookup"><span data-stu-id="236a1-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="236a1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="236a1-127">See Also</span></span>  
 [<span data-ttu-id="236a1-128">Configurare le risorse</span><span class="sxs-lookup"><span data-stu-id="236a1-128">Set up resources</span></span>](../psa/set-up-resources.md)
