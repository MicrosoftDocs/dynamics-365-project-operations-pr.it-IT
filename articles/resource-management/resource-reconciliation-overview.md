---
title: Panoramica della riconciliazione risorse
description: In questo argomento vengono fornite informazioni su come verificare che le prenotazioni di risorse e le assegnazioni ai progetti siano allineate.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897456"
---
# <a name="resource-reconciliation-overview"></a>Panoramica della riconciliazione risorse

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Per i membri del team, prenotazioni e assegnazioni non sono strettamente vincolate. In altre parole, le risorse possono avere assegnazioni ma nessuna prenotazione oppure prenotazioni ma nessuna assegnazione. Idealmente, prenotazioni e assegnazioni devono essere allineate, di modo che le risorse abbiano una capacità impegnata per eseguire le assegnazioni di attività. Tuttavia, le prenotazioni possono essere basate sulla disponibilità e le tempistiche inerenti alle attività possono cambiare con l'avanzamento del progetto. Di conseguenza, l'associazione non vincolante di prenotazioni e assegnazioni fornisce flessibilità.

La scheda **Riconciliazione** del modulo **Progetto** consente ai responsabili di progetto di riconciliare le prenotazioni dei membri del team e le relative assegnazioni per il team di progetto.

La scheda **Riconciliazione** inoltre mostra prenotazioni e assegnazioni fino al livello della singola assegnazione di attività per ogni membro del team. Le ore vengono visualizzate nelle celle che rappresentano periodi di tempo da mesi fino a giorni.

La scheda mostra inoltre un totale netto globale per il progetto insieme a una colonna **Totale**.

Per ogni risorsa, la scheda calcola la differenza tra le prenotazioni del membro del team e un rollup delle assegnazioni di attività di quel membro. Idealmente, questa differenza dovrebbe essere 0 (zero). In altre parole, non dovrebbe esserci alcuna differenza tra prenotazioni e assegnazioni. Le differenze sono colorate e ombreggiate per attirare l'attenzione su due condizioni:

- **Prenotazione insufficiente** - Una prenotazione insufficiente si ha quando una risorsa ha più assegnazioni che prenotazioni. Poiché tale capacità non è stata riservata, è possibile che un responsabile di progetto voglia correggere tale condizione estendendo le prenotazioni della risorsa per compensare la mancanza.
- **Prenotazioni in eccesso** - Si hanno prenotazioni in eccesso quando una risorsa è stata prenotata per il progetto ma non è stata assegnata ad attività. Questa condizione può essere accettabile nei casi in cui la risorsa è stata prenotata per il progetto prima dell'assegnazione di attività. Tuttavia, in altri casi, la risorsa non viene pianificata per essere assegnata ad attività. In tali casi, il responsabile di progetto deve prendere in considerazione la possibilità di annullare le prenotazioni della risorsa di modo che la capacità possa essere utilizzata per un altro progetto.

In alcuni casi, quando visualizzi il tempo a un livello superiore al livello del giorno (ad esempio a livello del mese), puoi osservare una differenza netta pari a zero per una risorsa (in altre parole, prenotazioni = assegnazioni). Tuttavia, se visualizzi il tempo a livello della settimana, è possibile che vi siano assegnazioni di 0 (zero) ore e prenotazioni di 40 ore nella prima settimana, ma assegnazioni di 40 ore e prenotazioni di 0 (zero) ore nella seconda settimana. Globalmente, le prenotazioni e le assegnazioni vengono riconciliate, ma differiscono da una settimana all'altra.

Quando visualizzi il tempo a livelli superiori, le celle nella scheda **Riconciliazione** presentano un indicatore che informa dell'esistenza di differenze a livelli inferiori. Facendo doppio clic su una cella, puoi fare zoom in avanti per visualizzare la differenza. Fai clic con il pulsante destro del mouse per fare zoom indietro. Selezionando una risorsa e quindi utilizzando il controllo **Differenza successiva** puoi passare alla differenza successiva tra prenotazioni e assegnazioni per quella risorsa. Per tornare alla differenza precedente, utilizza il controllo **Differenza precedente**. Puoi anche disattivare l'indicatore di differenza e il comportamento di navigazione in **Impostazioni**.


Se sono presenti assegnazioni di attività per una risorsa ma nessuna prenotazione, nella pagina **Progetti**, nella scheda **Riconciliazione**, seleziona la prenotazione insufficiente e quindi seleziona **Estendi prenotazione**. Viene visualizzata la finestra di dialogo **Estendi prenotazione** che mostra la prenotazione necessaria per compensare la mancanza della risorsa. Mostra inoltre le prenotazioni esistenti della risorsa in tutti i progetti o altre entità pianificabili. Se selezioni **OK** per creare la prenotazione della risorsa, indipendentemente dalla disponibilità di quella risorsa, è possibile che si abbia una sovraprenotazione.

Il responsabile di progetto o il responsabile delle risorse può quindi utilizzare la scheda di pianificazione per gestire situazioni in cui una risorsa è sovraprenotata aldilà della sua capacità.

