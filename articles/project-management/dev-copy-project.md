---
title: Sviluppare i modelli di progetto con Copia progetto
description: Questo argomento fornisce informazioni su come creare modelli di progetto utilizzando l'azione personalizzata Copia progetto.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131618"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="a6f0a-103">Sviluppare i modelli di progetto con Copia progetto</span><span class="sxs-lookup"><span data-stu-id="a6f0a-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="a6f0a-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="a6f0a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a6f0a-105">Dynamics 365 Project Operations supporta la possibilità di copiare un progetto e ripristinare eventuali assegnazioni alle risorse generiche che rappresentano il ruolo.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="a6f0a-106">I clienti possono utilizzare questa funzionalità per creare modelli di progetto di base.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="a6f0a-107">Quando selezioni **Copia progetto**, lo stato del progetto di destinazione viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="a6f0a-108">Usa il **motivo stato** per determinare quando l'azione di copia è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="a6f0a-109">La selezione di **Copia progetto** aggiorna anche la data di inizio del progetto sulla data di inizio corrente se non viene rilevata alcuna data di destinazione nell'entità del progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="a6f0a-110">Azione personalizzata Copia progetto</span><span class="sxs-lookup"><span data-stu-id="a6f0a-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="a6f0a-111">Nome</span><span class="sxs-lookup"><span data-stu-id="a6f0a-111">Name</span></span> 

<span data-ttu-id="a6f0a-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="a6f0a-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="a6f0a-113">Parametri di input</span><span class="sxs-lookup"><span data-stu-id="a6f0a-113">Input parameters</span></span>
<span data-ttu-id="a6f0a-114">Sono presenti tre parametri di input:</span><span class="sxs-lookup"><span data-stu-id="a6f0a-114">There are three input parameters:</span></span>

| <span data-ttu-id="a6f0a-115">Parametro</span><span class="sxs-lookup"><span data-stu-id="a6f0a-115">Parameter</span></span>          | <span data-ttu-id="a6f0a-116">Digita</span><span class="sxs-lookup"><span data-stu-id="a6f0a-116">Type</span></span>   | <span data-ttu-id="a6f0a-117">Valori</span><span class="sxs-lookup"><span data-stu-id="a6f0a-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="a6f0a-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="a6f0a-118">ProjectCopyOption</span></span>  | <span data-ttu-id="a6f0a-119">Stringa</span><span class="sxs-lookup"><span data-stu-id="a6f0a-119">String</span></span> | <span data-ttu-id="a6f0a-120">**{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="a6f0a-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="a6f0a-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="a6f0a-121">SourceProject</span></span>      | <span data-ttu-id="a6f0a-122">Riferimento entità</span><span class="sxs-lookup"><span data-stu-id="a6f0a-122">Entity Reference</span></span> | <span data-ttu-id="a6f0a-123">Progetto di origine</span><span class="sxs-lookup"><span data-stu-id="a6f0a-123">Source Project</span></span> |
| <span data-ttu-id="a6f0a-124">Destinazione</span><span class="sxs-lookup"><span data-stu-id="a6f0a-124">Target</span></span>             | <span data-ttu-id="a6f0a-125">Riferimento entità</span><span class="sxs-lookup"><span data-stu-id="a6f0a-125">Entity Reference</span></span> | <span data-ttu-id="a6f0a-126">Progetto di destinazione</span><span class="sxs-lookup"><span data-stu-id="a6f0a-126">Target Project</span></span> |


- <span data-ttu-id="a6f0a-127">**{"clearTeamsAndAssignments":true}**: il comportamento predefinito di Project per il Web e rimuove tutte le assegnazioni e i membri del team.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="a6f0a-128">**{"removeNamedResources":true}**: il comportamento predefinito di Project Operations e ripristina le assegnazioni a risorse generiche.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="a6f0a-129">Per ulteriori valori predefiniti delle azioni, vedi [Usare le azioni API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="a6f0a-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="a6f0a-130">Specificare i campi da copiare</span><span class="sxs-lookup"><span data-stu-id="a6f0a-130">Specify fields to copy</span></span> 
<span data-ttu-id="a6f0a-131">Quando l'azione viene chiamata, **Copia progetto** guarda la vista del progetto **Copia colonne di progetto** per determinare quali campi copiare quando il progetto viene copiato.</span><span class="sxs-lookup"><span data-stu-id="a6f0a-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
