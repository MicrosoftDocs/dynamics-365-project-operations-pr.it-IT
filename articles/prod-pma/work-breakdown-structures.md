---
title: Panoramica delle strutture di suddivisione del lavoro
description: Una struttura di suddivisione del lavoro è una descrizione del lavoro che sarà completato per un progetto. È una gerarchia di attività che rappresenta la comprensione da parte del team di progetto della composizione del lavoro e delle dimensioni, dei costi e della durata di ogni componente o attività.
author: Yowelle
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d0cfcc27c69695fc6fe897e798b2831528833e6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078851"
---
# <a name="work-breakdown-structures-overview"></a>Panoramica delle strutture di suddivisione del lavoro

[!include [banner](../includes/banner.md)]

Una struttura di suddivisione del lavoro è una descrizione del lavoro che sarà completato per un progetto. È una gerarchia di attività che rappresenta la comprensione da parte del team di progetto della composizione del lavoro e delle dimensioni, dei costi e della durata di ogni componente o attività. Una struttura di suddivisione del lavoro ha tre scopi principali:

-   Descrivi la suddivisione o la composizione del lavoro nelle attività.
-   Pianifica il lavoro del progetto.
-   Stima il costo di ogni attività.

Il grado di dettaglio in una struttura di suddivisione del lavoro dipende dal livello di accuratezza richiesto nelle stime e dal livello di monitoraggio richiesto a fronte di tali stime. I progetti che hanno una tolleranza molto bassa per gli slittamenti nella pianificazione o nei costi di solito richiedono una struttura di suddivisione del lavoro più dettagliata e un monitoraggio diligente dell'avanzamento del lavoro e dei costi rispetto a fronte della struttura di suddivisione del lavoro. Questo tipo di progetto è comune nei settori dell'edilizia e dell'ingegneria. 

Al contrario, i progetti in settori come i media e la pubblicità, il software e l'infrastruttura IT tendono ad essere unici e la produttività è relativa all'esperienza e alla competenza dell'individuo che esegue l'attività. Pertanto, questi settori utilizzano una struttura di suddivisione del lavoro per ottenere un'approssimazione delle dimensioni di un progetto, non per tenere traccia dell'avanzamento di quel progetto in dettaglio. 

La creazione di una struttura di suddivisione del lavoro è un processo intenso che di solito viene svolto per un lungo periodo e che richiede collaborazione e informazioni da un'ampia varietà di persone. Questo argomento descrive come utilizzare i miglioramenti della struttura di suddivisione del lavoro per soddisfare i requisiti di stima e monitoraggio.

## <a name="prerequisites-for-creating-a-wbs"></a>Prerequisiti per la creazione di una struttura di suddivisione del lavoro
Per creare una struttura di suddivisione del lavoro, devi essere in grado di creare un programma di lavoro e stimare il costo del lavoro.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Prerequisiti per la creazione di un programma di lavoro

Per utilizzare le funzionalità di pianificazione complete delle funzionalità di struttura di suddivisione del lavoro, completa la seguente configurazione:

1.  Configura un calendario predefinito e un calendario del progetto:
    1.  Fai clic su **Gestione progetti e contabilità** &gt; **Imposta** &gt; **Parametri Gestione progetti e contabilità** &gt; **Pianificazione**. Nel campo **Calendario di lavoro predefinito** , specifica un calendario predefinito. Questo sarà il calendario di lavoro predefinito per ogni nuovo progetto creato.
    2.  Puoi modificare il calendario predefinito per un progetto specifico. Fai clic sulla pagina dei dettagli del progetto e quindi nella Scheda dettaglio **Team progetto e programmazione** , aggiorna il campo **Calendario di programmazione** selezionando un altro calendario.

2.  Configura giorni lavorativi e orari di lavoro standard. Il calendario impostato come calendario di lavoro per il progetto verrà utilizzato nella struttura di suddivisione del lavoro per determinare le seguenti informazioni:

-   Giorni lavorativi e festivi
-   Il numero di ore di lavoro in un giorno

Per configurare i giorni lavorativi e l'orario di lavoro per un calendario o per creare un nuovo calendario, fai clic su **Amministrazione organizzazione** &gt; **Comune** &gt; **Calendari**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Prerequisiti per la stima del costo del lavoro

