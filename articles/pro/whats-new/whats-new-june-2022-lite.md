---
title: Novità di giugno 2022 - Distribuzione semplice di Project Operations
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di giugno 2022 della distribuzione lite di Microsoft Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959440"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Novità di giugno 2022 - Distribuzione semplice di Project Operations

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.43.0.77

## <a name="quality-updates"></a>Aggiornamenti di qualità

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Conto lavoro | 2708885 | Risolto il problema con il messaggio di errore che veniva visualizzato quando un utente creava un record di intestazione di prenotazione di una risorsa prenotabile in cui non veniva compilata alcuna risorsa prenotabile. |
| Pianificazione e rilevamento dei progetti | 2629441 | Corretta la logica di attivazione del flusso di lavoro per evitare un ciclo infinito quando le attività del progetto vengono aggiornate. |
| Tempistica e spesa | 2641209 | Le importazioni di inserimenti ore da assegnazioni/prenotazioni devono conservare un riferimento di risorsa prenotabile. |
| Pianificazione e rilevamento dei progetti | 2651148 | L'intestazione del documento di progetto deve essere protetta.|
| Pianificazione e rilevamento dei progetti | 2653145 | Aggiunte convalide per garantire che non sia possibile creare un record di progetto con caratteri non validi nel nome. |
| Tempistica e spesa | 2654710 | Corretto il filtro sulla pagina **Approvazioni**. |
| Determinazione dei prezzi e fatturazione | 2667805 | Aggiunte convalide per impedire la creazione di valori effettivi di vendite fatturate se il supporto dei valori effettivi di vendite non fatturate non esiste. |
| Determinazione dei prezzi e fatturazione | 2668378 | Aggiunte convalide per impedire l'aggiunta di una dimensione di determinazione dei prezzi personalizzata a meno che non vengano compilati un nome logico e un nome di campo. |
| Tempistica e spesa | 2700428 | È stata migliorata la logica delle approvazioni per garantire che altri set di approvazione per il progetto possano essere elaborati anche se uno dei set di approvazione è bloccato nei processi di sistema. |
