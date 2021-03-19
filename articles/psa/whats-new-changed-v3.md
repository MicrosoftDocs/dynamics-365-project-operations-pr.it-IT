---
title: Novità o modifiche in Project Service Automation versione 3
description: Questo argomento fornisce informazioni sulle novità e sulle modifiche in Project Service Automation versione 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2388aedec25915b3d364001fed11ca537b0f5507
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281123"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Novità o modifiche in Project Service Automation versione 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In questo argomento vengono fornite informazioni sulle modifiche all'interfaccia utente, alle funzionalità e alla terminologia di Project Service Automation tra la versione 2 o la versione 1 e la versione 3.

## <a name="project-scheduling"></a>Pianificazione di progetti
La pianificazione di progetti, nota come struttura di suddivisione del lavoro nelle versioni precedenti, è stata rinominata Pianificazione ed è possibile accedervi facendo clic sulla scheda **Pianifica**. 

![Pianificazione di progetti](media/psa-schedule-01.png)

La pianificazione ora ha una nuova superficie per l'interazione moderna e accessibile. Tuttavia, il motore di pianificazione di Project Service Automation sottostante non è cambiato. I pulsanti di controllo nella barra multifunzione della griglia di pianificazione ti consentono di interagire con la pianificazione come nella versione precedente di Project Service Automation. Ulteriori modifiche alla pianificazione includono:

- **Diagramma di Gantt** - Il diagramma di Gantt non è più disponibile. Una nuova visualizzazione di Gannt verrà inclusa in un aggiornamento futuro.
- **Intestazioni di colonne** - Puoi nascondere le intestazioni di colonne nella griglia facendo clic su un indicatore accanto al titolo della colonna. 
- **Colonne** - Puoi rendere visibili le colonne nascoste facendo clic su **Aggiungi colonna**. 
- **Categoria di transazione** - Un campo di ricerca **Categoria di transazione** è stato aggiunto alla griglia di pianificazione ed è visualizzato per impostazione predefinita. 
 
## <a name="project-templates"></a>Modelli di progetto
Le modifiche seguenti sono state apportate alla funzionalità dei modelli di progetto.

### <a name="create-a-project-template"></a>Creare un modello di progetto 
Puoi creare un modello di progetto nella versione 3 come nelle versioni precedente di Project Service Automation. Il modello può contenere solo una pianificazione e la pianificazione può includere assegnazioni, che tuttavia non sono obbligatorie. Se la pianificazione ha delle assegnazioni, queste possono essere applicate solo a risorse generiche. Puoi generare requisiti di risorsa per le risorse generiche, che non possono essere prenotate con risorse reali nel modello. Non puoi prenotare una risorsa reale per un team in un modello. 

### <a name="create-a-template-from-an-existing-template"></a>Creare un modello da un modello esistente
Quando crei un nuovo modello di progetto da un modello esistente in Project Service Automation versione 3, si verifica quanto segue: 

- La pianificazione del progetto di origine viene copiata nel modello. 
- Le risorse generiche vengono copiate nel team e vengono copiate tutte le assegnazioni di risorse generiche. I requisiti per le risorse generiche non vengono copiati. 

### <a name="create-a-template-from-an-existing-project"></a>Creare un modello da un progetto esistente
Quando crei un nuovo modello di progetto da un progetto esistente, si verifica quanto segue: 

- La pianificazione del progetto di origine viene copiata nel modello. 
- Le risorse generiche vengono copiate nel team e tutte le assegnazioni di risorse generiche vengono mantenute. I requisiti per le risorse generiche non vengono copiati.    
- Le risorse denominate, assegnate o non assegnate, vengono rimosse dal team e sostituite con risorse generiche.
- Se presenti, le informazioni sui clienti vengono rimosse. 
- Se presenti, i riferimenti alle offerte e ai contratti vengono rimossi. 

### <a name="create-a-project-from-a-template"></a>Crea un progetto da un modello
Quando crei un nuovo modello di progetto da un modello esistente in Project Service Automation versione 3, si verifica quanto segue:

- La pianificazione, il team e le assegnazioni vengono copiati nel nuovo progetto.   
- La data di inizio è la data della copia o la data selezionata dall'utente.   
- Per qualsiasi membro del team generico con requisiti di risorsa nel modello, i requisiti non vengono copiati o generati automaticamente. Devi generarli personalmente. 

