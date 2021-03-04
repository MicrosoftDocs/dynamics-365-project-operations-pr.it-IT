---
title: Aggiungere membri del team dalla griglia dei membri del team
description: In questo argomento vengono fornite informazioni su come gestire le risorse membri del team.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: de73dac28046ec98ed201e129be6511f894223fd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121538"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Aggiungere membri del team dalla griglia dei membri del team

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations include una dashboard Resource Manager che fornisce una panoramica visiva della domanda e dell'utilizzo delle risorse nell'organizzazione. Puoi utilizzare i grafici di questo dashboard per visualizzare le informazioni seguenti:

- **Richiesta di risorse**: il grafico **Richieste risorse attive** visualizza le risorse che sono state inviate. Le risorse sono aggregate per ruolo o progetto.
- **Richiesta di risorse non inviata**: il grafico **Richiesta di risorse non inviata** visualizza tutti i requisiti di risorsa che non sono stati inviati. Questo grafico Consente ai responsabili delle risorse di visualizzare la richiesta che non è definitiva e che può essere inviata tramite una richiesta di risorse.
- **Utilizzo fatturabile per la settimana passata**: il grafico **Utilizzo per ruolo** visualizza la percentuale dell'utilizzo fatturabile effettivo dell'organizzazione per ruolo rispetto al relativo utilizzo fatturabile di destinazione per ruolo.

    > [!NOTE]
    > Per rendere disponibile il grafico **Utilizzo per ruolo**, crea un processo che esegue il flusso di lavoro **UpdateRoleUtilization**. Questo processo ricorrente viene eseguito ogni sette giorni per calcolare l'utilizzo fatturabile dei sette giorni precedenti. I risultati sono aggregati per ruolo.

## <a name="manage-project-team-members"></a>Gestire membri del team di progetto

I responsabili di progetto possono utilizzare il dashboard dei responsabili delle risorse per gestire le risorse nei progetti. Ad esempio, possono aggiungere un membro del team direttamente a un progetto e prenotare un membro del team per soddisfare i requisiti di risorsa acquisiti da una risorsa generica.

### <a name="add-a-team-member-directly-to-a-project"></a>Aggiungere un membro del team direttamente a un progetto

Per aggiungere un membro del team direttamente a un progetto, nel modulo **Progetti**, nella scheda **Team**, seleziona **Nuovo**. Viene visualizzata la finestra di dialogo **Creazione rapida: Membro del team di progetto**. In questa finestra di dialogo, puoi eseguire le seguenti attività:

- **Prenotare una risorsa denominata**: nel campo **Risorsa prenotabile**, seleziona il nome della risorsa. Quindi seleziona il ruolo, imposta il periodo e seleziona un metodo di allocazione. La risorsa denominata selezionata viene aggiunta al progetto mediante il metodo di allocazione selezionato e il calendario delle risorse.
- **Aggiungere una risorsa generica**: lascia vuoto il campo **Risorsa prenotabile** e quindi seleziona il ruolo, imposta il periodo e seleziona il metodo di allocazione preferito. Una risorsa generica viene aggiunta al team come segnaposto. Il segnaposto contiene il modello di domanda utilizzato per prenotare le risorse con nome nel team. Il requisito viene creato in base al calendario del progetto.
- **Aggiungere una risorsa denominata al team senza consumare la capacità della risorsa**: nel campo **Risorsa prenotabile**, seleziona una risorsa. Seleziona il periodo, quindi seleziona **Nessuno** come metodo di allocazione. La risorsa viene aggiunta al team, ma la capacità della stessa non viene consumata a seguito della prenotazione.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Prenotare un membro del team per soddisfare i requisiti di risorsa di una risorsa generica

In Project Operations è possibile prenotare una risorsa generica per un team di progetto. È inoltre possibile specificare il ruolo, la capacità richiesta e la modalità di distribuzione di tale capacità. Per il requisito di risorsa, puoi specificare gli attributi associati alla risorsa generica. Tali attributi includono le competenze necessarie, l'unità organizzativa preferita e le risorse preferite.

Completa i passaggi seguenti per specificare le competenze necessarie di una risorsa generica per uno sviluppatore.

