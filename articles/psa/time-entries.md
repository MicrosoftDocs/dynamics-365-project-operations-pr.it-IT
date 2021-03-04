---
title: Creare inserimenti ore
description: In questo argomento vengono fornite informazioni su come creare inserimenti ore.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149683"
---
# <a name="create-time-entries"></a><span data-ttu-id="32cda-103">Creare inserimenti ore</span><span class="sxs-lookup"><span data-stu-id="32cda-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="32cda-104">Nelle versioni precedenti di Dynamics 365 Project Service Automation, gli inserimenti ore venivano immessi su base settimanale.</span><span class="sxs-lookup"><span data-stu-id="32cda-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="32cda-105">Nella versione 3 di Project Service Automation, gli inserimenti ore vengono immessi su base giornaliera.</span><span class="sxs-lookup"><span data-stu-id="32cda-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="32cda-106">Tuttavia, dopo la creazione di alcuni inserimenti, puoi crearli o copiarli in bulk.</span><span class="sxs-lookup"><span data-stu-id="32cda-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="32cda-107">Creare un inserimento ore</span><span class="sxs-lookup"><span data-stu-id="32cda-107">Create a time entry</span></span>

<span data-ttu-id="32cda-108">Segui questi passaggi per creare un inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="32cda-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="32cda-109">Nella pagina **Inserimenti ore**, seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="32cda-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="32cda-110">Nella finestra di dialogo **Creazione rapida: Inserimento ore**, immettere la durata dell'inserimento ore in minuti, ore, o giorni.</span><span class="sxs-lookup"><span data-stu-id="32cda-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="32cda-111">La durata deve essere immessa nel formato seguente: *x* minuti", *x* ore o *x* giorni.</span><span class="sxs-lookup"><span data-stu-id="32cda-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="32cda-112">Ore e giorni possono anche essere immessi come valori decimali, ad esempio *x,x* ore o *x,x* giorni.</span><span class="sxs-lookup"><span data-stu-id="32cda-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="32cda-113">Seleziona il tipo di inserimento ore e il progetto per il quale stai immettendo l'inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="32cda-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="32cda-114">Nel campo **Attività di progetto**, trova l'attività per questo inserimento ore.</span><span class="sxs-lookup"><span data-stu-id="32cda-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="32cda-115">Se stai creando un inserimento ore per un'attività non assegnata a un utente, nel campo **Attività di progetto**, seleziona il pulsante **Cerca**, seleziona **Cambia vista** e quindi **Tutte le attività di progetto attive** per elencare tutte le attività.</span><span class="sxs-lookup"><span data-stu-id="32cda-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="32cda-116">Immetti una descrizione, se una descrizione è richiesta, quindi seleziona **Salva e chiudi**.</span><span class="sxs-lookup"><span data-stu-id="32cda-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="32cda-117">Dopo la creazione e il salvataggio dell'inserimento ore, puoi modificarlo nella griglia degli inserimenti.</span><span class="sxs-lookup"><span data-stu-id="32cda-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="32cda-118">La griglia degli inserimenti ore supporta due formati:</span><span class="sxs-lookup"><span data-stu-id="32cda-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="32cda-119">Puoi immettere inserimenti ore nel formato **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="32cda-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="32cda-120">Questo formato viene quindi convertito in ore e frazioni.</span><span class="sxs-lookup"><span data-stu-id="32cda-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="32cda-121">Puoi immettere ore e frazioni direttamente.</span><span class="sxs-lookup"><span data-stu-id="32cda-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="32cda-122">Nota che le frazioni di un'ora non sono minuti.</span><span class="sxs-lookup"><span data-stu-id="32cda-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="32cda-123">Pertanto, 1,5 ore rappresenta 1 ora e 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="32cda-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="32cda-124">La stessa regola si applica alle frazioni di un giorno.</span><span class="sxs-lookup"><span data-stu-id="32cda-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="32cda-125">Un giorno è 24 ore e 0,5 giorni rappresenta 12 ore.</span><span class="sxs-lookup"><span data-stu-id="32cda-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="32cda-126">Creare inserimenti ore in bulk</span><span class="sxs-lookup"><span data-stu-id="32cda-126">Bulk create time entries</span></span>

<span data-ttu-id="32cda-127">Dopo la creazione di alcuni inserimenti ore, puoi copiarli per creare ulteriori inserimenti ore in bulk.</span><span class="sxs-lookup"><span data-stu-id="32cda-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="32cda-128">Nella pagina **Inserimenti ore**, seleziona **Copia settimana**.</span><span class="sxs-lookup"><span data-stu-id="32cda-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="32cda-129">Nel gruppo di campi **Da periodo**, nei campi **Data di fine** e **Data di inizio**, definisci un intervallo di date da cui copiare gli inserimenti ore.</span><span class="sxs-lookup"><span data-stu-id="32cda-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="32cda-130">Nel gruppo di campi **Al periodo**, nel campo **Data di inizio**, specifica la data a partire dalla quale creare gli inserimenti ore.</span><span class="sxs-lookup"><span data-stu-id="32cda-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="32cda-131">Seleziona **Copia** per creare una copia degli inserimenti ore che corrispondono al giorno della settimana specificato nel gruppo di campi **Al periodo**.</span><span class="sxs-lookup"><span data-stu-id="32cda-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="32cda-132">Ad esempio, l'inserimento ore per il lunedì dell'ultima settimana viene copiata nel lunedì della settimana specificata nel gruppo di campi **Al periodo**.</span><span class="sxs-lookup"><span data-stu-id="32cda-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="32cda-133">Importare dati per inserimenti ore</span><span class="sxs-lookup"><span data-stu-id="32cda-133">Import data for time entries</span></span>

<span data-ttu-id="32cda-134">Puoi importare dati da prenotazioni e assegnazioni di progetto.</span><span class="sxs-lookup"><span data-stu-id="32cda-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="32cda-135">Quando importi dati, puoi specificare l'intervallo di date delle prenotazioni da importare e quindi selezionare in modo esplicito le prenotazioni che devono essere create come inserimenti ore **Bozza**.</span><span class="sxs-lookup"><span data-stu-id="32cda-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="32cda-136">Raggruppare, ordinare, cercare e filtrare funzionalità</span><span class="sxs-lookup"><span data-stu-id="32cda-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="32cda-137">Puoi raggruppare e filtrare gli inserimenti ore in base alle dimensioni specificate nelle colonne.</span><span class="sxs-lookup"><span data-stu-id="32cda-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="32cda-138">Nel campo **Raggruppa per**, seleziona la dimensione da utilizzare per filtrare gli inserimenti ore.</span><span class="sxs-lookup"><span data-stu-id="32cda-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="32cda-139">Puoi anche ordinare record di inserimenti ore in ordine crescente o decrescente utilizzando la freccia di ordinamento nelle intestazioni delle colonne.</span><span class="sxs-lookup"><span data-stu-id="32cda-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="32cda-140">Inoltre, puoi visualizzare o nascondere gli inserimenti selezionando il pulsante **Filtra** nelle intestazioni delle colonne e quindi immettendo, nella casella **Cerca**, il testo che deve essere utilizzato per cercare inserimenti ore per nome di progetto, attività di progetto, inserimento ore o risorsa.</span><span class="sxs-lookup"><span data-stu-id="32cda-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
