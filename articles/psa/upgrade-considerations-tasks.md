---
title: Considerazioni sull'aggiornamento della struttura di suddivisione del lavoro
description: In questo argomento vengono fornite informazioni sull'aggiornamento della struttura di suddivisione del lavoro da Project Service Automation 2.x a 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 0b75fd372732f42a3557aaa5eccec1f24a644941
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121808"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Considerazioni sull'aggiornamento della struttura di suddivisione del lavoro
In questo argomento vengono fornite informazioni sull'aggiornamento della struttura di suddivisione del lavoro da Project Service Automation 2.x a 3.x. In questo argomento viene definito lo stato di integrità di un progetto in Project Service Automation (PSA) che è necessario per un aggiornamento corretto. Sono inoltre fornite informazioni sulle condizioni di blocco comuni che rendono impossibile l'aggiornamento. Per ulteriori informazioni sulla definizione delle attività di progetto e le relative funzioni in una pianificazione di progetto, vedi [Pianificazioni di progetto](project-creating.md).

## <a name="key-entities"></a>Entità chiave
Per una struttura di suddivisione del lavoro accurata già caricata con le risorse, sono necessarie le entità seguenti:

- [Progetto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Team di progetto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Attività di progetto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Assegnazioni di risorse](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Dipendenza attività di progetto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Risorse prenotabili](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Per definire una struttura di suddivisione del lavoro caricata con risorse, devi completare i passaggi seguenti:

1. Creare un nuovo progetto. Per ulteriori informazioni su come creare un nuovo progetto, vedi [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Creare una o più attività. Per ulteriori informazioni su come creare un'attività, vedi [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definire le dipendenze delle attività. Per ulteriori informazioni, vedere [Dipendenza attività di progetto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Assegnare membri del team di progetto al progetto. Per ulteriori informazioni, vedi l'[msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Assegnare membri del team di progetto alle attività. Per ulteriori informazioni, vedi l'[msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relazioni del team di progetto

Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:
- Tutti i membri del team di progetto devono essere associati a una risorsa prenotabile.
- Tutti i membri del team di progetto devono essere associati allo stesso progetto. 

## <a name="project-task-relationships"></a>Relazioni delle attività di progetto
Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:

- Tutte le attività correlate devono essere associate allo stesso progetto.
- Ogni attività riga deve avere un'attività padre.
- Ogni attività deve avere un progetto padre.

### <a name="valid-conditions"></a>Condizioni valide

- Tutte le durate delle attività devono essere superiori o uguali a (>=) un'ora e inferiori a 1.800.000 minuti (1.250 giorni).*
- Tutte le attività devono avere una data di inizio successiva a 01/01/2000.*
- Tutte le attività devono avere una data di inizio che rientra in un periodo di 17 anni a partire dalla data odierna.*
- Tutte le attività devono avere una data di inizio antecedente o corrispondente alla data di fine.
- Tutti i tipi di transazioni nelle classificazioni (Spese, Materiale, Imposta e Tempo) devono avere valori per **Unità predefinita** e **Unità di vendita**.
- I formati delle date con lettere devono essere evitati.

### <a name="potential-mitigation-steps"></a>Passaggi di mitigazione potenziali
- Utilizzare la ricerca avanzata per identificare le attività del progetto che non contengono un ID progetto.
- Utilizzare la ricerca avanzata per identificare le attività del progetto in cui la durata pianificata è maggiore di >1.800.000.
- Prima di apportare eventuali modifiche ai dati, è necessario esaminare le personalizzazioni associate all'entità che potrebbero aver danneggiato i dati. Queste personalizzazioni devono essere risolte prima di procedere con eventuali aggiornamenti relativi ai dati.
- Per le attività identificate che sono rimaste orfane, considerare la possibilità di eliminare queste attività se non sono necessarie o se devono essere associate al progetto padre corretto.
- Per qualsiasi attività in cui la durata è superiore a 1.250 giorni, prendere in considerazione l'aggiunta di più attività per rappresentare la durata totale, se possibile.

> [!NOTE]
> Le condizioni contrassegnate con un asterisco (\*) presentano limiti dovuti al fatto che Customer Relationship Management (CRM) supporta solo 7.320 espansioni di ricorrenza. È necessario rimanere al di sotto di tale limite.

## <a name="resource-assignment-relationships"></a>Relazioni delle assegnazioni di risorse
Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:

- Tutte le assegnazioni di risorse in una struttura di suddivisione del lavoro devono essere correlate allo stesso progetto.
- Tutte le assegnazioni di risorse in una struttura di suddivisione del lavoro devono essere associate ai membri del team di progetto nello stesso progetto.

### <a name="potential-mitigation-steps"></a>Passaggi di mitigazione potenziali
- Identificare tutte le attività che non rientrano nelle condizioni sopra descritte.  
- Eventuali assegnazioni di risorse non più valide devono essere eliminate.

## <a name="project-task-dependency-relationships"></a>Relazioni delle dipendenze delle attività di progetto
Per assicurare un aggiornamento corretto, le seguenti relazioni devono essere gestite correttamente:

- Tutte le dipendenze delle attività di progetto devono essere correlate allo stesso progetto.
- Non è possibile avere più riferimenti alla stessa dipendenza di un'attività.
