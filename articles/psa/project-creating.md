---
title: Pianificazioni di progetto
description: In questo argomento vengono fornite informazioni su come creare una pianificazione.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 8f1a0b0ed610ade094546782a1fa517682a390e4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283997"
---
# <a name="project-schedules"></a>Pianificazioni di progetto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Una pianificazione di progetto comunica il lavoro che deve essere completato, le risorse che realizzeranno il lavoro e l'intervallo di tempo entro il quale il lavoro deve essere ultimato. La pianificazione riflette il lavoro associato alla consegna puntuale del progetto. In Dynamics 365 Project Service Automation si crea una pianificazione di progetto suddividendo il lavoro in attività gestibili, stimando il tempo necessario per eseguire ogni attività, impostando le dipendenze delle attività e le durate delle attività, e stimando le risorse generiche che eseguiranno le attività. La pianificazione di progetto viene creata nella scheda **Pianificazione** della pagina del progetto.
 
## <a name="tasks"></a>Attività

Il primo passaggio consiste nel creare una pianificazione di progetto per suddividere il lavoro in parti gestibili. La pianificazione in PSA supporta le seguenti funzionalità:

- Nodo radice di progetto
- Attività di riepilogo o del contenitore
- Attività del nodo foglia

### <a name="project-root-node"></a>Nodo radice di progetto

Il nodo radice del progetto è l'attività di riepilogo di primo livello per il progetto. Tutte le altra attività di progetto vengono create al di sotto. Il nome del nodo radice è sempre il nome del progetto. Il lavoro richiesto, le date e la durata del nodo radice sono riepilogati in base ai valori nella gerarchia sottostante. Non puoi modificare le proprietà del nodo radice e nemmeno il nodo radice.

### <a name="summary-or-container-tasks"></a>Attività di riepilogo o del contenitore 

Le attività di riepilogo hanno attività secondarie o del contenitore. A queste attività non sono associati lavoro richiesto o costi. Il lavoro richiesto e il costo di queste attività sono invece un rollup del lavoro richiesto e del costo delle relative attività contenitore. La data di inizio dell'attività di riepilogo è la data di inizio delle attività contenitore e la data di fine è la data di fine delle attività contenitore. Il nome di un'attività di riepilogo può essere modificato, ma le proprietà di pianificazione (lavoro richiesto, date e durata) non possono essere modificate. Se elimini un'attività di riepilogo, elimina anche tutte le relative attività contenitore.

### <a name="leaf-node-tasks"></a>Attività del nodo foglia

Le attività del nodo foglia rappresentano il lavoro più dettagliato del progetto. Queste hanno un lavoro richiesto stimato, risorse, date di inizio e fine pianificate e una durata.
 
## <a name="creating-a-task-hierarchy"></a>Creazione di una gerarchia di attività

Puoi creare una gerarchia di attività utilizzando le seguenti opzioni:

- Pulsante **Aggiungi attività**
- Pulsante **Rientro attività**
- Pulsante **Rientro negativo attività**
- Pulsanti **Sposta su** e **Sposta giù**.
- Tasti di scelta rapida e accessibilità

### <a name="add-task"></a>Aggiungi attività

Il pulsante **Aggiungi attività** ti consente di creare una nuova attività nella gerarchia. Se non selezioni una posizione, l'attività viene inserita alla fine. 

Un ID pianificazione è assegnato a ogni attività. L'ID pianificazione rappresenta il livello e la posizione dell'attività nella gerarchia. Utilizza una numerazione con struttura. Per le attività nel primo livello sotto il nodo radice del progetto, viene utilizzato uno schema di numerazione con 1, 2, 3 e così via. Per le attività sotto il primo livello, viene utilizzato uno schema di numerazione con 1.1, 1.2, 1.3 e così via.

### <a name="indent-task"></a>Rientro attività

Quando a un'attività viene applicato un rientro, diventa un'attività figlio dell'attività soprastante. L'ID pianificazione dell'attività viene quindi ricalcolato di modo che sia basato sull'ID pianificazione del suo nuovo padre e segua lo schema di numerazione con struttura. L'attività padre è ora un'attività di riepilogo o un'attività contenitore. Pertanto, diventa un rollup delle relative attività figlio.

### <a name="outdent-task"></a>Rientro negativo attività 

Quando a un'attività viene applicato un rientro negativo, non è più un'attività figlio di quella che era la sua attività padre. L'ID pianificazione viene quindi ricalcolato di modo che rifletta il livello e la posizione aggiornati dell'attività nella gerarchia. Il lavoro richiesto, il costo e le date dell'attività padre precedente vengono ricalcolati di modo che non includano questa attività.

### <a name="move-up-and-move-down"></a>Sposta su e sposta giù 

I pulsanti **Sposta giù** e **Sposta su** cambiano la posizione di un'attività nella relativa gerarchia padre. Le modifiche di questo tipo non influiscono sul lavoro richiesto, il costo, le date o la durata dell'attività. Solo l'ID di pianificazione dell'attività viene influenzato. L'ID pianificazione viene ricalcolato di modo che rifletta la nuova posizione dell'attività nell'elenco di attività figlio dell'attività padre.

### <a name="accessibility-and-keyboard-shortcuts"></a>Tasti di scelta rapida e accessibilità

La griglia **Pianificazione** è completamente accessibile e può essere utilizzata con utilità per la lettura dello schermo, ad esempio Narrator, JAWS o NVDA. Puoi spostarti nell'area della griglia utilizzando i tasti di direzione (come in Microsoft Excel), utilizzare il tasto TAB per avanzare negli elementi dell'interfaccia utente interattiva e il tasto FRECCIA GIÙ, il tasto INVIO o la BARRA SPAZIATRICE per selezionare e visualizzare i menu a discesa. Anche le intestazioni di colonna sono interattive. Puoi nascondere e rendere visibili le colonne, utilizzare il tasto TAB e i tasti di direzione per spostarti tra le intestazioni di colonna e utilizzare i pulsanti di azione nella barra degli strumenti. Inoltre, puoi utilizzare i seguenti tasti di scelta rapida:

