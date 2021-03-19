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
ms.openlocfilehash: 5e4f3bf15589181e3095400c131d322184578afa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284633"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="dbdb3-103">Abilitare le funzionalità dell'app Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="dbdb3-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="dbdb3-104">Le risorse possono utilizzare l'app Project Finder Mobile nei telefoni con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per cercare nuovi progetti da utilizzare e per aggiornare il set di competenze.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skillsets.</span></span>  
  
 <span data-ttu-id="dbdb3-105">L'app è disponibile per telefoni [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] e [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="dbdb3-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
    
 <span data-ttu-id="dbdb3-106">Per consentire agli utenti di visualizzare i requisiti delle risorse del progetto e aggiornare le competenze, devi selezionare le opzioni nelle impostazioni dei parametri per l'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-106">To allow users to view project resource requirements and update skills, options must be selected in the parameter settings for your organizational unit.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="dbdb3-107">L'app Project Finder Mobile funziona solo con [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (non con installazioni locali).</span><span class="sxs-lookup"><span data-stu-id="dbdb3-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="dbdb3-108">Passa a **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="dbdb3-109">Fai clic sulle impostazioni dei parametri da utilizzare per consentire le funzionalità dell'app Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="dbdb3-110">Nell'area **Generale** imposta **Requisiti di risorse visibili a risorse** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="dbdb3-111">Imposta **Consenti aggiornamento competenze da risorsa** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="dbdb3-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="dbdb3-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="dbdb3-113">Tale impostazione è globale.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-113">This is a global setting.</span></span> <span data-ttu-id="dbdb3-114">I responsabili di progetto possono impostare se un progetto singolo sarà disponibile nella pagina **Team di progetto** del progetto.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="dbdb3-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="dbdb3-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="dbdb3-116">Notifiche tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="dbdb3-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="dbdb3-117">invia i messaggi di posta elettronica relativi alle richieste di risorse ai destinatari seguenti nei momenti indicati:</span><span class="sxs-lookup"><span data-stu-id="dbdb3-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="dbdb3-118">Destinatario</span><span class="sxs-lookup"><span data-stu-id="dbdb3-118">Recipient</span></span>|<span data-ttu-id="dbdb3-119">Evento</span><span class="sxs-lookup"><span data-stu-id="dbdb3-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="dbdb3-120">Responsabile di progetto</span><span class="sxs-lookup"><span data-stu-id="dbdb3-120">Project manager</span></span>|<span data-ttu-id="dbdb3-121">- Una risorsa si iscrive a un progetto con l'app Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-121">- A resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="dbdb3-122">Risorsa</span><span class="sxs-lookup"><span data-stu-id="dbdb3-122">Resource</span></span>|<span data-ttu-id="dbdb3-123">- Il lavoro del progetto per cui la risorsa si è iscritta è già stato eseguito da un'altra risorsa.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-123">- The project work that the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="dbdb3-124">- La propria richiesta di approvazione di competenze è stata approvata o rifiutata.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-124">- The skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="dbdb3-125">- La richiesta di iscrizione al progetto è stata approvata o rifiutata.</span><span class="sxs-lookup"><span data-stu-id="dbdb3-125">- The project sign-up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="dbdb3-126">Informativa sulla privacy</span><span class="sxs-lookup"><span data-stu-id="dbdb3-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="dbdb3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbdb3-127">See Also</span></span>  
 [<span data-ttu-id="dbdb3-128">Configurare le risorse</span><span class="sxs-lookup"><span data-stu-id="dbdb3-128">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]