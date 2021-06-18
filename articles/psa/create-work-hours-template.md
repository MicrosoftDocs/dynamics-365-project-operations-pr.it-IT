---
title: Creare un modello di ore lavorative
description: Questo argomento descrive come creare un modello delle ore lavorative in Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997201"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="fdcc8-103">Creare un modello delle ore lavorative (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fdcc8-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fdcc8-104">Per creare e gestire un progetto, è necessario applicare un modello di calendario al progetto.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="fdcc8-105">Il modello di calendario definisce i seguenti attributi del progetto:</span><span class="sxs-lookup"><span data-stu-id="fdcc8-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="fdcc8-106">Orario lavorative, inclusa l'ora di inizio e di fine</span><span class="sxs-lookup"><span data-stu-id="fdcc8-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="fdcc8-107">Giorni lavorativi</span><span class="sxs-lookup"><span data-stu-id="fdcc8-107">Working days</span></span>
- <span data-ttu-id="fdcc8-108">Eccezioni di calendario come giorni non lavorativi</span><span class="sxs-lookup"><span data-stu-id="fdcc8-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="fdcc8-109">Il modello di calendario applicato a un progetto è una copia del modello di calendario definito nelle impostazioni dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="fdcc8-110">Se modifichi il modello di calendario, tali modifiche non si propagano alle ore lavorative del progetto.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="fdcc8-111">Per modificare le ore lavorative del progetto, è necessario applicare un nuovo modello.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="fdcc8-112">Per creare un modello di calendario per la tua organizzazione, ci sono due requisiti chiave:</span><span class="sxs-lookup"><span data-stu-id="fdcc8-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="fdcc8-113">Definisci le ore lavorative desiderate del modello utilizzando una risorsa prenotabile nuova o esistente.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="fdcc8-114">Crea un nuovo modello di calendario e associa il modello alla risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="fdcc8-115">**Definisci le ore lavorative del modello**</span><span class="sxs-lookup"><span data-stu-id="fdcc8-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="fdcc8-116">Seleziona **Risorse** \> **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="fdcc8-117">Crea una nuova risorsa a cui fare riferimento nel modello di calendario o seleziona una risorsa esistente.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="fdcc8-118">Seleziona la scheda **Ore lavorative** della risorsa e completa le istruzioni in [Impostare le ore lavorative per una risorsa](/dynamics365/field-service/set-work-hours-resource.md) per configurare le regole del calendario.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="fdcc8-119">**Creare un nuovo modello di calendario**</span><span class="sxs-lookup"><span data-stu-id="fdcc8-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="fdcc8-120">Vai a **Impostazioni** \> **Modello di calendario**.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="fdcc8-121">Seleziona **Nuovo** e inserisci un nome, una descrizione e una risorsa modello.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="fdcc8-122">Quando si fa riferimento a una risorsa in un modello di calendario, una copia del calendario della risorsa viene associata al modello di calendario.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="fdcc8-123">Se le ore lavorative del modello copiato cambiano, tali modifiche non verranno propagate al modello di calendario.</span><span class="sxs-lookup"><span data-stu-id="fdcc8-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="fdcc8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdcc8-124">See Also</span></span>  
 [<span data-ttu-id="fdcc8-125">Configurare le risorse</span><span class="sxs-lookup"><span data-stu-id="fdcc8-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
