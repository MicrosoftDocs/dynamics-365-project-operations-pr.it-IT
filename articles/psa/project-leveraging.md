---
title: Progetti e stime di vendita
description: In questo argomento vengono fornite informazioni su come utilizzare la pianificazione e le stime nel processo di vendita.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 49d109be3d55e7f208edb2698e420f40bb7843df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998416"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="ee996-103">Progetti e stime di vendita</span><span class="sxs-lookup"><span data-stu-id="ee996-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ee996-104">Durante il processo di vendita, puoi creare stime di vendita collegando un progetto a un'offerta di vendita.</span><span class="sxs-lookup"><span data-stu-id="ee996-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="ee996-105">In questo modo, la stima deterministica può avvenire durante il processo di vendita, in modo da utilizzare le funzionalità di stima e pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="ee996-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="ee996-106">Se la vendita viene eseguita, la pianificazione utilizzata per scopi di stima delle vendite può essere utilizzata come base per un ulteriore perfezionamento del piano di progetto.</span><span class="sxs-lookup"><span data-stu-id="ee996-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="ee996-107">Collegamento di un progetto a una riga di offerta</span><span class="sxs-lookup"><span data-stu-id="ee996-107">Linking a project to a quote line</span></span>

<span data-ttu-id="ee996-108">Quando crei una riga di offerta basata su progetto, puoi creare un nuovo progetto o associare un progetto esistente nella pagina **Riga di offerta**.</span><span class="sxs-lookup"><span data-stu-id="ee996-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Modulo Riga di offerta](media/project-8.png)
 
<span data-ttu-id="ee996-110">Quando crei un nuovo progetto a partire dai dettagli della riga di offerta, puoi utilizzare i modelli di progetto.</span><span class="sxs-lookup"><span data-stu-id="ee996-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="ee996-111">I modelli di progetto sono progetti che rappresentano i piani di progetto standard e stime finanziarie tipici di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ee996-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="ee996-112">Possono anche rappresentare copie di stime e piani di progetto di progetti passati.</span><span class="sxs-lookup"><span data-stu-id="ee996-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Dettagli riga di offerta](media/project-9.png)
  
<span data-ttu-id="ee996-114">Quando crei il progetto a partire dall'offerta, questo viene automaticamente associato alla riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="ee996-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="ee996-115">Componenti di stime in un progetto</span><span class="sxs-lookup"><span data-stu-id="ee996-115">Components of estimates in a project</span></span>

<span data-ttu-id="ee996-116">Una pianificazione ti consente di dividere il lavoro in attività, gestire una gerarchia di attività, determinare quali risorse sono necessarie per completare un'attività e assegnare una stima del lavoro necessario per completare un'attività.</span><span class="sxs-lookup"><span data-stu-id="ee996-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="ee996-117">Puoi definire il lavoro richiesto e pianificare le stime utilizzando i campi nella scheda **Pianifica** della pagina **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="ee996-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="ee996-118">Poiché un listino prezzi è associato al progetto, le stime finanziarie vengono calcolate utilizzando prezzi di costo e vendita definiti nel listino prezzi.</span><span class="sxs-lookup"><span data-stu-id="ee996-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="ee996-119">Importazione di stime da un progetto in un'offerta</span><span class="sxs-lookup"><span data-stu-id="ee996-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="ee996-120">Dopo aver definito le stime di progetto, puoi importarle nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="ee996-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="ee996-121">Nella pagina **Dettagli riga di offerta**, seleziona **Importa da stime** nella barra multifunzione per riepilogare stime di progetto per tipo di transazione, ruolo o livello di attività.</span><span class="sxs-lookup"><span data-stu-id="ee996-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]