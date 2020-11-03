---
title: Prenotare provvisoriamente una risorsa
description: In questo argomento vengono fornite informazioni su come pianificare o prenotare provvisoriamente membri del team di progetto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: cb506a519dbc490ecdd579edf1e3fa5dd0153bdb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079001"
---
# <a name="soft-book-a-resource"></a>Prenotare provvisoriamente una risorsa

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

È possibile pianificare o prenotare provvisoriamente una risorsa di un team di progetto per mostrare che si intende assegnarla al progetto. Le prenotazioni provvisorie non utilizzano la capacità disponibile di una risorsa ed è possibile assegnare membri del team prenotati provvisoriamente ad attività di progetto. Tuttavia, poiché la prenotazione provvisoria non utilizza la capacità di una risorsa, è ancora possibile prenotare definitivamente la risorsa per altre attività nello stesso periodo. Le risorse generiche non possono essere prenotate provvisoriamente e una prenotazione provvisoria non può soddisfare una richiesta di risorse generiche.

I membri del team di progetto prenotati provvisoriamente sono elencati nella scheda **Team** della pagina **Progetto** , con le relative ore di prenotazione provvisoria visualizzate nella colonna **Ore prenotate provvisoriamente** della vista **Membri del team con nome**. I membri del team prenotati provvisoriamente sono elencati anche nella scheda di pianificazione. Poiché sono prenotati provvisoriamente, la scheda di pianificazione non visualizza alcun utilizzo della capacità per tali risorse. Il tempo prenotato provvisoriamente non è visualizzato nella scheda **Riconciliazione** e nemmeno nel campo **Estendi prenotazioni** della scheda **Riconciliazione** nella scheda di pianificazione. 

Vi sono due modi per prenotare provvisoriamente un membro del team per un progetto: direttamente dalla scheda di pianificazione o aggiungendo il membro del team nella scheda **Team**. 

## <a name="soft-book-from-the-schedule-board"></a>Prenotare provvisoriamente dalla scheda di pianificazione
Completare i passaggi seguenti per prenotare provvisoriamente una risorsa dalla scheda di pianificazione. 

1. Aprire la scheda di pianificazione e nel pannello **Requisiti prenotazione** selezionare la scheda **Progetto**.
2. Individuare il progetto per il quale si desidera prenotare provvisoriamente una risorsa. Se l'elenco include un gran numero di progetti, selezionare l'intestazione di colonna **Progetto** e quindi utilizzare i filtri per cercare uno o più progetti.
3. Selezionare il progetto e quindi trascinarlo sulla griglia temporale della risorsa.
5. Nel pannello **Crea prenotazione risorsa** modificare la data di inizio e quella di fine, impostare **Stato di prenotazione** su **Provvisoria** e impostare le ore. 
6. Fare clic su **Prenota**. Ora la risorsa viene visualizzata nella scheda **Team** come risorsa di un progetto. Nella vista **Membri del team con nome** sono visualizzate le ore prenotate provvisoriamente nella colonna **Ore prenotate provvisoriamente**.

> [!NOTE]
> Ora possibile assegnare la risorsa prenotata provvisoriamente alle attività nella scheda **Pianifica**. Nella scheda **Riconciliazione** , la risorsa mostra un disavanzo di prenotazione relativo all'assegnazione dell'attività in quanto la scheda **Riconciliazione** considera soltanto le prenotazioni definitive. È possibile utilizzare la funzionalità **Estendi prenotazioni** per prenotare definitivamente la risorsa ed eliminare il disavanzo delle prenotazioni definitive rispetto alle assegnazioni delle risorse. È necessario annullare manualmente la prenotazione provvisoria per la risorsa utilizzando **Gestisci prenotazioni**.

## <a name="soft-book-on-the-team-tab"></a>Prenotazione provvisoria nella scheda Team

È possibile aggiungere membri del team direttamente nella scheda **Team** e quindi modificarne lo stato di prenotazione da **Definitiva** a **Provvisoria** con **Gestisci prenotazioni**. Quando si aggiunge un membro del team in questo modo, si avrà sempre una prenotazione definitiva salvo se si seleziona **Nessuno** come metodo di allocazione.

Per utilizzare questo metodo, completare la procedura seguente.

1. Nella pagina **Progetto** , nella scheda **Team** , fai clic su **Nuovo**.
2. Selezionare la risorsa prenotabile, il ruolo e le date di inizio e di fine.
3. Selezionare un metodo di allocazione diverso da **Nessuno**.
4. Seleziona **Salva**. La risorsa sarà visualizzata nella griglia e le relative ore nella colonna **Ore prenotate definitivamente**.
5. Gestire le prenotazioni della risorsa selezionando **Gestisci prenotazioni**.
6. Quando la scheda di pianificazione viene aperta, espandere la risorsa per visualizzarne le prenotazioni. La prenotazione sarà indicata come **Definitiva**.
7. Fare clic con il pulsante destro del mouse sulla prenotazione e sotto **Cambia stato** , selezionare **Prenota provvisoriamente** \> **Provvisoria**. Lo stato della prenotazione è ora **Provvisoria**.
8. Dopo la chiusura della scheda di pianificazione, si noterà che le ore della risorsa sono passate dalla colonna **Ore prenotate definitivamente** alla colonna **Ore prenotate provvisoriamente** nella griglia della scheda **Team** della vista **Membri del team con nome**.

> [!NOTE]
> Quando si utilizza **Gestisci prenotazioni** per modificare lo stato da **Definitiva** a **Provvisoria** se si prenota definitivamente una risorsa del team e quindi gli si assegnano delle attività, le assegnazioni delle attività vengono mantenute per quella risorsa. Tuttavia, nella scheda **Riconciliazione** , la risorsa avrà un disavanzo di prenotazione in quanto solo le prenotazioni definitive vengono prese in considerazione durante la riconciliazione delle prenotazioni con le assegnazioni. È possibile utilizzare la funzionalità **Estendi prenotazioni** nella scheda **Riconciliazione** per prenotare definitivamente la risorsa ed eliminare il disavanzo delle prenotazioni definitive rispetto alle assegnazioni delle risorse. Sarà necessario annullare la prenotazione provvisoria per la risorsa utilizzando **Gestisci prenotazioni**.

Quando si è pronti a modificare una risorsa membro del team prenotata provvisoriamente in una risorsa membro del team prenotata definitivamente, procedere come segue:

1. Nella scheda di pianificazione, espandere la risorsa per visualizzarne le prenotazioni. La prenotazione sarà visualizzata come **Provvisoria**.
2. Fare clic con il pulsante destro del mouse sulla prenotazione e in **Cambia stato** selezionare **Prenota definitivamente** \> **Definitiva**. Lo stato della prenotazione è ora **Definitiva**.
3. Dopo la chiusura della scheda di pianificazione, ritornare al progetto e aprire la scheda **Team** , si noterà che le ore della risorsa sono passate dalla colonna **Ore prenotate provvisoriamente** alla colonna **Ore prenotate definitivamente** nella scheda **Team** della vista **Membri del team con nome**. Se la risorsa è stata assegnata alle attività, non mostrerà più un disavanzo di prenotazione nella scheda **Riconciliazione** in quanto le relative prenotazioni ora sono definitive.

