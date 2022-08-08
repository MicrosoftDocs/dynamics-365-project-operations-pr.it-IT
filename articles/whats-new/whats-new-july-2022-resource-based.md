---
title: Novità di luglio 2022 - Project Operations per scenari di risorse/materiali non stoccati
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di luglio 2022 di Microsoft Dynamics 365 Project Operations per scenari basati su risorse/materiali non stoccati.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183908"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di luglio 2022 - Project Operations per scenari basati su risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.44.0.22
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Non sono disponibili aggiornamenti per le mappe a doppia scrittura di Project Operations in questa versione. Per un elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni della mappa a doppia scrittura di Project Operations](../environment/resource-dual-write-maps.md).

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Distribuzione e configurazione | 2761472 | Viene gestito un errore di installazione di Project Operations. |
| Prezzi e fatturazione | 2746940 | Il nome della voce di conto lavoro deve avere una lunghezza massima di 100 caratteri. |
| Prezzi e fatturazione | 2739162 | I clienti devono essere in grado di vedere i pulsanti della barra multifunzione nella visualizzazione griglia dei valori effettivi. |
| Pianificazione e rilevamento dei progetti | 2730318 | Convalida aggiornata per caratteri non supportati nell'oggetto del progetto. |
| Prezzi e fatturazione | 2705361 | I valori effettivi delle vendite fatturate per passaggio fondamentale devono essere inclusi nei campi di monitoraggio del progetto. |
| Prezzi e fatturazione | 2675880 | Impedire il collegamento di un progetto a una voce di contratto non basata sul lavoro. |
| Prezzi e fatturazione | 2664396 | Se il listino prezzi di un'offerta viene salvato senza un'offerta, deve esserci un errore indicante che l'offerta non può essere vuota. |
| Prezzi e fatturazione | 2184019 | La scheda **Fatturazione basata su attività** non deve essere visualizzata per i progetti che non hanno un contratto o un'offerta di supporto. |

### <a name="project-management-and-accounting-in-finance"></a>Contabilità e gestione dei progetti in Finance

Per informazioni sulle correzioni di bug incluse in questo aggiornamento, accedi a Microsoft Dynamics Lifecycle Services (LCS), e visualizza [l'articolo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funzionalità attivate per impostazione predefinita nella prossima versione

Questa tabella elenca le funzionalità attivate per impostazione predefinita nella versione 10.0.29. La maggior parte delle funzionalità che sono state attivate automaticamente può essere disattivata in [Gestione funzionalità](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). In futuro, alcune funzionalità che sono state attivate automaticamente potrebbero essere rimosse da Gestione funzionalità e diventare obbligatorie. Questa modifica garantisce l'uso della funzionalità corrente da parte dei clienti, di modo che i miglioramenti possano essere basati sulla funzionalità corrente man mano che vengono aggiunti. Le funzionalità non verranno mai abilitate automaticamente in meno di un anno, a meno che non siano ritenute essenziali.

| Nome funzionalità | Data abilitazione | Funzionalità aggiunta | Stato funzionalità | Modulo |
| --- | --- | --- |--- |--- |
| Abilita rettifica della transazione oraria in base alla modifica dell'allocazione delle regole di finanziamento | 16 settembre 2022 | 7 ottobre 2020 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |
| Funzionalità di storno della fattura di pagamento anticipato dell'ordine di acquisto del progetto | 16 settembre 2022 | 6 ottobre 2021 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |
| Elimina righe della proposta di fattura quando si utilizza Project Operations per scenari basati su risorse/materiali non stoccati | 16 settembre 2022 | 6 ottobre 2021 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |
| Rettifica contabilità in una transazione di progetto registrata | 16 settembre 2022 | 10 Maggio 2020 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |
| Abilita impostazione della contabilità predefinita per il progetto | 16 settembre 2022 | 19 febbraio 2020 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |
| Abilita più voci di contratto per un progetto | 16 settembre 2022 | 29 giugno 2020 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |
| Rendi i giornali di registrazione ore di progetto di sola lettura se lo stato di approvazione corrente non consente la modifica | 16 settembre 2022 | 6 ottobre 2021 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |
| Abilita sincronizzazione delle righe di vendita in base alle righe di acquisto quando le righe di acquisto vengono aggiornate e il parametro di gestione delle modifiche all'ordine di acquisto è attivato | 16 settembre 2022 | 7 ottobre 2020 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |
| Abilitare Project Operations in Dynamics 365 Customer Engagement | 16 settembre 2022 | 29 giugno 2020 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |
| Funzionalità di correzione dello storno di transazione del progetto | 16 settembre 2022 | 13 luglio 2020 | Attiva per impostazione predefinita | Contabilità e gestione dei progetti |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funzionalità che diventeranno obbligatorie nella prossima versione

La tabella seguente elenca le funzionalità che diventeranno obbligatorie a partire dalla versione 10.0.29.

| Nome funzionalità | Data abilitazione | Funzionalità aggiunta | Stato funzionalità | Modulo |
| --- | --- | --- | --- | --- |
| Calcola valore impegnato in base alla fonte di finanziamento senza arrotondamento del tasso di cambio | 16 settembre 2022 | 14 giugno 2020 | Obbligatorio | Contabilità e gestione dei progetti |
| Abilita registrazione della rettifica del progetto con lo stesso conto di contabilità generale della transazione originale | 16 settembre 2022 | 14 giugno 2020 | Obbligatorio | Contabilità e gestione dei progetti |
| Dettaglio dell'importo impegnato del contratto di progetto | 16 settembre 2022 | 31 agosto 2019 | Obbligatorio | Contabilità e gestione dei progetti |
| Abilita ordinamento per risorsa durante la creazione della proposta di fattura di progetto | 16 settembre 2022 | 31 agosto 2019 | Obbligatorio | Contabilità e gestione dei progetti |