Per utilizzare le funzionalità complete di stima dei costi della struttura di suddivisione del lavoro, è consigliabile configurare i costi e i prezzi di vendita per i lavoratori, le categorie di manodopera, le spese, le tariffe e gli articoli.

-   Per configurare il costo e il prezzo di vendita delle categorie manodopera, spesa e tariffa, fai clic su **Gestione progetti e contabilità** &gt; **Imposta** &gt; **Prezzi**.
-   Per configurare il costo e il prezzo di vendita degli articoli, utilizza la pagina **Accordi commerciali** per ogni elemento nella pagina elenco **Prodotti rilasciati** dell'elenco in Gestione delle informazioni sul prodotto.

## <a name="creating-a-wbs"></a>Creazione di un WBS
La creazione di una struttura di suddivisione del lavoro prevede tre attività:

1.  **Scomposizione del lavoro** : crea una suddivisione del lavoro in blocchi o attività gestibili.
2.  **Programma lavori** : stima il tempo necessario per completare un'attività, imposta le interdipendenze delle attività e seleziona le date di inizio e fine per le attività.
3.  **Stima dei costi** : stima i costi per ogni attività.

Le sezioni seguenti illustrano come le funzionalità di struttura di suddivisione del lavoro possono essere utili in ciascuno di questi impegni.

### <a name="work-decomposition"></a>Scomposizione del lavoro

La creazione di una suddivisione o scomposizione del lavoro è solitamente il primo passaggio nel processo di creazione di una struttura di suddivisione del lavoro. La funzionalità di struttura di suddivisione del lavoro supporta i seguenti costrutti di base per la suddivisione o scomposizione del lavoro. 

**Attività principale del progetto** : l'attività principale del progetto è l'attività di riepilogo di primo livello per un progetto. Tutte le altre attività di progetto vengono create al di sotto. Il nome dell'attività radice è sempre il nome del progetto. L'impegno, le date e la durata del nodo radice riepilogano i valori per le attività sotto l'attività radice. Non puoi modificare le proprietà del nodo radice o eliminarlo.

**Attività di riepilogo o contenitore** : un'attività di riepilogo è un'attività che include attività secondarie o costituenti al di sotto. Un'attività di riepilogo non ha alcun lavoro o costo proprio. Invece, lo sforzo di lavoro e il costo di un'attività di riepilogo sono la somma dello sforzo di lavoro e il costo delle sue attività costitutive. La data di inizio meno recente delle attività costituenti viene utilizzata come data di inizio dell'attività di riepilogo mentre le data di fine più recente delle attività costituenti viene utilizzata come data di fine. Puoi modificare il nome di un'attività di riepilogo, ma non puoi modificare le proprietà di pianificazione per impegno, date e durata. Se elimini un'attività di riepilogo, elimina anche tutte le relative attività costituenti. 

**Attività del nodo foglia** : un'attività del nodo foglia rappresenta il pacchetto di lavoro più granulare del progetto. Un nodo foglia include un lavoro stimato, un numero pianificato di risorse, una data di inizio e una data di fine pianificate e una durata. 

Puoi completare le seguenti operazioni di gerarchia per abilitare la creazione di una gerarchia di lavoro o la scomposizione per un progetto. 

**Nuova attività** : qualsiasi nuova attività creata viene aggiunta automaticamente sotto il nodo principale e all'attività viene automaticamente assegnato un numero di struttura di suddivisione del lavoro. Il numero di struttura di suddivisione del lavoro rappresenta il livello dell'attività nella gerarchia. Per le attività nel primo livello sotto l'attività radice del progetto, viene utilizzato uno schema di numerazione con 1, 2, 3 e così via. Per le attività sotto il primo livello, viene utilizzato uno schema di numerazione con 1.1, 1.2, 1.3 e così via. Per ogni livello che viene aggiunto sotto un livello precedente, viene aggiunta una nuova serie di numeri tratteggiata. 

Attualmente non è possibile personalizzare la numerazione della struttura di suddivisione del lavoro. 

**Rientro attività** : quando fai rientrare un'attività, diventa un elemento figlio dell'attività che la precede. Il numero di struttura di suddivisione del lavoro della nuova attività figlio viene ricalcolato automaticamente in base al numero di struttura di suddivisione del lavoro del nuovo elemento padre. L'attività padre è ora un'attività di riepilogo o contenitore e quindi diventa un rollup delle sue attività costituenti. 

