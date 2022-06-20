---
title: Configurare impostazioni di parametri aggiuntivi
description: Come configurare le impostazioni dei parametri aggiuntivi in Project Service
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 75fe0aab8ea8bf41fcb98f4318380c93ac52fef8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919237"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Configurare le impostazioni dei parametri aggiuntivi (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Una volta configurati gli oggetti negli articoli precedenti, devi impostare altri parametri aggiuntivi del progetto da usare per i progetti. Quando hai installato per la prima volta [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] hai creato un'impostazione di parametri per creare prima tutti i record richiesti per [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. È ora di tornare indietro e configurare altri campi per queste impostazioni.  
  
 Dovrai configurare le seguenti impostazioni:  
  
-   Unità organizzativa  
  
-   Frequenza di fatturazione  
  
-   Modello di ore lavorative  
  
-   Listino prezzi  
 
In questo passaggio, dovrai indicare il tipo di assegnazione delle risorse desiderato:  
  
- **Centrale**. Solo i responsabili delle risorse possono assegnare le risorse ai progetti.  
  
- **Ibrido**. I responsabili delle risorse i, responsabili di progetto e gli account manager possono assegnare le risorse ai progetti.  
  
 
Per impostare i parametri di progetto:  
  
1. Passa a **Project Service > Parametri**.  
  
2. Fai clic sui parametri che desideri configurare (quello creato quando hai installato per la prima volta [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) oppure fai clic su **Nuovo** per crearne uno nuovo.  
  
3. Nell'area **Generale**, imposta tutte le opzioni per i parametri del progetto.  
  
4. Nell'area **Listino prezzi** fai clic su **+** per aggiungere un listino prezzi, seleziona un listino nell'elenco a discesa **Listino prezzi parametro di progetto**, quindi fai clic su **Salva**.  
  
5. Fai clic sul pulsante **Salva** nell'angolo in basso a destra dello schermo.  

> [!NOTE]
> Il record di parametri del progetto deve essere mantenuto per il corretto funzionamento di Project Service. Questo record non deve essere eliminato.

### <a name="see-also"></a>Vedi anche  
 [Configurare le risorse](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
