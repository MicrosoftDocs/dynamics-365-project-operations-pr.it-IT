---
title: Ordini di vendita di progetto per progetti relativi a tempi e materiali
description: Questo argomento spiega come creare ordini di vendita basati su progetto per progetti relativi a tempi e materiali.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009666"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="9c7f2-103">Ordini di vendita di progetto per progetti relativi a tempi e materiali</span><span class="sxs-lookup"><span data-stu-id="9c7f2-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9c7f2-104">Questo argomento descrive come creare un ordine di vendita per un progetto.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="9c7f2-105">Gli ordini di vendita possono essere creati solo per progetti di tipo **tempo e materiale**.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="9c7f2-106">Se un progetto relativo a tempi e materiali ha più fonti di finanziamento nel contratto di progetto, devi abilitare il parametro **Consenti ordini di vendita per progetti con più fonti di finanziamento** nella pagina **Gestione progetti e contabilità**.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="9c7f2-107">Il supporto per gli ordini di vendita del progetto con più fonti di finanziamento è disponibile a partire dalla versione dell'applicazione 10.0.2 e successive.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="9c7f2-108">Il parametro per abilitare il supporto per gli ordini di vendita del progetto con più fonti di finanziamento verrà rimosso nell'ondata di rilascio di aprile 2020, dopodiché la funzionalità sarà sempre abilitata.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="9c7f2-109">È possibile creare ordini di vendita basati su progetto in due modi:</span><span class="sxs-lookup"><span data-stu-id="9c7f2-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="9c7f2-110">Vai al progetto stesso.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-110">Go to the project itself.</span></span> <span data-ttu-id="9c7f2-111">Nel riquadro azioni seleziona **Gestisci > Attività articolo > Ordine di vendita**.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="9c7f2-112">Le informazioni sul progetto verranno impostate per impostazione predefinita sull'ordine di vendita del progetto.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="9c7f2-113">Se il contratto di progetto ha più di una fonte di finanziamento, sarà necessario selezionare la fonte di finanziamento per impostare il cliente per l'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="9c7f2-114">Se esiste una sola fonte di finanziamento per il progetto, il cliente verrà impostato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="9c7f2-115">Vai alla pagina elenco **Tutti gli ordini di vendita** e crea un nuovo ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="9c7f2-116">Sarà necessario selezionare il progetto per l'ordine di vendita.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="9c7f2-117">Dopo aver selezionato il progetto, il cliente verrà impostato dalla fonte di finanziamento o sarà necessario selezionare la fonte di finanziamento se il contratto di progetto ha più fonti di finanziamento.</span><span class="sxs-lookup"><span data-stu-id="9c7f2-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]