---
title: Registrazione dei costi di progetto
description: Questo argomento fornisce informazioni su come Project Operations registra l'avanzamento rispetto al costo e alla spesa di manodopera in un progetto.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d37df64db1808722b7851c952c20be731aa2d670fe066c02ef90386712487407
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987801"
---
# <a name="labor-cost-tracking-on-projects"></a>Registrazione del costo di manodopera nei progetti

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations registra le stime e le spese di manodopera con la granularità più bassa richiesta nel piano di progetto. La stima finanziaria del costo di manodopera si basa sul lavoro richiesto pianificato e sulle risorse generiche o denominate assegnate a ciascuna attività del nodo foglia nel piano di progetto. Quando il progetto ha inizio e le persone cominciano a segnalare il tempo di varie attività del progetto, viene riepilogata la spesa effettiva di manodopera che avvia un calcolo delle proiezioni.

## <a name="labor-cost-tracking-view"></a>Visualizzazione Registrazione costo di manodopera

Nella pagina **Progetti**, nella scheda **Registrazione**, puoi selezionare **Registrazione** > **Costo** per aprire la visualizzazione **Registrazione costi** e vedere l'avanzamento della spesa di manodopera in ogni attività nel piano di progetto. Questa visualizzazione confronta anche il costo di manodopera effettivo speso per un'attività al costo di manodopera pianificato dell'attività. Project Operations utilizza le seguenti formule per calcolare le metriche del costo di manodopera:

- **Costo pianificato**: costo stimato di tutte le assegnazioni di risorse in ciascuna attività del nodo foglia
- **Costo effettivo**: somma di tutti i valori effettivi del costo per il tempo registrato nell'attività
- **Percentuale consumo costi**: costo effettivo ÷ stima costo al completamento
- **Costo rimanente**: stima costo al completamento - costo effettivo
- **Costo al completamento**: costo rimanente + costo effettivo
- **Scostamento costo**: costo pianificato - costo stima al completamento

Ogni attività mostra una proiezione dello scostamento costo nell'attività. Se la stima del costo al completamento è superiore al costo pianificato, si prevede che l'attività supererà il budget. Se la stima del costo al completamento è inferiore al costo pianificato, si prevede che l'attività non supererà il budget.

