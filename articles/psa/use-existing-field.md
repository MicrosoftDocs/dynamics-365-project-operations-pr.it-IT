---
title: Utilizzare un campo esistente in Project Service come dimensione di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni sull'utilizzo dei campi di Project Service esistenti come dimensioni di determinazione dei prezzi.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008091"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Utilizzare un campo esistente in Project Service come dimensione di determinazione dei prezzi

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) include molti campi nell'entità **Valori effettivi** che possono essere utilizzati come dimensioni per la determinazione dei prezzi in base alle risorse nelle organizzazioni di progetto. Ad esempio, un campo comune è **Risorsa prenotabile**. Per le società di piccole dimensioni con meno di 20-30 risorse fatturabili, avere tassi di fatturazione e di costo specifici a ogni risorsa può essere un approccio più semplice. Tuttavia, con l'aumento della forza lavoro fatturabile, tassi specific possono risultare irrealisti in quanto i tassi di costo e fatturazione delle risorse iniziano a variare dal momento in cui le risorse vengono promosse, hanno più esperienza o acquisiscono competenze differenti. Poiché questo approccio è sempre appropriato per le aziende di una determinata dimensione, vedi [Utilizzare una risorsa prenotabile come dimensione di determinazione dei prezzi](bookable-resource-pricing-dimension.md) per comprendere come un campo di Project Service esistente può essere utilizzato come dimensione di determinazione dei prezzi.

Un altro esempio è la categoria di transazione. I clienti e i responsabili dell'implementazione hanno utilizzato la categoria di transazione in PSA per classificare il lavoro e utilizzare il campo per determinare prezzo e costo in base alla categoria di lavoro. Per ulteriori informazioni, vedi [Utilizzare una categoria di transazione come dimensione di determinazione dei prezzi](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]