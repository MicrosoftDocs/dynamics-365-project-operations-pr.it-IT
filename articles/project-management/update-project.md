---
title: Aggiornare un progetto
description: Questo argomento fornisce informazioni sull'aggiornamento di progetti in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078731"
---
# <a name="update-a-project"></a><span data-ttu-id="4cd3a-103">Aggiornare un progetto</span><span class="sxs-lookup"><span data-stu-id="4cd3a-103">Update a project</span></span>

<span data-ttu-id="4cd3a-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="4cd3a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4cd3a-105">Di seguito è riportato un riepilogo dei campi che possono essere aggiornati in un progetto dopo che è stato creato e le implicazioni applicabili degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="4cd3a-106">Campi dei dettagli di progetto</span><span class="sxs-lookup"><span data-stu-id="4cd3a-106">Project detail fields</span></span>

- <span data-ttu-id="4cd3a-107">**Nome** : il titolo del progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="4cd3a-108">**Descrizione** : una panoramica del progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="4cd3a-109">**Cliente** : l'azienda a cui verrà consegnato il progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="4cd3a-110">**Modello calendario** : le ore lavorative del progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="4cd3a-111">Quando il campo viene modificato, l'intera pianificazione viene ricalcolata.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="4cd3a-112">**Valuta** : la valuta per il progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="4cd3a-113">Il valore predefinito di questo campo si basa sulla valuta definita nell'unità contratto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="4cd3a-114">Quando l'unità contratto viene aggiornata, viene aggiornato anche il campo.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="4cd3a-115">**Unità contratto** : l'unità organizzativa che rappresenta la divisione o gruppo dell'azienda che è il responsabile principale dell'acquisizione della vendita e della gestione della fornitura del lavoro e dei servizi al cliente.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="4cd3a-116">**Responsabile di progetto** : il membro del team di progetto che ha l'autorità di rivedere e approvare gli inserimenti ore e le spese.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="4cd3a-117">Campi di stima</span><span class="sxs-lookup"><span data-stu-id="4cd3a-117">Estimate fields</span></span>

- <span data-ttu-id="4cd3a-118">**Data di inizio stimata** : la data in cui inizierà il progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="4cd3a-119">Quando questo campo viene aggiornato, tutte le attività del progetto si sposteranno proporzionalmente con la nuova data di inizio.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="4cd3a-120">**Data di fine** : la data in cui è prevista la fine del progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="4cd3a-121">**Lavoro richiesto** : il lavoro richiesto stimato del progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="4cd3a-122">Quando le attività vengono aggiunte al progetto, questo campo non è più modificabile.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="4cd3a-123">**Costo della manodopera stimato** : il costo stimato della manodopera del progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="4cd3a-124">Quando i costi di manodopera vengono aggiunti al progetto, questo campo non è più modificabile.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="4cd3a-125">**Spese stimate** : le spese stimate del progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="4cd3a-126">Quando le spese vengono aggiunte al progetto, questo campo non è più modificabile.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="4cd3a-127">Campi effettivi del progetto</span><span class="sxs-lookup"><span data-stu-id="4cd3a-127">Project actual fields</span></span>
- <span data-ttu-id="4cd3a-128">**Inizio effettivo** : la data di inizio del progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="4cd3a-129">**Fine effettiva** : da aggiornare quando un progetto è stato completato.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="4cd3a-130">Campi relativi allo stato del progetto</span><span class="sxs-lookup"><span data-stu-id="4cd3a-130">Project status fields</span></span>

- <span data-ttu-id="4cd3a-131">**Stato di progetto generale** : lo stato complessivo del progetto fornito dal responsabile di progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="4cd3a-132">**Commenti** : una descrizione dello stato attuale del progetto fornita dal responsabile di progetto.</span><span class="sxs-lookup"><span data-stu-id="4cd3a-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

