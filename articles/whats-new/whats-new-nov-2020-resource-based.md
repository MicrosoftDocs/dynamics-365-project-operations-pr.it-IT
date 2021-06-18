---
title: Novità di novembre 2020 - Project Operations per scenari basati su risorse/non stoccate
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di novembre 2020 di Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f6b14a1cbe7f3d41c86aedaf863434214f911eaa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995626"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di novembre 2020 - Project Operations per scenari basati su risorse/non stoccate

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

- Project Operations in ambiente CDS versione 4.4.0.70
- Gestione progetti e contabilità in ambiente Dynamics 365 Finance versione 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Aggiornamenti di Project Operations per scenari basati su risorse/non stoccate

### <a name="project-operations-on-cds"></a>Project Operations in CDS

| Area funzionalità                 | Numero di riferimento | Aggiornamento di qualità                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Gestione delle opportunità       | 2036993          | La riga di stima e le righe del contratto di assegnazione delle risorse vengono aggiornate sulle offerte acquisite quando il tipo di riga di offerta è **Tutte le attività**.                                                 |
| Determinazione dei prezzi e fatturazione          | 2070392          | Le righe del contratto di progetto sulla fattura aumentano ogni volta che **Aggiorna transazioni fattura** è selezionato.                                                                         |
| Pianificazione di un progetto             | 2043336          | Impossibile eliminare un record di un membro del team di progetto.                                                                                                                                  |
| Pianificazione di un progetto             | 2046013          | Comportamento incoerente per le colonne dei tag delle stime durante il caricamento rispetto al cambio del tipo di fase temporale.                                                                                   |
| Pianificazione di un progetto             | 2046647          | L'ora di inizio e di fine è disattivata per un'ora quando i requisiti di risorse vengono generati dai membri del team di progetto.                                                                      |
| Pianificazione di un progetto             | 2053879          | (Secondo l'imminente implementazione di CDS) PublishUnassignedAssignments interrompe il tentativo di salvare un'attività con l'errore "Il valore passato per ConditionOperator.In è vuoto."                       |
| Pianificazione di un progetto             | 2055501          | Il campo **Data di inizio del progetto** vuoto causa un errore nella pianificazione.                                                                                                      |
| Pianificazione di un progetto             | 2066817          | Non è possibile creare una risorsa generica utilizzando la selezione delle persone nella scheda **Attività**.                                                                                                   |
| Pianificazione di un progetto             | 2067034          | Il pulsante **Visualizza dettagli** non è disponibile nella pagina **Dettagli dell'attività**.                                                                                                       |
| Gestione delle risorse          | 2046667          | I membri generici del team non vengono eliminati anche dopo che tutte le risorse sono state soddisfatte.                                                                                                    |
| Inserimento rapido spesa e ore | 2047499          | Il pulsante **Nuovo** nella pagina Inserimento ore apre la pagina **Nuova firma e-mail**.                                                                                               |
| Inserimento rapido spesa e ore | 2059859          | Quando si crea una voce di spesa viene visualizzato un pop-up imprevisto.                                                                                                                         |
| Altro                        | 2044181          | (Disinstallazione dell'ordine di acquisto) Quando si tenta di disinstallare le soluzioni di base di Project Service msdyn_ProjectServiceCore_Patch e msdyn, si verifica l'errore "Record non disponibile".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Contabilità e gestione dei progetti in Dynamics 365 Finance

| Area funzionalità        | Numero di riferimento | Aggiornamento di qualità                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Riconoscimento ricavi | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | La percentuale di completamento della stima del progetto è errata quando il contratto utilizza una valuta estera e la percentuale di avanzamento del lavoro per il metodo di completamento.                     |
| Riconoscimento ricavi | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Impossibile pubblicare stime con il metodo di completamento **Costo effettivo**.                                                                                                    |
| Riconoscimento ricavi | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | L'eliminazione non riesce a causa di un errore di sbilanciamento del giustificativo quando la valuta della società e la valuta della transazione sono diverse.                                              |
| Gestione spese  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Per gli utenti non amministratori, i valori di ricerca per le colonne delle righe di spesa come **ID progetto** e **Categoria di spesa** non vengono visualizzati correttamente nel frame del connettore dati. |
| Gestione spese  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | L'impostazione predefinita della proprietà della riga non viene visualizzata per le categorie di spesa.                                                                                                         |
| Gestione spese  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | L'integrazione delle spese deve includere la proprietà della riga dalla nota spese.                                                                                             |
| Fattura           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Impossibile pubblicare le proposte di fatturazione del progetto a causa di un messaggio di errore che indica che la combinazione di FD non è stata convalidata.                                                    |
| Fattura           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Non è possibile visualizzare le transazioni dalla pagina dei dettagli **fattura**.                                                                                                              |
| Fattura           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Le righe di proposta di fattura possono essere eliminate.                                                                                                                                  |
| Contabilità di progetto  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Le voci del menu **Previsione** non sono visibili nella pagina elenco **Progetti**.                                                                                                   |
| Contabilità di progetto  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Impossibile aprire **Istruzione progetto**   > **Transazioni e previsioni**.                                                                                                       |
| Contabilità di progetto  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Regola contabilità** non è abilitato per le transazioni di progetto fatturate.                                                                                                  |
| Contabilità di progetto  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | I dettagli contabili non sono inclusi nella tabella **ProjCDSActualsImport** quando il giornale di registrazione **integrazione** è registrato.                                                  |
| Contabilità di progetto  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | La voce di previsione del progetto viene raddoppiata quando si rimuove e quindi si riaggiunge un'assegnazione di risorse.                                                                            |
| Contabilità di progetto  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | La selezione di un collegamento ID progetto non apre l'URL del collegamento diretto CDS.                                                                                                         |
| Contabilità di progetto  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Non è possibile aggiornare la data di inizio di un'attività in CDS.                                                                                                                           |
| Contabilità di progetto  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Abilitando la funzione, non è possibile utilizzare le righe di contratto multiple senza l'integrazione di CDS.                                                                                   |

### <a name="regulatory-updates"></a>Aggiornamenti normativi
Per informazioni sugli aggiornamenti normativi per le app Finance and Operations, vedi [Aggiornamenti normativi](/dynamics365/finance/localizations/regulatory-updates). È inoltre possibile accedere a LCS e visualizzare gli aggiornamenti normativi pianificati utilizzando lo strumento di ricerca dei problemi. La ricerca dei problemi ti consente di cercare per paese, tipo di funzionalità e versione.


[!INCLUDE[footer-include](../includes/footer-banner.md)]