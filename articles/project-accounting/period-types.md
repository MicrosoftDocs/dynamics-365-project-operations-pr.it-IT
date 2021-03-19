---
title: Tipi di periodo
description: Questo argomento fornisce informazioni su come configurare i tipi di periodo per la stima dei ricavi.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287288"
---
# <a name="period-types"></a><span data-ttu-id="ef603-103">Tipi di periodo</span><span class="sxs-lookup"><span data-stu-id="ef603-103">Period types</span></span>

<span data-ttu-id="ef603-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="ef603-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ef603-105">Un tipo di periodo definisce la frequenza con cui vengono stimate le entrate per un progetto.</span><span class="sxs-lookup"><span data-stu-id="ef603-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="ef603-106">Questo argomento fornisce informazioni su come configurare i tipi di periodo per la stima dei ricavi.</span><span class="sxs-lookup"><span data-stu-id="ef603-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="ef603-107">Creare e utilizzare tipi di periodo</span><span class="sxs-lookup"><span data-stu-id="ef603-107">Create and work with period types</span></span>
<span data-ttu-id="ef603-108">Per creare e utilizzare i tipi di periodo, completare i seguenti passaggi:</span><span class="sxs-lookup"><span data-stu-id="ef603-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="ef603-109">Nel tuo ambiente Dynamics 365 Finance, vai a **Contabilità e gestione progetti** > **Configurazione** > **Stime** > **Tipi di periodo**.</span><span class="sxs-lookup"><span data-stu-id="ef603-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="ef603-110">Seleziona **Nuovo** per creare un nuovo tipo di periodo.</span><span class="sxs-lookup"><span data-stu-id="ef603-110">Select **New** to create new period type.</span></span> <span data-ttu-id="ef603-111">Immetti un nome e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="ef603-111">Enter a name and description.</span></span>
3. <span data-ttu-id="ef603-112">Nel campo **Frequenza**, seleziona un valore.</span><span class="sxs-lookup"><span data-stu-id="ef603-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="ef603-113">Se selezioni **Settimana**, **Bisettimanale**, **Semestrale**, **Mese**, **Giorno**, **Trimestre** o **Anno**, il calendario verrà utilizzato per generare i periodi.</span><span class="sxs-lookup"><span data-stu-id="ef603-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="ef603-114">Se selezioni **Periodo contabile**, i periodi di contabilità generale dalla configurazione di contabilità generale verranno utilizzati per generare periodi.</span><span class="sxs-lookup"><span data-stu-id="ef603-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="ef603-115">Se selezioni **Illimitato**, puoi specificare periodi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="ef603-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="ef603-116">Selezionare il record del tipo di periodo e quindi selezionare **Genera periodi** per creare periodi per il tipo di periodo.</span><span class="sxs-lookup"><span data-stu-id="ef603-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="ef603-117">In base alla frequenza del periodo selezionata, potresti avere la possibilità di specificare una data di inizio o il numero di periodi da generare.</span><span class="sxs-lookup"><span data-stu-id="ef603-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="ef603-118">Seleziona **Periodi** per rivedere i periodi generati.</span><span class="sxs-lookup"><span data-stu-id="ef603-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]