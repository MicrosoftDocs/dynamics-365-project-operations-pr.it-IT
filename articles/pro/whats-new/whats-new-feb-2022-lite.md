---
title: Novità di febbraio 2022 - Distribuzione semplice di Project Operations
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di febbraio 2022 della distribuzione lite di Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922825"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Novità di febbraio 2022 - Distribuzione semplice di Project Operations

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.28.0.120

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

A partire da questa versione, puoi aggiungere fino a 300 membri del team a un singolo progetto. In precedenza, il limite al numero di membri del team era 150. Per altre informazioni, consulta l'articolo sui [limiti del progetto](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Aggiornamenti di qualità

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Determinazione dei prezzi e fatturazione | 2497369 | La correzione del materiale deve seguire il valore della data nei parametri **Correzione**. |
| Determinazione dei prezzi e fatturazione | 2498697 | Migliorata la configurazione di sicurezza per **Richiamo inserimento ore**. |
| Determinazione dei prezzi e fatturazione | 2517455 | L'azione **Transazioni riga di fattura aggiornate** non deve essere attivata più volte contemporaneamente per la stessa fattura. |
| Determinazione dei prezzi e fatturazione | 2517465 | L'azione **Disattiva dettagli riga di fattura** è bloccata perché non è supportata. |
| Determinazione dei prezzi e fatturazione | 2556660 | Risolto il problema con i controlli di validità della data che vengono eseguiti sul listino prezzi collegato a un record di parametri di progetto. |
| Gestione delle opportunità | 2369202 | Corretta la logica di business che verifica che i listini prezzi con date di validità sovrapposte possano essere collegati allo stesso contratto di progetto. |
| Gestione delle opportunità | 2385965 | Corretto il comportamento sulla scheda **Clienti** della pagina **Contratto di progetto** quando si seleziona **Salva e chiudi**. |
