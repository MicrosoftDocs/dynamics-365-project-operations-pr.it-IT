---
title: Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo spese?
description: Risoluzione del problema relativo all'impostazione automatica su zero del prezzo per gli effettivi costo spese.
author: rumant
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
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992791"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="41eab-103">Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo spese</span><span class="sxs-lookup"><span data-stu-id="41eab-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="41eab-104">Queste domande frequenti si applicano agli effettivi spese dove la classe di transazione è impostata su Spesa e il tipo di transazione è Costo.</span><span class="sxs-lookup"><span data-stu-id="41eab-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="41eab-105">Risoluzione del problema relativo al tasso di costo degli effettivi costo spese</span><span class="sxs-lookup"><span data-stu-id="41eab-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="41eab-106">Passare alla voce di spesa correlata e verificare che nel campo Voce di spesa sia visualizzato un importo.</span><span class="sxs-lookup"><span data-stu-id="41eab-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="41eab-107">Se per la voce di spesa di origine non era visualizzato un importo, il problema è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="41eab-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="41eab-108">Per risolvere il problema, ricreare la voce di spesa con un importo valido e approvarla.</span><span class="sxs-lookup"><span data-stu-id="41eab-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]