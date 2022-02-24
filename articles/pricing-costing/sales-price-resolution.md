---
title: Risolvere i prezzi di vendita per stime e valori effettivi
description: Questo argomento fornisce informazioni su come risolvere le tariffe di vendita per stime e valori effettivi.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9ce095723e8ac300caf7d11ae37b5c721b57795
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877450"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Risolvere i prezzi di vendita per stime e valori effettivi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Quando i prezzi di vendita su stime e valori effettivi vengono risolti in Dynamics 365 Project Operations, il sistema utilizza prima la data e la valuta dell'offerta o del contratto di progetto correlato per risolvere il listino prezzi di vendita. Dopo che il listino prezzi di vendita è stato risolto, il sistema risolve la tariffa di vendita o fatturazione.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Risolvere le tariffe di vendita sulle righe di stima e valori effettivi per il tempo

In Project Operations, le righe di stima per il tempo vengono utilizzate per indicare la riga di offerta e i dettagli della voce di contratto per il tempo e le assegnazioni di risorse nel progetto.

Dopo che un listino prezzi per le vendite è stato risolto, il sistema completa i seguenti passaggi per impostare la tariffa di fatturazione predefinita.

1. Il sistema utilizza i campi **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse** nella riga di stima affinché il tempo corrisponda alle righe di prezzo del ruolo nel listino prezzi risolto. Questa corrispondenza presuppone che vengano utilizzate dimensioni di determinazione del prezzo predefinite per le tariffe di fatturazione. Se hai configurato i prezzi in base ad altri campi al posto o in aggiunta a **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, verrà utilizzata tale combinazione per recuperare una riga di prezzo del ruolo corrispondente.
2. Se il sistema trova una riga di prezzo del ruolo con una tariffa di fatturazione per la combinazione di campi **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, questa è la tariffa di fatturazione predefinita.
3. Se il sistema non può corrispondere ai valori dei campi **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse** recupera le righe di prezzo del ruolo con un ruolo corrispondente, eccetto i valori nulli di **Unità risorsaUnit**. Dopo che il sistema trova un record di prezzo del ruolo corrispondente, imposta la tariffa di fatturazione da quel record. Questa corrispondenza presuppone una configurazione predefinita per la priorità relativa di **Ruolo** e **Unità gestione risorse** come dimensione di prezzi di vendita.

> [!NOTE]
> Se hai configurato una diversa priorità di **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse** oppure se hai altre dimensioni con priorità più alta, questo comportamento cambia di conseguenza. Il sistema recupera i record del prezzo del ruolo con i valori che corrispondono a ciascuno dei valori della dimensione del prezzo in ordine di priorità con le righe che hanno valori nulli per quelle dimensioni che arrivano per ultime.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Risolvere le tariffe di vendita sulle righe di stima e valori effettivi per la spesa

In Project Operations, le righe di stima per la spesa vengono utilizzate per indicare la riga di offerta e i dettagli della voce di contratto per le spese e le righe di stima di spesa nel progetto.

Dopo che un listino prezzi per le vendite è stato risolto, il sistema completa i seguenti passaggi per impostare il prezzo unitario di vendita.

1. Il sistema utilizza una combinazione dei campi **Categoria** e **Unità** nella riga di stima per affinché una spesa corrisponda alle righe prezzo di categoria nel listino prezzi risolto.
2. Se il sistema trova una riga di prezzo di categoria con una tariffa di vendita per la combinazione di campi **Categoria** e **Unità**, questa riga è la tariffa di vendita predefinita.
3. Se il sistema trova una riga di prezzo della categoria corrispondente, il metodo di determinazione del prezzo può essere utilizzato per impostare il prezzo di vendita predefinito. La tabella seguente mostra il comportamento predefinito del prezzo di spesa in Project Operations.

    | Contesto | Metodo di determinazione dei prezzi | Prezzo predefinito |
    | --- | --- | --- |
    | Stima | Prezzo unitario | Basato sulla riga di prezzo della categoria |
    | &nbsp; | Al costo | 0.00 |
    | &nbsp; | Ricarico sul costo | 0.00 |
    | Effettiva | Prezzo unitario | Basato sulla riga di prezzo della categoria |
    | &nbsp; | Al costo | In base al costo effettivo correlato |
    | &nbsp; | Ricarico sul costo | Applicando un ricarico come definito dalla riga del prezzo della categoria sulla tariffa di costo unitario del costo effettivo correlato |

4. Se il sistema non è in grado di abbinare i valori dei campi **Categoria** e **Unità** la tariffa di vendita è impostata su zero (0).

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Risolvere tariffe di vendita nelle righe effettive e di stima per Materiale

In Project Operations, le righe di stima per Materiale sono utilizzate per denotare la riga di offerta e dettagli delle voci di contratto per i materiali e le righe di stima materiale nel progetto.

Dopo che un listino prezzi per le vendite è stato risolto, il sistema completa i seguenti passaggi per impostare il prezzo unitario di vendita.

1. Il sistema utilizza la combinazione dei campi **Prodotto** e **Unità** nella riga di stima per la corrispondenza del materiale con le righe di voci di listino prezzi nel listino prezzi che è stato risolto.
2. Se il sistema trova una riga di voce di listino prezzi con una tariffa di vendita per la combinazione di campi **Prodotto** e **Unità** e il metodo di determinazione dei prezzi è **Importo valuta**, viene utilizzato il prezzo di vendita specificato nella riga del listino prezzi.
3. In caso di non corrispondenza con i valori dei campi **Prodotto** e **Unità**, il valore predefinito della tariffa di vendita è zero.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
