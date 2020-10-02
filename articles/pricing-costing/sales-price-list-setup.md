---
title: Configurazione del listino prezzi di vendita
description: Questo argomento fornisce informazioni sui listini prezzi di vendita per la determinazione dei prezzi del progetto.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896466"
---
# <a name="sales-price-list-setup"></a>Configurazione del listino prezzi di vendita

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Per le offerte e i contratti di progetto, un listino prezzi di progetto include un modello di sostituzione dei prezzi differente rispetto a un listino prezzi di prodotto. In una riga di offerta basata su catalogo prodotti, puoi sostituire il prezzo per ruoli e categorie direttamente nella riga di offerta in quanto ogni riga di offerta punta esattamente a un articolo del catalogo. Tuttavia, in una riga di offerta basata su progetto, non puoi sostituire il prezzo per ruoli e categorie direttamente nella riga di offerta. Puoi usare il listino prezzi di progetto per utilizzare i due modelli di sostituzione distinti.

> [!NOTE]
> Ti consigliamo di avere un listino prezzi distinto per le risorse del progetto e gli articoli del catalogo, per via delle differenze di comportamento tra i due quando si sostituisce il metodo di determinazione dei prezzi.

Ognuna delle seguenti entità può avere uno o più listini prezzi di vendita associati per la determinazione dei prezzi di progetto:

- Cliente (account) 
- Opportunità 
- Offerta 
- Contratto di progetto

L'associazione di queste entità con un listino prezzi è indicata dai listini prezzi di progetto. Puoi associare uno o più listini prezzi alle entità di vendita Cliente, Opportunità, Offerta e Contratto di progetto.

Un listino prezzi di progetto predefinito non viene automaticamente inserito in un record del cliente. Tuttavia, puoi associare manualmente un listino prezzi di progetto al record del cliente. Devi comunque associare manualmente un listino prezzi di progetto solo quando hai un accordo di determinazione dei prezzi personalizzato con il cliente. 

Quando un listino prezzi di progetto è associato a un'entità di vendita, le informazioni seguenti vengono convalidate:

- Il listino prezzi ha un contesto **Vendite**. 
- La valuta del listino prezzi corrisponde alla valuta del cliente. 

In un contratto di progetto, il seguente ordine di precedenza viene utilizzato per impostare automaticamente i listini prezzi di progetto correlati:

1. Offerta
2. Opportunità
3. Cliente 
4. Impostazioni globali 

Quando un listino prezzi di progetto viene immesso per impostazione predefinita, il sistema verifica che la valuta corrisponde alla valuta del cliente e che i listini prezzi predefiniti immessi abbiano un contesto **Vendite**.

Puoi associare più listini prezzi di progetto alle entità Cliente, Opportunità, Offerta e Contratto di progetto. Questa funzionalità supporta prezzi predefiniti specifici della data per un contratto di progetto di lunga durata, dove puoi necessitare molteplici listini prezzi per gli aggiornamenti dei prezzi che si hanno a causa dell'inflazione. Tuttavia, se i listini prezzi associati all'entità Cliente, Opportunità, Offerta o Contratto di progetto hanno date di validità sovrapposte, i prezzi predefiniti possono non essere corretti. Pertanto, devi assicurarti che i listini prezzi di progetto con date di validità che si sovrappongono non siano associati a tali entità.
