---
title: Ricevere gli articoli nell'ordine di acquisto dal requisito dell'articolo
description: Questo argomento spiega come ricevere articoli in un ordine di acquisto da un requisito articolo.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752581"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Ricevere gli articoli nell'ordine di acquisto dal requisito dell'articolo

[!include [task guide banner](../../includes/task-guide-banner.md)]

Questo argomento spiega come ricevere articoli in un ordine di acquisto da un requisito articolo.

Utilizzando un requisito articolo invece di una transazione articolo, è possibile pianificare la consegna appena prima che l'articolo venga effettivamente utilizzato, creare un ordine di acquisto, includere l'articolo nel quadro dell'accordo commerciale e includere il requisito articolo nella pianificazione della produzione. 

Questa attività utilizza il set di dati USSI.

1. Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Progetti > Tutti i progetti**.
2. Nell'elenco, seleziona il collegamento nella riga desiderata.
3. Nel riquadro Azioni seleziona **Piano**.
4. Seleziona **Requisiti articolo**.
5. Seleziona **Nuovo**.
6. Nella nuova riga, inserisci o seleziona un valore nel campo **Codice articolo**.
7. Nel campo **Quantità**, inserisci un numero.
8. Seleziona **Salva**.
9. Nel riquadro Azioni seleziona **Gestisci**.
10. Seleziona **Funzioni**.
11. Seleziona **Crea ordine di acquisto**.
12. Seleziona la casella di controllo **Includi tutto**.
13. Nel campo **Account fornitore**, inserisci o seleziona un valore.
14. Seleziona **OK**.
15. Nel riquadro di spostamento, vai a **Moduli > Contabilità fornitori > Ordini fornitore > Tutti gli ordini fornitore**.
16. Nell'elenco, seleziona il collegamento nella riga desiderata.
17. Nel riquadro Azioni seleziona **Acquista**.
18. Seleziona **Conferma**.
19. Nel riquadro Azioni seleziona **Ricevi**.
20. Seleziona **Entrata prodotti**.
21. Nel campo **Entrata prodotti**, digita un valore.
22. Seleziona **OK**.

