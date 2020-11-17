---
title: Risoluzione dei prezzi di costo per stime e valori effettivi
description: Questo argomento fornisce informazioni su come vengono risolti i prezzi di costo per stime e valori effettivi.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119694"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Risoluzione dei prezzi di costo per stime e valori effettivi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Per risolvere i prezzi di costo e il listino prezzi di costo per le stime e i valori effettivi, il sistema utilizza le informazioni nei campi **Data**, **Valuta** e **Unità contratto** del progetto correlato. Dopo che il listino prezzi di costo è stato risolto, l'applicazione risolve la tariffa di costo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Risoluzione delle tariffe di costo sulle righe di stima e valori effettivi per il tempo

Le righe di stima per tempo si riferiscono ai dettagli della riga di offerta e contratto per le assegnazioni di tempo e risorse di un progetto.

Dopo che un listino prezzi di costo è stato risolto, il sistema utilizza i campi **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse** nella riga di stima affinché il tempo corrisponda alle righe di prezzo del ruolo nel listino prezzi. Questa corrispondenza presuppone che tu stia utilizzando dimensioni di determinazione del prezzo predefinite per il costo del lavoro. Se hai configurato il sistema per abbinare i campi al posto o in aggiunta a **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, verrà utilizzata una combinazione diversa per recuperare una riga di prezzo del ruolo corrispondente. Se l'applicazione trova una riga di prezzo del ruolo con una tariffa di costo per la combinazione **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, questa riga è la tariffa di costo predefinita. Se l'applicazione non può corrispondere ai valori **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse** recupera le righe di prezzo del ruolo con un ruolo corrispondente, eccetto i valori nulli di **Unità gestione risorse**. Quando un record di prezzo del ruolo corrispondente è disponibile, la tariffa di costo viene impostata per impostazione predefinita da quel record. 

> [!NOTE]
> Se configuri una diversa priorità di **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse** oppure se hai altre dimensioni con priorità più alta, questo comportamento cambia di conseguenza. Il sistema recupera i record del prezzo del ruolo con i valori che corrispondono a ciascuno dei valori della dimensione del prezzo in ordine di priorità con le righe che hanno valori nulli per quelle dimensioni che arrivano per ultime.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Risoluzione delle tariffe di costo sulle righe di stima e valori effettivi per la spesa

Le righe di stima per spesa si riferiscono ai dettagli della riga di offerta e contratto per le righe di stima di spesa e spese di un progetto.

Dopo che un listino prezzi di costo è stato risolto, il sistema utilizza una combinazione dei campi **Categoria** e **Unità** nella riga di stima per affinché una spesa corrisponda alle righe **Prezzo categoria** nel listino prezzi risolto. Se il sistema trova una riga di prezzo di categoria con una tariffa di costo per la combinazione di campi **Categoria** e **Unità**, questa riga è la tariffa di costo predefinita. Se il sistema non può abbinare il valori **Categoria** e **Unità** o se è in grado di trovare una riga di prezzo di categoria corrispondente ma il metodo di determinazione del prezzo non è **Prezzo per unità**, per impostazione predefinita la tariffa di costo è impostata su zero (0).
