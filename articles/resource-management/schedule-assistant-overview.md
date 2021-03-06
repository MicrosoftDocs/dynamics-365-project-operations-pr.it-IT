---
title: Panoramica dell'assistente di pianificazione
description: Questo argomento fornisce informazioni su utilizzare l'assistente di pianificazione per prenotare le risorse.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908266"
---
# <a name="schedule-assistant-overview"></a>Panoramica dell'assistente di pianificazione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

L'assistente di pianificazione viene utilizzato per prenotare le risorse in base ai requisiti definiti dal responsabile di progetto. L'assistente di pianificazione si basa sui parametri forniti nel requisito di risorsa per trovare la risorsa. L'assistente di pianificazione consiglia risorse che soddisfano i requisiti pertinenti, come finestre temporali o competenze necessarie.

Dopo aver identificato le risorse appropriate, il responsabile delle risorse o del progetto può prenotare la risorsa per il lavoro.

## <a name="prerequisites"></a>Prerequisiti

L'assistente di pianificazione fa parte della soluzione Universal Resource Scheduling. Questa soluzione è inclusa e installata con Dynamics 365 Project Operations, Dynamics 365 Field Service e Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Requisiti e risorse corrispondenti

Un requisito di risorsa generato si basa su dettagli quali:

-   Caratteristiche
-   Ruoli
-   Business Unit
-   Preferenze di risorsa
-   Profili del lavoro richiesto
-   Fuso orario

L'assistente di pianificazione utilizza questi dettagli per filtrare le risorse.

## <a name="launch-the-schedule-assistant"></a>Avviare l'assistente di pianificazione

Sono disponibili due modi per avviare l'assistente di pianificazione. Se stai utilizzando la modalità ibrida, nella griglia dei membri del team puoi selezionare qualsiasi membro del team con un requisito di risorsa non soddisfatto e quindi selezionare **Prenota**. Se stai utilizzando la modalità centrale, il responsabile delle risorse trova e seleziona la risorsa.

## <a name="schedule-assistant-filters"></a>Filtri dell'assistente di pianificazione

Dopo l'esecuzione dell'assistente di pianificazione, i dettagli del requisito di risorsa vengono visualizzati come valori filtrati nel riquadro di sinistra. Il responsabile delle risorse o il responsabile del progetto possono ottimizzare i risultati regolando i filtri per soddisfare le esigenze di pianificazione.

Il riquadro dei filtri mostra le opzioni relative al lavoro, tra cui:

-   Inizio e fine lavoro
-   Caratteristiche
-   Ruoli
-   Unità organizzative
-   Società di gestione risorse
-   Tipi di risorsa
-   Risorse preferite
