---
title: Costi e ricavi di progetto
description: In questo argomento vengono fornite informazioni sulle stime di costi e ricavi di progetto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8afa297190406c7fab8237e16c56cfe232a220af
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283958"
---
# <a name="project-costs-and-revenue"></a>Costi e ricavi di progetto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Le stime di progetto forniscono una vista finanziaria del il lavoro stimato e pianificato nella pianificazione di progetto. La scheda **Stime** nella pagina **Progetti** mostra l'impatto di ricavi e costi del lavoro che si pianifica. Fornisce inoltre informazioni su molte dimensioni predefinite. 

> ![Scheda Stime](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Valori di costi e vendite del progetto

I listini prezzi definiscono i tassi di costo e fatturazione per i ruoli in un progetto. Puoi determinare l'impatto di ricavi e costi del lavoro in base ai ruoli associati al nome della posizione e alla risorsa denominata assegnata a un'attività. Se vi sono attività senza assegnazioni (generiche o denominate), non puoi ottenere stime di costi o vendite. I valori di costo e vendita prendono in considerazione la data definita nei listini prezzi.

### <a name="default-cost-price"></a>Prezzo di costo predefinito  

Ogni progetto appartiene a un'organizzazione. Questa organizzazione è visualizzata nel campo **Unità contratto** del progetto. Il listino prezzi associato all'unità contratto viene utilizzato per determinare il prezzo di costo unitario. Per determinare i prezzi di costo corretti per i ruoli per la data definita nelle righe di stima, cerca la combinazione di ruolo, unità e unità organizzativa nel listino prezzi di costo. 

Affinché sia possibile calcolare i prezzi di costo, tutte le attività devono essere assegnate a una risorsa. Le attività non assegnate avranno un prezzo di costo pari a 0,00.

Se la combinazione di ruolo, unità e unità organizzativa non restituisce un prezzo di costo dal listino prezzi dell'unità contratto, il sistema ignora l'unità. Cerca invece solamente la combinazione di ruolo e unità organizzativa. Se viene trovato un prezzo di costo, i fattori di conversione sono utilizzati per convertirlo nell'unità selezionata nella riga di stima.

Se la combinazione di ruolo e unità organizzativa non restituisce un prezzo di costo, il sistema ignora l'unità organizzativa. Cerca invece la combinazione di ruolo e unità per impostare il prezzo predefinito (dopo l'applicazione di qualsiasi conversione).

Se il sistema non trova un prezzo per il ruolo, il prezzo di costo nella riga di stima è impostato sul valore predefinito **0,00**. Tutti gli importi dei costi nelle righe di stima dei costi di progetto sono registrati nella valuta dell'unità contratto.

> [!NOTE]
> Per impostazione predefinita, Microsoft Dynamics 365 memorizza gli importi dei costi nella valuta di base. Tuttavia, gli importi dei costi visualizzati nella scheda **Stime** sono nella valuta dell'unità contratto.  

### <a name="default-sales-price"></a>Prezzo di vendita predefinito 

Il listino prezzi di vendita è determinato dall'entità di vendita a cui il progetto è associato o al cliente del progetto. Quando un'entità di vendita, ad esempio un'opportunità, un'offerta o un contratto, è associata al progetto, il prezzo di vendita dell'entità di vendita viene determinato dal listino prezzi associato all'offerta o al contratto. Se l'offerta o il contratto ha un listino prezzi personalizzato, quel listino prezzi viene utilizzato come listino predefinito per le stime di progetto. Se non esiste un'associazione con le entità di vendita, il listino prezzi di vendita predefinito nei parametri viene utilizzato come listino prezzi di vendita predefinito del progetto con la valuta cliente definita nel progetto.

A ogni riga di stima è associata un'unità di gestione risorse. L'unità di gestione risorse indica l'unità organizzativa da cui vengono prenotate le risorse per completare l'attività. Per determinare il prezzo di vendita dei ruoli associati, cerca la combinazione di ruolo, unità e unità di gestione risorse nel listino prezzi di vendita. Se non sono presenti assegnazioni per l'attività, il prezzo di vendita per l'attività è 0,00.

Se la combinazione di ruolo, unità e unità di gestione risorse non restituisce un prezzo di vendita dal listino prezzi di vendita, il sistema ignora l'unità. Cerca invece solamente la combinazione di ruolo e unità di gestione risorse. Se viene trovato un prezzo di vendita, i fattori di conversione sono utilizzati per convertirlo nell'unità selezionata nella riga di stima di vendita. 

