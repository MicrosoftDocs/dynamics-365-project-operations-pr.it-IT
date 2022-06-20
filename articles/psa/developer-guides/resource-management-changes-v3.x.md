---
title: Modifiche alla gestione delle risorse (Project Service Automation 3.x)
description: In questo articolo vengono fornite informazioni sulle modifiche all'area Gestione risorse.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cac11606811632bdc48f462eb3a09a163ba1620d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916017"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Modifiche alla gestione delle risorse (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Le sezioni di questo articolo forniscono informazioni sulle modifiche apportate all'area Gestione risorse di Dynamics 365 Project Service Automation versione 3.x.

## <a name="project-estimates"></a>Stime di progetto

Anziché essere basate sull'entità **msdyn\_projecttask** (**Attività di progetto**), le stime di progetto sono basate sull'entità **msdyn\_resourceassignment** (**Assegnazione risorse**). Le assegnazioni delle risorse sono diventate un'"origine di riferimento" per la pianificazione delle attività e la determinazione dei prezzi.

## <a name="line-tasks"></a>Attività riga

In PSA 3.x, le attività riga sono obsolete (deprecate). Le assegnazioni ora puntano all'intera attività anziché alle righe attività.

Nell'esempio seguente viene illustrato come un'attività denominata "Attività di test" viene assegnata ai membri del team A e B nelle versioni precedenti di PSA e in PSA 3.x.

- **Prima di PSA 3.x:**

    - Attività di test

        - Attività di test - Attività riga 1

            - Assegnazione a A

        - Attività di test - Attività riga 2

            - Assegnazione a B

- **PSA 3.x:**

    - Attività di test

        - Assegnazione a A
        - Assegnazione a B

## <a name="unassigned-assignment"></a>Assegnazione non assegnata

In PSA 3.x, un'assegnazione non assegnata è un'assegnazione che viene assegnata a un membro del team **NULL** e a una risorsa **NULL**. È possibile avere assegnazioni non assegnate in un paio di scenari:

- Se un'attività è stata creata, ma non è ancora stata assegnata a un membro del team, viene sempre creata un'assegnazione non assegnata. 
- Se tutti gli assegnatari di un'attività vengono rimossi, un'attività non assegnata viene ricreata per quell'attività.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Pianificare campi nell'entità Attività di progetto

I campi dell'entità **msdyn\_projecttask** sono stati deprecati o spostati nell'entità **msdyn\_resourceassignment**, oppure vi si fa riferimento dall'entità **msdyn\_projectteam** entity (**Membro del team di progetto**).

| Campo deprecato in msdyn\_projecttask (Attività di progetto) | Nuovo campo in msdyn\_resourceassignment (Assegnazione risorse) | Commento |
|---|---|---|
| msdyn\_assignedresources | Nessuna | |
| msdyn\_assignedteammembers | Nessuna | |
| msdyn\_numberofresources | Nessuna | |
| msdyn\_scheduledhours | Nessuna | |
| msdyn\_effortcontour | msdyn\_plannedwork | Il formato di una struttura di dati JavaScript Object Notation (JSON) archiviato nel campo è stato modificato. |

## <a name="schedule-contour"></a>Profilo di pianificazione

Il profilo di pianificazione è archiviato nel campo **Lavoro pianificato** (**msdyn\_plannedwork**) di ogni entità **Assegnazione risorse** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struttura

La nuova struttura del profilo di pianificazione presenta periodi di tempo flessibili definiti per ogni giorno della pianificazione. Ogni periodo di tempo ha le proprietà seguenti:

- **Inizio** - L'inizio delle ore lavorative del giorno, a seconda del calendario di progetto.
- **Fine** - La fine delle ore lavorative del giorno, a seconda del calendario di progetto.
- **Ore** - Il numero di ore assegnate in un giorno.

**Esempio**

In questo esempio viene utilizzato un calendario di progetto in cui il giorno lavorativo è dalle 9 alle 17 nel fuso orario UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Pianificazione automatica e pianificazione manuale

Se un'attività viene pianificata automaticamente, le ore sono caricate in anticipo e la durata dell'attività potrebbe essere ridotta.

**Esempio**

L'attività seguente è pianificata automaticamente per 18 ore su tre giorni (dal 3 dicembre 2018 al 5 dicembre 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Se un'attività viene pianificata manualmente, le ore sono distribuite uniformemente a tutte le date.

**Esempio**

L'attività seguente è pianificata manualmente per 18 su tre giorni (dal 3 dicembre 2018 al 5 dicembre 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unità assegnazione

L'unità assegnazione è stata deprecata in PSA 3.x. Le ore di lavoro richiesto dell'attività sono ora divise equamente, per giorno, tra tutte le risorse assegnate.

**Esempio**

In questo esempio, l'attività viene assegnata a due risorse e viene pianificata automaticamente per 36 ore su tre giorni (dal 3 dicembre 2018 al 5 dicembre 2018).

- Assegnazione 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Assegnazione 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensioni di determinazione dei prezzi

In PSA 3.x, i campi delle dimensioni di determinazione dei prezzi specifici delle risorse (come **Ruolo** e **Unità organizzativa**) sono stati rimossi dall'entità **msdyn\_projecttask**. Questi campi possono ora essere recuperati dal membro del team di progetto corrispondente (**msdyn\_projectteam**) dell'assegnazione delle risorse (**msdyn\_resourceassignment**) quando vengono generate le stime di progetto. Un nuovo campo, **msdyn\_organizationalunit**, è stato aggiunto all'entità **msdyn\_projectteam**.

| Campo deprecato in msdyn\_projecttask (Attività di progetto) | Al suo posto viene utilizzato il campo msdyn\_projectteam (Membro del team di progetto) |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Profili di distribuzione

I campi del profilo di stima e di determinazione dei prezzi sono stati deprecati nell'entità **msdyn\_projecttask** . Sono stati spostati nell'entità **msdyn\_resourceassignment**.

| Campo deprecato in msdyn\_projecttask (Attività di progetto) | Nuovo campo in msdyn\_resourceassignment (Assegnazione risorse) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

I campi seguenti sono stati aggiunti all'entità **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

I campi seguenti per costi e vendite pianificati, effettivi e rimanenti rimangono invariati nell'entità **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
