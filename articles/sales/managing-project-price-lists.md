---
title: Gestire i listini prezzi di progetto in un'offerta
description: In questo argomento vengono fornite informazioni sull'entità listino prezzi di progetto.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8cfabf98f1a38823c777b6e388fbbb65d02877e3cd433069dd3845c292f2b277
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003911"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Gestire i listini prezzi di progetto in un'offerta

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations estende l'entità Listino prezzi in Dynamics 365 Sales. 

## <a name="key-entities"></a>Entità chiave

Un listino prezzi include informazioni fornite da quattro entità diverse:

- **Listino prezzi**: in questa entità sono archiviate le informazioni relative a contesto, valuta, data di validità e unità di tempo per il tempo di determinazione dei prezzi. Il contesto indica se il listino prezzi include tassi di costo o di vendita. 
- **Valuta**: questa entità archivia la valuta dei prezzi nel listino prezzi. 
- **Data**: questa entità viene utilizzata quando il sistema tenta di immettere un prezzo predefinito in una transazione. Viene selezionato il listino prezzi con una validità di data che include la data della transazione. Se vengono trovati più listini prezzi validi per la data della transazione associata al relativo contratto, offerta o unità organizzativa, nessun prezzo viene impostato come predefinito. 
- **Tempo**: questa entità archivia l'unità di tempo in cui sono espressi i prezzi, ad esempio tariffa oraria o giornaliera. 

L'entità Listino prezzi include tre tabelle correlate che archiviano i prezzi:

  - **Prezzo ruolo**: questa tabella archivia un tasso per una combinazione di valori di ruolo e unità organizzativa e viene utilizzata per configurare i prezzi basati su ruolo per le risorse umane.
  - **Prezzo categoria di transazione**: questa tabella archivia i prezzi per categoria di transazione ed è utilizzata per configurare i prezzi delle categorie di spese.
  - **Voci di listino**: questa tabella archivia i prezzi dei prodotti in catalogo.
 
Il listino prezzi è un tariffario pubblicitario. Un tariffario pubblicitario è una combinazione dell'entità Listino prezzi e delle righe correlate nelle tabelle Prezzo ruolo, Prezzo categoria di transazione e Voci di listino.

## <a name="resource-roles"></a>Ruoli risorsa

Il termine *ruolo risorsa* fa riferimento a un insieme di competenze, qualifiche e certificazioni che una persona deve avere per eseguire uno specifico set di attività in un progetto.

Il tempo delle risorse umane viene stimato in base al ruolo di una risorsa in uno specifico progetto. Per il tempo delle risorse umane, i costi e la fatturazione sono basati sul ruolo risorsa. Il prezzo del tempo può essere in qualsiasi unità dell'unità di vendita **Tempo**.

L'unità di vendita **Tempo** viene creata quando si installa Project Operations. L'unità predefinita è **Ora**. Non puoi eliminare, rinominare, o modificare gli attributi dell'unità di vendita **Tempo** o dell'unità **Ora**. Puoi tuttavia aggiungere altre unità all''unità di vendita **Tempo**. Se cerchi di eliminare l'unità di vendita **Tempo** o l'unità **Ora**, è possibile che si verifichino errori nelle logica di business.
 
## <a name="transaction-categories-and-expense-categories"></a>Categorie di transazioni e di spese

Le spese di viaggio e altre spese dei consulenti per un progetto sono fatturate al cliente. La determinazione dei prezzi delle categorie di spese è completata mediante l'utilizzo di listini prezzi. Biglietti aerei, hotel e autonoleggio sono esempi di categorie di spese. Ogni riga di listino prezzi relativa alle spese specifica la determinazione dei prezzi per una specifica categoria di spese. I tre metodi seguenti vengono utilizzati per definire le categorie di spesa:

- **Al costo**: il costo della spesa viene fatturato al cliente e non viene applicato alcun ricarico.
- **Percentuale ricarico**: la percentuale sul costo effettivo viene fatturata al cliente. 
- **Prezzo unitario**: un prezzo di fatturazione viene impostato per ogni unità della categoria di spese. L'importo fatturato al cliente viene calcolato in base al numero di unità di spesa segnalato dal consulente. Per Indennità trasferta viene utilizzato il metodo di determinazione dei prezzi Prezzo unitario. Ad esempio, la categoria di spesa Indennità trasferta può essere configurata per 30 dollari USA (USD) al giorno o 2 USD per miglio. Quando un consulente segnala il chilometraggio per un progetto, l'importo da fatturare viene calcolato in base al numero di miglia indicato dal consulente.
 
## <a name="project-sales-pricing-and-overrides"></a>Determinazione dei prezzi di vendita di progetto e sostituzioni

Per le offerte e i contratti di progetto, un listino prezzi di progetto include un modello di sostituzione dei prezzi differente rispetto a un listino prezzi di prodotto. In una riga di offerta basata su catalogo prodotti, puoi sostituire il prezzo per ruoli e categorie direttamente nella riga di offerta in quanto ogni riga di offerta punta esattamente a un articolo del catalogo. Tuttavia, in una riga di offerta basata su progetto, non puoi sostituire il prezzo per ruoli e categorie direttamente nella riga di offerta. Utilizza il listino prezzi di progetto per supportare i due modelli di sostituzione distinti.

