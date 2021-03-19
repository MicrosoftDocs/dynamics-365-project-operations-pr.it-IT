---
title: Installazione dei dati di esempio
description: In questo argomento vengono fornite informazioni sul'installazione dei dati di esempio in Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 377e50fc5772c4dc146ccee098bf2806bbc8c6b7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275093"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Installazione di dati di esempio per l'applicazione Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Per consentire la creazione di ambienti demo, Microsoft fornisce pacchetti di dati di esempio scaricabili che presentano le funzionalità delle app utilizzate. Sono disponibili due tipi di pacchetti di dati di esempio:
- dati di riferimento/configurazione
- dati dimostrativi (riferimento/configurazione e dati transazionali come gli ordini di lavoro e i progetti)

I pacchetti di dati di **riferimento** di esempio possono essere scaricati in tre diversi pacchetti, quindi è possibile installare dati solo per Project Service o Field Service oppure installare dati di esempio per entrambe le applicazioni contemporaneamente.

I pacchetti di dati di configurazione/riferimento sono:

- [**V902PSMasterData** - solo Project Service versione 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - solo Field Service versione 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x e Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

L'ultimo pacchetto di dati **dimostrativi** è:

 - [**FPSDemoData** - Field Service 8.x e Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Le istruzioni di installazione differiscono leggermente per quanto riguarda la sezione di creazione e configurazione degli utenti, ma il resto è uguale al precedente [**post di blog**](https://aka.ms/fpsdemodatablog). Il pacchetto include un set di dati dimostrativi ridotto e richiede circa 3 ore per l'installazione.

Questi pacchetti di dati di esempio sono disponibili solo in inglese.

> [!IMPORTANT]
> **Non è possibile disinstallare i dati di esempio.** Questi pacchetti devono essere installati solo in sistemi demo, di valutazione, formazione e prova. Da notare inoltre che non è possibile installare un singolo pacchetto e quindi l'altro singolo pacchetto. Ciò significa che non è possibile installare **FSMasterData** seguito da **PSMasterData** o viceversa. Se si ritiene che dei dati di esempio saranno necessari in futuro per entrambe le applicazioni, installare il pacchetto. **v902FPSMasterData**.

Quando si installa uno dei pacchetti di dati di esempio, il processo di installazione esegue le seguenti azioni:

- Crea o imposta parametri predefiniti per l'utilizzo di Field Service, Project Service o entrambe le applicazioni (se applicabile).

- Importa dati di esempio per le applicazioni, come risorse prenotabili, ruoli specifici dell'applicazione, listini prezzi di costo e vendita, unità organizzative, record di processi di vendita e altre entità per mostrare le funzionalità chiave.  

Con il pacchetto di **dati dimostrativi**, vengono scaricati i dati transazionali descritti sopra e altri come ordini di lavoro e progetti.

Per scoprire quali sono le funzionalità che è possibile provare con i dati di esempio, Vedi lo scenario della Fabrikam Robotics in [Note tecniche](#technical-notes).

In caso di domande sull'installazione dei pacchetti di dati di esempio, [inviare un messaggio di posta elettronica a fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Requisiti

Il protocollo di installazione presuppone quanto segue per l'istanza di destinazione (org):

- La lingua di base è l'inglese e la valuta di base è il dollaro USA (USD, $).

- L'organizzazione non dispone di dati di Field Service o Project Service oppure ha solo dati barebone predefiniti forniti con qualsiasi nuova organizzazione.

- La versione corretta dell'applicazione aziendale è già installata:
       
    - **Per FPSDemoData or v902FPSMasterData:** l'organizzazione ha la versione 8.x di Field Service e la versione 3.x di Project Service installate.

    - **Per v902PSMasterData:** l'organizzazione ha la versione 3.x di Project Service installata.

    - **Per v902FSMasterData:** l'organizzazione ha la versione 8.x di Field Service installata.

> [!NOTE]
> Se è necessario installare i dati di esempio in un ambiente di valutazione o demo Field Service e Project Service esistente che ha già dati (opzione non consigliata), è necessario sospendere i precontrolli di sicurezza eseguiti dal programma di installazione. Per ulteriori informazioni, vedere le note tecniche più avanti.

## <a name="prepare-for-installation"></a>Preparazione per l'installazione

È necessario eseguire il programma di installazione in un computer con una versione recente di Windows (Windows 10 preferibilmente).

È necessario pianificare la connessione del computer a una rete e l'esecuzione dell'installazione per **un'ora** per i **dati di configurazione/riferimento**. (L'installazione richiede in genere 30 minuti per **FPSMasterData**, che include i dati di esempio per entrambe le applicazioni). Per **FPSDemoData**, l'installazione durerà circa **3 ore**.

La funzione screen saver del computer deve essere disattivata. In caso contrario, è possibile la perdita delle credenziali della sessione per l'installazione quando la funzione screen saver viene attivata (a meno che la sessione non viene mantenuta sempre attiva).

> [!div class="mx-imgBorder"]
> ![Schermata delle impostazioni di screen saver con tale funzione disattivata](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Scaricare e decomprimere

Il programma di installazione di dati di esempio di Field Service e Project Service è distribuito come eseguibile autoestraente. I nomi di file possono variare a seconda del pacchetto di dati di esempio, ma i passaggi sono gli stessi indipendentemente dal pacchetto installato.

Dopo aver scaricato un pacchetto, eseguire il file .exe ed accettare termini e condizioni per decomprimere il file ZIP compresso. Estrarre quindi il contenuto di quel file in una cartella nel computer.

A seconda del sistema operativo e delle impostazioni di sicurezza, è possibile che sia necessario eseguire la procedura seguente dopo la decompressione del file ZIP:

1. Trova e fai clic con il pulsante destro del mouse sul file **FPSDemoData.dll** nella cartella **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Scegliere **Sblocca**.

3. Selezionare **Applica**.

4. Seleziona **OK**.


## <a name="create-or-configure-users"></a>Creare o configurare utenti

Il pacchetto **FPSDemoData** richiede sei utenti mentre i pacchetti **FPSMasterData** richiedono un utente. Fai riferimento a quello corretto per il tuo pacchetto di dati di esempio.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Creare o configurare gli utenti - pacchetti di dati di installazione/riferimento

Il pacchetto **FPSMasterData** è stato progettato per l'installazione con un utente denominato Spencer Low e le impostazioni descritte qui. Per installare correttamente il pacchetto, è necessario creare (o rinominare temporaneamente) utenti nel proprio ambiente per la corrispondenza con la configurazione dei dati di esempio in arrivo.

Per creare o configurare utenti, accedere a **Impostazioni** > **Sicurezza** > **Utenti** ed eseguire le operazioni seguenti:

1. Impostare UserFullname="Spencer Low" con il nome utente "spencerl" (**in lettere minuscole**) per i ruoli Responsabile di progetto e Responsabile operativo.

2. Selezionare **Spencer Low** e quindi selezionare **Gestisci ruoli**. Trovare e selezionare il ruolo **Amministratore di sistema** e quindi selezionare **OK** per assegnare diritti di amministratore a Spencer Low. Questo passaggio è necessario per assicurare la creazione di record di esempio con la corretta proprietà utente e quindi popolare correttamente le visualizzazioni.

3. Dal pacchetto scaricato, è necessario aggiornare un file di mapping dei dati con indirizzi di posta elettronica del contesto dell'utente predefinito. A tale scopo, aprire **PkgFolder** e quindi individuare e aprire il file **ImportUserMapFile.xml** in Blocco note (o Visual Studio o un altro editor XML). Impostare il campo **DefaultUserToMapTo=** sull'indirizzo di posta elettronica dell'utente Spencer Low.

4. Se non si utilizza Spencer Low con il nome utente **spencerl**, è necessario aggiornare un file aggiuntivo. Aprire il file **DemoDataPreImportConfig.xml** e quindi trovare il tag **userstocreateandconfigure**. Aggiorna il tag **\<login\>** con il nome utente dell'utente Spencer Low. Per ulteriori informazioni, vedi le [Note tecniche](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Creare o configurare gli utenti - pacchetto di dati dimostrativi

Il pacchetto di dati dimostrativi richiede sei utenti. Affinché il pacchetto venga installato correttamente, effettua le operazioni seguenti:

 1. Crea o rinomina temporaneamente gli utenti esistenti in base alla configurazione dei dati di esempio in arrivo passando a **Impostazioni** > **Sicurezza** > **Utenti**.
 
    I ruoli sono necessari solo per i dati dimostrativi basati su persona.  
    - Nome completo utente="David So" come tecnico di Field Service   
    - Nome completo utente= " Jamie Reding" come dispatcher di Customer Service e Field Service   
    - Nome completo utente= "Molly Clark" come Account Manager   
    - Nome completo utente="Spencer Low" come Practice e Project Manager  
    - Nome completo utente="Veronica Quek" come membro del team   
    - Nome completo utente="William Contoso"
  
2. A scopo di importazione dei dati dimostrativi, assegna ai sei utenti descritti sopra il ruolo di amministratore in modo da importare correttamente i record di esempio. 

3. Apri **PkgFolder**, quindi individua ed apri **ImportUserMapFile.xml**. Aggiorna i campi **Nuovo=** sugli indirizzi e-mail degli utenti corrispondenti nel sistema.

   > [!div class="mx-imgBorder"]
   > ![Schermata di UserMapFile](media/sample-data-7.png)

4. Se l'utente con il nome completo "Spencer Low" ha un ID utente diverso da **"spencerl"**, devi aggiornare un file aggiuntivo. Apri **DemoDataPreImportConfig.xml**, quindi trova il tag **userstocreateandconfigure**. Aggiorna il tag **\<login\>** con il loginId (con distinzione tra maiuscole e minuscole). 

5. Il calendario del primo utente (nel tag **userstocreateandconfigure** ) viene utilizzato per inserire le ore lavorative per tutte le risorse prenotabili durante l'importazione dei dati dimostrativi. Accedi a **Impostazioni** > **Sicurezza** > **Utenti**, trova l'utente "Spencer Low", quindi apri l'ozpione "Ore lavorative". Modifica le ore lavorative esistenti, selezionando l'opzione **Intera pianificazione settimanale**. Verifica che le **ore lavorative siano impostate su 8 - 17 (9 ore), da Lunedì a Venerdì con il fuso orario impostato su Ora pacifico (USA e Canada)**. Ciò è necessario per garantire che la scheda di pianificazione e di progetto venga visualizzata come previsto.

**Raccomandazione:** considerare la possibilità di creare un backup dell'organizzazione ora, nel caso sia necessario ritornare al punto di partenza a seguito di problemi durante l'installazione dei dati di esempio. Per ulteriori informazioni, vedere [Backup e ripristino di istanze](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Eseguire Package Deployer

1. Trova ed esegui **PackageDeployer.exe** nella cartella **v902FPSMasterData** O **PackageDeployer_FPSDemoData**.

2. Accettare i termini e le condizioni.

3. Nella finestra successiva:

   a. Seleziona **Office 365** come tipo di distribuzione.

   b. Utilizzare l'utente e la password dell'amministratore di sistema configurato in "Creare o configurare utenti" ("Spencer Low" con nome utente "spencerl").

   c. Verificare che l'opzione **Visualizza l'elenco delle organizzazioni disponibili** sia selezionata.

      > [!div class="mx-imgBorder"]
      > ![Schermata della finestra Package Deployer con l'opzione "Visualizza l'elenco delle organizzazioni disponibili" selezionata](media/sample-data-2.png)

4. Selezionare l'organizzazione in cui si desidera installare i dati di esempio.

5. Selezionare **Avanti** finché non viene visualizzata la finestra di dialogo **Installazione dati dimostrativi**.

   > [!div class="mx-imgBorder"]
   > ![Schermata della finestra di stato del programma di installazione di dati dimostrativi](media/sample-data-3.png)

6. Prima di continuare, notare che l'installazione di dati di esempio può richiedere fino a un'ora (normalmente ~10 minuti). È necessario assicurarsi che il computer sia acceso e collegato a una rete durante il processo di installazione e che la sessione rimanga attiva.   

7. Quando si è pronti, fare clic su **Avanti** per avviare il processo di installazione dei dati di esempio. Dopo il caricamento dei dati di esempio, fare clic su **Fine**.

## <a name="verify-the-sample-data-installation"></a>Verificare l'installazione dei dati di esempio

Per un test di integrità, verificare che il numero di record e i tipi di entità elencate nello scenario fittizio Fabrikam Robotics siano visualizzati come previsto.

Dopo il completamento del caricamento dei dati di esempio, accedere come Spencer Low e confermare quanto segue:

- Se l'applicazione Project Service è installata, accedere a **Project Service** > **Impostazioni** > **Listini prezzi**. Confermare l'esistenza di tassi di fatturazione e di costo, con la valuta appropriata, per ogni paese/area geografica nel set di dati.

- Se l'applicazione Project Service è installata, accedi a **Universal Resource Scheduling** > **Impostazioni** > **Unità organizzative**. Confermare che un listino prezzi di costo con la valuta appropriata è stato associato a ogni unità dell'organizzazione (ad esclusione delle voci della city). Se non è il caso, trovare e associare il listino prezzi di costo corretto.

- Se l'applicazione Field Service è installata, accedere a **Project Service** > **Impostazioni** > **Listini prezzi**. Confermare che i tassi di fatturazione e di costo esistono. Selezionare **Field Service** > **Impostazioni** > **Listini prezzi** e verificare l'esistenza di tassi di fatturazione e di costo, con la valuta appropriata, per ogni paese/area geografica nel set di dati.

  > [!div class="mx-imgBorder"]
  > ![Schermata dei listini prezzi attivi](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Schermata delle unità organizzative attive](media/sample-data-5.png)

## <a name="technical-notes"></a>Note tecniche

Di seguito sono forniti ulteriori note tecniche sull'installazione di questi dati.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Installazione di dati di esempio sui dati esistenti (non consigliato)

Se è necessario installare i dati di esempio in un ambiente di valutazione o demo Field Service e Project Service esistente che ha già dati, è necessario sospendere i precontrolli di sicurezza eseguiti dal programma di installazione.

A tale scopo, accedere alla cartella **PkgFolder** per individuare e aprire il file **DemoDataPreImportConfig.xml** con Blocco note (o un altro editor XML).

Individuare il seguente valore e quindi modificare l'impostazione da true a false:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Con questa modifica, programma di installazione ignora alcuni controlli di sicurezza importanti, tra cui:

- La conferma dell'esistenza di un solo record **Unità organizzativa** attivo e la ridenominazione dello stesso in **Fabrikam US**.

- Conferma dell'esistenza di un solo record **Modello di lavoro** attivo.

- Conferma dell'esistenza di un solo record **Parametro progetto** attivo e la ridenominazione di quella voce in **Parametri**.

### <a name="configuration-components"></a>Componenti di configurazione

Sono disponibili vari altri componenti di configurazione in questo file di configurazione di pre-importazione. Per gli utenti esperti, alcuni di questi includono:

- **\<RequiredSolutions\>** specifica le installazioni delle soluzioni prerequisite e i relativi numeri di versione.

- **\<InstallSampleData\>** determina se vengono installati dati di esempio predefiniti per le app.

    - false - ignora l'installazione di questi dati predefiniti (che sono rimuovibili).

    - true - installa i dati predefiniti insieme ai dati di esempio di FS e PSA.

- **\<PreImportDataCollection\>** specifica i mapping dei dati dei file flat e i record associati da importare prima dell'installazione dei dati di esempio principale.

- **\<EntitiesToEnableScheduling\>** specifica quali entità devono essere abilitate per la prenotazione in Microsoft Dynamics Scheduling (noto anche come Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** specifica le risorse prenotabili che verranno create (se non esistono già) prima dell'importazione dei dati di esempio. Da notare che le risorse prenotabili dei dati di esempio del sistema di origine corrispondono alle risorse prenotabili del sistema di destinazione in FullName e nel login di ogni risorsa. Di conseguenza, NON è possibile modificare i nomi nel file di preconfigurazione a meno che non si importino dapprima dati di esempio in un sistema di destinazione utilizzando questi nomi, quindi si rinominino le risorse prenotabili con il set di nomi desiderato insieme ai record utenti abilitati e infine si esportino di nuovo i dati per l'importazione nel sistema di destinazione finale (aggiornando le voci **ImportUserMapFile.xml** precedenti e nuove di conseguenza).

- **\<PluginsToDisable\>** specifica plug-in di voci molto discrete che devono essere disabilitati durante l'importazione dei dati di esempio e quindi riabilitati in seguito.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Scenario fittizio Fabrikam Robotics

I pacchetti di dati di riferimento di esempio di Field Service e Project Service installano la **soluzione Fabrikam Manufacturing Master Data (v3.0.0.0)**, insieme a circa 4.000 record e circa 40 entità differenti. I pacchetti di dati di esempio distinti per Field Service e Project Service contengono un sottoinsieme dei dati di esempio **v902FPSMasterData** per tale applicazione. Il pacchetto **Dati dimostrativi** installa la **soluzione Fabrikam Manufacturing Demo Data (v 3.0.0.7)** con circa 22.000 record su 148 entità.

La società fittizia, Fabrikam Robotics, è un produttore di robot per catene di montaggio di dispositivi elettronici ed è nota per la qualità dei suoi prodotti, l'innovazione e un eccellente servizio clienti, con servizi di pianificazione delle installazioni, di implementazione e di manutenzione continua. La sede di Fabrikam si trova negli Stati Uniti (Fabrikam US) e ha succursali in Francia, India, Regno Unito e Svizzera.

Le operazioni di assistenza sul campo sono concentrate negli Stati Uniti nell'area di Seattle. La società utilizza la connettività IoT per monitorare le prestazioni dei cespiti dei clienti e fornire servizi sul posto sempre più proattivi.

Di seguito è riportata una panoramica generale dei dati di esempio:

- Elementi comuni dei dati di esempio (inclusi per entrambe le applicazioni)

    - 1 utente

    - 71 account

    - 137 contatti

    - Vari tipi di transazioni e categorie

    - 50 prodotti con un listino prezzi

    - 14 listini prezzi/di costo

    - 31 caratteristiche (competenze risorse) in 2 modelli di valutazione con 3 livelli (valori di classificazione)

- Project Service

    - 8 unità organizzative

    - 6 livelli di utilizzo specifici del ruolo

    - Più di 2800 specifiche di prezzo del ruolo

- Field Service

    - 4 aree

    - 5 tipi di ordini di lavoro

    - 22 cespiti cliente

    - 9 tipi di incidente con una gamma di caratteristiche di risorsa associate (9), servizi (13) e attività servizio (13)
   
Il pacchetto **Dati dimostrativi** installa circa 179 ordini di lavoro, 12 progetti e i dati transazionali associati. 

### <a name="change-the-work-hours-for-sample-resources"></a>Modificare le ore lavorative per le risorse di esempio

Per impostazione predefinita, tutte le risorse prenotabili hanno un calendario di 24 ore lavorative.

Se è necessario modificare le ore lavorative per le risorse prenotabili di esempio, vai a **Universal Resource Scheduling** > **Pianificazione** > **Risorse**.

Selezionare un utente (ad esempio, Spencer Low) e sostituire le ore lavorative di Spencer con le ore che si intende applicare a più utenti. Vai a **Universal Resource Scheduling** > **Impostazioni** > **Modelli di ore lavorative** e modifica il record **Modello di lavoro predefinito**. Nel campo **Risorsa Modello**, selezionare un utente con le ore lavorative che si desidera applicare ad altre risorse. Vai a **Universal Resource Scheduling** > **Pianificazione** > **Risorse** > .**Risorse prenotabili attive**. Selezionare le risorsa che si desidera modificare e quindi selezionare **Imposta calendario**. Nell'elenco a discesa **Modello di lavoro**, selezionare il modello **Ore lavorative predefinite** o un altro modello con la risorsa corretta. Quando accedi alla scheda di pianificazione, potrai vedere che le ore lavorative delle risorse sono state aggiornate.

> [!div class="mx-imgBorder"]
> ![Schermata delle risorse prenotabili attive](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]