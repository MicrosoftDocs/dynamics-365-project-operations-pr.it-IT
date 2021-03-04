---
title: Assegnare una risorsa a un‘attività
description: In questo argomento vengono fornite informazioni su come assegnare risorse ad attività.
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
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149998"
---
# <a name="assign-a-resource-to-a-task"></a>Assegnare una risorsa a un‘attività

[!include [banner](../includes/psa-now-project-operations.md)]

Vi sono tre modi di assegnare una risorsa ad un'attività in Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Prenotare una risorsa come membro del team e quindi assegnarla a un'attività

Puoi aggiungere una risorsa al team di progetto e quindi assegnarla risorsa alle attività nella pianificazione del progetto.

1. Nella scheda **Membro del team**, aggiungi un nuovo membro del team selezionando **Nuovo**. 

2. Viene aperto il pannello **Creazione rapida: Membro del team di progetto** dove puoi selezionare il nome della risorsa prenotabile e impostare un ruolo. 

    Seleziona uno dei seguenti metodi di allocazione per la prenotazione della risorsa:

    - **Piena capacità** prenota l'intera capacità della risorsa per le date di inizio e fine specificate.
    - **Percentuale capacità** prenota la risorsa per una percentuale della capacità della risorsa per le date di inizio e di fine specificate.
    - **Per ore - Distribuzione uniforme** prenota la risorsa per un determinato numero di ore, con una distribuzione giornaliera uniforme durante il periodo tra la data di inizio e quella di fine specificate.
    - **Per ore - Spese iniziali** prenota la risorsa per un determinato numero di ore, applicando spese iniziali alle ore giornaliere durante il periodo tra la data di inizio e quella di fine specificate.
    - **Nessuno** aggiunge la risorsa al team ma non crea prenotazioni che assorbono la capacità della risorsa.

3. Nella griglia **Pianificazione** di un'attività, seleziona l'icona **Risorsa** nella cella della risorsa e quindi sotto **Membri del team** seleziona il membro del team appena aggiunto. 

> [!NOTE]
> Nelle schede **Membro del team** e **Riconciliazione**, la risorsa mostra le ore prenotate e quelle assegnate. Le ore dovrebbero essere uguali, ma non è necessario in quanto prenotazioni e assegnazioni non sono strettamente associate. La scheda **Riconciliazione** fornisce i dettagli quando sono differenti, ad esempio, quando a una risorsa si assegnano più ore di quelle prenotate. Se necessario, puoi correggere le informazioni estendendo le prenotazioni della risorsa o modificando l'assegnazione.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Creare un membro del team generico mediante l'assegnazione di attività

Quando crei un membro del team generico mediante l'assegnazione di attività, crei una risorsa segnaposto o generica che descrive le caratteristiche della risorsa denominata che desideri utilizzare per le attività. Successivamente generi un requisito (o invii una richiesta utilizzando il requisito) che viene utilizzato per cercare e prenotare la risorsa denominata.

1. Nella griglia **Pianificazione** di un'attività, seleziona l'icona **Risorsa** nella cella della risorsa.

2. Digita un nome da utilizzare come nome della risorsa segnaposto. Ad esempio, "Program Manager".

3. Seleziona **Crea** e nel campo **Creazione rapida: membro del team di progetto**, imposta il ruolo per la risorsa generica.

4. Puoi continuare ad assegnare attività a questa risorsa segnaposto selezionando la risorsa nel **selettore delle risorse** per l'attività. Le attività sono elencate in **Membri del team**.

5. Dopo l'assegnazione della risorsa generica, seleziona la risorsa generica nella scheda **Team** e quindi **Genera requisito** per creare un requisito di risorsa per la risorsa generica.

6. Seleziona **Prenota** per la risorsa generica. Puoi quindi utilizzare la scheda di pianificazione per trovare e prenotare una risorsa reale. Puoi anche inviare il requisito che deve essere soddisfatto da un responsabile delle risorse.

7. Quando la risorsa generica viene soddisfatta con una risorsa denominata, la risorsa generica viene rimossa dal team e le assegnazioni delle attività per la risorsa generica sono assegnate alla risorsa denominata che ha soddisfatto il requisito di risorsa della risorsa generica.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Assegnare una risorsa denominata dall'elenco di tutte le risorse prenotabili

Puoi utilizzare la casella di ricerca nel **selettore delle risorse** per cercare tutte le risorse prenotabili in Project Service e assegnarle a un'attività.

Le risorse assegnate questo modo sono aggiunte al team senza alcuna prenotazione. Ciò equivale ad aggiungere un membro del team e a selezionare Nessuno come metodo di allocazione. La risorsa è visualizzata nelle schede **Team** e **Riconciliazione** come risorse con soltanto assegnazioni e un disavanzo di prenotazione. Prenotare se desideri utilizzarne la relativa disponibilità.

1. Nella griglia **Pianificazione** di un'attività, seleziona l'icona **Risorsa** nella cella della risorsa.

2. Inizia a digitare un nome. I risultati della ricerca per il nome sono visualizzati nel **selettore delle risorse** in **Altre risorse**.

3. Seleziona la risorsa a cui desideri assegnare l'attività.

