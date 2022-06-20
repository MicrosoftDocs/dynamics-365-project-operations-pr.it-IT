---
title: 'Connessioni di transazione: collegare i valori effettivi di diversi tipi di transazione'
description: Questo articolo spiega come una connessione di transazione viene utilizzata per collegare i valori effettivi di diversi tipi per aiutare a tenere traccia della redditività, del ritardo di fatturazione e dei calcoli delle entrate fatturate rispetto a quelle non fatturate.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926091"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Connessioni di transazione: collegare i valori effettivi di diversi tipi di transazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I record di connessione della transazione vengono creati per collegare i valori effettivi di diverso tipo man mano che il tempo, le spese o l'utilizzo dei materiali si spostano nel ciclo di vita dall'offerta o dalla fase di prevendita alla fase del contratto, approvazioni e/o richiami, potenzialmente fatturazione di note di accredito e correttiva.

Nell'esempio seguente viene illustrata l'elaborazione tipica degli inserimenti ore in un ciclo di vita di progetto di Project Operations.

> ![Elaborazione di inserimenti ore in Project Operations.](media/basic-guide-17.png)

L'elaborazione degli inserimenti ore in un ciclo di vita di un progetto Project Operations segue questi passaggi: 

1. L'invio di un inserimento ore comporta la creazione di due righe di giornale di registrazione: una per il costo e una per le vendite non fatturate. 
2. L'eventuale approvazione dell'inserimento ore comporta la creazione di due valori effettivi: uno per il costo e uno per le vendite non fatturate. Questi 2 valori effettivi sono collegati tramite le connessioni di transazione.
3. Quando l'utente crea una fattura di progetto, la transazione di riga fattura viene creata utilizzando i dati del valore effettivo delle vendite non fatturate.
4. Quando la fattura viene confermata, vengono creati due nuovi valori effettivi: uno storno delle vendite non fatturate e un valore effettivo delle vendite fatturate. Lo storno delle vendite non fatturate e le vendite effettive non fatturate originali sono collegate utilizzando connessioni di transazione di storno. Le vendite fatturate e le vendite effettive non fatturate originali sono anche collegate per mostrare i collegamenti tra ciò che un tempo era il ricavo arretrato o in corso di lavorazione (WIP) a ciò che ora è il ricavo fatturato.   

Ogni evento nel flusso di lavoro di elaborazione attiva la creazione di record nella tabella **Connessione della transazione**. Questo aiuta a creare una traccia delle relazioni tra i record che vengono creati attraverso i dettagli di inserimento ore, riga di giornale di registrazione, valore effettivo e riga di fattura.

Nella tabella seguente sono riportati i record dell'entità **Connessione della transazione** per il flusso di lavoro precedente.

|Event                   |Transazione 1                 |Ruolo transazione 1 |Tipo di transazione 1       |Transazione 2          |Ruolo transazione 2 |Tipo di transazione 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Invio inserimento ore   |GUID della riga giornale di registrazione (vendite)     |Vendite non fatturate |msdyn_journalline            |GUID della riga giornale di registrazione (costo)     |Costo            |msdyn_journalline  |
|Approvazione tempo           |GUID del valore effettivo non fatturato (vendite)  |Vendite non fatturate |msdyn_actual                 |GUID del valore effettivo costo (costo)       |Costo            |msdyn_actual       |
|Creazione fattura        |GUID dei dettagli di riga fattura      |Vendite fatturate   |msdyn_invoicelinetransaction |GUID del valore effettivo vendite non fatturate   |Vendite non fatturate  |msdyn_actual       |
|Conferma fattura    |GUID del valore effettivo storno         |Storno      |msdyn_actual                 |GUID delle vendite non fatturate originale |Originale        |msdyn_actual       |
|                        |GUID delle vendite fatturate             |Vendite fatturate   |msdyn_actual                 |GUID del valore effettivo vendite non fatturate   |Vendite non fatturate  |msdyn_actual       |
|Correzione bozza della fattura |GUID della transazione riga fattura|Sostituzione      |msdyn_invoicelinetransaction |GUID delle vendite fatturate            |Originale        |msdyn_actual       |
|Conferma correzione fattura|GUID dello storno vendite fatturate  |Storno      |msdyn_actual                 |GUID delle vendite fatturate            |Originale        |msdyn_actual       |
|                        |Nuovo GUID vendite non fatturate |Sostituzione            |msdyn_actual                 |GUID delle vendite fatturate            |Originale        |msdyn_actual       |


L'illustrazione seguente mostra i collegamenti che vengono creati tra diversi tipi di valori effettivi in vari eventi utilizzando l'esempio degli inserimenti ore in Project Operations.

> ![In che modo i valori effettivi di diversi tipi sono collegati tra loro in Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
