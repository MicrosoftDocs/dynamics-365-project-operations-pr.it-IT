---
title: Disattivare listini prezzi
description: Questo argomento spiega come disattivare o rimuovere listini prezzi non utilizzati o datati.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001341"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="0ac9e-103">Disattivare listini prezzi</span><span class="sxs-lookup"><span data-stu-id="0ac9e-103">Deactivate price lists</span></span> 

<span data-ttu-id="0ac9e-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="0ac9e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0ac9e-105">Per rimuovere i listini prezzi datati o inutilizzati da Dynamics 365 Project Operations, è necessario completare due passaggi.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="0ac9e-106">Rimuovere o eliminare il listino prezzi da pagine specifiche.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="0ac9e-107">Disattivare o eliminare il listino prezzi da Listini prezzi attivi nella pagina **Listini prezzi**.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="0ac9e-108">Devi completare entrambi i passaggi per rimuovere completamente un listino prezzi.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="0ac9e-109">L'esecuzione unicamente del passaggio 2, che consiste nell'eliminare o disattivare direttamente il listino prezzi dalla visualizzazione Listini prezzi attivi, non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="0ac9e-110">È anche necessario eliminare l'associazione di questo listino prezzi da tutti i luoghi menzionati al passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="0ac9e-111">Eliminare il listino prezzi da pagine specifiche</span><span class="sxs-lookup"><span data-stu-id="0ac9e-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="0ac9e-112">Per eliminare un listino prezzi da Project Operations, visualizza le seguenti pagine:</span><span class="sxs-lookup"><span data-stu-id="0ac9e-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="0ac9e-113">Pagina **Parametri progetto** > scheda **Listini prezzi**</span><span class="sxs-lookup"><span data-stu-id="0ac9e-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="0ac9e-114">Pagina **Unità organizzativa** > griglia **Listino prezzi**</span><span class="sxs-lookup"><span data-stu-id="0ac9e-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="0ac9e-115">Pagina **Conto** > griglia **Listini prezzi di progetto**</span><span class="sxs-lookup"><span data-stu-id="0ac9e-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="0ac9e-116">Pagina **Offerte di progetto** > griglia **Listini prezzi di progetto**: si applica a tutte le offerte di progetto attive.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="0ac9e-117">Pagina **Contratti di progetto** > griglia **Listini prezzi di progetto**: si applica a tutti i contratti di progetto attivi.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="0ac9e-118">Per ogni pagina, devi selezionare il listino prezzi che desideri eliminare, quindi seleziona **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="0ac9e-119">Eliminare o disattivare il listino prezzi nella pagina Listini prezzi</span><span class="sxs-lookup"><span data-stu-id="0ac9e-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="0ac9e-120">Per eliminare un listino prezzi dai listini prezzi attivi, accedi a **Vendite** > **Clienti** > **Listini prezzi**.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="0ac9e-121">Seleziona il listino prezzi che vuoi eliminare e quindi seleziona **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="0ac9e-122">Se si fa riferimento al listino prezzi in qualsiasi transazione esistente, non potrai eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="0ac9e-123">In tal caso, puoi disattivare il listino prezzi di modo che non appaia in nessuna visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="0ac9e-124">Per disattivare il listino prezzi, selezionare di nuovo il listino prezzi, quindi seleziona **Disattiva**.</span><span class="sxs-lookup"><span data-stu-id="0ac9e-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