> [!NOTE] 
> Quando fai rientrare le attività in un'attività che era un nodo foglia prima dell'operazione di rientro, l'attività di riepilogo appena creata perde le proprie date, il lavoro e il numero di risorse. Ora utilizza un riepilogo dei valori delle sue nuove attività costituenti. 

**Rientro negativo attività** : quando si crea un rientro negativo per un'attività, non è più un'attività costituente del suo elemento padre. Il numero di struttura di suddivisione del lavoro di questa attività viene ricalcolato automaticamente per riflettere il nuovo livello dell'attività nella gerarchia. Il lavoro richiesto, il costo e le date dell'attività padre precedente dell'attività vengono ricalcolati in modo da escludere tale attività. 

**Sposta su e sposta giù** : quando fai clic su **Sposta su** e **Sposta giù** , modifichi la posizione di un'attività all'interno della gerarchia del suo elemento padre. La posizione di un'attività non influisce sul lavoro richiesto, il costo, le date o la durata dell'attività. Tuttavia, il numero di struttura di suddivisione del lavoro dell'attività viene ricalcolato automaticamente per riflettere la nuova posizione dell'attività.

### <a name="schedule-estimation"></a>Stima di pianificazione

La stima della pianificazione è in genere il secondo passaggio nella creazione di una struttura di suddivisione del lavoro. Come migliore procedura, è consigliabile completare la stima della pianificazione dopo aver creato le attività. La pagina **Struttura di suddivisione del lavoro** in Finance ha due sezioni. Il riquadro superiore è destinato alla stima della pianificazione e il riquadro inferiore include una scheda **Costi e ricavi stimati** che puoi utilizzare per la stima dei costi. 
**Dipendenze attività** : in una struttura di suddivisione del lavoro puoi creare una relazione predecessore tra le attività. Quando assegni attività predecessore a un'attività, l'attività può iniziare solo dopo che tutte le attività predecessore sono state completate. La data di inizio pianificata dell'attività viene impostata automaticamente sulla data più recente di tutti i suoi predecessori. 

**Pianificazione attività** : i seguenti fattori determinano la pianificazione delle attività del nodo foglia:

-   Attività precedenti
-   Lavoro
-   Numero di risorse
-   Date di inizio e fine

La data di inizio di un'attività del nodo foglia privo di predecessori viene automaticamente impostata sulla data di inizio della pianificazione del progetto. La durata di un'attività del nodo foglia viene sempre calcolata come il numero dei giorni lavorativi tra le date di inizio e di fine. 

*<strong><em>Regole di pianificazione</em></strong>* Quando l'assistenza per la pianificazione automatica è attivata, le seguenti regole si applicano alla pianificazione delle attività per le attività del nodo foglia:

-   Le date di inizio e fine di un'attività devono sempre essere giorni lavorativi in base al calendario della pianificazione del progetto.
-   La data di inizio di un'attività con predecessori viene impostata automaticamente sull'ultima data di fine dei predecessori.
-   Lo sforzo per un'attività viene calcolato automaticamente come segue:

Numero delle persone × Durata × Numero di ore in un giorno lavorativo standard del calendario di progetto. 

In alcuni casi, può essere utile deviare dalle regole. Puoi disattivare la pianificazione automatica per impedire a Finance di impostare o correggere automaticamente le proprietà delle attività del nodo foglia. Quando immetti le informazioni per un'attività che causa una violazione delle regole di pianificazione, viene visualizzata un'icona di errore di pianificazione per l'attività. Se non desideri visualizzare gli errori di pianificazione, fai clic su **Gli errori di programmazione sono visualizzati** per disattivare la funzionalità. 

> [!NOTE] 
> I valori per un'attività di riepilogo o contenitore continuano a essere calcolati come la somma dei valori delle attività costituenti, indipendentemente dal fatto che l'assistenza per la pianificazione automatica sia attivata o disattivata. 

**Correzione degli errori di pianificazione** : quando l'assistenza per la pianificazione automatica è attivata, è improbabile che si verifichino errori di pianificazione. Tuttavia, se disattivi l'assistenza per la pianificazione automatica e la riattivi in un secondo momento, nella struttura di suddivisione del lavoro potrebbero essere visualizzate icone di errore di pianificazione. 

