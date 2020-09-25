---
title: Panoramica di Project Service Automation
description: Questo argomento fornisce informazioni sulla soluzione di integrazione tra Dynamics 365 Project Service Automation e Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752668"
---
# <a name="project-service-automation-overview"></a>Panoramica di Project Service Automation

[!include[banner](../includes/banner.md)]

La soluzione di integrazione da Project Service Automation a Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Dynamics 365 Finance e Dynamics 365 Project Service Automation tramite Common Data Service. I modelli di integrazione disponibili con la funzionalità Integrazione dati consentono il flusso di progetti, contratti di progetto, voci di contratto di progetto, fasi delle voci di contratto di progetto, attività di progetto, categorie di transazione di spesa, stime delle ore e stime delle spese da Project Service Automation a Finance.

> [!NOTE]
> - Se utilizzi la versione 7.3.0, devi installare KB 4074835. Potrai quindi integrare progetti a prezzo fisso.
> - Se stai utilizzando la versione 7.3.0 e stai trasferendo le transazioni delle commissioni da Project Service Automation, devi installare KB 4345320 per includere tali commissioni nella fattura del progetto.
> - Se stai utilizzando la versione 8.0, sarai in grado di utilizzare l'integrazione delle attività di progetto, le categorie delle transazioni di spesa, le stime delle ore, le stime delle spese e il blocco delle funzionalità.
> - Se stai utilizzando la versione 8.0.1 o successiva, sarai in grado di sincronizzare i valori effettivi.

Prima di poter integrare Project Service Automation Finance, è necessario configurare i parametri di integrazione di Project Service Automation. Per altre informazioni, vedi [Parametri di integrazione di Project Service Automation](PSA-parameters.md).

Questa soluzione di integrazione consente la sincronizzazione diretta nei seguenti scenari:

- Gestisci i contratti di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.
- Crea progetti in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.
- Gestisci le voci dei contratti di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.
- Gestisci le fasi delle voci dei contratti di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.
- Gestisci le attività di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.
- Gestisci le categorie delle transazioni di spesa in Finance e sincronizzale direttamente da Finance a Project Service Automation.
- Crea le stime delle ore di progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.
- Crea le stime di spesa del progetto in Project Service Automation e sincronizzali direttamente da Project Service Automation a Finance.
- Creare i tempi, le spese e le commissioni effettive del progetto in Project Service Automation e crea transazioni di progetto nel giornale di registrazione dell'integrazione di Project Service Automation in modo che possano essere registrate in Finance.

## <a name="data-synchronization"></a>Sincronizzazione dati

La figura seguente mostra come i dati vengono sincronizzati come parte dell'integrazione tra Project Service Automation e Finance.

> [!NOTE]
> Non tutti i modelli sono attualmente disponibili. I modelli verranno rilasciati non appena saranno completati.

[![Integrazione di Project Service Automation con Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Requisiti di sistema per Finance

Per utilizzare la soluzione di integrazione da Project Service Automation a Finance, è necessario installare Enterprise Edition 7.3 con Platform update 12 o successiva.

## <a name="system-requirements-for-project-service-automation"></a>Requisiti di sistema per Project Service Automation

Per utilizzare la soluzione di integrazione da Project Service Automation a Finance, è necessario installare i seguenti componenti:

- Dynamics 365 Project Service Automation 9.0.0.0 o versione successiva
- Soluzione da prospect a cassa per Dynamics 365 Sales, versione 1.14.0.0 (v14) o successiva
- Soluzione da Project Service Automation a Finance per Dynamics 365 Project Service Automation versione 1.0.0.0 o successiva

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installa la soluzione di integrazione da Project Service Automation a Finance nell'istanza di Project Service Automation

Scarica la soluzione di integrazione da Project Service Automation a Finance dal [Centro download Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) e segui le istruzioni incluse con la soluzione.