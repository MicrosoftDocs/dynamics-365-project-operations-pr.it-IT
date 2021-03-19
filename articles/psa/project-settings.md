---
title: Impostazioni di progetto
description: In questo argomento vengono fornite informazioni sulle impostazioni per la gestione di progetti.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: c55d0f4c8f8db231a995d91a46a582bca2e1e6e3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283733"
---
# <a name="project-settings"></a><span data-ttu-id="f28ff-103">Impostazioni di progetto</span><span class="sxs-lookup"><span data-stu-id="f28ff-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f28ff-104">Utilizza le impostazioni seguenti per accedere alle funzionalità di pianificazione di progetti.</span><span class="sxs-lookup"><span data-stu-id="f28ff-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="f28ff-105">Modello di lavoro</span><span class="sxs-lookup"><span data-stu-id="f28ff-105">Work template</span></span>

<span data-ttu-id="f28ff-106">Per creare una pianificazione di progetto, creai un modello di calendario di progetto che definisce il numero di ore lavorative giornaliere e le chiusure aziendali.</span><span class="sxs-lookup"><span data-stu-id="f28ff-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="f28ff-107">Per creare un modello di calendario di progetto, associ un modello di lavoro al campo **Modello calendario** del progetto.</span><span class="sxs-lookup"><span data-stu-id="f28ff-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="f28ff-108">Segui questi passaggi per creare un modello di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f28ff-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="f28ff-109">In PSA, nel riquadro di navigazione sinistro, fai clic su **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="f28ff-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="f28ff-110">Nella pagina elenco **Risorse**, apri un record utente, quindi seleziona **Mostra ore lavorative**.</span><span class="sxs-lookup"><span data-stu-id="f28ff-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f28ff-111">Verifica che le finestre pop-up siano consentite nella pagina del browser.</span><span class="sxs-lookup"><span data-stu-id="f28ff-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="f28ff-112">Ciò consente di visualizzare le ore lavorative impostate per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f28ff-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="f28ff-113">Nella scheda **Vista mensile**, fai clic su **Configura**.</span><span class="sxs-lookup"><span data-stu-id="f28ff-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="f28ff-114">Viene visualizzato un elenco con tre opzioni:</span><span class="sxs-lookup"><span data-stu-id="f28ff-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="f28ff-115">Nuova pianificazione settimanale</span><span class="sxs-lookup"><span data-stu-id="f28ff-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="f28ff-116">Pianificazione lavorativa per un giorno</span><span class="sxs-lookup"><span data-stu-id="f28ff-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="f28ff-117">Indisponibilità</span><span class="sxs-lookup"><span data-stu-id="f28ff-117">Time Off</span></span>

> ![Opzioni di Configura](media/project-13.png)

4. <span data-ttu-id="f28ff-119">Seleziona **Nuova pianificazione settimanale** e quindi imposta le opzioni per questa pianificazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f28ff-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="f28ff-120">Puoi impostare una pianificazione settimanale ricorrente, parametri orari giornalieri, chiusure aziendali e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="f28ff-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="f28ff-121">Imposta l'intervallo di date, seleziona **Salva** e quindi fai clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="f28ff-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="f28ff-122">Torna alla pagina elenco **Risorse** e seleziona la risorsa per la quale imposti le ore lavorative.</span><span class="sxs-lookup"><span data-stu-id="f28ff-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="f28ff-123">Seleziona **Imposta calendario come** per impostare il modello di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f28ff-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="f28ff-124">Nella finestra di dialogo **Modello di lavoro**, immetti un nome per il modello di lavoro e quindi seleziona **Applica**.</span><span class="sxs-lookup"><span data-stu-id="f28ff-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="f28ff-125">Ora puoi associare il modello di lavoro a un modello di calendario di progetto.</span><span class="sxs-lookup"><span data-stu-id="f28ff-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="f28ff-126">Ruoli risorsa</span><span class="sxs-lookup"><span data-stu-id="f28ff-126">Resource roles</span></span>

<span data-ttu-id="f28ff-127">Il termine *ruolo risorsa* fa riferimento al set di competenze, qualifiche e certificazioni che una persona deve avere per eseguire un insieme specifico di attività in un progetto.</span><span class="sxs-lookup"><span data-stu-id="f28ff-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="f28ff-128">PSA ti consente di determinare il costo del tempo di una risorsa e di fatturarlo in base al ruolo a cui quella risorsa è associata.</span><span class="sxs-lookup"><span data-stu-id="f28ff-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="f28ff-129">Ogni organizzazione deve impostare questi ruoli utilizzando il riquadro di navigazione sinistro nel menu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="f28ff-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="f28ff-130">Ogni organizzazione deve impostare questi ruoli nella pagina **Categorie di risorse attive**.</span><span class="sxs-lookup"><span data-stu-id="f28ff-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="f28ff-131">Per aprire questa pagina, nel riquadro di navigazione sinistro, seleziona **Ruoli risorsa**.</span><span class="sxs-lookup"><span data-stu-id="f28ff-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="f28ff-132">Listini prezzi</span><span class="sxs-lookup"><span data-stu-id="f28ff-132">Price lists</span></span>

<span data-ttu-id="f28ff-133">I listini prezzi consentono di impostare i prezzi di costo e di vendita per ruoli risorsa, categorie di spese, prodotti e altri elementi in un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f28ff-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="f28ff-134">Prima di impostare le stime finanziarie per il lavoro da eseguire per un progetto, devi creare un listino prezzi di costo e vendita di backup.</span><span class="sxs-lookup"><span data-stu-id="f28ff-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="f28ff-135">Nella sezione dei parametri, devi impostare anche un listino prezzi di costo e vendita predefinito applicabile a tutti i progetti creati nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f28ff-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="f28ff-136">Nella pagina **Parametri progetto attivi**, verifica di aver impostato un listino prezzi di costo e vendita predefinito.</span><span class="sxs-lookup"><span data-stu-id="f28ff-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]