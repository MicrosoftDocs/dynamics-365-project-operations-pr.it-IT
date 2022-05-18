---
title: Creare e verificare i giornali di registrazione di scritture contabili
description: Questo argomento fornisce informazioni su come creare e confermare i giornali di registrazione di scritture contabili in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584233"
---
# <a name="create-and-confirm-entry-journals"></a>Creare e verificare i giornali di registrazione di scritture contabili

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi utilizzare i giornali di registrazione di scritture contabili per registrare i dati effettivi direttamente in Microsoft Dynamics 365 Project Operations. Quando si utilizzano i giornali di registrazione di scritture contabili, non è necessario immettere i registri di utilizzo di inserimento ore, spese e materiali in Project Operations.

Un singolo giornale di registrazione di scritture contabili consente di creare più righe di registrazione. Quando il giornale di registrazione è confermato, una riga di registrazione di scritture contabili registra il valore effettivo per i seguenti dettagli:

- Il costo o il ricavo, a seconda del tipo di transazione selezionato.
- La classe di transazione selezionata. Le classi disponibili sono **Inserimento ore**, **Spese**, **Materiale**, **Acconto**, **Passaggio fondamentale**, e **Imposta**.
- Il progetto e/o un'attività selezionata nella riga del giornale di registrazione.

Segui la seguente procedura per creare un giornale di registrazione di scritture contabili in Project Operations.

