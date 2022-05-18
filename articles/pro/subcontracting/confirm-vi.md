---
title: Confermare una fattura fornitore di progetto
description: Questo argomento spiega come confermare una fattura fornitore di progetto in Microsoft Dynamics 365 Project Operations e l'impatto finanziario della conferma di una fattura fornitore di progetto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595733"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confermare una fattura fornitore di progetto

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dopo aver verificato tutte le righe di una fattura fornitore in Microsoft Dynamics 365 Project Operations, è possibile utilizzare l'azione Conferma per confermare la fattura fornitore.

Quando selezioni **Conferma** su una fattura fornitore, si verifica il seguente comportamento:

1. Lo stato della fattura fornitore viene aggiornato su **Confermato**.
2. La fattura fornitore confermata e i relativi record diventano di sola lettura e non possono essere modificati o eliminati.
3. Se eventuali costi effettivi fanno riferimento alla riga fattura fornitore nell'ambito del processo di corrispondenza, tutti i costi effettivi associati alla riga di fattura fornitore di riferimento vengono stornati.
4. I nuovi costi effettivi vengono creati utilizzando le informazioni nella riga di fattura fornitore.
5. Dopo che la fattura fornitore è stata confermata, non è più possibile creare giornali di registrazione correzioni, elaborare i richiami di inserimenti ore o annullare l'approvazione di valori effettivi per tempi, spese o materiali originali che sono stati stornati.

> [!NOTE]
> Se qualsiasi riga di una fattura fornitore ha uno stato di verifica diverso da **Completato**, la fattura fornitore non può essere confermata.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
