---
title: Tipi di periodo
description: Questo argomento fornisce informazioni su come configurare i tipi di periodo per la stima dei ricavi.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531467"
---
# <a name="period-types"></a>Tipi di periodo

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Un tipo di periodo definisce la frequenza con cui vengono stimate le entrate per un progetto. Questo argomento fornisce informazioni su come configurare i tipi di periodo per la stima dei ricavi. 

## <a name="create-and-work-with-period-types"></a>Creare e utilizzare tipi di periodo
Per creare e utilizzare i tipi di periodo, completare i seguenti passaggi:

1. Nel tuo ambiente Dynamics 365 Finance, vai a **Contabilità e gestione progetti** > **Configurazione** > **Stime** > **Tipi di periodo**.
2. Seleziona **Nuovo** per creare un nuovo tipo di periodo. Immetti un nome e una descrizione.
3. Nel campo **Frequenza**, seleziona un valore.

    - Se selezioni **Settimana**, **Bisettimanale**, **Semestrale**, **Mese**, **Giorno**, **Trimestre** o **Anno**, il calendario verrà utilizzato per generare i periodi. 
    - Se selezioni **Periodo contabile**, i periodi di contabilità generale dalla configurazione di contabilità generale verranno utilizzati per generare periodi.
    - Se selezioni **Illimitato**, puoi specificare periodi personalizzati.
4. Selezionare il record del tipo di periodo e quindi selezionare **Genera periodi** per creare periodi per il tipo di periodo. In base alla frequenza del periodo selezionata, potresti avere la possibilità di specificare una data di inizio o il numero di periodi da generare.
5. Seleziona **Periodi** per rivedere i periodi generati.

