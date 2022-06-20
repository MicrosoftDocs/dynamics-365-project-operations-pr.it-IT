---
title: Gestione risorse
description: In questo articolo vengono fornite informazioni su come gestire le risorse.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5709f7f179b14606690549c77ede7ba03b77e1b1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920433"
---
# <a name="manage-resources"></a>Gestione risorse

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation include un dashboard per i responsabili delle risorse che fornisce una panoramica visiva della domanda e dell'utilizzo delle risorse nell'organizzazione. Puoi utilizzare i grafici di questo dashboard per visualizzare le informazioni seguenti:

- **Richiesta di risorse** - Il grafico **Richieste risorse attive** visualizza le risorse che sono state inviate. Le risorse sono aggregate per ruolo o progetto.
- **Richiesta di risorse non inviata** - Il grafico **Richiesta di risorse non inviata** visualizza tutti i requisiti di risorsa che non sono stati inviati. Consente ai responsabili delle risorse di visualizzare la richiesta che non è definitiva e che può essere inviata tramite una richiesta di risorse.
- **Utilizzo fatturabile per la settimana passata** - Il grafico **Utilizzo per ruolo** visualizza la percentuale dell'utilizzo fatturabile effettivo dell'organizzazione per ruolo rispetto al relativo utilizzo fatturabile di destinazione per ruolo.

    > [!NOTE]
    > Per rendere disponibile il grafico **Utilizzo per ruolo**, crea un processo che esegue il flusso di lavoro UpdateRoleUtilization. Questo processo ricorrente viene eseguito ogni sette giorni per calcolare l'utilizzo fatturabile dei sette giorni precedenti. I risultati sono aggregati per ruolo.

## <a name="manage-project-team-members"></a>Gestire membri del team di progetto

I responsabili di progetto possono utilizzare il dashboard dei responsabili delle risorse per gestire le risorse nei progetti. Ad esempio, possono aggiungere un membro del team direttamente a un progetto e prenotare un membro del team per soddisfare i requisiti di risorsa acquisiti da una risorsa generica.

### <a name="add-a-team-member-directly-to-a-project"></a>Aggiungere un membro del team direttamente a un progetto

Per aggiungere un membro del team direttamente a un progetto, nella pagina **Progetti**, nella scheda **Team**, seleziona **Nuovo**. Viene visualizzata la finestra di dialogo **Creazione rapida: Membro del team di progetto**. In questa finestra di dialogo, puoi eseguire le seguenti attività:

- **Prenotare una risorsa denominata** - Nel campo **Risorsa prenotabile**, seleziona il nome della risorsa. Quindi seleziona il ruolo, imposta il periodo e seleziona un metodo di allocazione. La risorsa denominata selezionata viene aggiunta al progetto mediante il metodo di allocazione selezionato e il calendario delle risorse.
- **Aggiungere una risorsa generica** - Lascia vuoto il campo **Risorsa prenotabile** e quindi seleziona il ruolo, imposta il periodo e seleziona il metodo di allocazione preferito. Una risorsa generica viene aggiunta al team come segnaposto per mantenere il modello di domanda utilizzato per prenotare risorse denominate del team. Il requisito viene creato in base al calendario del progetto.
- **Aggiungere una risorsa denominata al team senza consumare la capacità della risorsa** - Nel campo **Risorsa prenotabile**, seleziona una risorsa. Quindi seleziona il periodo e **Nessuno** come metodo di allocazione. La risorsa viene aggiunta al team, ma la capacità della stessa non viene consumata a seguito della prenotazione.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Prenotare un membro del team per soddisfare i requisiti di risorsa di una risorsa generica

In PSA, puoi prenotare una risorsa generica in un team di progetto e puoi specificare il ruolo, la capacità richiesta e il modo in cui la capacità viene distribuita. Nel requisito di risorsa, puoi specificare gli attributi associati alla risorsa generica. Tali attributi includono le competenze necessarie, l'unità organizzativa preferita e le risorse preferite.

