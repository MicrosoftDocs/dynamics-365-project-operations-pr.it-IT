---
title: Gestire le proposte di fattura di progetto
description: Questo argomento fornisce dettagli sull'elaborazione delle fatture rivolte ai clienti con Project Operations per scenari di risorse/materiali non stoccati.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7e6d060c1cca08f86e2d04ca96c9315a17316d11
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001476"
---
# <a name="manage-project-invoice-proposals"></a>Gestire le proposte di fattura di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Le proposte di fatturazione del progetto possono essere elaborate dal reparto fatturazione quando sono soddisfatte le due condizioni seguenti:

  - Il Project manager conferma la fattura proforma in Microsoft Dataverse.
  - Tutte le transazioni di vendita non fatturate di tempo e materiali incluse nella fattura proforma vengono registrate utilizzando il giornare di registrazione Dynamics 365 **Integrazione Project Operations**.

Utilizza i passaggi seguenti per completare una proposta di fattura di progetto in Dynamics 365 Finance.

1. Rivedi le informazioni di fatturazione per le transazioni di tempo e materiali e registra il giornale di registrazione **Integrazione Project Operations**.
2. Rivedi le informazioni di fatturazione per i passaggi fondamentali di fatturazione a prezzo fisso.
3. Rivedi e formatta una proposta di fattura di progetto.
4. Registra e stampa le fatture di progetto.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Gestire le informazioni di fatturazione nel giornale di registrazione Integrazione Project Operations

I valori effettivi del progetto creati in Dataverse vengono esaminati e registrati in Finance dal contabile del progetto. Per ulteriori informazioni sull'utilizzo del giornale di registrazione integrazione, vedi [Giornale Integrazione di Project Operations](../project-accounting/project-operations-integration-journal.md).

I valori effettivi Costo e Vendite non fatturate vengono aggiunti al giornale di registrazione Integrazione come righe separate:

  - Il prezzo di costo unitario e l'importo in Valore effettivo costo viene ricavato per impostazione predefinita dalla transazione del costo effettivo del progetto in Dataverse.
  - Il prezzo di vendita unitario e l'importo di vendita nella transazione Vendite non fatturate per impostazione predefinita sono ricavati dalla transazione di vendite non fatturate effettiva del progetto in Dataverse.

### <a name="billing-sales-tax"></a>Fatturazione dell'IVA

Il calcolo dell'IVA per la fatturazione è determinato dalla combinazione di campi **Fatturazione della fascia IVA** e **Gruppo IVA articolo di fatturazione** su un record di vendite non fatturate nella riga del giornale **Integrazione Project Operations**. Il sistema imposta questi valori di campo per impostazione predefinita in base alle impostazioni nella scheda **Informazioni finanziarie** della pagina **Gestione progetti e parametri contabili**.

- Il **metodo del gruppo IVA** determina la logica predefinita della fascia IVA di fatturazione:
  
  - **Progetto**: L'impostazione predefinita è sempre la fascia IVA di fatturazione del progetto. Puoi rivedere o modificare la fascia IVA di fatturazione predefinita su un progetto selezionando **Mostra contabilità predefinita** nella pagina **Tutti i progetti**.
  - **Contratto di progetto**: L'impostazione predefinita è sempre la fascia IVA di fatturazione del contratto di progetto. Puoi rivedere o modificare la fascia IVA predefinita su un contratto di progetto selezionando **Mostra contabilità predefinita** nella pagina **Contratti di progetto**.
  - **Cliente**: L'impostazione predefinita è sempre la fascia IVA di fatturazione del cliente.
  - **Ricerca**: Cercherà in tutte le entità di cui sopra e selezionerà il primo valore disponibile. La ricerca inizia con l'entità **Progetto** quindi l'entità **Contratto di progetto** e infine l'entità **Cliente**.

- Il **metodo del gruppo IVA articolo di fatturazione** determina la logica predefinita del gruppo IVA articolo di fatturazione:
  
  - Per i tipi di transazione relative a tempo, spese e commissioni, la fascia IVA articolo di fatturazione sarà sempre predefinita dall'entità **Categoria di progetto**.
  - Per i tipi di transazione materiali, l'impostazione predefinita della fascia IVA articolo di fatturazione è basata sull'impostazione del **metodo del gruppo IVA articolo di fatturazione** in **Gestione progetti e parametri contabili**. Il numero articolo imposta per impostazione predefinita la fascia IVA articolo dall'entità **Prodotto rilasciato**. La categoria imposta per impostazione predefinita la fascia IVA articolo dall'entità **Categoria di progetto**.

### <a name="financial-dimensions"></a>Dimensioni finanziarie

