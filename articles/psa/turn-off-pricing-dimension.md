---
title: Disattivare una dimensione di determinazione dei prezzi
description: In questo argomento viene descritto come configurare dimensioni di determinazione dei prezzi nella soluzione Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078961"
---
# <a name="turn-off-a-pricing-dimension"></a>Disattivare una dimensione di determinazione dei prezzi

È possibile che sia necessario esaminare e aggiornare regolarmente la strategia di determinazione dei prezzi dopo alcuni anni. L'aggiornamento potrebbe richiedere la disattivazione di una dimensione di determinazione dei prezzi esistente e la creazione di una nuova dimensione. Ad esempio, è possibile che in precedenza si siano determinati i prezzi per **Ruolo** , ma che ora si intenda farlo per **Esperienza di lavoro**. Ciò può richiedere la disattivazione di **Ruolo** come dimensione di determinazione dei prezzi e la creazione di **Esperienza di lavoro** come nuova dimensione di determinazione dei prezzi. 

Per disattivare la dimensione di determinazione dei prezzi, indipendentemente dal fatto che sia predefinita o personalizzata, impostare i campi **Vendite applicabili a** e **Costo applicabile a** della dimensione di determinazione dei prezzi su **No**.

Tuttavia, quando si esegue tale operazione, potrebbe essere visualizzato il messaggio di errore seguente:

![Errore processo aziendale probabile quando si disattiva una dimensione di determinazione dei prezzi](media/Business-Process-Error.png)


Questo messaggio di errore indica che vi sono record di prezzi impostati precedentemente per la dimensione che si sta disattivando. Tutti i record **Prezzo ruolo** e **Ricarico prezzo ruolo** che fanno riferimento a una dimensione devono essere eliminati prima di impostare l'applicabilità della dimensione su **No**. Tale regola si applica alle dimensioni di determinazione dei prezzi predefinite e a quelle personalizzate eventualmente create. Il motivo di questa convalida è dovuto al fatto che Project Service presenta un vincolo secondo il quale ogni record **Prezzo ruolo** deve avere una combinazione univoca di dimensioni. Ad esempio, in un listino denominato **Tasso di costo USA 2018** , si hanno le seguenti righe **Prezzo ruolo**. 

| Titolo standard         | Unità organizzativa    |Unità   |Prezzo  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Sistemista|Contoso US|Ora| 100|USD|
| Sistemista esperto|Contoso US|Ora| 150| USD|


Quando si disattiva **Titolo standard** come dimensione di determinazione dei prezzi e il motore di determinazione dei prezzi di Project Service cerca un prezzo, questo utilizzerà solo il valore **Unità organizzativa** del contesto di input. Se l' **unità organizzativa** del contesto di input è "Contoso US", il risultato sarà non deterministico in quanto entrambe le righe corrisponderanno. Per evitare questo scenario, quando si creano record **Prezzo ruolo** , Project Service verifica che la combinazione di dimensioni è univoca. Se la dimensione viene disattivata dopo la creazione dei record **Prezzo ruolo** , il vincolo può essere violato. Pertanto, prima di disattivare una dimensione, è necessario eliminare tutte le righe **Ricarico prezzo ruolo** e **Prezzo ruolo** in cui è presente il valore della dimensione.
