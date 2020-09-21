---
title: Inviare una richiesta di risorse
description: In questo argomento vengono fornite informazioni sull'invio di una richiesta per una risorsa di progetto.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752691"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="7bfd2-103">Inviare una richiesta di risorse</span><span class="sxs-lookup"><span data-stu-id="7bfd2-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7bfd2-104">È possibile inviare un requisito di risorsa generato come richiesta di risorse.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="7bfd2-105">La richiesta viene quindi inviata a un responsabile delle risorse per essere evasa.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="7bfd2-106">In Project Service Automation (PSA), nella pagina **Progetti**, fare clic sulla scheda **Team** per visualizzare un elenco di risorse prenotabili.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="7bfd2-107">Selezionare la risorsa generica con un requisito di risorsa nell'elenco e fare clic su **Invia richiesta**.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Inviare una richiesta di risorse](media/RM-how-to-18.png)

<span data-ttu-id="7bfd2-109">Lo stato della richiesta del membro del team generico diventerà **Inviata**.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="7bfd2-110">Dopo che la richiesta viene soddisfatta dal responsabile delle risorse, la risorsa generica verrà sostituita da una risorsa denominata se il responsabile delle risorse soddisfa la richiesta con la prenotazione di una risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="7bfd2-111">In caso contrario, la risorsa generica rimarrà nel team e lo stato della richiesta diventerà **Revisione necessaria**, se il responsabile delle risorse ha proposto una risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="7bfd2-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
