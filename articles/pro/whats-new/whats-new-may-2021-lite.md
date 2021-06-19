---
title: Novità di maggio 2021 - Distribuzione semplice di Project Operations
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di maggio 2021 della distribuzione semplice di Project Operations.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060438"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Novità di maggio 2021 - Distribuzione semplice di Project Operations

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

   - Project Operations in ambiente Dataverse versione 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- [Modalità di pianificazione](../../project-management/scheduling-modes.md): i responsabili di progetto possono ora definire se un progetto deve essere gestito utilizzando una modalità di pianificazione a durata fissa, lavoro fisso o unità fisse.

## <a name="quality-updates"></a>Aggiornamenti di qualità

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Determinazione dei prezzi e fatturazione | 2224568 | Aggiunta logica per abilitare le personalizzazioni che implicano il richiamo del plug-in di conferma della fattura. |
| Determinazione dei prezzi e fatturazione | 2101098 | Migliorata la logica dei campi predefiniti per la fattura proforma. Questi campi includono, **Indirizzo di fatturazione**, **Nome fatturazione** e **Termini di pagamento**. I campi ora sono predefiniti dal record cliente del contratto di progetto corrispondente. |
| Determinazione dei prezzi e fatturazione | 2021413 | Aggiornati i campi **Costo effettivo** e **Vendite** nell'entità **Attività** per includere i valori di vendita delle spese non fatturate e fatturate delle attività. |
| Determinazione dei prezzi e fatturazione | 2182110 | Quando si copia un contratto di progetto, l'ID voce di contratto viene rigenerato nel contratto di progetto di destinazione per garantirne l'univocità. |
| Gestione delle opportunità | 2186741 | Aggiunte convalide per impedire l'aggiornamento del campo **Origine** e il tipo di transazione nei dettagli della riga di offerta esistente. |
| Gestione delle opportunità | 2191353 | La creazione di passaggi fondamentali non deve essere consentita in una voce di contratto di tempo e materiale. |
| Gestione delle opportunità | 2216956 | Risolti i problemi con **Aggiorna prezzi**. |
| Pianificazione e rilevamento | 2182979 | Migliorata la funzione di copia del progetto per garantire che le righe di stima delle spese vengano copiate dal progetto originale. |
| Pianificazione e rilevamento | 2184144 | Migliorata la funzione di copia del progetto per garantire che il nome della posizione della risorsa sia copiato dal progetto originale. |
| Pianificazione e rilevamento | 2184799 | Controllo rafforzato per garantire che la data di inizio stimata non possa essere modificata durante la copia del progetto. |
| Pianificazione e rilevamento | 2185134 | Durante la copia di un progetto, la data di inizio stimata del progetto di destinazione è impostata sulla data odierna. |
| Pianificazione e rilevamento | 2196373 | Assicurati che i record Responsabile di progetto e Membro del team non siano duplicati nel team di progetto durante la copia di un progetto. |
| Pianificazione e rilevamento | 2211833 | Le assegnazioni delle risorse vengono copiate dall'attività del progetto di origine nel progetto di destinazione. |
| Pianificazione e rilevamento | 2186541 | Risolti i problemi nella griglia **Stime** durante il raggruppamento per **Risorsa**. |
| Pianificazione e rilevamento | 2166906 | La categoria di transazione di un'attività deve essere copiata nell'entità **Assegnazione risorse**. |
| Gestione risorse | 2125362 | Risolti i problemi con la creazione di un membro del team generico utilizzando un metodo di allocazione basato sulle ore. |
| Ore e spesa | 2113603 | Risolto il problema relativo alla personalizzazione con la rimozione di attributi dalla pagina **Inserimento ore**. Il sistema controlla se l'attributo esiste nella pagina prima di accedervi utilizzando uno script. |
| Ore e spesa | 2204377 | I fogli presenze copiati devono essere visualizzati automaticamente quando selezioni **Copia settimana**. |
| Ore e spesa | 2209059 | Il campo **Stato** è modificabile per gli inserimenti ore di Dynamics 365 Field Service. |