**Correzione degli errori di pianificazione per attività** : quando fai doppio clic sull'icona dell'errore di pianificazione per un'attività specifica, una finestra di dialogo visualizza tutti gli errori di pianificazione per quell'attività. Puoi decidere quali errori di pianificazione correggere per l'attività. 

**Correzione di tutti gli errori di pianificazione** : se desideri che Finance corregga tutti gli errori di pianificazione nella struttura di suddivisione del lavoro, nel riquadro azioni fai clic su **Correggi tutte le discrepanze programmazione**. 

> [!NOTE] 
> Questa funzionalità può causare modifiche significative alla struttura di suddivisione del lavoro. Gli errori vengono corretti nel seguente ordine:

1.  L'impegno stimato su tutte le attività viene modificato in modo che sia uguale alla capacità definita nel calendario del progetto.
2.  La data di inizio di ciascuna attività viene modificata in modo che l'attività venga avviata al termine di tutte le attività precedenti.
3.  La data di inizio di ogni attività viene modificata per rimuovere le lacune nelle date di inizio delle attività precedenti.

### <a name="cost-estimation"></a>Stima del costo

Come accennato in precedenza in questo documento, immetti la stima dei costi per ciascuna attività del nodo foglia utilizzando la scheda **Costi e ricavi stimati** nel riquadro inferiore della pagina **Struttura di suddivisione del lavoro**. 

> [!NOTE] 
> Non puoi modificare la stima dei costi per un riepilogo o un'attività contenitore. La stima dei costi per un'attività di riepilogo è uguale alla somma della stima dei costi delle relative attività del nodo foglia. Il costo totale stimato per ciascuna attività viene calcolato come la somma degli importi dei costi stimati per i seguenti tipi di transazione:

-   Lavoro
-   Articolo o materiale
-   Spese

Un tipo di transazione **Commissione** viene utilizzato per stimare i ricavi basati su commissioni. Questo tipo di transazione non ha una componente di costo e pertanto non viene preso in considerazione quando vengono stimati i costi. 

Un tipo di transazione **Sul conto** viene utilizzato per registrare il valore delle vendite contrattate in un tipo di progetto a valore fisso. Anche questo tipo di transazione non viene considerato nella stima dei costi. 

Quando stimi i costi per manodopera, materiale e spese per ciascuna attività, devi assegnare una categoria di progetto al costo stimato. 

**Stima dei costi del lavoro** : per ogni attività del nodo foglia, assegni uno sforzo di lavoro in ore e una categoria predefinita. Pertanto, quando configuri una pianificazione per un'attività, la stima del costo della manodopera per tale attività viene aggiunta automaticamente nella categoria predefinita per la manodopera. Questa stima dei costi viene visualizzata nella scheda **Costi e ricavi stimati** nella griglia **Dettagli riga** per quell'attività. Se hai bisogno di più stime del costo del lavoro, puoi aggiungerle in questa scheda. Se aumenti o diminuisci le ore sulla stima del costo del lavoro, la pianificazione dell'attività viene ricalcolata automaticamente. 

**Stima delle spese e dei costi dei materiali** : la scheda **Costi e ricavi stimati** consente inoltre di stimare le spese e i costi dei materiali per un'attività, se sono necessarie stime. 

Il costo e il prezzo di vendita per ciascuna riga di stima della manodopera o delle spese si basano sulla configurazione definita per ciascuna categoria nelle tabelle dei prezzi su **Gestione progetti e contabilità** &gt; **Imposta** &gt; **Prezzi**. Per gli articoli, il costo e il prezzo di vendita vengono aggiunti per impostazione predeginita dai accordi commerciali e degli articoli nella pagina elenco **Prodotti rilasciati** in Gestione delle informazioni sul prodotto.

## <a name="tracking-progress-on-the-wbs"></a>Monitoraggio dei progressi sulla struttura di suddivisione del lavoro
Alcuni settori monitorano l'avanzamento di un progetto rispetto a una struttura di suddivisione del lavoro a un livello molto granulare, mentre altri monitorano l'avanzamento a un livello superiore della struttura di suddivisione del lavoro. Questa sezione descrive come utilizzare il monitoraggio della struttura di suddivisione del lavoro per i requisiti del progetto. 

