---
title: Metodi di allocazione delle prenotazioni
description: Questo articolo fornisce informazioni sul funzionamento dei metodi di allocazione delle prenotazioni in Project Operations.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 55bf54ada3150bb42d1d47046ddc7e3a1fd8d192
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912751"
---
# <a name="booking-allocation-methods"></a>Metodi di allocazione delle prenotazioni

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Se si aggiunge un membro del team direttamente a un progetto nella scheda **Team** o si prenota una risorsa per un progetto o requisito nella scheda di pianificazione, sono disponibili alcuni metodi di allocazione delle prenotazioni. Questo articolo descrive il funzionamento di ogni metodo e quale metodo potrebbe portare all'overbooking delle risorse.

## <a name="booking-allocation-methods"></a>Metodi di allocazione delle prenotazioni

Esistono sei metodi di assegnazione delle prenotazioni che puoi utilizzare:

- [Piena capacità](#full)
- [Capacità rimanente](#remaining)
- [Percentuale capacità](#percentage)
- [Ore distribuzione uniforme](#evenly)
- [Ore spese iniziali](#front)
- [Nessuno](#none)

### <a name="full-capacity"></a><a name="full"></a>Piena capacità 
Il metodo Piena capacità prenota l'intera capacità della risorsa per le date di inizio e fine specificate. Ad esempio, se una risorsa ha un calendario impostato per lavorare 8 ore al giorno, per 5 giorni alla settimana, l'impostazione di date di inizio e di fine che coprono 5 giorni lavorativi prenoterà la risorsa per 40 ore. La prenotazione viene eseguita senza considerare la capacità rimanente della risorsa. Se una risorsa è già prenotata per altri progetti durante quel periodo, le 40 ore sono prenotate come ore aggiuntive, che possono potenzialmente condurre all'overbooking.

### <a name="remaining-capacity"></a><a name="remaining"></a>Capacità rimanente
Il metodo Capacità rimanente è disponibile solo quando si prenota direttamente per un progetto utilizzando la scheda di pianificazione. Questo metodo prenota la capacità disponibile della risorsa nell'intervallo di date specificato. Ad esempio, se una risorsa ha una capacità di 40 ore alla settimana ed è già stata prenotata per 10 ore, la prenotazione per la stessa settimana risulta nella prenotazione delle 30 ore di capacità rimanenti per quella settimana.

### <a name="percentage-capacity"></a><a name="percentage"></a>Percentuale capacità
Il metodo Percentuale capacità prenota la risorsa per una percentuale della capacità per le date di inizio e di fine specificate. Ad esempio, se il calendario di una risorsa è impostato per lavorare 8 ore al giorno, per 5 giorni alla settimana, l'impostazione di date di inizio e di fine che coprono 5 giorni lavorativi al 50% della capacità prenoterebbe la risorsa per 20 ore. Le singole prenotazioni giornaliere sono distribuite uniformemente sull'intero periodo, 4 ore al giorno in questo esempio. La prenotazione viene eseguita senza considerare la capacità rimanente della risorsa. Se la risorsa è già prenotata durante quel periodo per altri progetti, le 20 ore sono prenotate come ore aggiuntive, che possono potenzialmente condurre all'overbooking.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Ore distribuzione uniforme
Il metodo Ore distribuzione uniforme prenota la risorsa per un determinato numero di ore, con una distribuzione giornaliera uniforme durante il periodo tra la data di inizio e quella di fine specificate. Ad esempio, se si prenota una risorsa per 20 ore per un periodo di 5 giorni, questo metodo distribuisce uniformemente le 20 ore, ovvero 4 ore al giorno. La prenotazione viene eseguita senza considerare la capacità rimanente della risorsa. Se la risorsa è già prenotata durante quel periodo per altri progetti, le 20 ore sono prenotate come ore aggiuntive, che possono potenzialmente condurre all'overbooking.

### <a name="front-load-hours"></a><a name="front"></a>Ore spese iniziali
Il metodo Ore spese iniziali prenota la risorsa per un determinato numero di ore, applicando spese iniziali alle ore giornaliere durante il periodo tra la data di inizio e quella di fine specificate. Questo metodo utilizza la capacità disponibile della risorsa secondo l'ordine "prima disponibile prima utilizzata". Ad esempio, se la pianificazione lavorativa di una risorsa è 8 ore al giorno, per 5 giorni alla settimana, e la risorsa non ha prenotazioni correnti, la prenotazione della risorsa per 20 ore su un periodo di 5 giorni lavorativi risulta nel modello di prenotazione giornaliero seguente: 

|                           |    Giorno 1    |    Giorno 2    |    Giorno 3    |    Giorno 4    |    Giorno 5    |    Totale    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Prenotazioni esistenti**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Nuova prenotazione**          |    8        |    8        |    4        |    0        |    0        |    20       |

Questo metodo prende in considerazione le prenotazioni esistenti e la capacità disponibile. Ad esempio, se la stessa risorsa è già prenotata per 20 ore nella settimana lavorativa, le nuove prenotazioni utilizzano la capacità rimanente come segue:

|                     | Giorno 1 | Giorno 2 | Giorno 3 | Giorno 4 | Giorno 5 | Totale |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Prenotazioni esistenti** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Nuova prenotazione**       | 0     | 0     | 4     | 8     | 8     | 20    |

Poiché la capacità disponibile viene presa in considerazione, è possibile che venga visualizzato un messaggio di errore se la risorsa non ha capacità rimanente che può essere assorbita dalla prenotazione. Con questo metodo, l'overbooking è impossibile.

### <a name="none"></a><a name="none"></a>Nessuna
Il metodo Nessuna è disponibile solo quando si eseguono prenotazioni dalla scheda **Team** in un progetto. Inoltre, aggiunge la risorsa come membro del team nel progetto, ma non crea prenotazioni che assorbono la capacità della risorsa. Questo metodo è utilizzato quando il membro del team responsabile di progetto predefinito viene aggiunto alla creazione di un progetto. L'utente responsabile di progetto che ha creato il progetto viene aggiunto per impostazione predefinita al progetto, di modo che il record dell'entità di progetto abbia un proprietario e un responsabile approvazione. Poiché questo utente non ha prenotazioni, se si desidera prenotare la risorsa è possibile eliminarla e quindi aggiungerla di nuovo utilizzando un altro metodo di allocazione, oppure aggiungere la risorsa alle attività e quindi utilizzare **Estendi prenotazioni** nella **Riconciliazione** per creare prenotazioni per le assegnazioni.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Metodi di allocazione che portano all'overbooking
Per riepilogare, i seguenti metodi di allocazione portano all'overbooking se la risorsa è già impegnata in altri progetti (o per altri ordini di lavoro o entità pianificabili):

- Piena capacità
- Percentuale capacità
- Ore distribuzione uniforme

Quando si utilizza uno di questi tre metodi di allocazione, non si riceverà una notifica in caso di overbooking della risorsa. Per correggere l'overbooking, sarà necessario utilizzare la scheda di pianificazione.


[!INCLUDE[footer-include](../includes/footer-banner.md)]