1. Nel modulo **Progetti**, nella scheda **Team**, seleziona **Nuovo** per prenotare una risorsa generica.
2. Nella vista **Tutti i membri del team**, nella colonna **Requisito di risorsa**, seleziona il collegamento per aggiungere le competenze richieste per la risorsa generica.
3. Nel modulo **Requisito di risorsa** visualizzata, nella griglia **Competenze**, seleziona i puntini di sospensione (**...**) e quindi **Aggiungi caratteristica nuovo requisito** per aggiungere le competenze richieste per lo sviluppatore.
4. Nel modulo **Creazione rapida: Caratteristica requisito** visualizzato, nel campo **Caratteristica**, seleziona la competenza richiesta.
5. Nel campo **Valore di valutazione**, seleziona il livello di esperienza per tale competenza. 
6. Nel campo **Requisito di risorsa**, imposta il requisito per utilizzare risorse delle unità organizzative o persino risorse denominate. Al termine, seleziona **Salva**.
7. Nel modulo **Requisito di risorsa**, seleziona **Prenota** per soddisfare il requisito. Puoi anche selezionare la risorsa generica nella griglia **Tutti i membri del team** e quindi selezionare **Prenota**.

    > [!NOTE]
    > In questo esempio, vi sono 40 ore richieste ma nessuna ora prenotata, in quanto le risorse generiche non hanno prenotazioni. Inoltre, non vi sono ore assegnate, in quanto la risorsa generica è stata aggiunta direttamente al team invece di essere aggiunta tramite l'assegnazione delle attività.

    Nel modulo **Assistente pianificazione**, puoi filtrare le risorse disponibili in base ai requisiti specificati nel requisito di risorsa. Le risorse sono ordinate in base ai parametri di ordinamento specificati nella scheda di pianificazione.

   Alcuni dei filtri più utilizzati sono:

    - **Caratteristiche con una valutazione**: consente di filtrare in base a competenze, certificazioni e altre qualità delle risorse, nonché in base alle valutazioni del livello di preparazione.
    - **Ruoli**: consente di filtrare in base ai ruoli predefiniti assegnati a risorse prenotabili.
    - **Unità organizzative**: consente di filtrare le risorse prenotabili in base alle unità organizzative a cui sono assegnate.

8. Se non sei soddisfatto dei risultati della ricerca iniziale, puoi modificare i criteri di filtro. Espandi il riquadro **Filtra vista** a sinistra e quindi seleziona **Cerca** per trovare ulteriori risorse. Per modificare l'ordinamento dei risultati, seleziona **Ordina**.
9. Seleziona le risorse in base alla richiesta specificata nel requisito, come indicato nella parte superiore della griglia. Puoi annullare la selezione di celle nella griglia e lasciare aperta tale capacità di risorsa. È possibile selezionare una sola una risorsa alla volta come prenotata.
10. Seleziona **Prenota** per prenotare la risorsa selezionata e lasciare aperta la scheda di pianificazione, in modo da poter selezionare ulteriori risorse. In alternativa, seleziona **Prenota e chiudi** per prenotare la risorsa selezionata e chiudere la scheda di pianificazione.
11. Torna alla vista **Tutti i membri del team**. Nella griglia, nota che la risorsa generica è stata sostituita dalla risorsa denominata e che 40 ore sono indicate come prenotate per quella risorsa.

    > [!NOTE]
    > Non sono visualizzate ore assegnate in quanto sono state prenotate direttamente nel team. Non sono state prenotate utilizzando l'assegnazione delle attività.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Assegnare risorse generiche ad attività e generare requisiti di risorsa

In Project Operations, puoi creare attività e quindi assegnarvi risorse generiche. La richiesta di risorse può quindi essere rappresentata da segnaposto mentre stimi la pianificazione e i dati finanziari. Puoi quindi generare requisiti di risorsa per le risorse generiche e soddisfarli.

1. Nel modulo **Progetti**, nella scheda **Pianifica**, seleziona **Aggiungi** per creare un'attività.
2. Nel campo **Risorse**, seleziona il simbolo del **selettore di risorse**. Viene visualizzato il selettore di risorse che mostra i membri del team esistenti per il progetto.
3. Immetti il nome della nuova risorsa generica e quindi seleziona **Crea**.
4. Nella finestra di dialogo **Creazione rapida: Membro del team di progetto** visualizzata, nel campo **Ruolo**, seleziona il ruolo della risorsa generica. 
5. Nel campo **Unità gestione risorse**, seleziona l'unità organizzativa per la risorsa generica. Quindi seleziona **Salva**. Il membro del team generico è ora assegnato all'attività.

   Nella scheda **Team**, viene visualizzato il nuovo membro del team generico. Nota che ha solo ore assegnate. Queste ore sono la somma di tutte le attività assegnate al membro del team generico. Il membro del team generico non ha ore richieste o un requisito di risorsa.

