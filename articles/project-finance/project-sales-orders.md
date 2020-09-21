---
title: Ordini di vendita di progetto per progetti relativi a tempi e materiali
description: Questo argomento spiega come creare ordini di vendita basati su progetto per progetti relativi a tempi e materiali.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752600"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="3a23b-103">Ordini di vendita di progetto per progetti relativi a tempi e materiali</span><span class="sxs-lookup"><span data-stu-id="3a23b-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="3a23b-104">Questo argomento descrive come creare un ordine di vendita per un progetto.</span><span class="sxs-lookup"><span data-stu-id="3a23b-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="3a23b-105">Gli ordini di vendita possono essere creati solo per progetti di tipo **tempo e materiale**.</span><span class="sxs-lookup"><span data-stu-id="3a23b-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="3a23b-106">Se un progetto relativo a tempi e materiali ha più fonti di finanziamento nel contratto di progetto, devi abilitare il parametro **Consenti ordini di vendita per progetti con più fonti di finanziamento** nella pagina **Gestione progetti e contabilità**.</span><span class="sxs-lookup"><span data-stu-id="3a23b-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="3a23b-107">Il supporto per gli ordini di vendita del progetto con più fonti di finanziamento è disponibile a partire dalla versione dell'applicazione 10.0.2 e successive.</span><span class="sxs-lookup"><span data-stu-id="3a23b-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="3a23b-108">Il parametro per abilitare il supporto per gli ordini di vendita del progetto con più fonti di finanziamento verrà rimosso nell'ondata di rilascio di aprile 2020, dopodiché la funzionalità sarà sempre abilitata.</span><span class="sxs-lookup"><span data-stu-id="3a23b-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="3a23b-109">È possibile creare ordini di vendita basati su progetto in due modi:</span><span class="sxs-lookup"><span data-stu-id="3a23b-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="3a23b-110">Vai al progetto stesso.</span><span class="sxs-lookup"><span data-stu-id="3a23b-110">Go to the project itself.</span></span> <span data-ttu-id="3a23b-111">Nel riquadro azioni seleziona **Gestisci > Attività articolo > Ordine di vendita**.</span><span class="sxs-lookup"><span data-stu-id="3a23b-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="3a23b-112">Le informazioni sul progetto verranno impostate per impostazione predefinita sull'ordine di vendita del progetto.</span><span class="sxs-lookup"><span data-stu-id="3a23b-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="3a23b-113">Se il contratto di progetto ha più di una fonte di finanziamento, sarà necessario selezionare la fonte di finanziamento per impostare il cliente per l'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="3a23b-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="3a23b-114">Se esiste una sola fonte di finanziamento per il progetto, il cliente verrà impostato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3a23b-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="3a23b-115">Vai alla pagina elenco **Tutti gli ordini di vendita** e crea un nuovo ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="3a23b-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="3a23b-116">Sarà necessario selezionare il progetto per l'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="3a23b-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="3a23b-117">Dopo aver selezionato il progetto, il cliente verrà impostato dalla fonte di finanziamento o sarà necessario selezionare la fonte di finanziamento se il contratto di progetto ha più fonti di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="3a23b-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

