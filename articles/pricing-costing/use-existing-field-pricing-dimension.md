---
title: Utilizzare i campi Project Operations come dimensioni di determinazione dei prezzi
description: Questo articolo fornisce informazioni sull'uso dei campi come dimensioni di determinazione dei prezzi in Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: baf2145d4df23893953a099ca3837160fa8ac764
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932807"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>Utilizzare i campi Project Operations come dimensioni di determinazione dei prezzi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

L'entità **Valori effettivi** ha molti campi che possono essere utilizzati come dimensioni di determinazione dei prezzi per la determinazione del prezzo basata sulle risorse. Ad esempio, un campo comune è **Risorsa prenotabile**. Per le società di piccole dimensioni con meno di 20-30 risorse fatturabili, avere tassi di fatturazione e di costo specifici a ogni risorsa può essere un approccio più semplice. Tuttavia, man mano che la forza lavoro fatturabile cresce, i tassi specifici delle risorse potrebbero diventare irrealistici da mantenere. Il costo delle risorse e i tassi di fatturazione iniziano a variare man mano che le risorse vengono promosse, acquisiscono maggiore esperienza o acquisiscono un diverso set di competenze. 

Un altro esempio è la categoria di transazione. I clienti e i responsabili dell'implementazione hanno utilizzato la categoria di transazione per classificare il lavoro e utilizzare il campo per determinare prezzo e costo in base alla categoria di lavoro.


[!INCLUDE[footer-include](../includes/footer-banner.md)]