6. Ora puoi assegnare il membro del team generico ad altre attività mediante il selettore di risorse.

   Al termine dell'assegnazione della risorsa generica alle attività, puoi generare un requisito di risorsa per la risorsa generica.

7. Nella scheda **Team**, seleziona la risorsa generica e quindi seleziona **Genera requisito**. Quando il requisito viene generato, il membro del team generico avrà delle ore richieste e un collegamento per il requisito di risorsa.

  Dopo la prenotazione di una risorsa denominata, la risorsa generica viene rimossa dal team e sostituita dalla risorsa denominata. Nella scheda **Pianifica**, le assegnazioni della risorsa generica vengono rimosse e sostituite dalla risorsa denominata.

  > [!NOTE]
  > Questo comportamento si ha solo quando una risorsa denominata è interamente prenotata per il requisito di risorsa generica. Quando una risorsa denominata sostituisce parzialmente il requisito di risorsa generica o molteplici risorse denominate sostituiscono il requisito di risorsa generica, la risorsa generica rimane assegnata all'attività.

Project Operations non assegna entrambe le risorse all'attività, poiché tale comportamento genererebbe una pianificazione meno prevedibile. In questo semplice esempio, è facile dividere equamente le ore tra due risorse. Tuttavia, negli scenari più complessi che includono molteplici attività e risorse, PSA deve ipotizzare il modo in cui allocare le prenotazioni ricevute per molteplici risorse in più attività.

Pertanto, in questi scenari, il responsabile di progetto deve analizzare le molteplici prenotazioni e assegnarle come necessario. Per allocare le prenotazioni, il responsabile di progetto assegna le attività dalle risorse generiche alle risorse denominate e quindi utilizza la vista **Riconciliazione** per assicurarsi che l'allocazione funzioni con le prenotazioni.

### <a name="edit-a-resource-requirement"></a>Modificare un requisito di risorsa

Dopo la creazione di un requisito di risorsa, è possibile che un responsabile di progetto o delle risorse desideri modificare i dettagli per perfezionare i criteri di ricerca quando si utilizza la scheda di pianificazione. Per modificare il requisito di risorsa, procedi come descritto di seguito.

1. Nel modulo **Progetti**, nella scheda **Team**, seleziona il collegamento a qualsiasi requisito di una risorsa generica.
2. Nel modulo **Requisito di risorsa** visualizzato, immetti le informazioni necessarie per il campo

   Nel modulo **Requisito di risorsa**, il responsabile di progetto o delle risorse può anche definire competenze, ruoli, preferenze per le risorse e l'unità organizzativa preferita.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Aggiornare le prenotazioni delle risorse dopo la prenotazione in un progetto

Dopo aver aggiunto una risorsa generica o denominata a un team di progetto, puoi modificare le prenotazioni delle risorse.

1. Nel modulo **Progetti**, nella scheda **Team**, seleziona un membro del team e quindi seleziona **Gestisci prenotazioni**.
 
   Viene visualizzata la scheda di pianificazione, in cui sono indicate le prenotazioni del membro del team di progetto. Espandi il record del membro del team per visualizzare le ore che sono state prenotate per questo progetto e per altri progetti che consumano la capacità del membro del team.

2. Seleziona e trascina la prenotazione per estenderla o ridurla. Viene visualizzata la finestra di dialogo **Crea prenotazione risorsa** in cui puoi modificare la prenotazione.
3. Fai clic con il pulsante destro del mouse sulla prenotazione. Puoi quindi utilizzare il menu di scelta rapida per completare le seguenti azioni:

    - Modificare lo stato della prenotazione
    - Modificare la prenotazione
    - Sostituire una risorsa nel team di progetto

### <a name="change-the-booking-status"></a>Modificare lo stato della prenotazione

Puoi modificare lo stato di qualsiasi prenotazione predefinita o personalizzata.

I seguenti stati sono inclusi in Project Operations:

- **Annullato**: annulla la prenotazione della risorsa e libera la capacità della risorsa.
- **Prenotazione definitiva**: consuma la capacità di una risorsa. In genere una prenotazione ha questo stato quando si apre **Gestisci prenotazioni** dalla griglia **Tutti i membri del team** nel modulo **Progetti**.
- **Prenotazione provvisoria**: aggiunge una risorsa a un team ma non consuma la capacità della risorsa. Questo stato indica che la risorsa è stata riservata per un potenziale lavoro, ma la sua capacità è ancora disponibile se è necessaria per altri lavori. Nella vista della disponibilità globale delle risorse, le prenotazioni provvisorie hanno uno stato diverso dalle prenotazioni definitive.
- **Proposta**: rappresenta la proposta di un responsabile delle risorse o un responsabile di progetto per una risorsa. Le proposte non consumano la capacità di una risorsa e la risorsa non viene aggiunta al team di progetto. Per prenotare definitivamente la risorsa nel team, il responsabile di progetto deve accettare la proposta.

### <a name="submit-resource-requests"></a>Inviare richieste di risorse

Le richieste di risorse sono utilizzate per trasmettere la domanda o requisito di risorsa che deve essere soddisfatta da un responsabile delle risorse. Per una risorsa generica già inclusa nel team, puoi inviare direttamente una richiesta di risorsa. Una richiesta di risorse può essere soddisfatta in due modi:

- Il responsabile delle risorse soddisfa direttamente la richiesta. In questo caso, la risorsa generica viene sostituita da una prenotazione definitiva che ha una risorsa denominata.
- Il responsabile delle risorse propone una risorsa al responsabile di progetto e questo approva o rifiuta la risorsa proposta.

#### <a name="direct-fulfillment-of-resource-requests"></a>Soddisfare direttamente requisiti di risorsa

Quando viene generato un requisito di risorsa, un responsabile di progetto può inviare una richiesta di risorsa per una risorsa generica selezionando la risorsa e quindi selezionando **Invia richiesta**. È possibile fornire commenti sulla risorsa al responsabile delle risorse che soddisfa la richiesta. Dopo l'invio della richiesta, il campo **Stato** del membro del team diventa **Inviata**. Quando il responsabile delle risorse soddisfa la richiesta, il membro del team generico viene sostituito dalla risorsa denominata nella griglia **Tutti i membri del team**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utilizzare una proposta di risorsa per le richieste di risorse

Anziché prenotare direttamente una risorsa in una richiesta di risorse, un responsabile delle risorse può proporre una risorsa al responsabile di progetto. Un responsabile delle risorse può utilizzare questa opzione quando un'esatta corrispondenza non è disponibile per i requisiti. Quando un responsabile delle risorse propone una risorsa, il responsabile di progetto vede che il campo **Stato** del membro del team generico è stato aggiornato a **Revisione necessaria**.

È possibile visualizzare la risorsa proposta insieme a una visualizzazione dell'effetto della prenotazione della proposta. 

1. Fai doppio clic sul membro del team con stato **Revisione necessaria**. 
2. Seleziona la scheda **Risorse proposte**.
3. Seleziona **Accetta tutte le proposte** per accettare tutte le risorse proposte o **Rifiuta tutte le proposte** per rifiutarle. Se accetti le risorse proposte, vengono prenotate definitivamente nel progetto come membri del team e sostituiscono le risorse generiche.

> [!NOTE]
> Devi accettare o rifiutare tutte le risorse proposte. Non puoi accettarle o rifiutarle parzialmente.

### <a name="substitute-a-resource-on-the-project-team"></a>Sostituire una risorsa nel team di progetto

Talvolta, un responsabile di progetto deve sostituire un membro del team prenotato in un progetto.

1. Nel modulo **Progetti**, nella scheda **Team**, seleziona la risorsa che deve essere sostituita, quindi seleziona **Gestisci prenotazioni**.
2. Espandi la risorsa per visualizzare i progetti a cui è assegnata.
3. Fai clic con il pulsante destro del mouse sul progetto e quindi scegli **Sostituisci risorsa**.
4. Se conosci la risorsa con cui vuoi sostituire la risorsa corrente, seleziona o digita il nome e quindi seleziona **Riassegna**.

Oppure. Se è necessario cercare una risorsa, completa i seguenti passaggi.

1. Seleziona **Trova sostituzione**.

   L'assistente di pianificazione restituisce un elenco di risorse sostitutive disponibili. Nell'assistente di pianificazione, puoi filtrare ulteriormente le risorse disponibili per trovare una risorsa sostitutiva adatta.

2. Per sostituire la risorsa, seleziona la risorsa desiderata e quindi seleziona **Sostituisci**.   

   Le prenotazioni e le assegnazioni sono sostituite da una nuova risorsa.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Riconciliare prenotazioni e assegnazioni di membri del team

