---
title: Novità di novembre 2022 - Project Operations per scenari basati su risorse/materiali non stoccati
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di novembre 2022 di Microsoft Dynamics 365 Project Operations per scenari basati su risorse/materiali non stoccati.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831086"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di novembre 2022 - Project Operations per scenari basati su risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.58.0.119
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Non sono disponibili aggiornamenti per le mappe a doppia scrittura di Project Operations in questa versione. Per un elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni della mappa a doppia scrittura di Project Operations](../environment/resource-dual-write-maps.md).

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

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


### <a name="project-management-and-accounting-in-finance"></a>Contabilità e gestione dei progetti in Finance

Per informazioni sulle correzioni di bug incluse in questo aggiornamento, accedi a Microsoft Dynamics Lifecycle Services e visualizza [l'articolo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
