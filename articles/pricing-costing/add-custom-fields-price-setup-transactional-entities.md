---
title: Aggiungere campi personalizzati richiesti all'impostazione e alle entità transazionali
description: Questo argomento fornisce informazioni su come aggiungere riferimenti di campi personalizzati richiesti a entità, moduli e viste.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a27bfe881fdb6431941fa860d279e3e7b526f623
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898311"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Aggiungere campi personalizzati richiesti all'impostazione e alle entità transazionali

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

In questo argomento si presuppone che siano state completate le procedure incluse in [Creare campi ed entità personalizzati come dimensioni di determinazione dei prezzi](create-custom-fields-entities-pricing-dimensions.md). Se non hai completato queste procedure, completale prima di leggere questo argomento. 

In questo argomento, le procedure mostreranno come aggiungere i riferimenti di campo personalizzati necessari alle entità e agli elementi dell'interfaccia utente come moduli e viste.

## <a name="add-custom-pricing-dimension-fields"></a>Aggiungere campi per dimensioni di determinazione dei prezzi personalizzate 
Dopo la creazione di campi ed entità personalizzati, è necessario indicare alla configurazione dei prezzi e alle entità transazionali l'esistenza di entità personalizzate o set di opzioni creando campi di riferimento. A seconda se l'elenco delle dimensioni di determinazione dei prezzi include dimensioni di set di opzioni o di entità oppure entrambe, segui solo i passaggi in **Dimensioni di determinazione dei prezzi personalizzate basate su set di opzioni** o in **Dimensioni di determinazione dei prezzi personalizzate basate su entità** oppure in entrambi le sezioni.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensioni di determinazione dei prezzi personalizzate basate su set di opzioni
Quando una dimensione di determinazione dei prezzi è basata su set di opzioni, aggiungila come campo alle entità chiave. Nella procedura seguente, **Ubicazione lavoro risorsa** e **Ore lavorative risorsa** vengono utilizzati come dimensioni di determinazione dei prezzi basate su set di opzioni. Questi devono essere dapprima aggiunti come campi alle entità di determinazione dei prezzi, ovvero **Prezzo ruolo** e **Ricarico prezzo ruolo**.

1. In Project Operations, seleziona **Impostazioni** > **Soluzioni** e fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Prezzo ruolo**.
3. Espandi l'entità **Prezzo ruolo** e seleziona **Campi**.
4. Seleziona **Nuovo** per creare un nuovo campo denominato **Ubicazione lavoro risorsa** e seleziona **Set di opzioni** come tipo di campo. 
5. Seleziona **Utilizza come set di opzioni esistente**, seleziona il set di opzioni **Ubicazione lavoro risorsa** e quindi seleziona **Salva**.
6. Ripeti i passaggi da 1 a 5 per aggiungere questo campo all'entità **Ricarico prezzo ruolo**. 
7. Ripeti i passaggi da 1 a 5 per il set di opzioni **Ore lavorative risorsa**.

> [!IMPORTANT]
> Quando aggiungi un campo a più entità, utilizza lo stesso nome di campo in tutte le entità. 

Nelle fasi di vendita e stima di un progetto, le stime del lavoro richiesto per completare il lavoro **Locale** e **In loco**, presenti in **Ore regolari** e **Ore di lavoro straordinario**, sono utilizzate per stimare il valore dell'offerta/del progetto. I campi **Ubicazione lavoro risorsa** e **Ore lavorative risorsa** sono aggiunti alle entità di stima **Dettagli riga di offerta**, **Dettaglio voce di contratto**, **Membro del team di progetto** e **Riga di stima**.

1. In Project Operations, seleziona **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Dettagli riga di offerta**.
3. Espandi l'entità **Dettagli riga di offerta** e seleziona **Campi**.
4. Seleziona **Nuovo** per creare un nuovo campo denominato **Ubicazione lavoro risorsa** e seleziona il tipo di campo **Set di opzioni**. 
5. Seleziona **Utilizza come set di opzioni esistente** e **Ubicazione lavoro risorsa** e quindi seleziona **Salva**.
6. Ripeti i passaggi da 1 a 5 per aggiungere questo campo alle entità **Dettagli di voce di contratto di progetto**, **Membro del team di progetto** e **Riga di stima**.
7. Ripeti i passaggi da 1 a 6 per il set di opzioni **Ore lavorative risorsa**. 

