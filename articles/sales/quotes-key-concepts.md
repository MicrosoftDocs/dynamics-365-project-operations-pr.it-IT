---
title: 'Concetti chiave: offerte'
description: Questo argomento fornisce informazioni sulle offerte di progetto e sulle offerte di vendita disponibili in Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42ea1eb71b3285159b3fdf79ba34a562f948fd6e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079042"
---
# <a name="quotes---key-concepts"></a>Concetti chiave: offerte

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Dynamics 365 Project Operations, esistono due tipi di offerte: progetto e vendite. Questi due tipi di offerte differiscono nei modi seguenti:

- **Griglie per le voci** : Un'offerta di vendita include una sola griglia per le voci. In un'offerta di progetto sono presenti due griglie per le voci. Una griglia è per le righe di progetto e l'altra per le righe di prodotto.
- **Attivazione e revisioni** : le offerte di vendita supportano l'attivazione e le revisioni. Questi processi non sono supportati in un'offerta di progetto.
- **Ordini allegati** : è possibile associare più ordini a un'offerta di vendita, ma un solo contratto di progetto a un'offerta di progetto.
- **Conclusione di un'offerta** : quando concludi un'offerta di vendita, l'opportunità correlata può rimanere aperta. Dopo l'acquisizione di un'offerta di progetto, la relativa opportunità viene chiusa.
- **Campi e concetti** : un'offerta di vendita non include alcuni campi e concetti inclusi in un'offerta di progetto. Questi campi sono **Unità contratto** , **Gestione account** e **Nome contatto fatturazione**.  
- **Tipo** : le offerte di vendita e di progetto sono inoltre identificate da un campo basato su set di opzioni denominato **Tipo**. Per un'offerta di vendita, il valore di questo campo è **Basato su articolo**. Per un'offerta di progetto, il valore di questo campo è **Basato su lavoro**.

In questo argomento vengono descritti i dettagli delle offerte di progetto.

Un'offerta di progetto in Project Operations può avere molteplici voci o righe di offerta. In effetti, un'offerta di progetto include due griglie per le voci. Una griglia è per le righe basate su progetto che consentono stime dettagliate. L'altra griglia è per le righe basate su prodotto che utilizzano un prezzo unitario e un approccio basato sulla quantità.

- **Basate su progetto** : il valore dell'offerta viene determinato dopo la stima della quantità di lavoro necessario. Puoi stimare il lavoro ad alto livello, direttamente come dettagli di riga sotto ogni riga di offerta o in base a stime iniziali, utilizzando un progetto e un piano di progetto. Le righe di offerta basate su progetto sono disponibili solo nelle offerte basate su progetto create utilizzando Project Operations. Questo tipo di riga di offerta è un modulo personalizzato delle righe di offerta fuori catalogo disponibili in Microsoft Dynamics 365 Sales.

- **Basate su prodotto** : il valore dell'offerta viene determinato in base alla quantità di unità vendute e al prezzo di vendita unitario. Il prodotto in una riga basata su prodotto può provenire da un catalogo prodotti in Sales, oppure può essere un prodotto che definisci. Questo tipo di riga di offerta è disponibile anche nelle offerte basate su progetto create utilizzando Project Operations.

L'importo di un'offerta è il totale delle righe basate su prodotto e delle righe basate su progetto.

> [!NOTE]
> Offerte e righe di offerta non sono necessarie in Project Operations. Puoi avviare il processo di progetto con un contratto di progetto (progetto venduto). Tuttavia, un'opportunità è sempre necessaria, indipendentemente se si inizia con un'offerta o un con contratto di progetto.

## <a name="project-based-quote-lines"></a>Righe dell'offerta basate sul progetto

Una riga di offerta basata su progetto in Project Operations ha i seguenti metodi di fatturazione:

- Tempistica e materiali
- Prezzo fisso

### <a name="time-and-material"></a>Tempistica e materiali

