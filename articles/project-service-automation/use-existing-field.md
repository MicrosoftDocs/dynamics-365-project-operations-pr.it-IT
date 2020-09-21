---
title: Utilizzare un campo esistente in Project Service come dimensione di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni sull'utilizzo dei campi di Project Service esistenti come dimensioni di determinazione dei prezzi.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: ed86e0c4-b2ea-4b3b-b9e3-cbfb3b512591
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: b280e2aeecc9d63fb65b77fad809edff817aff65
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752652"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="5174f-103">Utilizzare un campo esistente in Project Service come dimensione di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="5174f-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="5174f-104">Project Service Automation (PSA) include molti campi nell'entità **Valori effettivi** che possono essere utilizzati come dimensioni per la determinazione dei prezzi in base alle risorse nelle organizzazioni di progetto.</span><span class="sxs-lookup"><span data-stu-id="5174f-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="5174f-105">Ad esempio, un campo comune è **Risorsa prenotabile**.</span><span class="sxs-lookup"><span data-stu-id="5174f-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="5174f-106">Per le società di piccole dimensioni con meno di 20-30 risorse fatturabili, avere tassi di fatturazione e di costo specifici a ogni risorsa può essere un approccio più semplice.</span><span class="sxs-lookup"><span data-stu-id="5174f-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="5174f-107">Tuttavia, con l'aumento della forza lavoro fatturabile, questo approccio può risultare irrealista in quanto i tassi di costo e fatturazione delle risorse iniziano a variare dal momento in cui le risorse vengono promosse, hanno più esperienza o acquisiscono competenze differenti.</span><span class="sxs-lookup"><span data-stu-id="5174f-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="5174f-108">Poiché questo approccio è sempre appropriato per le aziende di una determinata dimensione, vedi l'argomento, [Utilizzare una risorsa prenotabile come dimensione di determinazione dei prezzi](bookable-resource-pricing-dimension.md) per comprendere come un campo di Project Service esistente può essere utilizzato come dimensione di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="5174f-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="5174f-109">Un altro esempio è la categoria di transazione.</span><span class="sxs-lookup"><span data-stu-id="5174f-109">Another example is that of transaction category.</span></span> <span data-ttu-id="5174f-110">I clienti e i responsabili dell'implementazione hanno utilizzato la categoria di transazione in PSA per classificare il lavoro e utilizzare il campo per determinare prezzo e costo in base alla categoria di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5174f-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="5174f-111">Per ulteriori informazioni, vedi [Utilizzare una categoria di transazione come dimensione di determinazione dei prezzi](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="5174f-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