Finance ha tre visualizzazioni per la struttura di suddivisione del lavoro di un progetto: la visualizzazione Pianificazione, la visualizzazione Registrazione lavoro e la visualizzazione Registrazione costi.

### <a name="planning-view"></a>Visualizzazione Pianificazione

La visualizzazione Pianificazione mostra la stima pianificata o prevista della pianificazione e le informazioni sui costi. Sebbene non siano presenti funzionalità per tenere traccia della versione e della previsione per una struttura di suddivisione del lavoro di progetto, i valori in questa visualizzazione hanno lo scopo di rappresentare la versione di base. Le sezioni Stima della pianificazione e Stima dei costi di questo argomento descrivono questa visualizzazione e come viene utilizzata per creare una struttura di suddivisione del lavoro.

### <a name="effort-tracking-view"></a>Visualizzazione registrazione lavoro richiesto

La vista Registrazione lavoro visualizza la registrazione dell'avanzamento delle attività nella struttura di suddivisione del lavoro. Confronta le ore di lavoro effettive accumulate per un'attività con le ore di lavoro pianificate. Le seguenti formule forniscono i valori nella visualizzazione Registrazione lavoro:

-   Percentuale di avanzamento = Lavoro richiesto effettivo fino a data odierna ÷ Lavoro richiesto pianificato per l'attività
-   Impegno rimanente (noto anche come Stima per il completamento \[ECCETERA\]) = Impegno pianificato - Impegno effettivo fino ad oggi
-   Stima al completamento = Lavoro richiesto rimanente + Lavoro richiesto effettivo fino a data odierna
-   Scostamento risorse previsto = Lavoro richiesto pianificato - Stima al completamento

La visualizzazione Registrazione lavoro mostra una proiezione della varianza dello sforzo per l'attività, a seconda che la stima al completamento sia maggiore o minore dell'impegno pianificato:

-   Se la stima al completamento è superiore al lavoro richiesto pianificato, si prevede che l'attività richiederà più tempo di quello inizialmente pianificato.
-   Se la stima al completamento è inferiore al lavoro richiesto pianificato, si prevede che l'attività richiederà meno tempo di quello inizialmente pianificato.

**Riproiezione del lavoro da parte del project manager** : occasionalmente, il project manager o un'altra persona che sta monitorando lo stato di avanzamento di un progetto dovrà rivedere le stime originali su un'attività. L'attività potrebbe progredire più velocemente o più lentamente di quanto originariamente previsto per vari motivi. Ad esempio, l'ambito è stato ridotto oi lavoratori hanno meno esperienza di quanto inizialmente previsto. Le proiezioni sono la percezione delle stime di un project manager, in base allo stato corrente del progetto. In generale, non è consigliabile modificare le cifre di riferimento, poiché una base di progetto rappresenta un documento pubblicato per la pianificazione e le stime di costi concordate con tutte le parti interessate. 

Vi sono due modi in cui un project manager può modificare il lavoro richiesto per le attività:

-   Modifica il lavoro rimanente impostato automaticamente per aggiornare il lavoro rimanente effettivo per l'attività.
-   Modifica la percentuale di avanzamento impostata automaticamente per aggiornare il lavoro rimanente effettivo per l'attività.

Entrambi questi approcci genera un nuovo calcolo di stima di completamento, stima al completamento, percentuale di avanzamento e scostamento risorse previsto dell'attività. Anche la stima di completamento, la stima al completamento e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento risorse. 

**Impegno modificato sulle attività di riepilogo** : puoi modificare l'impegno su attività di riepilogo o contenitore. Indipendentemente dal fatto che modifichi tali lavori in base al lavoro richiesto rimanente o alla percentuale di avanzamento delle attività di riepilogo, i calcoli vengono eseguiti automaticamente nell'ordine seguente:

1.  La stima di completamento, la stima al completamento e la percentuale di avanzamento dell'attività vengono calcolate.
2.  La nuova stima al completamento viene distribuita alle attività figlio nella stessa proporzione della stima al completamento originale.
3.  Viene calcolata la nuova stima al completamento su ogni attività del nodo foglia.
4.  La percentuale di lavoro rimanente e di avanzamento viene ricalcolata per tutte le attività figlio interessate, in base al nuovo valore di stima al completamento. Viene ricalcolata anche lo scostamento risorse delle attività.
5.  Anche la stima al completamento delle attività di riepilogo viene ricalcolata a partire dai nodi foglia.

