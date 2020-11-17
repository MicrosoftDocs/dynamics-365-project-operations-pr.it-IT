---
title: Prenotazioni di risorse e correlazione tra queste e le assegnazioni di attività
description: In questo argomento vengono fornite informazioni sulla gestione di risorse denominate, prenotazioni di risorse e assegnazioni di attività e sulla correlazione tra le stesse.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: c4b976b49bd643bc7a774a86b1ba89bd76d7c916
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125004"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Prenotazioni di risorse e correlazione tra queste e le assegnazioni di attività


Le risorse denominate possono essere prenotate per un team di progetto e assegnate ad attività di progetto in due modi:

- La risorsa può essere prenotata direttamente in un progetto e quindi assegnata ad attività di progetto.
- Le attività possono essere assegnate ad una risorsa generica, che viene quindi utilizzata per trovare e sostituire la risorsa generica con una risorsa denominata. 

In entrambi i casi, l'azione di prenotazione della risorsa prenota la capacità della risorsa.

Il responsabile di progetto che pianifica il progetto è proprietario del piano e della pianificazione del progetto. Utilizzando la risorsa generica per l'assegnazione e quindi generando una richiesta di risorsa dalla stessa, il responsabile di progetto può prenotare risorse nel progetto con i profili specificati nel piano di progetto. Può prenotare risorse in un progetto e quindi assegnarle ad attività, ma non è possibile allineare i profili delle prenotazioni a quelli delle attività. Le prenotazioni non alterano la pianificazione di progetto.

Si consideri un progetto complesso con molteplici attività che si sovrappongono e dove più risorse dello stesso tipo devono essere utilizzate simultaneamente. Se a una risorsa è assegnato un profilo che è diverso dall'aggregazione delle relative attività, è difficile modificare le attività per adattare il profilo delle prenotazioni alle relative attività discrete e ai relativi profili originali.

Nell'esempio seguente, il lavoro totale richiesto dalla stessa risorsa di un set di quattro attività è 62 ore su un periodo di due settimane ed è presente uno specifico profilo. Se la risorsa Bob è prenotata per 62 ore durante le stesse due settimane ma con un profilo differente, il requisito e le prenotazioni sono allineati.

| **Profili di attività**    | **Ore totali** | Lu 4/6 | Ma 5/6 | Me 6/6 | Gi 7/6 | Ve 8/6 | Sa 9/6 | Do 10/6 | Lu 11/6 | Ma 12/6 | Me 13/6 | Gi 14/6 | Ve 15/6 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Attività 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Attività 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Attività 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Attività 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totali**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Disponibilità di Bob
| **Prenotazione risorsa** | **Ore totali** | Lu 4/6 | Ma 5/6 | Me 6/6 | Gi 7/6 | Ve 8/6 | Sa 9/6 | Do 10/6 | Lu 11/6 | Ma 12/6 | Me 13/6 | Gi 14/6 | Ve 15/6 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Tuttavia, non c'è un modo sistematico di assegnare il profilo di ore prenotate alle attività su base giornaliera. Se il responsabile di progetto è disposto a modificare la pianificazione del progetto in base alla disponibilità della risorsa, deve rimuovere l'assegnazione e rivedere tutte le attività per la corrispondenza con i profili di prenotazione.

Nel caso in cui un'organizzazione ha assegnato l'attività di pianificazione di un progetto a un responsabile di progetto e a un responsabile delle risorse, il primo imposta la pianificazione e ciò include la creazione di profili per il lavoro richiesto. Il responsabile delle risorse non deve poter modificare la pianificazione senza l'approvazione del responsabile di modificare i profili di lavoro durante la prenotazione di risorse effettive. Se il responsabile delle risorse soddisfa altre richieste rispetto a quelle del responsabile di progetto, devono accordarsi sulle modifiche necessarie nella pianificazione del progetto.

Poiché prenotazioni e assegnazioni non sono strettamente associate, è possibile prenotare profili che sono differenti dai profili delle attività o modificare le assegnazioni per generare situazioni in cui prenotazioni e assegnazioni non sono allineate.

La **vista Riconciliazione** che consente al responsabile di progetto di visualizzare prenotazioni e assegnazioni per ogni membro del team di progetto. La vista utilizza colori e ombreggiature per indicare la mancata corrispondenza tra prenotazioni e assegnazioni dei membri di un team. In base a queste informazioni, il responsabile di progetto può effettuare delle correzioni per estendere le prenotazioni delle risorse per i casi in cui sono presenti assegnazioni ma nessuna prenotazione oppure per annullare le prenotazioni dove le risorse sono prenotate ma non hanno assegnazioni.

> [!NOTE]
> Se si sposta un'attività a cui si sono assegnati personalmente dei profili, questi profili non vengono gestiti. I profili vengono rigenerati in base al calendario del progetto per includere le modifiche alle ore lavorative e alle festività. Questo comportamento è predefinito in quanto il sistema non conosce l'intenzione del profilo originale e non può determinare se è logico mantenerlo in un nuovo periodo di tempo. Poiché prenotazioni e attività non sono associate, le prenotazioni mantengono i profili di prenotazione originali. In tal caso, sarà necessario annullare e prenotare di nuovo il nuovo profilo di assegnazione.

