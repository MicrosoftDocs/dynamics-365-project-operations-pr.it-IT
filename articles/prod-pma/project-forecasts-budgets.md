---
title: Previsioni e budget di progetto
description: Microsoft Dynamics 365 Finance fonrisce previsioni di progetto e budget di progetto per gestire e controllare i tuoi progetti.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078989"
---
# <a name="project-forecasts-and-budgets"></a>Previsioni e budget di progetto

[!include [banner](../includes/banner.md)]

Esistono due modi per gestire e controllare i tuoi progetti: previsioni di progetto e budget di progetto. 

Utilizza la previsione di progetto se l'organizzazione ha una prospettiva operativa e si concentra sui ricavi e sui costi derivati da transazioni specifiche. Utilizza il budget di progetto se la tua organizzazione si concentra maggiormente sugli importi finanziari. 

Sia le previsioni di progetto che i budget di progetto utilizzano modelli di previsione per contenere gli importi delle transazioni previste. 

Ognuno dei metodi presenta vantaggi specifici. È consigliabile considerare i seguenti punti prima di selezionare un metodo per la propria organizzazione.

|   Metodo di allocazione       |           Previsione di progetto            |        Budget di progetto                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Allocazione del periodo**     | Non è possibile allocare esplicitamente transazioni su un periodo fiscale. Invece, la previsione e il controllo della previsione si basano sulla durata del progetto. Poiché le previsioni si basano su una data specifica, devi dedurre il periodo dalla data. | Puoi allocare transazioni su un intero progetto o un periodo fiscale. Se effettui l'allocazione su un periodo, puoi trasferire gli importi non utilizzati sul prossimo periodo fiscale. |
| **Visualizzazione delle transazioni**  | Puoi visualizzare le transazioni nei moduli di previsione, dove puoi vedere le previsioni per l'intera azienda e per tutti i progetti, indipendentemente dalla gerarchia. Per concentrarti su un particolare progetto, devi filtrare i dati.                                       | Puoi visualizzare le transazioni di budget per una singola gerarchia di progetto. Pertanto, puoi visualizzare i dettagli della transazione per un progetto padre o i suoi sottoprogetti.                 |
| **Variabili di transazione** | Quando immetti transazioni previsionali, puoi utilizzare ogni attributo esistente per una transazione effettiva. Ciò consente maggiori dettagli nelle previsioni. Ad esempio, puoi immettere i dettagli per quantità, lavoratori, articoli o proprietà riga.         | Quando immetti i dettagli del budget, puoi utilizzare solo importi, categorie e attività.                    |
| **Sicurezza**              | La previsione si basa sulle transazioni immesse nei moduli di previsione e non prevede alcun meccanismo di controllo del processo. Qualsiasi ruolo di lavoro che dispone delle autorizzazioni per un modulo di previsione può modificare le informazioni senza approvazione.                                        | L'impostazione del budget utilizza il sistema del flusso di lavoro, che consente la gestione delle modifiche e consente di conservare una cronologia delle revisioni.         |
| **Tipi di immissione**           | Le voci di transazione previste si basano sul numero di unità e sui prezzi unitari di vendita e di costo.  | I dettagli del budget si basano sugli importi, suddivisi tra costi e ricavi.                                          |
| **Modelli di previsione**       | Poiché ogni previsione deve essere associata a un modello, puoi creare più modelli di previsione e impostare anche sottomodelli.           | Il budget di progetto limita i modelli di previsione utilizzati per il budget. Un minor numero di modelli previsionali può aiutare ad aumentare la coerenza nelle proiezioni.                           |
| **Sovraccarichi di costi**         | È possibile solo consentire o impedire l'inserimento di transazioni che causeranno un sovraccarico di costi.   | Il budget di progetto fornisce ulteriori opzioni di controllo per gli utenti. Puoi consentire avvisi e sovraccarichi.                    |
| **Controllo**               | Il controllo delle previsioni viene eseguito utilizzando la riduzione delle previsioni. Gli importi effettivi vengono sottratti dai saldi delle transazioni previste senza alcuna audit trail. Ciò può rendere più difficile rintracciare dove si sono verificate le transazioni effettive.                   | Nel controllo del budget di progetto, gli importi effettivi vengono sottratti dagli importi nel budget rimanente. Ciò consente un audit trail più chiaro.                                   |

## <a name="project-forecasts"></a>Previsioni di progetto
Quando utilizzi la previsione di progetto, puoi immettere transazioni di previsione nei moduli di previsione per ogni tipo di transazione. Ogni attributo disponibile per una transazione effettiva può essere utilizzato per una transazione di previsione, ad esempio, redditività della riga, attributi della riga, ruoli di lavoro o descrizioni. Puoi anche prevedere quanto tempo emettari fattura al cliente dopo aver sostenuto un costo. 

