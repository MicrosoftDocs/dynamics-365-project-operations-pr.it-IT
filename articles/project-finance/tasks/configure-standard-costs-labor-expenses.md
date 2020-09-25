---
title: Configurare i costi standard per manodopera e spese
description: Questo argomento spiega come configurare i costi standard per la manodopera e le spese per un progetto.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752737"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurare i costi standard per manodopera e spese

[!include [task guide banner](../../includes/task-guide-banner.md)]

Questo argomento spiega come configurare i costi standard per la manodopera e le spese per un progetto. Questa attività utilizza il set di dati USSI.

1. Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Prezzi > Prezzo di costo (ora)**.
2. Seleziona **Nuovo**.
3. Nel campo **Data di validità**, inserisci una data.
4. Nel campo **Prezzo di costo**, inserisci un numero. Puoi configurare un prezzo di costo standard per la categoria del progetto oppure configurare un prezzo di costo per numero di lavoratore, numero di progetto, categoria, data o qualsiasi combinazione di questi. Il prezzo di costo applicato è il prezzo di costo con il livello di dettaglio più elevato.  
5. Seleziona **Salva**.
6. Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Prezzi > Prezzo di vendita (ora)**.
7. Seleziona **Nuovo**.
8. Nel campo **Data di validità**, inserisci una data.
9. Nel campo **Valido per**, seleziona un'opzione.
10. Nel campo **Prezzi**, inserisci un numero. Puoi configurare un prezzo di vendita standard per le transazioni orarie o per una categoria di progetto. Puoi inoltre configurare i prezzi di vendita per numero lavoratore, numero progetto, categoria, data transazione o qualsiasi combinazione di questi. Il prezzo di vendita effettivo, che viene applicato quando un lavoratore immette una transazione nel giornale di registrazione Ore, è il prezzo di vendita con il livello di dettaglio più elevato. Ad esempio, se vengono configurati sia un prezzo di vendita generale che un prezzo di vendita specifico del lavoratore, viene utilizzato il prezzo di vendita specifico del lavoratore.  
11. Seleziona **Salva**.
12. Chiudi la pagina.
13. Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Prezzi > Prezzo di costo (spesa)**.
14. Seleziona **Nuovo**.
15. Nel campo **Data di validità**, inserisci una data.
16. Nel campo **Prezzo di costo**, inserisci un numero. È possibile compilare più campi, ma questo è il minimo necessario per salvare il record.  
17. Seleziona **Salva**.
18. Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Imposta > Prezzi > Prezzo di vendita (spesa)**.
19. Seleziona **Nuovo**.
20. Nel campo **Data di validità**, inserisci una data.
21. Nel campo **Valido per**, seleziona un'opzione.
22. Nel campo **Prezzi**, inserisci un numero. Il prezzo di vendita effettivo, che viene applicato quando un lavoratore immette le transazioni nel giornale di registrazione delle spese, è il prezzo di vendita con il livello di dettaglio più elevato. Ad esempio, se vengono configurati sia un prezzo di vendita generale che un prezzo di vendita specifico del lavoratore, viene utilizzato il prezzo di vendita specifico del lavoratore.  
23. Seleziona **Salva**.
