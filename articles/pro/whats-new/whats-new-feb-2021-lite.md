---
title: Novità di febbraio 2021 - Distribuzione semplice di Project Operations
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di febbraio 2021 di Distribuzione semplice di Project Operations.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f9f162dd07f62b1ef82367de7d8186002fedae57b56bb83dbc6741232d70e4f6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009311"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a>Novità di febbraio 2021 - Distribuzione semplice di Project Operations

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

  - Project Operations in ambiente Dataverse versione 4.7.0.95

## <a name="quality-updates"></a>Aggiornamenti di qualità

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| **Prezzi e fatturazione** | 2053736 | I dettagli della riga della fattura sono ora accessibili andando in **Fattura** > **Informazioni correlate**. |
| **Prezzi e fatturazione** | 2122613 | Le azioni **Attiva** e **Disattiva** sono state rimosse dalle entità associate **Listino prezzi**. |
| **Prezzi e fatturazione** | 2128606 | Risolto il problema con **ullReferenceException** nel plug-in **GetEstimatesForProject**. |
| **Distribuzione e configurazione** | 2140569 | La soluzione di progetto non deve essere installata negli ambienti Dataverse Teams. |
| **Distribuzione e configurazione** | 2086991 | Personalizzazione della localizzazione limitata delle risorse web. |
| **Gestione delle opportunità** | 2136794 | Viene visualizzato il messaggio di errore corretto quando il processo **Conferma fattura** o **Contrassegna fattura come pagata** non riesce. |
| **Gestione delle opportunità** | 2146376 | L'importo dell'imposta corretto in un valore effettivo non addebitabile viene creato dalla conferma della fattura. |
| **Pianificazione e rilevamento dei progetti** | 2099879 | La distribuzione dell'ambiente Dataverse deve creare una categoria di transazione predefinita con un ID statico e non generarne una in modo casuale per ambiente. |
| **Pianificazione e rilevamento dei progetti** | 2128577 | Corretti i privilegi dell'utente Project Service per aggiornare la categoria di transazione su un'assegnazione di risorse. |
| **Pianificazione e rilevamento dei progetti** | 2164035 | Problemi risolti con la funzione **Copia progetto**. |
| **Inserimento ore** | 2129161 | Vengono applicate restrizioni più rigide per garantire che gli utenti non possano modificare e aggiornare un inserimento ore inviato o approvato. |
| **Inserimento ore** | 2103572 | L'approvazione dell'ora per inserimenti ore non di progetto non deve cercare il ruolo di approvatore del progetto. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]