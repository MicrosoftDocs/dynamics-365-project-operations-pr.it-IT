---
title: Calendario di inserimenti ore
description: In questo argomento vengono fornite informazioni su come utilizzare il calendario di inserimenti ore.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cc78d9ae-9f1b-4bd4-8cdf-41406f859ff7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ea8c5113b9ba89e2255218e6a53f062c25badc98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752687"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="6b1bd-103">Calendario di inserimenti ore</span><span class="sxs-lookup"><span data-stu-id="6b1bd-103">Time entry calendar</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6b1bd-104">Nella pagina **Inserimenti ore**, puoi visualizzare gli inserimenti ore nel calendario selezionando **Mostra come** \> **Controllo calendario**.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="6b1bd-105">Controllo calendario aggiornato</span><span class="sxs-lookup"><span data-stu-id="6b1bd-105">Updated calendar control</span></span>

<span data-ttu-id="6b1bd-106">Dynamics 365 Project Service Automation offre una nuova esperienza di inserimento ore estendibile.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="6b1bd-107">Questa nuova esperienza sostituisce il controllo calendario personalizzato utilizzato nelle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="6b1bd-108">Tuttavia, è ancora possibile visualizzare gli inserimenti ore mediante un controllo calendario di sola lettura che il framework Unified Interface fornisce per viste giornaliere, settimanali o mensili.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="6b1bd-109">Il calendario non supporta azioni per singoli elementi del calendario e non è possibile selezionare uno o più elementi del calendario per l'invio o l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="6b1bd-110">È invece possibile selezionare un elemento del calendario per aprire la pagina dell'entità **Inserimento ore**, dove puoi completare le azioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="6b1bd-111">Estendibilità </span><span class="sxs-lookup"><span data-stu-id="6b1bd-111">Extensibility</span></span>

<span data-ttu-id="6b1bd-112">Nella pagina **Inserimenti ore** che include la griglia di inserimento ore, puoi aggiungere campi personalizzati, configurare campi di tipo lookup e creare viste personalizzate.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="6b1bd-113">Puoi anche impostare logica di business personalizzata basata sui valori selezionati o immessi nei campi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>
