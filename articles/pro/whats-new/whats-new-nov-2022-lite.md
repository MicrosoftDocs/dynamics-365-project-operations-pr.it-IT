---
title: Novità della versione di novembre 2022 - Distribuzione di Project Operations Lite
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di novembre 2022 della distribuzione lite di Microsoft Dynamics 365 Project Operations.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: ed61f8c03c4ab1960aaf97712b3d46dc298ce96a
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831091"
---
# <a name="whats-new-november-2022---project-operations-lite-deployment"></a>Novità della versione di novembre 2022 - Distribuzione di Project Operations Lite

_**Si applica a:** Distribuzione lite: dalla transazione alla fatturazione proforma_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.58.0.119


## <a name="quality-updates"></a>Aggiornamenti di qualità

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Prezzi e fatturazione | 2781818 | Errore di chiave non trovata durante l'impostazione predefinita del prezzo per il registro di utilizzo del materiale. |
| Prezzi e fatturazione | 2922373 | Impossibile collegare la riga di offerta al progetto che è stato chiuso come offerta persa. |
| Prezzi e fatturazione | 2943206 | Il campo **Riga contratto** nell'entità progetto deve essere facoltativo. |
| Prezzi e fatturazione | 2953182 | Migliora il messaggio di errore per le fatture di correzione.|
| Prezzi e fatturazione | 2959500 | Impossibile collegare la riga di offerta a un'attività di progetto già associata a un'offerta persa.|
| Prezzi e fatturazione | 2959560 | Messaggio "Questo cliente è già nel contratto di progetto" ricevuto durante la chiusura dell'offerta come vinta in determinate località. |
| Prezzi e fatturazione | 3031727 | Le assegnazioni delle risorse non riescono con l'errore Campo obbligatorio "msdyn_Company" mancante. |
| Prezzi e fatturazione | 3036905 | La società proprietaria non viene mai inizializzata su ProjectTeamMember. |
| Gestione delle opportunità | 2763519 | Errore di riferimento null in EnsureProjectContractAllowsUpdates. |
| Gestione delle opportunità | 2783798 | Quando si importano le stime di progetto nella riga di offerta, mancano le descrizioni delle attività per le stime delle spese e dei materiali.|
| Gestione delle opportunità | 2988635 | Migliora la descrizione del messaggio di errore durante l'eliminazione del cliente nell'offerta. |
| Gestione delle opportunità | 3001191 | Impossibile creare un'offerta da un'opportunità in cui il metodo di fatturazione è specificato come null. |
| Aggiornamento | 3012324 | La conversione del progetto non riesce per un progetto con i caratteri di controllo come la tabulazione nel nome. || Pianificazione e rilevamento dei progetti | 2790384 | Il timeout OperationSet in sospeso è troppo breve. |
| Pianificazione e rilevamento dei progetti | 3044275 | Localizzazione mancante per: missingProjectSchedulerErrorMessage. |
| Pianificazione e rilevamento dei progetti | 3044277 | La griglia di riconoscimento di progetto non viene caricata quando la pianificazione non è impostata.|
| Gestione risorse | 2943153 | Aggiorna la scheda Registrazione per mostrare due cifre decimali per Durata.|
| Conto lavoro | 2932774 | Errore di generazione non corretta della riga fattura fornitore di sola lettura. |
| Conto lavoro | 2939556 | Lo stato dell'intestazione della fattura fornitore non deve essere impostato su bozza nell'eliminazione di riga se non è attivo. |
| Ore e spesa | 2939998 | Adotta la nuova versione di TESA in ProjOps. |