Fai clic su **Espandi al livello** nella visualizzazione Registrazione lavoro per impostare il livello al quale monitorare e mantenere la tua struttura di suddivisione del lavoro. La struttura di suddivisione del lavoro viene automaticamente espansa a quel livello nella visualizzazione Registrazione lavoro ogni volta che viene aperta.

### <a name="cost-tracking-view"></a>Vista Registrazione costi

La visualizzazione Registrazione costi mostra la registrazione del consumo di costi per un'attività. In questa visualizzazione, il costo effettivo che è stato speso per un'attività fino ad oggi viene confrontato con il costo pianificato per l'attività. Le seguenti formule forniscono i valori nella visualizzazione Registrazione costi:

-   Percentuale di costo consumata = Costo effettivo fino a data odierna ÷ Costo pianificato per l'attività
-   Costi di completamento = Costo pianificato - Costo effettivo fino a data odierna
-   Stima al completamento (EAC) = CTC + Costo effettivo fino ad oggi
-   Scostamento costo previsto = Costo pianificato - Stima al completamento

La visualizzazione Registrazione costi mostra una proiezione della varianza dei costi per l'attività, a seconda che la stima al completamento sia maggiore o minore del costo pianificato:

-   Se la stima al completamento è superiore al costo pianificato, si prevede che l'attività richiederà più spese e il budget verrà superato.
-   Se la stima al completamento è inferiore al costo pianificato, si prevede che l'attività richiederà meno spese e il budget verrà rispettato.

**Riproiezione dei costi da parte del project manager** : i project manager devono utilizzare CTC per rivedere la stima dei costi originale su un'attività. Il project manager può modificare il valore CTC sul costo richiesto per completare l'attività. Se modifichi il valore CTC, vengono ricalcolati il CTC, la stima al completamento e la percentuale di costo consumato dell'attività e la varianza dei costi prevista per un'attività. Anche la stima al completamento, l'ETC e la percentuale di costo consumato delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione della varianza di costo. 

> [!NOTE] 
> Quando rivedi il lavoro per un'attività di struttura di suddivisione del lavoro nella visualizzazione Registrazione lavoro, i valori CTC, stima al completamento, la percentuale del costo consumato e lo scostamento del costo previsto dell'attività vengono ricalcolati nella visualizzazione Registrazione costi. Tuttavia, le revisioni dei costi non influiscono sui valori nella visualizzazione Registrazione lavoro, perché il costo per tipo di transazione (manodopera, materiale o spesa) o categoria di progetto non viene rivisto. 

**Revisione della proiezione dei costi sulle attività di riepilogo** : puoi rivedere i costi nelle attività di riepilogo e i calcoli vengono eseguiti automaticamente nell'ordine seguente:

1.  Vengono ricalcolati stima al completamento, CTC e la percentuale di costo utilizzata per l'attività.
2.  La nuova stima al completamento viene distribuita alle attività figlio nella stessa proporzione della stima al completamento originale delle attività.
3.  Viene calcolata la nuova stima al completamento per ogni attività.
4.  Il CTS e la percentuale di costo consumato vengono ricalcolati per le attività figlio interessate, in base al valore EAC. Viene ricalcolato anche lo scostamento di costo delle attività.
5.  La stima al completamento per tutte le attività di riepilogo viene ricalcolata in base a questa modifica.

Fai clic su **Espandi al livello** nella visualizzazione Registrazione costi per impostare il livello al quale monitorare e mantenere la tua struttura di suddivisione del lavoro. La struttura di suddivisione del lavoro viene espansa a quel livello nella visualizzazione Registrazione costi ogni volta che viene aperta.

### <a name="earned-value-management"></a>Gestione del costo realizzato

Puoi utilizzare il metodo del costo realizzato (EVM) per monitorare l'avanzamento di un progetto. Puoi visualizzare la metrica del costo realizzato nel Centro gestione ruolo del project manager. Il componente grafico del costo realizzato mostra i valori cronologici del valore pianificato e del costo effettivo. Il costo realizzato alla data corrente viene mostrato come un punto. I dati cronologici per il costo realizzato non sono attualmente disponibili. 