1. Vai in **Vendite** \> **Transazioni** \> **Giornali di registrazione**.
2. Sulla pagina elenco **Giornali di registrazione di scritture contabili**, nel riquadro azioni seleziona **Nuovo** per creare un giornale di registrazione.
3. Sulla pagina **Nuovo giornale di registrazione**, nel campo **Descrizione** immetti una descrizione del giornale di registrazione.
4. Assicurati che il campo **Tipo di giornale** si impostato su **Scrittura contabile**, quindi seleziona **Salva**. Dopo aver salvato il nuovo giornale di registrazione di scritture contabili, una scheda **Righe giornale di registrazione** viene visualizzata nella pagina del giornale di registrazione.
5. Sulla scheda **Righe giornale di registrazione** nella barra degli strumenti sopra la griglia, seleziona **Nuovo** per creare una riga del giornale di registrazione di scritture contabili.
6. Nella finestra di dialogo **Creazione rapida** per la creazione di una riga del giornale di registrazione di scritture contabili, imposta i campi come descritto nella tabella seguente.

    | Campo | Description | Impatto funzionale |
    | --- | --- | --- |
    | Classe di transazione | La riga del giornale di registrazione può essere classificata in una delle sei classi di transazione: **Inserimento ore**, **Spese**, **Materiale**, **Acconto**, **Passaggio fondamentale**, o **Imposta**. | La classe di transazione **Imposta** è stata deprecata in Project Operations. <br> Se crei una classe di transazione **Imposta**, non verrà elaborata tramite fatturazione o calcoli di costi o ricavi. **Passaggio fondamentale** è una classe di transazione di soli ricavi. <br>La classe di transazione **Acconto** rappresenta un anticipo ricevuto da un cliente. Deve sempre essere creata come una coppia di righe di registrazione vendite fatturate e non fatturate. |
    | Tipo di transazione | I tipi di transazione **Costo**, **Vendite interorganizzative**, e **Costo unità gestione risorse** devono essere utilizzati per registrare i costi.<br> I tipi di transazione **Vendite non fatturate** e **Vendite fatturate** devono essere utilizzati per registrare le entrate. | La classe di transazione **Acconto** funziona solo con i tipi di transazione **Vendite non fatturate** e **Vendite fatturate**.<br> La classe di transazione **Passaggio fondamentale** funziona solo con il tipo di transazione **Vendite fatturate**. <br>I tipi di transazione **Vendite interorganizzative** e **Costo unità gestione risorse** sono applicabili solo alla classe transazione **Inserimento ore** e sono disponibili solo sui giornali di registrazione di scritture contabili nello scenario di distribuzione Lite e non durante la distribuzione di Project Operations negli scenari Risorsa/Non stoccata. |
    | Selezione prodotto | Quando la classe di transazione **Materiale** è selezionata, questo campo consente di specificare se la transazione materiale per la quale si sta creando la riga del giornale di registrazione è un prodotto esistente o un prodotto fuori catalogo. | Se selezioni **Prodotto fuori catalogo**, puoi inserire un nome per il prodotto. |
    | Prodotto | Riferimento al prodotto dal catalogo. | |
    | Description | Una descrizione della riga del giornale di registrazione per facilitarne l'identificazione. | Per le righe del giornale di registrazione vendite non fatturate, il valore verrà utilizzato come descrizione quando vengono creati i dettagli della riga di fattura. |
    | Descrizione esterna | Una descrizione della riga del giornale di registrazione che può essere utilizzata per la condivisione con le parti interessate esterne. | Per le righe del giornale di registrazione vendite non fatturate, il valore verrà utilizzato come descrizione esterna quando vengono creati i dettagli della riga di fattura. Può anche apparire sulla fattura che viene inviata al cliente. |
    | Tipo di fatturazione | Un valore che indica se la riga del giornale di registrazione verrà conteggiata come componente addebitabile, gratuita o non addebitabile nel progetto. | In un flusso tipico, il tipo di fatturazione deriva dai termini concordati stabiliti nel contratto. Tuttavia, quando registri una riga del giornale di registrazione, è possibile immettere un valore in questo campo. |
    | Data documento | Usa la data in cui è stata eseguita la transazione. | |
    | Data di inizio | Usa la data in cui è stata eseguita la transazione. | Questo campo viene utilizzato per il confronto con la data di creazione della fattura per le transazioni di tipo **Vendite non fatturate**. Questo confronto ti aiuterà a decidere se la transazione è futura o passata. Solo le transazioni passate verranno aggiunte alla fattura. |
    | Data finali | Usa la data in cui è stata eseguita la transazione. | |
    | Data contabile | Utilizza la data in cui verrà registrato l'impatto contabile. | |
    | Cliente voce di contratto | Per impostazione predefinita, se la voce di contratto ha un solo cliente, questo campo viene impostato sul cliente nella voce di contratto quando la riga del giornale di registrazione viene salvata. Se la voce di contratto ha più clienti, seleziona il cliente corretto nella voce di contratto. | Se il sistema non è in grado di determinare il cliente della voce di contratto nella riga del giornale di registrazione e se è vuoto nell'effettivo di tipo **Vendite non fatturate** creato dalla riga del giornale di registrazione, l'effettivo non verrà fatturato. |
    | Project | Seleziona il progetto su cui registrare l'effettivo. | In base al progetto, alla classe di transazione e all'attività selezionati, il sistema tenterà di determinare il contratto, la voce di contratto e il cliente della voce di contratto. |
    | Attività | Seleziona l'attività su cui registrare l'effettivo. | Se sono state associate attività con voci di contratto durante l'impostazione del contratto, il sistema utilizzerà l'attività selezionata, insieme a un progetto e una classe di transazione, per determinare il contratto, la voce di contratto e il cliente della voce di contratto. |
    | Categoria di transazione | Seleziona la categoria di transazione su cui registrare l'effettivo. | Per le spese, la categoria di transazione selezionata determina il prezzo predefinito che verrà inserito nella riga del giornale di registrazione al momento del salvataggio. |
    | Ruolo | Questo campo è rilevante per le righe del giornale di registrazione Inserimento ore. Seleziona il ruolo della risorsa che ha dedicato del tempo al progetto e/o all'attività. | Per le righe del giornale di registrazione inserimento ore, se usi la configurazione predefinita per l'immissione dei costi delle risorse e delle tariffe di fatturazione predefinite, il ruolo selezionato viene utilizzato insieme all'unità di risorse per determinare il prezzo predefinito che verrà inserito nella riga del giornale di registrazione al momento del salvataggio. Se usi una configurazione personalizzata per l'immissione dei prezzi predefiniti, è necessario rivedere tale configurazione per determinare se il campo **Ruolo** viene utilizzato per inserire i valori di prezzo predefiniti. |
    | Conto lavoro | Se la riga del giornale di registrazione rappresenta la capacità in conto lavoro o le spese o i materiali in conto lavoro, seleziona il conto lavoro pertinente. | Quando vengono registrate le righe del giornale di registrazione costi, il conto lavoro selezionato determinerà il listino prezzi utilizzato per inserire il costo unitario predefinito. |
    | Riga conto lavoro | Se la riga del giornale di registrazione rappresenta la capacità in conto lavoro o le spese o i materiali in conto lavoro, seleziona la riga conto lavoro pertinente. | Quando le righe del giornale di registrazione costi vengono registrate, la riga di conto lavoro selezionata garantisce che i calcoli della capacità disponibile sulla riga di conto lavoro siano calcolati correttamente. |
    | Metodo di importo | Questo campo è impostato su **Moltiplica quantità per prezzo** per impostazione predefinita. Quando viene utilizzato questo metodo, l'importo verrà calcolato come *Quantità* × *Prezzo*. L'altro metodo supportato è **Prezzo fisso**. Quando viene utilizzato questo metodo, il prezzo verrà impostato sull'importo e la quantità non verrà utilizzata nel calcolo. | |
    | Pianificazione unità e unità | Insieme, la pianificazione unità e l'unità identificano l'unità della quantità. | La combinazione dell'unità e della categoria della transazione viene utilizzata per inserire i prezzi predefiniti per le spese. Nella configurazione predefinita di Project Operations, la combinazione di unità, ruolo e unità di risorse viene utilizzata per inserire i prezzi predefiniti per l'inserimento ore. Se hai una configurazione personalizzata per l'inserimento dei prezzi predefiniti, verrà utilizzata insieme all'unità. La combinazione del prodotto e dell'unità viene utilizzata per inserire i prezzi predefiniti per i materiali. |
    | Quantità | Immetti la quantità. | |
    | Prezzo | Se il prezzo viene lasciato vuoto quando viene creata la riga del giornale di registrazione, i valori pertinenti verranno utilizzati per immettere i prezzi predefiniti, a seconda della classe di transazione. Se viene immesso un prezzo quando viene creata la riga del giornale di registrazione, verrà utilizzato quel prezzo. | |
    | Imposta | Inserisci qualsiasi importo di imposta. | A seconda dell'importo dell'imposta inserito, l'importo esteso verrà calcolato come *Importo* + *Imposta*. |

