---
title: Creare una struttura di suddivisione del lavoro
description: Questo argomento spiega come creare una struttura di suddivisione del lavoro comprensiva dei controlli di base nella nuova interfaccia di pianificazione.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841358"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Creare una struttura di suddivisione del lavoro

Una pianificazione di progetto comunica il lavoro che deve essere completato, le risorse che realizzeranno il lavoro e l'intervallo di tempo entro il quale il lavoro deve essere terminato. La pianificazione riflette il lavoro associato alla consegna puntuale del progetto. In Dynamics 365 Project Operations, crei una pianificazione di progetto:

  - Suddividendo il lavoro in attività gestibili.
  - Stimando il tempo necessario per eseguire ciascuna attività.
  - Impostando le dipendenze delle attività.
  - Impostando la durata delle attività.
  - Stimando le risorse generiche che svolgeranno le attività. 

La pianificazione di progetto viene creata nella scheda **Pianificazione** della pagina **Progetto**.

## <a name="tasks"></a>Attività

Il primo passaggio consiste nel creare una pianificazione di progetto per suddividere il lavoro in parti gestibili. La pianificazione in Project Operations supporta le seguenti funzionalità:

- Attività di riepilogo o del contenitore
- Attività del nodo foglia

### <a name="summary-tasks"></a>Attività di riepilogo

Le attività di riepilogo possono archiviare altre attività di riepilogo o attività del nodo foglia. A queste attività non sono associati lavoro richiesto o costi. Il lavoro richiesto e il costo di queste attività sono invece un rollup del lavoro richiesto e del costo delle relative attività contenitore. La data di inizio dell'attività di riepilogo è la data di inizio delle attività contenitore e la data di fine è la data di fine delle attività contenitore. Il nome di un'attività di riepilogo può essere modificato, ma le proprietà di pianificazione, tra cui lavoro richiesto, date e durata, non possono essere modificate. Se elimini un'attività di riepilogo, elimina anche tutte le relative attività contenitore.

### <a name="leaf-node-tasks"></a>Attività del nodo foglia

Le attività del nodo foglia rappresentano il lavoro più dettagliato del progetto. Queste hanno un lavoro richiesto stimato, risorse, date di inizio e fine pianificate e una durata.

## <a name="create-a-task-hierarchy"></a>Creare una gerarchia di attività

### <a name="add-a-task"></a>Aggiungere un'attività

Completa la procedura seguente per aggiungere una o più attività.

1. Vai a **Progetti** e seleziona e apri il record del progetto per il quale vuoi creare una pianificazione. 
2. Seleziona la scheda **Attività**. 
3. Seleziona **Aggiungi nuova attività**, inserisci un nome per l'attività, quindi premi Invio.
2. Immetti un altro nome di attività e premi nuovamente Invio finché l'elenco delle attività non è completo.

### <a name="manage-hierarchy-of-a-task"></a>Gestire la gerarchia di un'attività

Quando a un'attività viene applicato un rientro, diventa un'attività figlio dell'attività soprastante. L'ID pianificazione dell'attività viene quindi ricalcolato di modo che sia basato sull'ID pianificazione del suo nuovo padre e segua lo schema di numerazione con struttura. L'attività padre è ora un'attività di riepilogo. Pertanto, diventa un rollup delle relative attività figlio. Quando a un'attività viene alzata di livello, non è più un'attività figlio di quella che era la sua attività padre. L'ID pianificazione viene quindi ricalcolato di modo che rifletta il livello e la posizione aggiornati dell'attività nella gerarchia. Il lavoro richiesto, il costo e le date dell'attività padre precedente vengono ricalcolati di modo che non includano questa attività.

Completa la procedura seguente per abbassare o alzare di livello un'attività.

1. Nella pagina **Progetto**, nella scheda **Attività** sotto **Attività di riepilogo**, seleziona i tre punti verticali accanto al nome dell'attività, quindi seleziona **Converti a sottoattività**. 
2. Seleziona l'attività da abbassare o alzare di livello. Per selezionare più di un'attività, seleziona un'attività, tieni premuto CTRL, quindi seleziona le altre attività.
2. Seleziona **Imposta come livello di struttura inferiore** o **Promuovi attività secondaria** per inserire o togliere le attività dalle attività di riepilogo.

### <a name="move-tasks-up-and-down"></a>Spostare le attività su e giù

Le attività possono essere spostate a qualsiasi livello nella struttura di suddivisione del lavoro in due modi:

