---
title: Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo spese?
description: Risoluzione del problema relativo all'impostazione automatica su zero del prezzo per gli effettivi costo spese.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122123"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="d704a-103">Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo spese?</span><span class="sxs-lookup"><span data-stu-id="d704a-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d704a-104">Queste domande frequenti si applicano agli effettivi spese dove la classe di transazione è impostata su Spesa e il tipo di transazione è Costo.</span><span class="sxs-lookup"><span data-stu-id="d704a-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="d704a-105">Risoluzione del problema relativo al tasso di costo degli effettivi costo spese</span><span class="sxs-lookup"><span data-stu-id="d704a-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="d704a-106">Passare alla voce di spesa correlata e verificare che nel campo Voce di spesa sia visualizzato un importo.</span><span class="sxs-lookup"><span data-stu-id="d704a-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="d704a-107">Se per la voce di spesa di origine non era visualizzato un importo, il problema è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="d704a-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="d704a-108">Per risolvere il problema, ricreare la voce di spesa con un importo valido e approvarla.</span><span class="sxs-lookup"><span data-stu-id="d704a-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