Segui questi passaggi per specificare le competenze necessarie di una risorsa generica per uno sviluppatore.

1. Nella pagina **Progetti**, nella scheda **Team**, seleziona **Nuovo** per prenotare una risorsa generica.

    ![Risorsa generica prenotata nel team.](media/Resource-Management-image9.png)

2. Nella vista **Tutti i membri del team**, nella colonna **Requisito di risorsa**, seleziona il collegamento per aggiungere le competenze richieste per la risorsa generica.

    ![Collegamento al requisito.](media/Resource-Management-image10.png)

3. Nella pagina **Requisito di risorsa** visualizzata, nella griglia **Competenze**, seleziona i puntini di sospensione (**...**) e quindi **Aggiungi caratteristica nuovo requisito** per aggiungere le competenze richieste per lo sviluppatore.

    ![Comando Aggiungi caratteristica nuovo requisito.](media/Resource-Management-image11.png)

4. Nella finestra di dialogo **Creazione rapida: Caratteristica requisito** visualizzata, nel campo **Caratteristica**, seleziona la competenza richiesta. Quindi, nel campo **Valore di valutazione**, seleziona il livello di esperienza per tale competenza. Infine, nel campo **Requisito di risorsa**, imposta il requisito per utilizzare risorse delle unità organizzative o persino risorse denominate. Al termine, seleziona **Salva**.

    ![Finestra di dialogo Creazione rapida: Caratteristica requisito.](media/Resource-Management-image12.png)

5. Nella pagina **Requisito di risorsa**, seleziona **Prenota** per soddisfare il requisito.

    ![Pulsante Prenota nella pagina Requisito di risorsa.](media/Resource-Management-image13.png)

    Puoi anche selezionare la risorsa generica nella griglia **Tutti i membri del team** e quindi selezionare **Prenota**.

    ![Pulsante Prenota sopra la griglia Tutti i membri del team.](media/Resource-Management-image14.png)

    > [!NOTE]
    > In questo esempio, vi sono 40 ore richieste ma nessuna ora prenotata, in quanto le risorse generiche non hanno prenotazioni. Inoltre, non vi sono ore assegnate, in quanto la risorsa generica è stata aggiunta direttamente al team. Non è stata aggiunta utilizzando l'assegnazione delle attività.

    Nella pagina **Assistente pianificazione**, puoi filtrare le risorse disponibili in base ai requisiti specificati nel requisito di risorsa. Le risorse sono ordinate in base ai parametri di ordinamento specificati nella scheda di pianificazione.

    ![Pagina Assistente pianificazione.](media/Resource-Management-image15.png)

    Di seguito sono riportati alcuni filtri utilizzati spesso:

    - **Caratteristiche con una valutazione** - Consente di filtrare in base a competenze, certificazioni e altre qualità delle risorse, nonché in base alle valutazioni del livello di preparazione.
    - **Ruoli** - Consente di filtrare in base ai ruoli predefiniti assegnati a risorse prenotabili.
    - **Unità organizzative** - Consente di filtrare le risorse prenotabili in base alle unità organizzative a cui sono assegnate.

6. Se non sei soddisfatto dei risultati della ricerca iniziale, puoi modificare i criteri di filtro. Espandi il riquadro **Filtra vista** a sinistra e quindi seleziona **Cerca** per trovare ulteriori risorse.

    ![Riquadro Filtra vista.](media/Resource-Management-image16.png)

7. Per modificare l'ordinamento dei risultati, seleziona **Ordina**.

    ![Comando Ordina.](media/Resource-Management-image17.png)

8. Seleziona le risorse in base alla richiesta specificata nel requisito, come indicato nella parte superiore della griglia. Puoi annullare la selezione di celle nella griglia e lasciare aperta tale capacità di risorsa. È possibile selezionare una sola una risorsa alla volta come prenotata.