Il metodo di fatturazione Tempistica e materiali è basato sul consumo. Quando selezioni questo metodo di fatturazione, il cliente viene fatturato quando il progetto comporta dei costi. Le fatture vengono create a una frequenza periodica basata sulla data. Durante il processo di vendita, il valore di un componente di tempistica e materiali dell'offerta fornisce solo una stima del costo finale per il cliente. Il fornitore non si impegna a completare il progetto esattamente per il valore esatto nell'offerta. I componenti di tempistica e materiali aumentano il rischio del cliente. È quindi possibile che i clienti vogliano negoziare ulteriori clausole di non superamento dei costi per ridurre al minimo i rischi. Project Operations non supporta la definizione di clausole di non superamento dei costi.

### <a name="fixed-price"></a>Prezzo fisso

Nel metodo di fatturazione Prezzo fisso, un fornitore si impegna a consegnare il progetto a un costo fisso al cliente. Al cliente viene fatturato il valore della riga di offerta a prezzo fisso indicato nell'offerta, indipendentemente dai costi incorsi dal fornitore per consegnare quella riga di offerta. Il valore della riga di offerta a prezzo fisso viene fatturato in uno dei modi seguenti: 

- Come importo forfettario all'inizio o alla fine del progetto, oppure in corrispondenza di una fase fondamentale del progetto. 
- Come pagamenti rateali uguali secondo una frequenza basata sulla data del valore fisso indicato nella riga di offerta. Questi pagamenti rateali sono noti come passaggi fondamentali periodici.
- Come pagamenti rateali con un valore monetario allineato all'avanzamento del lavoro o a specifici passaggi fondamentali raggiunti nel progetto. In tal caso, il valore di ogni pagamento rateale può differire, ma la somma totale deve corrispondere al valore fisso nella riga di offerta.

Project Operations supporta tutti e tre i tipi di pianificazioni di fatturazione per le righe di offerta a prezzo fisso.

## <a name="transaction-classification"></a>Classificazione delle transazioni

Le organizzazioni di servizi professionali in genere generano preventivi e fatture secondo la classificazione dei costi. I costi sono rappresentati dalle seguenti classificazioni di transazioni:

- **Tempo** : questa classificazione rappresenta il costo del tempo della manodopera o delle risorse umane in un progetto.
- **Spesa** : questa classificazione rappresenta tutti gli altri tipi di spese in un progetto. Poiché le spese possono essere classificate in modo ampio, la maggior parte delle organizzazioni crea sottocategorie, ad esempio Viaggi, Autonoleggio, Hotel o Forniture per ufficio.
- **Commissioni** : questa classificazione rappresenta spese generali varie, penalità e altre voci imputati al cliente. 
- **Imposte** : questa classificazione rappresenta gli importi delle imposte che gli utenti aggiungono quando immettono le spese.
- **Transazione materiale** : questa classificazione rappresenta valori effettivi delle righe di prodotto in una fattura di progetto confermata.
- **Passaggio fondamentale** : questa classificazione viene utilizzata dalla logica di fatturazione a prezzo fisso.

Una o più di queste classificazioni di transazioni possono essere associate a ogni riga di offerta. Dopo l'acquisizione di un'offerta, il mapping tra la classificazione delle transazioni e la riga di offerta viene trasferito alla voce di contratto.
  
Ad esempio, un'offerta può contenere le seguenti due righe di offerta: 

- Lavoro di consulenza che utilizza un metodo di fatturazione Tempistica e materiali in cui le classificazioni di tempo e commissioni sono applicabili. Ad esempio, tutte le transazioni tempo e commissioni per il progetto di esempio **Implementazione di Dynamics AX** vengono fatturate al cliente in base a tempistica e materiali utilizzati. 
- Spese di viaggio correlate che utilizzano un metodo di fatturazione Prezzo fisso. Ad esempio, tutte le spese di viaggio per il progetto di esempio **Implementazione di Dynamics AX** vengono fatturate a un valore monetario fisso.

> [!NOTE]
> La combinazione di progetto e classificazioni **Tempo** , **Spesa** e **Commissione** associate a una riga di offerta o voce di contratto deve essere univoca. Se si associa la stessa combinazione di progetto e classificazione di transazioni a più voci di contratto o righe di offerta, Project Operations non funzionerà correttamente.

## <a name="billing-types"></a>Tipo di fatturazione

Il campo **Tipo di fatturazione** definisce il concetto di esigibilità. Si tratta di un set di opzioni con i seguenti possibili valori:

