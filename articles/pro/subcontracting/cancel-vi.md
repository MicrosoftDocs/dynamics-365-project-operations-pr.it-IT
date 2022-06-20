---
title: Annullare una fattura fornitore di progetto
description: Questo articolo spiega come annullare una fattura fornitore di progetto in Microsoft Dynamics 365 Project Operations e l'impatto finanziario dell'annullamento di una fattura fornitore di progetto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911555"
---
# <a name="cancel-a-project-vendor-invoice"></a>Annullare una fattura fornitore di progetto

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dopo che una fattura fornitore è stata confermata, non può essere modificata o eliminata. Se si è verificato un errore su una fattura fornitore che è stata confermata, è possibile utilizzare l'azione Annulla per annullare l'impatto della fattura fornitore e creare una nuova fattura fornitore.

Quando selezioni **Annulla** su una fattura fornitore, si verifica il seguente comportamento:

1. Lo stato della fattura fornitore viene aggiornato su **Annullato**.
2. La fattura fornitore annullata e i relativi record diventano di sola lettura e non possono essere modificati o eliminati.
3. Eventuali costi effettivi creati in base alle righe di fattura fornitore come parte della conferma della fattura fornitore vengono stornati.
4. Se eventuali costi effettivi sono stati collegati alle righe di fattura fornitore nell'ambito del processo di corrispondenza, la conferma della fattura fornitore originale li ha stornati. Durante l'annullamento della fattura fornitore, i costi effettivi vengono ricreati. Le origini puntano alle voci di tempo, spesa o utilizzo del materiale.
5. Dopo che la fattura fornitore è stata annullata, è possibile creare nuovamente giornali di registrazione correzioni, elaborare i richiami di inserimenti ore e annullare l'approvazione di valori effettivi per tempi, spese o materiali originali.

> [!NOTE]
> È possibile annullare solo le fatture fornitore di progetto confermate. Le fatture fornitore in altri stati non possono essere annullate.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
