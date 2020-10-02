---
title: Utilizzare i campi Project Operations come dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni sull'uso dei campi come dimensioni di determinazione dei prezzi in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896421"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>Utilizzare i campi Project Operations come dimensioni di determinazione dei prezzi

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

L'entità **Valori effettivi** ha molti campi che possono essere utilizzati come dimensioni di determinazione dei prezzi per la determinazione del prezzo basata sulle risorse. Ad esempio, un campo comune è **Risorsa prenotabile**. Per le società di piccole dimensioni con meno di 20-30 risorse fatturabili, avere tassi di fatturazione e di costo specifici a ogni risorsa può essere un approccio più semplice. Tuttavia, man mano che la forza lavoro fatturabile cresce, i tassi specifici delle risorse potrebbero diventare irrealistici da mantenere. Il costo delle risorse e i tassi di fatturazione iniziano a variare man mano che le risorse vengono promosse, acquisiscono maggiore esperienza o acquisiscono un diverso set di competenze. 

Un altro esempio è la categoria di transazione. I clienti e i responsabili dell'implementazione hanno utilizzato la categoria di transazione per classificare il lavoro e utilizzare il campo per determinare prezzo e costo in base alla categoria di lavoro.
