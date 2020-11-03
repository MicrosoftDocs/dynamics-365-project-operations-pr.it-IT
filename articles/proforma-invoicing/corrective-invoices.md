---
title: Fatture corrette
description: In questo argomento vengono fornite informazioni sulle fatture corrette.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079044"
---
# <a name="corrected-invoices"></a>Fatture corrette

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Le fatture confermate possono essere modificate. Quando modifichi una fattura confermata, viene creata una bozza della fattura corretta. Poiché si presuppone che tu voglia stornare tutte le transazioni e quantità dalla fattura originale, questa fattura corretta include tutte le transazioni della fattura originale e tutte le relative quantità sono pari a zero (0).

Se alcune transazioni non richiedono la correzione, puoi rimuoverle dalla bozza di fattura correttiva. Per stornare o restituire solo una quantità parziale, puoi modificare il campo Quantità nel dettaglio della riga. Se apri il dettaglio di riga fattura, puoi vedere la quantità della fattura originale. Puoi quindi modificare la quantità della fattura corrente di modo che sia inferiore o superiore alla quantità della fattura originale.

Quando confermi una fattura correttiva, il valore effettivo delle vendite fatturate originali viene stornato e viene creato un nuovo valore effettivo di vendite fatturate. Se la quantità è stata ridotta, la differenza genererà anche la creazione di un nuovo valore effettivo delle vendite. Ad esempio, se lea vendita fatturata originale era per otto ore e il dettaglio di riga di fattura corretta presenta una quantità ridotta di sei ore, la riga delle vendite fatturate originali viene stornata e due nuovi valori effettivi vengono creati:

- Un valore effettivo delle vendite fatturate per sei ore.
- Un valore effettivo delle vendite non fatturate per le due ore rimanenti. Questa transazione può essere fatturata successivamente o contrassegnata come non addebitale, a seconda delle negoziazioni con il cliente.
