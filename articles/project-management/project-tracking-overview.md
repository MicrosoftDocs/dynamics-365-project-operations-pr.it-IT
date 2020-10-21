---
title: Panoramica della registrazione di progetto
description: In questo argomento vengono fornite informazioni su come tenere traccia dell'avanzamento dei progetti e del consumo dei costi.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907368"
---
# <a name="project-tracking-overview"></a>Panoramica della registrazione di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

La necessità di tenere traccia dell'avanzamento di un progetto rispetto a una pianificazione varia in base al settore di attività. Alcuni settori eseguono tale monitoraggio a un livello granulare, mentre altri lo svolgono a un livello superiore. In questo argomento viene illustrato come eseguire la pianificazione per soddisfare i requisiti dell'organizzazione.

## <a name="effort-tracking-view"></a>Vista registrazione lavoro richiesto

La vista **Registrazione lavoro richiesto** tiene traccia dell'avanzamento delle attività nella pianificazione confrontando le ore di lavoro effettive spese per un'attività con le ore di lavoro pianificate dell'attività. Dynamics 365 Project Operations utilizza le seguenti formule per calcolare le metriche di monitoraggio:

- **Percentuale di avanzamento**: lavoro richiesto effettivo fino a data odierna ÷ stima al completamento 
- **Stima di completamento**: lavoro richiesto pianificato - lavoro richiesto effettivo fino a data odierna 
- **Stima al completamento**: lavoro richiesto rimanente + lavoro richiesto effettivo fino a data odierna 
- **Scostamento risorse previsto**: lavoro richiesto pianificato - stima al completamento

Project Operations mostra una proiezione dello scostamento risorse dell'attività. Se la stima al completamento è superiore al lavoro richiesto pianificato, si prevede che l'attività richiederà più tempo di quello inizialmente pianificato. Se la stima al completamento è inferiore al lavoro richiesto pianificato, si prevede che l'attività richiederà meno tempo di quello inizialmente pianificato.

## <a name="reprojecting-effort"></a>Nuova proiezione del lavoro richiesto

I responsabili di progetto aggiornano spesso le stime originali di un'attività. Le nuove proiezioni di progetto sono la percezione delle stime di un responsabile di progetto, considerato lo stato corrente del progetto. Tuttavia, non è consigliabile che i responsabili di progetto modifichino le cifre di riferimento. Questo perché la linea di base del progetto rappresenta l'origine di riferimento stabilita per la pianificazione e la stima dei costi del progetto ed è stata concordata dalle parti interessate.

Vi sono due modi per un responsabile di progetto di eseguire una nuova proiezione del lavoro richiesto per le attività:

- Sostituire la stima di completamento predefinita con una nuova stima del lavoro richiesto rimanente effettivo per l'attività. 
- Sostituire la percentuale di avanzamento predefinita con una nuova stima dell'avanzamento effettivo dell'attività.

Ogni approccio genera un nuovo calcolo di stima di completamento, stima al completamento, percentuale di avanzamento e scostamento risorse previsto dell'attività. Anche la stima di completamento, la stima al completamento e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento risorse.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nuova proiezione del lavoro richiesto per le attività di riepilogo

È possibile eseguire una nuova proiezione del lavoro richiesto per le attività di riepilogo o le attività di contenitore. Indipendentemente dal fatto che l'utente esegua una nuova proiezione in base al lavoro richiesto rimanente o alla percentuale di avanzamento delle attività di riepilogo, viene eseguito quanto segue:

- La stima di completamento, la stima al completamento e la percentuale di avanzamento dell'attività vengono calcolate.
- La nuova stima al completamento viene distribuita alle attività figlio nella stessa proporzione della stima al completamento originale dell'attività.
- La nuova stima al completamento di ogni singola attività fino alle attività del nodo foglia viene calcolata. 
- La stima di completamento e la percentuale di avanzamento delle attività figlio interessate fino ai nodi foglia vengono ricalcolate in base al valore della stima al completamento. Ciò comporta una nuova proiezione per lo scostamento risorse dell'attività. 
- Le stime al completamento delle attività di riepilogo fino al nodo foglia vengono ricalcolate.

### <a name="cost-tracking-view"></a>Vista Registrazione costi 

La vista **Registrazione costi** confronta il costo effettivo di un'attività a quello pianificato di un'attività. 

> [!NOTE]
> Questa vista mostra solo i costi di manodopera e non include i costi dovuti alle stime di spesa. Project Operations utilizza le seguenti formule per calcolare le metriche di monitoraggio:

- **Percentuale di costo consumata**: costo effettivo fino a data odierna ÷ costo pianificato al completamento
- **Costi di completamento**: costo pianificato - costo effettivo fino a data odierna
- **Stima al completamento**: costo rimanente + costo effettivo fino a data odierna
- **Scostamento costo previsto**: costo pianificato - stima al completamento

Una proiezione dello scostamento costo viene visualizzata per l'attività. Se la stima al completamento è superiore al costo pianificato, si prevede che l'attività costerà più di quanto inizialmente pianificato. Pertanto, la tendenza è il superamento del budget. Se la stima al completamento è inferiore al costo pianificato, si prevede che l'attività costerà meno di quanto inizialmente pianificato. Pertanto, la tendenza è il non superamento del budget.

## <a name="project-managers-reprojection-of-cost"></a>Nuova proiezione dei costi del responsabile di progetto

Quando si esegue una nuova proiezione del lavoro richiesto, i costi di completamento, la stima al completamento, la percentuale di costo consumata e lo scostamento costo previsto vengono ricalcolati nella vista **Registrazione costi**.

## <a name="project-status-summary"></a>Riepilogo dello stato del progetto

La tracciabilità dei dati nelle viste **Tracciabilità risorse** e **Tracciabilità costi** mostra l'avanzamento e il consumo dei costi a livello del nodo radice del progetto, delle attività di riepilogo e delle attività del nodo foglia. La sezione **Stato** nella pagina **Entità progetto** mostra un riepilogo dello stato a livello di progetto.

## <a name="status-summary-fields"></a>Campi di riepilogo dello stato

Il campo **Stato di progetto generale** è un campo modificabile che mostra lo stato globale del progetto. Utilizza la codifica con colori, come verde, giallo e rosso, per indicare il rischio crescente. Il campo **Commenti** consente al responsabile di progetto di immettere specifici commenti sullo stato. Il campo **Data aggiornamento stato** non è modificabile e il valore è un timestamp che indica quando lo stato è stato aggiornato per l'ultima volta.

I campi **Prestazioni di pianificazione** e **Prestazioni costo** sono impostati in base alla data di tracciabilità. Quando lo scostamento pianificazione e lo scostamento costo per il nodo radice nella vista **Tracciabilità risorse** sono positivi, puoi impostare questi campi su **In anticipo**. Quando lo scostamento pianificazione e lo scostamento costo per il nodo principale sono negativi, puoi impostarli su **In ritardo**.
