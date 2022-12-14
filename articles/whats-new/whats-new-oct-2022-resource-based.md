---
title: Novità della versione di ottobre 2022 - Project Operations per scenari basati su risorse/materiali non stoccati
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di ottobre 2022 di Microsoft Dynamics 365 Project Operations per scenari basati su risorse/materiali non stoccati.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806634"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità della versione di ottobre 2022 - Project Operations per scenari basati su risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.57.0.176
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.30

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

| Area funzionalità | Nome funzionalità | Altre informazioni |
| --- | --- | --- |
| Pianificazione e rilevamento dei progetti | **Pianificazione esterna di Project Operations**<br>La modalità di pianificazione esterna consente ai clienti di creare, aggiornare ed eliminare in modo nativo entità correlate alle strutture di suddivisione del lavoro (WBS) usando le API Dataverse native, ma senza gli attuali limiti imposti da Microsoft Project for the Web. | [Pianificazione esterna](/dynamics365/project-operations/project-management/external-scheduling) |
| Distribuzione e configurazione | <p>**Consenti ai clienti di scegliere il tipo di distribuzione**<br>Gli aggiornamenti guidati dal prodotto (PDU) di Project Operations vengono usati per installare automaticamente la soluzione doppia scrittura di Project Operations quando nell'ambiente sono installate le soluzioni doppia scrittura core e di orchestrazione.</p><p>Questa funzione introduce un nuovo parametro **Comportamento di aggiornamento della soluzione** nei parametri di progetto. Quando questo parametro è impostato su **Solo Lite**, gli aggiornamenti guidati dal prodotto non installano automaticamente la soluzione doppia scrittura di Project Operations anche se nell'ambiente sono installate le soluzioni doppia scrittura core e di orchestrazione. Questo comportamento andrà a vantaggio dei clienti che intendono utilizzare le soluzioni di doppia scrittura per integrare gli ordini cliente nelle app per la finanza e le operazioni, ma desiderano utilizzare Project Operations in modalità Lite (ovvero senza integrazione nelle app per la finanza e le operazioni).</p> | |
| Prezzi e fatturazione | <p>**Conversione di valuta per transazioni di vendita non fatturate di spesa in ambienti integrati**<br>Per i clienti che usano Project Operations integrato con le app per la finanza e le operazioni (ovvero nel tipo di distribuzione risorsa/non in stock), i tassi di cambio sono in genere controllati nelle app per la finanza e le operazioni. Tuttavia, se una categoria di spesa deve essere valutata utilizzando il metodo di calcolo del prezzo "al costo" o "ricarico sul costo" quando il cliente viene fatturato, il tasso di cambio utilizzato per calcolare l'importo delle vendite utilizza i tassi di cambio in Dataverse, non i tassi di cambio delle app per la finanza e le operazioni.</p><p>Questa funzione introduce un nuovo parametro **Comportamento conversione di valuta** nei parametri di progetto. Quando questo parametro è impostato su **Esteso con fallback**, gli importi delle vendite non fatturate sulle transazioni di spesa vengono calcolati utilizzando i tassi di cambio delle app per la finanza e le operazioni.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Non sono disponibili aggiornamenti per le mappe a doppia scrittura di Project Operations in questa versione. Per un elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni della mappa a doppia scrittura di Project Operations](../environment/resource-dual-write-maps.md).

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Prezzi e fatturazione | 2316317 | Il sistema consente di creare fatture senza transazioni addebitabili. |
| Prezzi e fatturazione | 2737300 | Convalida per la disponibilità del campo **Cliente** prima di accedere al modulo. |
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
| Pianificazione e rilevamento dei progetti | 2957840 | Le attività non possono essere salvate e le colonne non possono essere aggiunte alla pagina **Attività** in Project Operations integrato. |
| Gestione risorse | 2751560 | Unità organizzative preferite incoerenti nel requisito di risorsa. |
| Conto lavoro | 2853245 | L'abbinamento per i valori effettivi della riga fattura fornitore non aggiorna lo stato di verifica se una riga contratto è già collegata alla riga fattura fornitore. |
| Conto lavoro | 2907231 | La fase di elaborazione delle fatture fornitore non può avanzare. |
| Ore e spesa | 2867363 | I record non vengono aggiornati dalla visualizzazione Assenze/Ferie per l'approvazione quando sono in coda per l'approvazione. |
| Ore e spesa | 2894405 | TESA: la directory POC inutilizzata causa problemi di conformità. |

### <a name="project-management-and-accounting-in-finance"></a>Contabilità e gestione dei progetti in Finance

Per informazioni sulle correzioni di bug incluse in questo aggiornamento, accedi a Microsoft Dynamics Lifecycle Services e visualizza [l'articolo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
