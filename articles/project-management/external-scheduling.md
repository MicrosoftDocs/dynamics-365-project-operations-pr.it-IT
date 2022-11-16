---
title: Pianificazione esterna
description: Questo articolo fornisce informazioni sulle modalità di pianificazione esterna.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736965"
---
# <a name="external-scheduling"></a>Pianificazione esterna

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

La modalità di pianificazione esterna consente di creare, aggiornare ed eliminare in modo nativo entità correlate alle strutture di suddivisione del lavoro (WBS), ma senza gli attuali limiti imposti da Microsoft Project for the Web. Fornisce inoltre una convalida limitata. Questa modalità deve essere utilizzata solo dai seguenti clienti:

- Clienti che dispongono degli strumenti necessari per definire una struttura di suddivisione del lavoro al di fuori della logica di pianificazione fornita da Project Operations
- Clienti che devono gestire la gerarchia di pianificazione, le dipendenze o la durata delle attività

> [!IMPORTANT]
> I dati non inseriti correttamente nelle entità correlate alla struttura di suddivisione del lavoro potrebbero non essere visualizzati nella griglia di riconciliazione delle risorse, nella griglia delle stime, nella griglia di rilevamento o nella griglia di assegnazione delle risorse.

## <a name="configuration"></a>Configuration

Questa funzionalità è abilitata per impostazione predefinita. Tuttavia, nella pagina principale predefinita per i progetti, il campo correlato non è visibile per impostazione predefinita. Per abilitare il campo, nel Maker Portal, apri la pagina principale dell'entità progetto, seleziona il campo **Motore di pianificazione**, quindi modifica il campo in **Visibile per impostazione predefinita**. Se non utilizzi la pagina principale del progetto predefinita, modifica la pagina esistente e aggiungi il campo **Motore di pianificazione** ad esso.

## <a name="settings"></a>Impostazioni

Per utilizzare la modalità di pianificazione esterna, devi prima creare un nuovo progetto e selezionare il motore di pianificazione **Pianificato esternamente** nell'elenco a discesa nella pagina principale del progetto. Dopo che questa modalità è stata impostata per un progetto, non può essere modificata.

## <a name="viewing-the-wbs"></a>Visualizzazione della struttura di suddivisione del lavoro

Se un progetto è pianificato esternamente, l'accesso a Project for the Web è limitato per quel progetto. Per visualizzare la struttura di suddivisione del lavoro, è necessario accedere alla griglia di rilevamento, dove viene visualizzata la struttura di suddivisione del lavoro completa.

## <a name="creating-and-editing-the-wbs"></a>Creazione e modifica della struttura di suddivisione del lavoro

Se la pianificazione esterna è abilitata per un progetto, è necessario definire i dati per tutte le entità correlate alla struttura di suddivisione del lavoro, incluse attività, membri del team, assegnazioni di risorse e dipendenze.

Nella figura seguente è illustrato il modello di dati per la pianificazione del progetto.

![Modello dati di pianificazione del progetto.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Limiti funzionali

Le seguenti operazioni non sono consentite su progetti pianificati esternamente.

### <a name="project-planning"></a>Pianificazione di un progetto

- **Copia progetto**: questa operazione non è supportata su progetti pianificati esternamente.
- **Sposta progetto**: le modifiche alla data di inizio di un progetto non sposteranno l'inizio di attività o assegnazioni di risorse nella struttura di suddivisione del lavoro.
- **Aggiornamento del responsabile di progetto**: le modifiche al responsabile di progetto nella pagina principale del progetto non creeranno automaticamente un nuovo membro del team di progetto finché il progetto non sarà stato convertito.
- **Aggiornamento del modello dell'ora di lavoro del progetto**: le modifiche al modello dell'ora di lavoro del progetto non ricalcolano la pianificazione del progetto.
- **Profili di distribuzione per l'assegnazione delle risorse**: la creazione delle assegnazioni di risorse non aggiornerà automaticamente il campo **mdyn\_PlannedWork**. Questo campo viene utilizzato per memorizzare i profili di distribuzione per lo sforzo di assegnazione delle risorse. Se si visualizza lo sforzo in fasi temporali nella griglia di assegnazione delle risorse o nella griglia di riconciliazione delle risorse, è necessario definire profili di distribuzione per l'assegnazione delle risorse valide. Questi profili di distribuzione devono essere formattati correttamente in modo che attivino il calcolo sia dei profili di distribuzione dei costi che dei profili di distribuzione dei prezzi di vendita. Ti consigliamo di creare un progetto di prova pianificato da Project for the Web e quindi di rivedere i dati associati per confermare i requisiti e la formattazione.

### <a name="resource-management"></a>Gestione delle risorse

- **Soddisfazione generica delle risorse**: l'adempimento delle risorse generiche non è supportato per i progetti pianificati esternamente. I tentativi di soddisfare i requisiti aperti attivi creeranno nuovi membri del team di progetto, ma non elimineranno il membro generico del team né sostituiranno il membro generico del team su eventuali assegnazioni di risorse esistenti.
- **Elimina membri del team**: l'eliminazione di un membro del team non eliminerà automaticamente le assegnazioni delle risorse.

### <a name="quoting-and-contracting"></a>Citare e contrattare

- **Importazione dei dettagli della riga del preventivo e della riga del contratto**: quando i dettagli di un preventivo o di una riga di contratto vengono importati da un progetto, l'applicazione è stata testata per supportare un massimo di sole 500 attività nella WBA, in base a un limite di 20 assegnazioni per attività.

### <a name="actuals-and-invoicing"></a>Contabilità e fatturazione

- Sebbene non siano state apportate modifiche alle convalide esistenti tra la struttura di suddivisione del lavoro e le transazioni finanziarie, è importante conformarsi al modello di dati predefinito per garantire che tutte le transazioni downstream vengano eseguite come previsto.
