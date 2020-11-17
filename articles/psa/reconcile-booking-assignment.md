---
title: Riconciliare prenotazioni e assegnazioni
description: In questo argomento vengono fornite informazioni su valori effettivi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: f5255b4aa2c6c8b7fa7320da2e10b2ed23a88fdd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120458"
---
# <a name="reconcile-bookings-and-assignments"></a>Riconciliare prenotazioni e assegnazioni

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Le prenotazioni di progetto e le assegnazioni di attività di progetto di un membro del team di progetto non sono strettamente vincolate. Pertanto, una risorsa può avere assegnazioni di attività che non corrispondono a prenotazioni e prenotazioni che non corrispondono ad assegnazioni di attività. Idealmente, le prenotazioni e le assegnazioni di progetto sono allineate, di modo che le risorse abbiano la capacità impegnata per eseguire le relative assegnazioni di attività. Tuttavia, in realtà, le prenotazioni possono essere eseguite in base alla disponibilità e le tempistiche delle attività possono cambiare durante il ciclo di vita del progetto. Di conseguenza, la debole associazione tra prenotazioni e assegnazioni consente una certa flessibilità.

Per questo motivo, l'entità Progetto include una scheda **Riconciliazione**. Questa scheda consente ai responsabili di progetto di riconciliare le prenotazioni dei membri del team e le relative assegnazioni per il team di progetto.

Per ogni membro del team denominato, la scheda **Riconciliazione** mostra prenotazioni e assegnazioni fino al livello della singola attività. Visualizza le ore nelle celle che possono rappresentare periodi da mesi a giorni.

Nel campo **Scala cronologica**, puoi selezionare **Mese**, **Settimana** o **Giorno**. L'impostazione predefinita è **Settimana**. Tuttavia, puoi modificare il valore predefinito selezionando il pulsante **Impostazioni**. Quando la scheda **Riconciliazione** viene aperta, visualizza la data corrente, ma puoi utilizzare il controllo calendario per spostarti a una data antecedente o successiva. Quando un progetto ha una data di inizio nel futuro, la tabella visualizza quella data quando viene aperta. Il controllo calendario include inoltre opzioni che ti consentono di passare alla date di inizio e di fine del progetto.

Puoi utilizzare i controlli dell'espansore in ogni risorsa per visualizzare i dettagli delle prenotazioni della risorsa. Puoi anche espandere le assegnazioni di ogni risorsa fino al livello della singola attività.

Nella parte inferiore della scheda **Riconciliazione** è visualizzato un totale netto globale per il progetto e la scheda include anche una colonna Totale. Per ogni risorsa, la scheda calcola la differenza tra le prenotazioni di un membro del team nel progetto e il rollup delle assegnazioni di attività di quel membro. Idealmente, la differenza è 0 (zero). In altre parole, non dovrebbe esserci differenza tra le prenotazioni della risorsa e le relative assegnazioni di attività. Le eventuali differenze sono colorate e presentano un'ombreggiatura per evidenziare due condizioni:

- **Prenotazione insufficiente** - Le prenotazioni sono insufficienti quando una risorsa ha più assegnazioni che prenotazioni. Poiché questa capacità non è stata riservata, un responsabile di progetto può correggere tale condizione estendendo le prenotazioni della risorsa per compensare l'insufficienza.
- **Prenotazioni in eccesso** - Si hanno prenotazioni in eccesso quando una risorsa è stata prenotata per il progetto ma non è stata assegnata ad attività. Questa condizione può essere accettabile se, ad esempio, la risorsa è stata prenotata prima dell'assegnazione di attività. Tuttavia, in altri casi, la risorsa può non essere pianificata per l'assegnazione alle attività. In tali casi, il responsabile di progetto deve prendere in considerazione la possibilità di annullare le prenotazioni della risorsa di modo che la capacità possa essere utilizzata per un altro progetto.

> [!NOTE]
> La legenda per queste condizioni può essere nascosta per lasciare più spazio disponibile per la griglia. In questo caso, rendi la legenda visibile selezionando il pulsante **Impostazioni**.

In alcuni casi, quando il campo **Scala cronologica** è impostato su un livello superiore a **Giorno**, le differenze possono essere pari a 0 (zero). Ad esempio, nel livello **Mese**, la differenza netta per una risorsa può essere 0 (zero) a indicare che le prenotazioni eguagliano le assegnazioni. Tuttavia, osservando il livello **Settimana**, puoi notare che vi sono assegnazioni di 0 (zero) ore e prenotazioni di 40 ore nella prima settimana del mese e assegnazioni di 40 ore e prenotazioni di 0 (zero) ore nella seconda settimana del mese. Sebbene le prenotazioni e le assegnazioni totali per il mese siano uguali, differiscono per settimana.

Quando visualizzi livelli di tempo superiori, nelle celle della scheda **Riconciliazione** viene visualizzato un indicatore che informa dell'esistenza di differenze nei livelli di tempo inferiori. Ad esempio, nell'illustrazione seguente, un indicatore di cella è visualizzato nella cella del mese di ottobre 2018 per la risorsa Elisa Lombardi. Pertanto, puoi vedere che, anche se le prenotazioni e le assegnazioni della risorsa sono uguali quando vengono aggregate al livello **Mese**, non corrispondono ai livelli inferiori.