9. Seleziona **Prenota** per prenotare la risorsa selezionata e lasciare aperta la scheda di pianificazione, in modo da poter selezionare ulteriori risorse. In alternativa, seleziona **Prenota e chiudi** per prenotare la risorsa selezionata e chiudere la scheda di pianificazione.

    ![Risorsa da prenotare.](media/Resource-Management-image19.png)

    Viene visualizzata una notifica sulle ore prenotate. Gli indicatori della domanda mostrano quanto del requisito di prenotazione è stato soddisfatto. Puoi anche vedere quanta capacità della risorsa selezionata risulta consumata. Seleziona **Espandi** per visualizzare ulteriori dettagli sulle prenotazioni delle risorse.

9. Torna alla vista **Tutti i membri del team**. Nella griglia, nota che la risorsa generica è stata sostituita dalla risorsa denominata e che 40 ore sono indicate come prenotate per quella risorsa.

    ![Griglia Tutti i membri del team aggiornata.](media/Resource-Management-image20.png)

    > [!NOTE]
    > Non sono visualizzate ore assegnate in quanto sono state prenotate direttamente nel team. Non sono state prenotate utilizzando l'assegnazione delle attività.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Assegnare risorse generiche ad attività e generare requisiti di risorsa

In PSA, puoi creare attività e quindi assegnarvi risorse generiche. In questo modo, la richiesta di risorse può essere rappresentata da segnaposto mentre stimi la pianificazione e i dati finanziari. Puoi quindi generare requisiti di risorsa per le risorse generiche e soddisfarli.

1. Nella pagina **Progetti**, nella scheda **Pianifica**, seleziona **Aggiungi** per creare un'attività.

    ![Nuova attività creata.](media/Resource-Management-image21.png)

2. Nel campo **Risorse**, seleziona il simbolo del **selettore di risorse**. Viene visualizzato il selettore di risorse che mostra i membri del team esistenti per il progetto.

    ![Selettore di risorse.](media/Resource-Management-image22.png)

3. Immetti il nome della nuova risorsa generica e quindi seleziona **Crea**.

    ![Immettere il nome di una nuova risorsa generica.](media/Resource-Management-image23.png)

