---
title: Risoluzione dei prezzi di costo in stime e valori effettivi - semplice
description: Questo argomento fornisce informazioni su come vengono risolti i prezzi di costo su stime e valori effettivi.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bbb79fdc5c68d67530b5aa34fe6105211eff1768
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274554"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Risoluzione dei prezzi di costo in stime e valori effettivi - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Per risolvere i prezzi di costo e il listino prezzi di costo per le stime e i valori effettivi, il sistema utilizza le informazioni nei campi **Data**, **Valuta** e **Unità contratto** del progetto correlato. Dopo che il listino prezzi di costo è stato risolto, l'applicazione risolve la tariffa di costo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Risoluzione delle tariffe di costo sulle righe di stima e valori effettivi per il tempo

Le righe di stima per tempo si riferiscono ai dettagli della riga di offerta e contratto per le assegnazioni di tempo e risorse di un progetto.

Dopo che un listino prezzi di costo è stato risolto, i campo **Ruolo** e **Unità risorse** nella riga di stima per Ora vengono confrontati con le righe di prezzo del ruolo nel listino prezzi. Questa corrispondenza presuppone che tu stia utilizzando le dimensioni di prezzo standard per il costo del lavoro. Se hai configurato il sistema per abbinare i campi al posto o in aggiunta a **Ruolo** e **Unità gestione risorse**, verrà utilizzata una combinazione diversa per recuperare una riga di prezzo del ruolo corrispondente. Se l'applicazione trova una riga di prezzo del ruolo con una tariffa di costo per la combinazione **Ruolo** e **Unità gestione risorse**, questa riga è la tariffa di costo predefinita. Se l'applicazione non può corrispondere ai valori **Ruolo** e **Unità gestione risorse** recupera le righe di prezzo del ruolo con un ruolo corrispondente, eccetto i valori nulli di **Unità gestione risorse**. Quando un record di prezzo del ruolo corrispondente è disponibile, la tariffa di costo viene impostata per impostazione predefinita da quel record. 

> [!NOTE]
> Se configuri una diversa priorità di **Ruolo** e **Unità gestione risorse** oppure se hai altre dimensioni con priorità più alta, questo comportamento cambia di conseguenza. Il sistema recupera i record del prezzo del ruolo con i valori che corrispondono a ciascuno dei valori della dimensione del prezzo in ordine di priorità con le righe che hanno valori nulli per quelle dimensioni che arrivano per ultime.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Risoluzione delle tariffe di costo sulle righe di stima e valori effettivi per la spesa

Le righe di stima per spesa si riferiscono ai dettagli della riga di offerta e contratto per le righe di stima di spesa e spese di un progetto.

Dopo che un listino prezzi di costo è stato risolto, il sistema utilizza una combinazione dei campi **Categoria** e **Unità** nella riga della stima delle spese da confrontare con le righe **Prezzo di categoria** del listino prezzi risolto. Se il sistema trova una riga di prezzo di categoria con una tariffa di costo per la combinazione di campi **Categoria** e **Unità**, questa riga è la tariffa di costo predefinita. Se il sistema non può abbinare i valori **Categoria** e **Unità** o se è in grado di trovare una riga di prezzo della categoria corrispondente ma il metodo di determinazione del prezzo non è **Prezzo per unità**, il tasso di costo predefinito è zero (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]