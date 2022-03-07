---
title: Novità o modifiche nella versione di aggiornamento 32 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 32 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129671"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Novità o modifiche nella versione di aggiornamento 32 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 32 di Project Service Automation V3. Questa versione ha un numero di build di V3.10.53.108 ed è generalmente disponibile tramite un aggiornamento automatico di giugno 2021.

## <a name="update-release-32"></a>Rilascio 32 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

#### <a name="general"></a>Generali

- Quando un aggiornamento importante non riesce, devono essere bloccati solo i punti di ingresso dell'applicazione principale, per garantire che le entità condivise siano ancora accessibili.

#### <a name="time-and-expense"></a>Ore e spesa

Sono stati risolti i seguenti problemi:

- **TimeEntriesImportFromResourceAssignment** non mantiene l'ora di inizio e l'ora di fine della sezione del profilo di assegnazione delle risorse.
- Quando selezioni **Apri inserimento** nella griglia **Inserimento ore**, potresti non essere in grado di selezionare altri moduli.
- Durante l'importazione delle assegnazioni agli inserimenti delle ore, la query del codice client potrebbe generare un URL lungo che non risolve la query.
- Nella griglia **Inserimento ore**, dopo che un valore è stato eliminato da una cella, lo stato attivo non rimane nella griglia.
- Il pulsante **Rifiuta** è stato rimosso dalla vista **Approvazioni in elaborazione** per le omologazioni moderne.
- La stabilità e le prestazioni dell'approvazione in blocco dell'inserimento ore sono influenzate da deadlock e dalla mancata gestione appropriata delle personalizzazioni relative all'entità **Inserimento ore**.

#### <a name="project-planning"></a>Pianificazione di progetti

- Un'eccezione di riferimento null viene generata quando si aggiorna un progetto che ha un valore null nel campo **Unità contratto**.
- **Aggiorna totali progetto** non calcola correttamente il costo rimanente e le vendite rimanenti su un progetto.
- I calcoli dei prezzi ridondanti influiscono sulle prestazioni correlate agli aggiornamenti sui contorni dell'assegnazione delle risorse.

#### <a name="resource-management"></a>Gestione risorse

Il problema seguente è stato risolto:

- Quando la capacità di calendario di una risorsa prenotabile è maggiore di 1, Project Service Automation riconosce erroneamente la capacità come 0 (zero). Pertanto, si verifica un ciclo infinito nella visualizzazione della pianificazione.

#### <a name="sales"></a>Vendite

Sono stati risolti i seguenti problemi:

- Quando viene creata una riga del giornale di registrazione con un tipo di transazione personalizzato, si verifica la seguente eccezione di riferimento null: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- I ruoli e le categorie disattivati prima della copia di un'offerta non devono essere aggiunti ai ruoli e alle categorie addebitabili dell'offerta appena copiata.
- La data del documento e la data contabile non sono allineate con la data di inizio fornita in un dettaglio della riga della fattura creato direttamente in una bozza di fattura.
- Le eccezioni di riferimento null vengono generate negli scenari correlati alla disattivazione di ruoli e categorie prima che venga copiata un'offerta.
- L'azione **Aggiorna prezzi** nella pagina **Progetti** non aggiorna le stime di spesa e le stime dei materiali.
