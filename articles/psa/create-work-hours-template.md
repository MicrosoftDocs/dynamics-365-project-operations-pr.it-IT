---
title: Creare un modello di ore lavorative
description: Questo argomento descrive come creare un modello delle ore lavorative in Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981260"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="117eb-103">Creare un modello delle ore lavorative (Project Service)</span><span class="sxs-lookup"><span data-stu-id="117eb-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="117eb-104">Per creare e gestire un progetto, è necessario applicare un modello di calendario al progetto.</span><span class="sxs-lookup"><span data-stu-id="117eb-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="117eb-105">Il modello di calendario definisce i seguenti attributi del progetto:</span><span class="sxs-lookup"><span data-stu-id="117eb-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="117eb-106">Orario lavorative, inclusa l'ora di inizio e di fine</span><span class="sxs-lookup"><span data-stu-id="117eb-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="117eb-107">Giorni lavorativi</span><span class="sxs-lookup"><span data-stu-id="117eb-107">Working days</span></span>
- <span data-ttu-id="117eb-108">Eccezioni di calendario come giorni non lavorativi</span><span class="sxs-lookup"><span data-stu-id="117eb-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="117eb-109">Il modello di calendario applicato a un progetto è una copia del modello di calendario definito nelle impostazioni dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="117eb-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="117eb-110">Se modifichi il modello di calendario, tali modifiche non si propagano alle ore lavorative del progetto.</span><span class="sxs-lookup"><span data-stu-id="117eb-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="117eb-111">Per modificare le ore lavorative del progetto, è necessario applicare un nuovo modello.</span><span class="sxs-lookup"><span data-stu-id="117eb-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="117eb-112">Per creare un modello di calendario per la tua organizzazione, ci sono due requisiti chiave:</span><span class="sxs-lookup"><span data-stu-id="117eb-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="117eb-113">Definisci le ore lavorative desiderate del modello utilizzando una risorsa prenotabile nuova o esistente.</span><span class="sxs-lookup"><span data-stu-id="117eb-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="117eb-114">Crea un nuovo modello di calendario e associa il modello alla risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="117eb-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="117eb-115">**Definisci le ore lavorative del modello**</span><span class="sxs-lookup"><span data-stu-id="117eb-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="117eb-116">Seleziona **Risorse** \> **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="117eb-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="117eb-117">Crea una nuova risorsa a cui fare riferimento nel modello di calendario o seleziona una risorsa esistente.</span><span class="sxs-lookup"><span data-stu-id="117eb-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="117eb-118">Seleziona la scheda **Ore lavorative** della risorsa e completa le istruzioni in [Impostare le ore lavorative per una risorsa](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) per configurare le regole del calendario.</span><span class="sxs-lookup"><span data-stu-id="117eb-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="117eb-119">**Creare un nuovo modello di calendario**</span><span class="sxs-lookup"><span data-stu-id="117eb-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="117eb-120">Vai a **Impostazioni** \> **Modello di calendario**.</span><span class="sxs-lookup"><span data-stu-id="117eb-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="117eb-121">Seleziona **Nuovo** e inserisci un nome, una descrizione e una risorsa modello.</span><span class="sxs-lookup"><span data-stu-id="117eb-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="117eb-122">Quando si fa riferimento a una risorsa in un modello di calendario, una copia del calendario della risorsa viene associata al modello di calendario.</span><span class="sxs-lookup"><span data-stu-id="117eb-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="117eb-123">Se le ore lavorative del modello copiato cambiano, tali modifiche non verranno propagate al modello di calendario.</span><span class="sxs-lookup"><span data-stu-id="117eb-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="117eb-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="117eb-124">See Also</span></span>  
 [<span data-ttu-id="117eb-125">Configurare le risorse</span><span class="sxs-lookup"><span data-stu-id="117eb-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
