---
title: Listini prezzi del prodotto
description: Questo argomento fornisce informazioni sui listini prezzi nei prezzi del catalogo utilizzati per offerte e contratti di progetto.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4feb7638dd7b6826e575d83457ae7f74ef6793bf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593249"
---
# <a name="product-price-lists"></a>Listini prezzi del prodotto

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

 In Project Operations, **Listini prezzi del prodotto** e le entità delle voci di listino correlate supportano la funzionalità per la determinazione dei prezzi dei prodotti nelle righe di offerta e nelle voci di contratto basate su progetto. Per i prodotti utilizzati nei progetti, vengono utilizzati i record delle voci di listino per i listini prezzi di progetto. 

I prodotti devono essere configurati in modo da avere costo e listini prezzi predefiniti nel catalogo prodotti. Utilizza il prezzo di listino, il costo standard e il costo corrente per configurare il costo e i prezzi di listino predefiniti. I prezzi di listino predefiniti sono utilizzati in una riga di offerta o in una voce di contratto di progetto solo quando il sistema non trova una riga di listino prezzi per quel prodotto nel listino prezzi prodotto dell'offerta o del contratto di progetto.

Il prezzo di costo delle righe del catalogo prodotti può essere modificato tra un'offerta e l'altra. Questa possibilità è importante, poiché se non tieni traccia in modo accurato dei costi, non puoi determinare i profitti operativi degli engagement di progetto. Per impostazione predefinita, il costo standard del prodotto è utilizzato come prezzo di costo. Tuttavia, il prezzo di costo predefinito può essere aggiornato nella riga di offerta se esiste un prezzo di costo differente per quell'offerta.

## <a name="price-list-items"></a>Voci di listino

Puoi aggiungere prodotti da un catalogo prodotti a differenti listini prezzi. Le righe di listino prezzi dei prodotti fanno sempre riferimento a una specifica unità. I prezzi di un prodotto nelle voci di listino possono essere configurati come importi in valuta. In alternativa, possono essere configurati come funzione di prezzo di listino, costo corrente o costo standard.

La funzionalità di determinazione dei prezzi supporta varie opzioni di arrotondamento quando i prezzi dei prodotti sono configurati come funzione di prezzo di listino, costo standard o costo corrente. Oltre a beneficiare di vari metodi di determinazione dei prezzi e delle opzioni di arrotondamento, puoi associare elenchi sconti a voci di listino. 

 
## <a name="default-product-price-list"></a>Listino prezzi prodotto predefinito
Ogni record cliente presente un campo **Listino prezzi predefinito** in cui puoi specificare un listino prezzi che corrisponde alla valuta del cliente. Un valore predefinito non viene automaticamente immesso in questo campo. Se esiste un contratto sui prezzi personalizzato con uno specifico cliente, puoi utilizzare questo campo per associare un listino prezzi a quel cliente.

Le entità Opportunità, Offerta e Contratto di progetto utilizzano l'ordine seguente per immettere listini prezzi prodotto predefiniti. Lo stesso ordine viene utilizzato per i listini prezzi progetto.

1.  Offerta
2.  Opportunità
3.  Cliente
4.  Impostazioni globali 

Per impostazione predefinita, il campo **Prodotto** nella riga di offerta elenca tutti i prodotti attivi nel listino prezzi prodotto dell'offerta. Se un prodotto è stato disattivato, o se è un prodotto bozza, non è elencato anche se è presente nel listino prezzi. 

Le righe del catalogo prodotti vengono aggiunte come righe fattura nella prima fattura creata per un contratto di progetto. In una bozza di fattura, queste righe fattura possono essere eliminate. In tal caso, le righe sono visualizzate in una fattura successiva fino a che non vengono fatturate o fino a che la fattura non viene inviata al cliente. Non è possibile fatturare una quantità parziale di una riga fattura prodotto. Quando le righe prodotto del contratto di progetto sono fatturate, vengono creati dei valori effettivi. Tuttavia, questi valori effettivi non sono collegati all'entità progetto correlata. In altre parole le voci di contratto di progetto basate su prodotto sono indipendenti da qualsiasi utilizzo basato su progetto. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
