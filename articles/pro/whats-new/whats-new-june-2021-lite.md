---
title: Novità di giugno 2021 - Distribuzione semplice di Project Operations
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di giugno 2021 della distribuzione lite di Project Operations.
author: sigitac
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 16fffb06ebb72ac25982374bff27a015eccfae1b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913947"
---
# <a name="whats-new-june-2021---project-operations-lite-deployment"></a>Novità di giugno 2021 - Distribuzione semplice di Project Operations

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo articolo si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

  - Project Operations in ambiente Dataverse versione 4.11.0.156 o 4.11.0.164.

## <a name="quality-updates"></a>Aggiornamenti di qualità

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Prezzi e fatturazione | 2281417 | Risolto il problema relativo all'esito negativo dell'azione di creazione automatica della fattura tramite la pianificazione fatturazione. |
| Prezzi e fatturazione | 2287835 |   Miglioramento delle prestazioni di conferma della fattura. |
| Gestione delle opportunità | 2222555 | L'addebito delle stime dei materiali deve essere copiato correttamente nei dettagli della riga del preventivo quando si utilizza **Importa da stima di progetto**. |
| Gestione delle opportunità | 2223427 | Le personalizzazioni sono ora consentite per l'azione **GenerateRetainersFromRetainerScheduleOptions**. |
| Gestione delle opportunità | 2277528 | Calcolo del valore fisso del passaggio fondamentale di fatturazione per righe di contratto di progetto con più clienti. |
| Pianificazione e rilevamento dei progetti | 2226110 | Risolto il problema intermittente con la funzione **Genera requisito** nella griglia **Team di progetto**. |
| Pianificazione e rilevamento dei progetti | 2208109 | Gli utenti non possono creare un progetto in una valuta con attività correlate in un'altra valuta. |
| Pianificazione e rilevamento dei progetti | 2258228 | L'elenco dei campi autorizzati alla modifica con le entità **Pianificazione** che utilizzano l'API di pianificazione sono state aggiornate. |
| Pianificazione e rilevamento dei progetti | 2293989 | La lingua e le impostazioni internazionali corrette devono essere trasmesse alla griglia **Attività di progetto**.|
| Gestione risorse | 2220493 | Risolto il problema con l'esperienza dell'utente nella griglia **Attività** quando si contrassegna rapidamente una richiesta di risorse come completata. |
| Gestione risorse | 2330496 | Risolto il problema di caricamento della **Scheda di pianificazione**. L'aggiornamento della qualità è disponibile nella versione 4.11.0.164 |
| Ore e spesa | 2194431 | La griglia **Inserimento ore** deve onorare l'inizio della settimana come stabilito nelle **Impostazioni di sistema**. |
| Ore e spesa | 2277311 | Dopo aver eliminato il valore in una cella nella griglia **Inserimento ore** il cursore rimane nella griglia. |
