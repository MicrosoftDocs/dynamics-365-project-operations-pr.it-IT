---
title: Abilitare le funzionalità dell'app Project Finder Mobile
description: Come abilitare le funzionalità dell'app Project Finder Mobile per Project Service
author: JohnPBurrows
manager: kfend
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132968"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="4df91-103">Abilitare le funzionalità dell'app Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4df91-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4df91-104">Le risorse possono utilizzare l'app Project Finder Mobile nei telefoni con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per cercare nuovi progetti da utilizzare e per aggiornare il set di competenze.</span><span class="sxs-lookup"><span data-stu-id="4df91-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="4df91-105">L'app è disponibile per telefoni [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] e [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="4df91-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="4df91-106">Devi impostare una coppia di opzioni nei parametri per l'unità organizzativa per consentire agli utenti di visualizzare i requisiti di risorsa dei progetti e aggiornare le proprie competenze.</span><span class="sxs-lookup"><span data-stu-id="4df91-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4df91-107">L'app Project Finder Mobile funziona solo con [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (non con installazioni locali).</span><span class="sxs-lookup"><span data-stu-id="4df91-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="4df91-108">Passa a **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="4df91-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="4df91-109">Fai clic sulle impostazioni dei parametri da utilizzare per consentire le funzionalità dell'app Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="4df91-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="4df91-110">Nell'area **Generale** imposta **Requisiti di risorse visibili a risorse** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="4df91-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="4df91-111">Imposta **Consenti aggiornamento competenze da risorsa** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="4df91-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="4df91-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="4df91-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="4df91-113">Tale impostazione è globale.</span><span class="sxs-lookup"><span data-stu-id="4df91-113">This is a global setting.</span></span> <span data-ttu-id="4df91-114">I responsabili di progetto possono impostare se un progetto singolo sarà disponibile nella pagina **Team di progetto** del progetto.</span><span class="sxs-lookup"><span data-stu-id="4df91-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="4df91-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="4df91-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="4df91-116">Notifiche tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="4df91-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="4df91-117">invia i messaggi di posta elettronica relativi alle richieste di risorse ai destinatari seguenti nei momenti indicati:</span><span class="sxs-lookup"><span data-stu-id="4df91-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="4df91-118">Destinatario</span><span class="sxs-lookup"><span data-stu-id="4df91-118">Recipient</span></span>|<span data-ttu-id="4df91-119">Eventi</span><span class="sxs-lookup"><span data-stu-id="4df91-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="4df91-120">Responsabile di progetto</span><span class="sxs-lookup"><span data-stu-id="4df91-120">Project manager</span></span>|<span data-ttu-id="4df91-121">-   Quando una risorsa si iscrive a un progetto con l'app Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="4df91-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="4df91-122">Risorsa</span><span class="sxs-lookup"><span data-stu-id="4df91-122">Resource</span></span>|<span data-ttu-id="4df91-123">-   Quando il lavoro del progetto per cui la risorsa si è iscritta è già stato eseguito da un'altra risorsa.</span><span class="sxs-lookup"><span data-stu-id="4df91-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="4df91-124">-   Quando la propria richiesta di approvazione di competenze è stata approvata o rifiutata.</span><span class="sxs-lookup"><span data-stu-id="4df91-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="4df91-125">-   Quando la richiesta di iscrizione al progetto è stata approvata o rifiutata.</span><span class="sxs-lookup"><span data-stu-id="4df91-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="4df91-126">Informativa sulla privacy</span><span class="sxs-lookup"><span data-stu-id="4df91-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="4df91-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4df91-127">See Also</span></span>  
 [<span data-ttu-id="4df91-128">Configurare le risorse</span><span class="sxs-lookup"><span data-stu-id="4df91-128">Set up resources</span></span>](../psa/set-up-resources.md)