Le transazioni di previsione del progetto si basano su unità e importi. 

Devi associare ciascuna previsione di progetto a un modello di previsione. Quando immetti una transazione di previsione, viene suggerito automaticamente un modello di previsione. Il modello di previsione funge da contenitore per le transazioni di previsione. 

Puoi designare modelli di previsione come sottomodelli per un modello. In questo modo puoi effettuare previsioni per area, periodo di tempo o reparto. Puoi copiare le transazioni di previsione in un modello per creare un nuovo modello e trasferire le transazioni nella contabilità generale. Poiché esiste una relazione uno a uno tra una previsione e un modello, ogni modello di previsione crea un budget separato per un progetto. 

I modelli di previsione possono utilizzare la riduzione delle previsioni come meccanismo di controllo per i progetti. Nella riduzione di previsione, le transazioni effettive riducono i saldi delle transazioni previste. Tuttavia, poiché la riduzione della previsione viene applicata al progetto più alto nella gerarchia, fornisce una visualizzazione limitata delle modifiche nella previsione. Ad esempio, se un ruolo di lavoro è associato a un sottoprogetto, le transazioni effettive per il ruolo di lavoro vengono registrate nel progetto padre. Ciò può rendere difficile tener traccia delle modifiche, perché non è possibile determinare facilmente quale transazione in quale sottoprogetto ha causato una riduzione dell'importo previsto. Pertanto, è una buona idea creare una copia di un modello di previsione da utilizzare per la riduzione della previsione. Puoi quindi utilizzare i report per visualizzare ciò che era stato originariamente previsto. 

Puoi rivedere, copiare, eliminare o trasferire previsioni di progetto in un budget di contabilità generale. Tuttavia, non esiste alcun controllo del processo. Qualsiasi ruolo di lavoro che dispone dell'autorizzazione per un modulo di previsione può efettuare revisioni senza rivedere.

-   **Rivedi**: puoi rivedere una transazione di previsione negli stessi modui in cui sono state create le voci originali.
-   **Copia o elimina**; quando copi le transazioni di previsione, copi le righe di transazione di un modello previsionale in un altro modello di previsione. Quando elimini una previsione, elimini le transazioni di previsione da un modello di previsione. Per limitare le transazioni previste che vengono copiate o eliminate, seleziona tipi di transazione e date specifici. Ciò consente di copiare o eliminare solo parti specifiche di una previsione.
-   **Trasferisci**: quando trasferisci una previsione di progetto a un budget di contabilità generale, trasferisci le transazioni di previsione di un modello di previsione su un budget di contabilità generale. Puoi sovrascrivere qualsiasi transazione trasferita in precedenza nel budget di contabilità generale in cui trasferisci la previsione di progetto.

## <a name="project-budgets"></a>Budget di progetto
Il budget di progetto è un metodo più semplice rispetto alla previsione, sebbene si integri con i modelli previsionali. Utilizza un unico modulo di immissione per i dettagli e le revisioni del budget originale e consente proiezioni basate solo su importo, categoria o attività. 

Nella definizione del budget di progetto, tutti i budget e le revisioni originali devono essere inviati a un flusso di lavoro del progetto per l'approvazione. I flussi di lavoro offrono un maggiore controllo sul processo e creano un record della cronologia delle modifiche. 

Il budget di progetto è simile al budget di contabilità generale, ma è più veloce e facile da configurare. Molte delle opzioni nel budget della contabilità generale, come sequenze numeriche o valuta, non devono essere configurate separatamente per i progetti.

I budget di progetto vengono associati automaticamente a due modelli di previsione, uno per il budget originale e uno per il budget rimanente. Pertanto, i report basati su modelli di previsione possono utilizzare i dati di budget. Quando un budget di progetto viene impegnato, il sistema crea transazioni previsionali in base ai modelli associati, che vengono utilizzati per scopi di reporting e controllo.

## <a name="forecast-models"></a>Modelli di previsione
I modelli di previsione hanno una gerarchia a livello singolo. Ciò significa che una previsione di progetto deve essere associata a un modello di previsione.

Se utilizzi la previsione del progetto, puoi identificare i modelli come sottomodelli. Puoi quindi creare previsioni per reparto, periodo di tempo o area. Ad esempio, puoi creare un modello di previsione per un anno e quindi creare sottomodelli per le previsioni delle aree nord-est, sud-est, nord-ovest e sud-ovest inviate dalle sedi regionali. Selezionando diverse opzioni nei report disponibili, puoi visualizzare le informazioni per previsione totale o per sottomodello.



