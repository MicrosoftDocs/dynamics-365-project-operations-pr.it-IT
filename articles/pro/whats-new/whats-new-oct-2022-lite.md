---
title: Novità della versione di ottobre 2022 - Distribuzione di Project Operations Lite
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di ottobre 2022 della distribuzione lite di Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806639"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Novità della versione di ottobre 2022 - Distribuzione di Project Operations Lite

_**Si applica a:** Distribuzione lite: dalla transazione alla fatturazione proforma_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.57.0.176

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

| Area funzionalità | Nome funzionalità | Altre informazioni |
| --- | --- | --- |
| Pianificazione e rilevamento dei progetti | **Pianificazione esterna di Project Operations**<br>La modalità di pianificazione esterna consente ai clienti di creare, aggiornare ed eliminare in modo nativo entità correlate alle strutture di suddivisione del lavoro (WBS) usando le API Dataverse native, ma senza gli attuali limiti imposti da Microsoft Project for the Web. | [Pianificazione esterna](/dynamics365/project-operations/project-management/external-scheduling) |
| Distribuzione e configurazione | <p>**Consenti ai clienti di scegliere il tipo di distribuzione**<br>Gli aggiornamenti guidati dal prodotto (PDU) di Project Operations vengono usati per installare automaticamente la soluzione doppia scrittura di Project Operations quando nell'ambiente sono installate le soluzioni doppia scrittura core e di orchestrazione.</p><p>Questa funzione introduce un nuovo parametro **Comportamento di aggiornamento della soluzione** nei parametri di progetto. Quando questo parametro è impostato su **Solo Lite**, gli aggiornamenti guidati dal prodotto non installano automaticamente la soluzione doppia scrittura di Project Operations anche se nell'ambiente sono installate le soluzioni doppia scrittura core e di orchestrazione. Questo comportamento andrà a vantaggio dei clienti che intendono utilizzare le soluzioni di doppia scrittura per integrare gli ordini cliente nelle app per la finanza e le operazioni, ma desiderano utilizzare Project Operations in modalità Lite (ovvero senza integrazione nelle app per la finanza e le operazioni).</p> | |

## <a name="quality-updates"></a>Aggiornamenti di qualità

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Prezzi e fatturazione | 2316317 | Il sistema consente di creare fatture senza transazioni addebitabili. |
| Prezzi e fatturazione | 2737300 | Convalida per la disponibilità del campo Cliente prima di accedere al modulo. |
| Prezzi e fatturazione | 2744948 | Aggiungi un controllo nullo per il metodo di fatturazione. |
| Prezzi e fatturazione | 2763515 | Handle di errore di riferimento null quando manca il contratto di vendita della fattura. |
| Prezzi e fatturazione | 2844301 | La creazione batch della fattura non riesce a causa di un errore. |
| Prezzi e fatturazione | 2845869 | Archiviazione errata del servizio di organizzazione. |
| Prezzi e fatturazione | 2853729 | I dettagli del ruolo e del prezzo vengono aggiornati quando viene modificato il tipo di fatturazione. |
| Prezzi e fatturazione | 2940350 | Quando vengono calcolati i prezzi effettivi, devono essere inseriti automaticamente solo i listini prezzi attivi. |
| Distribuzione e configurazione | 3001206 | L'entità msdyn\_replaylogheader impedisce gli aggiornamenti delle organizzazioni cliente. |
| Gestione delle opportunità | 2755582 | Le eccezioni di riferimento null vengono gestite nell'helper regola di fatturazione separata. |
| Gestione delle opportunità | 2761477 | Quando si utilizza la fatturazione separata, l'eliminazione di un passaggio fondamentale (intestazione) lascia i passaggi fondamentali orfani. |
| Gestione delle opportunità | 2767595 | Quando un record di utilizzo del materiale viene aperto nel modulo principale, la risorsa prenotabile per il record viene modificata nell'utente attualmente connesso. |
| Pianificazione e rilevamento dei progetti | 2790384 | Il timeout OperationSet in sospeso è troppo breve. |
| Gestione risorse | 2751560 | Unità organizzative preferite incoerenti nel requisito di risorsa. |
| Conto lavoro | 2907231 | La fase di elaborazione delle fatture fornitore non può avanzare. |
| Ore e spesa | 2867363 | I record non vengono aggiornati dalla visualizzazione Assenze/Ferie per l'approvazione quando sono in coda per l'approvazione. |
| Ore e spesa | 2894405 | TESA: la directory POC inutilizzata causa problemi di conformità. |
