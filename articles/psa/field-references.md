---
title: Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali
description: In questo argomento vengono fornite informazioni sull'aggiunta di campi personalizzati alla configurazione dei prezzi e ad entità transazionali.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cb4a99b10e5d0c79e80bcd46d2f60ccdab4487aa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596929"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali 

[!include [banner](../includes/psa-now-project-operations.md)]

In questo argomento si presuppone che siano state completate le procedure incluse in [Creare campi ed entità personalizzati](create-custom-fields-entities.md). Se non hai completato queste procedure, completale prima di leggere questo argomento. 

In questo argomento, le procedure mostreranno come aggiungere i riferimenti di campo personalizzati necessari alle entità e agli elementi dell'interfaccia utente come moduli e viste.

## <a name="add-custom-pricing-dimension-fields"></a>Aggiungere campi per dimensioni di determinazione dei prezzi personalizzate 
Dopo la creazione di campi ed entità personalizzati, è necessario indicare alla configurazione dei prezzi e alle entità transazionali l'esistenza di entità personalizzate o set di opzioni creando campi di riferimento. A seconda se l'elenco delle dimensioni di determinazione dei prezzi include dimensioni di set di opzioni o di entità oppure entrambe, segui solo i passaggi in **Dimensioni di determinazione dei prezzi personalizzate basate su set di opzioni** o in **Dimensioni di determinazione dei prezzi personalizzate basate su entità** oppure in entrambi le sezioni.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensioni di determinazione dei prezzi personalizzate basate su set di opzioni
Quando una dimensione di determinazione dei prezzi è basata su set di opzioni, aggiungila come campo alle entità chiave di Project Service. Nella procedura seguente, **Ubicazione lavoro risorsa** e **Ore lavorative risorsa** vengono utilizzati come dimensioni di determinazione dei prezzi basate su set di opzioni. Questi devono essere dapprima aggiunti come campi alle entità di determinazione dei prezzi, ovvero **Prezzo ruolo** e **Ricarico prezzo ruolo**.

1. In Project Service Automation (PSA) fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Prezzo ruolo**.
3. Espandi l'entità **Prezzo ruolo** e seleziona **Campi**.
4. Fai clic su **Nuovo** per creare un nuovo campo denominato **Ubicazione lavoro risorsa** e seleziona **Set di opzioni** come tipo di campo. 
5. Seleziona **Utilizza come set di opzioni esistente**, seleziona il set di opzioni **Ubicazione lavoro risorsa** e quindi fai clic su **Salva**.
6. Ripeti i passaggi da 1 a 5 per aggiungere questo campo all'entità **Ricarico prezzo ruolo**. 
7. Ripeti i passaggi da 1 a 5 per il set di opzioni **Ore lavorative risorsa**.

> [!IMPORTANT]
> Quando aggiungi un campo a più entità, utilizza lo stesso nome di campo in tutte le entità. 

> ![Aggiungere Ubicazione lavoro risorsa a Prezzo ruolo.](media/RWL-Field.png)

Nelle fasi di vendita e stima di un progetto, le stime del lavoro richiesto per completare il lavoro **Locale** e **In loco**, presenti in **Ore regolari** e **Ore di lavoro straordinario**, sono utilizzate per stimare il valore dell'offerta/del progetto. I campi **Ubicazione lavoro risorsa** e **Ore lavorative risorsa** sono aggiunti alle entità di stima **Dettagli riga di offerta**, **Dettaglio voce di contratto**, **Attività di progetto**, **Membro del team di progetto** e **Riga di stima**.

1. In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Dettagli riga di offerta**.
3. Espandi l'entità **Dettagli riga di offerta** e seleziona **Campi**.
4. Fai clic su **Nuovo** per creare un nuovo campo denominato **Ubicazione lavoro risorsa** e seleziona il tipo di campo **Set di opzioni**. 
5. Seleziona **Utilizza come set di opzioni esistente** e **Ubicazione lavoro risorsa** e quindi fai clic su **Salva**.
6. Ripeti i passaggi da 1 a 5 per aggiungere questo campo alle entità **Dettagli di voce di contratto di progetto**,**Attività di progetto**, **Membro del team di progetto** e **Riga di stima**.
7. Ripeti i passaggi da 1 a 6 per il set di opzioni **Ore lavorative risorsa**. 

> ![Aggiungere Ubicazione lavoro risorsa a Riga di stima.](media/RWL-Default-Value.png)


