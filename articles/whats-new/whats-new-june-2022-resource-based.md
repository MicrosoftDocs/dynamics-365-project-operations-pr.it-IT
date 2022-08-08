---
title: Novità di giugno 2022 - Project Operations per scenari di risorse/materiali non stoccati
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di giugno 2022 di Microsoft Dynamics 365 Project Operations per scenari basati su risorse/materiali non stoccati.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031336"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di giugno 2022 - Project Operations per scenari di risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in un ambiente Dataverse versione 4.43.0.77 o 4.43.0.119
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

La tabella seguente mostra le mappe a doppia scrittura che sono state modificate o aggiunte nella versione di Project Operations di giugno 2022.

| Mapping entità | Versione aggiornata | Commenti |
| --- | --- | --- |
| Entità di esportazione fattura fornitore progetto integrazione Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Deprecato il campo legacy e mappato al nuovo campo per il monitoraggio dello stato della fattura fornitore. |

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

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
| Conto lavoro | 2677485 | Aggiornata la versione di destinazione della mappa a doppia scrittura delle righe fattura fornitore. |
| Tempistica e spesa | 2700428 | È stata migliorata la logica delle approvazioni per garantire che altri set di approvazione per il progetto possano essere elaborati anche se uno dei set di approvazione è bloccato nei processi di sistema. |

### <a name="project-management-and-accounting-in-finance"></a>Contabilità e gestione dei progetti in Finance

Per informazioni sulle correzioni di bug incluse in questo aggiornamento, accedi a Microsoft Dynamics Lifecycle Services (LCS), e visualizza [l'articolo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
