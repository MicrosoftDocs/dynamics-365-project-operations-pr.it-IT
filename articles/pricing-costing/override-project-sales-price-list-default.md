---
title: Sostituire i listini prezzi di vendita di progetto
description: Questo argomento fornisce informazioni sulla creazione di listini prezzi di vendita personalizzati.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b26947822eb8e87b3b36fcde9c99c6ee69375aa942a5641112b9b1109dcaa26c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009581"
---
# <a name="override-project-sales-price-lists"></a>Sostituire i listini prezzi di vendita di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

## <a name="customer-specific-project-price-lists"></a>Listini prezzi di progetto specifici per il cliente

Gli accordi sui prezzi specifici del cliente possono essere impostati come listini prezzi di progetto in un record di conto in Dynamics 365 Project Operations.

Per impostare un listino prezzi di progetto specifico per il cliente, nell'area **Vendite** vai al record del conto.

1. Apri la pagina elenco **Conti**.
2. Individua e fai doppio clic su un record cliente per aprire la pagina dei dettagli del **conto**.
3. Nella scheda **Listini prezzi di progetto** seleziona **+ Nuovo listino prezzi di progetto**.
4. Nella pagina **Nuovo listino prezzi di progetto** seleziona un listino prezzi dal menu a discesa. Solo i listini prezzi che hanno il contesto impostato su **Vendite** e la cui valuta corrisponde alla valuta del conto sono inclusi.
5. Immetti un nome per l'associazione e seleziona **Salva**. Il listino prezzi di progetto specifico per il cliente è stato creato. Questo listino prezzi verrà utilizzato per i prezzi di progetto predefiniti sulle offerte di progetto o sui contratti creati per questo cliente in cui la data di creazione dell'offerta o del contratto di progetto rientra nella data di validità del listino prezzi.

## <a name="custom-pricing-on-project-quotes"></a>Prezzi personalizzati in offerte di progetto

Nelle offerte di progetto, è possibile avere prezzi di progetto che iniziano con un listino prezzi standard predefinito che viene impostato dal cliente o dai parametri del progetto.

Quando è necessario un prezzo personalizzato per il lavoro relativo al progetto su una particolare offerta, è possibile ottenerlo dall'entità associata ai listini prezzi di progetto.

Completa i seguenti passaggi per impostare il prezzo del progetto specifico dell'offerta.

1. Apri l'offerta di progetto e seleziona la scheda **Listini prezzi di progetto**.
2. Nella griglia secondaria seleziona **Crea determinazione dei prezzi personalizzata**.

Tutti i listini prezzi di progetto allegati all'offerta vengono copiati in nuovi listini prezzi. I nomi dei nuovi listini prezzi riflettono il nome dell'offerta con il timbro data-ora della creazione di questi listini prezzi.

Puoi utilizzare ciascuno di questi listini prezzi e aggiornare i prezzi di manodopera (prezzo del ruolo) e di spesa (prezzo della categoria). Questi prezzi saranno applicabili solo a questa offerta di progetto.

## <a name="price-lists-on-a-project-contract"></a>Listini prezzi in un contratto di progetto

In un contratto di progetto, il prezzo del progetto è sempre predefinito come un listino prezzi personalizzato con il nome del contratto e il timestamp della data di creazione aggiunto al nome. Questo è vero se il contratto è stato creato quando l'offerta è stata acquisita o se il contratto è stato creato da zero. Se necessario, è possibile rimuovere questa associazione al listino prezzi personalizzato e associare un listino prezzi standard al contratto di progetto.

Quando associ un listino prezzi standard ai listini prezzi di progetto su offerta o contratto, eventuali modifiche apportate ai prezzi nel listino prezzi avranno effetto su tutte le offerte e i contratti che utilizzano il listino prezzi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]