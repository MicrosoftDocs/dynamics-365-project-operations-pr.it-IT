---
title: Tener traccia dello stato di un progetto
description: Come registrare lo stato di un progetto in Project Service
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
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149593"
---
# <a name="track-a-projects-status-project-service"></a>Registrare lo stato di un progetto (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Utilizzare [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] per registrare l'avanzamento di un progetto del cliente.  

Quando l'impegno avanza, le fasi del progetto si aggiornano per riflettere la fase dell'impegno:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Nuovo**    | Quando crei un progetto, la fase è impostata su **Nuovo**. Se hai creato il progetto da un modello, in questa fase il progetto potrebbe avere una pianificazione, stime e dati del team. In caso contrario, sarà la struttura del progetto e sarà necessario immettere manualmente il resto dei componenti del progetto. |
|  **Offerta**   |      Quando si associa un progetto a un'offerta o lo si crea da un'offerta, la fase del progetto è impostata su **Offerta** e anche le date di inizio e di fine stimate vengono aggiornate. Quando il progetto si trova nella fase di offerta, vengono visualizzati dettagli sull'offerta nella scheda **Vendite** della pagina **Progetto**.      |
|   **Piano**   |                                     Quando viene acquisita un'offerta associata a un progetto e quando l'impegno avanza alla fase contratto, la fase del progetto si aggiorna a **Piano**. I dettagli del contratto vengono visualizzati nella scheda **Vendite** nella pagina **Progetto**.                                      |
| **Completo** |                    Quando il lavoro del progetto è completato, puoi passare la fase a **Completa**. Quando la fase del progetto è impostata su completo, è chiaro che il lavoro è completato al 100% ma viene tenuto aperto per tutte le voci di tempo e spesa da registrare.                     |
|  **Chiudi**   |           Quando tutte le transazioni sono state registrate nel progetto e non prevedi di registrarne altre, puoi impostare manualmente la fase su **Chiudi**. Quando il progetto è impostato su **Chiudi**, non è possibile registrare altre transazioni nel progetto e questo sarà di sola lettura.           |

## <a name="to-track-a-projects-status"></a>Per registra lo stato del progetto  

1.  Passa a **Project Service > Progetti**.  

2.  Fai clic sul progetto che desideri utilizzare.  

3.  Nella barra sulla parte superiore dello schermo, seleziona la freccia in giù accanto al nome del progetto e quindi fai clic su **Registrazione di progetto**.  

4.  Seleziona **Registrazione lavoro richiesto** o **Registrazione costi** nell'elenco a discesa sull'elenco attività.  

5.  Fai doppio clic sull'attività per modificarla. Puoi anche spostare o ridimensionare le barre nel diagramma di Gantt per modificare l'ora e l'avanzamento di un'attività.  

### <a name="see-also"></a>Vedi anche  
 [Guida del responsabile di progetto](../psa/project-manager-guide.md)
