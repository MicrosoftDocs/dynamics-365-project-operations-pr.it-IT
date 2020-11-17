---
title: Utilizzare i campi Project Operations come dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni sull'uso dei campi come dimensioni di determinazione dei prezzi in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119243"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="6c2ed-103">Utilizzare i campi Project Operations come dimensioni di determinazione dei prezzi</span><span class="sxs-lookup"><span data-stu-id="6c2ed-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="6c2ed-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="6c2ed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6c2ed-105">L'entità **Valori effettivi** ha molti campi che possono essere utilizzati come dimensioni di determinazione dei prezzi per la determinazione del prezzo basata sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="6c2ed-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="6c2ed-106">Ad esempio, un campo comune è **Risorsa prenotabile**.</span><span class="sxs-lookup"><span data-stu-id="6c2ed-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="6c2ed-107">Per le società di piccole dimensioni con meno di 20-30 risorse fatturabili, avere tassi di fatturazione e di costo specifici a ogni risorsa può essere un approccio più semplice.</span><span class="sxs-lookup"><span data-stu-id="6c2ed-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="6c2ed-108">Tuttavia, man mano che la forza lavoro fatturabile cresce, i tassi specifici delle risorse potrebbero diventare irrealistici da mantenere.</span><span class="sxs-lookup"><span data-stu-id="6c2ed-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="6c2ed-109">Il costo delle risorse e i tassi di fatturazione iniziano a variare man mano che le risorse vengono promosse, acquisiscono maggiore esperienza o acquisiscono un diverso set di competenze.</span><span class="sxs-lookup"><span data-stu-id="6c2ed-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="6c2ed-110">Un altro esempio è la categoria di transazione.</span><span class="sxs-lookup"><span data-stu-id="6c2ed-110">Another example is that of transaction category.</span></span> <span data-ttu-id="6c2ed-111">I clienti e i responsabili dell'implementazione hanno utilizzato la categoria di transazione per classificare il lavoro e utilizzare il campo per determinare prezzo e costo in base alla categoria di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6c2ed-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
