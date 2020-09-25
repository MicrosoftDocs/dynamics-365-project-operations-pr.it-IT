---
title: Prenotare provvisoriamente requisiti
description: In questo argomento vengono fornite informazioni su come prenotare provvisoriamente i requisiti.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 97323b73-c6de-4a7f-b889-19d4c42cf17a
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 08a8b46ee03fb93b30d178756e38c3086880f774
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752723"
---
# <a name="soft-book-requirements"></a>Prenotare provvisoriamente requisiti

Un requisito di risorsa può essere prenotato definitivamente. Una prenotazione definitiva crea una proposta che consuma la capacità di una risorsa. La proposta viene quindi rispedita al richiedente per l'approvazione. Una prenotazione provvisoria aggiunge una risorsa a un team di progetto e ha uno stato differente nella scheda di pianificazione, ma non consuma la capacità della risorsa. Per prenotare provvisoriamente una risorsa nella scheda di pianificazione, imposta il campo **Stato di prenotazione** su **Provvisoria**.

![Stato di prenotazione impostato su Provvisoria](media/Resource-Management-image77.png)

Quando la scheda **Team** è visualizzata nella vista **Membri del team con nome**, la risorsa è visualizzata in quella scheda. Le ore prenotate provvisoriamente sono indicate nella colonna **Ore prenotate provvisoriamente**.

![Ore prenotate provvisoriamente nella vista Membri del team con nome](media/Resource-Management-image78.png)

I membri del team prenotati provvisoriamente possono essere assegnati ad attività.

![Membro del team prenotato provvisoriamente assegnato a un'attività](media/Resource-Management-image79.png)

Nella scheda **Riconciliazione**, le prenotazioni di una risorsa prenotata provvisoriamente non sono visualizzate in quanto la scheda **Riconciliazione** considera solo le prenotazioni definitive.

![Risorsa prenotata provvisoriamente senza prenotazioni nella scheda Riconciliazione](media/Resource-Management-image80.png)

> [!NOTE]
> Non è possibile prenotare provvisoriamente una risorsa a partire da un requisito generato da un membro del team generico.

Nella scheda di pianificazione, le prenotazioni provvisorie per una risorsa sono indicate con un colore differente.

![Prenotazioni provvisorie nella scheda di pianificazione](media/Resource-Management-image81.png)

Per convertire una prenotazione provvisoria in una definitiva, nella scheda di pianificazione fai clic con il pulsante destro del mouse sulla prenotazione provvisoria e quindi scegli **Cambia stato** \> **Prenota definitivamente** \> **Definitiva**.

![Modificare lo stato della prenotazione in Definitiva](media/Resource-Management-image82.png)

La prenotazione e lo stato vengono modificati nella scheda di pianificazione. Poiché lo stato della prenotazione è ora **Definitiva**, la risorsa è visualizzata come prenotata e le relative capacità e disponibilità vengono rettificate.

Puoi utilizzare lo stesso metodo per annullare una prenotazione definitiva o provvisoria nella scheda di pianificazione.

Per convertire una risorsa prenotata provvisoriamente in una prenotata definitivamente nella scheda **Team** del progetto, seleziona la risorsa e quindi **Conferma**.

![Comando Conferma](media/Resource-Management-image83.png)