La fase temporale sul grafico del costo realizzato viene visualizzata per settimana o per mese. Questa sezione descrive i tre pilastri dell'EVM: valore pianificato, costo realizzato e costo effettivo. 

**Valore pianificato** : la teoria EVM afferma che il grafico del valore pianificato rappresenta la velocità con cui il team del progetto ha pianificato di guadagnare valore sul progetto. 

Finance utilizza la regola di guadagno 0:100 quando traccia il valore pianificato. In base a questa regola, il valore dell'attività viene registrato nell'attività alla data di fine. Non viene registrato alcun valore finché l'attività non viene completata al 100%. 

In Gestione progetti e contabilità, immetti la data di fine dei nodi foglia e il relativo costo pianificato. Quando il grafico del valore pianificato viene visualizzato per settimana, il valore pianificato viene riepilogato per settimana per tutte le attività del nodo foglia per la durata del progetto. 

**Costo realizzato** : la teoria EVM afferma che il grafico del costo realizzato rappresenta la velocità con cui il team del progetto sta effettivamente realizzando costi sul progetto. 

Finance utilizza la regola di guadagno 0:100 quando traccia il costo realizzato. In base a questa regola, il valore dell'attività viene registrato nell'attività alla data di fine. Non viene registrato alcun valore finché l'attività non viene completata al 100%. 

Quando viene calcolato il costo realizzato, viene considerata la percentuale di avanzamento di ciascuna attività. In base alla regola di guadagno 0:100, solo le attività completate in un determinato periodo vengono prese in considerazione per il calcolo del costo realizzato alla fine di tale periodo. Il valore ottenuto sul progetto viene calcolato per tutte le attività che sono state completate quando viene creato il grafico. 

> [!NOTE] 
> Attualmente, il sistema per la registrazione della struttura di suddivisione del lavoro non dispone di strutture di dati per memorizzare le percentuali di avanzamento cronologiche su ciascuna attività. Pertanto, il costo realizzato può essere riportato solo a partire dal momento in cui il cubo viene elaborato. Elabora regolarmente il cubo per aggiornare i dati sul costo realizzato visualizzati nel Centro gestione ruolo. 

**Costo effettivo** : la teoria dell'EVM afferma che il grafico dei costi effettivi rappresenta il tasso al quale il denaro viene speso per il progetto. 

Le transazioni registrate in un progetto vengono utilizzate per tracciare la riga di costo effettivo. I costi sono riepilogati per data. Questi dati vengono quindi utilizzati per rappresentare graficamente i costi effettivi per settimana o per mese sul grafico del costo realizzato.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Come utilizzare i concetti di valore pianificato, costo realizzato e costo effettivo

**Scostamento pianificazione** : durante la pianificazione, crei una previsione per il lavoro su una sequenza temporale. Pertanto, il valore pianificato è la velocità con cui i pianificatori del progetto pensavano che il lavoro sarebbe stato completato sul progetto. Dopo che un progetto è in corso, il lavoro è completato e il progetto guadagna valore. Confrontando il valore pianificato con il costo realizzato, puoi visualizzare lo stato di avanzamento del lavoro su un progetto. Il risultato di questo confronto è chiamato scostamento pianificazione. 

Se il valore pianificato per un periodo è superiore al costo realizzato, la quantità di lavoro che è stata eseguita su un progetto è inferiore a quanto pianificato. Pertanto, il progetto è in ritardo sulla pianificazione. Poiché il valore pianificato e il costo realizzato sono espressi in termini monetari, anche al tempo di ritardo del progetto viene assegnato un valore monetario. 

Se il valore pianificato per un periodo è inferiore al costo realizzato, la quantità di lavoro che è stata eseguita su un progetto è superiore a quanto pianificato. Pertanto, il progetto è in anticipo sulla pianificazione. A questo tempo di consegna viene anche assegnato un valore monetario.

**Scostamento costo** : poiché il costo realizzato utilizza il prezzo di costo come moltiplicatore, il costo realizzato indica il costo del lavoro svolto su un progetto. Man mano che un progetto avanza, il registro delle transazioni fornisce una registrazione del denaro effettivamente speso per quel progetto. Confrontando il costo realizzato con il costo effettivo, è possibile visualizzare la quantità di denaro speso rispetto al valore guadagnato. Il risultato di questo confronto è chiamato scostamento costo. 

