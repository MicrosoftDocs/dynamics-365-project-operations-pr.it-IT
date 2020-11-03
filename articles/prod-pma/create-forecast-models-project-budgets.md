---
title: Creare modelli previsionali per i budget di progetto
description: Questo argomento descrive come creare un modello di previsione per i budget residuo.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079012"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="28c32-103">Creare modelli previsionali per i budget di progetto</span><span class="sxs-lookup"><span data-stu-id="28c32-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28c32-104">Questo argomento descrive come creare un modello di previsione per i budget residuo.</span><span class="sxs-lookup"><span data-stu-id="28c32-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="28c32-105">Un progetto soggetto al controllo di budget utilizza due tipi di budget: originale e rimanente.</span><span class="sxs-lookup"><span data-stu-id="28c32-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="28c32-106">Quando crei un budget di progetto, devi specificare i modelli di previsione di budget originale e rimanente creati nella pagina **Modelli previsionali**.</span><span class="sxs-lookup"><span data-stu-id="28c32-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="28c32-107">I budget di progetto basati sui modelli specificati vengono creati quando si impegna il budget di progetto.</span><span class="sxs-lookup"><span data-stu-id="28c32-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="28c32-108">Un modello di previsione utilizzato per il controllo di budget non può avere un sottomodello o essere utilizzato come sottomodello.</span><span class="sxs-lookup"><span data-stu-id="28c32-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="28c32-109">Seleziona **Gestione progetti e contabilità** > **Impostazione** > **Previsioni**  > **Modelli previsionali**.</span><span class="sxs-lookup"><span data-stu-id="28c32-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="28c32-110">Seleziona **Nuovo** per creare un nuovo modello previsionale, quindi immetti un numero ID modello e un nome per il nuovo modello.</span><span class="sxs-lookup"><span data-stu-id="28c32-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="28c32-111">Imposta l'opzione **Interrotto** su **Sì** per impedire qualsiasi modifica alle righe di previsione per il modello previsionale.</span><span class="sxs-lookup"><span data-stu-id="28c32-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="28c32-112">Se le righe di previsione a cui è associato il modello devono generare previsioni di flusso di cassa nella contabilità generale, imposta **Includi in previsioni del flusso di cassa** su **Sì.**</span><span class="sxs-lookup"><span data-stu-id="28c32-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="28c32-113">Per utilizzare la data del progetto come data della fattura, imposta **Data fattura prevista** su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="28c32-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="28c32-114">Nel campo **Tipo di budget** seleziona uno dei tipi di modello indicati di seguito:</span><span class="sxs-lookup"><span data-stu-id="28c32-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="28c32-115">**Budget originale** : utilizza gli importi di budget originale impegnati quando il budget iniziale viene creato e approvato.</span><span class="sxs-lookup"><span data-stu-id="28c32-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="28c32-116">**Budget residuo** : utilizza gli importi di budget residuo durante la durata del progetto.</span><span class="sxs-lookup"><span data-stu-id="28c32-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="28c32-117">I saldi in questo modello di previsione vengono ridotti dalle transazioni effettive e aumentati o diminuiti dalle revisioni di budget.</span><span class="sxs-lookup"><span data-stu-id="28c32-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="28c32-118">**Riporto in avanti** : utilizzare gli importi di budget da riportare in avanti per il progetto.</span><span class="sxs-lookup"><span data-stu-id="28c32-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="28c32-119">Il riporto in avanti è un processo opzionale che può essere eseguito per trasferire importi di budget non utilizzati da un anno fiscale a un altro.</span><span class="sxs-lookup"><span data-stu-id="28c32-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="28c32-120">Imposta le opzioni seguenti come necessario:</span><span class="sxs-lookup"><span data-stu-id="28c32-120">Set the following options as required:</span></span>

   - <span data-ttu-id="28c32-121">Abilita **Data fattura prevista** per utilizzare la data del progetto come data della fattura.</span><span class="sxs-lookup"><span data-stu-id="28c32-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="28c32-122">Abilita **Previsione con WIP** per prevedere in base al lavoro in corso (WIP), quindi seleziona il tipo di WIP.</span><span class="sxs-lookup"><span data-stu-id="28c32-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="28c32-123">Puoi mantenere l'impostazione predefinita del **Tipo di budget** come **Nessuno** o inserire un nuovo tipo.</span><span class="sxs-lookup"><span data-stu-id="28c32-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="28c32-124">Il tipo di budget non può essere modificato dopo aver modificato un record.</span><span class="sxs-lookup"><span data-stu-id="28c32-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="28c32-125">Se modifichi il tipo di budget predefinito, tutte le altre opzioni non saranno disponibili per gli aggiornamenti e non potrai riutilizzare questo modello di previsione.</span><span class="sxs-lookup"><span data-stu-id="28c32-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

