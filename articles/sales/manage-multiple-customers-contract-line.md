---
title: Gestire più clienti sulle voci di contratto basate su progetto
description: Questo articolo fornisce informazioni sull'utilizzo di righe di contratto e contratti che contengono più clienti.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e0652d4b9cdb0489d4f191ef0f3b251e39262f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914867"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Gestire più clienti sulle voci di contratto basate su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le voci di contratto basate su progetto possono includere un elenco di clienti responsabili del pagamento. Questo elenco di clienti nella voce di contratto basata su progetto può essere uguale all'elenco dei clienti nel contratto, ma non è obbligatorio. Quando si acquisisce un'offerta di progetto e viene creato un contratto di progetto, l'elenco dei clienti nella riga di offerta viene copiato nella voce di contratto corrispondente. I clienti dell'offerta vengono copiati nel contratto.

Quando il contratto di progetto viene fatturato, l'elenco di clienti nella voce di contratto basata su progetto ha la priorità sull'elenco di clienti nel contratto. L'elenco di clienti nel contratto di progetto viene utilizzato solo per le nuove voci di contratto predefinite.

Tutti i clienti di contratto nella scheda **Clienti** del contratto di progetto vengono impostati come clienti della voce di contratto su qualsiasi nuova voce di contratto creata per il contratto di progetto. Eventuali voci di contratto esistenti non erediteranno i nuovi record del cliente di contratto creati dopo di esse.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Creare, aggiornare o eliminare un record cliente di voce di contratto

È possibile creare, aggiornare o eliminare un cliente voce di contratto dalla scheda **Clienti voce di contratto** nella pagina **Voce di contratto basata su progetto**. Quando un nuovo cliente viene aggiunto alla voce di contratto basata su progetto, viene aggiunto anche al contratto complessivo come cliente del contratto con una percentuale di suddivisione della fatturazione predefinita dello zero percento. La percentuale di ripartizione della fatturazione sul contratto complessivo viene copiata nelle nuove voci di contratto e nell'eventuale contratto di progetto. Tuttavia, quando si fattura dal contratto, viene utilizzata la percentuale di suddivisione della fatturazione a livello di voce di contratto e non la percentuale di suddivisione della fatturazione a livello di contratto generale. 

Di seguito sono riportati i campi del record cliente voce di contratto di una voce di contratto basata su progetto da tenere a mente mentre ci si lavora:

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| Conto | Griglia modificabile nella scheda **Clienti voce di contratto** e i moduli Principale e Creazione rapida per un cliente di voce di contratto | Tutti i conti attivi. Questo campo è bloccato dopo la creazione del record. Per aggiornare il campo, elimina il record e crea un nuovo record. Se hai registrato dei valori effettivi, non puoi eliminare il record. Tuttavia, puoi contrassegnare la percentuale di suddivisione della fatturazione come zero per quel conto. Quando il record è contrassegnato come zero, vengono influenzati eventuali costi futuri e ricavi effettivi attribuiti o suddivisi per questo cliente. | Quando si seleziona un conto dall'elenco principale dei conti per aggiungerli e salvarli, anche il cliente della voce di contratto viene aggiunto come cliente di contratto. I clienti della voce di contratto vengono utilizzati quando vengono generate le fatture. |
| Percentuale di suddivisione fatturazione | Griglia modificabile nella scheda **Clienti voce di contratto** e i moduli Principale e Creazione rapida per un cliente di voce di contratto | Questo campo rappresenta la percentuale di ciascuna transazione di vendita non fatturata attribuita a questo cliente di voce di contratto. | I clienti della voce di contratto e le percentuali di suddivisione della fatturazione vengono utilizzati quando i valori effettivi vengono creati dopo l'approvazione e quando viene generata la fattura. |
| Limite da non superare | Griglia modificabile nella scheda **Clienti voce di contratto** e i moduli Principale e Creazione rapida per un cliente di voce di contratto | Indica se esiste un limite negoziato o un limite all'importo complessivo che verrà fatturato al cliente per la voce di contratto. | Il limite da non superare per il cliente della voce di contratto viene utilizzato quando vengono creati i valori effettivi e vengono generate le fatture. |
| Società proprietaria | Griglia modificabile nella scheda **Clienti riga di offerta** e i moduli Principale e Creazione rapida per un cliente di riga di offerta | La persona giuridica in cui è impostato questo cliente. Questo campo è di sola lettura ed è impostato sulla società proprietaria dell'offerta. L'elenco dei clienti da aggiungere nel campo **Conto** è già filtrato con l'elenco di questa società proprietaria. | Il concetto di società proprietaria equivale al concetto di persona giuridica. Tutti i costi e le entrate derivanti da questo progetto sono contabilizzati nella contabilità generale della società proprietaria. |
| Arrotondamento | Griglia modificabile nella scheda **Clienti voce di contratto** e i moduli Principale e Creazione rapida per un cliente di voce di contratto | Questo campo indica se questo cliente è un cliente con arrotondamento predefinito per questa voce di contratto basata su progetto. | Quando generi un valore effettivo in base alla percentuale di suddivisione della fatturazione, potrebbero esserci alcune differenze di arrotondamento. A questo cliente vengono attribuite le differenze di arrotondamento in questo caso. |

## <a name="edit-billing-split-percentages"></a>Modifica delle percentuali di separazione della fatturazione

Le percentuali di suddivisione della fatturazione possono essere modificate nella griglia. Quando le percentuali di suddivisione della fatturazione non raggiungono il 100 percento viene visualizzato un errore. Dopo aver modificato le percentuali di suddivisione della fatturazione, aggiorna la pagina per rimuovere l'errore.

Puoi anche provare a selezionare **Distribuzione uniforme** sulla griglia secondaria dei clienti della voce di contratto. Questa azione assegna in modo uniforme le suddivisioni di fatturazione a tutti i clienti della voce di contratto. Se è presente un fattore di arrotondamento, verrà aggiunto al cliente con arrotondamento. Un cliente della voce di contratto viene sempre contrassegnato come cliente con **arrotondamento** con il contrassegno **Arrotondamento** impostato su **Sì**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]