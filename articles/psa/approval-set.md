---
title: Set di approvazioni
description: Questo argomento fornisce informazioni sul set di approvazioni, le richieste e i sottoinsiemi di tali operazioni.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e57944b3031ff8b6da163125bb6668875ae77bd06f23a5b8c4ef06f396210e4f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995496"
---
# <a name="approval-sets"></a>Set di approvazioni

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

L'approvazione consente di configurare le richieste di approvazione in sottoinsiemi di operazioni più piccoli. Questo raggruppamento consente di elaborare le approvazioni in ordine per Progetto e consente di ripristinare e mettere in sequenza. Il raggruppamento migliora l'affidabilità e la tracciabilità del processo di approvazione per grandi volumi di approvazioni.

I set di approvazione indicano lo stato di elaborazione complessivo dei relativi record. Quando un record di approvazione viene elaborato utilizzando un set di approvazione, il record si sposta da **Inviato** in **Approvato** e viene scollegato dal set di approvazioni. Se un record restituisce un errore quando viene presentato per l'approvazione, il record rimane in uno stato di **Inviato** e il set di approvazione è contrassegnato come non riuscito. Il set di approvazioni registra il messaggio dell'errore.

## <a name="processing-approvals-and-approval-sets"></a>Elaborazione di approvazioni e set di approvazioni
Le approvazioni in coda per l'elaborazione sono visibili nella vista **Approvazioni in elaborazione**. Il sistema tenta di elaborare tutte le voci più volte in modo asincrono, incluso un nuovo tentativo di approvazione se i tentativi precedenti non sono riusciti.

Il campo **Durata del set di approvazioni** registra il numero di tentativi rimasti per elaborare il set prima che venga contrassegnato come fallito.

## <a name="failed-approvals-and-approval-sets"></a>Approvazioni non riuscite e set di approvazioni
La vista **Approvazioni non riuscite** elenca tutte le approvazioni che richiedono l'intervento dell'utente. Apri i registri dei set di approvazioni associati per identificare la causa dell'errore.
Se selezioni **Riprova** viene aggiunto al conteggio della durata del set di approvazioni, riporta il set di approvazioni allo stato **Elaborazione** e tenta di elaborare i record rimanenti.

## <a name="configure-approval-sets"></a>Configurazione dei set di approvazione

###  <a name="enable-the-approval-sets-feature"></a>Abilita la funzione Set di approvazioni
Prima di abilitare la funzione Set di approvazioni, verifica che non vi siano approvazioni in corso di elaborazione.

- Vai alla pagina **Parametri progetto** e seleziona **Controllo funzionalità** > **Abilita approvazioni moderne**.

### <a name="turn-off-the-approval-sets-feature"></a>Disabilita la funzione Set di approvazioni
Prima di disabilitare la funzione Set di approvazioni, verifica che non vi siano approvazioni in corso di elaborazione.

- Vai alla pagina **Parametri progetto** e seleziona **Controllo funzionalità** > **Disabilita approvazioni moderne**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurazione della soglia asincrona 
Quando vengono creati i set di approvazioni, l'elaborazione passa in background quando il numero selezionato di record per l'approvazione supera la soglia indicata. Usa il campo **Soglia asincrona** per configurare quando l'elaborazione dell'approvazione deve essere eseguita in modo sincrono o asincrono.
Valori validi:

  - Zero: tutte le richieste devono essere elaborate in modo asincrono. 
  - Numeri maggiori di zero: le approvazioni vengono elaborate in modo asincrono solo quando il numero di approvazioni inviato supera questo valore.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