4. Nella finestra di dialogo **Creazione rapida: Membro del team di progetto** visualizzata, nel campo **Ruolo**, seleziona il ruolo della risorsa generica. Nel campo **Unità gestione risorse**, seleziona l'unità organizzativa per la risorsa generica. Quindi seleziona **Salva**.

    ![Finestra di dialogo Creazione rapida: Membro del team di progetto.](media/Resource-Management-image24.png)

    Il membro del team generico è ora assegnato all'attività.

    ![Membro del team generico assegnato all'attività.](media/Resource-Management-image25.png)

    Nella scheda **Team**, viene visualizzato il nuovo membro del team generico. Nota che ha solo ore assegnate. Queste ore sono la somma di tutte le attività assegnate al membro del team generico. Il membro del team generico non ha ancora ore richieste o un requisito di risorsa.

    ![Membro del team generico nella scheda Team.](media/Resource-Management-image26.png)

5. Ora puoi assegnare il membro del team generico ad altre attività mediante il selettore di risorse.

    ![Membro del team generico nel selettore di risorse.](media/Resource-Management-image27.png)

    Al termine dell'assegnazione della risorsa generica alle attività, puoi generare un requisito di risorsa per la risorsa generica.

5. Nella scheda **Team**, seleziona la risorsa generica e quindi seleziona **Genera requisito**.

    ![Comando Genera requisito.](media/Resource-Management-image28.png)

    Quando il requisito viene generato, il membro del team generico avrà delle ore richieste e un collegamento per il requisito di risorsa.

    ![Collegamento per il requisito di risorsa.](media/Resource-Management-image29.png)

    Dopo la prenotazione di una risorsa denominata, la risorsa generica viene rimossa dal team e sostituita dalla risorsa denominata.

    ![Risorsa generica sostituita dalla risorsa denominata.](media/Resource-Management-image30.png)

    Nella scheda **Pianifica**, le assegnazioni della risorsa generica vengono rimosse e sostituite dalla risorsa denominata.

    ![Assegnazioni della risorsa generica sostituite dalla risorsa denominata nella scheda Pianifica.](media/Resource-Management-image31.png)

    > [!NOTE]
    > Questo comportamento si ha solo quando una risorsa denominata è interamente prenotata per il requisito di risorsa generica. Quando una risorsa denominata sostituisce parzialmente il requisito di risorsa generica o molteplici risorse denominate sostituiscono il requisito di risorsa generica, la risorsa generica rimane assegnata all'attività.

    Nella figura seguente, un'attività di 80 ore è stata pianificata per una durata di cinque giorni (16 ore al giorno per cinque giorni) ed è stata assegnata alla risorsa generica denominata **Funzionale**.

    ![Attività di ottanta ore durante cinque giorni assegnata alla risorsa generica Funzionale.](media/Resource-Management-image32.png)

    Quando generi il requisito, corrisponde a 80 ore durante cinque giorni.

    ![Requisito generato per 80 ore durante cinque giorni.](media/Resource-Management-image33.png)

    Poiché le risorse disponibili lavorano otto ore al giorno, sono necessarie due risorse per soddisfare il requisito.

    ![Seconda risorsa.](media/Resource-Management-image35.png)

    Nella scheda **Team**, puoi ora vedere che la risorsa generica non ha ore richieste, ma che le ore assegnate sono ancora visualizzate con le due risorse denominate che compongono il requisito.

    ![Due risorse denominate nella scheda Team.](media/Resource-Management-image36.png)

    Nella scheda **Pianifica**, la risorsa generica rimane assegnata all'attività.

    ![Risorse generiche nella scheda Pianifica.](media/Resource-Management-image37.png)

PSA non assegna entrambe le risorse all'attività, poiché tale comportamento genererebbe una pianificazione meno prevedibile. In questo semplice esempio, è facile dividere equamente le ore tra due risorse. Tuttavia, negli scenari più complessi che includono molteplici attività e risorse, PSA deve ipotizzare il modo in cui allocare le prenotazioni ricevute per molteplici risorse in più attività.

Pertanto, in questi scenari, il responsabile di progetto deve analizzare le molteplici prenotazioni e assegnarle come necessario. Per allocare le prenotazioni, il responsabile di progetto assegna le attività dalle risorse generiche alle risorse denominate e quindi utilizza la vista **Riconciliazione** per assicurarsi che l'allocazione funzioni con le prenotazioni.

### <a name="edit-a-resource-requirement"></a>Modificare un requisito di risorsa

Dopo la creazione di un requisito di risorsa, è possibile che un responsabile di progetto o delle risorse desideri modificare i dettagli per perfezionare i criteri di ricerca quando si utilizza la scheda di pianificazione. Per modificare il requisito di risorsa, procedi come descritto di seguito.

1. Nella pagina **Progetti**, nella scheda **Team**, seleziona il collegamento a qualsiasi requisito di una risorsa generica.
2. Nella pagina **Requisito di risorsa** che viene visualizzata, puoi aggiornare vari attributi. Di seguito sono riportati alcuni esempi.

    - Nome
    - Dal
    - Fino al
    - Durata
    - Tipo di risorsa

Nella pagina **Requisito di risorsa**, il responsabile di progetto o delle risorse può anche definire le informazioni seguenti:

- Competenze
- Ruoli
- Preferenze delle risorse
- Unità organizzative preferita

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Aggiornare le prenotazioni delle risorse dopo la prenotazione in un progetto

Dopo aver aggiunto una risorsa generica o denominata a un team di progetto, puoi modificare le prenotazioni delle risorse.

1. Nella pagina **Progetti**, nella scheda **Team**, seleziona un membro del team e quindi seleziona **Gestisci prenotazioni**.

    ![Scheda di pianificazione aperta per il membro del team selezionato.](media/Resource-Management-image40.png)

    Viene visualizzata la scheda di pianificazione, in cui sono indicate le prenotazioni del membro del team di progetto. Espandi il record del membro del team per visualizzare le ore che sono state prenotate per questo progetto e per altri progetti che consumano la capacità del membro del team.

2. Seleziona e trascina la prenotazione per estenderla o ridurla. Viene visualizzata la finestra di dialogo **Crea prenotazione risorsa** in cui puoi modificare la prenotazione.

    ![Finestra di dialogo Crea prenotazione risorsa.](media/Resource-Management-image41.png)

3. Fai clic con il pulsante destro del mouse sulla prenotazione. Puoi quindi utilizzare il menu di scelta rapida per completare le seguenti azioni:

    - Modificare lo stato della prenotazione.
    - Modificare la prenotazione.
    - Sostituire una risorsa nel team di progetto.

### <a name="change-the-booking-status"></a>Modificare lo stato della prenotazione

Puoi modificare lo stato di qualsiasi prenotazione predefinita o personalizzata.

![Comando Cambia stato.](media/Resource-Management-image42.png)

I seguenti stati sono inclusi in PSA:

- **Annullato** - Questo stato annulla la prenotazione della risorsa e libera la capacità della risorsa.
- **Prenotazione definitiva** - Questo stato consuma la capacità della risorsa. In genere una prenotazione ha questo stato quando si apre **Gestisci prenotazioni** dalla griglia **Tutti i membri del team** nella pagina **Progetti**.
- **Prenotazione provvisoria** - Questo stato aggiunge una risorsa a un team ma non consuma la capacità della risorsa. Indica che la risorsa è stata riservata per un potenziale lavoro, ma la sua capacità è ancora disponibile se è necessaria per altri lavori. Nella vista della disponibilità globale delle risorse, le prenotazioni provvisorie hanno uno stato diverso dalle prenotazioni definitive.
- **Proposta** - Questo stato rappresenta la proposta di un responsabile delle risorse o un responsabile di progetto per una risorsa. Le proposte non consumano la capacità di una risorsa e la risorsa non viene aggiunta al team di progetto. Per prenotare definitivamente la risorsa nel team, il responsabile di progetto deve accettare la proposta.

### <a name="submit-resource-requests"></a>Inviare richieste di risorse

Le richieste di risorse sono utilizzate per trasmettere la domanda (requisito di risorsa) che deve essere soddisfatta da un responsabile delle risorse. Per una risorsa generica già inclusa nel team, puoi inviare direttamente una richiesta di risorsa. Una richiesta di risorse può essere soddisfatta in due modi:

- Il responsabile delle risorse soddisfa direttamente la richiesta. In questo caso, la risorsa generica viene sostituita da una prenotazione definitiva che ha una risorsa denominata.
- Il responsabile delle risorse propone una risorsa al responsabile di progetto e questo approva o rifiuta la risorsa proposta.

#### <a name="direct-fulfillment-of-resource-requests"></a>Soddisfare direttamente requisiti di risorsa

Quando viene generato un requisito di risorsa, un responsabile di progetto può inviare una richiesta di risorsa per una risorsa generica selezionando la risorsa e quindi selezionando **Invia richiesta**.

![Pulsante Invia richiesta.](media/Resource-Management-image45.png)

È possibile fornire commenti sulla risorsa al responsabile delle risorse che soddisfa la richiesta. Dopo l'invio della richiesta, il campo **Stato** del membro del team diventa **Inviata**.

![Immettere commenti facoltativi.](media/Resource-Management-image46.png)

Quando il responsabile delle risorse soddisfa la richiesta, il membro del team generico viene sostituito dalla risorsa denominata nella griglia **Tutti i membri del team**.

![Membro del team generico sostituito dalla risorsa denominata nella griglia Tutti i membri del team.](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utilizzare una proposta di risorsa per le richieste di risorse

Anziché prenotare direttamente una risorsa in una richiesta di risorse, un responsabile delle risorse può proporre una risorsa al responsabile di progetto. Un responsabile delle risorse può utilizzare questa opzione quando un'esatta corrispondenza non è disponibile per i requisiti. Quando un responsabile delle risorse propone una risorsa, il responsabile di progetto vede che il campo **Stato** del membro del team generico è stato aggiornato a **Revisione necessaria**.

![Stato del membro del team generico aggiornato a Revisione necessaria.](media/Resource-Management-image48.png)

Per visualizzare la risorsa proposta insieme a una visualizzazione dell'effetto della prenotazione della proposta, fai doppio clic sul membro del team il cui stato è **Revisione necessaria**. Quindi seleziona la scheda **Risorse proposte**.

![Scheda Risorse proposte.](media/Resource-Management-image49.png)

Seleziona **Accetta tutte le proposte** per accettare tutte le risorse proposte o **Rifiuta tutte le proposte** per rifiutarle. Se accetti le risorse proposte, vengono prenotate definitivamente nel progetto come membri del team e sostituiscono le risorse generiche.

> [!NOTE]
> Devi accettare o rifiutare tutte le risorse proposte. Non puoi accettarle o rifiutarle parzialmente.

### <a name="substitute-a-resource-on-the-project-team"></a>Sostituire una risorsa nel team di progetto

Talvolta, un responsabile di progetto deve sostituire un membro del team prenotato in un progetto.

1. Nella pagina **Progetti**, nella scheda **Team**, seleziona la risorsa che deve essere sostituita, quindi seleziona **Gestisci prenotazioni**.
2. Espandi la risorsa per visualizzare i progetti a cui è assegnata.

    ![Risorsa espansa per visualizzare i progetti assegnati.](media/Resource-Management-image50.png)

3. Fai clic con il pulsante destro del mouse sul progetto e quindi scegli **Sostituisci risorsa**.
4. Se conosci la risorsa con cui vuoi sostituire la risorsa corrente, seleziona o digita il nome e quindi seleziona **Riassegna**.

    ![Specificare una risorsa sostitutiva.](media/Resource-Management-image51.png)

    In alternativa, procedi come descritto di seguito per cercare una risorsa:

    1. Seleziona **Trova sostituzione**.

        ![Cercare una risorsa sostitutiva.](media/Resource-Management-image52.png)

        L'assistente di pianificazione restituisce un elenco di risorse sostitutive disponibili. Nell'assistente di pianificazione, puoi filtrare ulteriormente le risorse disponibili per trovare una risorsa sostitutiva adatta.

        ![Elenco delle risorse sostitutive disponibili.](media/Resource-Management-image53.png)

    2. Per sostituire la risorsa, seleziona la risorsa desiderata e quindi seleziona **Sostituisci**.

        ![Risorsa sostitutiva selezionata.](media/Resource-Management-image54.png)

    Le prenotazioni e le assegnazioni sono sostituite da una nuova risorsa.

    ![Prenotazioni e assegnazioni sostituite da una nuova risorsa.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Riconciliare prenotazioni e assegnazioni di membri del team

Per i membri del team, prenotazioni e assegnazioni non sono strettamente vincolate. In altre parole, le risorse possono avere assegnazioni ma nessuna prenotazione oppure prenotazioni ma nessuna assegnazione. Idealmente, prenotazioni e assegnazioni devono essere allineate, di modo che le risorse abbiano una capacità impegnata per eseguire le assegnazioni di attività. Tuttavia, le prenotazioni possono essere basate sulla disponibilità e le tempistiche inerenti alle attività possono cambiare con l'avanzamento del progetto. Di conseguenza, l'associazione non vincolante di prenotazioni e assegnazioni fornisce flessibilità.

PSA include una scheda **Riconciliazione** che consente ai responsabili di progetto di riconciliare le prenotazioni dei membri del team e le relative assegnazioni per il team di progetto.

![Scheda Riconciliazione.](media/Resource-Management-image56.png)

La scheda **Riconciliazione** mostra prenotazioni e assegnazioni fino al livello della singola assegnazione di attività per ogni membro del team. Mostra le ore nelle celle che rappresentano periodi di tempo da mesi fino a giorni.

La scheda mostra inoltre un totale netto globale per il progetto insieme a una colonna relativa al totale.

Per ogni risorsa, la scheda calcola la differenza tra le prenotazioni del membro del team e un rollup delle assegnazioni di attività di quel membro. Idealmente, questa differenza dovrebbe essere 0 (zero). In altre parole, non dovrebbe esserci alcuna differenza tra prenotazioni e assegnazioni. Le differenze sono colorate e ombreggiate per attirare l'attenzione su due condizioni:

- **Prenotazione insufficiente** - Una prenotazione insufficiente si ha quando una risorsa ha più assegnazioni che prenotazioni. Poiché tale capacità non è stata riservata, è possibile che un responsabile di progetto voglia correggere tale condizione estendendo le prenotazioni della risorsa per compensare la mancanza.
- **Prenotazioni in eccesso** - Si hanno prenotazioni in eccesso quando una risorsa è stata prenotata per il progetto ma non è stata assegnata ad attività. Questa condizione può essere accettabile nei casi in cui la risorsa è stata prenotata per il progetto prima dell'assegnazione di attività. Tuttavia, in altri casi, la risorsa non viene pianificata per essere assegnata ad attività. In tali casi, il responsabile di progetto deve prendere in considerazione la possibilità di annullare le prenotazioni della risorsa di modo che la capacità possa essere utilizzata per un altro progetto.

In alcuni casi, quando visualizzi il tempo a un livello superiore al livello del giorno (ad esempio a livello del mese), puoi osservare una differenza netta pari a zero per una risorsa (in altre parole, prenotazioni = assegnazioni). Tuttavia, se visualizzi il tempo a livello della settimana, è possibile che vi siano assegnazioni di 0 (zero) ore e prenotazioni di 40 ore nella prima settimana, ma assegnazioni di 40 ore e prenotazioni di 0 (zero) ore nella seconda settimana. Globalmente, le prenotazioni e le assegnazioni vengono riconciliate, ma differiscono da una settimana all'altra.

Quando visualizzi il tempo a livelli superiori, le celle nella scheda **Riconciliazione** presentano un indicatore che informa dell'esistenza di differenze a livelli inferiori. Facendo doppio clic su una cella, puoi fare zoom in avanti per visualizzare la differenza. Fai clic con il pulsante destro del mouse per fare zoom indietro. Selezionando una risorsa e quindi utilizzando il controllo **Differenza successiva** puoi passare alla differenza successiva tra prenotazioni e assegnazioni per quella risorsa. Per tornare alla differenza precedente, utilizza il controllo **Differenza precedente**. Puoi anche disattivare l'indicatore di differenza e il comportamento di navigazione in **Impostazioni**.

![Indicatore di differenza.](media/Resource-Management-image57.png)

Se sono presenti assegnazioni di attività per una risorsa ma nessuna prenotazione, nella pagina **Progetti**, nella scheda **Riconciliazione**, seleziona la prenotazione insufficiente e quindi seleziona **Estendi prenotazione**. Viene visualizzata la finestra di dialogo **Estendi prenotazione** che mostra la prenotazione necessaria per compensare la mancanza della risorsa. Mostra inoltre le prenotazioni esistenti della risorsa in tutti i progetti o altre entità pianificabili. Se selezioni **OK** per creare la prenotazione della risorsa, indipendentemente dalla disponibilità di quella risorsa, è possibile che si abbia una sovraprenotazione.

![Finestra di dialogo Estendi prenotazione.](media/Resource-Management-image58.png)

Il responsabile di progetto o il responsabile delle risorse può quindi utilizzare la scheda di pianificazione per gestire situazioni in cui una risorsa è sovraprenotata aldilà della sua capacità.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
