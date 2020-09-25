---
title: Sincronizzare le attività di progetto direttamente da Project Service Automation a Finance and Operations
description: Questo argomento descrive il modello e l'attività sottostante utilizzati per sincronizzare le attività del progetto direttamente da Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752710"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizzare le attività di progetto direttamente da Project Service Automation a Finance and Operations

[!include[banner](../includes/banner.md)]

Questo argomento descrive il modello e l'attività sottostante utilizzati per sincronizzare le attività del progetto direttamente da Dynamics 365 Project Service Automation a Dynamics 365 Finance.

> [!NOTE]
> - L'integrazione delle attività di progetto, le categorie delle transazioni di spesa, le stime delle ore, le stime delle spese e il blocco delle funzionalità sono disponibili nella versione 8.0.
> - Se stai utilizzando Enterprise Edition 7.3.0 dopo aver installato KB 4132657 e KB 4132660, potrai utilizzare i modelli per integrare attività di progetto, categorie di transazioni di spesa, stime di ore, stime di spesa e valori effettivi e per configurare il blocco delle funzionalità. Se devi reimpostare le distribuzioni contabili, è consigliabile installare anche KB 4131710.
> - L'integrazione dei dati effettivi è disponibile nella versione 8.0.1 o successiva.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flusso di dati per Project Service Automation su Finance

La soluzione di integrazione da Project Service Automation a Finance utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra le istanze di Project Service Automation e Finance. Il modello di integrazione disponibile con la funzionalità Integrazione dati consente il flusso di dati sulle attività del progetto da Project Service Automation a Finance.

La figura seguente mostra come i dati vengono sincronizzati tra Project Service Automation e Finance.

[![Flusso di dati per l'integrazione di Project Service Automation con Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Modello e attività

Per accedere al modello, nell'interfaccia di amministrazione di Microsoft Power Apps, seleziona **Progetti**, quindi, nell'angolo in alto a destra, seleziona **Nuovo progetto** per selezionare modelli pubblici.

Il modello seguente e l'attività sottostante vengono utilizzati per sincronizzare le attività di progetto da Project Service Automation a Finance:

- **Nome del modello in Integrazione dati:** attività di progetto (da PSA a Fin e Ops)
- **Nome dell'attività nel progetto:** attività di progetto

Prima di sincronizzare le attività di progetto , è necessario sincronizzare i contratti di progetto e i progetti.

## <a name="entity-set"></a>Set di entità

| Project Service Automation | Finanza                             |
|----------------------------|-------------------------------------|
| Attività di progetto              | Entità di integrazione per attività di progetto |

## <a name="entity-flow"></a>Flusso di entità

Le attività di progetto vengono gestiti in Project Service Automation e vengono sincronizzate con Finance come impegni di progetto.

## <a name="prerequisites-and-mapping-setup"></a>Configurazione di prerequisiti e mapping

Prima di sincronizzare le attività di progetto , è necessario sincronizzare i contratti di progetto e i progetti.

## <a name="power-query"></a>Power Query

Devi utilizzare Microsoft Power Query per Excel per filtrare i dati se viene soddisfatta la seguente condizione:

- Hai record specifici della risorsa in un'attività di progetto.

Se devi utilizzare Power Query, segui queste linee guida:

- Il modello Attività di progetto (da PSA a Fin e Ops) ha un filtro predefinito che esclude i record specifici della risorsa da un'attività di progetto impostando il filtro di **IsLineTask** su **Falso**. Se crei il tuo modello, devi aggiungere questo filtro.

## <a name="template-mapping-in-data-integration"></a>Mapping dei modelli nell'integrazione dei dati

La figura seguente mostra un esempio dei mapping delle attività del modello in Integrazione dati. Il mapping mostra le informazioni sui campi che verranno sincronizzate da Project Service Automation a Finance.

[![Mapping dei modelli](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)