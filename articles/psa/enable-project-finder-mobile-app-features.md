---
title: Abilitare le funzionalità dell'app Project Finder Mobile
description: Come abilitare le funzionalità dell'app Project Finder Mobile per Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078883"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Abilitare le funzionalità dell'app Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Le risorse possono utilizzare l'app Project Finder Mobile nei telefoni con [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per cercare nuovi progetti da utilizzare e per aggiornare il set di competenze.  
  
 L'app è disponibile per telefoni [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] e [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Devi impostare una coppia di opzioni nei parametri per l'unità organizzativa per consentire agli utenti di visualizzare i requisiti di risorsa dei progetti e aggiornare le proprie competenze.  
  
> [!NOTE]
>  L'app Project Finder Mobile funziona solo con [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (non con installazioni locali).  
  
1. Passa a **Project Service > Parametri**.  
  
2. Fai clic sulle impostazioni dei parametri da utilizzare per consentire le funzionalità dell'app Project Finder Mobile.  
  
3. Nell'area **Generale** imposta **Requisiti di risorse visibili a risorse** su **Sì**.  
  
4. Imposta **Consenti aggiornamento competenze da risorsa** su **Sì**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Tale impostazione è globale. I responsabili di progetto possono impostare se un progetto singolo sarà disponibile nella pagina **Team di progetto** del progetto.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notifiche tramite posta elettronica  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] invia i messaggi di posta elettronica relativi alle richieste di risorse ai destinatari seguenti nei momenti indicati:  
  
|Destinatario|Eventi|  
|---------------|-----------|  
|Responsabile di progetto|-   Quando una risorsa si iscrive a un progetto con l'app Project Finder Mobile.|  
|Risorsa|-   Quando il lavoro del progetto per cui la risorsa si è iscritta è già stato eseguito da un'altra risorsa.<br />-   Quando la propria richiesta di approvazione di competenze è stata approvata o rifiutata.<br />-   Quando la richiesta di iscrizione al progetto è stata approvata o rifiutata.|  
  
## <a name="privacy-notice"></a>Informativa sulla privacy  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Vedi anche  
 [Configurare le risorse](../psa/set-up-resources.md)
