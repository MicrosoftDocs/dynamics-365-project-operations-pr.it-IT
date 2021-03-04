---
title: Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo ora?
description: Risoluzione del problema relativo all'impostazione automatica su zero del prezzo per gli effettivi costo ora.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146263"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="e9b28-103">Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo ora?</span><span class="sxs-lookup"><span data-stu-id="e9b28-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e9b28-104">Queste domande frequenti si applicano agli effettivi dove la classe di transazione è impostata su Ora e il tipo di transazione è Costo.</span><span class="sxs-lookup"><span data-stu-id="e9b28-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="e9b28-105">I seguenti tre controlli consentono di risolvere il problema relativo all'impostazione automatica del prezzo su 0 degli effettivi costo ora.</span><span class="sxs-lookup"><span data-stu-id="e9b28-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="e9b28-106">Controllo 1: identificare il listino prezzi di costo per il progetto</span><span class="sxs-lookup"><span data-stu-id="e9b28-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="e9b28-107">Individuare il progetto nel campo del progetto dell'effettivo e quindi passare alla pagina del progetto.</span><span class="sxs-lookup"><span data-stu-id="e9b28-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="e9b28-108">Fare clic sul collegamento dell'unità contratto nel campo.</span><span class="sxs-lookup"><span data-stu-id="e9b28-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="e9b28-109">Nella pagina Unità contratto, verificare se l'unità contratto ha un listino prezzi nella griglia Listini prezzi di costo.</span><span class="sxs-lookup"><span data-stu-id="e9b28-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="e9b28-110">Se sono presenti più listini prezzi, il problema è stato isolato.</span><span class="sxs-lookup"><span data-stu-id="e9b28-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="e9b28-111">Project Service supporta un solo listino prezzi per unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="e9b28-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="e9b28-112">Rimuovere tutti i listini prezzi da questa entità fino a che non vi sia un solo listino prezzi allegato alla griglia Listini prezzi di costo dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="e9b28-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="e9b28-113">Se non sono presenti listini prezzi allegati all'unità organizzativa, prendere nota della valuta dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="e9b28-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="e9b28-114">Accedere a Project Service e quindi a Parametri e aprire la scheda Listini prezzi. Verificare se sono presenti listini prezzi con contesto impostato su Costo e con la valuta corrispondente alla valuta dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="e9b28-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="e9b28-115">Se non sono presenti listini prezzi che soddisfano quei criteri, il problema è stato isolato.</span><span class="sxs-lookup"><span data-stu-id="e9b28-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="e9b28-116">Verificare di disporre di almeno un listino prezzi il cui contesto è impostato su Costo e la cui valuta corrisponde alla valuta dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="e9b28-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="e9b28-117">Se sono presenti più listini prezzi che soddisfano quei criteri, continuare a leggere questo documento per eseguire ulteriori controlli.</span><span class="sxs-lookup"><span data-stu-id="e9b28-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="e9b28-118">Controllo 2: i listini prezzi identificati precedentemente sono validi per la data specifica dell'effettivo costo ora?</span><span class="sxs-lookup"><span data-stu-id="e9b28-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="e9b28-119">Affinché Project Service consideri un listino prezzi per l'impostazione automatica del prezzo, il listino prezzi deve essere applicabile per la data dell'effettivo costo ora.</span><span class="sxs-lookup"><span data-stu-id="e9b28-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="e9b28-120">Controllare quanto segue per verificare se i listini prezzi identificati precedentemente sono applicabili:</span><span class="sxs-lookup"><span data-stu-id="e9b28-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="e9b28-121">Verificare che i campi della data di inizio e della data di fine nella scheda Generale dei listini prezzi allegati non siano vuoti.</span><span class="sxs-lookup"><span data-stu-id="e9b28-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="e9b28-122">Se quei campi sono vuoti per i listini prezzi identificati in precedenza, il problema è stato isolato.</span><span class="sxs-lookup"><span data-stu-id="e9b28-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="e9b28-123">Prendere nota del campo della data di inizio dell'effettivo costo ora e controllare se qualsiasi listino prezzi identificato è applicabile per tale data.</span><span class="sxs-lookup"><span data-stu-id="e9b28-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="e9b28-124">Ad esempio, la data dell'effettivo costo ora deve rientrare nella data di inizio e nella data di fine sul listino prezzi.</span><span class="sxs-lookup"><span data-stu-id="e9b28-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="e9b28-125">Se non vi sono listini prezzi che coprono quella data per l'effettivo costo ora, il problema è stato isolato.</span><span class="sxs-lookup"><span data-stu-id="e9b28-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="e9b28-126">Modificare la data di inizio e quella di fine del listino prezzi per assicurarsi che il listino prezzi copra la data dell'effettivo costo ora.</span><span class="sxs-lookup"><span data-stu-id="e9b28-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="e9b28-127">Se vi sono più listini prezzi che coprono la data dell'effettivo costo ora, il problema è stato isolato.</span><span class="sxs-lookup"><span data-stu-id="e9b28-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="e9b28-128">È possibile risolvere questo problema modificando la data di inizio e quella di fine dei listini prezzi affinché sia presente un solo listino prezzi che copre la data dell'effettivo costo ora.</span><span class="sxs-lookup"><span data-stu-id="e9b28-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="e9b28-129">Se esiste un solo listino prezzi che copre la data dell'effettivo costo ora, passare al controllo successivo nel documento.</span><span class="sxs-lookup"><span data-stu-id="e9b28-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="e9b28-130">Dopo aver effettuato le correzioni necessarie, ricreare un inserimento ore, approvarlo e verificare che l'effettivo costo ora visualizzi un prezzo valido.</span><span class="sxs-lookup"><span data-stu-id="e9b28-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="e9b28-131">Controllo 3: esiste un prezzo nel listino prezzi per le dimensioni di determinazione dei prezzi dell'effettivo costo ora?</span><span class="sxs-lookup"><span data-stu-id="e9b28-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="e9b28-132">Se il controllo 1 e il controllo 2 sono stati completati correttamente, si dovrebbe ora disporre di un solo listino prezzi che è applicabile per la data dell'effettivo costo ora.</span><span class="sxs-lookup"><span data-stu-id="e9b28-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="e9b28-133">Aprire il listino prezzi e accedere alla scheda Prezzi ruolo. Assicurarsi che vi sia una riga nella griglia per le dimensioni di determinazione dei prezzi dell'effettivo costo ora.</span><span class="sxs-lookup"><span data-stu-id="e9b28-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="e9b28-134">Se non è disponibile alcuna riga nella griglia dei prezzi di ruolo per le dimensioni di determinazione dei prezzi dell'effettivo costo ora, il problema è stato isolato.</span><span class="sxs-lookup"><span data-stu-id="e9b28-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="e9b28-135">Creare una riga nella griglia dei prezzi di ruolo per le dimensioni di determinazione dei prezzi dell'effettivo costo ora.</span><span class="sxs-lookup"><span data-stu-id="e9b28-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="e9b28-136">Successivamente, ricreare un inserimento ore, approvarlo e verificare che l'effettivo costo ora visualizzi un prezzo valido.</span><span class="sxs-lookup"><span data-stu-id="e9b28-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="e9b28-137">Se non viene ancora visualizzato un prezzo valido per l'effettivo costo ora dopo aver eseguito i tre controlli descritti precedentemente, creare un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="e9b28-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



