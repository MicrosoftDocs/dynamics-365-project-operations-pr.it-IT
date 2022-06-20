---
title: Novità di aprile 2021 - Distribuzione semplice di Project Operations
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di aprile 2021 della distribuzione lite di Project Operations.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 987eeaf2e57659a6facae6b0a3688f15992e8bb9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931244"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Novità di aprile 2021 - Distribuzione semplice di Project Operations

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo articolo si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

  - Project Operations in ambiente Dataverse versione 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- Materiali non stoccati per progetti. Le funzionalità chiave includono:
  - Stima e prezzo dei materiali non stoccati durante il ciclo di vendita di un progetto. Per ulteriori informazioni, vedi [Impostare le tariffe di vendita e costi per i prodotti del catalogo - semplice](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Monitoraggio dell'utilizzo di materiali non stoccati durante la consegna del progetto. Per ulteriori informazioni, vedi [Registrare l'utilizzo di materiale in progetti e attività di progetto](../../material/material-usage-log.md).
  - La fatturazione ha utilizzato costi di materiali non stoccati. Per ulteriori informazioni, vedi [Gestire il backlog di fatturazione - semplice](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Nuove API in Dynamics 365 Dataverse consentono l'esecuzione di operazioni di creazione, aggiornamento ed eliminazione con **Entità di pianificazione**. Per ulteriori informazioni, vedi [Utilizzare le API di pianificazione per eseguire operazioni con le entità di pianificazione](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Aggiornamenti di qualità

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Determinazione dei prezzi e fatturazione | 2224568 | Aggiunta logica per abilitare le personalizzazioni che implicano il richiamo del plug-in di conferma della fattura. |
| Determinazione dei prezzi e fatturazione | 2101098 | Migliorata la logica dei campi predefiniti per la fattura proforma: i valori di **Indirizzo di fatturazione**, **Nome fatturazione** e **Condizioni di pagamento** ora coincidono con il record Cliente contratto di progetto corrispondente. |
| Determinazione dei prezzi e fatturazione | 2021413 | Aggiornati i campi **Costo effettivo** e **Vendite** nell'entità **Attività** per includere i valori di vendita delle spese non fatturate e fatturate delle attività. |
| Determinazione dei prezzi e fatturazione | 2182110 | Quando si copia un contratto di progetto, l'ID voce di contratto viene rigenerato nel contratto di progetto di destinazione per garantirne l'univocità. |
| Gestione delle opportunità | 2186741 | Aggiunte convalide per impedire l'aggiornamento dei campi **Origine** e **Tipo di transazione** nei dettagli della riga di offerta esistente. |
| Gestione delle opportunità | 2191353 | I passaggi fondamentali non devono essere creati in una voce di contratto di tempo e materiale. |
| Gestione delle opportunità | 2216956 | Problemi risolti con **Aggiorna prezzi**. |
| Pianificazione e rilevamento | 2182979 | Migliorata la funzione di copia del progetto per garantire che le righe di stima delle spese vengano copiate dal progetto originale. |
| Pianificazione e rilevamento | 2184144 | Migliorata la funzione di copia del progetto per garantire che il nome della posizione della risorsa sia copiato dal progetto originale. |
| Pianificazione e rilevamento | 2184799 | Copia del progetto: controllo rafforzato per garantire che la data di inizio stimata non possa essere modificata durante la copia. |
| Pianificazione e rilevamento | 2185134 | Copia del progetto: la data di inizio stimata del progetto di destinazione è impostata sulla data odierna. |
| Pianificazione e rilevamento | 2196373 | Copia del progetto: assicurati che i record Responsabile di progetto e Membro del team non siano duplicati nel team di progetto. |
| Pianificazione e rilevamento | 2211833 | Copia del progetto: le assegnazioni delle risorse vengono copiate dall'attività del progetto di origine nel progetto di destinazione. |
| Pianificazione e rilevamento | 2186541 | Risolti i problemi nella griglia **Stime** durante il raggruppamento per risorsa. |
| Pianificazione e rilevamento | 2166906 | La categoria di transazione di un'attività deve essere copiata nell'entità **Assegnazione risorse**. |
| Gestione risorse | 2125362 | Risolti i problemi con la creazione di un membro del team generico utilizzando un metodo di allocazione basato sulle ore. |
| Ore e spesa | 2113603 | Risolto il problema relativo alla personalizzazione con la rimozione di attributi dalla pagina **Inserimento ore**. Il sistema ora controlla se l'attributo esiste nella pagina prima di accedervi utilizzando uno script. |
| Ore e spesa | 2204377 | I fogli presenze copiati devono essere visualizzati automaticamente quando selezioni **Copia settimana** durante l'inserimento ore. |
| Ore e spesa | 2209059 | Il campo **Stato** può essere modificato per gli inserimenti ore di Dynamics 365 Field Service. |
