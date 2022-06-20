---
title: Integrazione di doppia scrittura di Project Operations
description: Questo articolo fornisce una panoramica dell'integrazione della doppia scrittura di Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927977"
---
# <a name="project-operations-dual-write-integration-overview"></a>Panoramica dell'integrazione di doppia scrittura di Project Operations

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Usa le [capacità di doppia scrittura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) di Project Operations per sincronizzare i dati tra Microsoft Dataverse e Dynamics 365 Finance.

La seguente illustrazione mostra come i dati vengono sincronizzati come parte di questa integrazione tra Dataverse e Finance.

![Panoramica dei flussi di dati di Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations in Dataverse fornisce una moderna interfaccia utente (UI) e una facile estensibilità senza codice/uso limitato di codice utilizzando le capacità Power Platform. I responsabili di progetto, i responsabili delle risorse, i membri del team di progetto e altri personaggi del front-office svolgono le loro attività in Project Operations su Dataverse.

Project Operations in Finance fornisce supporto per la contabilità del progetto e il riconoscimento dei ricavi. Project Operations si collega alla struttura finanziaria in Finance per il calcolo dell'IVA, i tassi di cambio valutari, i report sulle dimensioni finanziarie e altro ancora. Le esperienze dei contabili di progetto si svolgono principalmente in Finance.

L'integrazione di Project Operations consiste nella seguente integrazione di componenti:


- [Configurazione di Project Operations e integrazione dei dati di configurazione](resource-dual-write-setup-integration.md) 
- [Stime e valori effettivi di progetto](resource-dual-write-estimates-actuals.md)
- [Fatture di progetto](resource-dual-write-project-invoice.md)
- [Gestione spese](resource-dual-write-expense.md)
- [Fattura fornitore](resource-dual-write-vendor-invoice.md)
