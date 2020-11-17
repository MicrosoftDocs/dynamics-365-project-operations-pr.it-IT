---
title: Spostamento nell'interfaccia utente
description: Questo argomento fornisce informazioni sulla gestione dei progetti in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127523"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="77b1c-103">Spostamento nell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="77b1c-103">Navigating the user interface</span></span>

<span data-ttu-id="77b1c-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="77b1c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="77b1c-105">Panoramica</span><span class="sxs-lookup"><span data-stu-id="77b1c-105">Overview</span></span>

<span data-ttu-id="77b1c-106">Il modulo principale del progetto è suddiviso in diverse schede.</span><span class="sxs-lookup"><span data-stu-id="77b1c-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="77b1c-107">Ciascuna scheda rappresenta un diverso livello di dettaglio all'interno del progetto.</span><span class="sxs-lookup"><span data-stu-id="77b1c-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="77b1c-108">**Riepilogo**: fornisce una descrizione del progetto e aggrega le prestazioni del progetto pianificate ed effettive.</span><span class="sxs-lookup"><span data-stu-id="77b1c-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Scheda Riepilogo e campi](media/navigation7.png)

- <span data-ttu-id="77b1c-110">**Attività**: fornisce i dettagli relativi alla struttura di suddivisione del lavoro rappresentata da una vista griglia, una vista scheda e un diagramma di Gantt.</span><span class="sxs-lookup"><span data-stu-id="77b1c-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Scheda Attività e campi](media/navigation8.png)

- <span data-ttu-id="77b1c-112">**Team**: fornisce dettagli sui partecipanti al progetto.</span><span class="sxs-lookup"><span data-stu-id="77b1c-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="77b1c-113">Anche il lavoro richiesto assegnato a ciascun membro del team è riepilogato in questa vista.</span><span class="sxs-lookup"><span data-stu-id="77b1c-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Scheda Team e campi](media/navigation9.png)

- <span data-ttu-id="77b1c-115">**Assegnazioni risorse**: fornisce una visualizzazione cronologica del lavoro richiesto per ciascuna risorsa in un progetto.</span><span class="sxs-lookup"><span data-stu-id="77b1c-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Scheda Assegnazioni risorse e campi](media/navigation10.png)

- <span data-ttu-id="77b1c-117">**Riconciliazione risorse**: fornisce una visualizzazione cronologica delle differenze tra le assegnazioni di ciascuna risorsa denominata e le relative prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="77b1c-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Scheda Riconciliazione risorse e campi](media/navigation11.png)

- <span data-ttu-id="77b1c-119">**Stime**: fornisce una visualizzazione cronologica delle stime di vendita e costi di un progetto.</span><span class="sxs-lookup"><span data-stu-id="77b1c-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Scheda Stime e campi](media/navigation12.png)

- <span data-ttu-id="77b1c-121">**Registrazione**: fornisce una visualizzazione che mostra lo stato di avanzamento delle attività nella struttura di suddivisione del lavoro per lavoro richiesto, costo e vendite.</span><span class="sxs-lookup"><span data-stu-id="77b1c-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Scheda Registrazione e campi](media/navigation13.png)

- <span data-ttu-id="77b1c-123">**Vendite**: fornisce collegamenti diretti a offerte e contratti associati al progetto.</span><span class="sxs-lookup"><span data-stu-id="77b1c-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="77b1c-124">**Stime di spesa**: fornisce una griglia che definisce le spese del progetto in base alle categorie di spesa dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="77b1c-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Scheda Stime di spesa e campi](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="77b1c-126">Controlli della griglia</span><span class="sxs-lookup"><span data-stu-id="77b1c-126">Grid controls</span></span>

<span data-ttu-id="77b1c-127">Di seguito è riportata una breve panoramica dei controlli tipici presenti nelle varie schede di pianificazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="77b1c-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="77b1c-128">Refresh</span><span class="sxs-lookup"><span data-stu-id="77b1c-128">Refresh</span></span>

<span data-ttu-id="77b1c-129">**Aggiorna**: recupera i dati più recenti dal server se sono state apportate modifiche dopo il caricamento della griglia.</span><span class="sxs-lookup"><span data-stu-id="77b1c-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Pulsante Aggiorna](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="77b1c-131">Raggruppa per</span><span class="sxs-lookup"><span data-stu-id="77b1c-131">Group by</span></span>

<span data-ttu-id="77b1c-132">**Raggruppa per**: aggiorna il raggruppamento delle righe nella griglia per riflettere risorse, ruoli o categorie in base alle esigenze dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77b1c-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Pulsante Raggruppa per](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="77b1c-134">Precedente/Successivo</span><span class="sxs-lookup"><span data-stu-id="77b1c-134">Previous/Next</span></span>

<span data-ttu-id="77b1c-135">**Precedente**/**Successivo**: aggiorna i periodi di tempo visibili sulle griglie temporali.</span><span class="sxs-lookup"><span data-stu-id="77b1c-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Pulsanti Precedente e Successivo](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="77b1c-137">Scala cronologica</span><span class="sxs-lookup"><span data-stu-id="77b1c-137">Timescale</span></span>

<span data-ttu-id="77b1c-138">**Scala cronologica**: modifica l'aggregazione dei dati cronologici tra giorni, settimane, mesi e anni.</span><span class="sxs-lookup"><span data-stu-id="77b1c-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Pulsante Scala cronologica](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="77b1c-140">Espansione</span><span class="sxs-lookup"><span data-stu-id="77b1c-140">Expand</span></span>

<span data-ttu-id="77b1c-141">**Espandi**: esegue il rendering della griglia visibile a schermo intero consentendo di vedere ruoli aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="77b1c-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Pulsante Espandi](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="77b1c-143">Scala cronologica per</span><span class="sxs-lookup"><span data-stu-id="77b1c-143">Time-phase by</span></span>

<span data-ttu-id="77b1c-144">**Scala cronologica per**: aggiorna il raggruppamento delle righe nella griglia per riflettere le stime dei costi per le stime di vendita.</span><span class="sxs-lookup"><span data-stu-id="77b1c-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="77b1c-145">Questo controllo si applica anche allo script di stima e alla griglia di registrazione.</span><span class="sxs-lookup"><span data-stu-id="77b1c-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Pulsante Scala cronologica per](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="77b1c-147">Aggiungi colonna</span><span class="sxs-lookup"><span data-stu-id="77b1c-147">Add column</span></span>

<span data-ttu-id="77b1c-148">**Aggiungi colonna**: consente all'utente di definire le colonne visibili nella griglia.</span><span class="sxs-lookup"><span data-stu-id="77b1c-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="77b1c-149">È possibile aggiungere solo colonne predefinite alle griglie nel modulo **Pianificazione progetto**.</span><span class="sxs-lookup"><span data-stu-id="77b1c-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Pulsante Aggiungi colonna](media/navigation5.png)
