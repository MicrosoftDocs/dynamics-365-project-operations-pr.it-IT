---
title: Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo spese?
description: Risoluzione del problema relativo all'impostazione automatica su zero del prezzo per gli effettivi costo spese.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078897"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="82a79-103">Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo spese?</span><span class="sxs-lookup"><span data-stu-id="82a79-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="82a79-104">Queste domande frequenti si applicano agli effettivi spese dove la classe di transazione è impostata su Spesa e il tipo di transazione è Costo.</span><span class="sxs-lookup"><span data-stu-id="82a79-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="82a79-105">Risoluzione del problema relativo al tasso di costo degli effettivi costo spese</span><span class="sxs-lookup"><span data-stu-id="82a79-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="82a79-106">Passare alla voce di spesa correlata e verificare che nel campo Voce di spesa sia visualizzato un importo.</span><span class="sxs-lookup"><span data-stu-id="82a79-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="82a79-107">Se per la voce di spesa di origine non era visualizzato un importo, il problema è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="82a79-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="82a79-108">Per risolvere il problema, ricreare la voce di spesa con un importo valido e approvarla.</span><span class="sxs-lookup"><span data-stu-id="82a79-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