Per la consegna e la fatturazione, è necessario determinare correttamente il prezzo del lavoro completato per specificare se è **Locale** o **In loco** e se è stato completato durante le **Ore regolari** o le **Ore di lavoro straordinario** per i valori effettivi di progetto. I campi **Ore lavorative di una risorsa** e **Ubicazione lavoro risorsa** devono essere aggiunti alle entità **Inserimento ore**, **Valore effettivo**, **Dettagli di riga fattura** e **Riga giornale di registrazione**.

1. In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Inserimento ore**.
3. Espandi l'entità **Dettagli riga di offerta** e seleziona **Campi**.
4. Fai clic su **Nuovo** per creare un nuovo campo denominato **Ubicazione lavoro risorsa** e seleziona **Set di opzioni** come tipo di campo. 
5. Seleziona **Utilizza come set di opzioni esistente**, seleziona il set di opzioni **Ubicazione lavoro risorsa** e quindi fai clic su **Salva**.
6. Ripeti i passaggi da 1 a 5 per aggiungere questo campo alle entità **Valore effettivo**, **Dettagli di riga fattura** e **Riga giornale di registrazione**.
7. Ripeti i passaggi da 1 a 6 per il set di opzioni **Ore lavorative risorsa**. 

> ![Aggiungere Ubicazione lavoro risorsa a Inserimento ore.](media/RWL-time-entry.png)

Questa operazione completa le modifiche allo schema necessarie per le dimensioni personalizzate basate su set di opzioni.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensioni di determinazione dei prezzi personalizzate basate su entità

Quando la dimensione di determinazione dei prezzi personalizzata è un'entità, aggiungi la relazione 1:N tra l'entità di dimensione e le entità chiave di Project Service. Utilizzando l'esempio Titolo standard precedente, è ragionevole prevedere che a ogni dipendente sia assegnato un titolo standard. Di conseguenza, necessiti una relazione 1:N tra Titolo standard e Risorsa prenotabile oppure una relazione N:1 se è stata creata tra Risorsa prenotabile e Titolo standard.

1. In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Titolo standard**.
3. Espandi l'entità **Titolo standard** e seleziona **Relazione 1:N**.
4. Fai clic su **Nuovo** per creare un nuova relazione 1:N denominata **Da Titolo standard a Risorsa prenotabile**. Immetti le informazioni richieste e quindi fai clic su **Salva**.

> ![Aggiungere Titolo standard come campo di riferimento a Risorsa prenotabile.](media/ST-BR.png)

Anche Titolo standard deve essere aggiunto alle entità di determinazione dei prezzi di Project Service, ovvero **Prezzo ruolo** e **Ricarico prezzo ruolo**. Anche questa operazione viene eseguita utilizzando relazioni 1:N tra le entità **Titolo standard** e **Prezzo ruolo** e tra le entità **Titolo standard** e **Ricarico prezzi ruolo**.

1. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Titolo standard**.
2. Espandi l'entità **Titolo standard** e seleziona **Relazione 1:N**.
3. Fai clic su **Nuovo** per creare un nuova relazione 1:N denominata **Da Titolo standard a Prezzo ruolo**. Immetti le informazioni richieste e quindi fai clic su **Salva**.
4. Ripeti i passaggi da 1 a 4 per creare relazioni 1:N tra le entità **Titolo standard** e **Ricarico di prezzo ruolo**.

Nelle fasi di vendita e stima del progetto, per determinare il prezzo dell'offerta/del progetto, sono necessarie stime del lavoro richiesto per ogni titolo standard. Ciò significa che sono necessarie relazioni 1:N tra Titolo standard e ognuna di queste entità di stima in Project Service: 

- **Dettagli riga di offerta**
- **Dettagli di voce di contratto di progetto**
- **Attività di progetto**
- **Membro del team di progetto**
- **Riga di stima**

5. Ripeti i passaggi da 1 a 5 per creare relazioni 1:N tra **Titolo standard** e **Dettagli riga di offerta**, **Dettagli di voce di contratto di progetto**, **Attività di progetto**, **Membro del team di progetto** e **Riga di stima**.

> ![Aggiungere Titolo standard come campo di riferimento a Riga di stima.](media/ST-Estimate-Line.png)

Nelle fasi di consegna e fatturazione, è necessario determinare accuratamente il prezzo del lavoro completato per ogni titolo standard nel valori effettivi di progetto. Ciò significa che deve esistere una relazione 1:N tra **Titolo standard** e le entità **Inserimento ore**, **Valore effettivo**, **Dettagli di riga fattura** e **Riga giornale di registrazione**.

6. Ripeti i passaggi da 1 a 6 per creare relazioni 1:N tra **Titolo standard** e le entità **Inserimento ore**, **Valore effettivo**, **Dettagli di riga fattura** e **Riga giornale di registrazione**.

