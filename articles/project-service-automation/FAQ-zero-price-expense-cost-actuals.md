---
title: Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo spese?
description: Risoluzione del problema relativo all'impostazione automatica su zero del prezzo per gli effettivi costo spese.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752638"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="babcd-103">Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo spese?</span><span class="sxs-lookup"><span data-stu-id="babcd-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="babcd-104">Queste domande frequenti si applicano agli effettivi spese dove la classe di transazione è impostata su Spesa e il tipo di transazione è Costo.</span><span class="sxs-lookup"><span data-stu-id="babcd-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="babcd-105">Risoluzione del problema relativo al tasso di costo degli effettivi costo spese</span><span class="sxs-lookup"><span data-stu-id="babcd-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="babcd-106">Passare alla voce di spesa correlata e verificare che nel campo Voce di spesa sia visualizzato un importo.</span><span class="sxs-lookup"><span data-stu-id="babcd-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="babcd-107">Se per la voce di spesa di origine non era visualizzato un importo, il problema è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="babcd-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="babcd-108">Per risolvere il problema, ricreare la voce di spesa con un importo valido e approvarla.</span><span class="sxs-lookup"><span data-stu-id="babcd-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