Le dimensioni finanziarie per i record delle vendite non fatturate nel giornale **Integrazione Project Operations** predefinite vengono impostate dall'entità **Progetto**. Le dimensioni finanziarie possono essere riviste e regolate selezionando **Distribuisci importi**. Se è necessario modificare le dimensioni finanziarie del record delle vendite non fatturate dopo la registrazione del giornale di registrazione Integrazione ma prima che la fattura proforma venga confermata, vai a **Tutti i progetti** > **Gestisci** > **Transazioni registrate**, seleziona la transazione, quindi seleziona **Elabora** > **Regola contabilità**.

### <a name="exchange-rates"></a>Tassi di cambio

La valuta della transazione non fatturata in Dataverse viene utilizzata come valuta di transazione in Finance e convertita nella valuta contabile della società utilizzando i tassi di cambio definiti in Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Gestire gli attributi finanziari dei passaggi fondamentali di fatturazione 

Le righe di contratto di progetto che utilizzano il metodo di fatturazione a prezzo fisso vengono fatturate tramite i [passaggi fondamentali del prezzo fisso](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Il contabile del progetto può rivedere i passaggi fondamentali di fatturazione in Finance accedendo a **Contabilità e gestione dei progetti** > **Tutti i progetti** > **Gestisci** > **Transazioni in conto**.

### <a name="billing-sales-tax"></a>Fatturazione dell'IVA

I valori predefiniti di **Gruppo IVA** e **Gruppo IVA articolo** vengono ricavati dalle impostazioni quando viene creata un nuovo passaggio fondamentale di fatturazione in Dataverse. Il sistema imposta questi valori sui campi per impostazione predefinita in base alle impostazioni nella scheda **Commercio all'ingrosso, al dettaglio, riparazioni** della pagina **Gestione progetti e parametri contabili**.

- Il **metodo del gruppo IVA** determina la logica predefinita della **fascia IVA di fatturazione**:

    - **Progetto**: L'impostazione predefinita sarà sempre la fascia IVA di fatturazione del progetto. Puoi rivedere o modificare la fascia IVA predefinita su un progetto selezionando **Mostra contabilità predefinita** nella pagina **Tutti i progetti**.
    - **Contratto di progetto**: L'impostazione predefinita sarà sempre la fascia IVA di fatturazione del contratto di progetto. Puoi rivedere o modificare la fascia IVA predefinita su un contratto di progetto selezionando **Mostra contabilità predefinita** nella pagina **Contratti di progetto**.
    - **Cliente**: L'impostazione predefinita sarà sempre la fascia IVA di fatturazione del cliente.
    - **Ricerca**: Cercherà in tutte le entità di cui sopra nell'elenco e selezionerà il primo valore disponibile. La ricerca inizia con l'entità **Progetto** quindi l'entità **Contratto di progetto** e quindi l'entità **Cliente**.

- **Gruppo IVA articolo passaggio fondamentale prezzo fisso** viene utilizzato come valore predefinito nel campo **Gruppo IVA articolo** per il passaggio fondamentale di fatturazione. Il contabile può rivedere e modificare questo valore nella pagina **Transazioni in acconto**. Il sistema utilizza il valore della transazione in acconto durante la creazione di una riga proposta di fattura progetto.
 

### <a name="financial-dimensions"></a>Dimensioni finanziarie

Le dimensioni finanziarie predefinite per il passaggio fondamentale di fatturazione prezzo fisso vengono impostate nelle righe del contratto di progetto. Vai a **Contratti di progetto** > **Mostra contabilità predefinita** e nella scheda **Righe contratto** seleziona **riga di contratto di prezzo**, quindi imposta i valori di dimensione finanziaria che desideri utilizzare come predefiniti.

Il contabile di progetto può modificare le informazioni sull'IVA e le dimensioni finanziarie sui passaggi fondamentali della fattura fino a quando non viene creata la proposta di fattura di progetto.


## <a name="create-project-invoice-proposals"></a>Creare le proposte di fattura di progetto

Le proposte di fatturazione di progetto possono essere riviste nel modulo **Gestione progetto e contabilità** andando a **Fatture di progetto** > **Proposte di fatturazione di progetto**.

L'intestazione della proposta di fattura di progetto viene creata in Finance quando la fattura proforma viene confermata in Dataverse. Per facilitare la riconciliazione, il sistema imposta il numero di proposta di fattura di progetto in Finance sullo stesso numero dell'ID fattura proforma in Dataverse. Poiché le fatture proforma non sono necessariamente confermate nello stesso ordine in cui vengono create, la sequenza numerica della proposta di fattura di progetto in Finance deve consentire le modifiche ai numeri inferiori e superiori. Configura le sequenze numeriche utilizzando i seguenti passaggi:

1. In Finance, vai a **Amministrazione organizzazione** > **Sequenze numeriche** > **Sequenze numeriche**.
2. Nel filtro **Area** seleziona **Progetti**.
3. Nel filtro **Riferimento** seleziona **Proposta di fattura**.
4. Usa il campo **Società** per filtrare ogni persona giuridica con l'integrazione Project Operations Dataverse abilitata.
5. Apri **Dettagli sequenza numerica** e nella scheda **Generale** imposta:

    - **Consenti modifiche utente: a un numero inferiore** = **Sì**
    - **Consenti modifiche utente: a un numero superiore** = **Sì**

Le righe di proposta di fattura di progetto vengono aggiunte dal sistema utilizzando il processo periodico **Importa dalla tabella di staging** (**Gestione progetti e contabilità** > **Periodico** > **Integrazione Project Operations** > **Importa dalla tabella di staging**). Il processo può essere eseguito manualmente o utilizzando una pianificazione periodica. Il sistema non aggiungerà righe al documento di proposta di fattura finché tutte le righe non saranno pronte per essere fatturate. Le transazioni di tempo e materiali sono pronte per essere fatturate solo quando vengono registrate utilizzando il giornale **Integrazione Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Formattare e stampare le proposte di fattura

Il contabile di progetto può personalizzare la stampa di una fattura di progetto utilizzando la pagina **Formatta proposta di fattura** e le funzionalità di gestione della stampa.

### <a name="format-invoice-proposals"></a>Formattare le proposte di fattura

La pagina **Formatta proposte di fatturazione** consente di visualizzare le transazioni di raggruppamento personalizzate nella fattura di progetto del cliente.

1. Nella pagina **Proposta di fattura di progetto** seleziona **Stampa** > **Formatta proposta di fattura**.
2. Seleziona **Nuovo** per creare un nuovo raggruppamento per la stampa della fattura di progetto.
3. Nel campo **Dettaglio/Riepilogo** seleziona le opzioni per questo raggruppamento:

    - Seleziona **Dettagli** per stampare i dettagli della transazione della fattura del cliente.
    - Seleziona **Riepilogo** per stampare il riepilogo della transazione della fattura del cliente.

> [!NOTE]
> La selezione nel campo **Dettagli/Riepilogo** della pagina **Formatta proposta di fattura** sostituisce l'opzione selezionata nel campo **Formato fattura** della pagina **Proposte di fattura** per stampare una fattura dettagliata o una fattura riepilogativa.

- Seleziona le righe della transazione da includere in questa sezione nella scheda **Transazioni disponibili** e seleziona **Includi transazioni** per spostarle nella scheda **Transazioni selezionate**.
- Seleziona **Sposta su** e **Sposta giù** per modificare l'ordine delle sezioni.
- Seleziona **Anteprima di stampa** per visualizzare l'anteprima della fattura formattata.

### <a name="print-management"></a>Gestione stampa

La gestione della stampa utilizza diversi file di report per stampare, specificare le destinazioni e personalizzare il testo del piè di pagina per la fattura. La gestione della stampa può essere configurata a livello di modulo, tuttavia queste impostazioni possono essere sovrascritte per un cliente, un contratto o una proposta di fattura specifici. Per accedere a questa funzione nella pagina **Proposta di fattura di progetto** seleziona **Stampa** > **Gestione stampa**.

L'impostazione della gestione della stampa viene visualizzata come una visualizzazione ad albero, in cui ogni livello di nodo visualizza i documenti disponibili da regolare. Puoi assegnare stampe personalizzate a livello di documento di modulo, cliente, contratto o proposta di fattura. Per modificare la stampa del documento originale, espandi il nodo desiderato e seleziona **Elemento originale**. Nel campo **Formato report** seleziona il formato del report da utilizzare per la stampa. Puoi utilizzare formati di report personalizzati usando il [Framework di gestione dei documenti aziendali](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Registrare le proposte di fattura

Dopo che la fattura è stata rivista e modificata e le righe di proposta di fattura sono soddisfacenti, controlla i totali della fattura e l'IVA. Nel gruppo **Dettagli** seleziona **Totali** e poi seleziona **Registra** per registrare la fattura.

Per visualizzare la fattura prima della registrazione, deseleziona la casella di controllo **Registrazione**. **Proforma** verrà stampato sulla fattura per indicare che si tratta di una fattura di esempio. Per stampare la fattura, seleziona la casella di controllo **Stampa fattura**.

In aggiunta alla pagina **Proposta di fattura**, le proposte di fatturazione possono essere registrate anche eseguendo il processo periodico **Registra proposte di fatturazione**. Per trovare questo processo, vai a **Gestione progetti e contabilità** > **Periodico** > **Fatture di progetto** > **Registra proposte di fatturazione**.

Questa pagina mostra tutte le proposte di fatturazione pronte per la registrazione. Puoi pianificare la registrazione delle proposte di fatturazione selezionando **Batch**. Imposta **Parametro di elaborazione batch** su **Sì** e imposta la ricorrenza dell'elaborazione batch selezionando **Ricorrenza**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