- **Addebitabile** : il costo accumulato per questo ruolo/categoria è un costo diretto che determina l'esecuzione del progetto e il cliente pagherà per tale lavoro. Il pagamento può essere gestito come accordo Tempistica e materiali o Prezzo fisso. Tuttavia, il dipendente impiegato per questo tempo riceverà il credito corrispondente per il suo utilizzo fatturabile.
- **Non addebitabile** : il costo accumulato per questo ruolo/categoria viene considerato un costo diretto che determina l'esecuzione del progetto, anche se il cliente non riconosce questo fatto e non pagherà per tale lavoro. Il dipendente impiegato per questo tempo non riceverà alcun credito per l'utilizzo fatturabile.
- **Gratuito** : il costo accumulato per questo ruolo/categoria è considerato un costo diretto che determina l'esecuzione del progetto e il cliente riconosce tale fatto. Il dipendente che spende questo tempo riceverà un credito per l'utilizzo fatturabile. Tuttavia, questo costo non viene addebitato al cliente.
- **Non disponibile** : questa opzione consente di tenere traccia dei costi sostenuti per i progetti interni che non richiedono la tracciabilità dei ricavi.

## <a name="invoice-schedule"></a>Pianificazione di fatturazione

Una pianificazione di fatturazione è un insieme di date alle quali viene eseguita la fatturazione di un progetto. Puoi eventualmente creare una pianificazione di fatturazione per una riga di offerta. Ogni riga di offerta può avere una propria pianificazione di fatturazione. Per creare una pianificazione di fatturazione, devi fornire i seguenti valori di attributo:

- Una data di inizio fatturazione 
- Una data di consegna che rappresenta la data di fine fatturazione del progetto
- Una frequenza di fatturazione

Questi tre valori di attributo vengono utilizzati per generare un set di date provvisorie sulle quali basare la fatturazione.

## <a name="invoice-frequency"></a>Frequenza di fatturazione

Frequenza di fatturazione è un'entità in cui sono archiviati i valori di attributo che consentono di esprimere la frequenza di creazione delle fatture. I seguenti attributi esprimono o definiscono l'entità Frequenza di fatturazione:

- **Periodo** : sono supportati periodi mensili, bisettimanali e settimanali. 
- **Esecuzioni per periodo** : per i periodi settimanali e bisettimanali, puoi definire una sola esecuzione per periodo. Per i periodi mensili, puoi definire tra una e quattro esecuzioni per periodo. 
- **Giorni di esecuzione** : i giorni in cui la fatturazione deve essere eseguita. Puoi configurare questo attributo in due modi:
  - **Giorni feriali** : ad esempio, puoi scegliere di eseguire la fatturazione ogni lunedì o ogni secondo lunedì del mese. È possibile che i clienti che devono eseguire la fatturazione in un giorno lavorativo preferiscano questo tipo di configurazione. 
  - **Giorni di calendario** : ad esempio, puoi scegliere di eseguire la fatturazione il settimo giorno e il ventunesimo giorno di ogni mese. Alcune organizzazioni possono preferire questo tipo di configurazione in quanto garantisce l'esecuzione della fatturazione a date fisse ogni mese.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Pianificazione della fatturazione per una riga di offerta a prezzo fisso

Per una riga di offerta a prezzo fisso, puoi utilizzare la griglia **Pianificazione fatturazione** per creare passaggi fondamentali di fatturazione che eguagliano il valore della riga di offerta.

- Per creare passaggi fondamentali di fatturazione equamente divisi, seleziona la frequenza di fatturazione, immetti la data di inizio della fatturazione nella riga di offerta e seleziona **Data di completamento richiesta** per l'offerta nella sezione **Riepilogo** dell'intestazione dell'offerta. Quindi seleziona **Genera passaggi fondamentali periodici** per creare passaggi fondamentali suddivisi equamente in base alla frequenza di fatturazione selezionata. 
- Per creare un passaggio fondamentale di fatturazione con somma forfettaria, crea un passaggio fondamentale e quindi immetti il valore della riga di offerta come importo del passaggio fondamentale.
- Per creare passaggi fondamentali di fatturazione basati su specifiche attività del piano di progetto, crea un passaggio fondamentale e mappalo all'elemento di pianificazione del progetto nell'interfaccia utente dei passaggi fondamentali di fatturazione.
