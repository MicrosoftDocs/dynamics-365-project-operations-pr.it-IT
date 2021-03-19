---
title: Eliminare una stima di progetto
description: Questo argomento fornisce informazioni sull'eliminazione di una stima di progetto una volta completata.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270683"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="c7ad5-103">Eliminare una stima di progetto</span><span class="sxs-lookup"><span data-stu-id="c7ad5-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7ad5-104">Le stime di progetto forniscono una vista finanziaria del il lavoro stimato e pianificato per un progetto.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="c7ad5-105">Per utilizzare le stime per un progetto, è necessario collegare il progetto a un progetto di stima.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="c7ad5-106">Un progetto di stima si basa sempre su un progetto esistente, tuttavia più progetti possono fare riferimento a un singolo progetto di stima.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="c7ad5-107">Ai progetti di stima possono essere collegati solo progetti a prezzo fisso e di investimento e tali progetti devono appartenere allo stesso gruppo di progetti del progetto di stima.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="c7ad5-108">Il progetto di stima deve essere completo per poter essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="c7ad5-109">I passaggi seguenti spiegano come eliminare una stima.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="c7ad5-110">Vai a **Gestione progetti e contabilità** > **Tutti i progetti** e apri il progetto.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="c7ad5-111">Nella scheda **Gestione** seleziona **Stime** e nella pagina **Stima** seleziona **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="c7ad5-112">Nella pagina **Elimina stima** nella scheda **Generale** imposta le seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="c7ad5-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="c7ad5-113">**Codice periodo**: Seleziona il codice del periodo per scegliere i progetti di stima appropriati.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="c7ad5-114">**Data di stima**: Seleziona la data di stima appropriata per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="c7ad5-115">**Elimina con gli avvisi WIP**: Abilita questa opzione per fornire una notifica quando una stima collegata a un lavoro in corso (WIP) verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="c7ad5-116">Quando questa opzione non è abilitata, l'eliminazione non può continuare se esistono transazioni non stimate.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="c7ad5-117">Questa opzione è disponibile solo quando l'eliminazione viene applicata a un progetto di stima.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="c7ad5-118">Non è disponibile se usi le registrazioni periodiche.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="c7ad5-119">Questa impostazione funziona con le impostazioni nella scheda **Stima** della pagina **Parametri di progetto** nel gruppo di campi **Consenti eliminazione quando esistono transazioni non stimate**.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="c7ad5-120">**Imposta la fase su Finito**: Abilita questa opzione per impostare la fase del progetto di stima su **Finito** dopo aver eseguito l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="c7ad5-121">**Stampa elenco stime**: Seleziona le informazioni da includere quando viene stampato l'elenco delle stime.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="c7ad5-122">**Mostra infolog**: Abilita questa opzione per visualizzare l'infolog.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="c7ad5-123">**Data registrazione**: Scegli la data di registrazione contabile della stima.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="c7ad5-124">Seleziona **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-124">Select **OK**.</span></span>
5. <span data-ttu-id="c7ad5-125">Una volta completato il processo di eliminazione, il progetto di stima eliminato viene visualizzato con un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="c7ad5-126">Se non intendevi eliminare una stima, puoi selezionare la stima eliminata e selezionare **Annulla eliminazione**.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]