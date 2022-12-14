---
title: Creare assegnazioni di risorse
description: Questo articolo fornisce informazioni sulla creazione di assegnazioni di risorse generiche e denominate.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811998"
---
# <a name="create-resource-assignments"></a>Creare assegnazioni di risorse

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


Un'assegnazione di risorse è l'associazione diretta di un membro del team di progetto a un'attività del nodo foglia. Questo articolo fornisce informazioni sui diversi modi per assegnare le risorse.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Creare un membro del team generico mediante l'assegnazione di attività


Quando crei un membro del team generico tramite l'assegnazione di attività, crei un segnaposto o una risorsa generica. Questa risorsa generica descrive le caratteristiche della risorsa denominata che desideri utilizzare per le attività. Successivamente generi un requisito (o invii una richiesta utilizzando il requisito) che viene utilizzato per cercare e prenotare la risorsa denominata.

1. Nella griglia Pianificazione di un'attività, seleziona l'icona Risorsa nella cella della **risorsa**.
2. Digita un nome da utilizzare come nome della risorsa segnaposto. Ad esempio, "Program Manager".
3. Seleziona **Crea** e nel campo **Creazione rapida: membro del team di progetto**, imposta il ruolo per la risorsa generica.
4. Assegna le attività a questa risorsa segnaposto selezionando la risorsa nel **selettore delle risorse** per l'attività. Le risorse elencate in **Membri del team**.
5. Dopo l'assegnazione della risorsa generica, seleziona la risorsa generica nella scheda **Team** e quindi **Genera requisito** per creare un requisito di risorsa per la risorsa generica.
6. Seleziona **Prenota** per la risorsa generica e utilizza la scheda di pianificazione per trovare e prenotare una risorsa reale. Puoi anche inviare il requisito che deve essere soddisfatto da un responsabile delle risorse.
7. Quando la risorsa generica è completamente soddisfatta con una risorsa denominata, la risorsa generica viene rimossa dal team. L'adempimento parziale dei requisiti delle risorse non comporterà un'assegnazione di risorse. Le assegnazioni di attività per la risorsa generica vengono assegnate alla risorsa denominata che ha soddisfatto il requisito di risorse della risorsa generica.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Assegnare una risorsa denominata dall'elenco di tutte le risorse prenotabili

Puoi utilizzare la casella di ricerca nel **selettore delle risorse** per cercare tutte le risorse prenotabili attive in Project Service e assegnarle a un'attività del nodo foglia. Le risorse assegnate questo modo sono aggiunte al team senza alcuna prenotazione. Ciò equivale ad aggiungere un membro del team e a selezionare **Nessuno** come metodo di allocazione. La risorsa è visualizzata nelle schede **Team**, **Assegnazione risorse** e **Riconciliazione** come risorse con soltanto assegnazioni e un disavanzo di prenotazione. Prenotare se desideri utilizzarne la relativa disponibilità.

1. Dalla griglia delle attività, dalla bacheca o dalla sequenza temporale, vai alla cella **Assegnato a**.
2. Nella casella di ricerca, inizia a digitare un nome. I risultati della ricerca per il nome sono visualizzati nel **selettore delle risorse** in **Altre risorse**.
3. Seleziona la risorsa che desideri assegnare all'attività o seleziona il nome della risorsa sotto **Altre risorse del team**.

## <a name="editing-resource-assignment-contours"></a>Modifica dei profili di assegnazione delle risorse

Per impostazione predefinita, quando le risorse vengono assegnate a un'attività nella pianificazione, il loro impegno viene distribuito linearmente a ciascuna risorsa, in base all'orario di lavoro della risorsa e alla modalità di pianificazione del progetto. Un responsabile di progetto può utilizzare la griglia di assegnazione delle risorse per perfezionare le stime dell'impegno di ogni risorsa assegnata a una o più attività nelle diverse scale temporali. Questa funzionalità aiuta i responsabili di progetto a produrre stime di costi e vendite più accurate, che sono guidate dai profili di assegnazione delle risorse che vengono generati quando una risorsa viene assegnata a un'attività. Inoltre, i responsabili di progetto possono riflettere più facilmente la domanda di risorse necessaria per creare la domanda in un requisito di risorsa.

### <a name="navigation"></a>Navigazione

Per accedere alla griglia di modifica del profilo, il responsabile di progetto seleziona prima la scheda **Attività** nella pagina principale del progetto e poi seleziona la scheda **Assegnazioni**.

![Scheda Assegnazioni nella scheda Attività della pagina principale del progetto.](media/AssignmentGrid.png)

La griglia supporta due metodi di raggruppamento: **raggruppa per risorsa** e **raggruppa per attività**. A differenza della vista griglia, le colonne non sono configurabili. Le uniche colonne visibili sono **Assegnato a**, **Nome attività**, **Inizio assegnazione**, **Fine assegnazione**, e **Impegno assegnazione**.

Quando la griglia viene inizialmente sottoposta a rendering, inizia dal primo profilo di assegnazione. Se la tua pianificazione non contiene assegnazioni che richiedono impegno, la griglia sarà vuota e non visualizzerà nulla.

![Griglia di assegnazione vuota.](media/emptyassignmentgrid.png)

Se desideri visualizzare i tuoi profili e diverse scale temporali, sono disponibili anche la griglia di assegnazione delle risorse di sola lettura e la griglia di riconciliazione delle risorse.

### <a name="resource-calendars"></a>Calendari delle risorse

La possibilità di modificare un profilo per un giorno specifico è regolata dai giorni lavorativi della risorsa, come indicato nel relativo calendario. Se una cella è disabilitata per una determinata risorsa, quella risorsa non ha giorni lavorativi in quel periodo.

I profili di una risorsa possono estendersi oltre le date di inizio e fine correnti dell'attività assegnata. Se un profilo viene aggiornato in modo che sia successivo all'ultima data di fine di un'attività o alla prima data di inizio di un'attività, la data di fine o la data di inizio dell'attività verrà modificata in modo appropriato. Tuttavia, se un profilo viene aggiornato in modo che sia precedente alla data di inizio di un'attività collegata a un predecessore, l'aggiornamento avrà esito negativo perché l'assegnazione attiverà l'avvio dell'attività prima del completamento del suo predecessore e tale comportamento non è attualmente supportato.

### <a name="co-authoring"></a>Creazione condivisa

Le modifiche alla griglia di assegnazione delle risorse si riflettono automaticamente in tutte le visualizzazioni associate, incluse le visualizzazioni grafico, sequenza temporale, bacheca e griglia. Se più utenti stanno esaminando il progetto contemporaneamente, tutte le modifiche apportate da un utente si rifletteranno nella griglia. Viceversa, qualsiasi modifica apportata nella griglia di assegnazione delle risorse verrà mostrata a tutti gli altri utenti che stanno visualizzando il progetto nella stessa sessione.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
