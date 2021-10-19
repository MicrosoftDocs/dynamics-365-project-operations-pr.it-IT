---
title: Dettagli dell'intestazione per conti lavoro
description: Questo argomento spiega la funzionalità fornita nell'intestazione del conto lavoro in Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501331"
---
# <a name="header-details-for-subcontracts"></a>Dettagli dell'intestazione per conti lavoro

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento spiega la funzionalità fornita nell'intestazione del conto lavoro in Dynamics 365 Project Operations.

In quanto responsabile di progetto pianifica ed esegue progetti, può assumere terzisti e acquistare prodotti e servizi dai fornitori. Quando un responsabile di progetto deve acquistare prodotti o servizi, può creare un conto lavoro in Project Operations.

Per creare un conto lavoro, completare la seguente procedura.

1. Nel riquadro di spostamento, seleziona **Conti lavoro** e nella pagina **Conto lavoro**, seleziona **Nuovo**.
2. Immetti le informazioni richieste e quindi seleziona **Salva**.

    La seguente tabella fornisce informazioni sui campi nella pagina **Intestazione Conto lavoro**.

    | Campo | Descrizione |Impatto funzionale |
    |---|------|---| 
    | Nome | Il nome del conto lavoro. | In tutti gli elenchi a discesa del conto lavoro, il nome del conto lavoro è elencato nella prima colonna per facilitare l'identificazione del conto lavoro. | 
    | Descrizione | Una breve descrizione dei servizi e dei prodotti acquistati in conto lavoro. | Nessuna |
    | Fornitore | Il nome dell'azienda da cui vengono acquistati i prodotti e i servizi. Questo record di account ha un tipo di relazione di **Fornitore** o **Venditore**. | In base al fornitore selezionato, i valori predefiniti vengono inseriti automaticamente per i seguenti campi:<br/> **• Valuta** </br> **• Listini prezzi** </br> **• Condizioni di pagamento**</br> **• Indirizzo pagamento**</br> **• Indirizzo di fatturazione**</br> **• Nome fatturazione** </br>**• Responsabile conto fornitore**|
    | Data di conto lavoro | Data di creazione del conto lavoro. | La data del conto lavoro viene utilizzata per selezionare il listino prezzi di acquisto corretto dai listini prezzi allegati al relativo fornitore o dai parametri del progetto. |
    | Motivo stato | Lo stato del conto lavoro. | Lo stato determina dove si trova il conto lavoro nel processo aziendale e se può essere modificato. <br/>I valori includono:<br>• **Bozza**: il conto lavoro può essere modificato. Puoi solo modificare i conti lavoro con stato **Bozza**.<br/>• **Confermato**: la negoziazione con il fornitore è completata e il conto lavoro è approvato per la consegna. <br/>• **Chiuso**: la consegna del conto lavoro è stata completata.<br/>• **Annullato**: il conto lavoro è stato annullato e non è prevista alcuna consegna.  | 
    | Valuta | La valuta in cui vengono acquistati prodotti e servizi. Il valore predefinito viene inserito automaticamente dal conto fornitore, ma può essere modificato. | La valuta del conto lavoro viene utilizzata per selezionare il listino prezzi di acquisto corretto dai listini prezzi allegati al relativo fornitore o dai parametri del progetto. I listini prezzi in un'altra valuta non possono essere associati al conto lavoro. Il costo del tempo, delle spese e dei materiali che le risorse del fornitore consegnano da questo conto lavoro sono registrati in questa valuta nel progetto. Dopo aver salvato il record del conto lavoro, la valuta del conto lavoro non può essere modificata.|
    | Unità di contratto | La divisione della società che sta stipulando un contratto di acquisto o un conto lavoro con il fornitore. | Nessuna |
    | Condizioni di pagamento | I termini di pagamento sulle fatture fornitore emesse in questo conto lavoro. Il valore predefinito viene inserito automaticamente dal record di account del fornitore. | I termini di pagamento del contratto del conto lavoro vengono copiati in tutte le fatture fornitore correlate a questo conto lavoro. I termini di pagamento possono essere aggiornati se il conto lavoro ha uno stato **Bozza**. | 
    | Indirizzo pagamento | L'indirizzo del fornitore a cui devono essere inviati i pagamenti. Il valore predefinito viene inserito automaticamente dal record di account del fornitore. | L'indirizzo di pagamento del conto lavoro viene copiato come indirizzo di pagamento in tutte le fatture fornitore create per questo conto lavoro. L'indirizzo di pagamento può essere aggiornato se il conto lavoro ha uno stato **Bozza**.|
    | Nome fatturazione | Il nome della persona o della divisione nell'azienda del fornitore che invierà la fattura. Il valore predefinito viene inserito automaticamente dal record di account del fornitore. | Il valore **Nome fatturazione** del conto lavoro viene copiato in tutte le fatture fornitore correlate a questo conto lavoro. Questo campo può essere aggiornato se il conto lavoro ha uno stato **Bozza**.|
    | Indirizzo di fatturazione | L'indirizzo utilizzato nelle fatture del fornitore. Il valore predefinito viene inserito automaticamente dal record di account del fornitore. | Questo indirizzo è l'indirizzo "fattura da" sulle fatture fornitore create per questo conto lavoro. |
    | Subtotale | Se un conto lavoro non contiene righe, inserisci il totale parziale dell'ordine al lordo delle imposte. Se il conto lavoro contiene righe, questo campo è in sola lettura. L'importo visualizzato è l'importo del subtotale di tutte le righe del conto lavoro. | Nessuna |
    | Totale imposte | Se un conto lavoro non contiene righe, inserisci il totale delle imposte su questo conto lavoro. Se il conto lavoro contiene righe, questo campo è in sola lettura. L'importo visualizzato è la somma dell'importo delle imposte di tutte le righe del conto lavoro. | Nessuna |
    | Totale importo | Questo campo calcolato mostra l'importo totale del conto lavoro dopo l'inclusione delle imposte. | Nessuna |
    | Data confermata | La data di conferma del conto lavoro. | Nessuna |
    | Richiesto da | Per impostazione predefinita, questo campo è impostato sul nome dell'utente che crea il conto lavoro. Tuttavia, il creatore del conto lavoro può modificare il valore per indicare la persona per conto della quale sta creando il conto lavoro. | Nessuna |
    | Responsabile conto fornitore | Il nome del contatto primario dell'account fornitore. Il valore predefinito viene inserito automaticamente dal record di account del fornitore. Puoi selezionare un contatto diverso come responsabile del conto fornitore del conto lavoro. | Puoi impostare avvisi e-mail per informare il contatto quando vengono apportate modifiche al conto lavoro a seguito di negoziazioni dei prezzi. |