## <a name="confirm-an-entry-journal"></a>Confermare un giornale di registrazione di scritture contabili

Dopo aver inserito tutte le righe del giornale di registrazione in un giornale di registrazione di scritture contabili, è possibile confermare il giornale di registrazione. Questo processo registrerà ogni riga del giornale di registrazione come effettiva sui progetti appropriati.

Dopo che un giornale di registrazione è stato confermato, non è più possibile modificare il giornale né le sue righe.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Effettivi creati dalla conferma del giornale di registrazione di scritture contabili

Esistono alcune differenze fondamentali tra gli effettivi creati dalla conferma del giornale di registrazione di scritture contabili e gli effettivi creati durante l'approvazione dei registri di utilizzo di inserimento ore, spese e materiali e la conferma della fattura in Project Operations:

- I giornali di registrazione di scritture contabili non utilizzano le connessioni transazione per collegare il costo effettivo alle vendite effettive non fatturate. Gli effettivi creati quando i registri di utilizzo di inserimento ore, spese e materiali vengono approvati utilizzano sempre le connessioni transazione per collegare il costo e gli effettivi di vendita non fatturati.
- I giornali di registrazione di scritture contabili non utilizzano le origini transazione per collegare il costo effettivo e le vendite effettive non fatturate a un record di origine. Gli effettivi creati quando i registri di utilizzo di inserimento ore, spese e materiali vengono approvati utilizzano sempre le origini transazione per collegare il costo e gli effettivi di vendita non fatturati all'inserimento ore di origine.
- Quando le vendite effettive non fatturate create dalla conferma del giornale di registrazione di scritture contabili vengono fatturate, le vendite effettive fatturate create durante la conferma fattura sono collegate alle vendite effettive non fatturate, in modo simile alle vendite effettive non fatturate che vengono create quando i registri di utilizzo Inserimento ore, Spese e Materiale sono approvati.
- Le righe del giornale di registrazione di scritture contabili create per l'inserimento ore immesso da risorse interorganizzative non causano effettivi di tipo **Costo unità gestione risorse** e **Vendite interorganizzative** da creare automaticamente. Questi effettivi devono essere creati manualmente. Questo comportamento è diverso dal comportamento per gli inserimenti ore registrati da risorse interorganizzative. In tal caso, una volta approvato l'inserimento ore, l'applicazione crea automaticamente gli effettivi di tipo **Costo** nel progetto e gli effettivi di tipo **Costo unità gestione risorse** e **Vendite interorganizzative** sulla divisione proprietaria del dipendente. Quindi utilizza le connessioni delle transazioni per collegare insieme questi effettivi e le origini delle transazioni per collegarli all'inserimento ore di origine.
- Quando i giornali di registrazione di scritture contabili vengono confermati, creano valori effettivi. Tuttavia, i giornali di registrazione correzioni non possono essere utilizzati per correggere questi effettivi. Questo comportamento è diverso dal comportamento per i valori effettivi creati quando vengono approvati i registri di utilizzo di inserimento ore, spese e materiali. In tal caso, l'applicazione consente di utilizzare i giornali di registrazione di correzioni per correggere gli effettivi ed eventuali errori, a condizione che tali effettivi non siano ancora stati fatturati. Se sono già stati fatturati, puoi comunque correggere un effettivo se elabori l'intero credito dell'effettivo al cliente.

> [!NOTE]
> I giornali di registrazione di scritture contabili non applicano rigide regole predefinite. Pertanto, utilizza questi giornali di registrazione di scritture contabili il meno possibile e presta attenzione a non creare dati finanziari corrotti nel sistema. Ogni volta che puoi, utilizza i registri di utilizzo di inserimento, spese e materiali, l'impostazione passaggio fondamentale e acconto sui contratti di progetto e il processo di conferma della fattura del progetto anziché i giornali di registrazione di scrittura contabili per creare i valori effettivi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
