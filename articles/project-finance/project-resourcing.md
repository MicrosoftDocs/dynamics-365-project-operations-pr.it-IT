---
title: Assegnazione di risorse ai progetti
description: In questo argomento vengono fornite informazioni sull'assegnazione di risorse ai progetti.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752582"
---
# <a name="project-resourcing"></a>Assegnazione di risorse ai progetti

[!include [banner](../includes/banner.md)]

In questo argomento vengono fornite informazioni sull'assegnazione di risorse ai progetti.

Una sfida per i project manager e i responsabili delle risorse durante la fase di pianificazione del progetto è l'allocazione delle risorse, in cui devono determinare e prenotare la risorsa corretta per lavorare su un progetto. In Dynamics 365 Finance, le funzionalità di assegnazione delle risorse per i progetti consentono di definire ruoli che vengono trattati come risorse temporanee che possono essere riservate per un impegno specifico o parte di un impegno. Questo tipo di risorse consente ai project manager e ai responsabili delle risorse di completare le seguenti attività:

- Definire un ruolo che abbia le competenze richieste, in modo che sia facile abbinare le risorse.
- Utilizzare i ruoli per definire una pianificazione di interazione basata su risorse prenotate.
- Stimare i costi e determinare un budget iniziale, in base ai ruoli e alle risorse assegnati per un progetto.
- Utilizzare i ruoli per stimare il numero di prenotazioni di risorse necessarie per ogni interazione.
- Stimare il numero di risorse necessarie per l'intero ciclo di vita di un progetto.
- Redigere una struttura di suddivisione del lavoro (WBS) utilizzando le assegnazioni di risorse iniziali.

