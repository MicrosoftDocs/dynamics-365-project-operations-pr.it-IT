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
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128828"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="7010b-104">Inviare una richiesta di risorsa</span><span class="sxs-lookup"><span data-stu-id="7010b-104">Submit a resource request</span></span>

<span data-ttu-id="7010b-105">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="7010b-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7010b-106">È possibile inviare un requisito di risorsa generato come richiesta di risorse.</span><span class="sxs-lookup"><span data-stu-id="7010b-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="7010b-107">La richiesta viene quindi inviata a un responsabile delle risorse per essere evasa.</span><span class="sxs-lookup"><span data-stu-id="7010b-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="7010b-108">In Dynamics 365 Project Operations, nella pagina **Progetti**, seleziona la scheda **Team** per visualizzare un elenco di risorse prenotabili.</span><span class="sxs-lookup"><span data-stu-id="7010b-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="7010b-109">Seleziona la risorsa generica con un requisito di risorsa nell'elenco e fai clic su **Invia richiesta**.</span><span class="sxs-lookup"><span data-stu-id="7010b-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="7010b-110">Lo stato della richiesta del membro del team generico diventerà **Inviata**.</span><span class="sxs-lookup"><span data-stu-id="7010b-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="7010b-111">Dopo che la richiesta viene soddisfatta, la risorsa generica viene sostituita da una risorsa denominata se il responsabile delle risorse soddisfa la richiesta con la prenotazione di una risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="7010b-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="7010b-112">In caso contrario, se il responsabile delle risorse propone una risorsa denominata, la risorsa generica rimane nel team e lo stato della richiesta diventerà **Revisione necessaria**.</span><span class="sxs-lookup"><span data-stu-id="7010b-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
