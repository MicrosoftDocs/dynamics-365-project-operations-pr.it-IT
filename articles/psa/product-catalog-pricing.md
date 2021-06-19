---
title: Prezzi del catalogo prodotti
description: In questo argomento vengono fornite informazioni sui prezzi del catalogo prodotti in Dynamics 365 Project Service Automation (PSA).
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 148f52f74ee64c2ee218dda3b09e1188e70217b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009216"
---
# <a name="product-catalog-pricing"></a>Prezzi del catalogo prodotti 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Le entità Listini prezzi e Voce di listino supportano i prezzi del catalogo prodotti. In genere, questa funzionalità è utilizzata per le righe basate su catalogo delle offerte e dei contratti di progetto.

Per le righe basate su progetto, un contratto rappresenta la transazione dopo che questa è stata acquisita. Poiché il processo di negoziazione in genere precede l'acquisizione, i prezzi associati all'offerta sono sempre copiati così come sono in un nuovo listino prezzi e associati al contratto. Questo nuovo listino prezzi non può essere modificato al di fuori dall'ambito del contratto. Questa limitazione consente di proteggere il tariffario pubblicitario concordato da qualsiasi modifica dei prezzi apportata nel listino prezzi master.

I prodotti devono essere configurati in modo da avere costo e listini prezzi predefiniti nel catalogo prodotti. Devi utilizzare il prezzo di listino, il costo standard e il costo corrente per configurare il costo e i prezzi di listino predefiniti. I prezzi di listino predefiniti sono utilizzati in una riga di offerta o in una voce di contratto di progetto solo quando il sistema non trova una riga di listino prezzi per quel prodotto nel listino prezzi prodotto dell'offerta o del contratto di progetto.

Il prezzo di costo delle righe del catalogo prodotti può essere modificato tra un'offerta e l'altra. Questa possibilità è importante, poiché se non tieni traccia in modo accurato dei costi, non puoi determinare i profitti operativi degli engagement di progetto. Per impostazione predefinita, il costo standard del prodotto è utilizzato come prezzo di costo. Tuttavia, il prezzo di costo predefinito può essere aggiornato nella riga di offerta se esiste un prezzo di costo differente per quell'offerta.

## <a name="price-list-items"></a>Voci di listino

Puoi aggiungere prodotti da un catalogo prodotti a differenti listini prezzi. Le righe di listino prezzi dei prodotti fanno sempre riferimento a una specifica unità. I prezzi di un prodotto nelle voci di listino possono essere configurati come importi in valuta. In alternativa, possono essere configurati come funzione di prezzo di listino, costo corrente o costo standard.

PSA supporta varie opzioni di arrotondamento quando i prezzi sono configurati come funzione di prezzo di listino, costo standard o costo corrente. Oltre a beneficiare di vari metodi di determinazione dei prezzi e delle opzioni di arrotondamento, puoi associare elenchi sconti a voci di listino. 

> ![Aggiungere prodotti da un catalogo a differenti listini prezzi](media/basic-guide-16.png)

Quando crei un nuovo listino prezzi personalizzato per un'offerta selezionando **Crea determinazione dei prezzi personalizzata** nella pagina **Offerta di progetto**, PSA crea una copia del listino prezzi e il campo **Entità** nell'intestazione del nuovo listino prezzi è impostato su **Entità vendite**. Il nome del nuovo listino prezzi viene aggiunto al nome dell'offerta e a un timestamp. Puoi anche utilizzare il nome del nuovo listino prezzi e il nome dell'offerta in flussi di lavoro personalizzati per avviare ulteriori analisi e approvazioni delle offerte che utilizzano prezzi personalizzati.

 
## <a name="default-product-price-list"></a>Listino prezzi prodotto predefinito
Ogni record cliente presente un campo **Listino prezzi predefinito** in cui puoi specificare un listino prezzi che corrisponde alla valuta del cliente. In PSA, un valore predefinito non viene automaticamente immesso in questo campo. Se esiste un contratto sui prezzi personalizzato con uno specifico cliente, puoi utilizzare questo campo per associare un listino prezzi a quel cliente.

Le entità Opportunità, Offerta e Contratto di progetto utilizzano l'ordine seguente per immettere listini prezzi prodotto predefiniti. Lo stesso ordine viene utilizzato per i listini prezzi progetto.

1.  Offerta
2.  Opportunità
3.  Cliente
4.  Impostazioni globali per PSA

Per impostazione predefinita, il campo **Prodotto** nella riga di offerta elenca tutti i prodotti attivi nel listino prezzi prodotto dell'offerta. Se un prodotto è stato disattivato, o se è un prodotto bozza, non è elencato anche se è presente nel listino prezzi. 

Le righe del catalogo prodotti vengono aggiunte come righe fattura nella prima fattura creata per un contratto di progetto. In una bozza di fattura, queste righe fattura possono essere eliminate. In tal caso, le righe sono visualizzate in una fattura successiva fino a che non vengono fatturate o fino a che la fattura non viene inviata al cliente. In PSA, non è possibile fatturare una quantità parziale di una riga fattura prodotto. Quando le righe prodotto del contratto di progetto sono fatturate, vengono creati dei valori effettivi. Tuttavia, questi valori effettivi non sono collegati all'entità progetto correlata. In altre parole le voci di contratto di progetto basate su prodotto sono indipendenti da qualsiasi utilizzo basato su progetto. PSA non tiene traccia del consumo dei materiali nei progetti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]