---
title: Contratti di progetto
description: Questo argomento fornisce esempi dei contratti di progetto che puoi creare per vari tipi di progetti e fonti di finanziamento, e come puoi gestire i contratti e inviare fattura ai clienti del progetto.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752676"
---
# <a name="project-contracts"></a>Contratti di progetto

[!include [banner](../includes/banner.md)]

Questo articolo fornisce esempi dei contratti di progetto che puoi creare per vari tipi di progetti e fonti di finanziamento, e come puoi gestire i contratti e inviare fattura ai clienti del progetto.

Il tipo di progetto creato per un contratto di progetto determina il metodo utilizzato per fatturare i clienti del progetto. Puoi modificare un contratto di progetto e il progetto correlato, ma non puoi modificare il tipo di progetto. 

Utilizzando un contratto di progetto, puoi fatturare uno o più progetti contemporaneamente. Il contratto di progetto aiuta anche a garantire una procedura di fatturazione coerente per ogni sottoprogetto in una struttura di progetto. 

Ogni progetto che verrà fatturato deve essere associato a un contratto di progetto. Le impostazioni per un contratto di progetto si applicano a tutti i progetti e sottoprogetti associati a quel contratto di progetto. 

Un contratto di progetto può specificare una o più fonti di finanziamento. Pertanto, è possibile suddividere la fatturazione tra più finanziatori, impostare limiti di finanziamento in modo che le fonti di finanziamento non vengano fatturate per più di un importo specificato e configurare le regole di finanziamento per l'addebito delle spese.

## <a name="funding-for-project-contracts"></a>Finanziamenti per contratti a progetto
Alcuni contratti di progetto specificano che più parti condividono la responsabilità del finanziamento dei costi del progetto. Di seguito sono riportati alcuni esempi.

-   Un grande cliente che ha più divisioni richiede che il finanziamento di un progetto sia suddiviso per divisione.
-   La tua azienda condivide i costi di un grande progetto con un'organizzazione esterna.
-   Un progetto stradale è cofinanziato da due comuni.
-   Un progetto per un ponte è finanziato da una sovvenzione governativa e da una società privata.

In Dynamics 365 Finance, puoi suddividere la fatturazione per una singola transazione o un intero progetto tra più clienti, sovvenzioni o organizzazioni. 

Nei progetti che hanno più finanziatori, tutte le parti che contribuiscono al finanziamento di un progetto di finanziamento avanzato sono chiamate fonti di finanziamento. Dopo che un cliente, un'organizzazione o una sovvenzione è stata definita come fonte di finanziamento, può essere assegnata a una o più regole di finanziamento. Le regole di finanziamento contengono i criteri che determinano il modo in cui gli addebiti vengono assegnati alle varie fonti di finanziamento per un progetto. 

Poiché gli articoli in magazzino, come quelli che compaiono nelle richieste di acquisto e negli ordini di acquisto, non possono essere suddivisi, l'importo del costo non può essere suddiviso tra più fonti di finanziamento al momento della distribuzione. Pertanto, il valore della fonte di finanziamento rimane 0 (zero) fino a quando non viene registrata l'uscita di magazzino. Quando viene registrata l'uscita di magazzino, l'importo del costo viene distribuito in base alle regole di distribuzione del conto per il progetto.

Di seguito sono riportati alcuni passaggi che puoi eseguire per semplificare la suddivisione della fatturazione tra più fonti di finanziamento:

-   Specifica che tutte le transazioni immesse per un progetto utilizzano la stessa valuta di vendita del contratto di progetto.
-   Configura i limiti di finanziamento, in modo che a una fonte di finanziamento non venga fatturato più di un importo specificato per un progetto.
-   Configura le regole di finanziamento e i limiti di finanziamento per ogni ruolo di lavoro, articolo, categoria, gruppo di categorie e tipo di transazione (o per tutti i tipi di transazione).
-   Seleziona le date di inizio e di fine facoltative per definire il periodo di validità di ciascuna regola di finanziamento.
-   Specifica la percentuale di cui è responsabile ciascuna fonte di finanziamento.
-   Specifica quale fonte di finanziamento è responsabile dell'arrotondamento delle differenze causate dai calcoli di allocazione dei finanziamenti.
-   Configura le regole che determinano il modo in cui i costi del progetto vengono fatturati ai clienti esterni e addebitati alle organizzazioni interne.
-   Registra le transazioni in un conto di finanziamento sospeso fino a quando non è possibile ottenere finanziamenti aggiuntivi o finché non decidi di sostenere i costi internamente.

