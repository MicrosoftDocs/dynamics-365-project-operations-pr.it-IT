---
title: Inviare una richiesta di risorsa
description: È possibile inviare un requisito di risorsa generato come richiesta di risorse. La richiesta viene quindi inviata a un responsabile delle risorse per essere evasa.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014031"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="bb2d6-104">Inviare una richiesta di risorsa</span><span class="sxs-lookup"><span data-stu-id="bb2d6-104">Submit a resource request</span></span>

<span data-ttu-id="bb2d6-105">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="bb2d6-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bb2d6-106">È possibile inviare un requisito di risorsa generato come richiesta di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb2d6-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="bb2d6-107">La richiesta viene quindi inviata a un responsabile delle risorse per essere evasa.</span><span class="sxs-lookup"><span data-stu-id="bb2d6-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="bb2d6-108">In Dynamics 365 Project Operations, nella pagina **Progetti**, seleziona la scheda **Team** per visualizzare un elenco di risorse prenotabili.</span><span class="sxs-lookup"><span data-stu-id="bb2d6-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="bb2d6-109">Seleziona la risorsa generica con un requisito di risorsa nell'elenco e fai clic su **Invia richiesta**.</span><span class="sxs-lookup"><span data-stu-id="bb2d6-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="bb2d6-110">Lo stato della richiesta del membro del team generico diventerà **Inviata**.</span><span class="sxs-lookup"><span data-stu-id="bb2d6-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="bb2d6-111">Dopo che la richiesta viene soddisfatta, la risorsa generica viene sostituita da una risorsa denominata se il responsabile delle risorse soddisfa la richiesta con la prenotazione di una risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="bb2d6-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="bb2d6-112">In caso contrario, se il responsabile delle risorse propone una risorsa denominata, la risorsa generica rimane nel team e lo stato della richiesta diventerà **Revisione necessaria**.</span><span class="sxs-lookup"><span data-stu-id="bb2d6-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]