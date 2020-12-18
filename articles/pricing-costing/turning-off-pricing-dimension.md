---
title: Disattivare una dimensione di determinazione dei prezzi
description: In questo argomento vengono fornite informazioni su come disattivare le dimensioni di determinazione dei prezzi.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650054"
---
# <a name="turning-off-a-pricing-dimension"></a>Disattivare una dimensione di determinazione dei prezzi

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

È possibile che sia necessario esaminare e aggiornare regolarmente la strategia di determinazione dei prezzi dopo alcuni anni. L'aggiornamento potrebbe richiedere la disattivazione di una dimensione di determinazione dei prezzi esistente e la creazione di una nuova dimensione. Ad esempio, è possibile che in precedenza si siano determinati i prezzi per **Ruolo**, ma che ora si intenda farlo per **Esperienza di lavoro**. Ciò può richiedere la disattivazione di **Ruolo** come dimensione di determinazione dei prezzi e la creazione di **Esperienza di lavoro** come nuova dimensione di determinazione dei prezzi. 

Per disattivare la dimensione di determinazione dei prezzi, indipendentemente dal fatto che sia predefinita o personalizzata, impostare i campi **Vendite applicabili a** e **Costo applicabile a** della dimensione di determinazione dei prezzi su **No**.

Tuttavia, quando esegui questa operazione, potresti ricevere il messaggio di errore **La dimensione di determinazione dei prezzi non può essere aggiornata o eliminata se sono presenti record di prezzo associati.**

![Errore processo aziendale probabile quando si disattiva una dimensione di determinazione dei prezzi](media/Business-Process-Error.png)

Questo messaggio di errore indica che vi sono record di prezzi impostati precedentemente per la dimensione che si sta disattivando. Tutti i record **Prezzo ruolo** e **Ricarico prezzo ruolo** che fanno riferimento a una dimensione devono essere eliminati prima di impostare l'applicabilità della dimensione su **No**. Tale regola si applica alle dimensioni di determinazione dei prezzi predefinite e a quelle personalizzate eventualmente create. Il motivo di questa convalida è dovuto al fatto che ogni record **Prezzo ruolo** deve avere una combinazione univoca di dimensioni. Ad esempio, in un listino denominato **Tasso di costo USA 2018**, si hanno le seguenti righe **Prezzo ruolo**. 

| Titolo standard         | Unità organizzativa    |Unità   |Prezzo  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Sistemista|Contoso US|Ora| 100|USD|
| Sistemista esperto|Contoso US|Ora| 150| USD|


Quando si disattiva **Titolo standard** come dimensione di determinazione dei prezzi e il motore di determinazione dei prezzi cerca un prezzo, questo utilizzerà solo il valore **Unità organizzativa** del contesto di input. Se l'**unità organizzativa** del contesto di input è "Contoso US", il risultato sarà non deterministico in quanto entrambe le righe corrisponderanno. Per evitare questo scenario, quando si creano record **Prezzo ruolo**, il sistema verifica che la combinazione di dimensioni è univoca. Se la dimensione viene disattivata dopo la creazione dei record **Prezzo ruolo**, il vincolo può essere violato. Pertanto, prima di disattivare una dimensione, è necessario eliminare tutte le righe **Ricarico prezzo ruolo** e **Prezzo ruolo** in cui è presente il valore della dimensione.
