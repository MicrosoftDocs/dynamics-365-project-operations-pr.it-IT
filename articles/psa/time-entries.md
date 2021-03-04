---
title: Creare inserimenti ore
description: In questo argomento vengono fornite informazioni su come creare inserimenti ore.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149683"
---
# <a name="create-time-entries"></a>Creare inserimenti ore

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nelle versioni precedenti di Dynamics 365 Project Service Automation, gli inserimenti ore venivano immessi su base settimanale. Nella versione 3 di Project Service Automation, gli inserimenti ore vengono immessi su base giornaliera. Tuttavia, dopo la creazione di alcuni inserimenti, puoi crearli o copiarli in bulk.

## <a name="create-a-time-entry"></a>Creare un inserimento ore

Segui questi passaggi per creare un inserimento ore.

1. Nella pagina **Inserimenti ore**, seleziona **Nuovo**.
2. Nella finestra di dialogo **Creazione rapida: Inserimento ore**, immettere la durata dell'inserimento ore in minuti, ore, o giorni. La durata deve essere immessa nel formato seguente: *x* minuti", *x* ore o *x* giorni. Ore e giorni possono anche essere immessi come valori decimali, ad esempio *x,x* ore o *x,x* giorni.
3. Seleziona il tipo di inserimento ore e il progetto per il quale stai immettendo l'inserimento ore.
4. Nel campo **Attività di progetto**, trova l'attività per questo inserimento ore.

    > [!NOTE]
    > Se stai creando un inserimento ore per un'attività non assegnata a un utente, nel campo **Attività di progetto**, seleziona il pulsante **Cerca**, seleziona **Cambia vista** e quindi **Tutte le attività di progetto attive** per elencare tutte le attività.

5. Immetti una descrizione, se una descrizione è richiesta, quindi seleziona **Salva e chiudi**.

Dopo la creazione e il salvataggio dell'inserimento ore, puoi modificarlo nella griglia degli inserimenti. La griglia degli inserimenti ore supporta due formati:

- Puoi immettere inserimenti ore nel formato **hh:mm**. Questo formato viene quindi convertito in ore e frazioni.
- Puoi immettere ore e frazioni direttamente.

Nota che le frazioni di un'ora non sono minuti. Pertanto, 1,5 ore rappresenta 1 ora e 30 minuti. La stessa regola si applica alle frazioni di un giorno. Un giorno è 24 ore e 0,5 giorni rappresenta 12 ore.

## <a name="bulk-create-time-entries"></a>Creare inserimenti ore in bulk

Dopo la creazione di alcuni inserimenti ore, puoi copiarli per creare ulteriori inserimenti ore in bulk.

1. Nella pagina **Inserimenti ore**, seleziona **Copia settimana**.
2. Nel gruppo di campi **Da periodo**, nei campi **Data di fine** e **Data di inizio**, definisci un intervallo di date da cui copiare gli inserimenti ore.
3. Nel gruppo di campi **Al periodo**, nel campo **Data di inizio**, specifica la data a partire dalla quale creare gli inserimenti ore.
4. Seleziona **Copia** per creare una copia degli inserimenti ore che corrispondono al giorno della settimana specificato nel gruppo di campi **Al periodo**. Ad esempio, l'inserimento ore per il lunedì dell'ultima settimana viene copiata nel lunedì della settimana specificata nel gruppo di campi **Al periodo**.

## <a name="import-data-for-time-entries"></a>Importare dati per inserimenti ore

Puoi importare dati da prenotazioni e assegnazioni di progetto. Quando importi dati, puoi specificare l'intervallo di date delle prenotazioni da importare e quindi selezionare in modo esplicito le prenotazioni che devono essere create come inserimenti ore **Bozza**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Raggruppare, ordinare, cercare e filtrare funzionalità

Puoi raggruppare e filtrare gli inserimenti ore in base alle dimensioni specificate nelle colonne. Nel campo **Raggruppa per**, seleziona la dimensione da utilizzare per filtrare gli inserimenti ore. Puoi anche ordinare record di inserimenti ore in ordine crescente o decrescente utilizzando la freccia di ordinamento nelle intestazioni delle colonne. Inoltre, puoi visualizzare o nascondere gli inserimenti selezionando il pulsante **Filtra** nelle intestazioni delle colonne e quindi immettendo, nella casella **Cerca**, il testo che deve essere utilizzato per cercare inserimenti ore per nome di progetto, attività di progetto, inserimento ore o risorsa.
