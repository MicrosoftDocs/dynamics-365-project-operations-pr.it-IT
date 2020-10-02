---
title: Configurare la creazione automatica della fattura
description: Questo argomento fornisce informazioni su come configurare il sistema per generare fatture automaticamente.
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898131"
---
# <a name="configure-automated-invoice-creation"></a>Configurare la creazione automatica della fattura

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Completa i passaggi seguenti per configurare l'esecuzione automatica della fattura in Project Operations.

1. Passa a **Impostazioni** \> **Processi batch**.
2. Crea un processo batch e denominalo **Project Operations - Creazione di fatture**. Il nome del processo batch deve includere il termine "creazione di fatture".
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
