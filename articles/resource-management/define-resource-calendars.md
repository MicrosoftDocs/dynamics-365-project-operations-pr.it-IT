---
title: Definire i calendari delle risorse
description: Questo argomento fornisce informazioni su come definire i calendari di ore lavorative per le risorse in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078724"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="ed137-103">Definire i calendari delle risorse</span><span class="sxs-lookup"><span data-stu-id="ed137-103">Define resource calendars</span></span>

<span data-ttu-id="ed137-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="ed137-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ed137-105">Ogni risorsa prenotabile che lavora su un progetto deve avere un calendario delle ore lavorative per definirne la disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ed137-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="ed137-106">L'orario di lavoro di una risorsa può essere definito in due modi:</span><span class="sxs-lookup"><span data-stu-id="ed137-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="ed137-107">Definisci regole di calendario individuali per una risorsa</span><span class="sxs-lookup"><span data-stu-id="ed137-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="ed137-108">Applica un modello di calendario esistente per la risorsa</span><span class="sxs-lookup"><span data-stu-id="ed137-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="ed137-109">Definire l'orario di lavoro di una risorsa</span><span class="sxs-lookup"><span data-stu-id="ed137-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="ed137-110">Nel menu **Risorse** , seleziona **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="ed137-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="ed137-111">Dalla visualizzazione griglia, seleziona la **Risorsa prenotabile** applicabile.</span><span class="sxs-lookup"><span data-stu-id="ed137-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="ed137-112">Nella pagina **Dettagli risorsa** , seleziona la scheda **Ore lavorative**. Per impostazione predefinita, il calendario delle risorse prenotabili utilizza per impostazione predefinita l'orario di lavoro del modello di ora di lavoro predefinito definito per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ed137-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="ed137-113">Per aggiornare l'orario di lavoro, fai clic con il tasto destro sulla data di inizio della regola di calendario proposta da definire.</span><span class="sxs-lookup"><span data-stu-id="ed137-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="ed137-114">Utilizza il menu delle regole del calendario per definire una regola del calendario per un giorno specifico, il resto della serie o l'intero calendario.</span><span class="sxs-lookup"><span data-stu-id="ed137-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="ed137-115">Dopo che l'opzione è stata selezionata, puoi definire:</span><span class="sxs-lookup"><span data-stu-id="ed137-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="ed137-116">Il giorno della settimana in cui si applicherà l'orario di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ed137-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="ed137-117">Gli orari di lavoro all'interno di ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="ed137-117">The working times within each day.</span></span>
    - <span data-ttu-id="ed137-118">Il fuso orario per la regola del calendario.</span><span class="sxs-lookup"><span data-stu-id="ed137-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="ed137-119">Se applicabile, è possibile specificare anche l'orario non lavorativo per la regola.</span><span class="sxs-lookup"><span data-stu-id="ed137-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="ed137-120">Applicazione di un modello di calendario a una risorsa</span><span class="sxs-lookup"><span data-stu-id="ed137-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="ed137-121">Nel menu **Risorse** , seleziona **Risorse**.</span><span class="sxs-lookup"><span data-stu-id="ed137-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="ed137-122">Dalla visualizzazione griglia, seleziona fino a 25 **Risorse prenotabili** per aggiornare.</span><span class="sxs-lookup"><span data-stu-id="ed137-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="ed137-123">Seleziona **Imposta calendario** e una finestra di dialogo ti chiederà un elenco di modelli di ore lavorative disponibili.</span><span class="sxs-lookup"><span data-stu-id="ed137-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="ed137-124">Seleziona il modello che vuoi utilizzare, quindi seleziona **Applica**.</span><span class="sxs-lookup"><span data-stu-id="ed137-124">Select the template you want to use, and then select **Apply**.</span></span>