![Prenotazioni e assegnazioni non corrispondenti a livello di mese](media/reconcile-assignments-01.JPG)

Fai doppio clic su una cella per eseguire uno zoom avanti fino al livello inferiore successivo e visualizzare la differenza. Ad esempio, se fai doppio clic sulla differenza di ottobre 2018 per Elisa Lombardi, esegui il drill-down fino al livello **Settimana**. Puoi quindi osservare che la risorsa ha prenotazioni di 16 ore ma nessuna assegnazione nelle prime due settimane di ottobre e 16 ore di assegnazioni ma nessuna prenotazione nella terza settimana di ottobre.

![Prenotazioni e assegnazioni non corrispondenti a livello di settimana](media/reconcile-assignments-02.JPG)

Puoi fare clic con il pulsante destro del mouse su una cella per eseguire uno zoom indietro fino al livello superiore successivo. Puoi inoltre disattivare l'indicatore di cella selezionando il pulsante **Impostazioni**. 

Puoi utilizzare i pulsanti **Precedente** e **Successivo** sopra la griglia per passare da una differenza all'altra nel progetto. Per utilizzare questi pulsanti, devi innanzitutto selezionare una risorsa. Seleziona **Successivo** per passare alla differenza successiva tra prenotazioni e assegnazioni per quella risorsa. Seleziona **Precedente** per passare alla differenza precedente.

Nei casi in cui vi sono assegnazioni di attività per una risorsa ma non prenotazioni, puoi selezionare Prenotazione insufficiente e quindi **Estendi prenotazione**. Puoi quindi vedere la prenotazione che è necessaria per risolvere l'insufficienza. Puoi anche visualizzare le prenotazioni della risorsa nel progetto corrente e in altri progetti. Seleziona **OK** per creare la prenotazione per la risorsa indipendentemente dalla disponibilità corrente. Il responsabile di progetto o il responsabile delle risorse può quindi utilizzare la scheda di pianificazione per gestire situazioni in cui una risorsa risulta sovraprenotata a causa dell'estensione delle relative prenotazioni.

## <a name="managing-with-time-zones"></a>Gestione con i fusi orari
Per garantire risultati accurati e prevedibili quando si utilizza Estendi prenotazione, ci sono due prerequisiti chiave che devono essere soddisfatti:  

- L'utente deve configurare il fuso orario del proprio dispositivo affinché corrisponda al fuso orario definito nelle impostazioni di personalizzazione del sistema.
 
  ![Impostazioni di fuso orario in Windows 10](media/reconcile-assignments-03.png)

  ![Impostazioni di fuso orario nelle impostazioni di personalizzazione](media/reconcile-assignments-04.png)
 
- La risorsa prenotabile deve avere almeno un minuto di orario di lavoro che si sovrappone ai profili utilizzati per definire l'estensione richiesta. Ad esempio, l'esempio seguente mostra le risorse di revisione con orari di lavoro che cadono tra le 9:00 e le 19:00. 

  ![Confronto dei profili delle risorse](media/reconcile-assignments-05.png)

La tabella seguente mostra:

- Un modello di calendario di progetto.
- Risorsa A: questa risorsa ha lo stesso calendario ed è nello stesso fuso orario del progetto. L'ora di inizio delle prenotazioni sarà alle 9:00.
- Risorse B: questa risorsa si trova in un fuso orario diverso rispetto al progetto e pertanto inizia alle 7:00 nel suo fuso orario. Tuttavia, le prenotazioni inizieranno alle 9:00 in quanto è il primo orario di inizio del profilo dell'assegnazione.
- Risorse C e D: le risorse si trovano in fusi orari diversi, entrambi diversi tra loro e dal progetto e le prenotazioni iniziano non prima dei rispettivi orari di inizio disponibili.

|Entità  |Calendario  |
|-|-|
|Modello di calendario di progetto   | ![calendario di progetto](media/reconcile-assignments-06.png) |
|Risorsa A  | ![Calendario della risorsa A](media/reconcile-assignments-06.png) |
|Risorsa B  |  ![Calendario della risorsa B](media/reconcile-assignments-07.png) |
|Risorsa C  |  ![Calendario della risorsa C](media/reconcile-assignments-08.png) |
|Risorsa D  | ![Calendario della risorsa D](media/reconcile-assignments-09.png)  |
 
Quando si accede alla visualizzazione di riconciliazione, verranno visualizzate le assegnazioni delle risorse e le relative insufficienze di prenotazione.
 ![Visualizzazione di riconciliazione prima dell'estensione](media/reconcile-assignments-10.png)

Dopo che la funzionalità di estensione della prenotazione è stata eseguita su ciascuna risorsa, le prenotazioni vengono estese correttamente per ogni risorsa. Questo perché le ore lavorative di ciascuna risorsa si sovrappongono ai profili dell'insufficienza.
 ![Visualizzazione di riconciliazione dopo l'estensione della prenotazione](media/reconcile-assignments-11.png) 

Tuttavia, uno sguardo più attento ai dettagli delle prenotazioni mostra differenze nell'orario di inizio delle prenotazioni. Le prenotazioni inizieranno non prima dell'orario di inizio del profilo di assegnazione e non prima dell'orario di inizio disponibile della risorsa.
 ![Nuove prenotazioni delle risorse nella scheda di pianificazione](media/reconcile-assignments-12.png)
