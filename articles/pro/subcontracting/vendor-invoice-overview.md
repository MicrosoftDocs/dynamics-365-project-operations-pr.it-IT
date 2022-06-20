---
title: Fatturazione fornitore - Concetto e creazione
description: Questo articolo descrive il concetto di fatture fornitore, gli scenari da utilizzare e come creare le fatture fornitore in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911463"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Fatturazione fornitore - Concetto e creazione

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

La fatturazione fornitore in Microsoft Dynamics 365 Project Operations può essere utilizzata per registrare i costi delle consegne di servizi e/o materiali in un progetto da parte dei fornitori.

Quando i servizi e/o i materiali vengono assegnati in conto lavoro a un fornitore, un conto lavoro rappresenta l'accordo contrattuale con quel fornitore. Quando il fornitore fornisce i servizi o i materiali vengono ricevuti e utilizzati per le attività di progetto, i costi vengono registrati nel progetto. Periodicamente, il fornitore invia le fatture verificate e abbinate ai costi registrati nel progetto. Al termine del processo di verifica, la fattura fornitore viene confermata e rilasciata per il pagamento.

## <a name="scenarios-for-use"></a>Scenari per l'utilizzo

Le fatture fornitore in Project Operations possono essere utilizzate per supportare due scenari distinti.

### <a name="customers-use-the-full-subcontracting-experiences"></a>I clienti utilizzano le esperienze di conto lavoro complete

Le esperienze di fattura fornitore forniscono un modo per verificare e abbinare gli inserimenti ore, l'utilizzo del materiale e le voci di spesa che fanno riferimento a componenti in conto lavoro con le righe di fattura fornitore. Questo processo può essere utilizzato per verificare l'accuratezza delle righe di fattura fornitore. Dopo che il processo di verifica è stato completato e la fattura fornitore è stata confermata, l'applicazione annullerà i valori effettivi registrati dai registri di utilizzo di inserimento ore, spese e materiali approvati e creerà nuovi costi effettivi utilizzando le righe di fattura fornitore.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>I clienti non utilizzano le esperienze di conto lavoro complete ma desiderano avere una visione unificata dei costi sui progetti in Project Operations

Se stai monitorando il processo di conto lavoro in un sistema di terze parti, puoi registrare i costi da tale sistema di terze parti in Project Operations creando fatture fornitore che non fanno riferimento ai conti lavoro. In questo modo, i project manager possono avere una visione unica e unificata di tutti i costi di un determinato progetto.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Creazione di fatture fornitore in Project Operations

Le fatture fornitore possono essere create in due modi:

- Dalla pagina dell'elenco delle fatture fornitore o dalla pagina dei dettagli per una singola fattura fornitore
- Dalla pagina dell'elenco dei conti lavoro o dalla pagina dei dettagli per un singolo conto lavoro

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Creazione dalla pagina dell'elenco delle fatture fornitore o dalla pagina dei dettagli

1. Vai in **Acquisti** \> **Fatture fornitore**.
2. Nella pagina dell'elenco delle fatture fornitore o nella pagina dei dettagli per una singola fattura fornitore, seleziona **Nuovo** per creare una nuova fattura fornitore.

Le fatture fornitore create in questo modo possono fare riferimento anche a un conto lavoro.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Creazione dalla pagina dell'elenco dei conti lavoro o dalla pagina dei dettagli

1. Vai in **Acquisti** \> **Conti lavoro**.
2. Seleziona una o più conti lavoro.
3. Nella pagina dell'elenco dei conti lavoro o nella pagina dei dettagli per un singolo conto lavoro, seleziona **Crea fattur fornitore** per creare una nuova fattura fornitore.

Una nuova fattura fornitore in stato di **Bozza** viene creata per ogni conto lavoro selezionato.

Le fatture fornitore create in questo modo fanno sempre riferimento al conto lavoro nell'intestazione della fattura fornitore. Ciascuna riga del conto lavoro che dispone di un metodo di fatturazione Tempo e materiale causerà la creazione di una riga nella fattura fornitore. Ciascuna riga del conto lavoro che dispone di un metodo di fatturazione a prezzo fisso causerà la creazione di una riga nella fattura fornitore per ogni passaggio fondamentale di riga del conto lavoro con stato **Pronto per la fatturazione**.

I seguenti campi e relativi record verranno copiati dal conto lavoro nell'intestazione della fattura fornitore:

- Fornitore.
- I listini prezzi correlati verranno copiati nella fattura fornitore come listini prezzi.
- Valuta.
- Unità di contratto.
- Condizioni pagamento.

Per le righe tempo e materiale in conto lavoro, i seguenti campi e i record correlati verranno copiati dalla riga conto lavoro alla riga di fattura fornitore:

- Riferimenti di conto lavoro e di riga di conto lavoro
- Classe di transazione
- Ruolo
- Categoria di transazione
- Campi di prodotto
- Project
- Attività
- Risorsa prenotabile

Per le righe prezzo fizzo in conto lavoro, i seguenti campi verranno copiati dalla riga conto lavoro e dal passaggio fondamentale riga conto lavoro alla riga di fattura fornitore:

- Riferimenti di conto lavoro e di riga di conto lavoro.
- Classe di transazione. Per impostazione predefinita, il valore sarà **Passaggio fondamentale**.
- Il nome e l'importo del passaggio fondamentale verranno copiati dal relativo passaggio fondamentale della riga conto lavoro.
- L'utente potrà selezionare un progetto e un'attività nella riga di fattura fornitore.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
