---
title: Creare un modello di progetto
description: Come creare un modello di progetto in Project Service
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
ms.openlocfilehash: 78d25183aad8d86593d3f2582295db59eb84cf14
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133193"
---
# <a name="create-a-project-template-project-service"></a>Creare un modello di progetto (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

I modelli di progetto consentono di risparmiare tempo se la società esegue regolarmente offerte per tipi di progetti simili. Tali modelli forniscono un set standard di ruoli e di ore previste per tipo di progetto. I responsabili di gestione account e di progetto possono creare i progetti in base a un modello di progetto o possono copiare il modello ed eseguirne di personalizzati.  
  
## <a name="components-of-project-template"></a>Componenti del modello di progetto
 Un modello di progetto è composto da tre componenti:  
  
- **Struttura di suddivisione del lavoro**: una struttura di suddivisione del lavoro nel modello di progetto ha lo stesso set di elementi del progetto. È possibile creare una gerarchia di attività, associare ruoli all'attività, definire gli attributi di pianificazione, impostare dipendenze e visualizzare i dati nel diagramma di Gantt. La struttura di suddivisione del lavoro in modelli di progetto supporta anche modalità di attività per ogni attività. Non esiste una differenza tra un modello di progetto e un progetto quando si crea una pianificazione del lavoro.  
  
- **Stime di progetto**: e stime di progetto nei modelli funzionano nello stesso modo in cui funzionano nei progetti, ad eccezione del fatto che i costi e i prezzi di vendita specificati sono sempre i costi e i listini prezzi di vendita predefiniti indicati nei parametri di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Per il resto, il funzionamento è analogo a quello del progetto.  
  
- **Formazione del team di progetto**: quando si crea un team di progettazione per un modello di progetto, non puoi prenotare una risorsa denominata nel modello. Puoi utilizzare **Genera team progetto** nella struttura di suddivisione del lavoro per creare un gruppo di risorse generiche. Puoi anche specificare le attività e le competenze necessarie per risorse generiche. Non puoi sostituire una risorsa generica a una risorsa prenotabile in modelli di progetto.  
  
## <a name="create-a-project-from-a-template"></a>Crea un progetto da un modello  
 Puoi creare un progetto da un modello nei modi seguenti:  
  
-   Quando si crea un progetto dall'offerta, puoi scegliere un modello di progetto nel modulo di creazione rapida del progetto stesso.  
  
-   Quando si crea un progetto facendo clic su **Nuovo progetto**, viene visualizzato il modulo del progetto prima di salvare il record. Qui puoi fare clic sul campo **Seleziona un modello** per scegliere un modello nell'elenco dei modelli predefiniti nell'organizzazione.  
  
-   Fai clic su **Crea progetto da un modello** nella pagina **Modello di progetto** per creare un progetto dal modello.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Copia di componenti di un modello in un progetto  
 Quando si copiano i componenti di un modello in un progetto, è necessario tenere in considerazione alcuni aspetti.  
  
 **Copia di una struttura di suddivisione del lavoro**: quando si copia la struttura di suddivisione del lavoro utilizzando un modello di progetto, se il progetto ha un calendario diverso dal progetto, le ore lavorative nel calendario di progetto verranno applicate alla pianificazione di attività. In questo modo viene modificata la pianificazione nel calendario di progetto di backup. Analogamente, la prima attività sulla struttura di suddivisione del lavoro ha come data quella di inizio del progetto, in modo che il resto della pianificazione della gerarchia di attività venga aggiornato in base alla durata e alle dipendenze specificate nella struttura di suddivisione del lavoro del modello.  
  
 **Copia di stime di progetto**: quando si copia nelle righe di stima del progetto, i listini prezzi vengono aggiornati in base all'unità proprietaria del progetto per il listino prezzi di costo e in base al cliente per il listino prezzi di vendita. Il costo unitario e i prezzi di vendita vengono determinati da tali listini prezzi dei progetti associati a un'entità di vendita.  
  
 **Copia di un team di progetto**: quando si copia il team di progetto dal modello in un progetto, le risorse generiche vengono copiate, insieme alle competenze definite nel modello. Le assegnazioni di risorse generiche vengono memorizzate come nel modello del progetto.  
  
### <a name="see-also"></a>Vedi anche  
 [Guida del responsabile di progetto](../psa/project-manager-guide.md)