Se la combinazione di ruolo e unità di gestione risorse non restituisce un prezzo di vendita dal listino prezzi di vendita, il sistema ignora l'unità di gestione risorse. Cerca invece la combinazione di ruolo e unità per impostare il prezzo predefinito (dopo l'applicazione di qualsiasi conversione).

Se il sistema non trova un prezzo per il ruolo, il prezzo di vendita nella riga di stima è impostato sul valore predefinito **0,00**.

La scheda **Stime** include una vista griglia che mostra le righe di stima. La griglia include colonne per unità, prezzo di costo totale e prezzo di vendita totale, come illustrato nella figura seguente. 

> ![Vista Griglia nella scheda Stime](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Visualizzazione su scala cronologica delle stime di progetto

La vista su scala cronologica delle stime di progetto visualizza i dati delle stime della vista griglia nella sequenza temporale, secondo una scala temporale che hai selezionato. Per impostazione predefinita, i dati delle stime sono basati sulla dimensione **Ruolo**.

> ![Vista su scala cronologica delle stime di progetto](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Allocare il lavoro richiesto stimato in base alla modalità attività

Nella vista su scala cronologica, distribuisci il lavoro richiesto totale che viene stimato per l'attività allocando un determinato numero di ore di lavoro richiesto per periodo di tempo unitario nella scala temporale selezionata. La modalità attività determina il modo in cui il lavoro richiesto viene allocato per la durata dell'attività. I due tipi di allocazione sono **Uniforme** e **Basata su ore lavorative**.

### <a name="work-hours-based-allocation"></a>Allocazione basata su ore lavorative
 
Nella modalità attività pianificata automaticamente, le ore predefinite giornaliere per le risorse dell'attività sono impostate sulla tariffa oraria di lavoro completa. Questo comportamento viene applicato quando l'allocazione del lavoro richiesto ne comporta la distribuzione sulla durata dell'attività nella vista su scala cronologica. Ad esempio, se stimi che un'attività verrà completata da una risorsa nella scala temporale **Giorno**, il lavoro richiesto allocato al giorno non supererà le ore lavorative giornaliere definite nel calendario di progetto. Pertanto, l'allocazione del lavoro richiesto assicura sempre che le risorse vengono stimate per un utilizzo durante un giorno intero.

### <a name="even-allocation"></a>Allocazione uniforme

Nella modalità attività pianificata manualmente, le ore lavorative nel calendario di progetto non sono utilizzate. La pianificazione dell'attività è basata sull'input utente. Per tali attività, l'allocazione del lavoro richiesto per periodo di tempo unitario nella scala temporale selezionata non ha alcun fattore di limitazione. Il lavoro richiesto totale per l'attività viene suddiviso equamente e allocato per ogni periodo di tempo unitario nella scala temporale scelta. Di conseguenza, la modalità attività definita nell'attività determina la distribuzione del lavoro richiesto oppure l'allocazione di tale lavoro per periodo di tempo unitario in stime su scala cronologica.

## <a name="grouping-and-time-phasing-options"></a>Opzioni di raggruppamento e suddivisione in fase

La vista su scala cronologica visualizza la distribuzione delle stime di lavoro richiesto, costi e vendite su base giornaliera, settimanale o annuale. Per impostazione predefinita, i dati delle stime sono basati sulla dimensione **Ruolo**. Tuttavia, puoi utilizzare l'opzione **Raggruppa** affinché siano basati su altre due dimensioni: **Categoria** e **Risorsa**.

Nella vista griglia e nella vista su scala cronologica, puoi scegliere i campi da visualizzare. I totali di ogni blocco di tempo sono visualizzati nella parte inferiore del progetto. Questi mostrano i totali stimati di costi, vendite e lavoro richiesto per giorno, settimana, mese o anno. Il prezzo di costo e quello di vendita predefiniti dipendono dalla data. In altre parole cambiano per ogni risorsa, in base alla vista su scala cronologica selezionata.

## <a name="expense-estimates"></a>Stime di spesa

Il pulsante **Aggiungi una nuova stima di spesa** nella vista griglia ti consente di registrare tutte le spese del progetto che non sono direttamente correlate alla manodopera. Puoi registrare le stime di spesa per una specifica attività o per l'intero progetto. Seleziona le categorie di spesa e la data possibile in cui prevedi di avere delle spese. Se il listino prezzi di costo e il listino prezzi di vendita associati hanno prezzi predefiniti (o se le percentuali di ricarico sono definite per le categorie di spesa), sono automaticamente immessi nella riga di stima al momento dell'associazione.


[!INCLUDE[footer-include](../includes/footer-banner.md)]