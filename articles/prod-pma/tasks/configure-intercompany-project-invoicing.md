---
title: Configurare la fatturazione del progetto interaziendale
description: Questo argomento mostra come configurare la fatturazione del progetto tra due società della tua organizzazione.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001206"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="9e22d-103">Configurare la fatturazione del progetto interaziendale</span><span class="sxs-lookup"><span data-stu-id="9e22d-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e22d-104">Questo argomento mostra come configurare la fatturazione del progetto tra due società della tua organizzazione.</span><span class="sxs-lookup"><span data-stu-id="9e22d-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="9e22d-105">Questa attività utilizza il set di dati USSI.</span><span class="sxs-lookup"><span data-stu-id="9e22d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9e22d-106">Nel riquadro di spostamento, vai a **Moduli > Contabilità fornitori > Fornitori > Tutti i fornitori**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="9e22d-107">Nell'elenco **Tutti i fornitori**, trova e seleziona il record desiderato.</span><span class="sxs-lookup"><span data-stu-id="9e22d-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="9e22d-108">Nel riquadro Azioni seleziona **Generale**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="9e22d-109">Seleziona **Interaziendale**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="9e22d-110">Imposta **Attivo** su **Sì** per consentire la negoziazione interaziendale.</span><span class="sxs-lookup"><span data-stu-id="9e22d-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="9e22d-111">Nel campo **Società cliente**, inserisci o seleziona un valore.</span><span class="sxs-lookup"><span data-stu-id="9e22d-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="9e22d-112">Nel campo **Account personale**, inserisci o seleziona un valore.</span><span class="sxs-lookup"><span data-stu-id="9e22d-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="9e22d-113">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-113">Select **Save**.</span></span>
9. <span data-ttu-id="9e22d-114">Chiudi le pagine per tornare alla home page.</span><span class="sxs-lookup"><span data-stu-id="9e22d-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="9e22d-115">Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Parametri Gestione progetti e contabilità**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="9e22d-116">Seleziona la scheda **Interaziendale**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="9e22d-117">Sposta il cursore su **Sì** per abilitare la pianificazione delle risorse interaziendali e i fogli presenza.</span><span class="sxs-lookup"><span data-stu-id="9e22d-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="9e22d-118">Nell'elenco, contrassegna la riga selezionata.</span><span class="sxs-lookup"><span data-stu-id="9e22d-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="9e22d-119">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-119">Select **New**.</span></span>
15. <span data-ttu-id="9e22d-120">Nel campo **Persona giuridica mutuante**, inserisci o seleziona un valore.</span><span class="sxs-lookup"><span data-stu-id="9e22d-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="9e22d-121">Seleziona la casella di controllo **Accumula ricavi**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="9e22d-122">Nel campo **Categoria di foglio presenze predefinita**, inserisci o seleziona un valore.</span><span class="sxs-lookup"><span data-stu-id="9e22d-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="9e22d-123">Nel campo **Categoria di spesa predefinita**, inserisci o seleziona un valore.</span><span class="sxs-lookup"><span data-stu-id="9e22d-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="9e22d-124">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-124">Select **Save**.</span></span>
20. <span data-ttu-id="9e22d-125">Chiudi la pagina.</span><span class="sxs-lookup"><span data-stu-id="9e22d-125">Close the page.</span></span>
21. <span data-ttu-id="9e22d-126">Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Registrazione > Impostazioni registrazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="9e22d-127">Nel campo **Tipi di conto CoGe**, seleziona un'opzione.</span><span class="sxs-lookup"><span data-stu-id="9e22d-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="9e22d-128">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-128">Select **New**.</span></span>
24. <span data-ttu-id="9e22d-129">Nel campo **Account principale** della nuova riga, specifica i valori desiderati.</span><span class="sxs-lookup"><span data-stu-id="9e22d-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="9e22d-130">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-130">Select **Save**.</span></span>
26. <span data-ttu-id="9e22d-131">Chiudi la pagina.</span><span class="sxs-lookup"><span data-stu-id="9e22d-131">Close the page.</span></span>
27. <span data-ttu-id="9e22d-132">Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Prezzi > Prezzo di trasferimento**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="9e22d-133">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-133">Select **New**.</span></span>
29. <span data-ttu-id="9e22d-134">Nel campo **Data di validità**, inserisci una data.</span><span class="sxs-lookup"><span data-stu-id="9e22d-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="9e22d-135">Nel campo **Persona giuridica mutuante**, inserisci o seleziona un valore.</span><span class="sxs-lookup"><span data-stu-id="9e22d-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="9e22d-136">Nel campo **Modello prezzo di trasferimento**, seleziona un'opzione.</span><span class="sxs-lookup"><span data-stu-id="9e22d-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="9e22d-137">Nel campo **Prezzi**, inserisci un numero.</span><span class="sxs-lookup"><span data-stu-id="9e22d-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="9e22d-138">Seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="9e22d-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]