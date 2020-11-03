---
title: Offerte e righe di offerta
description: In questo argomento vengono fornite informazioni su offerte e righe di offerta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
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
ms.openlocfilehash: ae48c691fd855e6f22d0642965fc0c1617793368
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078991"
---
# <a name="quotes-and-quote-lines"></a>Offerte e righe di offerta

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Dynamics 365 Project Service Automation, esistono due tipi di offerte: offerte di progetto e offerte di vendita. Questi due tipi differiscono nei modi seguenti:

- Un'offerta di vendita include una sola griglia per le voci. Un'offerta di progetto include due griglie per le voci: una per le righe di progetto e una per le righe di prodotto.
- Un'offerta di vendita supporta l'attivazione e le revisioni. Un'offerta di progetto non supporta questi processi.
- È possibile associare più ordini a un'offerta di vendita ma un solo contratto di progetto a un'offerta di progetto.
- È possibile acquisire un'offerta di vendita e mantenere aperta la relativa opportunità. Dopo l'acquisizione di un'offerta di progetto, la relativa opportunità viene chiusa.
- Un'offerta di vendita non include alcuni campi e i concetti inclusi in un'offerta di progetto hanno dei campi. Questi campi sono **Unità contratto** , **Gestione account** e **Nome contatto fatturazione**.  
- Le offerte di vendita e quelle di progetto sono inoltre identificate da un campo basato su set di opzioni denominato **Tipo**. Per un'offerta di vendita, il valore di questo campo è **Basato su articolo**. Per un'offerta di progetto, il valore di questo campo è **Basato su lavoro**.

In questo argomento vengono descritti i dettagli delle offerte di progetto.

Un'offerta di progetto in PSA può avere molteplici voci o righe di offerta. In effetti, un'offerta di progetto include due griglie per le voci. Una griglia è per le righe basate su progetto che consentono stime dettagliate. L'altra griglia è per le righe basate su prodotto che utilizzano un prezzo unitario e un approccio basato sulla quantità.

- **Basate su progetto** - L'importo (valore dell'offerta) viene determinato dopo la stima della quantità di lavoro necessario. Puoi stimare il lavoro ad alto livello oppure stimarlo direttamente come dettagli di riga sotto ogni riga di offerta. Infine, puoi valutare il lavoro in base a stime eseguite da zero, utilizzando un progetto e un piano di progetto. Le righe di offerta basate su progetto sono disponibili solo nelle offerte basate su progetto create utilizzando Project Service Automation. Questo tipo di riga di offerta è un modulo personalizzato delle righe di offerta fuori catalogo disponibili in Microsoft Dynamics 365 Sales.
- **Basate su prodotto** - L'importo (valore dell'offerta) viene determinato in base alla quantità di unità vendute e al prezzo di vendita unitario del prodotto. Il prodotto in una riga basata su prodotto può provenire da un catalogo prodotti in Sales, oppure può essere un prodotto che definisci. Questo tipo di riga di offerta è disponibile anche nelle offerte basate su progetto create utilizzando PSA.

L'importo di un'offerta è il totale delle righe basate su prodotto e delle righe basate su progetto.

> [!NOTE]
> Offerte e righe di offerta non sono necessarie in PSA. Puoi avviare il processo di progetto con un contratto di progetto (progetto venduto). Tuttavia, un'opportunità è sempre necessaria, indipendentemente se si inizia con un'offerta o un con contratto di progetto.

## <a name="project-based-quote-lines"></a>Righe di offerta basate su progetto

Una riga di offerta basata su progetto in PSA ha i seguenti metodi di fatturazione:

- Tempistica e materiali
- Prezzo fisso

### <a name="time-and-material"></a>Tempistica e materiali

Il metodo di fatturazione Tempistica e materiali è basato sul consumo. Quando selezioni questo metodo di fatturazione, il cliente viene fatturato quando il progetto comporta dei costi. Le fatture vengono create a una frequenza periodica basata sulla data. Durante il processo di vendita, il valore di un componente di tempistica e materiali dell'offerta fornisce solo una stima del costo finale per il cliente. Il fornitore non si impegna a completare il progetto esattamente per il valore esatto nell'offerta. I componenti di tempistica e materiali aumentano il rischio del cliente. È quindi possibile che i clienti vogliano negoziare ulteriori clausole di non superamento dei costi per ridurre al minimo i rischi. PSA non supporta la definizione di clausole di non superamento dei costi.

