---
title: Panoramica dell'utilizzo della risorsa
description: In questo argomento vengono fornite informazioni sull'utilizzo delle risorse in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401381"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="6246b-103">Panoramica dell'utilizzo della risorsa</span><span class="sxs-lookup"><span data-stu-id="6246b-103">Resource utilization overview</span></span>

<span data-ttu-id="6246b-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="6246b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6246b-105">Le risorse possono avere un utilizzo di destinazione fatturabile.</span><span class="sxs-lookup"><span data-stu-id="6246b-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="6246b-106">Questo utilizzo di destinazione è definito come attributo per il ruolo predefinito di una risorsa o impostato nel record della singola risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="6246b-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="6246b-107">I calcoli dell'utilizzo sono basati sulle ore effettive che le risorse hanno indicato utilizzando inserimenti ore approvati.</span><span class="sxs-lookup"><span data-stu-id="6246b-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="6246b-108">Le seguenti formule vengono utilizzate per calcolare l'utilizzo:</span><span class="sxs-lookup"><span data-stu-id="6246b-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="6246b-109">Utilizzo fatturabile = Ore effettive addebitabili ÷ Capacità della risorsa</span><span class="sxs-lookup"><span data-stu-id="6246b-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="6246b-110">Utilizzo non fatturabile = Tempo effettivo con ID tipo di fatturazione = Non addebitabile, Complementare o Non disponibile ÷ Capacità della risorsa</span><span class="sxs-lookup"><span data-stu-id="6246b-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="6246b-111">Interno = Tempo effettivo senza contratto di vendita ÷ Capacità della risorsa</span><span class="sxs-lookup"><span data-stu-id="6246b-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="6246b-112">Capacità della risorsa = Ore lavorative della risorsa - Fuori sede - Giorni non lavorativi</span><span class="sxs-lookup"><span data-stu-id="6246b-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="6246b-113">La vista **Utilizzo risorsa** si trova nel riquadro **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="6246b-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="6246b-114">Ogni cella nella griglia rappresenta la percentuale di utilizzo fatturabile della risorsa in un periodo, ad esempio un giorno, una settimana o un mese.</span><span class="sxs-lookup"><span data-stu-id="6246b-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="6246b-115">Le seguenti formule vengono utilizzate per colorare le celle:</span><span class="sxs-lookup"><span data-stu-id="6246b-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="6246b-116">**Verde**: utilizzo fatturabile >= utilizzo di destinazione risorsa</span><span class="sxs-lookup"><span data-stu-id="6246b-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="6246b-117">**Giallo**: utilizzo di destinazione – 20 <= utilizzo fatturabile < utilizzo di destinazione</span><span class="sxs-lookup"><span data-stu-id="6246b-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="6246b-118">**Rosso**: utilizzo fatturabile <= utilizzo di destinazione – 20</span><span class="sxs-lookup"><span data-stu-id="6246b-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="6246b-119">Poiché la vista **Utilizzo risorsa** è basata sulla scheda di pianificazione, puoi utilizzare le funzionalità di filtro della scheda di pianificazione per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="6246b-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="6246b-120">La griglia richiede l'impostazione di un utilizzo di destinazione per il ruolo o la singola risorsa.</span><span class="sxs-lookup"><span data-stu-id="6246b-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="6246b-121">A questo proposito, seleziona **Risorse** > **Ruoli risorsa**.</span><span class="sxs-lookup"><span data-stu-id="6246b-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="6246b-122">Inoltre, un ruolo predefinito deve essere assegnato a ogni risorsa prenotabile.</span><span class="sxs-lookup"><span data-stu-id="6246b-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="6246b-123">Seleziona **Risorse** > **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="6246b-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="6246b-124">Nella scheda **Project Service** verifica che un ruolo risorsa sia definito e che il relativo campo **Predefinito** sia impostato su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="6246b-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="6246b-125">Puoi aggiungere ruoli aggiuntivi dove **Predefinito** = **No**.</span><span class="sxs-lookup"><span data-stu-id="6246b-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="6246b-126">Il ruolo dove **Predefinito** = **Sì** viene utilizzato per valutare l'utilizzo della risorsa in base alla destinazione di quel ruolo.</span><span class="sxs-lookup"><span data-stu-id="6246b-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="6246b-127">Nella scheda **Project Service**, puoi impostare un singolo utilizzo di destinazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6246b-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="6246b-128">Per il calcolo dell'utilizzo viene quindi utilizzato l'utilizzo di destinazione allo scopo di valutare la destinazione della risorsa anziché la destinazione del ruolo predefinito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6246b-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="6246b-129">L'utilizzo viene visualizzato per una risorsa solo se ha tempo addebitabile approvato durante il periodo visualizzato nella griglia.</span><span class="sxs-lookup"><span data-stu-id="6246b-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>
