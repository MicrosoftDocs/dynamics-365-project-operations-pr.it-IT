---
title: Sincronizzare la capacità delle risorse
description: Questo argomento fornisce informazioni su come sincronizzare la capacità di una risorsa tra calendari e progetti.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288566"
---
# <a name="synchronize-resource-capacity"></a>Sincronizzare la capacità delle risorse

[!include [banner](../includes/banner.md)]

I processi per la sincronizzazione delle risorse aiutano a garantire che le informazioni per il calendario e il calendario di base si riflettano nella pianificazione delle risorse del progetto. Se il calendario viene modificato, i processi apportano gli aggiornamenti richiesti alla pianificazione delle risorse del progetto. I processi aiutano anche a migliorare le prestazioni, perché le informazioni sulle risorse del calendario vengono sincronizzate in anticipo. Pertanto, gli aggiornamenti alle informazioni sulla pianificazione delle risorse avvengono più rapidamente. Si consiglia di pianificare i processi come batch anziché uno alla volta. In caso contrario, c'è il rischio che qualcuno dimentichi le date incluse in cui le informazioni sono state sincronizzate l'ultima volta. Se le date incluse non vengono utilizzate, possono verificarsi degli intervalli durante la sincronizzazione della data.

![Sincronizzazione del calendario](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizzare il rollup della capacità delle risorse

Il processo di sincronizzazione è progettato per sincronizzare tutte le informazioni del calendario delle risorse. Queste informazioni includono le informazioni del calendario di base su eventuali modifiche alla tabella della capacità del calendario delle risorse del progetto. Se vengono aggiunte nuove risorse al progetto, la sincronizzazione aiuta a garantire che le informazioni di calendario aggiornate siano disponibili. Questa sincronizzazione può essere eseguita in qualsiasi momento.

Si consiglia di utilizzare un batch. Le opzioni sono disponibili durante la sincronizzazione delle prenotazioni della capacità.

1. Seleziona **Gestione progetti e contabilità** &gt; **Periodico** &gt; **Sincronizzazione capacità** &gt; **Sincronizza i roll-up della capacità delle risorse**.
2. Imposta le opzioni nella tabella seguente.

    | Opzione      | Descrizione |
    |-------------|-------------|
    | Codice periodo | Facoltativamente, seleziona il codice intervallo data di contabilità generale per impostare le date di inizio e fine per il processo di sincronizzazione per i roll-up della capacità delle risorse. |
    | Data di inizio  | Immetti la data di inizio per il processo di sincronizzazione per i roll-up della capacità delle risorse. |
    | Data di fine    | Immetti la data di fine per il processo di sincronizzazione per i roll-up della capacità delle risorse. |

[![Processo di sincronizzazione](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]