> ![Aggiungere Titolo standard come campo di riferimento a Inserimento ore.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Configurare l'impostazione predefinita del valore della dimensione utilizzando funzionalità di mapping della piattaforma
Per Inserimento ore, sarebbe utile che il sistema utilizzasse, per impostazione predefinita, il titolo standard nell'inserimento ore anziché quello della risorsa prenotabile che sta registrando l'inserimento ore. Utilizza i passaggi seguenti per aggiungere mapping di campi nella relazione 1:N tra **Risorsa prenotabile** e **Inserimento ore**.

1. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Titolo standard**.
2. Espandi l'entità **Titolo standard** e seleziona **Relazione 1:N**.
3. Fai doppio clic su **Da Risorsa prenotabile a Inserimento ore**. Nella pagina **Relazione**, fai clic su **Utilizza mapping campi**. 
4. Fai clic su **Nuovo** per creare un nuovo mapping dei campi tra il campo **Titolo standard** dell'entità **Risorsa prenotabile** e il campo di riferimento **Titolo standard** dell'entità **Inserimento ore**. 

> ![Impostare mapping di campi per consentire l'impostazione predefinita di Titolo standard da Risorsa prenotabile a Inserimento ore.](media/ST-Mapping2.png)


Questa operazione completa le modifiche allo schema necessarie per le dimensioni personalizzate basate su entità.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Aggiungere campi personalizzati a moduli, viste e regole di business

Dopo aver apportato tutte le modifiche necessarie allo schema, è necessario rendere i campi visibili nell'interfaccia utente tramite l'aggiunta di campi ai moduli e alle viste.

1. Apri il modulo o la vista. Nel riquadro di spostamento a destra, seleziona il campo e trascinalo nel canvas del modulo. 
2. Se modifichi una vista, utilizza il riquadro di spostamento destro, fai clic su **Aggiungi campi** e nella finestra di dialogo **Elenco campi**, seleziona i campi necessari e fai clic su **OK**.

La tabella seguente fornisce un elenco completo di moduli e viste predefinite, elencati per entità, che devono essere aggiornati con i nuovi campi. Se nelle personalizzazioni di queste entità sono presenti ulteriori viste o moduli, aggiungi i nuovi campi anche a questi.

| Entità Project Service        | Moduli che necessitano il nuovo campo   |Viste che necessitano il nuovo campo      |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezzo ruolo|• Informazioni |• Prezzi categorie di risorse attivi<br> • Vista Prezzo categoria di risorsa associata|
|  Ricarico prezzo ruolo|• Informazioni|• Ricarico prezzo ruolo attivo<br>• Vista Ricarico prezzo ruolo associata|
|  Dettagli riga di offerta|• Informazioni sul progetto<br>• Creazione rapida progetti|• Dettagli di riga di offerta attiva<br>• Dettagli di riga di offerta combinata<br>• Vista Dettagli riga di offerta associata|
|  Dettagli di voce di contratto di progetto|• Informazioni sul progetto<br>• Creazione rapida progetti|• Dettagli voce di contratto combinati<br>• Dettagli voce di contratto attivi<br>• Vista Dettaglio riga di contratto associata|
|  Attività di progetto|• Informazioni<br>• Nuovo modulo||
|  Membro del team di progetto|• Informazioni<br>• Nuovo modulo|• Membri del team di progetto attivi<br>• Membri del team di progetto<br>• Vista Membri del team di progetto associata|
|  Inserimento ore|• Informazioni<br>• Crea inserimento ore|• Inserimenti ore personali per data<br>• Inserimenti ore personali per questa settimana<br>• Inserimenti ore per l'approvazione.|
|  Riga giornale di registrazione|• Informazioni<br>• Creazione rapida|• Righe giornale di registrazione attive<br>• Vista Riga giornale di registrazione associata|
|  Dettagli di riga fattura|• Informazioni<br>• Creazione rapida|• Dettagli di riga fattura attiva<br>• Transazioni fattura addebitabili<br>• Transazioni fattura gratuite<br>• Vista Dettagli di riga fattura associata<br>• Transazione fattura non addebitabile|
|  Valore effettivo|• Informazioni<br>• Valori effettivi attivi|• Vista Valore effettivo associata|

A seconda di quanto hai definito, è possibile che sia necessario aggiungere campi personalizzati anche alle regole di business. Un esempio predefinito riguarda la regola di business **Possibilità di modifica di Inserimento ore basata sullo stato**. Tale regola definisce quali campi devono essere bloccati quando lo stato di Inserimento ore non è modificabile ad esempio **Approvato**. Aggiungi campi a questa regola di business di modo che i campi siano bloccati per la modifica quando lo stato di Inserimento ore non è **Bozza** o **Restituito**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
