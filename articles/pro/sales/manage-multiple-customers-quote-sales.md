---
title: Gestione di più clienti nelle offerte di progetto
description: Questo argomento fornisce informazioni su come utilizzare offerte con più clienti che finanzieranno il progetto. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966806"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Gestione di più clienti nelle offerte di progetto (Vendite)

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le offerte di progetto supportano lo scenario in cui la proposta coinvolge più clienti che finanzieranno la transazione. La scheda **Riepilogo** dell'offerta contiene il campo **Potenziale cliente** che identifica il cliente principale della transazione. Altri clienti per la transazione possono essere impostati nella scheda **Clienti** dell'offerta di progetto.

Tutti i clienti dell'offerta nella scheda **Clienti** dell'offerta di progetto vengono impostati in modo predefinito come clienti della riga dell'offerta in qualsiasi **nuova** riga dell'offerta basata sul progetto creata per l'offerta. Eventuali righe dell'offerta basate sul progetto esistenti non erediteranno i nuovi record cliente dell'offerta creati successivamente.

Le righe dell'offerta basate sul prodotto vengono automaticamente associate al cliente primario, che è anche il cliente nel campo **Potenziale cliente** nella scheda **Riepilogo** dell'offerta.

I clienti dell'offerta e quelli della riga dell'offerta possono essere aggiunti, aggiornati o eliminati in qualsiasi momento prima che l'offerta venga acquisita.

## <a name="concept-of-a-primary-customer"></a>Concetto di cliente primario

Il cliente che si trova nella scheda Riepilogo dell'offerta di progetto come potenziale cliente è il cliente primario dell'offerta. Quando si tenta di eliminare il cliente primario dall'elenco dei clienti nell'offerta, verrà visualizzato un errore relativo all'impossibilità di eliminare un record del cliente primario in un'offerta.

Il cliente primario non deve essere aggiornato dall'elenco dei clienti nell'offerta. Tuttavia, puoi determinare il cliente primario modificando il potenziale cliente nella scheda **Riepilogo** dell'offerta. Quando questo campo viene aggiornato in **Riepilogo offerta**, il potenziale cliente appena selezionato viene aggiunto come nuovo cliente dell'offerta con il contrassegno **Primario** impostato. Il vecchio potenziale cliente sarà ancora un cliente dell'offerta.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Creare, aggiornare o eliminare un record del cliente dell'offerta

Un cliente dell'offerta può essere creato, aggiornato o eliminato dalla scheda **Clienti offerta** nella pagina **Offerta**. I campi elencati nella tabella seguente si trovano nel record del cliente dell'offerta di un'offerta di progetto.

| **Campo** | **Luogo** | **Pertinenza, scopo e indicazioni** | **Impatto downstream** |
| --- | --- | --- | --- |
| Conto | Griglia modificabile nella scheda **Clienti offerta** e i moduli **Principale** e **Creazione rapida** per un cliente dell'offerta. | Elenca tutti gli account attivi. Questo campo è bloccato dopo la creazione del record. Se desideri aggiornarlo, elimina il record e ricrealo. Se sono stati registrati valori effettivi o se il record del cliente dell'offerta è un cliente primario, sarà possibile eliminare il record. | I clienti dell'offerta vengono copiati come clienti della riga dell'offerta quando viene creata una riga dell'offerta. I clienti dell'offerta vengono copiati anche nei clienti del contratto di progetto quando un'offerta viene acquisita. |
| Percentuale di suddivisione fatturazione | Griglia modificabile nella scheda **Clienti offerta** e i moduli **Principale** e **Creazione rapida** per un cliente dell'offerta. | Rappresenta la percentuale di ciascuna transazione di vendita non fatturata che verrà attribuita a questo cliente dell'offerta. | Copiato nelle nuove righe dell'offerta e nei clienti del contratto di progetto. |
| Nome contatto fatturazione | Griglia modificabile nella scheda **Clienti offerta** e i moduli **Principale** e **Creazione rapida** per un cliente dell'offerta. | Questo è un campo di testo e deve essere utilizzato per identificare la persona di contatto per le fatture per questo cliente. Questi sono impostati in modo predefinito dal record dell'account correlato | Copiato nei clienti del contratto di progetto quando viene acquisita un'offerta e nel campo del nome del contatto di fatturazione sulla fattura generata per questo cliente. |
| Nome fatturazione | Griglia modificabile nella scheda **Clienti offerta** e i moduli **Principale** e **Creazione rapida** per un cliente dell'offerta. | Questo campo di testo deve essere utilizzato per identificare la persona di contatto per le fatture per questo cliente. | Copiato nei clienti del contratto di progetto quando viene acquisita un'offerta e nel campo **Nome contatto fatturazione** sulla fattura generata per questo cliente. |
| Condizioni di pagamento | Griglia modificabile nella scheda **Clienti offerta** e i moduli **Principale** e **Creazione rapida** per un cliente dell'offerta. | Questo è un set di opzioni con valori impostati in modo predefinito dal record dell'account correlato. | Copiato nei clienti del contratto di progetto quando viene acquisita un'offerta e nel campo **Nome contatto fatturazione** sulla fattura generata per questo cliente. |
| Arrotondamento | Griglia modificabile nella scheda **Clienti offerta** e i moduli **Principale** e **Creazione rapida** per un cliente dell'offerta. | Indica se questo cliente è un cliente di arrotondamento predefinito per questa transazione. | Copiato nei clienti del contratto di progetto quando un'offerta viene acquisita. |
| Limite da non superare | Griglia modificabile nella scheda **Clienti offerta** e i moduli **Principale** e **Creazione rapida** per un cliente dell'offerta. | Indica se esiste un limite negoziato o un limite massimo per l'importo complessivo che verrà fatturato a questo cliente per questo impegno | Copiato nei clienti del contratto di progetto quando un'offerta viene acquisita. |

## <a name="editing-billing-split-percentages"></a>Modifica delle percentuali di suddivisione della fatturazione

Puoi modificare le percentuali di suddivisione della fatturazione utilizzando l'esperienza di modifica della griglia in linea. Quando le percentuali di suddivisione della fatturazione non raggiungono il 100%, si verifica un errore. Dopo aver aggiornato le percentuali di suddivisione della fatturazione, aggiorna la pagina per rimuovere l'errore.

Puoi anche provare a selezionare **Distribuzione uniforme** nella griglia secondaria dei clienti dell'offerta. Questa azione assegna le suddivisioni della fatturazione a tutti i clienti dell'offerta. Se è presente un fattore di arrotondamento, verrà aggiunto al cliente di arrotondamento. Uno dei clienti dell'offerta viene sempre contrassegnato come cliente di arrotondamento. Ciò significa che il record del cliente dell'offerta ha il contrassegno **Arrotondamento** impostato su **Sì**. In genere questo è il cliente primario dell'offerta, ma può essere modificato.
