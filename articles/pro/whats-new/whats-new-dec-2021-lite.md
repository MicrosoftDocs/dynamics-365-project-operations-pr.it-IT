---
title: Novità della versione di dicembre 2021 - Distribuzione di Project Operations Lite
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di dicembre 2021 della distribuzione di Project Operations Lite.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585383"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novità della versione di dicembre 2021 - Distribuzione di Project Operations Lite

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

### <a name="subcontract-management"></a>Gestione dei conti lavoro 

- [Membri del team di progetto in conto lavoro](../subcontracting/subcontracting-project-team-members.md): un responsabile di progetto può creare membri del team denominati o generici con conto lavoro e righe di conto lavoro per influire sul personale e sulla stima.
- [Opzioni di conto lavoro per i membri del team di progetto](../subcontracting/subcon-options.md): quando si effettuano scelte di personale per membri del team di progetto denominati o generici, il responsabile di progetto può rivedere i conti lavoro esistenti o creare nuovi conto lavoro per uno o più membri del team di progetto. 
- [Stima dei costi delle assegnazioni di risorse in conto lavoro](../subcontracting/costing-subcon-ra.md): la stima dei costi del progetto terrà conto delle assegnazioni delle risorse in conto lavoro e le calcola utilizzando i listini prezzi di acquisto associati ai conti lavoro. 
- [Configura la scheda di pianificazione per mostrare i lavoratori a contratto e la capacità in conto lavoro](../subcontracting/configure-sb-subcon.md): la scheda di pianificazione in Project Operations può ora essere configurata per cercare e suggerire il tipo di lavoratore a contratto di risorse prenotabili e capacità in conto lavoro insieme ai dipendenti. Questa configurazione può essere applicata durante la ricerca di risorse nel contesto del personale per un requisito di progetto specifico o durante la ricerca al di fuori del contesto di un requisito di progetto.
- [Personale di un progetto con lavoratori a contratto e capacità in conto lavoro](../subcontracting/staffing-cw.md): ora i lavoratori a contratto possono essere prenotati su progetti utilizzando le esperienze della scheda di pianificazione.
- [Registrazione di tempi, spese e utilizzo di materiale su progetti per componenti in conto lavoro](../subcontracting/recording-subcon-actuals.md): i lavoratori a contratto possono registrare tempi e spese e i membri del team di progetto possono anche registrare l'utilizzo di materiali acquistati utilizzando un conto lavoro su un progetto. Ciò si tradurrà nella registrazione accurata dei costi sui progetti che utilizzano capacità o materiali acquistati.
- [Transizioni di stato su un conto lavoro](../subcontracting/subcon-states.md): i conti lavoro possono essere verificati per completare la negoziazione con il fornitore, chiusi per indicare il completamento della consegna o annullati per indicare la risoluzione del contratto con il fornitore prima del completamento della consegna.

### <a name="task-planning"></a>Pianificazione delle attività
- Guida alla risoluzione dei problemi migliorata per gli amministratori di sistema. Quando un utente non può aprire un progetto, l'amministratore può esaminare gli errori non relativi alla licenza generati da Project for the Web nei [Registri di pianificazione del progetto](../../project-management/schedule-api-logs.md).
- [Usa gli elenchi di controllo delle attività in Microsoft Project for the web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). In Microsoft Project for the Web è possibile aggiungere un elenco di controllo a un'attività per tenere traccia di elementi specifici.

## <a name="quality-updates"></a>Aggiornamenti di qualità

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Pianificazione e rilevamento | 2392596 | Le API di pianificazione ora consentono gli aggiornamenti ai campi **Lavoro rimanente**, **Lavoro completato**, e **% completamento**. |
| Pianificazione e rilevamento | 2478497 | I campi delle API di pianificazione **Numero attività** e **ID attività** possono essere vuoti perché il sistema li compilerà utilizzando la numerazione automatica.|
| Ore e spesa | 2468135 | Il numero di nuovi tentativi di approvazione è ridotto da cinque a tre. |
| Ore e spesa | 2468188 | Risolto il problema con il testo del registro che superava la lunghezza massima nell'attributo **notetext** dell'entità **annotazione**. |
