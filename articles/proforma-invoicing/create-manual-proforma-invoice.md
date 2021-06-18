---
title: Fatture proforma
description: Questo argomento fornisce informazioni sulle fatture proforma in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3eaf2f19506c5464c302176fc620aad5f29b4ae7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000666"
---
# <a name="proforma-invoices"></a>Fatture proforma

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

La fatturazione proforma fornisce ai responsabili di progetto un secondo livello di approvazione prima della creazione di fatture per i clienti. Il primo livello di approvazione viene completato quando le voci di tempo, spesa e materiale inviate dai membri del team di progetto sono approvate. Le fatture proforma confermate sono disponibili nel modulo Contabilità di progetto di Project Operations. I contabili del progetto possono eseguire aggiornamenti aggiuntivi come IVA, contabilità e layout delle fatture.


## <a name="creating-project-invoices"></a>Creare fatture di progetto

Le fatture di progetto possono essere create individualmente o in blocco. Puoi crearle manualmente oppure configurarle di modo che siano generate mediante esecuzioni automatizzate.

### <a name="manually-create-project-invoices"></a>Creare fatture di progetto manualmente 

Nella pagina elenco **Contratti di progetto**, puoi creare fatture di progetto separatamente per ogni contratto di progetto, oppure puoi creare fatture in blocco per molteplici contratti di progetto.

Segui questa procedura per creare una fattura per uno specifico contratto di progetto.

- Nella pagina elenco **Contratti di progetto**, apri un contratto di progetto e quindi seleziona **Crea fattura**.

    Una fattura viene generata per tutte le transazioni del contratto di progetto selezionato il cui stato è **Pronto per la fatturazione**. Queste transazioni includono tempi, spese, materiali, passaggi fondamentali e altre righe giornale di registrazione vendite non fatturate.

Segui questa procedura per creare fatture in blocco.

1. Nella pagina elenco **Contratti di progetto**, seleziona uno o più contratti di progetto per i quali devi creare una fattura per e quindi seleziona **Crea fatture di progetto**.

    Un messaggio di avviso informa che la creazione delle fatture può richiedere un certo tempo. Il processo viene anche visualizzato.

2. Seleziona **OK** per chiudere la finestra del messaggio.

    Una fattura viene generata per tutte le transazioni in una voce di contratto il cui stato è **Pronto per la fatturazione**. Queste transazioni includono tempi, spese, materiali, passaggi fondamentali e altre righe giornale di registrazione vendite non fatturate.

3. Per visualizzare le fatture generate, seleziona **Sales** \> **Fatturazione** \> **Fatture**. Viene visualizzata una fattura per ogni contratto di progetto.

### <a name="set-up-automated-creation-of-project-invoices"></a>Impostare la creazione automatica di fatture di progetto 

Segui questa procedura per configurare un'esecuzione di fatturazione automatizzata.

1. Passa a **Impostazioni** \> **Processi batch**.
2. Crea un processo batch e denominalo **Project Operations - Creazione di fatture**. Il nome del processo batch deve includere il termine "Creazione di fatture".
3. Nel campo **Tipo di processo** seleziona **Nome**. Per impostazione predefinita, le opzioni **Frequenza giornaliera** e **Attivo** sono impostate su **Sì**.
4. Seleziona **Esegui flusso di lavoro**. Nella finestra di dialogo **Cerca record**, vengono visualizzati tre flussi di lavoro:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleziona **ProcessRunCaller** e quindi **Aggiungi**.
6. Nella finestra di dialogo successiva, seleziona **OK**. Un flusso di lavoro **Sospendi** è seguito da un flusso di lavoro **Elabora**.

    Puoi anche selezionare **ProcessRunner** nel passaggio 5. Successivamente, quando selezioni **OK**, un flusso di lavoro **Elabora** è seguito da un flusso di lavoro **Sospendi**.

I flussi di lavoro **ProcessRunCaller** e **ProcessRunner** creano le fatture. **ProcessRunCaller** chiama **ProcessRunner**. **ProcessRunner** è il flusso di lavoro che crea le fatture. Esamina tutte le voci di contratto per le quali devono essere create le fatture e crea le fatture per tali voci. Per determinare le voci di contratto per le quali creare le fatture, il processo analizza le date di esecuzione delle fatture per le voci di contratto. Se le voci di contratto appartenenti a un contratto hanno la stessa data di esecuzione delle fatture, le transazioni sono combinate in una fattura con due righe fattura. Se non sono presenti transazioni per le quali creare fatture, il processo ignora la creazione delle fatture.

