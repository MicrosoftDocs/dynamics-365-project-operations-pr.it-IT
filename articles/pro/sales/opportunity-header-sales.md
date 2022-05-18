---
title: Impostazioni delle opportunità - semplice
description: Questo argomento fornisce informazioni su transazioni basate su progetto e righe di opportunità basate su progetto.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f40154fed5790083e3a4d3264cc9f8cc23ae18bc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596837"
---
# <a name="header-details-for-project-opportunities"></a>Dettagli dell'intestazione per opportunità di progetto

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

L'intestazione Opportunità acquisisce le informazioni generali su una transazione basata su progetto che si applica a tutte le righe dell'opportunità basata su progetto.

Le opportunità basate su progetto in Dynamics 365 Project Operations sono estensioni di opportunità in Dynamics 365 Sales. Queste estensioni forniscono funzionalità aggiuntive specifiche e richieste per le opportunità basate sul progetto. Queste estensioni possono includere nuovi campi e azioni della barra multifunzione disponibili nelle opportunità basate sul progetto. Alcuni campi, funzionalità e logica di impostazione predefinita disponibili in Sales potrebbero non essere disponibili in Project Operations.

La tabella seguente include i campi in un'opportunità basata su progetto che sono univoci per Project Operations o presentano alcune importanti modifiche nel comportamento rispetto alle opportunità in Sales.

| **Campo** | **Luogo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- | --- |
| Digita | Scheda Generale (nascosta) | Questo campo di set di opzioni include le seguenti opzioni:</br>- Basato su lavoro (disponibile solo con Project Operations)</br>- Basato su articolo (disponibile solo quando sono installati Project Operations e Sales)</br>- Basato su manutenzione di servizio (disponibile quando è installato Field Service) | Quando si utilizza Project Operations, questo valore di campo viene impostato automaticamente su **Basato su lavoro** che classifica l'opportunità come basata su progetto. Un'opportunità deve essere basata su progetto per abilitare tutte le estensioni e funzionalità specifiche del progetto nel processo di vendita downstream per questa transazione. |
| Contatto | Scheda Generale | Riferimento al contatto primario del cliente per questa transazione. | |
| Conto | Scheda Generale | Riferimento alla società o al record di account del cliente. | |
| Gestione account | Scheda Generale | Il nome del responsabile della gestione account per questa opportunità basata sul progetto. | Il responsabile della gestione account è responsabile della gestione del rapporto con il cliente fino al completamento di questo progetto. In base al record della risorsa prenotabile collegato al responsabile della gestione account, l'unità contratto è predefinita. |
| Unità contratto | Scheda Generale | L'unità organizzativa responsabile della consegna del progetto o dei progetti associati a questa transazione. | L'unità contratto è la divisione dell'azienda che completerà i progetti dopo la chiusura della trattativa. Ogni unità contratto ha una valuta e questa valuta viene utilizzata per riportare i costi stimati ed effettivi sostenuti durante il progetto. |

Per tutti gli altri campi e sezioni della scheda **Riepilogo** dell'opportunità, vedi [Creare o modificare opportunità (Vendite e Hub delle vendite)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
