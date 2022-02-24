---
title: Risoluzione dei prezzi di costo per stime e valori effettivi
description: Questo argomento fornisce informazioni su come vengono risolti i prezzi di costo per stime e valori effettivi.
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877317"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Risoluzione dei prezzi di costo per stime e valori effettivi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Per risolvere i prezzi di costo e il listino prezzi di costo per le stime e i valori effettivi, il sistema utilizza le informazioni nei campi **Data**, **Valuta** e **Unità contratto** del progetto correlato. Dopo che il listino prezzi di costo è stato risolto, l'applicazione risolve la tariffa di costo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Risoluzione delle tariffe di costo sulle righe di stima e valori effettivi per il tempo

Le righe di stima per tempo si riferiscono ai dettagli della riga di offerta e contratto per le assegnazioni di tempo e risorse di un progetto.

Dopo che un listino prezzi di costo è stato risolto, il sistema utilizza i campi **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse** nella riga di stima affinché il tempo corrisponda alle righe di prezzo del ruolo nel listino prezzi. Questa corrispondenza presuppone che tu stia utilizzando dimensioni di determinazione del prezzo predefinite per il costo del lavoro. Se hai configurato il sistema per abbinare i campi al posto o in aggiunta a **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, verrà utilizzata una combinazione diversa per recuperare una riga di prezzo del ruolo corrispondente. Se l'applicazione trova una riga di prezzo del ruolo con una tariffa di costo per la combinazione **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, questa riga è la tariffa di costo predefinita. Se l'applicazione non può corrispondere esattamente alla combinazione dei valori **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, recupererà le righe del prezzo del ruolo con un valore di ruolo corrispondente, ma avrà valori nulli per **Unità gestione risorse** e **Società di gestione risorse**. Dopo aver trovato un record di prezzo del ruolo corrispondente al valore del prezzo del ruolo corrispondente, il tasso di costo predefinito è quello di quel record. 

> [!NOTE]
> Se configuri una diversa priorità di **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse** oppure se hai altre dimensioni con priorità più alta, questo comportamento cambia di conseguenza. Il sistema recupera i record del prezzo del ruolo con valori che corrispondono a ciascuno dei valori delle dimensioni di determinazione dei prezzi in ordine di priorità con righe che hanno valori nulli per quelle dimensioni che arrivano per ultime nell'ordine di priorità.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Risoluzione delle tariffe di costo sulle righe di stima e valori effettivi per la spesa

Le righe di stima per spesa si riferiscono ai dettagli della riga di offerta e contratto per le righe di stima di spesa e spese di un progetto.

Dopo che un listino prezzi di costo è stato risolto, il sistema utilizza una combinazione dei campi **Categoria** e **Unità** nella riga di stima per affinché una spesa corrisponda alle righe **Prezzo categoria** nel listino prezzi risolto. Se il sistema trova una riga di prezzo di categoria con una tariffa di costo per la combinazione di campi **Categoria** e **Unità**, questa riga è la tariffa di costo predefinita. Se il sistema non può abbinare il valori **Categoria** e **Unità** o se è in grado di trovare una riga di prezzo di categoria corrispondente ma il metodo di determinazione del prezzo non è **Prezzo per unità**, per impostazione predefinita la tariffa di costo è impostata su zero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Risoluzione dei tassi di costo nelle righe effettive e di stima per Materiale

Le righe di stima per Materiale si riferiscono ai dettagli delle righe di offerta e delle voci di contratto per i materiali e alle righe di stima del materiale in un progetto.

Dopo che un listino prezzi di costo viene risolto, il sistema utilizza una combinazione dei campi **Prodotto** e **Unità** nella riga di stima per una stima del materiale da abbinare alle righe **Voci di listino** del listino risolto. Se il sistema trova una riga di prezzo del prodotto con un tasso di costo per la combinazione dei campi **Prodotto** e **Unità**, il tasso di costo viene impostato automaticamente. Se il sistema non può abbinare i valori **Prodotto** e **Unità**, il costo unitario predefinito è zero. Questa impostazione predefinita si verifica anche se è presente una riga di voce di listino corrispondente, ma il metodo di determinazione dei prezzi è basato su un costo standard o su un costo corrente non definito nel prodotto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
