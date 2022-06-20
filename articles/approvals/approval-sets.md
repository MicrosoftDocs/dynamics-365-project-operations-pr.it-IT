---
title: Set di approvazioni
description: Questo articolo spiega come lavorare con set di approvazione, richieste e sottoinsiemi di tali operazioni.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 5e030c1aa4a41b428a0f4541fd204a7a3deaba08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918087"
---
# <a name="approval-sets"></a>Set di approvazioni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

L'approvazione consente di configurare le richieste di approvazione in sottoinsiemi di operazioni più piccoli. Questo raggruppamento consente di elaborare le approvazioni per progetto, in un ordine specifico e consente di riprovare e mettere in sequenza. Il raggruppamento delle richieste di approvazione migliora l'affidabilità e la tracciabilità del processo di approvazione per grandi volumi di approvazioni.

I set di approvazione indicano lo stato di elaborazione complessivo dei relativi record. Quando un record di approvazione viene elaborato utilizzando un set di approvazioni, il record si sposta da **Inviato** ad **Approvato** e non è più collegato al set di approvazioni. Se un record restituisce un errore quando viene presentato per l'approvazione, il record rimane in uno stato di **Inviato** e il set di approvazione è contrassegnato come non riuscito. Il set di approvazioni registra il messaggio dell'errore.

## <a name="processing-approvals-and-approval-sets"></a>Elaborazione di approvazioni e set di approvazioni
Le approvazioni in coda per l'elaborazione sono visibili nella vista **Approvazioni in elaborazione**. Il sistema elabora tutte le voci più volte in modo asincrono, inclusi i tentativi di approvazione se i tentativi precedenti non sono riusciti.

Il campo **Durata del set di approvazioni** registra il numero di tentativi rimasti per elaborare il set prima che venga contrassegnato come fallito.

I set di approvazione vengono elaborati attraverso l'attivazione periodica basata su un **Flusso cloud** denominato **Project Service - Pianifica in modo ricorrente i set di approvazioni progetto**. Questo si trova nella **Soluzione** denominata **Project Operations**. 

Assicurati che il flusso sia attivato completando i seguenti passaggi.

1. Come amministratore, accedi a [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Nell'angolo in alto a destra, passa all'ambiente che usi per Dynamics 365 Project Operations.
3. Seleziona **Soluzioni** per elencare le soluzioni installate nell'ambiente.
4. Nell'elenco delle soluzioni, seleziona **Project Operations**.
5. Passare dal filtro **Tutto** al filtro **Flussi cloud**.
6. Verifica che il flusso **Project Service - Pianifica in modo ricorrente i set di approvazioni progetto** sia impostata su **Attivato**. In caso contrario, seleziona il flusso, quindi seleziona **Attiva**.
7. Verificare che l'elaborazione avvenga ogni cinque minuti esaminando l'elenco **Processi di sistema** nell'area **Impostazioni** all'interno dell'ambiente Dataverse di Project Operations.

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
