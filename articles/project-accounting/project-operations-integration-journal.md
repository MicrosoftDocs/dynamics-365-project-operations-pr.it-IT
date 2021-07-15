---
title: Giornale di registrazione integrazione in Project Operations
description: Questo argomento fornisce informazioni sull'utilizzo del giornale di registrazione integrazione in Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f4428bac8e82bdfc848c199b0e294486b9fde82e
ms.sourcegitcommit: 639ec8a41fda15dedfd6918702d33ea406999ba6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304261"
---
# <a name="integration-journal-in-project-operations"></a>Giornale di registrazione integrazione in Project Operations

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Le voci di tempi e spese creano transazioni di **valori effettivi** che rappresentano la visione operativa del lavoro completato rispetto a un progetto. Dynamics 365 Project Operations fornisce ai contabili uno strumento per rivedere le transazioni e modificare gli attributi di contabilità secondo necessità. Dopo aver completato la revisione e le rettifiche, le transazioni vengono registrate nella contabilità secondaria del progetto e nella contabilità generale. Un contabile può eseguire queste attività utilizzando il giornale di registrazione **Integrazione Project Operations** (**Dynamics 365 Finance** > **Gestione progetti e contabilità** > **Giornali di registrazione** > **Integrazione Project Operations**).

![Flusso del giornale di registrazione integrazione](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Creare record nel giornale di registrazione integrazione Project Operations

I record nel giornale di registrazione integrazione Project Operations vengono creati utilizzando un processo periodico, **Importa da tabella di gestione temporanea**. Puoi eseguire questo processo andando in **Dynamics 365 Finance** > **Gestione progetti e contabilità** > **Periodico** > **Integrazione Project Operations** > **Importa da tabella di gestione temporanea**. È possibile eseguire il processo in modo interattivo o configurarlo in modo che venga eseguito in background, se necessario.

Quando viene eseguito il processo periodico, vengono trovati tutti i valori effettivi che non sono stati ancora aggiunti al giornale di registrazione di integrazione Project Operations. Viene creata una riga di giornale di registrazione per ogni transazione effettiva.
Il sistema raggruppa le righe del giornale di registrazione in giornali separati in base al valore selezionato nel campo **Unità periodo nel giornale di registrazione di integrazione Project Operations** (**Finance** > **Gestione progetti e contabilità** > **Configurazione** > **Gestione progetti e parametri contabili**, scheda **Project Operations in Dynamics 365 Customer Engagement**). I valori possibili per questo campo includono:

  - **Giorni**: i valori effettivi sono raggruppati per data di transazione. Per ogni giorno viene creato un giornale di registrazione separato.
  - **Mesi**: i valori effettivi sono raggruppati per mese di calendario. Per ogni mese viene creato un giornale di registrazione separato.
  - **Anni**: i valori effettivi sono raggruppati per anno di calendario. Per ogni anno viene creato un giornale di registrazione separato.
  - **Tutto**: tutte le transazioni effettive sono incluse nello stesso giornale di registrazione di integrazione. Se il giornale di registrazione non è disponibile durante l'esecuzione del processo periodico, ad esempio se il giornale di registrazione è in fase di registrazione delle transazioni, viene creato un nuovo giornale di registrazione.

Le righe di giornale di registrazione vengono create in base ai valori effettivi del progetto. Il seguente elenco include alcune delle regole predefinite e di trasformazione più importanti:

  - Ogni transazione effettiva del progetto ha una riga nel giornale di registrazione di integrazione Project Operations. Le transazioni di costo e di vendita non fatturate per il tipo di fatturazione di tempo e materiale vengono visualizzate su righe separate.
  - Il campo **Data** rappresenta la data della transazione. Il campo **Data contabile** rappresenta la data in cui la transazione viene registrata nel libro mastro. Se la data contabile è in un [periodo finanziario chiuso](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) e il parametro **Imposta automaticamente la data contabile per aprire il periodo contabile** è impostato nella scheda **Finanziario** della pagina **Gestione progetti e parametri contabili**, il sistema adatterà la data contabile della transazione alla prima data nel successivo periodo di libro mastro aperto.
  - Il campo **Giustificativo** mostra il numero del giustificativo per ogni transazione effettiva. La sequenza del numero del giustificativo è definita nella scheda **Sequenze numeriche** della pagina **Gestione progetti e parametri contabili**. Ad ogni riga viene assegnato un nuovo numero. Dopo aver registrato il giustificativo, è possibile visualizzare la correlazione tra il costo e la transazione di vendita non fatturata selezionando **Giustificativi correlati** nella pagina **Transazione giustificativo**.
  - Il campo **Categoria** rappresenta una transazione di progetto e le impostazioni predefinite in base alla categoria di transazione per il valore effettivo di progetto correlato.
    - Se **Categoria di transazione** è impostato nel valore effettivo di progetto e una **categoria di progetto** correlata esiste in una determinata persona giuridica, la categoria predefinita è questa categoria di progetto.
    - Se **Categoria di transazione** non è impostato nel valore effettivo di progetto, il sistema utilizza il valore del campo **Valori predefiniti categoria di progetto** della scheda **Project Operations in Dynamics 365 Customer Engagement** nella pagina **Gestione progetti e parametri contabili**.
  - Il campo **Risorsa** rappresenta la risorsa del progetto relativa a questa transazione. La risorsa viene utilizzata come riferimento nelle proposte di fatturazione del progetto ai clienti.
  - Il campo **Tasso di cambio** è predefinito dal **Tasso di cambio valuta** impostato in Dynamics 365 Finance. Se manca l'impostazione del tasso di cambio, il processo periodico **Importa da gestione temporanea** non aggiungerà il record a un giornale di registrazione e verrà aggiunto un messaggio di errore al registro di esecuzione del lavoro.
  - Il campo **Proprietà riga** rappresenta il tipo di fatturazione nei valori effettivi del progetto. La proprietà della riga e la mappatura del tipo di fatturazione sono definite nella scheda **Project Operations in Dynamics 365 Customer Engagement** della pagina **Gestione progetti e parametri contabili**.

Solo i seguenti attributi di contabilità possono essere aggiornati nelle righe del giornale di registrazione di integrazione Project Operations:

- **Fatturazione della fascia IVA** e **Gruppo IVA articolo di fatturazione**
- **Dimensioni finanziarie** (usando l'azione **Distribuisci importi**)

Le righe del giornale di registrazione integrazione possono essere eliminate, tuttavia tutte le righe non registrate verranno inserite nuovamente nel giornale dopo aver rieseguito il processo periodico **Importa da gestione temporanea**.

Quando registri il giornale di registrazione integrazione, vengono creati un registro secondario del progetto e le transazioni di contabilità generale. Questi vengono utilizzati nella fatturazione dei clienti downstream, nel riconoscimento dei ricavi e nel reporting finanziario.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