[![Ciclo di vita del progetto](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Man mano che la pianificazione del progetto procede, le risorse pianificate possono essere sostituite con risorse con personale. Il project manager può anche tornare indietro e aggiornare le prenotazioni delle risorse durante qualsiasi fase del progetto.

## <a name="set-up-project-resources"></a>Configurare le risorse di progetto
Devi configurare un calendario e associarlo a un dipendente o a un lavoratore. Il calendario viene utilizzato per pianificare il progetto e l'orario di lavoro delle risorse riservate al progetto. Durante la configurazione del calendario, i project manager possono eseguire il livellamento delle risorse come parte dell'ottimizzazione delle risorse. In base alla pianificazione del calendario, è possibile applicare restrizioni alle risorse. Puoi configurare un calendario nella pagina **Calendari**.

Quando configuri un lavoratore come risorsa del progetto, puoi selezionare tra i lavoratori che lavorano nell'azienda per cui stai configurando le risorse. In alternativa, puoi selezionare lavoratori di altre società nella tua organizzazione. Questi lavoratori sono noti come risorse interaziendali.

Le seguenti procedure spiegano come configurare un lavoratore come risorsa di progetto nella propria azienda e come configurare una risorsa di progetto interaziendale.

### <a name="set-up-a-worker-as-a-project-resource"></a>Configurare un lavoratore come risorsa del progetto

1. Nella pagina **Lavoratori** pagina, nell'elenco **Lavoratori**, seleziona il lavoratore che stai aggiungendo come risorsa del progetto e apri il record del lavoratore.
2. Nel riquadro azioni seleziona **Progetto**&gt; **Imposta** &gt;**Impostazione progetto**.
3. Seleziona un calendario e quindi chiudi la pagina.

Puoi inoltre specificare progetti predefiniti per una risorsa come tipo di pre-assegnazione. Le pre-assegnazioni possono essere utilizzate quando il responsabile delle risorse o il project manager sa in anticipo su quali progetti lavorerà la risorsa. Le pre-assegnazioni possono anche essere basate sulla richiesta di uno sponsor del progetto o di un cliente. Per pre-assegnare un progetto, nella pagina **Assegna progetti**, nella scheda **Progetti**, nell'elenco **Progetti rimanenti**, seleziona il progetto appropriato.

### <a name="set-up-an-intercompany-resource"></a>Configurare una risorsa interaziendale

Quando si configura un lavoratore come risorsa interaziendale, devi completare la configurazione sia nella società mutuante che nella società mutuataria.

**Nella società mutuante**

1. In Finance, verifica che la società mutuante sia selezionata, quindi completa la procedura nella sezione precedente, "Configurare un lavoratore come risorsa di progetto".
2. Nella pagina **Contabilità interaziendale**, seleziona **Nuovo**.
3. Nel campo **ID persona giuridica**, seleziona la società mutuante. Compila i campi rimanenti come necessario e quindi seleziona **Salva**.
4. Nella pagina **Prezzo di trasferimento**, seleziona **Nuovo**.
5. Nel campo **Persona giuridica richiedente**, seleziona la società appropriata.
6. Per prestare alla società mutuataria solo la risorsa che hai creato all'inizio di questa sezione, nel campo **Risorsa**, seleziona il nome della risorsa che hai creato. Per rendere disponibili alla società mutuataria tutte le risorse della società mutuante, lascia vuoto il campo **Risorsa**.
7. Nella pagina **Parametri Gestione progetti e contabilità**, nella scheda **Interaziendale**, imposta l'opzione **Abilita programmazione risorse interaziendale e fogli presenze** su **Sì**.

**Nella società mutuataria**

- Nella pagina **Elenco risorse**, nel filtro di ricerca, inserisci il nome della risorsa che hai creato per la società mutuante, per verificare che il nome sia incluso nell'elenco delle risorse per la società mutuataria.

## <a name="manage-resource-competencies"></a>Gestire le competenze delle risorse
Le competenze delle risorse sono una parte essenziale della gestione delle risorse. Le competenze possono essere utilizzate come base per determinare le risorse che hanno il corretto equilibrio tra competenze, istruzione, certificazione ed esperienza di progetto. È consigliabile configurare queste informazioni per ciascuna risorsa e aggiornarle regolarmente. In questo modo, puoi massimizzare le capacità quando le competenze specifiche delle risorse vengono abbinate durante l'assegnazione delle risorse del progetto.

[![Esempi di competenze, certificazioni, istruzione ed esperienza di progetto](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Le seguenti procedure spiegano come configurare alcune delle competenze per una risorsa.

Per configurare le competenze per un lavoratore, puoi utilizzare la pagina elenco **Lavoratori** in Risorse umane o la pagina elenco **Risorse** in Gestione progetti e contabilità. Per le seguenti procedure, viene utilizzata la pagina elenco **Lavoratori** in Risorse umane.

### <a name="set-up-competencies-certificates"></a>Configurare le competenze: certificati

1. Nella pagina elenco **Lavoratori**, seleziona la riga per il lavoratore per cui aggiungere le informazioni sul certificato.
2. Nel riquadro azioni, nella scheda **Lavoratore**, nel gruppo **Competenze**, seleziona **Certificati**.
3. Seleziona **Nuovo**, quindi, nel campo **Tipo di certificato**, seleziona **PMP**.
4. Nel campo **Data d'inizio**, seleziona **10/1/2015** e seleziona **Salva**.

### <a name="set-up-competencies-skills"></a>Configurare le competenze: competenze

1. Nella pagina elenco **Lavoratori**, assicurati che il lavoratore che hai utilizzato nella procedura precedente sia ancora selezionato. Quindi, nel riquadro azioni, nella scheda **Lavoratore**, nel gruppo **Competenze**, seleziona **Competenze**.
2. Seleziona **Nuovo**.
3. Nel campo **Competenza**, seleziona **Gestione dei progetti**.
4. Nel campo **Livello**, seleziona **5 Esperto**.
5. Nel campo **Data livello**, seleziona **1-/14/2014**.
6. Nel campo **Anni di esperienza**, inserisci **10**.
7. Seleziona **Salva** e quindi chiudi la pagina.

## <a name="create-a-new-project"></a>Crea un nuovo progetto
1. Nella pagina **Gestione dei progetti**, seleziona **Nuovo progetto**, quindi immetti i valori seguenti:

    - **Tipo di progetto:** tempo e materiale
    - **Nome progetto:** fase di aggiornamento XYZ 2
    - **Gruppo di progetto:** TM\_WIP
    - **ID contratto di progetto:** 00000002

2. Seleziona **Crea progetto**.

### <a name="assign-a-resource-to-a-project"></a>Assegnare una risorsa a un progetto

1. Nella pagina **Lavoratori** pagina, nell'elenco **Lavoratori**, seleziona il record per il lavoratore per cui hai impostato in precedenza le competenze e apri il record del lavoratore.
2. Nel riquadro azioni, nella scheda **Progetto**, nel gruppo **Imposta**, seleziona **Assegna progetti**.
3. Nella pagina **Assegnazioni di progetti di convalida delle risorse**, nella scheda **Progetti**, nel campo **Aggiungi il progetto ai progetti selezionati**, filtra nel progetto **Fase di aggiornamento XYZ 2**.
4. Nel riquadro **Progetti rimanenti**, seleziona un progetto, quindi seleziona il pulsante freccia per aggiungerlo al riquadro **Progetti selezionati**.

Puoi inoltre assegnare categorie a una risorsa in base alle tue esigenze. Il tipo di categoria è **Costo** o **Ricavi**. Il tipo di categoria è determinato dalla tua organizzazione. Se nessuna categoria è assegnata a una risorsa, Finance cerca la categoria predefinita sui prezzi orari per costi e ricavi.

### <a name="set-up-project-resource-and-role-characteristics"></a>Configurare le caratteristiche di ruolo e risorsa del progetto

Un project manager può utilizzare la funzionalità di assegnazione delle risorse del progetto per creare i ruoli richiesti per il progetto. I ruoli possono essere utilizzati se le risorse confermate sono ancora sconosciute quando le risorse vengono prenotate. I ruoli possono essere riservati temporaneamente come risorse pianificate, in modo da poter continuare le fasi di pianificazione del progetto.

[![Esempio di un ruolo](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso è stato assunto per completare un progetto di tempistica e materiali con uno statuto progetto approvato. Il project manager junior sta ancora completando l'ambito del progetto. Il responsabile delle risorse sta attualmente individuando risorse specifiche che saranno prenotate per lavorare sul nuovo progetto. A causa della natura critica del progetto, lo sponsor del progetto ha richiesto il Senior Project Manager come uno dei ruoli. Il responsabile delle risorse deve acquisire la nuova risorsa e definire il ruolo nel sistema nel caso in cui il project manager junior richieda le informazioni sulla risorsa durante la pianificazione del progetto.

I passaggi seguenti mostrano come il responsabile delle risorse può configurare il ruolo di Senior project manager e associarvi le caratteristiche della risorsa. Successivamente, il ruolo può essere utilizzato per cercare le risorse disponibili che corrispondono alle competenze delle risorse richieste.

1. Nella pagina **Configura ruoli**, seleziona **Nuovo**, quindi immetti i valori seguenti:

    - **ID ruolo:** Senior Project Manager
    - **Descrizione:** Senior Project Manager

2. Seleziona **Crea**.
3. Seleziona il ruolo **Senior Project Manager**, quindi seleziona **Configura caratteristiche**.
4. Nel campo **Tipo di caratteristiche**, seleziona **Competenza**.
5. Nel campo **Caratteristiche disponibili**, immetti la competenza da cercare.
6. Nel campo **Tipo di caratteristica**, seleziona **Certificato**.
7. Nel campo **Caratteristiche disponibili**, immetti il tipo di certificato da cercare.

### <a name="assign-a-project-resource-to-a-project"></a>Assegnare una risorsa di progetto a un progetto

1. Nella pagina **Tutti i progetti**, seleziona il progetto **Fase di aggiornamento XYZ 2**.
2. Nella scheda **Team progetto e programmazione**, seleziona **Aggiungi**.
3. Nel campo **Ruolo**, seleziona **Membro del team**.
4. Seleziona **Prenota da calendario**.
5. Nella pagina **Disponibilità risorse**, seleziona **Visualizza impostazioni**.
6. Nella pagina **Modifica impostazioni visualizzazione**, immetti i seguenti valori:

    - **Formato per la visualizzazione dell'intervallo di date:** giornaliero
    - **Visualizza descrizioni disponibili:** Sì
    - **Visualizza capacità rimanente:** Sì

7. Seleziona una risorsa dall'elenco delle risorse.
8. Seleziona **Prenota definitivamente** e **Piena capacità**.


### <a name="assign-a-resource-to-a-default-role"></a>Assegnare una risorsa a un ruolo predefinito

Per aiutare i responsabili di progetto o risorse possono eseguire il drill-down sulle risorse che possono essere prenotate per un progetto. Puoi associare un ruolo predefinito a una risorsa esistente o a una risorsa appena acquisita. Ad esempio, quando è stato assunto Daniel, aveva l'esperienza e le competenze per ricoprire il ruolo di analista aziendale. Il responsabile delle risorse ha assegnato questo ruolo come ruolo predefinito di Daniel. Pertanto, il responsabile delle risorse ha aggiunto Daniel a un pool di analisti aziendali disponibili a lavorare sui progetti.

Durante la prenotazione delle risorse, i project manager possono filtrare le risorse ruolo disponibili per lavorare sui progetti. Possono utilizzare queste informazioni come un criterio quando eseguono l'analisi decisionale multicriterio durante l'evasione delle risorse. Possono anche aggiungere altre caratteristiche delle risorse al filtro per cercare risorse con competenze, istruzione ed esperienza specifiche per un determinato progetto.

**Scenario:** è stato avviato un progetto approvato e il ruolo di Senior project manager è stato riservato come risorsa pianificata durante la fase di pianificazione del progetto. Il responsabile delle risorse ha ora acquisito una risorsa per svolgere il ruolo di Senior project manager.

1. Nella pagina **Elenco risorse**, seleziona **Daniel Goldschmidt**.
2. Nella pagina **Ruolo risorsa**, seleziona **Nuovo**, quindi immetti i valori seguenti:

    - **Validità:** immetti la data corrente.
    - **Scadenza:** immetti **Mai**.
    - **Ruolo:** immetti **Senior Project Manager**.

3. Seleziona **Salva** e quindi chiudi la pagina.
4. Nella scheda **Competenze**, aggiungi la competenza **ProjectMgmt** e il certificato **PMP**.

## <a name="set-up-role-based-pricing"></a>Configurare i prezzi basati sui ruoli
Tutti i costi, le vendite e i prezzi di trasferimento possono essere configurati per i ruoli.

1. Nella pagina **Prezzo di vendita (ora)**, seleziona **Nuovo** e inserisci una data di validità.
2. Nella colonna **Ruolo** seleziona un ruolo.
3. Nella colonna **Prezzi**, inserisci un prezzo per il ruolo risorsa selezionato.

## <a name="form-a-project-team"></a>Formare un team di progetto
Per utilizzare i ruoli precedentemente configurati in un progetto, un project manager deve associare i ruoli al progetto. È possibile assegnare più ruoli per un progetto. Per evitare confusione, questi ruoli vengono etichettati automaticamente durante la prenotazione. Ad esempio, se il project manager richiede tre ingegneri software, tre ruoli di ingegnere software che hanno **ingegnere software 1**, **ingegnere software 2** e **ingegnere software 3** come loro etichette vengono generati automaticamente. Se le caratteristiche del ruolo erano state precedentemente impostate per il ruolo, vengono applicate come filtro durante le ricerche di una risorsa. Ulteriori caratteristiche possono essere aggiunte secondo necessità per affinare ulteriormente la ricerca.

Le impostazioni di visualizzazione possono anche essere personalizzate per fornire una migliore visualizzazione della disponibilità delle risorse. Sono disponibili opzioni per mostrare la disponibilità oraria, giornaliera, settimanale, mensile, trimestrale e annuale. Esiste anche un'opzione per mostrare la capacità disponibile e rimanente sulle risorse. Questa opzione è utile per la gestione del tempo, quando si stima il tempo disponibile per le attività o la disponibilità delle risorse.

Il project manager può selezionare un ruolo nella pagina e quindi, se è disponibile una risorsa che soddisfa il requisito, selezionare per prenotare una risorsa per ricoprire il ruolo. Tieni presente che le risorse non devono essere prenotate a questo punto della fase di pianificazione. Quando crei una struttura di suddivisione del lavoro, puoi sostituire i ruoli con risorse di personale per il progetto. Se i ruoli vengono sostituiti con risorse con personale nella struttura di suddivisione del lavoro, la configurazione delle risorse aggiorna automaticamente l'elenco e la pianificazione del team di progetto.

[![Elenco del team di progetto che include sia i ruoli che le risorse effettive](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Il project manager ha varie opzioni per prenotare una risorsa per un progetto, ad esempio **Capacità rimanente**, **Piena capacità**, **Percentuale di capacità** e **Specifica orari**. Queste opzioni di prenotazione possono essere annullate in qualsiasi momento se le assegnazioni delle risorse cambiano. Sono supportati due tipi di prenotazione:

- **Prenotazione definitiva**: la prenotazione della risorsa è stata approvata e confermata per lavorare sull'impegno per la durata specificata.
- **Prenotazione temporanea**: le prenotazioni della risorsa sono state temporaneamente impostate per lavorare sull'impegno per la durata specificata.

La procedura seguente illustra come creare un team di progetto.

### <a name="create-a-project-team"></a>Creare un team di progetto

1. Nella pagina elenco **Tutti i progetti**, seleziona un progetto, quindi seleziona **Modifica**.
2. Nella scheda **Team progetto e programmazione**, nel campo **Data di fine della pianificazione** immetti la data di inizio della pianificazione più un mese. Ad esempio, se la data di inizio della pianificazione è il 24 giugno 2017 (24/06/2017), immetti **24/07/2017**.
3. Seleziona **Aggiungi**.
4. Nel riquadro  **Aggiungi ruoli al progetto**, nel campo **Ruolo**, seleziona **Senior Project Manager**.
5. Seleziona **Competenze richieste**.
6. Nella pagina **Scegli caratteristiche**, le caratteristiche precedentemente impostate per il ruolo di Senior project manager sono selezionate per impostazione predefinita. Seleziona **OK**.
7. Nella pagina **Aggiungi ruoli al progetto**, nel campo **Numero di risorse**, inserisci **1**.
8. Nel campo **Risorsa**, la ricerca mostra tutte le risorse che hanno le competenze richieste. Seleziona **Daniel Goldschmidt**, quindi seleziona **Crea**.
9. Nella pagina **Progetto** seleziona **Aggiungi**.
10. Nel riquadro  **Aggiungi ruoli al progetto**, nel campo **Ruolo**, seleziona **Membro del team**. Nel campo **Numero di risorse**, immetti **5**.
11. Seleziona **Crea**.
12. Nella pagina **Progetti**, seleziona **Soddisfa capacità risorsa**.

## <a name="resource-capacity-synchronization"></a>Sincronizzazione della capacità delle risorse
I processi per la sincronizzazione delle risorse aiutano a garantire che le informazioni per il calendario e il calendario di base si riflettano nella pianificazione delle risorse del progetto. Se il calendario viene modificato, i processi apportano gli aggiornamenti richiesti alla pianificazione delle risorse del progetto. I processi aiutano anche a migliorare le prestazioni, perché le informazioni sulle risorse del calendario vengono sincronizzate in anticipo. Pertanto, gli aggiornamenti alle informazioni sulla pianificazione delle risorse avvengono più rapidamente. Si consiglia di pianificare i processi come batch anziché uno alla volta. In caso contrario, c'è il rischio che qualcuno dimentichi le date incluse in cui le informazioni sono state sincronizzate l'ultima volta. Se le date incluse non vengono utilizzate, possono verificarsi degli intervalli durante la sincronizzazione della data.

![Sincronizzazione del calendario](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizzare il rollup della capacità delle risorse

Il processo di sincronizzazione è progettato per sincronizzare tutte le informazioni del calendario delle risorse. Queste informazioni includono le informazioni del calendario di base su eventuali modifiche alla tabella della capacità del calendario delle risorse del progetto. Se vengono aggiunte nuove risorse al progetto, la sincronizzazione aiuta a garantire che le informazioni di calendario aggiornate siano disponibili. Questa sincronizzazione può essere eseguita in qualsiasi momento.

Si consiglia di utilizzare un batch. Le opzioni sono disponibili durante la sincronizzazione delle prenotazioni della capacità.

1. Seleziona **Gestione progetti e contabilità** &gt; **Periodico** &gt; **Sincronizzazione capacità** &gt; **Sincronizza i roll-up della capacità delle risorse**.
2. Imposta le opzioni nella tabella seguente.

    | Opzione      | Descrizione |
    |-------------|-------------|
    | Codice periodo | Facoltativamente, seleziona il codice intervallo data di contabilità generale per impostare le date di inizio e fine per il processo di sincronizzazione per i roll-up della capacità delle risorse. |
    | Data di inizio  | Immetti la data di inizio per il processo di sincronizzazione per i roll-up della capacità delle risorse. |
    | Data di fine    | Immetti la data di fine per il processo di sincronizzazione per i roll-up della capacità delle risorse. |

[![Processo di sincronizzazione](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Configurare i ruoli sui modelli di struttura di suddivisione del lavoro
I project manager possono impostare modelli di struttura di suddivisione del lavoro che possono applicare quando creano una struttura di suddivisione del lavoro per nuovi progetti. I project manager possono aggiungere ruoli quando creano un modello. Utilizza la procedura seguente per assegnare un ruolo a un modello di struttura di suddivisione del lavoro.

1. Seleziona **Gestione progetti e contabilità** &gt; **Imposta** &gt; **Progetti** &gt; **Modelli di struttura di suddivisione del lavoro**.
2. Seleziona **Dettagli** per un modello di struttura di suddivisione del lavoro selezionato.
3. Seleziona un'attività nell'elenco, quindi, nel campo **Ruolo** seleziona un ruolo da assegnare all'attività.

### <a name="work-with-a-wbs"></a>Utilizzare una struttura di suddivisione del lavoro

È possibile creare una nuova struttura di suddivisione del lavoro oppure copiare una struttura di suddivisione del lavoro da un modello di struttura di suddivisione del lavoro esistente. Un project manager può gestire facilmente le risorse assegnando ruoli a nuove attività sulla struttura di suddivisione del lavoro. I ruoli possono essere sostituiti dopo l'acquisizione di una risorsa o dopo l'identificazione di una risorsa confermata per lavorare sull'attività. Questa flessibilità consente ai project manager di eseguire le seguenti attività:

- Identificare il numero di risorse richieste per i pacchetti di lavoro della struttura di suddivisione del lavoro.
- Stimare i costi del progetto.
- Determinare un budget preliminare.
- Stimare la durata dell'attività, in base a ruoli e risorse.
- Sviluppare alcuni piani di gestione del progetto, sulla base delle informazioni di progetto disponibili.

Sono state aggiunte ulteriori opzioni nella struttura di suddivisione del lavoro per utilizzare meglio la funzionalità di risorse.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Assegnazioni risorse</td>
<td>Visualizza le risorse assegnate, le date, il numero di ore e il tipo di prenotazione per le attività sulla struttura di suddivisione del lavoro.</td>
</tr>
<tr class="even">
<td>Generare automaticamente il team</td>
<td>Aggiungi automaticamente le risorse pianificate utilizzando i ruoli associati a un'attività. Finance suggerisce automaticamente le risorse pianificate utilizzando l'analisi decisionale multicriterio basata sui ruoli. Dopo che i ruoli e lo sforzo (ore) sono stati impostati per le attività in una struttura di suddivisione del lavoro e dopo che la struttura è stata rilasciata, seleziona <strong>Genera automaticamente team</strong>. Il numero richiesto di risorse pianificate viene aggiunto alla struttura di suddivisione del lavoro e alla scheda <strong>Team progetto e programmazione</strong>.</td>
</tr>
<tr class="odd">
<td>Risorsa (elenco a discesa)</td>
<td>Nella pagina <strong>Avvia modulo di assegnazione risorse</strong>, puoi selezionare le risorse da prenotare definitivamente o temporaneamente in base alla durata specificata. Puoi modificare le impostazioni di visualizzazione per vedere e impostare la durata delle attività delle risorse. Puoi selezionare e assegnare risorse a livello di pacchetto di lavoro utilizzando le seguenti opzioni:
<ul>
<li><strong>Accetta</strong>: conferma le modifiche alla risorsa assegnata a un'attività.</li>
<li><strong>Annulla</strong>: annulla le modifiche alla risorsa assegnata a un'attività.</li>
<li><strong>Assegna automaticamente</strong>: una risorsa con personale disponibile che ha un ruolo corrispondente viene automaticamente selezionata e assegnata all'attività selezionata.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Nella pagina **Tutti i progetti**, seleziona il progetto **Fase di aggiornamento XYZ 2**.
2. Seleziona **Piano** &gt; **Impegni** &gt; **Struttura di suddivisione del lavoro**.
3. Seleziona **Nuovo** per aggiungere le seguenti attività di primo livello alla struttura di suddivisione del lavoro:

    - Avvio
    - Pianificazione
    - Esecuzione in corso
    - Monitoraggio e controllo
    - Chiuso

4. Imposta le date e lo sforzo (ore), come mostrato nell'illustrazione seguente.

    [![Impostazione delle date e dell'impegno](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Seleziona la riga attività **Avvio**, quindi, nel campo **Ruolo**, seleziona **Senior Project Manager**.
6. Seleziona **Pubblica**.
7. Sulla stessa riga, nel campo **Risorsa**, seleziona **Daniel Goldschmidt** e quindi seleziona **Accetta**.
8. Seleziona la riga attività **Pianificazione**, quindi, nel campo **Ruolo**, selezionare **Analista aziendale**.
9. Seleziona **Pubblica** e quindi seleziona **Generare automaticamente il team**.
10. Nella finestra del messaggio che verrà visualizzata, seleziona **Sì**.
11. Nel campo **Risorsa**, verifica che il valore sia **Analista aziendale 1**.
12. Per la risorsa **Analista aziendale 1**, apri la ricerca e seleziona **Avvia assegnazioni di risorse**. Quindi seleziona un lavoratore per l'attività.
13. Seleziona **Assegnazione temporanea** &gt; **Piena capacità**.

    > [!NOTE] 
    > Non ricevi un avviso che la risorsa specificata è ora 2, perché il numero di risorse rimane 1.

14. Nella pagina **Struttura di suddivisione del lavoro**, convalida l'assegnazione delle risorse sulla struttura di suddivisione del lavoro, quindi seleziona **Salva**.

## <a name="resource-fulfillment-for-planned-resources"></a>Soddisfazione delle risorse per le risorse pianificate
Un project manager può pianificare i ruoli delle risorse richieste per un progetto. Il responsabile delle risorse vedrà queste risorse pianificate come richieste nella pagina **Possibilità di soddisfare la capacità delle risorse** e può assegnare risorse effettive.

1. Nella pagina **Tutti i progetti**, seleziona il progetto **Fase di aggiornamento XYZ 2**.
2. Seleziona **Progetto** e quindi seleziona **Modifica**.
3. Nella scheda **Team progetto e programmazione**, seleziona **Aggiungi**.
4. Nella finestra di dialogo **Aggiungi ruoli**, seleziona il ruolo **Sviluppatore software**.
5. Seleziona **Crea** e quindi chiudi la pagina del progetto.
6. Nella pagina **Soddisfazione risorse**, seleziona **Sviluppatore software 1** per il progetto **Progetto di aggiornamento XYZ Fase 2**.
7. Seleziona un ruolo di lavoro e quindi seleziona **Assegna**.
8. Verifica che la riga per **Sviluppatore software 1** sia stata rimossa per il progetto **Progetto di aggiornamento XYZ Fase 2**.
9. Nella scheda **Team progetto e programmazione**, per il progetto **Aggiornamento XYZ fase 2**, verifica che il ruolo di lavoro selezionato nel passaggio precedente sia stato aggiunto come **Sviluppatore software**.

## <a name="requests-for-project-resources"></a>Richieste di risorse di progetto
La funzionalità per la pianificazione delle risorse di progetto consente solo ai responsabili delle risorse di distribuire le risorse con personale su impegni o progetti. Per abilitare questa funzionalità, completa le seguenti attività o verifica che siano state completate:

- Configura le sequenze numeriche.
- Configura i flussi di lavoro di gestione dei progetti e contabilità.
- Abilita i flussi di lavoro delle richieste di risorse.

Dopo che le attività precedenti sono state completate, puoi completare le seguenti attività come richiesto:

- Crea una richiesta di risorse da una risorsa con personale con prenotazione provvisoria.
- Monitora le richieste di risorse.
- Soddisfa richieste di risorse.
- Richiedi una risorsa con personale da una struttura di suddivisione del lavoro.
- Prenota risorse per un progetto senza dover richiedere una risorsa con personale.

## <a name="monitor-project-teams"></a>Monitorare i team di progetto
1. Nella pagina **Tutti i progetti**, seleziona il collegamento **ID progetto** per il progetto **Aggiornamento XYZ Fase 2**.
2. Nella Scheda dettaglio **Team progetto e programmazione**, verifica che le risorse del progetto elencate siano corrette.
