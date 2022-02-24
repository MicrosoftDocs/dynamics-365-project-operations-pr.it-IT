---
title: Pianificare un progetto con una struttura di suddivisione del lavoro
description: Come pianificare un progetto con una struttura di suddivisione del lavoro in Project Service
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
ms.openlocfilehash: cf12cc3bcf061e1daffafb248cfd76809c6444ec
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149818"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Pianificare un progetto con una struttura di suddivisione del lavoro (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Una pianificazione del progetto comunica il lavoro da eseguire, le risorse che realizzeranno il lavoro e il calendario in cui il lavoro dovrà essere ultimato. La pianificazione del progetto riflette il lavoro associato alla consegna puntuale del progetto. Uno dei primi passaggi nella fase di inizializzazione del progetto è di realizzare una pianificazione del progetto. Per stabilire una pianificazione del progetto, è necessario creare una struttura di suddivisione del lavoro.  
  
 Crea una struttura del progetto con una struttura di suddivisione del lavoro che consente di:  
  
- Suddividere il lavoro in attività gestibili  
  
- Stimare il tempo necessario per completare un'attività  
  
- Impostare le relazioni tra attività e la durata dell'attività  
  
- Determinare i ruoli richiesti per completare ogni attività  
  
  La pianificazione del progetto nella struttura di suddivisione del lavoro ha un aspetto comune, completo di un diagramma di Gantt interattivo.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Crea una struttura di suddivisione del lavoro per un progetto  
 Crea una struttura di suddivisione del lavoro per rappresentare la sequenza di attività in un progetto. La struttura di suddivisione del lavoro include le attività, i requisiti per ogni attività e le informazioni sui ricavi e i costi. Nella struttura di suddivisione del lavoro, puoi aggiungere:  
  
-   La sequenza di attività in una gerarchia  
  
-   Eventuali altre attività che devono essere completate prima che possa essere avviata un'attività  
  
-   La data di inizio, la data di fine e la durata di un'attività  
  
-   Il numero di ore necessarie per un'attività  
  
-   Qualsiasi competenza e formazione del lavoro richiesta  
  
-   I lavoratori a cui è assegnata un'attività  
  
-   Costi e ricavi stimati  
  
## <a name="task-types"></a>Tipi di attività  
Utilizzerai i seguenti tipi di attività quando si crea la struttura di suddivisione del lavoro:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Nodo radice di progetto** | L'attività di riepilogo di livello superiore per il progetto. Tutte le altra attività di progetto vengono create al di sotto. Il nome dell'attività principale è il nome del progetto. Il lavoro, le date e la durata del nodo radice sono basati sui valori nella gerarchia sottostante. Non puoi modificare le proprietà del nodo radice o eliminare il nodo radice. | 
| **Attività di riepilogo o del contenitore** | Un'attività di riepilogo ha un'attività secondaria sottostante. Un'attività di riepilogo non ha alcun lavoro o costo proprio. Il suo lavoro e il suo costo sono un rollup delle attività secondarie. Puoi modificare il nome di un'attività di riepilogo, ma non puoi modificare il lavoro, le date o la durata, perché vengono calcolate automaticamente. L'eliminazione di un'attività di riepilogo elimina l'attività stessa e le attività secondarie.|  
| **Attività del nodo foglia** | Un'attività del nodo foglia rappresenta il lavoro più dettagliato del progetto. Ha un lavoro stimato, un numero pianificato di risorse, date di inizio e fine pianificate e una durata.|

  
## <a name="task-hierarchy"></a>Gerarchia attività  
 Sono disponibili le opzioni seguenti quando si crea una gerarchia dell'attività:  
  
- **Aggiungi attività**.   Puoi aggiungere un'attività a una posizione scelta nella gerarchia dell'attività. Se non selezioni una posizione, la nuova attività viene visualizzata alla fine.  
  
- **Rientro attività**.   Rientra un'attività per fare in modo che sia figlia dell'attività direttamente al di sopra.  
  
- **Rientro negativo attività**.   Imposti un rientro negativo di un'attività in modo che non sia più un'attività secondaria dell'attività padre originale.  
  
- **Sposta su e sposta giù**.   Sposta le attività in alto e in basso nella gerarchia dell'attività padre. Se si sposta un'attività in alto o in basso non ci sono conseguenze sul lavoro, il costo, le date o la durata.  
  
## <a name="task-attributes"></a>Attributi attività  
 Un nome dell'attività descrive il lavoro che deve essere completato. Utilizza vari attributi dell'attività per descrivere i requisiti di pianificazione e assegnazione del personale per l'attività.  
  
### <a name="schedule-attributes"></a>Attributi di pianificazione

 - Assegna i valori a **Ore di lavoro**, **Numero di risorse**, **Data di inizio**, **Data di fine** e **Durata** per determinare la pianificazione dell'attività. 
 - **Lavoro** è una stima delle ore necessarie per completare l'attività.
 - **Numero di risorse** è una stima che il responsabile di progetto inserisce nell'attività per ottenere la migliore pianificazione possibile. 
 - **Durata** (in giorni) indica il numero di giorni lavorativi che ci vorranno per completare l'attività.  
  