- **Aggiornare**: ALT+MAIUSC+F5
- **Eliminare**: ALT+MAIUSC+INS
- **Eliminare**: ALT+MAIUSC+CANC
- **Spostare su/giù**: ALT+MAIUSC+FRECCIA SU/GIÙ
- **Rientro/rientro negativo**: ALT_MAIUSC+freccia SINISTRA/DESTRA
- **Espandere/comprimere gerarchie**: ALT+MAIUSC+tasti Più/Meno

## <a name="task-attributes"></a>Attributi attività

Il nome di un'attività descrive il lavoro che deve essere completato. In PSA, gli attributi associati a un'attività descrivono la pianificazione dell'attività e i relativi requisiti di assegnazione del personale.

> ![Attributi attività](media/project-2.png)
 
### <a name="schedule-attributes"></a>Attributi di pianificazione

Gli attributi **Lavoro richiesto**, **Data di inizio**, **Data di fine** e **Durata** definiscono la pianificazione dell'attività.

Ulteriori attributi di pianificazione includono:

- **Ore lavoro richiesto**: immetti una stima delle ore necessarie per completare l'attività. 
- **Durata**: specifica il numero di giorni lavorativi necessari per completare l'attività.
- **ID pianificazione**: questo ID generato automaticamente viene utilizzato per ordinare le attività nella gerarchia. Le dipendenze tra le attività gestiscono l'ordine effettivo in cui le attività vengono eseguite.
 
### <a name="staffing-attributes"></a>Attributi di assegnazione del personale

Agli attributi di assegnazione del personale si accede tramite il campo **Risorse** nella pianificazione. Puoi cercare una risorsa esistente oppure fare clic su **Crea** e nel riquadro **Creazione rapida**, aggiungere un membro del team di progetto come nuova risorsa.

I campi **Ruolo**, **Unità gestione risorse** e **Nome posizione** sono utilizzati per descrivere i requisiti di assegnazione del personale per l'attività. Questi attributi, insieme alla pianificazione dell'attività, sono utilizzati per trovare le risorse disponibili per eseguire l'attività.

**Ruolo** - Specifica il tipo di risorsa necessaria per eseguire l'attività.

**Unità gestione risorse** - Specifica l'unità dalla quale assegnare le risorse per l'attività. Questo attributo influenza la stima di vendita e costo per l'attività se il tasso di costo e fatturazione per la risorsa sono impostati in base alle unità di gestione risorse.

**Nome posizione** - Immetti un nome descrittivo per la risorsa generica che funge da segnaposto per la risorsa che eseguirà il lavoro.

Il campo **Risorse** contiene il nome di posizione della risorsa generica o della risorsa denominata quando una è disponibile.

Il campo **Categoria** include i valori che indicano un tipo di lavoro più ampio in cui è possibile raggruppare l'attività. Questo campo non ha alcun effetto sulla pianificazione o sull'assegnazione del personale. Viene utilizzato solo per la creazione di report.

### <a name="task-dependencies"></a>Dipendenze attività 

Puoi utilizzare la pianificazione in PSA per creare relazioni predecessore tra attività. Il campo **Predecessore** sotto **Attività** utilizza uno o più valori per indicare le attività da cui dipende un'attività. Quando i valori di predecessore sono assegnati a un'attività, l'attività può iniziare solo dopo che tutte le attività predecessore sono state completate. A causa della dipendenza, la data di inizio pianificata dell'attività viene impostata sulla data di completamento delle attività predecessore.

La modalità di attività non influisce sugli aggiornamenti delle date di inizio e fine delle attività predecessore/dipendenti.

## <a name="task-mode"></a>Modalità attività 

La modalità di attività determina la pianificazione delle attività del nodo foglia. PSA supporta due diverse modalità di attività per ogni attività: pianificazione automatica e pianificazione manuale.

### <a name="auto-scheduling"></a>Pianificazione automatica 
 
Quando la modalità di attività è impostata su **Pianificata automaticamente** per un'attività, il motore di pianificazione delle attività utilizza le regole di pianificazione negli attributi di attività per determinare la pianificazione per l'attività:

#### <a name="scheduling-rules"></a>Regole di pianificazione

Per impostazione predefinita, se un'attività del nodo foglia è priva di predecessori, la relativa data di inizio viene impostata sulla data di inizio pianificata del progetto. La durata di un'attività del nodo foglia viene sempre calcolata come il numero dei giorni lavorativi tra le date di inizio e di fine. Quando un'attività viene pianificata automaticamente, il motore di pianificazione segue queste regole:

- Le date di inizio e fine dell'attività devono sempre essere giorni lavorativi in base al calendario della pianificazione del progetto. 
- Peer qualsiasi attività con attività predecessore, la data di inizio viene impostata automaticamente sulla data di fine più recente dei relativi predecessori.
- Il lavoro richiesto viene calcolato utilizzando la formula: Numero di persone × Durata × Ore in un giorno lavorativo standard nel calendario di progetto.

### <a name="manual-scheduling"></a>Pianificazione manuale

Se le regole di pianificazione automatica non soddisfano i requisiti, puoi impostare la modalità di attività per l'attività su **Pianificata manualmente**. Questa impostazione interrompe il calcolo dei valori di altri attributi di pianificazione da parte del motore di pianificazione. Indipendentemente dalla modalità di attività, l'impostazione di predecessori per le attività influenza sempre la data di inizio dell'attività dipendente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]