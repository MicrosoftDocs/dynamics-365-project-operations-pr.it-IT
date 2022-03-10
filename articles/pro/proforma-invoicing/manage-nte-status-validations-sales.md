---
title: Gestire convalide e stato da non superare
description: Questo argomento fornisce informazioni sui controlli del limite da non superare eseguiti in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b08a6834fa0bc5254f4baab15b40c7f733d0dc6ec7e6c4fceea2836e5e4c656a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003506"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Gestire convalide e stato da non superare 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

## <a name="not-to-exceed-on-approvals"></a>Limiti da non superare nelle approvazioni

Quando si invia una voce di tempo, spesa o utilizzo di materiale, viene creato un record approvazione. Se l'approvazione è addebitabile ed è mappata a una voce di contratto relativa a tempi e materiali, il sistema completa una verifica di convalida dei limiti da non superare ai seguenti livelli:

  - Verifica del limite impostato per il cliente nella voce di contratto di progetto
  - Verifica del limite impostato per la voce di contratto
  - Verifica del limite impostato per il cliente
  - Verifica del limite impostato per il contratto

Le verifiche a ciascun livello implicano la garanzia che l'importo del valore delle vendite in questa approvazione non violerà il limite da non superare a quel livello dopo aver contabilizzato l'importo del backlog di fatturazione già registrato e l'importo fatturato fino alla data a quel livello.

Se il controllo viene superato, all'approvazione viene assegnato uno stato di convalida di **Operazione completata**.

Se il controllo non viene superato, all'approvazione viene assegnato uno stato di convalida di **Non riuscito**. Il dettaglio della convalida del limite da non superare informerà l'utente a quale livello la convalida non è riuscita.

Quando la voce di tempo, spesa o utilizzo di materiale inviata è considerata non addebitabile, lo stato di convalida da non superare è **Non applicabile** con il dettaglio di convalida **Non applicabile**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Limite da non superare per i valori effettivi delle vendite non fatturate

Quando una voce di tempo, spesa o utilizzo di materiale viene approvata, vengono creati record di valori effettivi di costo e vendite non fatturate. Se il valore di vendita effettivo non fatturata creato è addebitabile ed è mappato a una voce di contratto relativa a tempi e materiali, l'applicazione esegue una verifica di convalida dei limiti da non superare ai seguenti livelli:

  - Verifica del limite impostato per il cliente della voce di contratto di progetto
  - Verifica del limite impostato per la voce di contratto
  - Verifica del limite impostato per il cliente
  - Verifica del limite impostato per il contratto

Le verifiche a ciascun livello garantiscono che l'importo del valore delle vendite nel valore effettivo non violerà il limite da non superare a quel livello dopo aver contabilizzato l'importo del backlog di fatturazione già registrato e l'importo fatturato fino alla data a quel livello.

Se il controllo viene superato, al valore effettivo di vendite non fatturate viene assegnato uno stato di limite da non superare **Confermato**.

Se il controllo non viene superato, al valore effettivo di vendite non fatturate viene assegnato uno stato di limite da non superare **Non riuscito**. Il dettaglio della convalida informa l'utente a quale livello la convalida non è riuscita.

Quando il valore effettivo di vendite non fatturate è considerato non addebitabile o gratuito, se non è stato impostato un limite da non superare in nessuno dei quattro livelli o se il valore effettivo creato è Costo, Acconto, Unità gestione risorse o Vendite interorganizzative, i campi **Stato da non superare** e **Dettagli convalida limite da non superare** devono essere impostati su **Non applicabile**.

## <a name="reset-the-not-to-exceed-status"></a>Reimpostare lo stato da non superare

È possibile eseguire un ripristino in blocco dello stato da non superare. I responsabili di progetto possono regolare la convalida da non superare per dare la priorità alla fatturazione di un particolare corpo di lavoro, tempo, spesa o utilizzo di materiale rispetto ad altri già confermati dall'importo da non superare disponibile.

Dopo che lo stato da non superare viene reimpostato sui valori effettivi di vendite non fatturate, l'importo confermato viene ridotto. Il responsabile di progetto può selezionare un'altra voce di corpo di lavoro, tempo, spesa o utilizzo di materiale che in precedenza non ha superato la convalida da non superare ed eseguire una nuova valutazione. Con la riduzione dell'importo confermato, questi valori effettivi ora superano la convalida che aiuta il responsabile di progetto a esercitare una maggiore influenza e controllo sulle transazioni fatturabili per quel periodo.

Per reimpostare lo stato da non superare, seleziona uno o più valori effettivi dalla visualizzazione **Backlog di fatturazione tempo e materiale** o **Valori effettivi** quindi seleziona **Reimposta stato da non superare**.

Lo stato da non superare viene reimpostato su **Non valutato** per tutti i valori effettivi selezionati pertinenti. I valori effettivi per cui è stato reimpostato lo stato da non superare sono i valori effettivi di vendita non fatturati che non sono già fatturati, non in una bozza di fattura e contrassegnati come addebitabili. Qualsiasi altro valore effettivo selezionato viene ignorato.

## <a name="reevaluate-not-to-exceed-status"></a>Rivalutare lo stato da non superare

È possibile eseguire una rivalutazione in blocco dello stato da non superare. La rivalutazione dello stato da non superare è utile quando:

  - C'è stata una rinegoziazione dei limiti da non superare con il cliente e i valori effettivi devono essere rivalutati.
  - Il responsabile di progetto desidera mettere a punto la fatturazione del backlog di vendite non fatturate dando priorità a un lavoro rispetto a un altro.

Per rivalutare lo stato da non superare, seleziona uno o più valori effettivi dalla visualizzazione **Backlog di fatturazione tempo e materiale** o **Valori effettivi** quindi seleziona **Rivaluta stato da non superare**.

Tutti i valori effettivi selezionati pertinenti con un limite da non superare verranno valutati rispetto all'impostazione del limite da non superare. I valori effettivi rilevanti per la rivalutazione dello stato da non superare sono i valori effettivi di vendita non fatturati che non sono fatturati, non in una bozza di fattura e contrassegnati come addebitabili. Qualsiasi altro valore effettivo selezionato.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