Per i membri del team, prenotazioni e assegnazioni non sono strettamente vincolate. In altre parole, le risorse possono avere assegnazioni ma nessuna prenotazione oppure prenotazioni ma nessuna assegnazione. Idealmente, prenotazioni e assegnazioni devono essere allineate, di modo che le risorse abbiano una capacità impegnata per eseguire le assegnazioni di attività. Tuttavia, le prenotazioni possono essere basate sulla disponibilità e le tempistiche inerenti alle attività possono cambiare con l'avanzamento del progetto. Di conseguenza, l'associazione non vincolante di prenotazioni e assegnazioni fornisce flessibilità.

Project Operations include una scheda **Riconciliazione** che consente ai responsabili di progetto di riconciliare le prenotazioni dei membri del team e le relative assegnazioni per il team di progetto.

La scheda **Riconciliazione** mostra prenotazioni e assegnazioni fino al livello della singola assegnazione di attività per ogni membro del team. Mostra le ore nelle celle che rappresentano periodi di tempo da mesi fino a giorni.

La scheda mostra inoltre un totale netto globale per il progetto insieme a una colonna relativa al totale.

Per ogni risorsa, la scheda calcola la differenza tra le prenotazioni del membro del team e un rollup delle assegnazioni di attività di quel membro. Idealmente, questa differenza dovrebbe essere 0 (zero). In altre parole, non dovrebbe esserci alcuna differenza tra prenotazioni e assegnazioni. Le differenze sono colorate e ombreggiate per attirare l'attenzione su due condizioni:

- **Prenotazione insufficiente**: si ha quando una risorsa ha più assegnazioni che prenotazioni. Poiché tale capacità non è stata riservata, è possibile che un responsabile di progetto voglia correggere tale condizione estendendo le prenotazioni della risorsa per compensare la mancanza.
- **Prenotazioni in eccesso**: si hanno quando una risorsa è stata prenotata per il progetto ma non è stata assegnata ad attività. Questa condizione può essere accettabile nei casi in cui la risorsa è stata prenotata per il progetto prima dell'assegnazione di attività. Tuttavia, in altri casi, la risorsa non viene pianificata per essere assegnata ad attività. In tali casi, il responsabile di progetto deve prendere in considerazione la possibilità di annullare le prenotazioni della risorsa di modo che la capacità possa essere utilizzata per un altro progetto.

In alcuni casi, quando visualizzi il tempo a un livello superiore al livello del giorno (ad esempio a livello del mese), puoi osservare una differenza netta pari a zero per una risorsa. In altre parole, prenotazioni = assegnazioni. Tuttavia, se visualizzi il tempo a livello della settimana, è possibile che vi siano assegnazioni di 0 (zero) ore e prenotazioni di 40 ore nella prima settimana, ma assegnazioni di 40 ore e prenotazioni di 0 (zero) ore nella seconda settimana. Globalmente, le prenotazioni e le assegnazioni vengono riconciliate, ma differiscono da una settimana all'altra.

Quando visualizzi il tempo a livelli superiori, le celle nella scheda **Riconciliazione** presentano un indicatore che informa dell'esistenza di differenze a livelli inferiori. Fai doppio clic su una cella per fare zoom avanti per visualizzare la differenza. Fai clic con il pulsante destro del mouse per fare zoom indietro. Selezionando una risorsa e quindi selezionando **Differenza successiva** puoi passare alla differenza successiva tra prenotazioni e assegnazioni per quella risorsa. Seleziona **Differenza precedente** per tornare indietro. Puoi anche disattivare l'indicatore di differenza e il comportamento di navigazione in **Impostazioni**.

Se sono presenti assegnazioni di attività per una risorsa ma nessuna prenotazione, nel modulo **Progetti**, nella scheda **Riconciliazione**, seleziona la prenotazione insufficiente e quindi seleziona **Estendi prenotazione**. Viene visualizzata la finestra di dialogo **Estendi prenotazione** che mostra la prenotazione necessaria per compensare la mancanza della risorsa. La finestra di dialogo mostra inoltre le prenotazioni esistenti della risorsa in tutti i progetti o altre entità pianificabili. Se selezioni **OK** per creare la prenotazione della risorsa, indipendentemente dalla disponibilità di quella risorsa, è possibile che si abbia una sovraprenotazione.

Il responsabile di progetto o il responsabile delle risorse può quindi utilizzare la scheda di pianificazione per gestire situazioni in cui una risorsa è sovraprenotata aldilà della sua capacità.


[!INCLUDE[footer-include](../includes/footer-banner.md)]