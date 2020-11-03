---
title: Definire le competenze e i livelli di preparazione
description: In questo argomento vengono fornite informazioni su come configurare i modelli del livello di preparazione per valutare le risorse.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078820"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="931b1-103">Definire le competenze e i livelli di preparazione</span><span class="sxs-lookup"><span data-stu-id="931b1-103">Define skills and proficiencies</span></span>

<span data-ttu-id="931b1-104">_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="931b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="931b1-105">Le competenze sono caratteristiche delle risorse condivise tra Dynamics 365 Project Operations e se presente Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="931b1-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="931b1-106">Per gestire l'archivio delle competenze in Project Operations, seleziona **Risorse** \> **Competenze risorse**.</span><span class="sxs-lookup"><span data-stu-id="931b1-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="931b1-107">Utilizzare modelli del livello di preparazione per valutare le risorse</span><span class="sxs-lookup"><span data-stu-id="931b1-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="931b1-108">Le competenze delle risorse vengono valutate mediante modelli del livello di preparazione.</span><span class="sxs-lookup"><span data-stu-id="931b1-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="931b1-109">Le singole valutazioni sono incluse in un modello del livello di preparazione.</span><span class="sxs-lookup"><span data-stu-id="931b1-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="931b1-110">Per creare un modello del livello di preparazione, seleziona **Risorse** \> **Modelli di livello di preparazione** e quindi **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="931b1-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="931b1-111">Nel nuovo modello di valutazione, specificare il valore di valutazione minimo, quello massimo e l'entità che viene valutata.</span><span class="sxs-lookup"><span data-stu-id="931b1-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="931b1-112">Nella griglia secondaria **Valori di valutazione** , puoi definire diversi valori di valutazione, da quello minimo a quello massimo.</span><span class="sxs-lookup"><span data-stu-id="931b1-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="931b1-113">Questi valori di valutazione sono visualizzati nei filtri **Requisiti di risorse** , **Scheda di pianificazione** e **Assistente di pianificazione**.</span><span class="sxs-lookup"><span data-stu-id="931b1-113">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
