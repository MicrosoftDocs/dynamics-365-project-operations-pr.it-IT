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
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287288"
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]