> [!NOTE]
> Ti consigliamo di avere un listino prezzi distinto per le risorse del progetto e gli articoli del catalogo, per via delle differenze di comportamento tra i due quando si sostituisce il metodo di determinazione dei prezzi.

Ognuna delle seguenti entità può avere uno o più listini prezzi di vendita associati per la determinazione dei prezzi di progetto:

- Cliente (account) 
- Opportunità 
- Offerta 
- Contratto di progetto

L'associazione di queste entità con un listino prezzi è indicata dai listini prezzi di progetto. Puoi associare uno o più listini prezzi alle entità di vendita Cliente, Opportunità, Offerta e Contratto di progetto.

Un listino prezzi di progetto predefinito non viene automaticamente inserito in un record del cliente. Tuttavia, puoi associare manualmente un listino prezzi di progetto al record del cliente. Devi comunque associare manualmente un listino prezzi di progetto solo quando hai un accordo di determinazione dei prezzi personalizzato con il cliente. 

Quando un listino prezzi di progetto è associato a un'entità di vendita, le informazioni seguenti vengono convalidate:

- Il listino prezzi ha un contesto **Vendite**. 
- La valuta del listino prezzi corrisponde alla valuta del cliente. 

In un contratto di progetto, il seguente ordine di precedenza per impostare automaticamente i listini prezzi di progetto correlati:

1. Offerta
2. Opportunità
3. Cliente 
4. Impostazioni globali 

Quando un listino prezzi di progetto viene immesso per impostazione predefinita, il sistema verifica che la valuta corrisponde alla valuta del cliente e che i listini prezzi predefiniti immessi abbiano un contesto **Vendite**.

Puoi associare più listini prezzi di progetto alle entità Cliente, Opportunità, Offerta e Contratto di progetto. Questa funzionalità supporta prezzi predefiniti specifici della data per un contratto di progetto di lunga durata, dove puoi necessitare molteplici listini prezzi per gli aggiornamenti dei prezzi che si hanno a causa dell'inflazione. Tuttavia, se i listini prezzi associati all'entità Cliente, Opportunità, Offerta o Contratto di progetto hanno date di validità sovrapposte, i prezzi predefiniti possono non essere corretti. Pertanto, devi assicurarti che i listini prezzi di progetto con date di validità che si sovrappongono non siano associati a tali entità.

### <a name="deal-specific-price-overrides"></a>Sostituzioni di prezzi specifici a transazioni

Puoi creare sostituzioni specifiche a transazioni per i prezzi selezionati nei listini prezzi di progetto che vengono immessi per impostazione predefinita in un'offerta o in un contratto di progetto.

Per impostazione predefinita, un contratto di progetto ottiene sempre una copia del listino prezzi di vendita master anziché un collegamento diretto allo stesso. Questo comportamento assicura che gli accordi sui prezzi stipulati con un cliente per una descrizione dei lavori non cambiano se il listino prezzi master cambia.

Tuttavia, in un'offerta, puoi utilizzare un listino prezzi master. In alternativa, puoi copiare un listino prezzi master e modificarlo per creare un listino prezzi personalizzato applicabile solo a quell'offerta. Per creare un nuovo listino prezzi specifico a un'offerta, nella pagina **Offerta**, seleziona **Crea determinazione dei prezzi personalizzata**. Puoi accedere al listino prezzi di progetto specifico della transazione solo dall'offerta. 

Quando crei un listino prezzi di progetto personalizzato, solo i componenti di progetto del listino prezzi vengono copiati. In altre parole un nuovo listino prezzi creato come copia del listino prezzi di progetto esistente viene associato all'offerta e questo nuovo listino prezzi include solo i prezzi per ruolo e i prezzi per categoria di transazione correlati.
  
## <a name="tracking-costs"></a>Tenere traccia dei costi

Project Operations tiene traccia dei costi relativi all'utilizzo del tempo delle risorse umane nei progetti. Tiene inoltre traccia dei costi relativi ad altre spese sostenute durante il progetto, come le spese di viaggio.

Come i tassi di fatturazione, anche i tassi di costo per le risorse umane sono configurati utilizzando i listini prezzi. Di seguito sono riportate le differenze principali nel comportamento del listino prezzi di costo e il listino prezzi di vendita:

- Il tasso di costo di una risorsa non può essere sostituito in un progetto, contratto o offerta specifico. Tuttavia, i tassi di fatturazione possono essere sostituiti ad ogni transazione se vengono apportate modifiche specifiche alla natura della transazione. 

- L'ordine seguente viene utilizzato per risolvere un listino prezzi di costo:

    1. Il listino prezzi di costo associato all'unità organizzativa.
    2. Il listino prezzi di costo associato ai parametri di Project Operations. Poiché i listini prezzi di costo in molte differenti valute possono essere associati ai parametri, viene completata una corrispondenza di valuta tra la valuta dell'unità organizzativa di contratto del progetto, del contratto o dell'offerta e la valuta del listino prezzi di costo.
    3. Per le spese, i metodi di determinazione dei prezzi Al costo e Ricarico sul costo non sono applicabili ai listini prezzi di costo. Anche se questi metodi di determinazione dei prezzi vengono utilizzati nelle righe dei listini prezzi di costo per configurare i costi delle categorie di transazioni, il sistema li ignora e non viene immesso alcun prezzo di costo predefinito.


[!INCLUDE[footer-include](../includes/footer-banner.md)]