- Seleziona una o più attività e trascinale nella posizione desiderata.
- Seleziona una o più attività, fai clic con il tasto destro e seleziona **Taglia**, seleziona la cella di destinazione nella pianificazione, quindi fai clic con il pulsante destro del mouse e seleziona **Incolla**.

## <a name="task-attributes"></a>Attributi attività

Il nome di un'attività descrive il lavoro che deve essere completato. In Project Operations, gli attributi associati a un'attività descrivono la pianificazione dell'attività e i relativi requisiti di assegnazione del personale.

## <a name="schedule-attributes"></a>Attributi di pianificazione

Gli attributi **Lavoro richiesto**, **Data di inizio**, **Data di fine** e **Durata** definiscono la pianificazione dell'attività.

La tabella seguente mostra gli attributi di pianificazione aggiuntivi.

| **Nome visualizzato finale** | **Descrizione finale** |
| --- | --- |
| Lavoro completato (ore) | Lavoro completato per l'attività in ore. |
| Durata | Visualizza la durata dell'attività espressa in giorni. |
| Lavoro totale | Lavoro totale per l'attività in ore. |
| Fine | Data e ora di fine. |
| % completamento | Percentuale di completamento dell'attività. |
| Bucket di progetto | La scheda attività può essere raggruppata per bucket in modo che ogni bucket abbia la propria colonna. |
| Lavoro rimanente (ore) | Lavoro rimanente per l'attività in ore. |
| Venga avviato | Data e ora di inizio. |
| Nome | Nome dell'attività. |
| ID | L'ID dell'attività nella struttura di suddivisione del lavoro. |

## <a name="staffing-attributes"></a>Attributi di assegnazione del personale

Agli attributi di assegnazione del personale si accede tramite il campo **Risorse** nella pianificazione. Puoi cercare una risorsa esistente oppure selezionare **Crea** e nel riquadro **Creazione rapida** aggiungere un membro del team di progetto come nuova risorsa.

I campi **Ruolo**, **Unità gestione risorse** e **Nome posizione** sono utilizzati per descrivere i requisiti di assegnazione del personale per l'attività. Questi attributi, insieme alla pianificazione dell'attività, sono utilizzati per trovare le risorse disponibili per eseguire l'attività.

   - **Ruolo**: Specifica il tipo di risorsa necessaria per eseguire l'attività.
   - **Unità gestione risorse**: Specifica l'unità dalla quale assegnare le risorse per l'attività. Questo attributo influenza la stima di vendita e costo per l'attività se il tasso di costo e fatturazione per la risorsa sono impostati in base alle unità di gestione risorse.
   - **Nome posizione**: Immetti un nome per la risorsa generica che funge da segnaposto per la risorsa che eseguirà il lavoro.

Il campo **Risorse** contiene il nome di posizione della risorsa generica o della risorsa denominata quando una è disponibile.

Il campo **Categoria** include i valori che indicano un tipo di lavoro più ampio in cui è possibile raggruppare l'attività. Questo campo non ha alcun effetto sulla pianificazione o sull'assegnazione del personale. Il campo viene utilizzato solo per i rapporti.

## <a name="task-dependencies"></a>Dipendenze attività

Puoi utilizzare la pianificazione in Project Operations per creare relazioni predecessore tra attività. Il campo **Predecessore** utilizza uno o più valori per indicare le attività da cui dipende un'attività. Quando i valori di predecessore sono assegnati a un'attività, l'attività può iniziare solo dopo che tutte le attività predecessore sono state completate. A causa della dipendenza, la data di inizio pianificata dell'attività viene impostata sulla data di completamento delle attività predecessore.

La modalità di attività non influisce sugli aggiornamenti delle date di inizio e fine delle attività predecessore/dipendenti.

## <a name="accessibility-and-keyboard-shortcuts"></a>Tasti di scelta rapida e accessibilità

La griglia **Pianificazione** è completamente accessibile e può essere utilizzata con utilità per la lettura dello schermo, ad esempio Narrator, JAWS o NVDA. Puoi spostarti nell'area della griglia utilizzando i tasti di direzione (come in Microsoft Excel), utilizzare il tasto TAB per avanzare negli elementi dell'interfaccia utente interattiva e il tasto FRECCIA GIÙ, il tasto INVIO o la BARRA SPAZIATRICE per selezionare e aprire i menu a discesa.