### <a name="staffing-attributes"></a>Attributi di assegnazione del personale

 - **Ruolo**, **Unità organizzativa risorsa**, **Numero di risorse** e **Risorse** descrivono i requisiti di assegnazione del personale per l'attività. 
 - **Ruolo** descrive il tipo di risorsa necessario per eseguire l'attività. 
 - **Unità organizzativa risorsa** indica l'unità organizzativa da cui le risorse devono avere assegnato del personale per questa attività, influisce inoltre sulla stima di costo e vendite dell'attività, poiché viene contabilizzata quando si determina il prezzo di vendita dell'unità per la risorsa. 
 - **Risorse** include una risorsa generica o una risorsa denominata quando ne viene trovata una.  
  
## <a name="task-dependencies"></a>Dipendenze attività  
 Puoi creare relazioni di predecessore tra una o più attività nella struttura di suddivisione del lavoro. Puoi impostare uno o più valori per il campo di predecessore nelle attività per indicare le attività da cui sarà dipendente. Quando assegni un valore di predecessore a un'attività, l'attività può iniziare solo quando tutte le attività predecessore sono state completate. Impostando questa dipendenza in un'attività darà come risultato il ricalcolo della data di inizio pianificata dell'attività come l'ultima fine di tutti i predecessori. Le conseguenze correlate ai predecessori in una pianificazione non sono limitate dalla modalità dell'attività definita nell'attività.  
  
## <a name="task-mode"></a>Modalità attività  
 La modalità attività è uno dei fattori importanti che determinano la pianificazione attività del nodo foglia. Esistono due diverse modalità di attività per ogni attività: la modalità di pianificazione automatica e la modalità di pianificazione manuale.  
  
-   **Pianificazione automatica**.   Quando imposti la modalità di attività su Pianificata automaticamente, il motore di pianificazione dell'attività utilizza le regole di pianificazione nei seguenti attributi di attività per determinare la pianificazione per l'attività:  
  
    -   Attività precedenti  
  
    -   Risorse  
  
    -   Numero di risorse  
  
    -   Date di inizio e fine  
  
-   **Regole di pianificazione**.   La data di inizio di un'attività del nodo foglia privo di impostazioni predefinite dei predecessori alla data di inizio della pianificazione del progetto. La durata di un'attività del nodo foglia viene sempre calcolata come il numero dei giorni lavorativi tra le date di inizio e di fine. Quando un'attività viene pianificata automaticamente, il motore di pianificazione segue le regole riportate di seguito:  
  
    -   Le date di inizio e fine di un'attività devono sempre essere giorni lavorativi in base al calendario della pianificazione del progetto  
  
    -   La data di inizio di un'attività con impostazioni predefinite dei predecessori sull'ultima data di fine dei predecessori  
  
    -   Lavoro = Numero delle persone * Durata * Ore in un giorno lavorativo standard del calendario di progetto  
  
-   **Responsabile pianificazione**.   In alcuni casi, può essere utile deviare dalle regole. In questi casi, puoi impostare la modalità di attività per l'attività da pianificare manualmente. Ciò interrompe il calcolo dei valori da parte del motore di pianificazione per gli attributi di pianificazione. L'impostazione dei predecessori nelle attività influenza sempre la data di inizio dell'attività dipendente.  
  
## <a name="create-a-work-breakdown-structure"></a>Crea una struttura di suddivisione del lavoro  
  
1.  Passa a **Project Service > Progetti**.  
  
2.  Fai clic sul progetto che desideri utilizzare.  
  
3.  Nella barra sulla parte superiore dello schermo, seleziona la freccia in giù accanto al nome del progetto e quindi fai clic sulla Struttura di suddivisione del lavoro.  
  
4.  Per aggiungere un'attività, fai clic su **Aggiungi attività**. Compila i campi per l'attività, quindi fai clic su **Salva**.  
  
5.  Continua ad aggiungere attività fino a che la struttura di suddivisione del lavoro non è stata completata. Durante la creazione della struttura di suddivisione del lavoro, puoi eseguire le operazioni seguenti per organizzare le seguenti:  
  
    -   Seleziona un'attività e fai clic su **Rientro** per spostarla in un'altra attività oppure fai clic su Rientro negativo per spostarlo di un livello.  
  
    -   Seleziona un'attività e fai clic su **Sposta su** o **Sposta giù** per spostarla in alto o in basso nell'elenco.  
  
    -   Fai clic su **Nascondi Gantt** per nascondere il diagramma di Gantt e fai clic su **Mostra Gantt** per visualizzarlo di nuovo.  
  
    -   Seleziona un periodo di tempo diverso per il diagramma di Gantt in **Scala temporale**.  
  
6.  Per aggiungere i ruoli specificati nella struttura di suddivisione del lavoro ai membri del team del progetto, fai clic su **Genera team di progetto**.  
  
7.  Una volta terminato di apportare modifiche, fai clic su **Salva** nell'angolo in basso a destra dello schermo.  
  
### <a name="see-also"></a>Vedi anche  
 [Guida del responsabile di progetto](../psa/project-manager-guide.md)
