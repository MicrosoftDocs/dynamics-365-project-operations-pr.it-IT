---
title: Registrazione delle vendite di progetto
description: Questo argomento fornisce informazioni su come Project Operations registra l'avanzamento rispetto al ricavo manodopera in un progetto.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fff5fa6b12dddd780eb6bf77edca85a3a0c0629c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583451"
---
# <a name="project-sales-tracking"></a>Registrazione delle vendite di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations tiene traccia delle stime relative alla manodopera e delle entrate con la granularità più bassa richiesta in un piano di progetto. La stima del ricavo manodopera si basa sul lavoro richiesto pianificato e sulle risorse generiche o denominate assegnate a ciascuna attività del nodo foglia nel piano di progetto. Quando il progetto ha inizio e le persone cominciano a segnalare il tempo di varie attività del progetto, viene riepilogato il ricavo manodopera effettivo che avvia un calcolo delle proiezioni.

## <a name="labor-revenue-tracking-view"></a>Visualizzazione della registrazione del ricavo manodopera

Nella pagina **Progetti**, nella scheda **Registrazione**, puoi selezionare **Registrazione** > **Costo** per aprire la visualizzazione **Registrazione costi**. Oppure puoi selezionare **Uso** > **Tasso di fatturazione** per aprire la visualizzazione **Registrazione ricavo**, che mostra l'avanzamento del ricavo manodopera in ciascuna attività nel piano di progetto. Questa visualizzazione confronta anche il ricavo manodopera effettivo speso per un'attività al ricavo manodopera pianificato dell'attività. Project Operations utilizza le seguenti formule per calcolare le metriche del ricavo manodopera:

- **Ricavi pianificati**: valori di vendita stimati di tutte le assegnazioni di risorse in ciascuna attività del nodo foglia
- **Ricavi effettivi**: somma di tutti i valori effettivi delle vendite non fatturate per il tempo registrato nell'attività
- **Ricavi fatturabili %**: ricavo effettivo ÷ stima ricavo al completamento
- **Ricavi rimanenti**: stima ricavo al completamento - ricavo effettivo
- **Ricavi stimati al completamento**: ricavo rimanente + ricavo effettivo
- **Scostamento ricavi**: ricavo pianificato - ricavo stimato al completamento


> [!NOTE]
> Project Operations mostra solo i ricavi manodopera nella pagina **Progetto** della scheda **Registrazione**. Sebbene i materiali e le spese possano essere stimati e registrati per il consumo, questi ricavi non sono inclusi in quelli mostrati nella scheda **Registrazione**. Questa scheda è progettata per funzionare solo per riproiettare i ricavi manodopera riproiettando il lavoro richiesto.  
> Tutti gli importi dei ricavi visualizzati vengono convertiti nella valuta di costo del progetto. La valuta di costo del progetto è la valuta dell'unità contratto del progetto. Per i progetti a prezzo fisso, i dati dei ricavi nella visualizzazione **Registrazione ricavi manodopera** non sono pertinenti perché i valori effettivi di vendite non fatturate non vengono registrati nell'approvazione del tempo.
> I valori di vendita stimati per il tempo visualizzati nella scheda **Stima** del progetto potrebbe non sommarsi al valore dei ricavi pianificati nella scheda **Registrazione**. Il motivo di questa discrepanza è dovuta a due possibili ragioni:
><ol>
   ><li> La scheda <b>Stime</b> mostra il ricavo stimato nella valuta di vendita, mentre la scheda <b>Registrazione</b> mostra il ricavo pianificato convertito nella valuta di costo. </li>
   ><li> Quando le vendite stimate vengono convertite dalla valuta del contratto visualizzata nella scheda <b>Stime</b> nella valuta del progetto, la conversione prevede passaggi che potrebbero comportare una certa perdita di precisione: </li>
><ol>
><li> L'importo delle vendite stimato nella valuta del contratto viene prima convertito nella valuta di base (conversione 1).</li>
><li> L'importo delle vendite stimato nella valuta di base viene convertito nella valuta di costo del progetto (conversione 2). </li>
></ol>
></ol>
> La precisione della valuta viene applicata in entrambi i passaggi, il che si traduce in una deviazione del ricavo pianificato nella valuta del progetto dalle vendite pianificate nella valuta del contratto.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Riproiezione dei ricavi nelle attività del nodo foglia