### <a name="fixed-price"></a>Prezzo fisso

Nel metodo di fatturazione Prezzo fisso, un fornitore si impegna a consegnare il progetto a un costo fisso al cliente. Al cliente viene fatturato il valore della riga di offerta a prezzo fisso indicato nell'offerta, indipendentemente dai costi incorsi dal fornitore per consegnare quella riga di offerta. Il valore della riga di offerta a prezzo fisso viene fatturato in uno dei modi seguenti: 

- Come importo forfettario all'inizio o alla fine del progetto, oppure in corrispondenza di una fase fondamentale del progetto. 
- Come pagamenti rateali uguali secondo una frequenza basata sulla data del valore fisso indicato nella riga di offerta. Questi pagamenti rateali sono noti come passaggi fondamentali periodici.
- Come pagamenti rateali con un valore monetario allineato all'avanzamento del lavoro o a specifici passaggi fondamentali raggiunti nel progetto. In tal caso, il valore di ogni pagamento rateale può differire, ma la somma totale deve corrispondere al valore fisso nella riga di offerta.

PSA supporta tutti e tre i tipi di pianificazioni di fatturazione per le righe di offerta a prezzo fisso.

## <a name="transaction-classification"></a>Classificazione delle transazioni

Le organizzazioni di servizi professionali in genere generano preventivi e fatture secondo la classificazione dei costi. In PSA, i costi sono rappresentati dalle seguenti classificazioni di transazioni:

- **Tempo** - Questa classificazione rappresenta il costo del tempo della manodopera o delle risorse umane in un progetto.
- **Spesa** - Questa classificazione rappresenta tutti gli altri tipi di spese in un progetto. Poiché le spese possono essere classificate in modo ampio, la maggior parte delle organizzazioni crea sottocategorie, ad esempio Viaggi, Autonoleggio, Hotel o Forniture per ufficio.
- **Commissioni** - Questa classificazione rappresenta spese generali varie, penalità e altre voci imputati al cliente. 
- **Imposte** - Questa classificazione rappresenta gli importi delle imposte che gli utenti aggiungono quando immettono le spese.
- **Transazione materiale** - Questa classificazione rappresenta valori effettivi delle righe di prodotto in una fattura di progetto confermata.
- **Passaggio fondamentale** - Questa classificazione viene utilizzata dalla logica di fatturazione a prezzo fisso in PSA.

Una o più di queste classificazioni di transazioni possono essere associate a ogni riga di offerta. Dopo l'acquisizione di un'offerta, il mapping tra la classificazione delle transazioni e la riga di offerta viene trasferito alla voce di contratto.
 
> ![Screenshot del mapping tra tipi di transazioni e righe di offerta e voci di contratto](media/basic-guide-5.png)
  
Ad esempio, un'offerta può contenere le seguenti due righe di offerta: 
- Lavoro di consulenza che utilizza un metodo di fatturazione Tempistica e materiali in cui le classificazioni di tempo e commissioni sono applicabili. Ad esempio, tutte le transazioni tempo e commissioni per il progetto di esempio **Implementazione di Dynamics AX** vengono fatturate al cliente in base a tempistica e materiali utilizzati. 
- Spese di viaggio correlate che utilizzano un metodo di fatturazione Prezzo fisso. Ad esempio, tutte le spese di viaggio per il progetto di esempio **Implementazione di Dynamics AX** vengono fatturate a un valore monetario fisso.

> [!NOTE]
> La combinazione di progetto e classificazioni **Tempo** , **Spesa** e **Commissione** associate a una riga di offerta o voce di contratto deve essere univoca. Se si associa la stessa combinazione di progetto e classificazione di transazioni a più voci di contratto o righe di offerta, PSA non funzionerà correttamente.

## <a name="billing-types"></a>Tipo di fatturazione

Il campo **Tipo di fatturazione** definisce il concetto di esigibilità in PSA. Si tratta di un set di opzioni con i seguenti possibili valori:

