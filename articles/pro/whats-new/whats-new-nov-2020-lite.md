---
title: 'Novità di novembre 2020 - Distribuzione semplice di Project Operations: dalla transazione alla fatturazione proforma'
description: 'Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di novembre 2020 di Distribuzione semplice di Project Operations: dalla transazione alla fatturazione proforma.'
author: sigitac
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eb7c15fa937d508fa30ed2c04a6aa9cb117ef011
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272078"
---
# <a name="whats-new-november-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Novità di novembre 2020 - Distribuzione semplice di Project Operations: dalla transazione alla fatturazione proforma

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

La tabella seguente elenca gli aggiornamenti di Project Operations in ambiente CDS versione 4.4.0.70.

| Area funzionalità                 | Numero di riferimento | Aggiornamento di qualità                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Gestione delle opportunità       | 2036993          | La riga di stima e le righe del contratto di assegnazione delle risorse vengono aggiornate sulle offerte acquisite quando il tipo di riga di offerta è **Tutte le attività**.                                                 |
|   Gestione delle opportunità       | 2071514          | Non è possibile creare una fattura per un passaggio fondamentale a prezzo fisso su un contratto in cui è abilitata la fatturazione basata su attività.                                                                          |
| Determinazione dei prezzi e fatturazione          | 2070392          | Le righe del contratto di progetto sulla fattura aumentano ogni volta che **Aggiorna transazioni fattura** è selezionato.                                                                       |
| Pianificazione di un progetto             | 2043336          | Impossibile eliminare un record di un membro del team di progetto.                                                                                                                                    |
| Pianificazione di un progetto             | 2046013          | Comportamento incoerente per le colonne dei tag delle stime durante il caricamento rispetto al cambio del tipo di fase temporale.                                                                                   |
| Pianificazione di un progetto             | 2046647          | L'ora di inizio e di fine è disattivata per un'ora quando i requisiti di risorse vengono generati dai membri del team di progetto.                                                                      |
| Pianificazione di un progetto             | 2053879          | (Secondo l'imminente implementazione di CDS) PublishUnassignedAssignments interrompe il tentativo di salvare un'attività con l'errore "Il valore passato per ConditionOperator.In è vuoto." |
| Pianificazione di un progetto             | 2055501          | Il campo **Data di inizio del progetto** vuoto causa un errore nella pianificazione.                                                                                                      |
| Pianificazione di un progetto             | 2066817          | Non è possibile creare una risorsa generica utilizzando la selezione delle persone nella scheda **Attività**.                                                                                               |
| Pianificazione di un progetto             | 2067034          | Il pulsante **Visualizza dettagli** non è disponibile nella pagina **Dettagli dell'attività**.                                                                                                         |
| Gestione delle risorse          | 2046667          | I membri generici del team non vengono eliminati anche dopo che tutte le risorse sono state soddisfatte.                                                                                                     |
| Inserimento rapido spesa e ore | 2047499          | Il pulsante **Nuovo** nella pagina Inserimento ore apre la pagina **Nuova firma e-mail**.                                                                                               |
| Inserimento rapido spesa e ore | 2059859          | Quando si crea una voce di spesa viene visualizzato un pop-up imprevisto.                                                                                                                         |
| Altro                        | 2044181          | [Disinstallazione PO] - L'errore "Record non disponibile" si verifica quando si tenta di disinstallare le soluzioni di base di Project Service **msdyn_ProjectServiceCore_Patch** e msdyn.        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]