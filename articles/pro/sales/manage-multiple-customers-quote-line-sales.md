---
title: Gestione di più clienti sulle righe di offerta basate su progetto
description: Questo argomento descrive come gestire più clienti sulle righe di offerta basate su progetto.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6a509fcf8d1fa11b4ce1ba1493d9c3cc64b4f22f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078777"
---
# <a name="managing-multiple-customers-on-project-based-quote-lines"></a>Gestione di più clienti sulle righe di offerta basate su progetto

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le righe di offerta basate su progetto supportano scenari in cui ogni riga di offerta include un elenco di clienti che stanno pagando per essa. Questo elenco di clienti nella riga di offerta basata su progetto può essere uguale all'elenco di clienti nell'offerta. Puoi anche modificare l'elenco dei clienti in modo che sia diverso. Dopo l'acquisizione di un'offerta di progetto, l'elenco di clienti nella riga di offerta basata su progetto viene copiato nella voce di contratto basata su progetto corrispondente per creare l'eventuale contratto di progetto. I clienti dell'offerta basata sul progetto vengono copiati nel contratto di progetto.

Quando si fattura l'eventuale contratto di progetto, l'elenco dei clienti nella riga del contratto basato sul progetto ha la priorità sull'elenco nel contratto di progetto. L'elenco di clienti nel contratto di progetto viene utilizzato solo per i valori predefiniti nelle nuove voci del contratto di progetto.

Tutti i clienti dell'offerta nella scheda **Clienti** dell'offerta di progetto vengono impostati in modo predefinito come clienti della riga dell'offerta in qualsiasi nuova riga dell'offerta basata sul progetto creata per l'offerta. Eventuali righe dell'offerta basate sul progetto esistenti non ereditano i nuovi record cliente dell'offerta creati successivamente.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Creare, aggiornare o eliminare un record del cliente della riga di offerta

È possibile creare, aggiornare o eliminare un cliente della riga di offerta nella scheda **Clienti riga di offerta** della pagina **Riga di offerta basata su progetto**. Quando si aggiunge un nuovo cliente alla riga dell'offerta basata sul progetto, il cliente viene aggiunto anche all'offerta complessiva come cliente dell'offerta, con una percentuale di suddivisione della fatturazione predefinita sullo 0%. La percentuale di suddivisione della fatturazione sull'offerta complessiva viene copiata nelle nuove righe dell'offerta e nell'eventuale contratto di progetto. Tuttavia, quando si fattura dal contratto, viene utilizzata la percentuale di suddivisione della fatturazione a livello di riga dell'offerta, non la percentuale di suddivisione della fatturazione a livello di contratto generale. 

I campi elencati nella tabella seguente si trovano nel record del cliente della riga di offerta di una riga di offerta basata su progetto.

| Campo | Ufficio | Descrizione e istruzioni | Impatto downstream |
| --- | --- | --- | --- |
| **Account** | Una griglia modificabile nella scheda **Clienti riga offerta** , il modulo principale e i moduli Creazione rapida per un cliente della riga dell'offerta. | Elenca tutti gli account attivi. Questo campo è bloccato dopo la creazione del record. Se è necessario aggiornare il campo, elimina e ricrea il record. Se hai registrato dei valori effettivi, non puoi eliminare il record. | Quando selezioni un account dall'elenco master degli account da aggiungere, anche il cliente della riga dell'offerta viene aggiunto come cliente dell'offerta quando viene salvato. Quando un'offerta viene acquisita, i clienti della riga dell'offerta vengono copiati nei clienti della voce del contratto di progetto. |
| **Percentuale di separazione fatturazione** | Una griglia modificabile nella scheda **Clienti riga offerta** , il modulo principale e i moduli Creazione rapida per un cliente della riga dell'offerta. | Rappresenta la percentuale di ciascuna transazione di vendita non fatturata che verrà attribuita a questo cliente della riga di offerta. | Copiato nei clienti del contratto di progetto. |
| **Limite da non superare** | Una griglia modificabile nella scheda **Clienti riga offerta** , il modulo principale e i moduli Creazione rapida per un cliente della riga dell'offerta. | Indica se esiste un limite negoziato o un limite massimo per l'importo complessivo che verrà fatturato a questo cliente per questa riga di offerta. | Copiato nei clienti del contratto di progetto quando un'offerta viene acquisita. |
| **Arrotondamento** | Una griglia modificabile nella scheda **Clienti riga offerta** , il modulo principale e i moduli Creazione rapida per un cliente della riga dell'offerta. | Indica se questo cliente è un cliente di arrotondamento predefinito per questa riga di offerta basata su progetto. | Copiato nei clienti del contratto di progetto quando un'offerta viene acquisita. |

## <a name="edit-billing-split-percentages"></a>Modifica delle percentuali di separazione della fatturazione

È possibile modificare le percentuali di suddivisione della fatturazione in linea. Quando le percentuali di suddivisione della fatturazione non raggiungono il 100%, si verifica un errore. Dopo aver modificato le percentuali di suddivisione della fatturazione, aggiorna la pagina della riga di offerta rimuovere l'errore.

Utilizza l'azione di distribuzione uniforme nella griglia secondaria dei clienti della riga di offerta per allocare le suddivisioni di fatturazione a tutti i clienti della riga di offerta. Se è presente un fattore di arrotondamento, verrà aggiunto al cliente di arrotondamento. Uno dei clienti della riga di offerta è sempre contrassegnato come cliente di arrotondamento, il che significa che il record del cliente della riga di offerta ha il flag di arrotondamento impostato su **Sì**. 
