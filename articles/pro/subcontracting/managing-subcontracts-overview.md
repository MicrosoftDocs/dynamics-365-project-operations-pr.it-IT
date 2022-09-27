---
title: Gestione dei conti lavoro in Project Operations
description: Questo articolo fornisce una panoramica del processo di gestione del conto lavoro end-to-end tipico nelle organizzazioni basate su progetti.
author: rumant
ms.date: 09/14/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b2e4518f77b2099f9818ea56623be9efb20b01f4
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522330"
---
# <a name="subcontract-management-in-project-operations"></a>Gestione dei conti lavoro in Project Operations


_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

Questo articolo fornisce una panoramica del processo di gestione del conto lavoro end-to-end nelle organizzazioni basate su progetti. Il conto lavoro per i servizi in genere segue il flusso del processo aziendale mostrato nel diagramma seguente.

![Flusso del processo dei conti lavoro](../media/SubcontractingProcessFlow.png)

Il seguente elenco riporta una descrizione dettagliata del processo di conti lavoro.

1. Il project manager crea un conto lavoro con un fornitore. Per impostazione predefinita, per il conto lavoro vengono utilizzati i listini prezzi associati al record del fornitore. Il conto fornitore ha un tipo di relazione di tipo **fornitore** o **venditore**.
2. Il project manager può dettagliare tutti gli acquisti come voci nel conto lavoro. Le righe del conto lavoro possono riguardare tempi, spese o prodotti. La classe di transazione della voce di conto lavoro determina a cosa serve la riga.
3. L'account manager del fornitore e il project manager possono eseguire iterazioni sul conto lavoro. È possibile apportare modifiche ai prezzi nei listini prezzi di acquisto associati al conto lavoro.
4. A questo punto o in una fase successiva del processo, se la riga di conto lavoro è per il tempo, l'account manager del fornitore associa i contatti dei fornitori a ciascuna riga di conto lavoro. Questa associazione fornisce informazioni al project manager che sta lavorando sul conto lavoro. Quando un contatto fornitore è associato a una riga di conto lavoro, il sistema crea automaticamente una risorsa prenotabile dal contatto, se non esiste già una risorsa prenotabile.
5. Il metodo di fatturazione su ciascuna riga di subappalto può essere di tipo **prezzo fisso** o **tempo e materiale**. Per le righe di conto lavoro a prezzo fisso viene impostata una pianificazione fattura basata su passaggi fondamentali.
6.  Dopo che il conto lavoro è stato impostato e la negoziazione è stata completata, viene confermata. I conti lavoro confermati non possono essere modificati, ma in caso di modifiche, puoi "aprire nuovamente per la modifica"; questa operazione imposta lo stato da **Confermato** torna a **Bozza** e la trattativa può essere riaperta. 
7.  Quando si crea un membro del team generico in un progetto, il membro del team può essere associato a una voce di conto lavoro. Ciò indica la necessità di dotare il membro del team generico di personale con capacità di terzista.
8.  I membri del team nominati possono essere creati direttamente su un progetto o creati prenotandoli utilizzando le esperienze di pianificazione delle risorse. Se un membro del team di progetto denominato è un lavoratore a contratto, puoi associarlo a una voce di conto lavoro. Ciò ridurrà la capacità disponibile su una voce di conto lavoro.
9.  Le risorse del terzista possono registrare ore, spese e utilizzo di materiale su progetti e attività progettuali e quindi inviarle per l'approvazione. Questa operazione è simile per i dipendenti. Durante la registrazione delle ore, un lavoratore a contratto può selezionare un conto lavoro specifico e una riga di conto lavoro.
10. Dopo l'approvazione, il tempo approvato dai terzisti registrerà i costi effettivi del progetto in base al prezzo di acquisto del lavoratore a contratto o al ruolo svolto nel progetto.
11. Le fatture fornitore e le voci della fattura fornitore possono essere registrate nel sistema per il lavoro svolto dalle risorse del fornitore o dai prodotti consegnati dal fornitore. Le righe della fattura fornitore devono essere specifiche per un progetto e per una classe di transazione di ore, spesa, prodotto/materiale, passaggio fondamentale o corrispettivo. Facoltativamente, le voci della fattura fornitore possono fare riferimento a una voce di conto lavoro.
12. Il sistema associerà automaticamente alla fattura fornitore tutti i costi effettivi che corrispondono alla riga e al progetto di conto lavoro. Ciò faciliterà una corrispondenza a 3 vie e un processo di verifica.
13. Il responsabile di progetto può quindi rivedere gli effettivi del progetto abbinati automaticamente, rimuovere o aggiungere altri effettivi dei costi del progetto e completare il processo di verifica.
14. Il completamento del processo di verifica su tutte le righe contrassegnerà la fattura del fornitore come **Pronta per il pagamento**. In questa fase, la fattura fornitore e le righe possono essere trasferite a un sistema Contabilità o Contabilità fornitori per elaborare il pagamento al fornitore. I costi del progetto registrati in precedenza verranno stornati e i costi effettivi dalla voce della fattura fornitore verranno registrati nel progetto.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Voci di conto lavoro basate sulla quantità e righe di conto lavoro basate sul lavoro

Una voce di conto lavoro può essere basata su quantità o su lavoro. 

Quando una voce di conto lavoro è **basata su quantità**, la quantità acquistata nella voce del conto lavoro per ore, spese o materiale può essere utilizzata in qualsiasi progetto.

Quando una voce di conto lavoro è **basata sul lavoro**, la voce del conto lavoro viene mappata a un corpo di lavoro rappresentato da un nodo nel piano di progetto. Il valore della voce di conto lavoro è la somma di tutti i componenti necessari per consegnare quel corpo di lavoro. Questi sono modellati come dettagli della voce di conto lavoro e possono essere una raccolta di ore, spese o materiali. Per una voce di conto lavoro basata sul lavoro, anche la voce di conto lavoro è dedicata a un singolo progetto. Questi tipi di conto lavoro non sono attualmente supportati da Project Operations.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

