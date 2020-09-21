---
title: Disattivare una dimensione di determinazione dei prezzi
description: In questo argomento viene descritto come configurare dimensioni di determinazione dei prezzi nella soluzione Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752684"
---
# <a name="turn-off-a-pricing-dimension"></a>Disattivare una dimensione di determinazione dei prezzi

È possibile che sia necessario esaminare e aggiornare regolarmente la strategia di determinazione dei prezzi dopo alcuni anni. L'aggiornamento potrebbe richiedere la disattivazione di una dimensione di determinazione dei prezzi esistente e la creazione di una nuova dimensione. Ad esempio, è possibile che in precedenza si siano determinati i prezzi per **Ruolo**, ma che ora si intenda farlo per **Esperienza di lavoro**. Ciò può richiedere la disattivazione di **Ruolo** come dimensione di determinazione dei prezzi e la creazione di **Esperienza di lavoro** come nuova dimensione di determinazione dei prezzi. 

Per disattivare la dimensione di determinazione dei prezzi, indipendentemente dal fatto che sia predefinita o personalizzata, impostare i campi **Vendite applicabili a** e **Costo applicabile a** della dimensione di determinazione dei prezzi su **No**.

Tuttavia, quando si esegue tale operazione, potrebbe essere visualizzato il messaggio di errore seguente:

![Errore processo aziendale probabile quando si disattiva una dimensione di determinazione dei prezzi](media/Business-Process-Error.png)


Questo messaggio di errore indica che vi sono record di prezzi impostati precedentemente per la dimensione che si sta disattivando. Tutti i record **Prezzo ruolo** e **Ricarico prezzo ruolo** che fanno riferimento a una dimensione devono essere eliminati prima di impostare l'applicabilità della dimensione su **No**. Tale regola si applica alle dimensioni di determinazione dei prezzi predefinite e a quelle personalizzate eventualmente create. Il motivo di questa convalida è dovuto al fatto che Project Service presenta un vincolo secondo il quale ogni record **Prezzo ruolo** deve avere una combinazione univoca di dimensioni. Ad esempio, in un listino denominato **Tasso di costo USA 2018**, si hanno le seguenti righe **Prezzo ruolo**. 

| Titolo standard         | Unità organizzativa    |Unità   |Prezzo  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Sistemista|Contoso US|Ora| 100|USD|
| Sistemista esperto|Contoso US|Ora| 150| USD|


Quando si disattiva **Titolo standard** come dimensione di determinazione dei prezzi e il motore di determinazione dei prezzi di Project Service cerca un prezzo, questo utilizzerà solo il valore **Unità organizzativa** del contesto di input. Se l'**unità organizzativa** del contesto di input è "Contoso US", il risultato sarà non deterministico in quanto entrambe le righe corrisponderanno. Per evitare questo scenario, quando si creano record **Prezzo ruolo**, Project Service verifica che la combinazione di dimensioni è univoca. Se la dimensione viene disattivata dopo la creazione dei record **Prezzo ruolo**, il vincolo può essere violato. Pertanto, prima di disattivare una dimensione, è necessario eliminare tutte le righe **Ricarico prezzo ruolo** e **Prezzo ruolo** in cui è presente il valore della dimensione.

