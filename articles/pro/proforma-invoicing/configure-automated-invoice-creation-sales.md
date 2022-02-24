---
title: Configurare la creazione automatica della fattura - semplice
description: Questo argomento fornisce informazioni sulla configurazione della creazione automatica delle fatture proforma.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176571"
---
# <a name="configure-automatic-invoice-creation---lite"></a>Configurare la creazione automatica della fattura - semplice
 
_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi configurare la creazione automatica della fattura in Dynamics 365 Project Operations. Il sistema crea una bozza di fattura proforma basata sulla pianificazione della fattura per ogni contratto di progetto e voce di contratto. Le pianificazioni delle fatture vengono configurate a livello di voce di contratto. Ogni riga di un contratto può avere una pianificazione fattura distinta oppure la stessa pianificazione fattura può essere inclusa in ogni voce del contratto.

Quando crei una fattura, il sistema crea sempre almeno una fattura per contratto di progetto. In alcuni casi, potrebbero essere create più fatture.

Ad esempio, se il contratto ha più clienti, verrà creato lo stesso numero di fatture del numero di clienti che hanno transazioni fatturabili da fatturare su quel contratto di progetto.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Informazioni su come le transazioni sono incluse in una fattura 

A volte, ogni voce di contratto basata su progetto specifica una pianificazione fattura separata. Ad esempio, i servizi di implementazione per il contratto Adatum hanno le seguenti voci di contratto:

- Il lavoro prototipo che è un prezzo fisso con due passaggi fondamentali creati manualmente.
- Il lavoro di implementazione che include il tempo e verrà fatturato bisettimanalmente il lunedì.
- Le spese sostenute che devono essere fatturate mensilmente il primo lunedì di ogni mese.

Le pianificazioni delle fatture definite su ciascuno di questi due articoli riga sono simili alla tabella seguente:

| Voce di contratto | Data esecuzione fattura | Data limite transazione | Data passaggio fondamentale | Importo passaggio fondamentale |
| --- | --- | --- | --- | --- |
| Lavoro prototipo | Lunedì 5 ottobre | - | Lunedì 5 ottobre | 5000 USD |
| - | Martedì 3 novembre | - | Martedì 3 novembre | 12,000 USD |
| Lavoro di implementazione | Lunedì 5 ottobre | Domenica 4 ottobre | - | - |
| - | Lunedì 19 ottobre | Domenica 18 ottobre | - | - |
| - | Lunedì 2 novembre | Domenica 1 novembre | - | - |
| - | Lunedì 16 novembre | Domenica 15 novembre | - | - |
| Spese sostenute | Lunedì 5 ottobre | Domenica 4 ottobre | - | - |
| - | Lunedì 2 novembre | Domenica 1 novembre | - | - |

In questo esempio, quando la fatturazione automatica viene eseguita il:

- **4 ottobre o prima**: nessuna fattura viene generata per questo contratto perché la tabella **Pianificazione fattura** per ciascuna di queste voci di contratto non chiama domenica 4 ottobre, come data di esecuzione della fattura.
- **Lunedì 5 ottobre**: viene generata una fattura per:

    - Il lavoro prototipo che include il passaggio fondamentale se è contrassegnato come **Pronto per la fatturazione**.
    - Il lavoro di implementazione che include tutte le transazioni temporali create prima della data limite della transazione di domenica 4 ottobre, contrassegnata come **Pronto per la fatturazione**.
    - La spesa sostenuta che include tutte le transazioni di spesa create prima della data limite della transazione di domenica 4 ottobre, contrassegnata come **Pronto per la fatturazione**.
  
- **Il 6 ottobre o prima del 19 ottobre**: nessuna fattura viene generata per questo contratto perché la tabella **Pianificazione fattura** per ciascuna di queste voci di contratto non chiama il 6 ottobre o una data prima del 19 ottobre, come data di esecuzione della fattura.
- **Lunedì 19 ottobre**: una fattura viene generata per il lavoro di implementazione che include tutte le transazioni temporali create prima della data limite della transazione di domenica 18 ottobre, contrassegnata come **Pronto per la fatturazione**.
- **Lunedì 2 novembre**: viene generata una fattura per:

    - Il lavoro di implementazione che include tutte le transazioni temporali create prima della data limite della transazione di domenica 1 novembre, contrassegnata come **Pronto per la fatturazione**.
    - La spesa sostenuta che include tutte le transazioni di spesa create prima della data limite della transazione di domenica 1 novembre, contrassegnata come **Pronto per la fatturazione**.

- **Martedì 3 novembre**: viene generata una fattura per il lavoro prototipo che include il passaggio fondamentale per 12000 USD, se contrassegnata come **Pronto per la fatturazione**.

## <a name="configure-automatic-invoicing"></a>Configurare la fatturazione automatica

Completa questa procedura per configurare un'esecuzione di fatturazione automatizzata.

1. In **Project Operations**, vai a **Impostazioni** > **Impostazione fattura ricorrente**.
2. Crea un processo batch e denominalo **Project Operations - Creazione di fatture**. Il nome del processo batch deve includere le parole "creazione di fatture".
3. Nel campo **Tipo di processo** seleziona **Nome**. Per impostazione predefinita, i campi **Frequenza giornaliera** e **Attivo** sono impostate su **Sì**.
4. Seleziona **Esegui flusso di lavoro**. Nella finestra di dialogo **Cerca record**, vengono visualizzati tre flussi di lavoro:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Seleziona **ProcessRunCaller** e quindi **Aggiungi**.
6. Nella finestra di dialogo successiva, seleziona **OK**. Un flusso di lavoro **Sospendi** è seguito da un flusso di lavoro **Elabora**. 

> [!NOTE]
> Puoi anche selezionare **ProcessRunner** nel passaggio 5. Successivamente, quando selezioni **OK**, un flusso di lavoro **Elabora** è seguito da un flusso di lavoro **Sospendi**.

I flussi di lavoro **ProcessRunCaller** e **ProcessRunner** creano le fatture. **ProcessRunCaller** chiama **ProcessRunner**. **ProcessRunner** è il flusso di lavoro che crea le fatture. Il flusso di lavoro esamina tutte le voci di contratto per le quali devono essere create le fatture e crea le fatture per tali voci. Per determinare le voci di contratto per le quali creare le fatture, il processo analizza le date di esecuzione delle fatture per le voci di contratto. Se le voci di contratto appartenenti a un contratto hanno la stessa data di esecuzione delle fatture, le transazioni sono combinate in una fattura con due righe fattura. Se non sono presenti transazioni per le quali creare fatture, il processo ignora la creazione di una fattura.

Dopo il termine dell'esecuzione di **ProcessRunner**, questo flusso di lavoro chiama **ProcessRunCaller**, fornisce l'ora di fine e viene chiuso. **ProcessRunCaller** avvia quindi un timer che viene eseguito per 24 ore a partire dall'ora di fine specificata. Alla fine dell'esecuzione del timer, **ProcessRunCaller** viene chiuso.

Il processo batch per la creazione di fatture è un processo ricorrente. Se questo processo batch viene eseguito molte volte, vengono create molteplici istanze del processo che causa gli errori. Pertanto, devi avviare il processo batch una sola volta e riavviarlo solo se viene interrotto.

> [!NOTE]
> La fatturazione in batch in Project Operations viene eseguita solo per le voci di contratto di progetto configurate dalle pianificazioni fatturazione. Una riga di contratto con un metodo di fatturazione a prezzo fisso deve avere i passaggi fondamentali configurati. Una riga di contratto di progetto con un metodo di fatturazione di tempo e materiali richiederà una pianificazione fatturazione basata sulla data.
