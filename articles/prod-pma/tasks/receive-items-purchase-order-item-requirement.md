---
title: Ricevere gli articoli nell'ordine di acquisto dal requisito dell'articolo
description: Questo argomento spiega come ricevere articoli in un ordine di acquisto da un requisito articolo.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079043"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Ricevere gli articoli nell'ordine di acquisto dal requisito dell'articolo

[!include [banner](../../includes/banner.md)]

Questo argomento spiega come ricevere articoli in un ordine di acquisto da un requisito articolo.

Utilizzando un requisito articolo invece di una transazione articolo, è possibile pianificare la consegna appena prima che l'articolo venga effettivamente utilizzato, creare un ordine di acquisto, includere l'articolo nel quadro dell'accordo commerciale e includere il requisito articolo nella pianificazione della produzione. 

Questa attività utilizza il set di dati USSI.

1. Nel riquadro di spostamento vai a **Moduli > Gestione progetti e contabilità > Progetti > Tutti i progetti**.
2. Nell'elenco, seleziona il collegamento nella riga desiderata.
3. Nel riquadro Azioni seleziona **Piano**.
4. Seleziona **Requisiti articolo**.
5. Seleziona **Nuovo**.
6. Nella nuova riga, inserisci o seleziona un valore nel campo **Codice articolo**.
7. Nel campo **Quantità** , inserisci un numero.
8. Seleziona **Salva**.
9. Nel riquadro Azioni seleziona **Gestisci**.
10. Seleziona **Funzioni**.
11. Seleziona **Crea ordine di acquisto**.
12. Seleziona la casella di controllo **Includi tutto**.
13. Nel campo **Account fornitore** , inserisci o seleziona un valore.
14. Seleziona **OK**.
15. Nel riquadro di spostamento, vai a **Moduli > Contabilità fornitori > Ordini fornitore > Tutti gli ordini fornitore**.
16. Nell'elenco, seleziona il collegamento nella riga desiderata.
17. Nel riquadro Azioni seleziona **Acquista**.
18. Seleziona **Conferma**.
19. Nel riquadro Azioni seleziona **Ricevi**.
20. Seleziona **Entrata prodotti**.
21. Nel campo **Entrata prodotti** , digita un valore.
22. Seleziona **OK**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]