Se il costo effettivo speso per un periodo è superiore al costo realizzato, è stato speso più denaro di quanto guadagnato. Pertanto, il progetto è fuori budget. 

Se il costo effettivo speso per un periodo è inferiore al costo realizzato, è stato guadagnato più denaro di quanto speso. Pertanto, il progetto rientra perfettamente nel budget.

## <a name="wbs-templates"></a>Modelli di struttura di suddivisione del lavoro
Puoi utilizzare la funzionalità dei modelli di struttura di suddivisione del lavoro per creare modelli standard per i progetti. Se i progetti offerti dalla tua azienda comportano molto lavoro ripetibile, dovresti prendere in considerazione la creazione di un modello di struttura di suddivisione del lavoro. 

Puoi creare un modello di struttura di suddivisione del lavoro dalla struttura di suddivisione del lavoro di un progetto esistente, in modo che le conoscenze e le procedure migliori raccolte durante la pianificazione di quel progetto possano essere riutilizzate su progetti simili in futuro. Tuttavia, a volte, potrebbe non avere senso salvare l'intera struttura di suddivisione del lavoro come modello. Pertanto, è anche possibile creare modelli da parti della struttura di suddivisione del lavoro per un progetto.

### <a name="saving-a-projects-wbs-as-a-template"></a>Salvataggio della struttura di suddivisione del lavoro di un progetto come modello

Dopo aver creato un modello, puoi importarlo nella struttura di suddivisione del lavoro di un nuovo progetto sotto il nodo radice o in qualsiasi attività nella struttura di suddivisione del lavoro del progetto.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importazione di un modello di struttura di suddivisione del lavoro nella struttura di suddivisione del lavoro di un progetto

Quando importi le attività, le attività nel modello sono organizzate in base alla data di inizio dell'attività in cui sono state importate. Durante l'importazione, le relazioni del predecessore nelle attività del modello vengono utilizzate per calcolare le date di inizio delle attività importate. Il calendario di lavoro standard del progetto di destinazione viene applicato per calcolare le date di fine delle attività importate, in modo che i giorni lavorativi e l'orario di lavoro standard definiti nel calendario di lavoro del progetto corrente vengano mantenuti. 

Gli importi dei costi e i prezzi di vendita nelle righe di stima vengono applicati per garantire che i prezzi specifici del progetto o del contratto di progetto abbiano date valide.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Differenze tra la struttura di suddivisione del lavoro di un progetto e un modello di struttura di suddivisione del lavoro

-   Le attività nei modelli di struttura di suddivisione del lavoro non hanno date di inizio e date di fine.

I giorni lavorativi e non lavorativi non sono impostati per i modelli di struttura di suddivisione del lavoro.

-   I modelli di struttura di suddivisione del lavoro utilizzano sempre il calendario di pianificazione configurato come calendario predefinito per tutti i progetti.

Il calendario di pianificazione predefinito viene utilizzato solo per conoscere le ore in una giornata lavorativa standard.

-   Le relazioni del predecessore non vengono copiate in un modello di struttura di suddivisione del lavoro.

Poiché i modelli di struttura di suddivisione del lavoro non hanno date, la logica della data di inizio basata sulla data di fine di un predecessore non è richiesta.

-   Quando viene creata un'attività in un modello di struttura di suddivisione del lavoro, viene creata automaticamente una riga di stima del costo del lavoro. Il prezzo di vendita e l'importo del costo vengono copiati dal ruolo di lavoro selezionato.

I costi di spesa e articolo possono essere creati manualmente, proprio come nella struttura di suddivisione del lavoro di un progetto.

-   Gli errori di pianificazione vengono visualizzati quando ci sono scostamenti dalla seguente formula:

Risorse = Numero di risorse × Durata × Numero di ore in una giornata lavorativa standard 

Puoi correggere tutti gli errori di pianificazione contemporaneamente facendo clic su **Correggi tutti gli errori di pianificazione**. 

In alternativa, puoi correggere gli errori di pianificazione singolarmente facendo clic sull'icona di avviso per ciascuna attività.





[!INCLUDE[footer-include](../includes/footer-banner.md)]