- **Addebitabile** - Il costo accumulato per questo ruolo/categoria è un costo diretto che determina l'esecuzione del progetto e il cliente pagherà per tale lavoro. Il pagamento può essere gestito come accordo Tempistica e materiali o Prezzo fisso. Tuttavia, il dipendente impiegato per questo tempo riceverà il credito corrispondente per il suo utilizzo fatturabile.
- **Non addebitabile** - Il costo accumulato per questo ruolo/categoria viene considerato un costo diretto che determina l'esecuzione del progetto, anche se il cliente non riconosce questo fatto e non pagherà per tale lavoro. Il dipendente impiegato per questo tempo non riceverà alcun credito per l'utilizzo fatturabile.
- **Gratuito** - Il costo accumulato per questo ruolo/categoria è considerato un costo diretto che determina l'esecuzione del progetto e il cliente riconosce tale fatto. Il dipendente che spende questo tempo riceverà un credito per l'utilizzo fatturabile. Tuttavia, questo costo non viene addebitato al cliente.
- **Non disponibile** - Questa opzione consente di tenere traccia dei costi sostenuti per i progetti interni che non richiedono la tracciabilità dei ricavi.

## <a name="invoice-schedule"></a>Pianificazione di fatturazione

Una pianificazione di fatturazione è un insieme di date alle quali viene eseguita la fatturazione di un progetto. Puoi eventualmente creare una pianificazione di fatturazione per una riga di offerta in PSA. Ogni riga di offerta può avere una propria pianificazione di fatturazione. Per creare una pianificazione di fatturazione, devi fornire i seguenti valori di attributo:

- Una data di inizio fatturazione 
- Una data di consegna che rappresenta la data di fine fatturazione del progetto
- Una frequenza di fatturazione

PSA utilizza questi tre valori di attributo per generare un set di date provvisorie sulle quali basare la fatturazione.

## <a name="invoice-frequency"></a>Frequenza di fatturazione

Frequenza di fatturazione è un'entità in cui sono archiviati i valori di attributo che consentono di esprimere la frequenza di creazione delle fatture. I seguenti attributi esprimono o definiscono l'entità Frequenza di fatturazione:

- **Periodo** - Sono supportati periodi mensili, bisettimanali e settimanali. 
- **Esecuzioni per periodo** - Per i periodi settimanali e bisettimanali, puoi definire una sola esecuzione per periodo. Per i periodi mensili, puoi definire tra una e quattro esecuzioni per periodo. 
- **Giorni di esecuzione** - I giorni in cui la fatturazione deve essere eseguita. Puoi configurare questo attributo in due modi:
  - **Giorni feriali** - Ad esempio, puoi scegliere di eseguire la fatturazione ogni lunedì o ogni secondo lunedì del mese. È possibile che i clienti che devono eseguire la fatturazione in un giorno lavorativo preferiscano questo tipo di configurazione. 
  - **Giorni di calendario** - Ad esempio, puoi scegliere di eseguire la fatturazione il settimo giorno e il ventunesimo giorno di ogni mese. Alcune organizzazioni possono preferire questo tipo di configurazione in quanto garantisce l'esecuzione della fatturazione a date fisse ogni mese.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Pianificazione della fatturazione per una riga di offerta a prezzo fisso

Per una riga di offerta a prezzo fisso, puoi utilizzare la griglia **Pianificazione fatturazione** per creare passaggi fondamentali di fatturazione che eguagliano il valore della riga di offerta.

- Per creare passaggi fondamentali di fatturazione equamente divisi, seleziona la frequenza di fatturazione, immetti la data di inizio della fatturazione nella riga di offerta e seleziona **Data di completamento richiesta** per l'offerta nella sezione **Riepilogo** dell'intestazione dell'offerta. Quindi seleziona **Genera passaggi fondamentali periodici** per creare passaggi fondamentali suddivisi equamente in base alla frequenza di fatturazione selezionata. 
- Per creare un passaggio fondamentale di fatturazione con somma forfettaria, crea un passaggio fondamentale e quindi immetti il valore della riga di offerta come importo del passaggio fondamentale.
- Per creare passaggi fondamentali di fatturazione basati su specifiche attività del piano di progetto, crea un passaggio fondamentale e mappalo all'elemento di pianificazione del progetto nell'interfaccia utente dei passaggi fondamentali di fatturazione.
