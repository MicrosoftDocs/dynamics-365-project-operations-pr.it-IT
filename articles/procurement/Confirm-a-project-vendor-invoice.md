---
title: Confermare le fattura fornitore di progetto
description: Questo articolo spiega come confermare una fattura fornitore di progetto in Microsoft Dynamics 365 Project Operations e descrive l'impatto finanziario della conferma di una fattura fornitore di progetto.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475426"
---
# <a name="confirm-project-vendor-invoices"></a>Confermare le fattura fornitore di progetto

_ **Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati

Quando il parametro **Conferma manuale del PM necessaria** è abilitato, le fatture fornitore create in Microsoft Dataverse hanno lo stato **Bozza**. Le fatture fornitore create in questo modo devono essere riviste e confermate manualmente. Quando il parametro **Conferma manuale del PM necessaria** è disabilitato, le fatture fornitore create in Dataverse vengono confermate automaticamente. Non sono richieste altre azioni. 

Dopo aver verificato tutte le righe di una fattura fornitore in  Dynamics 365 Project Operations, seleziona **Conferma** per confermare la fattura fornitore.

Quando selezioni **Conferma** su una fattura fornitore, si verifica il seguente comportamento:

1. Lo stato della fattura fornitore viene aggiornato su **Confermato**.
1. La fattura fornitore confermata e i relativi record diventano di sola lettura e non possono essere modificati o eliminati.
1. Se eventuali costi effettivi fanno riferimento alla riga fattura fornitore nell'ambito del processo di corrispondenza, tutti i costi effettivi associati alla riga di fattura fornitore di riferimento vengono stornati.
1. I nuovi costi effettivi vengono creati utilizzando le informazioni nella riga di fattura fornitore.
1. Non è più possibile creare giornali di registrazione correzioni, elaborare i richiami di inserimenti ore o annullare l'approvazione di valori effettivi per tempi, spese o materiali originali che sono stati stornati.
1. In Dynamics 365 Finance, il valore **Costo progetto** viene aggiornato utilizzando il giornale di integrazione di Project e l'account di integrazione Approvvigionamento è *invertito* dopo la registrazione del giornale di integrazione di Project.

> [!NOTE]
> Se qualsiasi riga di una fattura fornitore ha uno stato di verifica diverso da **Completato**, la fattura fornitore non può essere confermata.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