>[!NOTE]
> Project Operations mostra solo i costi manodopera nella pagina **Progetto** della scheda **Registrazione**. Sebbene i materiali e le spese possano essere stimati e registrati per il consumo, questi costi non sono inclusi in quelli mostrati nella scheda **Registrazione**. Questa scheda è progettata per funzionare solo per riproiettare i costi manodopera riproiettando il lavoro richiesto.
Tutti gli importi di costo visualizzati vengono convertiti nella valuta DI costo del progetto dalla valuta del prezzo di costo del progetto utilizzata per determinare il tasso di costo. La valuta di costo del progetto è la valuta dell'unità contratto del progetto. È possibile che i valori del costo stimato per il tempo visualizzati nella scheda **Stime** della pagina **Progetto** non vengano sommati al costo pianificato nella scheda **Registrazione**. La ragione di questa discrepanza è dovuta alle differenze nel modo in cui il costo stimato viene riepilogato nella griglia **Stime** e nel modo in cui il costo pianificato viene calcolato nella griglia **Registrazione**. 
>
> - La **scheda Stime** calcola il costo stimato utilizzando la stessa valuta del tasso di costo nel listino prezzi. Quindi, il costo stimato nella valuta del listino prezzi viene convertito nel costo stimato nella valuta del costo del progetto. Il costo stimato nella valuta del progetto viene mostrato arrotondato a 2 cifre decimali. In nessun momento durante questa conversione viene applicata la precisione della valuta. 
> - Nella scheda **Registrazione**, il calcolo del costo pianificato segue un ordine di calcolo leggermente diverso che prevede l'applicazione della precisione della valuta in due fasi: 
   ><ol>
   ><li>L'importo del costo stimato nella valuta del listino prezzi viene convertito nella valuta base (conversione 1).</li>
   ><li>L'importo del costo stimato nella valuta di base viene convertito nella valuta del costo di progetto (conversione 2). </li>
   ></ol>
   >La precisione della valuta viene applicata in entrambi i passaggi per ottenere un costo pianificato (nella scheda **Registrazione**) che si discosta leggermente dal costo stimato (nella visualizzazione **Scala cronologica** della scheda **Stime**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Riproiezione dei costi nelle attività del nodo foglia

Non è possibile eseguire una riproiezione dei costi di manodopera in un'attività del nodo foglia direttamente nella scheda **Registrazione** della pagina **Progetto**. Tuttavia, puoi usare la visualizzazione **Registrazione lavoro richiesto** per riproiettare il lavoro richiesto rimanente in un'attività. Ciò causa un ricalcolo del costo rimanente nell'attività. Quanto segue è una descrizione di tale ricalcolo.

1. Un responsabile di progetto può riproiettare il lavoro richiesto nelle attività aggiornando il valoro predefinito nel campo **Lavoro richiesto rimanente** con una nuova stima del lavoro richiesto rimanente dell'attività. La riproiezione genera un ricalcolo della stima del lavoro richiesto al completamento dell'attività, della percentuale di avanzamento e dello scostamento del lavoro richiesto proiettato di un'attività. La stima al completamento, la stima da completare e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento del lavoro richiesto.
2. In base al nuovo valore per il lavoro richiesto rimanente nell'attività, il sistema calcola il costo rimanente nella visualizzazione **Registrazione costi**. Per calcolare il costo rimanente in base la lavoro richiesto rimanente, il sistema calcola innanzitutto il costo medio di un'ora di lavoro richiesto nell'attività come costo pianificato o lavoro richiesto pianificato. Il costo pianificato è la somma del costo di tutte le assegnazioni di risorse nell'attività. Il costo medio orario viene utilizzato per calcolare il costo rimanente del lavoro richiesto appena proiettato nell'attività.
3. Il costo al completamento e la percentuale di consumo costi nell'attività del nodo foglia vengono ricalcolati.
4. Il valore del costo al completamento delle attività di riepilogo fino al nodo foglia viene ricalcolato.

## <a name="reprojecting-costs-on-summary-tasks"></a>Riproiezione dei costi nelle attività di riepilogo

Puoi riproiettare i costi di manodopera nelle attività di riepilogo o nelle attività contenitore. Tuttavia, non puoi riproiettare direttamente il costo della manodopera in un'attività di progetto di riepilogo nella scheda **Registrazione** della pagina **Progetto**. Analogamente alle attività del nodo foglia, è possibile riproiettare attività di riepilogo e contenitore utilizzando la visualizzazione **Registrazione lavoro richiesto**. In questa visualizzazione, puoi riproiettare il lavoro richiesto rimanente in un'attività di riepilogo provocando un ricalcolo del costo rimanente nell'attività di riepilogo. Quanto segue è una descrizione di tale ricalcolo.

1. Un responsabile di progetto può riproiettare il lavoro richiesto nelle attività di riepilogo aggiornando il valore predefinito del lavoro richiesto rimanente con una nuova stima dell'attività. Questo aggiornamento genera un nuovo calcolo della stima al completamento dell'attività di riepilogo, della percentuale di avanzamento e dello scostamento del lavoro richiesto proiettato in un'attività. Anche la stima di completamento, la stima da completare e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento del lavoro richiesto.
2. In base al nuovo valore per il lavoro richiesto rimanente nell'attività di riepilogo, il sistema calcola il costo rimanente nella visualizzazione **Registrazione costi**. Per calcolare il costo rimanente in base la lavoro richiesto rimanente, il sistema calcola innanzitutto il costo medio di un'ora di lavoro richiesto nell'attività di riepilogo come costo pianificato o lavoro richiesto pianificato. Il costo medio orario viene utilizzato per calcolare il costo del lavoro richiesto appena proiettato nell'attività di riepilogo.
3. Il costo al completamento e la percentuale di consumo costi nell'attività di riepilogo del nodo foglia vengono ricalcolati.
4. Il nuovo costo al completamento viene distribuito alle attività figlio nella stessa proporzione del costo pianificato originale nell'attività.
5. Viene calcolato il nuovo valore del costo al completamento di ogni singola attività fino alle attività del nodo foglia. In base a questo valore, per le attività figlio interessate fino ai nodi foglia verranno ricalcolati il costo rimanente e la percentuale di consumo costi in base al valore del costo al completamento. Questo valore comporta una nuova proiezione per lo scostamento costo dell'attività. 


Il campo **Prestazioni costo** può essere impostato dai dati di registrazione. Quando lo scostamento costo per il nodo radice nella visualizzazione **Registrazione costi** è negativo, puoi impostare questo campo su **Sotto budget**. Quando lo scostamento costo per il nodo radice è positivo, è possibile impostare il valore su **Oltre budget**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
