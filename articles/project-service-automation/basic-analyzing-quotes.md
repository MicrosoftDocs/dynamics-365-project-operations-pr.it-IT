---
title: Analisi delle offerte di progetto
description: In questo argomento vengono fornite informazioni sull'analisi delle offerte di progetto.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752587"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="41920-103">Analisi delle offerte di progetto</span><span class="sxs-lookup"><span data-stu-id="41920-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="41920-104">Dynamics 365 Project Service Automation analizza le offerte di progetto per stimare la redditività.</span><span class="sxs-lookup"><span data-stu-id="41920-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="41920-105">Inoltre, analizza l'allineamento dell'offerta alle aspettative dei clienti rispetto alla data di consegna o di completamento e al budget.</span><span class="sxs-lookup"><span data-stu-id="41920-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="41920-106">Analisi della redditività</span><span class="sxs-lookup"><span data-stu-id="41920-106">Profitability analysis</span></span>

<span data-ttu-id="41920-107">Project Service Automation analizza la redditività utilizzando il margine lordo e il margine lordo rettificato.</span><span class="sxs-lookup"><span data-stu-id="41920-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="41920-108">I margini lordi vengono calcolati mediante la formula seguente:</span><span class="sxs-lookup"><span data-stu-id="41920-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="41920-109">Il margine lordo rettificato viene calcolato mediante la formula seguente:</span><span class="sxs-lookup"><span data-stu-id="41920-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="41920-110">Se i valori del margine lordo e del margine lordo rettificato differiscono di un margine importante, molto del lavoro nell'offerta viene classificato come non addebitabile.</span><span class="sxs-lookup"><span data-stu-id="41920-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="41920-111">Analisi delle aspettative dei clienti</span><span class="sxs-lookup"><span data-stu-id="41920-111">Analysis of customer expectations</span></span>

<span data-ttu-id="41920-112">È possibile analizzare le offerte e generare grafici per le aspettative dei clienti in relazione a pianificazione e budget se si immettono valori nei campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="41920-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="41920-113">Il campo **Data consegna richiesta** nell'intestazione dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="41920-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="41920-114">Il campo **Budget cliente** per ogni riga dell'offerta (per le righe basate su progetto e le righe basate su prodotto).</span><span class="sxs-lookup"><span data-stu-id="41920-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="41920-115">L'analisi delle aspettative dei clienti rispetto alla pianificazione viene eseguita confrontando la data di fine più recente del dettaglio della riga di offerta alla data di consegna richiesta in tutte le righe di offerta nell'offerta.</span><span class="sxs-lookup"><span data-stu-id="41920-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="41920-116">L'analisi delle aspettative dei clienti rispetto al budget viene eseguita confrontando la somma del totale del budget del cliente all'importo indicato in tutte le righe dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="41920-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
