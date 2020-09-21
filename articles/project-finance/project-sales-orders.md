---
title: Ordini di vendita di progetto per progetti relativi a tempi e materiali
description: Questo argomento spiega come creare ordini di vendita basati su progetto per progetti relativi a tempi e materiali.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752600"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Ordini di vendita di progetto per progetti relativi a tempi e materiali

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Questo argomento descrive come creare un ordine di vendita per un progetto. Gli ordini di vendita possono essere creati solo per progetti di tipo **tempo e materiale**.

Se un progetto relativo a tempi e materiali ha più fonti di finanziamento nel contratto di progetto, devi abilitare il parametro **Consenti ordini di vendita per progetti con più fonti di finanziamento** nella pagina **Gestione progetti e contabilità**. 

> [!NOTE]
> - Il supporto per gli ordini di vendita del progetto con più fonti di finanziamento è disponibile a partire dalla versione dell'applicazione 10.0.2 e successive.
> - Il parametro per abilitare il supporto per gli ordini di vendita del progetto con più fonti di finanziamento verrà rimosso nell'ondata di rilascio di aprile 2020, dopodiché la funzionalità sarà sempre abilitata.

È possibile creare ordini di vendita basati su progetto in due modi:

- Vai al progetto stesso. Nel riquadro azioni seleziona **Gestisci > Attività articolo > Ordine di vendita**. Le informazioni sul progetto verranno impostate per impostazione predefinita sull'ordine di vendita del progetto. Se il contratto di progetto ha più di una fonte di finanziamento, sarà necessario selezionare la fonte di finanziamento per impostare il cliente per l'ordine di vendita. Se esiste una sola fonte di finanziamento per il progetto, il cliente verrà impostato automaticamente.
- Vai alla pagina elenco **Tutti gli ordini di vendita** e crea un nuovo ordine di vendita. Sarà necessario selezionare il progetto per l'ordine di vendita. Dopo aver selezionato il progetto, il cliente verrà impostato dalla fonte di finanziamento o sarà necessario selezionare la fonte di finanziamento se il contratto di progetto ha più fonti di finanziamento.

