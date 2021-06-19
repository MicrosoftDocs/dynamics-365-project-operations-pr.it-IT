---
title: Utilizzare i campi Project Operations come dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni sull'utilizzo dei campi come dimensioni di determinazione dei prezzi in Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004491"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="03ff3-103">Utilizzare i campi Project Operations come dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="03ff3-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="03ff3-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="03ff3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="03ff3-105">L'entità **Valori effettivi** ha molti campi che possono essere utilizzati come dimensioni di determinazione dei prezzi per la determinazione del prezzo basata sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="03ff3-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="03ff3-106">Ad esempio, un campo comune è **Risorsa prenotabile**.</span><span class="sxs-lookup"><span data-stu-id="03ff3-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="03ff3-107">Per le società di piccole dimensioni con meno di 20-30 risorse fatturabili, avere tassi di fatturazione e di costo specifici a ogni risorsa può essere un approccio più semplice.</span><span class="sxs-lookup"><span data-stu-id="03ff3-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="03ff3-108">Tuttavia, man mano che la forza lavoro fatturabile cresce, i tassi specifici delle risorse potrebbero diventare irrealistici da mantenere.</span><span class="sxs-lookup"><span data-stu-id="03ff3-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="03ff3-109">Il costo delle risorse e i tassi di fatturazione iniziano a variare man mano che le risorse vengono promosse, acquisiscono maggiore esperienza o acquisiscono un diverso set di competenze.</span><span class="sxs-lookup"><span data-stu-id="03ff3-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="03ff3-110">Un altro esempio è la categoria di transazione.</span><span class="sxs-lookup"><span data-stu-id="03ff3-110">Another example is that of transaction category.</span></span> <span data-ttu-id="03ff3-111">I clienti e i responsabili dell'implementazione hanno utilizzato la categoria di transazione per classificare il lavoro e utilizzare il campo per determinare prezzo e costo in base alla categoria di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03ff3-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]