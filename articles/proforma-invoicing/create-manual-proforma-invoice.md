---
title: Creare una fattura proforma manuale
description: Questo argomento fornisce informazioni sulla creazione di una fattura proforma.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ad85262482f782391eca85f46ca0e63a887c89f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896110"
---
# <a name="create-a-manual-proforma-invoice"></a>Creare una fattura proforma manuale

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

La fatturazione offre ai responsabili di progetto un secondo livello di approvazione prima della creazione di fatture per i clienti. Il primo livello di approvazione viene completato quando le voci di spesa e gli inserimenti ore inviati dai membri del team di progetto sono approvate.

Dynamics 365 Project Operations non è progettato per generare fatture per i clienti, per i motivi seguenti:

- Non contiene informazioni fiscali.
- Non può convertire altre valute nella valuta di fatturazione utilizzando tassi di cambio configurati correttamente.
- Non può formattare le fatture correttamente in modo da poterle stampare.

In alternativa, puoi utilizzare un sistema finanziario o di contabilità per creare fatture per i clienti che utilizzano le informazioni delle proposte di fatturazione generate.

## <a name="creating-project-invoices"></a>Creare fatture di progetto

Le fatture di progetto possono essere create individualmente o in blocco. Puoi crearle manualmente oppure configurarle di modo che siano generate mediante esecuzioni automatizzate.

### <a name="manually-create-project-invoices"></a>Creare fatture di progetto manualmente 

Nella pagina elenco **Contratti di progetto**, puoi creare fatture di progetto separatamente per ogni contratto di progetto, oppure puoi creare fatture in blocco per molteplici contratti di progetto.

Segui questa procedura per creare una fattura per uno specifico contratto di progetto.

- Nella pagina elenco **Contratti di progetto**, apri un contratto di progetto e quindi seleziona **Crea fattura**.

    Una fattura viene generata per tutte le transazioni del contratto di progetto selezionato il cui stato è **Pronto per la fatturazione**. Queste transazioni includono voci di contratto basate su prodotto, tempo, spese e passaggi fondamentali.

Segui questa procedura per creare fatture in blocco.

1. Nella pagina elenco **Contratti di progetto**, seleziona uno o più contratti di progetto per i quali devi creare una fattura per e quindi seleziona **Crea fatture di progetto**.

    Un messaggio di avviso informa che la creazione delle fatture può richiedere un certo tempo. Il processo viene anche visualizzato.

2. Seleziona **OK** per chiudere la finestra del messaggio.

    Una fattura viene generata per tutte le transazioni in una voce di contratto il cui stato è **Pronto per la fatturazione**. Queste transazioni includono voci di contratto basate su prodotto, tempo, spese e passaggi fondamentali.

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

Quando crei una bozza di fattura di progetto, tutte le transazioni di vendita non fatturate create all'approvazione delle voci di spesa e degli inserimenti ore tempo sono inseriti nella fattura. Puoi eseguire le seguenti rettifiche quando la fattura è ancora nello stato bozza:

- Eliminare o modificare dettagli di riga fattura.
- Modificare e rettificare la quantità e il tipo di fatturazione.
- Aggiungere direttamente tempo, spese e imposte come transazioni nella fattura. Puoi utilizzare questa funzionalità se la riga fattura viene mappata a una voce di contratto che consente queste classi di transazioni.

Seleziona **Conferma** per confermare una fattura. L'azione Conferma è unidirezionale. Quando selezioni **Conferma**, il sistema rende la fattura di sola lettura e crea valori effettivi di vendite fatturate da ogni dettaglio di ogni riga fattura. Se il dettaglio di riga fattura fa riferimento a un valore effettivo di vendite non fatturate, il sistema storna anche questo valore. (qualsiasi dettaglio di riga fattura creato da una voce di spesa o un inserimento ore farà riferimento a un valore effettivo di vendite non fatturate). I sistemi di integrazione di contabilità generale possono utilizzare questo storno per stornare il lavoro in corso del progetto per scopi di contabilità.

### <a name="correct-a-confirmed-invoice"></a>Correggere una fattura confermata

Le fatture confermate possono essere modificate (corrette). Quando correggi una fattura confermata, viene creata una nuova bozza di fattura correttiva. Poiché si presuppone che tu voglia stornare tutte le transazioni e quantità dalla fattura originale, questa fattura correttiva include tutte le transazioni della fattura originale e tutte le relative quantità sono pari a 0 (zero).

Se alcune transazioni non richiedono la correzione, puoi rimuoverle dalla bozza di fattura correttiva. Se desideri stornare o restituire solo una quantità parziale, puoi modificare il campo **Quantità** nel dettaglio della riga. Se apri il dettaglio di riga fattura, puoi vedere la quantità della fattura originale. Puoi quindi modificare la quantità della fattura corrente di modo che sia inferiore o superiore alla quantità della fattura originale.

Quando confermi una fattura correttiva, il valore effettivo delle vendite fatturate originali viene stornato e viene creato un nuovo valore effettivo di vendite fatturate. Se la quantità è stata ridotta, la differenza genererà anche la creazione di un nuovo valore effettivo delle vendite. Ad esempio, se lea vendita fatturata originale era per otto ore e il dettaglio di riga di fattura correttiva presenta una quantità ridotta di sei ore, la riga delle vendite fatturate originali viene stornata e due nuovi valori effettivi vengono creati:

- Un valore effettivo delle vendite fatturate per sei ore.
- Un valore effettivo delle vendite non fatturate per le due ore rimanenti. Questa transazione può essere fatturata successivamente o contrassegnata come non addebitale, a seconda delle negoziazioni con il cliente.
