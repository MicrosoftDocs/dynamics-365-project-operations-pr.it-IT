---
title: Dettagli dell'intestazione per conti lavoro
description: Questo argomento spiega la funzionalità fornita nell'intestazione del conto lavoro in Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323646"
---
# <a name="header-details-for-subcontracts"></a>Dettagli dell'intestazione per conti lavoro

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento spiega la funzionalità fornita nell'intestazione del conto lavoro in Dynamics 365 Project Operations.

In quanto responsabile di progetto pianifica ed esegue progetti, può assumere terzisti e acquistare prodotti e servizi dai fornitori. Quando un responsabile di progetto deve acquistare prodotti o servizi, può creare un conto lavoro in Project Operations.

Per creare un conto lavoro, completare la seguente procedura.

1. Nel riquadro di spostamento, seleziona **Conti lavoro** e nella pagina **Conto lavoro**, seleziona **Nuovo**.
2. Immetti le informazioni richieste e quindi seleziona **Salva**.

    La seguente tabella fornisce informazioni sui campi nella pagina dell'intestazione Conto lavoro.

    | **Campo** | **Descrizione** |
    | --- | --- | 
    | Nome | Il nome del conto lavoro. |
    | Descrizione | Una breve descrizione dei servizi e dei prodotti acquistati in conto lavoro. |
    | Fornitore | Il nome dell'azienda da cui vengono acquistati i prodotti e i servizi. Questo record di account ha un tipo di relazione di **Fornitore** o **Venditore**. |
    | Data di conto lavoro | La data di creazione del conto lavoro. |
    | Motivo stato | Lo stato del conto lavoro. |
    | Valuta | La valuta in cui vengono acquistati prodotti e servizi. Il valore in questo campo è predefinito dal conto fornitore ma può essere modificato. I listini prezzi dei progetti utilizzati per la determinazione del prezzo di prodotti e servizi nel conto lavoro devono essere in questa valuta. Al conto lavoro non possono essere associati listini prezzi in altra valuta. Il costo dei prodotti e dei servizi sostenuti per questo conto lavoro sarà registrato sul progetto in questa valuta. |
    | Unità di contratto | La divisione della società che sta stipulando un contratto di acquisto o un conto lavoro con il fornitore. |
    | Condizioni di pagamento | I termini di pagamento sulle fatture dei fornitori emesse in questo conto lavoro. Il valore in questo campo è predefinito dal record di account del fornitore. |
    | Indirizzo pagamento | L'indirizzo a cui viene inviato il pagamento sulle fatture fornitore. Il valore in questo campo è predefinito dal record di account del fornitore. |
    | Nome fatturazione | Il nome della persona o della divisione nell'azienda del fornitore che invierà la fattura. Il valore in questo campo è il valore predefinito dal record di account fornitore e verrà utilizzato come nome del contatto primario nelle fatture fornitore create per questo conto lavoro. |
    | Indirizzo di fatturazione | L'indirizzo utilizzato nelle fatture di questo fornitore. Il valore in questo campo è predefinito dal record di account del fornitore. Questo indirizzo viene utilizzato anche come indirizzo della fattura proveniente dalle fatture fornitore create per questo conto lavoro. |
    | Subtotale | Se un conto lavoro non contiene righe, immetti un valore in questo campo che indichi il totale parziale dell'ordine al lordo delle imposte. Se il conto lavoro contiene righe, questo campo è in sola lettura. L'importo visualizzato è l'importo del subtotale di tutte le righe del conto lavoro. |
    | Totale imposte | Se un conto lavoro non contiene righe, immetti un valore in questo campo che indichi imposte in questo conto lavoro. Se il conto lavoro contiene righe, questo campo è in sola lettura. L'importo visualizzato è la somma dell'importo delle imposte di tutte le righe del conto lavoro. |
    | Totale importo |  Questo campo calcolato mostra l'importo totale del conto lavoro dopo l'inclusione delle imposte.  |
    | Data confermata | La data di conferma del conto lavoro.  |
    | Richiesto da | Il valore in questo campo per impostazione predefinita è il nome dell'utente che crea il conto lavoro. Questo valore può essere modificato dall'autore del conto lavoro per indicare la persona per conto della quale si sta creando il conto lavoro.  |
    | Responsabile conto fornitore | Il nome del contatto primario dell'account fornitore. Il valore in questo campo è predefinito dal record di account del fornitore. Questo valore del campo può essere modificato dall'utente per selezionare un contatto diverso come responsabile del conto fornitore del conto lavoro. Avvisi e-mail e trattative sui prezzi possono essere configurati e inviati da questo contatto. |


