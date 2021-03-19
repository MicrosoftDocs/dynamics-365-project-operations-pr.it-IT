---
title: Inviare una richiesta di risorsa
description: È possibile inviare un requisito di risorsa generato come richiesta di risorse. La richiesta viene quindi inviata a un responsabile delle risorse per essere evasa.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279143"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="2b932-104">Inviare una richiesta di risorsa</span><span class="sxs-lookup"><span data-stu-id="2b932-104">Submit a resource request</span></span>

<span data-ttu-id="2b932-105">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="2b932-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2b932-106">È possibile inviare un requisito di risorsa generato come richiesta di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b932-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="2b932-107">La richiesta viene quindi inviata a un responsabile delle risorse per essere evasa.</span><span class="sxs-lookup"><span data-stu-id="2b932-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="2b932-108">In Dynamics 365 Project Operations, nella pagina **Progetti**, seleziona la scheda **Team** per visualizzare un elenco di risorse prenotabili.</span><span class="sxs-lookup"><span data-stu-id="2b932-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="2b932-109">Seleziona la risorsa generica con un requisito di risorsa nell'elenco e fai clic su **Invia richiesta**.</span><span class="sxs-lookup"><span data-stu-id="2b932-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="2b932-110">Lo stato della richiesta del membro del team generico diventerà **Inviata**.</span><span class="sxs-lookup"><span data-stu-id="2b932-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="2b932-111">Dopo che la richiesta viene soddisfatta, la risorsa generica viene sostituita da una risorsa denominata se il responsabile delle risorse soddisfa la richiesta con la prenotazione di una risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="2b932-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="2b932-112">In caso contrario, se il responsabile delle risorse propone una risorsa denominata, la risorsa generica rimane nel team e lo stato della richiesta diventerà **Revisione necessaria**.</span><span class="sxs-lookup"><span data-stu-id="2b932-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]