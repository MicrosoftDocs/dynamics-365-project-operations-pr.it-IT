---
title: Come si prenotano provvisoriamente le risorse nell'app versione 2.x?
description: In questo articolo viene descritto come prenotare provvisoriamente i membri del team di progetto con Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18a1176c131e233f62f74dc0dd8a6aa3ee561da5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286028"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Come si prenotano provvisoriamente le risorse nell'app Web (app Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

È possibile pianificare o prenotare provvisoriamente una risorsa di un team di progetto per mostrare che si intende assegnarla a un progetto. Le prenotazioni provvisorie non utilizzano la capacità disponibile di una risorsa. I membri del team prenotati provvisoriamente non possono essere assegnati ad attività di progetto. Solo le risorse il cui stato è Prenotato definitivamente e il tipo di esecuzione è Impegnato possono essere assegnate ad attività (presupponendo che dispongono di ore di prenotazione definitiva sufficienti per coprire l'intervento).

I membri del team di progetto prenotati provvisoriamente sono visualizzati nella griglia Membro del team con le relative ore di prenotazione provvisoria nella colonna Prenota provvisoriamente. Sono visualizzati anche nella scheda di pianificazione. Anche qui, non indicano un utilizzo della capacità in quanto la prenotazione provvisoria non utilizza la capacità di una risorsa.

Vi sono tre modi per prenotare provvisoriamente un membro del team per un progetto con Project Service versione 2.x. È possibile eseguire una prenotazione provvisoria con la scheda di pianificazione, mediante la funzionalità Gestisci prenotazioni oppure creando una risorsa generica. Questi metodi sono descritti di seguito.

## <a name="soft-book-with-the-schedule-board"></a>Prenotare provvisoriamente con la scheda di pianificazione

Per prenotare provvisoriamente con la scheda di pianificazione, utilizzare questa procedura: 
1. Aprire la scheda di pianificazione.
2. Selezionare la scheda Progetto nella parte inferiore del pannello Requisiti prenotazione della scheda di pianificazione.
3. Individuare il progetto per il quale si desidera prenotare provvisoriamente una risorsa. Se si hanno molti progetti, fare clic sull'intestazione della colonna Progetto e quindi utilizzare il filtro per trovare il progetto.
4. Fare clic sul progetto, quindi trascinarlo sulla griglia temporale della risorsa.
5. Viene visualizzato il pannello Crea prenotazione risorsa a destra. Modificare la data di inizio e quella di fine, selezionare lo stato di prenotazione Provvisoria e impostare le ore. 
6. Fare clic su Prenota.
7. La risorsa è ora visualizzata come membro del team con le ore di prenotazione provvisoria nella colonna Prenota provvisoriamente.

Da notare che non è possibile assegnarla ad attività nella struttura di suddivisione del lavoro in quanto le risorse devono essere prenotate definitivamente per il team per essere assegnate.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Prenotare provvisoriamente utilizzando la funzionalità Gestisci prenotazioni

Per prenotare provvisoriamente con Gestisci prenotazioni, utilizzare questa procedura:
1. Nella griglia dei membri del team, fare clic su Nuovo.
2. Selezionare la risorsa prenotabile, il ruolo, le date di inizio e di fine.
3. Selezionare un metodo di allocazione diverso da Nessuno:
- Piena capacità
- Percentuale capacità
- Per ore - Distribuzione uniforme
- Per ore - Spese iniziali
4. Fare clic su Salva. La risorsa sarà visualizzata nella griglia del team e le relative ore sono indicate come Definitiva.
5. Gestire le prenotazioni della risorsa facendo clic su Gestisci prenotazioni.
6. Quando la scheda di pianificazione viene aperta, espandere la risorsa per visualizzarne le prenotazioni. La prenotazione sarà indicata come Definitiva.
7. Fare clic con il pulsante destro del mouse sulla prenotazione, in Cambia stato, selezionare Prenota provvisoriamente e quindi su Provvisoria. Lo stato della prenotazione è ora Provvisoria.
8. Dopo la chiusura della scheda di pianificazione, si noterà che lo stato delle ore della risorsa è passato da Definitiva a Provvisoria nella griglia dei membri del team.
Se si prenota definitivamente una risorsa del team e quindi gli si assegnano delle attività nella struttura di suddivisione del lavoro, quando si utilizza Gestisci prenotazioni per cambiare lo stato da Definitiva a Provvisoria, le assegnazioni saranno rimosse dalle attività per quella risorsa in quanto solo le risorse prenotate definitivamente possono essere assegnate alle attività.

## <a name="soft-book-by-creating-a-generic-resource"></a>Eseguire una prenotazione provvisoria creando una risorsa generica

È possibile creare una prenotazione provvisoria generando un membro del team di risorsa generica, utilizzando la scheda di pianificazione o Richiesta di risorse e modificando il tipo durante la prenotazione.
A questo proposito, utilizzare la procedura seguente:

1. Nella struttura di suddivisione del lavoro del progetto, assegnare dei ruoli alle attività per le quali si intende generare membri del team generici.
2. Fare clic su Genera team di progetto.
3. Nella griglia dei membri del team di progetto, selezionare la risorsa generica e fare clic su Prenota.
4. Nella scheda di pianificazione, selezionare la risorsa che si desidera prenotare.
5. Nel pannello Crea prenotazione risorsa della scheda di pianificazione, modificare lo stato della prenotazione su Provvisoria.
6. Fare clic su Provvisoria o Provvisoria e Esci.

Dopo la chiusura della scheda di pianificazione, la risorsa selezionata sarà aggiunta al team con le ore di prenotazione provvisoria e le ore assegnate. Si noterà inoltre che la risorsa generica rimane nel team come indicatore delle attività assegnate a un membro del team prenotato provvisoriamente.

Quando si è pronti a modificare una risorsa membro del team prenotata provvisoriamente in una risorsa membro del team prenotata definitivamente di modo che sia possibile assegnarla ad attività, procedere come segue:

1. Selezionare quella risorsa e fare clic su Gestisci prenotazioni.
2. Quando la scheda di pianificazione viene aperta, espandere la risorsa per visualizzarne le prenotazioni. La prenotazione sarà contrassegnata come Provvisoria.
3. Fare clic con il pulsante destro del mouse sulla prenotazione e in Cambia stato scegliere selezionare Prenota definitivamente e quindi Definitiva. Lo stato della prenotazione è ora Definitiva.
4. Dopo la chiusura della scheda di pianificazione, si noterà che lo stato delle ore della risorsa è passato da Provvisoria a Definitiva nella griglia dei membri del team. A questo punto, è possibile assegnare la risorsa alle attività (purché esista un allineamento tra le ore prenotate definitivamente e le ore risorsa dell'attività per l'assegnazione). Da notare che se è stato eseguito il passaggio 3 sopra, la modifica dello stato della risorsa prenotabile da Provvisoria a Definitiva comporta la rimozione del membro del team generico dal team.


[!INCLUDE[footer-include](../includes/footer-banner.md)]