Per determinare quale gruppo fiscale associare a una transazione, nel progetto viene eseguita la ricerca di un'assegnazione di gruppo fiscale. Se non è stata effettuata alcuna assegnazione di gruppo fiscale a livello di progetto, viene eseguita una ricerca nel contratto di progetto.

### <a name="example-multiple-funding-sources-simple"></a>Esempio: più fonti di finanziamento (semplice)

La tabella seguente fornisce gli scenari per la gestione dell'allocazione dei finanziamenti tra più fonti di finanziamento. Questi scenari si basano sui seguenti presupposti:

-   Le impostazioni di priorità vengono prese in considerazione nell'allocazione dei fondi prima che vengano applicati altri criteri delle regole di finanziamento.
-   Non è stato specificato alcun intervallo di date per definire il periodo in cui la regola di finanziamento è valida.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenario</strong></td>
<td><strong>Fonte di finanziamento</strong></td>
<td><strong>Percentuale di allocazione</strong></td>
<td><strong>Priorità di allocazione</strong></td>
</tr>
<tr class="even">
<td>Vuoi allocare i costi a una fonte di finanziamento finché i suoi fondi non sono esauriti, allocare i costi a una seconda fonte di finanziamento fino a quando i suoi fondi non sono esauriti e infine allocare i costi rimanenti a una terza fonte di finanziamento.</td>
<td><ul>
<li>Fonte di　finanziamento　1</li>
<li>Fonte di　finanziamento　2</li>
<li>Fonte di　finanziamento　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vuoi allocare il 75% dei costi a una fonte di finanziamento e il 25% a una seconda fonte di finanziamento. Quando una di queste fonti di finanziamento è esaurita, vuoi pagare i costi rimanenti da una terza fonte di finanziamento.</td>
<td><ul>
<li>Fonte di　finanziamento　1</li>
<li>Fonte di　finanziamento　2</li>
<li>Fonte di　finanziamento　3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Vuoi allocare il 75% dei costi a una fonte di finanziamento e il 25% a una seconda fonte di finanziamento. Quando una di queste fonti di finanziamento è esaurita, vuoi dividere i costi rimanenti tra una terza e una quarta fonte di finanziamento.</td>
<td><ul>
<li>Fonte di　finanziamento　1</li>
<li>Fonte di　finanziamento　2</li>
<li>Fonte di　finanziamento　3</li>
<li>Fonte di　finanziamento　4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vuoi allocare il primo 25% dei costi a una fonte di finanziamento e il resto a una seconda fonte di finanziamento.</td>
<td><ul>
<li>Fonte di　finanziamento　1</li>
<li>Fonte di　finanziamento　2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Esempio: più fonti di finanziamento (complessa)

Hai tre fonti di finanziamento che desideri utilizzare nel seguente ordine:

1.  Utilizza la fonte di finanziamento 2 e la fonte di finanziamento 3 allo stesso modo fino a quando la fonte di finanziamento 2 non è esaurita.
2.  Continua a utilizzare la fonte di finanziamento 3 fino all'esaurimento.
3.  Utilizza la fonte di finanziamento 1 dopo che la fonte di finanziamento 3 è esaurita.

Per realizzare questo obiettivo, devi fare quanto segue:

-   Configura i limiti di finanziamento per la fonte di finanziamento 2 e la fonte di finanziamento 3, per i rispettivi importi.
-   Creare le regole di finanziamento seguenti:
    -   Regola 1 (Priorità 1): Assegna il 50% delle transazioni alla fonte di finanziamento 2 e il 50% alla fonte di finanziamento 3.
    -   Regola 2 (Priorità 2): Assegna il 100% delle transazioni alla fonte di finanziamento 3.
    -   Regola 3 (Priorità 3): Assegna il 100% delle transazioni alla fonte di finanziamento 1.

