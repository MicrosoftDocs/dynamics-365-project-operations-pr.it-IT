---
title: Note spese riprogettate
description: Questo argomento fornisce informazioni sull'esperienza riprogettata e reinventata per l'inserimento della nota spese in Microsoft Dynamics 365 Finance. La nuova esperienza semplifica il processo di completamento delle note spese e riduce il tempo necessario.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f2acd9eab52629b0baeb82a399993fbc6337c722
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650144"
---
# <a name="redesigned-expense-reports"></a>Note spese riprogettate
[!include[banner](../includes/banner.md)]

L'immissione della nota spese è stata riprogettata per semplificare il processo di completamento delle note spese e ridurre il tempo necessario. Ecco le componenti principali della nuova esperienza di spesa:

- Una nuova area di lavoro per la gestione delle spese che ti consente di accedere alle spese del tuo delegato.
- Una nuova esperienza di abbinamento delle ricevute per mostrare meglio le ricevute a livello di intestazione e semplificare il processo per allegare le ricevute alle righe di spesa.
- Una nuova griglia di sola lettura che consente di visualizzare molte più righe di spesa e colonne di dati aggiuntive. È ora possibile visualizzare tutte le righe dettagliate e suddivise, insieme alle spese padre.
- Un riquadro semplificato per la modifica delle spese.
- Messaggi di errore, di avviso e di criteri riprogettati per fornire il contesto corretto per comprendere il problema e come risolverlo. Microsoft ha rimosso molti messaggi che apparivano prima che gli utenti avessero l'opportunità di completare le loro attività e risolvere i problemi, come il messaggio di classificazione incompleta.
- Una nuova pagina per specificare quali campi sono richiesti dalla tua organizzazione, quali campi sono facoltativi e quali campi non devono essere acquisiti. Questa pagina aiuta a ridurre il numero di campi che devono essere impostati dagli utenti.
- Un nuovo aspetto per le note spese, in modo che le relazioni non sembrino più progettate per gli utenti tipo della contabilità.

Per attivare la nuova esperienza, utilizza l'area di lavoro **Gestione delle funzionalità** per attivare la funzionalità **Note spese riprogettate**. Quando attivi questa funzionalità, si verificano le seguenti azioni:

- L'area di lavoro esistente per le spese viene sostituita con la nuova area di lavoro.
- Viene aggiunta una nuova voce di menu per la visibilità del campo di spesa.
- Nessuna voce di menu esistente per le note spese (la pagina esistente) o i campi della nota spese viene rimossa.
- I flussi di lavoro e le eventuali approvazioni ti portano comunque alla pagina delle note spese esistenti.

## <a name="getting-started-video-for-new-users"></a>Video di informazioni generali per i nuovi utenti

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Il video [Esperienza di spesa in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (mostrato sopra) è incluso nella [playlist di Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) disponibile su YouTube.

## <a name="new-features"></a>Nuove funzionalità

| Nuova funzionalità | Descrizione |
|---|----|
| Visibilità del campo di spesa | Una nuova pagina di configurazione consente di specificare quali campi devono essere disabilitati per un'organizzazione, quali campi devono essere obbligatori e quali sono consigliati. |
| Campi obbligatori | La nuova configurazione semplice consente di rendere obbligatori alcuni campi senza dover utilizzare il framework dei criteri. |
| Campi facoltativi | Viene aggiunta una seconda pagina per i campi facoltativi. In questo modo, i dipendenti non si sentiranno obbligati a impostare i campi, ma i campi sono comunque facilmente accessibili. |
| Aggiungere ricevute non allegate | La possibilità di aggiungere ricevute non allegate alla nota spese è più visibile dall'area di lavoro e nella nota spese. |
| Messaggistica migliorata | La visibilità nelle righe di spesa che contengono avvisi o errori è migliore. |
| Riduzione dei messaggi nella barra dei messaggi| Il numero di messaggi Infolog è stato ridotto e in molti casi è stato fatto uno sforzo per impedire la visualizzazione di messaggi duplicati. |
| Azioni comuni raggruppate | L'interfaccia è stata ripulita con l'aggiunta di un nuovo pulsante di azioni per la maggior parte delle azioni comuni a livello di riga e l'aggiunta di un pulsante con i puntini di sospensione (...) per l'intestazione e altre azioni meno frequenti. |
| Nuova area di lavoro per aumentare la visibilità | Una nuova area di lavoro unifica funzionalità e collegamenti che consentono agli utenti di spostarsi in aree diverse. |
| Aggiungere le spese e le ricevute esistenti durante la creazione delle spese | Quando si creano note spese, è possibile aggiungere le spese e le ricevute selezionate o tutte. |
| Calcolatore del tasso di cambio | Viene aggiunto un calcolatore del tasso di cambio che consente di calcolare il tasso di cambio per le transazioni multivaluta vive. |
| Salvare e aggiungere nuove righe di spesa | I pulsanti **Salva** e **Nuovo** sono disponibili quando vengono inserite nuove spese, per aiutarti a inserire rapidamente le righe di spesa. |
| Migliore visibilità nelle righe suddivise e dettagliate | Le righe dettagliate e suddivise vengono aggiunte direttamente all'elenco delle spese per aumentare la visibilità e aiutarti a determinare facilmente se ci sono errori di criteri o altri errori. |
| Mostrare le ricevute durante la classificazione | Le ricevute possono essere mostrate durante la classificazione. |

La versione iniziale si concentra sugli scenari di registrazione delle spese. Qualsiasi scenario di revisione o approvazione della nota spese continuerà a utilizzare la pagina di registrazione delle spese esistente.

Le seguenti funzionalità sono presenti nella pagina esistente ma non sono ancora presenti nella nuova pagina. Queste funzionalità verranno reintrodotte nelle prossime versioni:

- Approvazioni
- Approvazione contabilità fornitori e possibilità di modificare la contabilità
- Più punti di ingresso
- Integrazione della richiesta di viaggio
- Entità di dati per la visibilità del campo di spesa
- Inserimento delle spese giornaliere
- Flusso di lavoro a livello di riga
- Supporto per approvatori provvisori
- Classificazione avanzata
