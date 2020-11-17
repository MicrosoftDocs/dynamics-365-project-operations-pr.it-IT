---
title: Creare una prenotazione di progetto dalla scheda di pianificazione
description: In questo argomento vengono fornite informazioni su come creare una prenotazione di progetto dalla scheda di pianificazione.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: ccbfedec82b2d9035b51cf1b283ae5c441f1cbcc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122303"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Creare una prenotazione di progetto dalla scheda di pianificazione

È possibile prenotare una risorsa in un progetto direttamente dalla scheda **Team** del progetto o generando un requisito di risorsa da un'assegnazione di membro del team generico e quindi soddisfacendo il requisito generato con un membro del team di progetto.

È inoltre possibile prenotare una risorsa in un progetto direttamente dalla scheda di pianificazione. A questo scopo è possibile procedere in tre modi:

- **Prenotare da un requisito di risorsa generato:** è possibile generare un requisito di risorsa dopo aver creato una risorsa generica e assegnare attività in un progetto.

- **Prenotare dal requisito primario:** i requisiti principali sono visualizzati nella scheda di pianificazione nella scheda **Progetto**. 

- **Prenotare da un nuovo requisito di risorsa:** è possibile creare un requisito di risorsa da zero e associarlo a un progetto. Nella scheda di pianificazione, il requisito di risorsa è visualizzato nella scheda **Apri requisiti**.

## <a name="book-from-a-generated-resource-requirement"></a>Prenotare da un requisito di risorsa generato

È possibile creare una risorsa generica e assegnarla a una o più attività in un progetto. Successivamente, è possibile generare un requisito di risorsa dal membro del team generico. 

1.  Nella scheda di pianificazione, questa risorsa sarà visualizzata nella scheda **Apri requisiti**. I filtri delle colonne nella griglia possono rivelarsi utili se vi sono molti requisiti aperti. 

    ![Scheda Apri requisiti nella scheda di pianificazione](media/FAQ-Project-Booking-Schedule-Board-1.png "Tabella delle prenotazioni e delle assegnazioni")

2. Selezionare il requisito. La scheda **Trova disponibilità** verrà visualizzata nella parte superiore della riga selezionata.
 
3. La selezione della scheda attiva la modalità Assistente di pianificazione della scheda di pianificazione e filtra le risorse disponibili che soddisfano il requisito di risorsa. A questo punto è possibile prenotare una risorsa.

4. È inoltre possibile trascinare la riga selezionata dalla parte inferiore della scheda di pianificazione in una cella della risorsa nella griglia precedente. Viene visualizzato il pannello **Crea prenotazione risorsa** a destra.

    Se si seleziona **Prenota**, la risorsa viene prenotata nel team di progetto.

![Pannello Crea prenotazione risorsa](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Prenotare dal requisito primario

La creazione di un progetto in Project Service crea automaticamente un requisito di risorsa definito requisito primario. Si tratta di un requisito vuoto utilizzato per prenotare rapidamente una risorsa con la scheda di pianificazione senza generare un requisito o crearne uno da zero. Poiché il requisito è vuoto, sarà necessario specificare le date nonché il metodo di allocazione e le ore se applicabile. 

1. Per prenotare una risorsa con il requisito primario, nella scheda di pianificazione, selezionare la scheda **Progetto**. Se esistono più progetti, il filtro della colonna **Progetto** può consentire di trovare più facilmente il progetto desiderato.

   ![Filtri della colonna nella scheda di pianificazione](media/FAQ-Project-Booking-Schedule-Board-2.png "Tabella delle prenotazioni e delle assegnazioni")

2. Selezionare il requisito il cui nome è quello del progetto e la cui durata è zero (0).

3. Selezionare la scheda **Trova disponibilità** visualizzata nella riga selezionata. In questo modo, viene attivata la modalità Assistente di pianificazione della scheda di pianificazione e vengono visualizzate le risorse disponibili che possono essere prenotate per il progetto.

4. Poiché un **requisito primario** è un requisito vuoto con durata zero (0), è necessario impostare la durata nel pannello **Crea prenotazione risorsa** quando si seleziona e prenota una risorsa.

5. È inoltre possibile selezionare il **requisito primario del progetto** nella parte inferiore della scheda di pianificazione e trascinarlo su una risorsa per prenotarla.
 
    Poiché un **requisito primario** è un requisito vuoto con durata zero (0), è necessario impostare la durata nel pannello **Crea prenotazione risorsa** quando si seleziona e prenota una risorsa.
 
    Quando si prenota una risorsa mediante il **requisito primario** nella scheda di pianificazione, lo si aggiunge al team del progetto senza alcuna attività.
 
## <a name="book-from-a-new-resource-requirement"></a>Prenotare da un nuovo requisito di risorsa
Completare i passaggi seguenti per prenotare da un nuovo requisito di risorsa. 

1. Accedere a **Requisiti di risorsa** e selezionare **Nuovo** per creare un nuovo requisito di risorsa.

2. Nella scheda **Progetto**, selezionare un progetto per associare il requisito al progetto.
 
    Nella scheda di pianificazione, questo nuovo requisito è visualizzato come **requisito aperto** che è possibile soddisfare.

3. Prenotare la risorsa per aggiungerla al team di progetto.

4. Ora che la risorsa è prenotata, è necessario assegnare manualmente le attività.

