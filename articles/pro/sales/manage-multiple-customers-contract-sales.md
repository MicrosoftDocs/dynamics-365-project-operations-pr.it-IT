---
title: Gestire più clienti nei contratti di progetto - semplice
description: Questo articolo fornisce informazioni sulla gestione di più clienti nei contratti di progetto.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17cd464bad81a01f5f334524a542104d6f25717b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917210"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Gestire più clienti nei contratti di progetto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

I contratti di progetto in Dynamics 365 Project Operations supportano lo scenario in cui un contratto coinvolge più clienti che stanno finanziando una transazione. La scheda **Sommario** della pagina **Contratto di progetto** include il campo **Cliente**. Questo campo identifica il cliente principale della transazione. Altri clienti per la transazione possono essere impostati nella scheda **Clienti** della pagina **Contratto di progetto**.

Tutti i clienti di contratto elencati nel contratto di progetto vengono impostati come clienti della voce di contratto su qualsiasi nuova voce di contratto basata su progetto creata per il contratto di progetto. Le voci di contratto esistenti basate su progetto non ereditano i nuovi clienti di contratto quando vengono creati nuovi record.

Le voci di contratto basate su prodotto vengono automaticamente associate al cliente principale.

I clienti del contratto e i clienti della voce di contratto possono essere aggiunti, aggiornati o eliminati in qualsiasi momento prima che il contratto venga acquisito.

## <a name="primary-customer"></a>Cliente primario

Il cliente elencato nella scheda **Sommario** del contratto di progetto come potenziale cliente è il cliente primario del contratto. Quando tenti di eliminare il cliente primario dall'elenco dei clienti nel contratto, verrà visualizzato un messaggio di errore indicante che un record del cliente primario in un contratto non può essere eliminato.

Il cliente principale non può essere aggiornato dall'elenco dei clienti di contratto. Cambia invece il cliente potenziale nella scheda **Sommario** del contratto. Quando questo campo viene aggiornato nella pagina **Riepilogo del contratto**, il nuovo cliente viene aggiunto come nuovo cliente del contratto con il contrassegno **Primario** impostato. Il cliente principale precedente sarà ancora un cliente del contratto.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Creare, aggiornare o eliminare un record cliente di contratto

È possibile creare, aggiornare o eliminare un cliente di contratto dalla scheda **Clienti** della pagina **Contratto di progetto**. I campi nella tabella seguente si trovano nel record cliente di contratto di un contratto di progetto e devono essere tenuti in considerazione quando si lavora con il contratto.

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| **Account** | La griglia può essere modificata nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto. | Elenca tutti gli account attivi. Questo campo è bloccato dopo la creazione del record. Per aggiornare il conto, elimina il record e ricrealo. Se sono stati registrati valori effettivi o se il record cliente di contratto è un cliente principale, non è possibile eliminare il record. | I clienti di contratto vengono copiati come clienti della voce di contratto quando viene creata una voce di contratto. |
| **Percentuale di separazione fatturazione** | La griglia può essere modificata nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto. | Rappresenta la percentuale di ciascuna transazione di vendita non fatturata attribuita a questo cliente di contratto. | Copiato nelle nuove voci di contratto e nei clienti della voce di contratto di progetto sulle nuove voci di contratto di progetto. |
| **Nome contatto fatturazione** | La griglia può essere modificata nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto. | Questo campo di testo deve essere utilizzato per identificare la persona di contatto per le fatture per questo cliente. L'impostazione predefinita di questo campo è il record del conto correlato. | Copiato nel campo **Fattura a nome contratto** sulla fattura generata per questo cliente. |
| **Nome fatturazione** | La griglia può essere modificata nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto | Questo campo di testo deve essere utilizzato per identificare la persona di contatto per le fatture per questo cliente. L'impostazione predefinita di questo campo è il record del conto correlato. | Copiato nel campo **Fattura a nome contratto** sulla fattura generata per questo cliente. |
| **Condizioni di pagamento** | La griglia può essere modificata nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto. | I valori vengono impostati dal record del conto correlato. | Copiato nel campo **Fattura a nome contratto** sulla fattura generata per questo cliente. |
| **Arrotondamento** | La griglia può essere modificata nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto. | Indica se questo cliente è un cliente di arrotondamento predefinito per questa transazione. Può esserci un solo cliente con arrotondamento su un contratto di progetto. | Quando le suddivisioni dei costi e delle vendite non fatturate in base alla quantità determinano una differenza di arrotondamento, tale differenza viene applicata al valore effettivo associato a questo cliente. |
| **Limite da non superare** | La griglia può essere modificata nella scheda **Clienti di contratto** e i moduli **Principale** e **Creazione rapida** per un cliente di contratto | Indica se esiste un limite negoziato o un limite all'importo complessivo che verrà fatturato al cliente per questo impegno. | Il **Limite da non superare** verrà valutato a livello di cliente di contratto in **Valori effettivi vendite non fatturate** che fanno riferimento a questo cliente di contratto. |

## <a name="edit-billing-split-percentages"></a>Modifica delle percentuali di separazione della fatturazione

Le percentuali di suddivisione della fatturazione possono essere modificate utilizzando l'esperienza di modifica della griglia in linea. Quando le percentuali di suddivisione della fatturazione non raggiungono il 100 percento, verrà visualizzato un errore. Dopo aver modificato le percentuali di suddivisione della fatturazione, aggiorna la pagina per eliminare l'errore.

Puoi anche selezionare **Distribuisci uniformemente** nella griglia secondaria **Clienti di contratto** per allocare le ripartizioni di fatturazione in modo uniforme a tutti i clienti del contratto. Se è presente un fattore di arrotondamento, verrà aggiunto al cliente con arrotondamento. Uno dei clienti del contratto è sempre contrassegnato come cliente con **arrotondamento** il che significa che il record del cliente del contratto ha il contrassegno di arrotondamento impostato su **Sì**. In genere, questo è il cliente principale del contratto, ma può anche essere modificato.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]