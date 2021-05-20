---
title: Definire i calendari del progetto
description: Questo argomento fornisce informazioni su come applicare un modello di calendario a un progetto per tenere traccia della pianificazione del progetto.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981305"
---
# <a name="define-project-calendars"></a><span data-ttu-id="c45a1-103">Definire i calendari del progetto</span><span class="sxs-lookup"><span data-stu-id="c45a1-103">Define project calendars</span></span>

<span data-ttu-id="c45a1-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="c45a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c45a1-105">Per creare e gestire un progetto, è necessario applicare un modello di calendario al progetto.</span><span class="sxs-lookup"><span data-stu-id="c45a1-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="c45a1-106">Il modello di calendario definisce i seguenti attributi del progetto:</span><span class="sxs-lookup"><span data-stu-id="c45a1-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="c45a1-107">Orario lavorative, inclusa l'ora di inizio e di fine</span><span class="sxs-lookup"><span data-stu-id="c45a1-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="c45a1-108">Giorni lavorativi</span><span class="sxs-lookup"><span data-stu-id="c45a1-108">Working days</span></span>
- <span data-ttu-id="c45a1-109">Eccezioni di calendario come giorni non lavorativi</span><span class="sxs-lookup"><span data-stu-id="c45a1-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="c45a1-110">Il modello di calendario applicato a un progetto è una copia del modello di calendario definito nelle impostazioni dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c45a1-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="c45a1-111">Se modifichi il modello di calendario, tali modifiche non si propagano alle ore lavorative del progetto.</span><span class="sxs-lookup"><span data-stu-id="c45a1-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="c45a1-112">Per modificare le ore lavorative del progetto, è necessario applicare un nuovo modello.</span><span class="sxs-lookup"><span data-stu-id="c45a1-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="c45a1-113">Per creare un modello di calendario per la tua organizzazione, ci sono due requisiti chiave:</span><span class="sxs-lookup"><span data-stu-id="c45a1-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="c45a1-114">Definisci le ore lavorative desiderate del modello utilizzando una risorsa prenotabile nuova o esistente.</span><span class="sxs-lookup"><span data-stu-id="c45a1-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="c45a1-115">Crea un nuovo modello di calendario e associa il modello alla risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="c45a1-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="c45a1-116">**Definisci le ore lavorative del modello**</span><span class="sxs-lookup"><span data-stu-id="c45a1-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="c45a1-117">Seleziona **Risorse** \> **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="c45a1-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="c45a1-118">Crea una nuova risorsa a cui fare riferimento nel modello di calendario o seleziona una risorsa esistente.</span><span class="sxs-lookup"><span data-stu-id="c45a1-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="c45a1-119">Seleziona la scheda **Ore lavorative** della risorsa e completa le istruzioni in [Impostare le ore lavorative per una risorsa](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) per configurare le regole del calendario.</span><span class="sxs-lookup"><span data-stu-id="c45a1-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="c45a1-120">**Creare un nuovo modello di calendario**</span><span class="sxs-lookup"><span data-stu-id="c45a1-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="c45a1-121">Vai a **Impostazioni** \> **Modello di calendario**.</span><span class="sxs-lookup"><span data-stu-id="c45a1-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="c45a1-122">Seleziona **Nuovo** e inserisci un nome, una descrizione e una risorsa modello.</span><span class="sxs-lookup"><span data-stu-id="c45a1-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="c45a1-123">Quando si fa riferimento a una risorsa in un modello di calendario, una copia del calendario della risorsa viene associata al modello di calendario.</span><span class="sxs-lookup"><span data-stu-id="c45a1-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="c45a1-124">Se le ore lavorative del modello copiato cambiano, tali modifiche non verranno propagate al modello di calendario.</span><span class="sxs-lookup"><span data-stu-id="c45a1-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="c45a1-125">Ora puoi associare il modello di lavoro a un modello di calendario di progetto.</span><span class="sxs-lookup"><span data-stu-id="c45a1-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