Per la consegna e la fatturazione, è necessario determinare correttamente il prezzo del lavoro completato per specificare se è **Locale** o **In loco** e se è stato completato durante le **Ore regolari** o le **Ore di lavoro straordinario** per i valori effettivi di progetto. I campi **Ore lavorative di una risorsa** e **Ubicazione lavoro risorsa** devono essere aggiunti alle entità **Inserimento ore**, **Valore effettivo**, **Dettagli di riga fattura** e **Riga giornale di registrazione**.

1. Seleziona **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Inserimento ore**.
3. Espandi l'entità **Dettagli riga di offerta** e seleziona **Campi**.
4. Seleziona **Nuovo** per creare un nuovo campo denominato **Ubicazione lavoro risorsa** e seleziona **Set di opzioni** come tipo di campo. 
5. Seleziona **Utilizza come set di opzioni esistente**, seleziona il set di opzioni **Ubicazione lavoro risorsa** e quindi seleziona **Salva**.
6. Ripeti i passaggi da 1 a 5 per aggiungere questo campo alle entità **Valore effettivo**, **Dettagli di riga fattura** e **Riga giornale di registrazione**.
7. Ripeti i passaggi da 1 a 6 per il set di opzioni **Ore lavorative risorsa**. 

Questa operazione completa le modifiche allo schema necessarie per le dimensioni personalizzate basate su set di opzioni.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensioni di determinazione dei prezzi personalizzate basate su entità

Quando la dimensione di determinazione dei prezzi personalizzata è un'entità, aggiungi la relazione 1:N tra l'entità di dimensione e le entità chiave. Utilizzando l'esempio Titolo standard precedente, è ragionevole prevedere che a ogni dipendente sia assegnato un titolo standard. Di conseguenza, necessiti una relazione 1:N tra Titolo standard e Risorsa prenotabile oppure una relazione N:1 se è stata creata tra Risorsa prenotabile e Titolo standard.

1. In Project Operations, seleziona **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Titolo standard**.
3. Espandi l'entità **Titolo standard** e seleziona **Relazione 1:N**.
4. Seleziona **Nuovo** per creare un nuova relazione 1:N denominata **Da Titolo standard a Risorsa prenotabile**. Immetti le informazioni richieste e quindi seleziona **Salva**.

Anche Titolo standard deve essere aggiunto alle entità di determinazione dei prezzi, ovvero **Prezzo ruolo** e **Ricarico prezzo ruolo**. Anche questa operazione viene eseguita utilizzando relazioni 1:N tra le entità **Titolo standard** e **Prezzo ruolo** e tra le entità **Titolo standard** e **Ricarico prezzi ruolo**.

1. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Titolo standard**.
2. Espandi l'entità **Titolo standard** e seleziona **Relazione 1:N**.
3. Seleziona **Nuovo** per creare un nuova relazione 1:N denominata **Da Titolo standard a Prezzo ruolo**. Immetti le informazioni richieste e quindi seleziona **Salva**.
4. Ripeti i passaggi da 1 a 4 per creare relazioni 1:N tra le entità **Titolo standard** e **Ricarico di prezzo ruolo**.

Nelle fasi di vendita e stima del progetto, per determinare il prezzo dell'offerta/del progetto, sono necessarie stime del lavoro richiesto per ogni titolo standard. Ciò significa che sono necessarie relazioni 1:N tra Titolo standard e ognuna di queste entità di stima: 

- **Dettagli riga di offerta**
- **Dettagli di voce di contratto di progetto**
- **Membro del team di progetto**
- **Riga di stima**

5. Ripeti i passaggi da 1 a 5 per creare relazioni 1:N tra **Titolo standard** e **Dettagli riga di offerta**, **Dettagli di voce di contratto di progetto**, **Membro del team di progetto** e **Riga di stima**.

  Nelle fasi di consegna e fatturazione, è necessario determinare accuratamente il prezzo del lavoro completato per ogni titolo standard nel valori effettivi di progetto. Ciò significa che deve esistere una relazione 1:N tra **Titolo standard** e le entità **Inserimento ore**, **Valore effettivo**, **Dettagli di riga fattura** e **Riga giornale di registrazione**.