I ricavi manodopera in un'attività del nodo foglia non possono essere riproiettati direttamente nella scheda **Registrazione** della pagina **Progetto**. Tuttavia, puoi usare la visualizzazione **Registrazione lavoro richiesto** per riproiettare il lavoro richiesto rimanente in un'attività. Ciò causa un ricalcolo del ricavo rimanente dell'attività. Quanto segue è una descrizione di tale ricalcolo.

1. Un responsabile di progetto può riproiettare il lavoro richiesto nelle attività aggiornando il valoro predefinito nel campo **Lavoro richiesto rimanente** con una nuova stima del lavoro richiesto rimanente dell'attività. La riproiezione genera un ricalcolo della stima del lavoro richiesto al completamento dell'attività, della percentuale di avanzamento e dello scostamento del lavoro richiesto proiettato di un'attività. La stima al completamento, la stima da completare e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento del lavoro richiesto.
2. In base al nuovo valore per il lavoro richiesto rimanente nell'attività, il sistema calcola il ricavo rimanente nella visualizzazione **Registrazione ricavi**. Per calcolare il ricavo rimanente in base la lavoro richiesto rimanente, il sistema calcola innanzitutto il ricavo medio di un'ora di lavoro richiesto nell'attività come ricavo pianificato o lavoro richiesto pianificato. Il ricavo pianificato è la somma dei ricavi di tutte le assegnazioni di risorse nell'attività. Il ricavo medio orario viene utilizzato per calcolare il ricavo rimanente del lavoro richiesto appena proiettato nell'attività.
3. Il ricavo stimato al completamento e la percentuale di consumo del ricavo nell'attività del nodo foglia vengono ricalcolati.
4. Il valore del ricavo al completamento delle attività di riepilogo fino al nodo foglia viene ricalcolato.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Riproiezione dei ricavi nelle attività di riepilogo

Puoi riproiettare il ricavo manodopera nelle attività di riepilogo o nelle attività contenitore. Tuttavia, non puoi riproiettare direttamente i ricavi manodopera in un'attività di progetto di riepilogo nella scheda **Registrazione** della pagina **Progetto**. Analogamente alle attività del nodo foglia, è possibile riproiettare attività di riepilogo e contenitore utilizzando la visualizzazione **Registrazione lavoro richiesto**. In questa visualizzazione, è possibile riproiettare il lavoro richiesto rimanente in un'attività di riepilogo provocando un ricalcolo del ricavo rimanente nell'attività di riepilogo. Quanto segue è una descrizione di tale ricalcolo.

1. Un responsabile di progetto può riproiettare il lavoro richiesto nelle attività aggiornando il valoro predefinito nel campo **Lavoro richiesto rimanente** con una nuova stima del **Lavoro richiesto rimanente** dell'attività. La riproiezione genera un ricalcolo della stima al completamento dell'attività, della percentuale di avanzamento e dello scostamento del lavoro richiesto proiettato di un'attività. Anche la stima di completamento, la stima da completare e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento del lavoro richiesto.
2. In base al nuovo valore nel campo **Lavoro richiesto rimanente** nell'attività, il sistema calcola il ricavo rimanente nella visualizzazione **Registrazione ricavo**. Per calcolare il ricavo rimanente in base la lavoro richiesto rimanente, il sistema calcola innanzitutto il ricavo medio di un'ora di lavoro richiesto nell'attività come ricavo pianificato o lavoro richiesto pianificato. Il ricavo pianificato è la somma dei ricavi di tutte le assegnazioni di risorse nell'attività. Questo ricavo medio orario viene quindi utilizzato per calcolare il ricavo del lavoro richiesto appena proiettato nell'attività.
3. Il ricavo stimato al completamento e la percentuale di consumo del ricavo nell'attività di riepilogo vengono ricalcolati.
4. Il nuovo valore per il ricavo stimato al completamento viene distribuito alle attività figlio nella stessa proporzione del ricavo pianificato originale nell'attività.
5. Viene calcolato il nuova ricavo stimato al completamento di ogni singola attività fino alle attività del nodo foglia. In base a questo valore, per le attività figlio interessate fino ai nodi foglia verranno ricalcolati il ricavo rimanente e la percentuale di consumo del ricavo in base al valore del ricavo al completamento. Ciò comporta una nuova proiezione per lo scostamento del ricavo dell'attività. 
6. Il valore del ricavo al completamento delle attività di riepilogo fino al nodo foglia viene ricalcolato.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