## <a name="copy-a-project"></a>Copiare un progetto
Quando copi un progetto in Project Service Automation versione 3, si verifica quanto segue: 

- La data di inizio stimata viene copiata ma può essere modificata.  
- La pianificazione e le attività di progetto vengono copiate. 
- Le risorse generiche e le relative assegnazioni vengono copiate. I requisiti di risorsa per le risorse generiche non vengono copiati. Devi rigenerarli. 
- Le risorse reali e le relative assegnazioni non vengono copiate. Vengono invece sostituite da risorse generiche. 
- I valori effettivi non vengono copiati nel nuovo progetto. 

## <a name="move-a-scheduled-project"></a>Spostare un progetto pianificato
Quando sposti avanti la pianificazione di un progetto esistente, si verifica quanto segue: 

- Le date delle attività vengono spostate automaticamente affinché corrispondano al periodo di spostamento. 
- Le risorse generiche assegnate rimangono assegnate.   
- Se vengono generate prima dello spostamento del progetto, i requisiti per le risorse generiche rimangono invariati e non vengono rigenerati automaticamente. Dovrai generarle di nuovo per riflettere le nuove assegnazioni dovute allo spostamento delle attività. 
- Le assegnazioni delle risorse reali cambiano per corrispondere allo spostamento delle date delle assegnazioni. Le prenotazioni delle risorse reali non cambiano. Devi modificare le prenotazioni mediante la vista Riconciliazione. 
- Le risorse del team con prenotazioni ma senza assegnazioni non cambiano. 
- I valori effettivi non vengono spostati. 

## <a name="estimates"></a>Stime
Le stime sono state suddivise in due schede, **Assegnazione risorse** e **Stime**. La scheda **Assegnazione risorse** contiene le stime del lavoro richiesto e mostra le assegnazioni delle risorse per le attività in una vista su scala cronologica. Puoi modificare le stime in funzione di quanto generato dal motore di pianificazione.

![Scheda Assegnazioni risorse con stime del lavoro richiesto e assegnazioni delle risorse per le attività](media/resource-assignments-tab-02.png)

La scheda **Stime** mostra gli importi di costo e di vendite per le assegnazioni delle risorse. Gli importi sono di sola lettura. La determinazione dei costi e quella dei prezzi di vendita sono ora basate sulle assegnazioni dei membri del team nella pianificazione. Ciò significa che se hai un'attività senza assegnazioni, questa viene visualizzata sotto il bucket non assegnato. Ciò significa anche che senza **ruolo**, ovvero una dimensione di determinazione dei prezzi predefinita, non si ha una vendita o un costo stimato se un cliente o un contratto/offerta è associato al progetto. 

![Scheda Stime che mostra importi di costo e vendite](media/estimates-tab-03.png)
  
La categoria è supportata anche per le attività nella vista Pianifica. Il raggruppamento per categoria nella vista su scala cronologica delle stime fornirà una migliore esperienza, soprattutto quando sono disponibili anche stime di spesa nel progetto. Le stime di spesa vengono immesse utilizzando una griglia in una scheda distinta. 

Le stime di spesa possono essere immesse nella griglia nella scheda **Stime di spesa**. 