Questa configurazione funziona perché le transazioni vengono verificate a fronte di regole e limiti per determinare se qualcuno di essi si applica alla transazione. Se alla transazione non si applicano regole o limiti specifici, si applica la regola Tutte le transazioni. La regola Tutte le transazioni corrisponde a tutte le transazioni. 

Se viene trovata una regola che corrisponde a una transazione, la percentuale che è stata assegnata in quella regola viene applicata per prima, ma solo dopo che le corrispondenze sono state verificate rispetto ai limiti impostati. Se è stato raggiunto un limite e i fondi di una fonte di finanziamento sono esauriti, la regola di finanziamento associata al limite di finanziamento viene ignorata e il programma verifica la regola successiva che si applica. 

In alcuni casi, solo una parte di una transazione può essere allocata in base a una regola. Ciò potrebbe accadere perché viene raggiunto un limite quando la transazione viene allocata. In questo caso, in base a tale regola viene assegnato solo un determinato importo, ad esempio il 50 percento a ciascuna fonte di finanziamento. Questo è il caso della regola 1, descritta in precedenza in questa sezione. Il resto viene assegnato in base alla regola successiva nella sequenza. 

La tabella seguente esamina questo scenario in maggior dettaglio.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Obiettivo mirato</strong></td>
<td><strong>Dettagli</strong></td>
</tr>
<tr class="even">
<td>Regole di finanziamento</td>
<td><ul>
<li>Regola 1 (priorità 1): tutte le transazioni. Effettua l'allocazione alla fonte di finanziamento 2 al 50% e la fonte di finanziamento 3 al 50%.</li>
<li>Regola 2 (priorità 2): tutte le transazioni. Assegna la fonte di finanziamento 3 al 100%.</li>
<li>Regola 3 (priorità 2): tutte le transazioni. Assegna la fonte di finanziamento 1 al 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Limiti di finanziamento</td>
<td><ul>
<li>Limite fonte di finanziamento 1 = 10.000,00</li>
<li>Limite fonte di finanziamento 2 = 500,00</li>
<li>Limite fonte di finanziamento 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transazione 1</td>
<td><strong>Importo transazione:</strong> 100,00 <strong>Finanziamento:</strong> la transazione viene pagata solo in base alla regola 1, perché la transazione è completamente pagata dopo l'applicazione della regola 1. La transazione è finanziata equamente tra la fonte di finanziamento 2 e la fonte di finanziamento 3.
<ul>
<li>Fonte di finanziamento 2: 50,00</li>
<li>Fonte di finanziamento 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transazione 2</td>
<td><strong>Importo transazione:</strong> 5.000,00 <strong>Finanziamento:</strong> la transazione viene pagata secondo tutte e tre le regole. <strong>Regola 1</strong>
<ul>
<li>Fonte di finanziamento 2: 450,00</li>
<li>Fonte di finanziamento 3: 450,00</li>
</ul>
<strong>Regola 2</strong>
<ul>
<li>Fonte di finanziamento 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regola 3</strong>
<ul>
<li>Fonte di finanziamento 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Fondi totali distribuiti per ciascuna fonte di finanziamento</td>
<td><ul>
<li>Fonte di finanziamento 1: 3.850,00</li>
<li>Fonte di finanziamento 2: 500,00</li>
<li>Fonte di finanziamento 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Regole di fatturazione
Quando negozi un contratto di progetto con un cliente, definisci come e quando puoi fatturare al cliente il lavoro su un progetto. Dopo aver configurato il contratto di progetto e il progetto, puoi configurare le regole di fatturazione per il progetto. Le regole di fatturazione si basano sui termini del progetto specificati nel contratto di progetto. Le regole di fatturazione che puoi creare dipendono dai termini del contratto di progetto e dal tipo di progetto, ad esempio Tempo e materiale o Prezzo fisso, che associ alla regola di fatturazione. Puoi creare più di una regola di fatturazione per un contratto di progetto. Puoi anche assegnare una regola di fatturazione a più progetti associati allo stesso contratto di progetto e con termini di fatturazione simili. 

Puoi configurare i seguenti tipi di regole di fatturazione:

-   **Unità di consegna**: fattura un cliente quando completi un'unità di consegna. Le unità di consegna vengono definite nel contratto.
-   **Progresso**: fattura un cliente quando completi una determinata percentuale del progetto. Puoi configurare una regola di fatturazione per calcolare automaticamente la percentuale di lavoro completato oppure è possibile calcolare manualmente la percentuale di lavoro completato e l'importo da fatturare al cliente.
-   **A fasi**: fattura a un cliente l'intero importo di una fase del progetto quando viene raggiunta.
-   **Commissione**: fattura un cliente per i tuoi servizi più una commissione di gestione, che in genere è una percentuale del costo dei servizi.
-   **Tempo e materiale**: fattura a un cliente il valore del tempo e dei materiali utilizzati in un progetto.

Per tutti i tipi di regole di fatturazione, puoi specificare una percentuale di conservazione che viene detratta dalle fatture del cliente fino a quando un progetto non raggiunge una fase concordata. La percentuale di trattenuta del pagamento è specificata nel contratto di progetto. L'importo viene calcolato in base al e sottratto dal valore totale delle righe in una fattura cliente. 

Per le regole di fatturazione **Tempo e materiale** e **Progresso**, puoi assegnare categorie addebitabili. Le categorie addebitabili indicano le transazioni che dovrebbero essere incluse nelle fatture dei clienti. 

Quando sei pronto per fatturare al cliente, l'importo da fatturare per il progetto viene calcolato in base alle regole di fatturazione e viene generata una proposta di fattura progetto. 

Le sezioni seguenti forniscono esempi che mostrano come configurare e gestire le regole di fatturazione per un progetto.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Esempio: crea una regola di fatturazione basata sul numero di unità consegnate

La tua organizzazione stipula un accordo per fornire un totale di cinque sessioni di formazione ai dipendenti di un cliente al costo di 10.000 per sessione di formazione. Fatturi al cliente dopo ogni sessione di formazione. 

Quando configuri le regole di fatturazione per il contratto, utilizzi i seguenti valori:

-   L'unità di consegna è una sessione di formazione.
-   Il prezzo unitario è 10.000 per sessione di formazione.
-   Il numero totale di unità è di cinque sessioni di formazione.

Dopo aver completato una sessione di formazione, puoi creare una fattura per 10.000, per la prima unità consegnata, e inviare la fattura al cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Esempio: crea una regola di fatturazione basata su una percentuale specificata di completamento del progetto (calcolo manuale)

La tua organizzazione, una società di consulenza software, stipula un accordo con un cliente per sviluppare parte di un prodotto che il cliente sta sviluppando. La tua organizzazione accetta di fornire il codice software per un periodo di sei mesi. Il cliente accetta di pagare alla tua organizzazione un totale di 100.000 per il lavoro. Crei una regola di fatturazione per fatturare al cliente in base alla percentuale di lavoro completata sul progetto, come specificato nel contratto.

-   Alla fine del primo mese, incontri il cliente per determinare la percentuale di lavoro completato. Dopo che tu e il cliente avete esaminato il progetto, decidete che il progetto è stato completato al 15%.
-   Crei una fattura per 15.000 (15 percento di 100.000) e la invii al cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Esempio: crea una regola di fatturazione basata su una percentuale specificata di completamento del progetto (calcolo automatico)

La tua organizzazione, una società di sviluppo software, accetta di sviluppare un pacchetto di contabilità salari per un cliente per 30.000. Il cliente accetta di pagare alla tua organizzazione in base alla percentuale di lavoro completato. Stimi che i costi del progetto siano 20.000. Il contratto di progetto specifica le categorie di lavoro che utilizzi nel processo di fatturazione. Configuri regole di fatturazione che calcolano automaticamente gli importi delle fatture per la percentuale di lavoro completata per ciascuna categoria. Hai configurato un budget per ogni categoria:

-   **Sviluppo**: costo di 15.000 e ricavi di 20.000
-   **Installazione**: costo di 5.000 e ricavi di 10.000

Quando crei una fattura cliente per la prima volta, l'importo della fattura viene calcolato automaticamente in base alle seguenti informazioni:

