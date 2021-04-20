---
title: Registrazione del lavoro richiesto di progetto
description: In questo argomento vengono fornite informazioni su come registrare il lavoro richiesto di progetto e l'avanzamento del lavoro.
author: ruhercul
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ead8821c8861ded1e7afd5c192af414f758edef9
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2021
ms.locfileid: "5710945"
---
# <a name="project-effort-tracking"></a>Registrazione del lavoro richiesto di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

La necessità di tenere traccia dell'avanzamento di un progetto rispetto a una pianificazione varia in base al settore di attività. Alcuni settori eseguono tale monitoraggio a un livello granulare, mentre altri lo svolgono a un livello superiore. In questo argomento viene illustrato come eseguire la pianificazione per soddisfare i requisiti dell'organizzazione.

## <a name="effort-tracking-view"></a>Vista registrazione lavoro richiesto

La vista **Registrazione lavoro richiesto** tiene traccia dell'avanzamento delle attività nella pianificazione confrontando le ore di lavoro effettive spese per un'attività con le ore di lavoro pianificate dell'attività. Dynamics 365 Project Operations utilizza le seguenti formule per calcolare le metriche di monitoraggio:

- **Percentuale di avanzamento**: lavoro richiesto effettivo fino a data odierna ÷ stima al completamento 
- **Lavoro richiesto rimanente**: lavoro richiesto stimato al completamento - lavoro richiesto effettivo fino a data odierna 
- **Stima al completamento**: lavoro richiesto rimanente + lavoro richiesto effettivo fino a data odierna 
- **Scostamento lavoro richiesto previsto**: lavoro richiesto pianificato - stima al completamento

Project Operations mostra una proiezione dello scostamento del lavoro richiesto dell'attività. Se la stima al completamento è superiore al lavoro richiesto pianificato, si prevede che l'attività richiederà più tempo di quello inizialmente pianificato. Se la stima al completamento è inferiore al lavoro richiesto pianificato, si prevede che l'attività richiederà meno tempo di quello inizialmente pianificato.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Riproiezione del lavoro richiesto nelle attività del nodo foglia

I responsabili di progetto aggiornano spesso le stime originali di un'attività. Le riproiezioni di progetto sono la percezione delle stime di un responsabile di progetto, considerato lo stato corrente del progetto. Tuttavia, non consigliamo ai responsabili di progetto di modificare i dati del lavoro richiesto pianificato. Questo perché il lavoro richiesto pianificato del progetto rappresenta l'origine di riferimento stabilita per la pianificazione del progetto e la stima dei costi, e tutte le parti interessate del progetto l'hanno accettata.

Un responsabile di progetto può riproiettare il lavoro richiesto sulle attività aggiornando il **Lavoro richiesto rimanente** predefinito con una nuova stima dell'attività. Questo aggiornamento genera un nuovo calcolo della stima al completamento dell'attività, della percentuale di avanzamento e dello scostamento del lavoro richiesto proiettato di un'attività. Anche la stima al completamento, la stima da completare e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento del lavoro richiesto.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Riproiezione del lavoro richiesto per le attività di riepilogo

È possibile eseguire una riproiezione del lavoro richiesto per le attività di riepilogo o le attività di contenitore. I responsabili di progetto possono aggiornare il lavoro richiesto rimanente nelle attività di riepilogo. L'aggiornamento del lavoro richiesto rimanente attiva la seguente serie di calcoli nell'applicazione:

- La stima al completamento e la percentuale di avanzamento dell'attività vengono calcolate.
- La nuova stima al completamento viene distribuita alle attività figlio nella stessa proporzione della stima al completamento originale dell'attività.
- La nuova stima al completamento di ogni singola attività fino alle attività del nodo foglia viene calcolata. 
- Il lavoro richiesto rimanente e la percentuale di avanzamento delle attività figlio interessate fino ai nodi foglia vengono ricalcolate in base al valore della stima al completamento. Ciò comporta una nuova proiezione per lo scostamento del lavoro richiesto dell'attività. 
- Le stime al completamento delle attività di riepilogo fino al nodo foglia vengono ricalcolate.


## <a name="project-status-summary"></a>Riepilogo dello stato del progetto

La registrazione dei dati nelle viste **Registrazione lavoro richiesto** e **Registrazione costi** mostra l'avanzamento e il consumo dei costi a livello del nodo radice del progetto, delle attività di riepilogo e delle attività del nodo foglia. La sezione **Stato** nella pagina **Entità progetto** mostra un riepilogo dello stato a livello di progetto.

## <a name="status-summary-fields"></a>Campi di riepilogo dello stato

Il campo **Stato di progetto generale** è un campo modificabile che mostra lo stato globale del progetto. Utilizza la codifica con colori, come verde, giallo e rosso, per indicare il rischio crescente. Il campo **Commenti** consente al responsabile di progetto di immettere specifici commenti sullo stato. Il campo **Data aggiornamento stato** non è modificabile e il valore è un timestamp che indica quando lo stato è stato aggiornato per l'ultima volta.

I campi **Prestazioni di pianificazione** e **Prestazioni costo** sono impostati in base alla data di registrazione. Quando lo scostamento pianificazione e lo scostamento costo per il nodo radice nella vista **Registrazione lavoro richiesto** sono positivi, puoi impostare questi campi su **In anticipo**. Quando lo scostamento pianificazione e lo scostamento costo per il nodo principale sono negativi, puoi impostarli su **In ritardo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
