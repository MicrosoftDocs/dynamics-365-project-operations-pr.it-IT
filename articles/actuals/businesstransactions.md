---
title: Transazioni commerciali in Project Operations
description: Questo argomento fornisce una panoramica del concetto di transazioni commerciali in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582209"
---
# <a name="business-transactions-in-project-operations"></a>Transazioni commerciali in Project Operations

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Microsoft Dynamics 365 Project Operations, *transazione commerciale* è un concetto astratto che non è rappresentato da alcuna entità. Tuttavia, alcuni campi e processi comuni delle entità sono progettati per utilizzare il concetto di transazioni commerciali. Le seguenti entità utilizzano questo concetto:

- Dettagli riga di offerta
- Dettagli voce di contratto
- Righe di stima
- Righe giornale di registrazione
- Valori effettivi

Tra queste entità, Dettagli riga di offerta, Dettagli voce di contratto e Righe di stima sono mappate alla *fase di stima* nel ciclo di vita del progetto. Le entità Righe giornale di registrazione e Valori effettivi sono mappate alla *fase di esecuzione* nel ciclo di vita del progetto.

Project Operations tratta i record in queste cinque entità come transazioni commerciali. La sola distinzione è che i record nelle entità mappate alla fase di stima (Dettagli riga di offerta, Dettagli voce di contratto e Righe di stima) sono considerati *previsioni finanziarie*, mentre i record nelle entità mappate alla fase di esecuzione (Righe giornale di registrazione e Valori effettivi)sono considerati come *fatti finanziari* già accaduti.

Per ulteriori informazioni, vedi [Stime](../project-management/estimating-projects-overview.md) e [Valori effettivi](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Concetti specifici delle transazioni commerciali

I seguenti concetti sono specifici del concetto di transazioni commerciali:

- Tipo di transazione
- Classe di transazione
- Origine transazione
- Connessione della transazione

### <a name="transaction-type"></a>Tipo di transazione

Il tipo di transazione rappresenta il timing e il contesto dell'impatto finanziario su un progetto. È definito da un set di opzioni che ha i seguenti valori supportati in Project Operations:

- Costo
- Contratto di progetto
- Vendite non fatturate
- Vendite fatturate
- Vendite interorganizzative
- Costo unità gestione risorse

### <a name="transaction-class"></a>Classe di transazione

La classe di transazione rappresenta i differenti tipi di costi sostenuti nei progetti. È definito da un set di opzioni che ha i seguenti valori supportati in Project Operations:

- Inserimento ore
- Spesa
- Materiale
- Quota
- Passaggio fondamentale
- Imposta

> [!NOTE]
> Il valore **Passaggio fondamentale** viene in genere utilizzato dalla logica di business per la fatturazione a prezzo fisso in Project Operations.

### <a name="transaction-origin"></a>Origine transazione

L'origine della transazione è un'entità che memorizza l'origine di ogni transazione commerciale per facilitare la segnalazione e la tracciabilità. All'inizio dell'esecuzione del progetto, ogni transazione commerciale crea un'altra transazione commerciale che, a sua volta, creerà un'altra transazione commerciale e così via.

### <a name="transaction-connection"></a>Connessione della transazione

Connessione della transazione è un'entità che archivia la relazione tra due transazioni commerciali simili, ad esempio il costo e i valori effettivi di vendita correlati, oppure storni di transazioni attivati dalle attività di fatturazione come la conferma o le correzioni delle fatture.

Con l'utilizzo combinato delle entità Origine transazione e Connessione della transazione puoi tenere traccia delle relazioni tra transazioni commerciali e azioni che provocano la creazione di una specifica transazione commerciale.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