-   Dopo un mese, il lavoratore del progetto invia una scheda attività per il progetto. Il costo delle ore del lavoratore è di 5.000 per lo sviluppo e 1.000 per l'installazione. Il lavoro di sviluppo è completato al 33% (5.000 costi effettivi/15.000 costi a budget) e il lavoro di installazione è completato al 20% (1.000 costi effettivi/5.000 costi a budget).
-   L'importo della fattura di 8.667 viene calcolato automaticamente (33 percento di 20.000 + 20 percento di 10.000).
-   Crei una fattura per 8.667 e la invii al cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Esempio: crea una regola di fatturazione basata su fasi concordate

La tua organizzazione, una società di consulenza gestionale, accetta di condurre ricerche di mercato per un prodotto di consumo che il cliente intende vendere. Il cliente accetta di utilizzare i tuoi servizi per un periodo di tre mesi, a partire da marzo, e accetta di pagare alla tua organizzazione 50.000. Il progetto ha tre fasi:

-   Fase 1: raccolta dei dati sui consumatori - 31 marzo
-   Fase 2: analisi dei dati sui consumatori - 30 aprile
-   Fase 3: presentazione di una proposta di fattibilità del prodotto - 31 maggio

Il cliente accetta di pagare alla tua organizzazione 10.000 per la prima fase, 20.000 per la seconda e 20.000 per la terza. 

Quando configuri il contratto di progetto, accetti di fatturare al cliente in base alla fase che hai completato. La configurazione della regola di fatturazione include i seguenti passaggi:

-   Definisci le fasi del progetto.
-   Definisci l'importo da fatturare al cliente al completamento di ogni fase.

Quando la prima fase viene completata il 31 marzo, contrassegni la fase come completata, quindi crei una fattura per 10.000 e la invii al cliente. Non puoi creare una fattura per una fase finché non è stata contrassegnata come completata.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Esempio: crea una regola di fatturazione basata sui servizi più una commissione di gestione

La tua organizzazione, una società di consulenza gestionale, accetta di condurre ricerche di mercato per valutare la fattibilità di un prodotto che il cliente, una società di vendita al dettaglio, sta sviluppando. I termini dell'accordo specificano che fornirai i servizi dei tuoi primi tre consulenti di gestione, che condurranno la ricerca in base al tempo e ai materiali. Il cliente accetta di pagare 100 all'ora, più una commissione di gestione del 10% per le ore di consulenza addebitate al progetto. 

Quando configuri il contratto di progetto, crea una regola di fatturazione per aggiungere una commissione di gestione del 10% alle ore di consulenza addebitate al progetto. 

Quando crei una fattura per il cliente, al cliente viene addebitata una commissione di gestione del 10% più il costo delle ore di consulenza. Ad esempio, se i tre consulenti hanno lavorato un totale di 200 ore al progetto, viene creata una fattura per 22.000 in base al seguente calcolo:

-   200 ore a 100 all'ora = 20.000
-   Commissione di gestione del 10% = 2.000
-   Importo totale fattura = 22.000

Se le commissioni sono imponibili a un cliente e si seleziona una fascia IVA nel contratto di progetto, la fascia IVA viene inserita automaticamente in una regola di fatturazione per le commissioni.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Esempio: crea una regola di fatturazione per il valore del tempo e dei materiali

La tua organizzazione, una società di consulenza software, accetta di fornire cinque consulenti tecnici per lavorare su un progetto di sviluppo software per un cliente per i prossimi sei mesi. Il cliente si impegna a pagare 150 per ogni ora di consulenza, più il costo delle forniture per ufficio. La tua organizzazione invia una fattura al cliente alla fine di ogni mese. 

Quando configuri il contratto di progetto, accetti di fatturare al cliente ogni mese il tempo e i materiali relativi al progetto. Crei una regola di fatturazione che include le seguenti informazioni:

-   La durata del contratto è di sei mesi.
-   Il tempo di consulenza è calcolato a una tariffa di 150 all'ora.
-   Le forniture per ufficio vengono fatturate al costo e il costo totale del progetto non deve superare 10.000.
-   Crei una fattura cliente alla fine di ogni mese di calendario durante il progetto.

Durante il primo mese, i consulenti sul progetto registrano un totale di 800 ore. Il costo delle forniture per ufficio addebitate al progetto è di 2.000. Pertanto, alla fine del mese, crei una fattura per 122.000, che viene calcolata come 800 ore a 150 l'ora, più 2.000 per le forniture per ufficio.



