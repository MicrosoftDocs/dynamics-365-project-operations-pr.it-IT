---
title: Set di approvazioni
description: Questo argomento spiega come lavorare con i set di approvazioni, le richieste e i sottoinsiemi di tali operazioni.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323241"
---
# <a name="approval-sets"></a>Set di approvazioni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

L'approvazione consente di configurare le richieste di approvazione in sottoinsiemi di operazioni più piccoli. Questo raggruppamento consente di elaborare le approvazioni per progetto, in un ordine specifico e consente di riprovare e mettere in sequenza. Il raggruppamento delle richieste di approvazione migliora l'affidabilità e la tracciabilità del processo di approvazione per grandi volumi di approvazioni.

I set di approvazione indicano lo stato di elaborazione complessivo dei relativi record. Quando un record di approvazione viene elaborato utilizzando un set di approvazioni, il record si sposta da **Inviato** ad **Approvato** e non è più collegato al set di approvazioni. Se un record restituisce un errore quando viene presentato per l'approvazione, il record rimane in uno stato di **Inviato** e il set di approvazione è contrassegnato come non riuscito. Il set di approvazioni registra il messaggio dell'errore.

## <a name="processing-approvals-and-approval-sets"></a>Elaborazione di approvazioni e set di approvazioni
Le approvazioni in coda per l'elaborazione sono visibili nella vista **Approvazioni in elaborazione**. Il sistema elabora tutte le voci più volte in modo asincrono, inclusi i tentativi di approvazione se i tentativi precedenti non sono riusciti.

Il campo **Durata del set di approvazioni** registra il numero di tentativi rimasti per elaborare il set prima che venga contrassegnato come fallito.

## <a name="failed-approvals-and-approval-sets"></a>Approvazioni non riuscite e set di approvazioni
La vista **Approvazioni fallite** elenca tutte le approvazioni che richiedono l'intervento dell'utente. Apri i registri dei set di approvazioni associati per identificare la causa dell'errore.
Se selezioni **Riprova** viene aggiunto al conteggio della durata del set di approvazioni, riporta il set di approvazioni allo stato **Elaborazione** e tenta di elaborare i record rimanenti.

## <a name="configure-approval-sets"></a>Configurazione dei set di approvazione

### <a name="enable-the-approval-sets-feature"></a>Abilita la funzione Set di approvazioni
Prima di abilitare la funzione Set di approvazioni, verifica che non vi siano approvazioni in corso di elaborazione.

- Vai alla pagina **Parametri progetto** e seleziona **Controllo funzionalità** > **Abilita approvazioni moderne**.

### <a name="turn-off-the-approval-sets-feature"></a>Disabilita la funzione Set di approvazioni
Prima di disabilitare la funzione Set di approvazioni, verifica che non vi siano approvazioni in corso di elaborazione.

- Vai alla pagina **Parametri progetto** e seleziona **Controllo funzionalità** > **Disabilita approvazioni moderne**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurazione della soglia asincrona 
Quando vengono creati i set di approvazioni, l'elaborazione passa in background quando il numero selezionato di record per l'approvazione supera la soglia indicata. Usa il campo **Soglia asincrona** per configurare quando l'elaborazione dell'approvazione deve essere eseguita in modo sincrono o asincrono. Seleziona uno dei valori seguenti:

  - Zero: tutte le richieste devono essere elaborate in modo asincrono. 
  - Numeri maggiori di zero: le approvazioni vengono elaborate in modo asincrono solo quando il numero di approvazioni inviato supera questo valore.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