6. Ripeti i passaggi da 1 a 6 per creare relazioni 1:N tra **Titolo standard** e le entità **Inserimento ore**, **Valore effettivo**, **Dettagli di riga fattura** e **Riga giornale di registrazione**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Configurare l'impostazione predefinita del valore della dimensione utilizzando funzionalità di mapping della piattaforma
Per Inserimento ore, sarebbe utile che il sistema utilizzasse, per impostazione predefinita, il titolo standard nell'inserimento ore anziché quello della risorsa prenotabile che sta registrando l'inserimento ore. Utilizza i passaggi seguenti per aggiungere mapping di campi nella relazione 1:N tra **Risorsa prenotabile** e **Inserimento ore**.

1. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità > Titolo standard**.
2. Espandi l'entità **Titolo standard** e seleziona **Relazione 1:N**.
3. Fai doppio clic su **Da Risorsa prenotabile a Inserimento ore**. Nella pagina **Relazione** seleziona **Utilizza mapping campi**. 
4. Seleziona **Nuovo** per creare un nuovo mapping dei campi tra il campo **Titolo standard** dell'entità **Risorsa prenotabile** e il campo di riferimento **Titolo standard** dell'entità **Inserimento ore**. 

Questa operazione completa le modifiche allo schema necessarie per le dimensioni personalizzate basate su entità.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Aggiungere campi personalizzati a moduli, viste e regole di business

Dopo aver apportato tutte le modifiche necessarie allo schema, è necessario rendere i campi visibili nell'interfaccia utente tramite l'aggiunta di campi ai moduli e alle viste.

1. Apri il modulo o la vista. Nel riquadro di spostamento a destra, seleziona il campo e trascinalo nel canvas del modulo. 
2. Se modifichi una vista, utilizza il riquadro di spostamento destro, seleziona **Aggiungi campi** e nella finestra di dialogo **Elenco campi**, seleziona i campi necessari e seleziona **OK**.

La tabella seguente fornisce un elenco completo di moduli e viste predefinite, elencati per entità, che devono essere aggiornati con i nuovi campi. Se nelle personalizzazioni di queste entità sono presenti ulteriori viste o moduli, aggiungi i nuovi campi anche a questi.

| Entity        | Moduli che necessitano il nuovo campo   |Viste che necessitano il nuovo campo      |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezzo ruolo|• Informazioni |• Prezzi categorie di risorse attivi<br> • Vista Prezzo categoria di risorsa associata|
|  Ricarico prezzo ruolo|• Informazioni|• Ricarico prezzo ruolo attivo<br>• Vista Ricarico prezzo ruolo associata|
|  Dettagli riga di offerta|• Informazioni sul progetto<br>• Creazione rapida progetti|• Dettagli di riga di offerta attiva<br>• Dettagli di riga di offerta combinata<br>• Vista Dettagli riga di offerta associata|
|  Dettagli di voce di contratto di progetto|• Informazioni sul progetto<br>• Creazione rapida progetti|• Dettagli voce di contratto combinati<br>• Dettagli voce di contratto attivi<br>• Vista Dettaglio riga di contratto associata|
|  Membro del team di progetto|• Informazioni<br>• Nuovo modulo|• Membri del team di progetto attivi<br>• Membri del team di progetto<br>• Vista Membri del team di progetto associata|
|  Inserimento ore|• Informazioni<br>• Crea inserimento ore|• Inserimenti ore personali per data<br>• Inserimenti ore personali per questa settimana<br>• Inserimenti ore per l'approvazione.|
|  Riga giornale di registrazione|• Informazioni<br>• Creazione rapida|• Righe giornale di registrazione attive<br>• Vista Riga giornale di registrazione associata|
|  Dettagli di riga fattura|• Informazioni<br>• Creazione rapida|• Dettagli di riga fattura attiva<br>• Transazioni fattura addebitabili<br>• Transazioni fattura gratuite<br>• Vista Dettagli di riga fattura associata<br>• Transazione fattura non addebitabile|
|  Valore effettivo|• Informazioni<br>• Valori effettivi attivi|• Vista Valore effettivo associata|

A seconda di quanto hai definito, è possibile che sia necessario aggiungere campi personalizzati anche alle regole di business. Un esempio predefinito riguarda la regola di business **Possibilità di modifica di Inserimento ore basata sullo stato**. Tale regola definisce quali campi devono essere bloccati quando lo stato di Inserimento ore non è modificabile ad esempio **Approvato**. Aggiungi campi a questa regola di business di modo che i campi siano bloccati per la modifica quando lo stato di Inserimento ore non è **Bozza** o **Restituito**.