Dopo il termine dell'esecuzione di **ProcessRunner**, questo flusso di lavoro chiama **ProcessRunCaller**, fornisce l'ora di fine e viene chiuso. **ProcessRunCaller** avvia quindi un timer che viene eseguito per 24 ore a partire dall'ora di fine specificata. Alla fine dell'esecuzione del timer, **ProcessRunCaller** viene chiuso.

Il processo batch per la creazione di fatture è un processo ricorrente. Se questo processo batch viene eseguito molte volte, vengono create molteplici istanze del processo che causano errori. Pertanto, devi avviare il processo batch una sola volta e riavviarlo solo se viene interrotto.

> [!NOTE]
> La fatturazione batch viene eseguita solo per le righe di contratto di progetto configurate dalle pianificazioni fatture. Una riga di contratto con un metodo di fatturazione a prezzo fisso deve avere i passaggi fondamentali configurati. Una riga di contratto di progetto con un metodo di fatturazione di tempo e materiali richiederà una pianificazione fatturazione basata sulla data. Lo stesso vale per una riga di contratto basato su progetto.      
 
### <a name="edit-a-draft-invoice"></a>Modificare una bozza di fattura

Quando crei una bozza di fattura di progetto, tutte le transazioni di vendita non fatturate create all'approvazione delle voci di tempo, spesa e utilizzo di materiale sono inseriti nella fattura. Puoi eseguire le seguenti rettifiche quando la fattura è ancora nello stato bozza:

- Eliminare o modificare dettagli di riga fattura.
- Modificare e rettificare la quantità e il tipo di fatturazione.

Seleziona **Conferma** per confermare una fattura. L'azione Conferma è unidirezionale. Quando selezioni **Conferma**, il sistema rende la fattura di sola lettura e crea valori effettivi di vendite fatturate da ogni dettaglio di ogni riga fattura. Se il dettaglio di riga fattura fa riferimento a un valore effettivo di vendite non fatturate, il sistema storna anche questo valore. (qualsiasi dettaglio di riga fattura creato da una voce di spesa o un inserimento ore farà riferimento a un valore effettivo di vendite non fatturate). I sistemi di integrazione di contabilità generale possono utilizzare questo storno per stornare il lavoro in corso del progetto per scopi di contabilità.

### <a name="correct-a-confirmed-invoice"></a>Correggere una fattura confermata

Le fatture confermate possono essere modificate (corrette). Quando correggi una fattura confermata, viene creata una nuova bozza di fattura correttiva. Poiché si presuppone che tu voglia stornare tutte le transazioni e quantità dalla fattura originale, questa fattura correttiva include tutte le transazioni della fattura originale e tutte le relative quantità sono pari a 0 (zero).

Se alcune transazioni non richiedono la correzione, puoi rimuoverle dalla bozza di fattura correttiva. Se desideri stornare o restituire solo una quantità parziale, puoi modificare il campo **Quantità** nel dettaglio della riga. Se apri il dettaglio di riga fattura, puoi vedere la quantità della fattura originale. Puoi quindi modificare la quantità della fattura corrente di modo che sia inferiore o superiore alla quantità della fattura originale.

Quando confermi una fattura correttiva, il valore effettivo delle vendite fatturate originali viene stornato e viene creato un nuovo valore effettivo di vendite fatturate. Se la quantità è stata ridotta, la differenza genererà anche la creazione di un nuovo valore effettivo delle vendite. Ad esempio, se lea vendita fatturata originale era per otto ore e il dettaglio di riga fattura correttiva presenta una quantità ridotta di sei ore, la riga delle vendite fatturate originali viene stornata e due nuovi valori effettivi vengono creati:

- Un valore effettivo delle vendite fatturate per sei ore.
- Un valore effettivo delle vendite non fatturate per le due ore rimanenti. Questa transazione può essere fatturata successivamente o contrassegnata come non addebitale, a seconda delle negoziazioni con il cliente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
