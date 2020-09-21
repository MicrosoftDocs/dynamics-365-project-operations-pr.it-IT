---
title: Avanzamento del progetto e consumo dei costi
description: In questo argomento vengono fornite informazioni su come tenere traccia dell'avanzamento dei progetti e del consumo dei costi.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752704"
---
# <a name="project-progress-and-cost-consumption"></a>Avanzamento del progetto e consumo dei costi

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

La necessità di tenere traccia dell'avanzamento di un progetto rispetto a una pianificazione varia in base al settore di attività. Alcuni settori eseguono tale monitoraggio a un livello granulare, mentre altri lo svolgono a un livello superiore. In questo argomento viene illustrato come eseguire la pianificazione per soddisfare i requisiti dell'organizzazione.

## <a name="effort-tracking-view"></a>Vista registrazione lavoro richiesto

La vista **Registrazione lavoro richiesto** tiene traccia dell'avanzamento delle attività nella pianificazione. Questa vista confronta le ore di lavoro effettive dedicate a un'attività alle ore di lavoro previste per quell'attività. PSA utilizza le seguenti formule per calcolare le metriche di monitoraggio:

- Percentuale di avanzamento = Lavoro richiesto effettivo fino a data odierna ÷ Lavoro richiesto pianificato per l'attività 
- Stima di completamento = Lavoro richiesto pianificato - Lavoro richiesto effettivo fino a data odierna 
- Stima al completamento = Lavoro richiesto rimanente + Lavoro richiesto effettivo fino a data odierna 
- Scostamento risorse previsto = Lavoro richiesto pianificato - Stima al completamento

PSA mostra una proiezione dello scostamento risorse dell'attività. Se la stima al completamento è superiore al lavoro richiesto pianificato, si prevede che l'attività richiederà più tempo di quello inizialmente pianificato. Pertanto, è in ritardo. Se la stima al completamento è inferiore al lavoro richiesto pianificato, si prevede che l'attività richiederà meno tempo di quello inizialmente pianificato. Pertanto, è in anticipo.

## <a name="re-projecting-effort"></a>Nuova proiezione del lavoro richiesto

È normale per un responsabile di progetto aggiornare le stime originali di un'attività. Le nuove proiezioni di progetto sono la percezione delle stime di un responsabile di progetto, considerato lo stato corrente del progetto. Tuttavia, non raccomandiamo la modifica delle cifre di riferimento da parte dei responsabili di progetto, poiché la linea di base del progetto rappresenta l'origine di riferimento stabilita per la pianificazione e la stima dei costi del progetto ed è stata concordata dalle parti interessate.

Vi sono due modi per un responsabile di progetto di eseguire una nuova proiezione del lavoro richiesto per le attività:

- Sostituire la stima di completamento predefinita con una nuova stima del lavoro richiesto rimanente effettivo per l'attività. 
- Sostituire la percentuale di avanzamento predefinita con una nuova stima dell'avanzamento effettivo dell'attività.

Ognuno di questi approcci genera un nuovo calcolo di stima di completamento, stima al completamento, percentuale di avanzamento e scostamento risorse previsto dell'attività. Anche la stima di completamento, la stima al completamento e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento risorse.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Nuova proiezione del lavoro richiesto per le attività di riepilogo

È possibile eseguire una nuova proiezione del lavoro richiesto per le attività di riepilogo o le attività di contenitore. Indipendentemente dal fatto che l'utente esegua una nuova proiezione in base al lavoro richiesto rimanente o alla percentuale di avanzamento delle attività di riepilogo, viene eseguito quanto segue:

- La stima di completamento, la stima al completamento e la percentuale di avanzamento dell'attività vengono calcolate.
- La nuova stima al completamento viene distribuita alle attività figlio nella stessa proporzione della stima al completamento originale dell'attività.
- La nuova stima al completamento di ogni singola attività fino alle attività del nodo foglia viene calcolata. 
- La stima di completamento e la percentuale di avanzamento delle attività figlio interessate fino ai nodi foglia vengono ricalcolate in base al valore della stima al completamento. Ciò comporta una nuova proiezione per lo scostamento risorse dell'attività. 
- Le stime al completamento delle attività di riepilogo fino al nodo foglia vengono ricalcolate.

### <a name="cost-tracking-view"></a>Vista Registrazione costi 

La vista **Registrazione costi** confronta il costo effettivo di un'attività a quello pianificato di un'attività. 

> [!NOTE]
> Questa vista mostra solo i costi di manodopera e non include i costi dovuti alle stime di spesa. 

PSA utilizza le seguenti formule per calcolare le metriche di monitoraggio:

- Percentuale di costo consumata = Costo effettivo fino a data odierna ÷ Costo pianificato per l'attività
- Costi di completamento = Costo pianificato - Costo effettivo fino a data odierna
- Stima al completamento = Costi di completamento + Costo effettivo fino a data odierna
- Scostamento costo previsto = Costo pianificato - Stima al completamento

Una proiezione dello scostamento costo viene visualizzata per l'attività. Se la stima al completamento è superiore al costo pianificato, si prevede che l'attività costerà più di quanto inizialmente pianificato. Pertanto, la tendenza è il superamento del budget. Se la stima al completamento è inferiore al costo pianificato, si prevede che l'attività costerà meno di quanto inizialmente pianificato. Pertanto, la tendenza è il non superamento del budget.

## <a name="project-managers-re-projection-of-cost"></a>Nuova proiezione dei costi del responsabile di progetto

Quando si esegue una nuova proiezione del lavoro richiesto, i costi di completamento, la stima al completamento, la percentuale di costo consumata e lo scostamento costo previsto vengono ricalcolati nella vista **Registrazione costi**.

## <a name="project-status-summary"></a>Riepilogo dello stato del progetto

La tracciabilità dei dati nelle viste **Tracciabilità risorse** e **Tracciabilità costi** mostra l'avanzamento e il consumo dei costi a livello del nodo radice del progetto, delle attività di riepilogo e delle attività del nodo foglia. La sezione **Stato** nella pagina **Entità progetto** mostra un riepilogo dello stato a livello di progetto.

## <a name="status-summary-fields"></a>Campi di riepilogo dello stato

Il campo **Stato di progetto generale** è un campo modificabile che mostra lo stato globale del progetto. Utilizza la codifica con colori, come verde, giallo e rosso, per indicare il rischio crescente. Il campo **Commenti** consente al responsabile di progetto di immettere specifici commenti sullo stato. Il campo **Data aggiornamento stato** non è modificabile e il valore è un timestamp che indica quando lo stato è stato aggiornato per l'ultima volta.

I campi **Prestazioni di pianificazione** e **Prestazioni costo** sono impostati in base alla data di tracciabilità. Quando lo scostamento pianificazione e lo scostamento costo per il nodo radice nella vista **Tracciabilità risorse** sono positivi, puoi impostare questi campi su **In anticipo**. Quando lo scostamento pianificazione e lo scostamento costo per il nodo principale sono negativi, puoi impostarli su **In ritardo**.
