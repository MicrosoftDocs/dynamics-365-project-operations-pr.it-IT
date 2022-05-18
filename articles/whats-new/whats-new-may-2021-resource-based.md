---
title: Novità di maggio 2021 - Project Operations per scenari basati su risorse/materiali non stoccati
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di maggio 2021 di Project Operations per scenari basati su risorse/materiali non stoccati.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d0af6d99a24619b3613a3aaa027404556b1b81c4
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723773"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di maggio 2021 - Project Operations per scenari basati su risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

- Project Operations sulla versione degli ambienti Dynamics 365 Dataverse 4.10.0.186
- Gestione progetti e contabilità in ambienti per app per la finanza e le operazioni versione 10.0.18

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- [Modalità di pianificazione](../project-management/scheduling-modes.md): i responsabili di progetto possono definire se un progetto deve essere gestito utilizzando la modalità di pianificazione a durata fissa, lavoro fisso o unità fisse.
- [Imposta l'indennità di trasferta utilizzando i livelli delle tariffe per le indennità](../expense/set-up-mileage.md): aggiorna i livelli della tariffa chilometrica per le note spese dei dipendenti.

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Il seguente elenco mostra le mappe a doppia scrittura che sono state modificate o aggiunte nella versione Project Operations di maggio 2021.

| Mapping entità | Versione aggiornata | Commenti |
| --- | --- | --- |
| Fonte di finanziamento del progetto (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sincronizzazione dei termini di pagamento del cliente del contratto di progetto. |
| Proposta di fattura di progetto V2 (fatture) | 1.0.0.3 | Sincronizzazione dei termini di pagamento della fattura proforma. |
| Entità di esportazione riga fattura fornitore progetto integrazione Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Aggiornamenti di qualità |
| Progetti V2 (msdyn\_projects) | 1.0.0.2 | Aggiornamenti di qualità |

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione delle app per la finanza e le operazioni. Alcune funzionalità e capacità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato una mappa di tabella predefinita, riapplica le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema con l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi di doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Prezzi e fatturazione | 2227635 | I valori nei campi **Gruppo unità** e **Unità** vengono predefiniti dal prodotto nella griglia **Stime materiali**. |
| Prezzi e fatturazione | 2234127 | Il campo **ID attività** ora si integra correttamente con gli effettivi del progetto Dataverse quando viene registrata una fattura fornitore. |
| Prezzi e fatturazione | 2235564 | Il salvataggio della riga del giornale di registrazione garantisce che la valuta visualizzata nella voce della riga del giornale di registrazione corrisponda alla valuta predefinita della riga dopo il salvataggio. |
| Prezzi e fatturazione | 2246671 | Rendere una transazione non addebitabile durante la fatturazione storna il record delle vendite non fatturate originale e crea un nuovo record delle vendite non fatturate come non addebitabile. |
| Prezzi e fatturazione | 2264042 | La correzione della fattura valida non deve essere bloccata se sono presenti dettagli di correzione della fattura non validi nell'ambiente. |
| Prezzi e fatturazione | 2146367 | La mappatura a doppia scrittura dell'intestazione della fattura di progetto è stata estesa per includere i termini di pagamento. |
|   Gestione delle opportunità | 2086888 | Non aggiungere ruoli e categorie disattivati prima di aver copiato un'offerta in ruoli e categorie a pagamento di un preventivo di cui si è appena effettuata un'offerta. |
|   Gestione delle opportunità | 2234376 | I campi di sola lettura sono disattivati nella griglia **Stime materiali**. |
|   Gestione delle opportunità | 2238337 | Un'offerta basata su un contatto può essere salvata anche se non è associata a un listino prezzi di progetto. |
|   Gestione delle opportunità | 2239810 | La chiusura di un'offerta come persa chiude anche il progetto associato e annulla eventuali prenotazioni. |
| Pianificazione e rilevamento dei progetti | 2099559 | Aggiunte ulteriori convalide per l'integrità del sistema prima dell'apertura della griglia **Attività di progetto**. |
| Pianificazione e rilevamento dei progetti | 2178987 | Risolto un errore temporaneo che si verifica durante la selezione di **Fase successiva** nella pagina **Progetto**. |
| Gestione risorse | 2224817 | La funzionalità di estendere le prenotazioni è predefinita per lo stato delle prenotazioni corretto. |
| Inserimento ore | 2202476 | La pagina **Inserimento ore** utilizza ora il controllo della griglia di reazione e risolve problemi come il disallineamento della griglia. |
| Inserimento ore | 2223377 | L'inserimento ore è nascosto dalla sezione **Elementi correlati** nella pagina **Risorsa prenotabile** per evitare confusione con l'usabilità. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestione progetti e contabilità in Dynamics 365 Finance

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Contabilità e gestione dei progetti | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | In Project Operations per scenari basati su risorse: non è possibile convertire un preventivo in vinto a causa di un errore di integrazione. |
| Contabilità e gestione dei progetti | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | In Project Operations: viene visualizzato un messaggio di errore quando si tenta di associare una voce di contratto a un ID progetto a causa del controllo della sovrapposizione di voci di contratto e tipi di transazione. |
| Contabilità e gestione dei progetti | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** imposta l'indirizzo di fatturazione della fonte di finanziamento da un cliente diverso. |
| Viaggi e spese | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Si può verificare un errore di pubblicazione relativo all'impostazione del chilometraggio. |
| Viaggi e spese | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | La funzionalità **Dividi in personale** non funziona per le transazioni di spesa in valuta estera. |
| Viaggi e spese | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | I valori del menu a discesa della categoria di spese visualizzano categorie non corrette per i delegati indipendentemente dal fatto che siano una risorsa. |
| Viaggi e spese | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Non è possibile salvare una nota spese interaziendale a causa di un errore di **convalida della risorsa/categoria**. |
| Viaggi e spese | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Il calcolo della tariffa chilometrica errato nella registrazione della nota spese presenta righe di divisione. |
| Viaggi e spese | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Non è possibile registrare una nota spese interaziendale quando l'IVA è inclusa e il tipo di conto di contropartita nel metodo di pagamento è **Lavoratore**. |
| Viaggi e spese | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Rollback dell'entità di dati **TrvRequisitionLine** e dell'indice univoco associato. |
| Viaggi e spese | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Report spese supporta la creazione e l'aggiornamento della riga del documento di origine. |
| Viaggi e spese | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Un giornale di registrazione secondario non corretto viene visualizzato in uno scenario interaziendale se l'IVA viene registrata nella persona giuridica di destinazione. |
| Viaggi e spese | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: le stime di spesa non vengono eliminate da Finance quando vengono eliminate da Dataverse. |
| Viaggi e spese | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Quando la categoria di spesa è una categoria non di progetto, le dimensioni finanziarie selezionate nella pagina **Spese** non vengono copiate nella nota spese. |
