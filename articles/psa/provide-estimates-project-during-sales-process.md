---
title: Fornire stime di lavoro per un progetto durante il processo di vendita
description: Come fornire stime di lavoro per un progetto durante il processo di vendita in Project Service
author: ruhercul
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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283553"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Fornire stime di lavoro per un progetto durante il processo di vendita (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Durante il processo di vendita, puoi eseguire le stime di vendita dal basso fino alle voci di un'offerta. Le funzionalità [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] offrono un modo più scientifico e deterministico per fornire le stime di vendita suddividendo gli elementi di lavoro e associando gli attributi pertinenti che contribuiscono alle stime del progetto nella struttura di suddivisione del lavoro.  
  
 Dopo aver acquisito la vendita, puoi utilizzare la struttura di suddivisione del lavoro associata al piano di progetto, ridefinendolo come necessario per il buon completamento del progetto.  
  
## <a name="link-a-project-to-a-quote-line"></a>Collega un progetto a una riga di offerta  
 Quando si crea una riga di offerta basata sul progetto offerta, puoi creare un nuovo progetto dalla riga di offerta. Puoi quindi utilizzare i modelli di progetto, che sono piani di progetto standard preconfigurati e stime finanziarie comuni all'organizzazione, o una copia di un piano di progetto e stime da un progetto passato. Quando crei un progetto, la scelta di un modello di progetto offre una base per ridefinire il piano di progetto, le stime e i requisiti del ruolo. Creando il progetto dall'offerta, questo viene automaticamente associato alla riga dell'offerta.  
  
## <a name="project-estimate-components"></a>Componenti della stima del progetto  
 La struttura di suddivisione del lavoro in un progetto offre un modo per suddividere il lavoro in attività, di gestire una gerarchia di attività e assegnare una stima del lavoro richiesto per completare ogni attività. Puoi associare i ruoli a un'attività per indicare una stima del tipo di risorsa richiesto per completare un'attività e una pianificazione.  
  
 La struttura di suddivisione del lavoro consente di determinare le stime di lavoro e di pianificazione. Per impostazione predefinita, il progetto utilizza i listini prezzi definiti in precedenza. I prezzi di costo e di vendita definiti nei listini prezzi consentono di determinare le stime finanziarie per la suddivisione del lavoro del progetto.  
  
 Se il progetto è associato a un'offerta e l'offerta ha un listino prezzi diverso da quello predefiniti, il listino prezzi dell'offerta viene utilizzato per stime finanziarie.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importa le stime da un progetto a un'offerta  
 Con le stime di progetto nel progetto, puoi importarle nella riga dell'offerta:  
  
-   In **Dettagli riga di offerta** fai clic su **Importa da stime**. 

-   Seleziona se importare le stime di progetto riepilogate dal tipo delle transazioni, ruolo, o livello del nodo della struttura di suddivisione del lavoro.  
  
### <a name="see-also"></a>Vedi anche  
 [Guida del responsabile di progetto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]