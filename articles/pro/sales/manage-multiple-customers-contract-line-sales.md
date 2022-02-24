---
title: Gestire più clienti sulle voci di contratto basate su progetto - semplice
description: Questo argomento fornisce informazioni sulla gestione di più clienti sulle voci di contratto basate su progetto.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f28e7d1363647621f7bd23504aa6d4ea3fc95fc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181629"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Gestire più clienti sulle voci di contratto basate su progetto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le voci di contratto basate su progetto possono includere un elenco di clienti responsabili del pagamento. Questo elenco di clienti nella voce di contratto basata su progetto può essere uguale all'elenco dei clienti nel contratto, ma non è obbligatorio. Quando si acquisisce un'offerta di progetto e viene creato un contratto di progetto, l'elenco dei clienti nella riga di offerta viene copiato nella voce di contratto corrispondente. I clienti dell'offerta vengono copiati nel contratto.

Quando il contratto di progetto viene fatturato, l'elenco di clienti nella voce di contratto basata su progetto ha la priorità sull'elenco di clienti nel contratto. L'elenco di clienti nel contratto di progetto viene utilizzato solo per le nuove voci di contratto predefinite.

Tutti i clienti di contratto nella scheda **Clienti** del contratto di progetto vengono impostati come clienti della voce di contratto su qualsiasi nuova voce di contratto creata per il contratto di progetto. Eventuali voci di contratto esistenti non erediteranno i nuovi record del cliente di contratto creati dopo di esse.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Creare, aggiornare o eliminare un record cliente di voce di contratto

È possibile creare, aggiornare o eliminare un cliente voce di contratto dalla scheda Clienti voce di contratto nella pagina Voce di contratto basata su progetto. Quando un nuovo cliente viene aggiunto alla voce di contratto basata su progetto, viene aggiunto anche al contratto complessivo come cliente del contratto con una percentuale di suddivisione della fatturazione predefinita dello zero percento. La percentuale di ripartizione della fatturazione sul contratto complessivo viene copiata nelle nuove voci di contratto e nell'eventuale contratto di progetto. Tuttavia, quando si fattura dal contratto, viene utilizzata la percentuale di suddivisione della fatturazione a livello di voce di contratto e non la percentuale di suddivisione della fatturazione a livello di contratto generale.

Di seguito sono riportati i campi del record cliente voce di **contratto** di una voce di contratto basata su progetto da tenere a mente mentre ci si lavora:

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| **Account** | Griglia modificabile nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto. | Tutti i conti attivi. Questo campo è bloccato dopo la creazione del record. Per aggiornare il campo, elimina il record e crea un nuovo record. Se hai registrato dei valori effettivi, non puoi eliminare il record. Tuttavia, puoi contrassegnare la percentuale di suddivisione della fatturazione come zero per quel conto. Quando il record è contrassegnato come zero, vengono influenzati eventuali costi futuri e ricavi effettivi attribuiti o suddivisi per questo cliente. | Quando si seleziona un conto dall'elenco principale dei conti per aggiungerli e salvarli, anche il cliente della voce di contratto viene aggiunto come cliente di contratto. I clienti della voce di contratto vengono utilizzati quando vengono generate le fatture. |
| **Percentuale di separazione fatturazione** | Griglia modificabile nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto. | Questo campo rappresenta la percentuale di ciascuna transazione di vendita non fatturata attribuita a questo cliente di voce di contratto. | I clienti della voce di contratto e le percentuali di suddivisione della fatturazione vengono utilizzati quando i valori effettivi vengono creati dopo l'approvazione e quando viene generata la fattura. |
| **Limite da non superare** | Griglia modificabile nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto. | Indica se esiste un limite negoziato o un limite all'importo complessivo che verrà fatturato al cliente per la voce di contratto. | Il limite da non superare per il cliente della voce di contratto viene utilizzato quando vengono creati i valori effettivi e vengono generate le fatture. |
| **Arrotondamento** | Griglia modificabile nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di voce di contratto. | Questo campo indica se questo cliente è un cliente con arrotondamento predefinito per questa voce di contratto basata su progetto. | Quando generi un valore effettivo in base alla percentuale di suddivisione della fatturazione, potrebbero esserci alcune differenze di arrotondamento. A questo cliente vengono attribuite le differenze di arrotondamento in questo caso. |

## <a name="edit-billing-split-percentages"></a>Modifica delle percentuali di separazione della fatturazione

Le percentuali di suddivisione della fatturazione possono essere modificate nella griglia. Quando le percentuali di suddivisione della fatturazione non raggiungono il 100 percento viene visualizzato un errore. Dopo aver modificato le percentuali di suddivisione della fatturazione, aggiorna la pagina per rimuovere l'errore.

Puoi anche selezionare **Distribuzione uniforme** sulla griglia secondaria dei clienti della voce di contratto. Questa azione assegna in modo uniforme le suddivisioni di fatturazione a tutti i clienti della voce di contratto. Se è presente un fattore di arrotondamento, verrà aggiunto al cliente con arrotondamento. Un cliente della voce di contratto viene sempre contrassegnato come cliente con **arrotondamento** con il contrassegno **Arrotondamento** impostato su **Sì**.
