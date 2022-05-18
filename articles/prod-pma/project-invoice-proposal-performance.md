---
title: Prestazioni delle proposte di fatturazione progetto
description: Questo argomento fornisce informazioni sui miglioramenti delle prestazioni delle proposte di fatturazione progetto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e707b0d9b379df59726271b5a0441ac04e269b9a
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683451"
---
# <a name="project-invoice-proposal-performance"></a>Prestazioni delle proposte di fatturazione progetto

[!include [banner](../includes/banner.md)]

Quando crei una nuova proposta di fatturazione, potresti riscontrare problemi di prestazioni con l'aumento del numero di progetti e sottoprogetti. Per migliorare le prestazioni, è disponibile una funzione che riduce il tempo necessario per creare una nuova proposta di fatturazione per le transazioni di progetto registrate.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Abilitare il miglioramento delle prestazioni delle proposte di fatturazione progetto
Per abilitare la funzionalità di miglioramento delle prestazioni delle proposte di fatturazione progetto, completa i seguenti passaggi.

1.  Vai a **Gestione funzionalità** > **Tutte**. Nell'elenco delle funzionalità, individua **Miglioramento delle prestazioni delle proposte di fatturazione progetto**.
2.  Seleziona **Abilita ora**.
3.  Aggiorna il browser, quindi crea una nuova proposta di fatturazione.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Disabilitare il miglioramento delle prestazioni delle proposte di fatturazione progetto
Per disabilitare la funzionalità di miglioramento delle prestazioni delle proposte di fatturazione progetto, completa i seguenti passaggi.

1.  Vai a **Gestione funzionalità** > **Tutte**. Nell'elenco delle funzionalità, individua **Miglioramento delle prestazioni delle proposte di fatturazione progetto**.
2.  Seleziona **Disabilita**.
3.  Aggiorna il browser.

> [!NOTE]
> Le prestazioni della proposta di fattura non possono essere applicate quando le regole di fatturazione sono abilitate.
> 
> Durante il processo batch per creare proposte di fattura, il numero di sottoattività suddivide le attività in un numero massimo basato sul numero di contratti con transazioni fatturabili, indipendentemente da ciò che hai inserito. Ad esempio, se inserisci **3** per il numero di attività secondarie per la creazione di proposte di fattura in batch e sono presenti solo due contratti con transazioni fatturabili, vengono create solo due attività secondarie.