![Scheda Stime di spesa con la griglia delle stime di spesa](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Gestione risorse
In Project Service Automation versione 3, con la nuova interfaccia utente e le modifiche nella relazione tra prenotazioni e assegnazioni, l'assegnazione di risorse generiche o reali a un progetto è cambiata in modo considerevole rispetto alla versione 2 e alla versione 1. Tuttavia, i concetti di risorse prenotabili, **reali** e **generiche**, rimangono invariati, così come i membri del team, i requisiti, le assegnazioni e le prenotazioni.   

![Utilizzare il selettore di risorse](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Assegnare una risorsa prenotabile reale 
In Project Service Automation versione 3, le prenotazioni e le assegnazioni di attività non sono strettamente intrecciate come nelle versioni precedenti di Project Service Automation. Puoi utilizzare la griglia del team per prenotare un membro del team **reale**, come con le versioni sul mercato.

Utilizzando il selettore di risorse nella pianificazione, puoi selezionare il membro del team creato nella vista del team e quindi assegnarlo ad attività. Puoi continuare ad assegnargli attività anche dopo le sue prenotazioni. Utilizza la scheda **Riconciliazione** per riconciliare i membri del team che presentano differenze tra prenotazioni e assegnazioni.

Il selettore di risorse visualizza i membri del team per il progetto. Puoi anche utilizzare il selettore di risorse per cercare e visualizzare altre risorse prenotabili che non fanno parte del team di progetto. Puoi assegnarle a un'attività di modo che facciano parte del team di progetto. Devi prenotarle utilizzando la **scheda di pianificazione** o la scheda **Riconciliazione**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Assegnare una risorsa prenotabile generica a un'attività e a un team di progetto e utilizzare una risorsa reale tramite la scheda di pianificazione 
In Project Service Automation versione 3, la funzionalità di generazione di team non viene utilizzata per le risorse generiche. Puoi invece creare e assegnare direttamente una risorsa generica dalla pianificazione digitando il nome posizione di tale risorsa nella cella di risorsa della pianificazione. Oppure puoi selezionare l'icona della risorsa nella cella e quindi, tramite il selettore di risorse, digitare il nome della risorsa generica che intendi creare. Viene aperto un pannello di creazione rapida che consente di impostare il ruolo e l'unità organizzativa del membro del team di risorse generiche. Dopo la creazione della risorsa, questa viene assegnata all'attività e puoi continuare ad assegnare tale risorsa generica ad altre attività nella pianificazione.    
 
Quando hai assegnato la risorsa a tutte le attività appropriate, puoi generare un requisito di risorse e quindi soddisfarlo prenotando direttamente con la **scheda di pianificazione** o inviando una richiesta di risorse. Puoi anche aggiungere risorse generiche direttamente alla griglia del membro del team. 

Le risorse generiche sono aggiunte al team di progetto senza requisiti di risorsa e con le date di inizio/fine del progetto fino a che il requisito di risorsa non viene generato. Per generare un requisito, seleziona la risorsa generica e fai clic su **Genera**. Il collegamento del requisito viene ora visualizzato e le ore richieste vengono popolate con le ore assegnate. Puoi fare clic sul collegamento per aprire e aggiornare il requisito.
  
Quando la prenotazione viene completata e soddisfatta completamente con una risorsa, denominata, la risorsa generica viene sostituita con la risorsa denominata e l'assegnazione nella pianificazione viene aggiornata con tale risorsa. 

Le risorse proposte per i requisiti sono ora archiviate in una scheda anziché in una sezione distinta.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Soddisfare la capacità di una risorsa generica con molteplici risorse denominate
Quando un requisito viene soddisfatto con molteplici risorse, la risorsa generica rimane nel team e assegnata all'attività. I membri del team denominati prenotati non sono assegnati come parte della posizione. Il responsabile di progetto può assegnare il lavoro come appropriato alle risorse reali.  La vista **Riconciliazione** fornisce una ripartizione delle prenotazioni tra più risorse per molteplici assegnazioni di attività. Questa operazione non viene eseguita automaticamente in quanto negli scenari più complessi, come nel caso in cui il requisito è costituito da un gruppo di attività, è necessario supporre l'intenzione con la quale il responsabile di progetto desidera eseguire le assegnazioni. Poiché il sistema non può comprendere l'intenzione, è probabile che quanto supposto sia differente da quanto previsto e quindi si avrà un risultato incorretto o imprevedibile. Il risultato prevedibile è che la risorsa generica rimane assegnata fino a che il responsabile di progetto non assegna deliberatamente le risorse utilizzando la vista **Riconciliazione**.

### <a name="reconciliation"></a>Riconciliazione
La scheda **Riconciliazione** mostra le prenotazioni e tutte le assegnazioni di ogni membro del team di progetto. La vista mostra le ore nelle celle che possono rappresentare periodi di tempo da mesi fino a giorni. Questa vista consente ai responsabili di progetto di riconciliare le prenotazioni dei membri del team e le relative assegnazioni per il team di progetto. Ciò è utile in quanto le prenotazioni e le assegnazioni di attività non sono strettamente vincolate, consentendo una maggiore flessibilità nella pianificazione di un progetto. 

![Scheda Riconciliazione che mostra prenotazioni e assegnazioni per i membri del team di progetto](media/resource-reconciliation-tab-06.png)

Per ogni risorsa, la vista calcola la differenza tra le prenotazioni di un membro del team e un rollup delle relative assegnazioni di attività e mostra le seguenti due differenze che possono verificarsi con prenotazioni e assegnazioni in un progetto: 

- **Prenotazione insufficiente** - Le prenotazioni sono insufficienti quando una risorsa ha più assegnazioni che prenotazioni. Poiché questa capacità non è stata riservata, un responsabile di progetto può correggere questa condizione estendendo le prenotazioni della risorsa per compensare l'insufficienza. 
- **Prenotazioni in eccesso** - Le prenotazioni in eccesso si hanno quando una risorsa è stata prenotata per il progetto ma non è stata assegnata ad attività.  Questa condizione può essere accettabile se, ad esempio, la risorsa è stata prenotata prima dell'assegnazione di attività. Tuttavia, in altri casi, la risorsa può non essere pianificata per l'assegnazione e il responsabile di progetto deve prendere in considerazione l'annullamento delle prenotazioni della risorsa per consentire l'utilizzo della capacità con un altro progetto. 

Quando sono presenti assegnazioni di attività per una risorsa senza prenotazioni (prenotazione insufficiente), puoi selezionare la prenotazione insufficiente e quindi fare clic su **Estendi prenotazione**. Puoi quindi visualizzare la prenotazione necessaria per compensare l'insufficienza della risorsa e la relativa disponibilità. 
 
## <a name="time-and-expense"></a>Tempo e spesa
Questa sezione fornisce informazioni sulle modifiche relative a tempo, spese e approvazioni nella versione 3 di Project Service Automation. Come parte della soluzione Dynamics 365 Project Service Automation, la funzionalità **Inserimento ore** è stata aggiornata per utilizzare il framework Unified Interface. Ciò consente di fornire un'interfaccia utente coerente e uniforme che applica i principi di progettazione interattiva per una visualizzazione ottimale su uno schermo o dispositivo di qualsiasi dimensione. 

### <a name="landing-page"></a>Pagina di destinazione
L'esperienza di inserimento ore personalizzata non estendibile è stata deprecata nella versione 3 ed è stata sostituita da un'esperienza di griglia nativa estendibile e accessibile. Puoi accedere alla funzionalità di inserimento ore utilizzando la mappa del sito a sinistra. In seguito a questa modifica, non è più possibile utilizzare un inserimento ore per una settimana alla volta, ma è necessario creare un inserimento ore per ogni giorno nella griglia. Dopo la creazione di alcuni inserimenti ore, gli utenti possono creare inserimenti ore in blocco con la funzione **Copia** descritta oltre in questo argomento. 

![Pagina di destinazione Inserimento ore](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Creare nuovi inserimenti ore 
Fai clic su **Nuovo** nella barra multifunzione per aprire una pagina di creazione rapida per l'inserimento ore dove immettere la durata in minuti, ore o giorni. A tale scopo, digita h, m oppure d con la quantità.  

![Creazione rapida inserimento ore](media/quick-create-time-entry-08.png)

I campi di ricerca sono supportati da viste di sistema. Ad esempio, dopo l'immissione di informazioni sul progetto, per impostazione predefinita il campo **Attività di progetto** viene impostato sulla vista **Attività di progetto personali aperte**. Per creare inserimenti ore per le attività non assegnate all'utente, fai clic su **Cambia vista** nella finestra di dialogo di ricerca e quindi seleziona **Tutte le attività di progetto attive**. Dopo la creazione e la visualizzazione dell'inserimento ore nella vista, puoi modificare qualsiasi valore di riga direttamente nella griglia.  

### <a name="bulk-createcopy"></a>Creare/copiare in blocco 
Dopo la creazione di alcuni inserimenti ore, puoi utilizzare la funzionalità di copia per creare ulteriori inserimenti ore in blocco. Fai clic su **Copia** per aprire la finestra di dialogo **Copia**. In **Dal periodo: Data di inizio**, imposta l'intervallo di date a partire dal quale le date devono essere copiate. In **Al periodo: Data di inizio**, specifica la data per la quale è necessario creare inserimenti ore. Fai clic su **Copia** per copiare gli inserimenti ore nel giorno della settimana corrispondente indicato in **Al periodo**. Ad esempio, l'inserimento ore di lunedì dell'ultima settimana viene copiato nel lunedì della settimana indicata in **Al periodo**. 

![Copiare inserimenti ore in blocco](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importa dati 
Le assegnazioni e gli scambi seguono lo stesso modello di interfaccia utente e ciò consente all'utente di specificare l'intervallo di date a partire dal quale le prenotazioni devono essere importate. Devi quindi scegliere in modo esplicito le prenotazioni che devono essere copiate negli inserimenti ore **Bozza**. Nella versione 3, non è più possibile visualizzare il modello degli inserimenti ore **Consigliato** nella griglia e nel calendario.  

### <a name="change-in-calendar-control"></a>Modifica del controllo calendario
Nella versione 3 il controllo calendario personalizzato è stato deprecato e viene ora utilizzato il calendario UC per visualizzare gli inserimenti ore per la settimana. Con questo calendario è possibile visualizzare il giorno, la settimana e il mese. 

> [!NOTE]
> Una limitazione del calendario è che questo controllo non supporta azioni su singoli elementi del calendario. Ad esempio, non è possibile selezionare uno o più elementi del calendario e inviare o eliminare tali elementi. Fai clic su un elemento del calendario per aprire la pagina **Inserimento ore** per azioni aggiuntive. 

### <a name="extensibility"></a>Estendibilità
**Acquisire dati nei campi personalizzati unicamente nelle entità Inserimento ore e Voce di spesa** - Inserimento ore utilizza una griglia modificabile, una griglia di sola lettura e controlli del calendario a partire dalla piattaforma. Tutti questi controlli sono nativi e quindi supportano le personalizzazioni. In Project Service Automation versione 3, è possibile aggiungere ulteriori campi personalizzati, impostare campi di ricerca e creare viste personalizzate. Puoi inoltre impostare logica di business personalizzata basata sui valori selezionati nei campi personalizzati.  

**Acquisire dati nei campi personalizzati di inserimenti ore e voci di spesa e propagarli mediante entità che supportano il flusso di invio e approvazione** - L'elaborazione tipica degli inserimenti ore è illustrata nel diagramma seguente.

![Flusso di elaborazione di inserimenti ore](media/process-time-entries-10.png)

Se i requisiti aziendali stipulano che le entità di tempo e spesa devono acquisire dimensioni di determinazione dei prezzi personalizzate e propagare i valori impostati da una risorsa di tempo e spesa nella dimensione di determinazione dei prezzi personalizzata mediante tutte le entità nel grafico precedente, vedi [Impostare campi personalizzati come dimensioni di determinazione dei prezzi](set-up-pricing-dimensions.md)

Per supportare requisiti aziendali dove le entità di tempo e spesa devono acquisire dimensioni non di determinazione dei prezzi personalizzate e propagare i valori, puoi utilizzare la configurazione delle dimensioni di determinazione dei prezzi ed esprimere le dimensioni personalizzate come dimensioni di determinazione dei prezzi senza tassi di costo o fatturazione. Un altro scenario sarebbe aggiungere un campo personalizzato a ogni entità, utilizzando lo stesso nome di campo in tutte le entità. Puoi creare plug-in personalizzati per associare record nelle entità che partecipano al flusso di invio/approvazione utilizzando entità di origine delle transazioni e di connessione delle transazioni.  

### <a name="delegate-time-and-expense-entry"></a>Delegare inserimenti ore e voci di spesa
La piattaforma Common Data Service non consente a un utente di impersonare un altro utente, di conseguenza la versione 3 di Project Service Automation non supporta gli inserimenti ore e le voci di spesa delegati. Tuttavia, partner e clienti hanno trovato una soluzione alternativa per consentire il supporto delle esperienze di inserimenti ore delegati nella versione 3. Si tratta soltanto di una soluzione alternativa e non di una soluzione completa, pertanto è importante comprenderne i limiti e utilizzare questo approccio solo tali limiti sono accettabili. 

> [!IMPORTANT]
> Tali informazioni devono essere considerate soltanto come un suggerimento per un'implementazione personalizzata da parte di un partner/cliente. Il team del prodotto non offre alcun supporto formale per questa funzionalità attraverso i suoi canali di supporto.

### <a name="customization-details"></a>Dettagli sulla personalizzazione 
Con la personalizzazione è possibile aggiungere **Risorsa prenotabile** alle esperienze di creazione e modifica, le quali consentono a un utente di agire come delegato modificando il campo **Prenotazione risorsa** di un altro utente per il quale è necessario registrare inserimenti ore e voci di spesa. I passaggi seguenti sono relativi alla delega degli inserimenti ore. Le stesse informazioni si applicano alla delega delle voci di spesa. 
 
1.  Verifica che l'utente delegato disponga di un accesso di sicurezza globale per i progetti e le attività di progetto. 
1.  Poiché **Risorsa prenotabile**, che è un campo nell'entità **Inserimento ore**, non viene esposto nella pagina **Creazione rapida**, devi aggiungerlo.

    -oppure-

    Crea una vista personalizzata che include la colonna **Risorsa prenotabile** per visualizzare solo gli inserimenti ore creati per la risorsa. Pubblica le personalizzazioni nella finestra di progettazione del modulo dell'app affinché questa vista sia visualizzata sotto **Selettore vista** nella pagina **Inserimenti ore**. Esistono due plug-in che gestiscono la configurazione del responsabile per gli inserimenti ore non di progetto:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Crea un nuovo plug-in per sovrascrivere il campo **Responsabile** con il responsabile dell'utente assegnato nel campo **Risorsa prenotabile**. Utilizza la stessa **Fase esecuzione** del plug-in out-of-band (OOB) (pre-convalida) e un **Ordine esecuzione** superiore ai plug-in OOB (maggiore di 1). Ciò assicurerà l'esecuzione del plug-in personalizzato dopo i plug-in OOB.  
 
### <a name="end-user-experience"></a>Esperienza dell'utente finale
1.  Quando crei un inserimento ore nella pagina di creazione rapida, immetti i dettagli di progetto e attività di progetto e quindi nel campo **Risorsa prenotabile** scegli l'utente per il quale è necessario registrate gli inserimenti ore. 
2.  Per impostazione predefinita, questo campo viene impostato sull'utente collegato; tuttavia, dato che l'utente ha sostituito tale campo, l'inserimento ore viene creato per la **Risorsa prenotabile** scelta.
3.  Quando invii gli inserimenti ore creati per tali record, questi vengono messi in coda per il responsabile approvazione del progetto come previsto. 
4.  Quando richiami gli inserimenti ore creati per l'altro utente, gli inserimenti ore ritornano allo stato **Bozza** con il campo **Risorsa prenotabile** impostato per l'altro utente. 
5.  Se lo desideri, puoi passare alla vista personalizzata per filtrare gli inserimenti ore creati per l'altro utente. 
 
### <a name="limitations"></a>Limitazioni
Le funzionalità **Copia** e **Importa** funzionano solo nel contesto dell'utente collegato. Ciò significa che non è possibile copiare o importare inserimenti ore creati per l'utente collegato come risorsa prenotabile.

Gli inserimenti ore non creati per un progetto vengono indirizzati per l'approvazione al responsabile della risorsa prenotabile solo se il passaggio 4 nella sezione **Dettagli sulla personalizzazione** vista precedentemente è stato completato. In caso contrario, gli inserimenti ore non di progetto per l'altro utente vengono indirizzati in modo non corretto al responsabile dell'utente connesso. 

### <a name="other-changes"></a>Altre modifiche 
La funzionalità **Prenotazioni e attività** è stata rimossa. 

## <a name="multidimensional-pricing"></a>Determinazione dei prezzi multidimensionale
Per massimizzare la flessibilità e soddisfare i differenti requisiti aziendali, la versione 3 di Project Service Automation supporta l'applicazione discreta di set di dimensioni di determinazione dei prezzi a tassi di costo e fatturazione. I valori delle dimensioni possono essere impostati come predefiniti e quindi propagati al processo di determinazione di prezzi e costi dal profilo delle risorse all'inserimento ore ai valori effettivi di progetto. La configurazione e la modifica o l'estensione specifica del cliente utilizzano l'infrastruttura di personalizzazione standard.

Project Service Automation include un set predefinito di dimensioni di determinazione dei prezzi, ruoli e unità di risorsa e consente la configurazione di prezzi e costi per ogni combinazione di ruolo e unità organizzativa.

Per i clienti di Project Service Automation che desiderano continuare a utilizzare questi campi predefiniti come dimensioni di determinazione dei prezzi nella versione 3, non vi sono altre modifiche osservabili. Puoi continuare a utilizzare Project Service Automation come di consueto. Se, tuttavia, devi determinare prezzi o costi per le risorse utilizzando ulteriori attributi, la versione 3 consente l'aggiunta di dimensioni di determinazione dei prezzi personalizzate a Project Service Automation. L'estensione delle dimensioni di determinazione dei prezzi è un'esperienza di configurazione complessa. 

## <a name="quotes-and-contracts"></a>Offerte e contratti
Nella versione 3 di Project Service Automation, gli aspetti di configurazione e gestione di offerte e contratti sono stati modificati. Le sezioni seguenti forniscono informazioni più dettagliate.

### <a name="set-up-chargeability-options"></a>Configurare opzioni di esigibilità
Nelle versioni 1 e 2, la configurazione delle opzioni di esigibilità di ruoli e categorie per specifiche offerte e contratti veniva eseguita utilizzando la vista **Esigibilità**, accessibile dalla barra di navigazione superiore di una riga di offerta o di una voce di contratto. Questa vista consentiva inoltre di configurare i prezzi per tali ruoli e categorie di spesa.

A partire dalla versione 3, la configurazione delle opzioni di esigibilità per ruolo e categoria di spesa viene eseguito a livello di riga di offerta o di voce di contratto. La configurazione della funzionalità di determinazione dei prezzi è distinta da quella dell'esigibilità. Puoi trovare i **Ruoli addebitabili** e le **Categorie addebitabili** come schede nelle pagine **Riga di offerta** e **Voce di contratto** senza dover utilizzare la barra di navigazione superiore.

![Ruoli addebitabili](media/chargeable-12.png)
 
La configurazione dei ruoli addebitabili e delle categorie addebitabili utilizza anche il controllo di griglia modificabile predefinito. Per ogni ruolo e categoria, le opzioni supportate per il tipo di fatturazione durante le fasi Offerta e Contratto rimangono invariate (**Addebitabile** e **Non addebitabile**) rispetto alle versioni precedenti. **Gratuito** non è un tipo supportato durante la fase Offerta o Contratto. **Gratuito** è supportato solo durante l'approvazione di tempo o spese.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Creare e modificare la funzionalità di determinazione dei prezzi personalizzata per un'offerta e un contratto di progetto di Project Service Automation
Nelle versioni 1 e 2, l'utilizzo del listino prezzi personalizzato per specifici contratti e offerte era possibile mediante l'opzione **Modifica prezzi** nella vista **Esigibilità**. La vista **Esigibilità** si trovava nella barra di navigazione superiore di una riga di offerta o di una voce di contratto. In questa vista era anche possibile configurare le opzioni di esigibilità per ruoli e categorie di spesa.

A partire dalla versione 3, la procedura di creazione e utilizzo di un listino prezzi di progetto personalizzato in un offerta e in un contratto di progetto Project Service Automation è stata separata dalla configurazione dell'esigibilità. L'offerta e e i contratti di progetto Project Service Automation presentano una nuova scheda denominata **e i contratti di progetto**. Questa scheda mostra una vista associata di tutti i listini prezzo di progetto associati a un'offerta o a un contratto di progetto Project Service Automation. Per creare un listino prezzi personalizzato da un listino prezzi esistente già associato all'offerta o al contratto di progetto, fai clic su **Crea determinazione dei prezzi personalizzata**. Ciò crea una copia di tutti i listini prezzi associati e li collega all'offerta o al contratto. Ora puoi aprire il listino prezzi e modificare il prezzo del ruolo o della categoria di spese di modo che queste modifiche alla determinazione dei prezzi siano applicate a tale offerta o contratto. 
  
Nel grafico seguente non sono visualizzati i listini prezzi personalizzati che sono stati creati.

![Listini prezzi personalizzati precedenti](media/before-custom-price-lists-13.png)

Nel grafico seguente sono visualizzati i listini prezzi personalizzati che sono stati creati.

![Listini prezzi successivi](media/after-custom-price-lists-14.png)

> [!NOTE]
> È possibile che la creazione di un listino prezzi non sia immediata dopo che fai clic su **Crea determinazione dei prezzi personalizzata**. È consigliabile aggiornare la griglia anziché fare clic più volte. Un listino prezzi personalizzato viene creato se il nome di listino prezzi associato include il nome dell'offerta o il nome del contratto di progetto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]