---
title: Prodotti
description: Questo argomento fornisce informazioni sul catalogo dei prodotti che puoi utilizzare per fornire informazioni ai clienti sui prodotti e sui prezzi offerti dalla tua organizzazione.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 5c57b2596e1d480ff59591618f073ceb8f70a289
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574113"
---
# <a name="products"></a>Prodotti

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I prodotti sono le spina dorsale dell'azienda. Il catalogo prodotti in Dynamics 365 Sales Professional è una raccolta di prodotti e informazioni sui prezzi. Aiuta i rappresentanti di vendita a incrementare le vendite creando rapidamente un catalogo prodotti.

## <a name="add-a-product"></a>Aggiungere un prodotto

1.  Assicurati di disporre del ruolo di sicurezza Amministratore di sistema o Responsabile Sales Professional in modo da poter aggiungere prodotti in Dynamics 365 Sales Professional.
2.  Nella mappa del sito, sotto **Configurazione**, seleziona **Prodotti**.
3.  Seleziona **Aggiungi prodotto** e inserisci le seguenti informazioni:

    -  **Nome**
    -  **ID prodotto**
    -  **Padre**: seleziona una famiglia di prodotti padre per il prodotto. Se si crea un prodotto figlio in una famiglia di prodotti, il nome della famiglia di prodotto padre viene popolato qui. Questa impostazione non può essere modificata dopo il salvataggio del record.
    -  **Valido da**/**Valido fino a**: definire il periodo di validità dell'aggregazione dei prodotti selezionando una data **Valido da** e **Valido fino a**.
    -  **Unità di vendita**: seleziona un'unità di vendita. Un'unità di vendita è una raccolta di diverse unità presso le quali un prodotto viene venduto e definisce come i singoli elementi sono raggruppati in quantità maggiori. Ad esempio, se si è scelto di aggiungere i semi come prodotto, è probabile che sia stata creata un'unità di vendita denominata "Semi" e che la relativa unità primaria sia stata definita come "pacchetto".
    -  **Unità predefinita**: seleziona l'unità più comune per la vendita del prodotto. Le unità sono le quantità o le misure in cui vengono vendute i prodotti. Ad esempio, se intendi aggiungere i semi come prodotto, puoi venderli in pacchetti, caselle o pallet. Ognuno di questi diventa un'unità del prodotto. Se i semi sono venduti principalmente in pacchetti, selezionare pacchetto come unità.
    -  **Listino prezzi predefinito**: nel caso di un nuovo prodotto, questo campo sarà di sola lettura. Prima di poter selezionare un listino prezzi predefinito, devi compilare tutti i campi obbligatori e quindi salvare il record. Sebbene il listino prezzi predefinito non sia obbligatorio, dopo aver salvato il record del prodotto è consigliabile impostare un listino prezzi predefinito per ogni prodotto. In questo modo, se il record di un cliente non contiene un listino prezzi, Vendite potrà utilizzare il listino prezzi predefinito per generare offerte, ordini e fatture.
    -  **Decimali supportati**: immetti un numero intero compreso tra 0 e 5. Se il prodotto non può essere suddiviso in quantità frazionarie, immettere 0. La precisione del campo **Quantità** nel record del prodotto offerta, ordine o fattura è convalidata in base al valore di questo campo se al prodotto non è associato un listino prezzi.
    -  **Argomento**: associa il prodotto a un argomento. Gli argomenti consentono di suddividere i prodotti in categorie e filtrare i report.

4.  Seleziona **Salva**.
5.  Nella scheda **Dettagli aggiuntivi** nella sezione **Voci di listino**, seleziona l'icona **Altri comandi** e quindi seleziona **Aggiungi nuova entità Voce di listino**.
7.  Nella scheda **Dettagli aggiuntivi** nella sezione **Relazione prodotti**, seleziona l'icona **Altri comandi** e quindi seleziona **Aggiungi nuova relazione prodotti**.
8.  Nel modulo **Nuova relazione prodotti** immetti i seguenti dettagli e sulla barra dei comandi seleziona **Salva e chiudi**:

    -   **Prodotto correlato**: seleziona un prodotto che vuoi aggiungere come prodotto correlato al record di prodotto esistente al quale stai lavorando.
    -   **Tipo di relazione vendite**: seleziona se vuoi aggiungere il prodotto come una up-sell, cross-sell, accessorio o prodotto sostitutivo.
    -   **Direzione**: seleziona se la relazione tra i prodotti sarà unidirezionale o bidirezionale. Quando si seleziona Unidirezionale, il prodotto selezionato in **Prodotto correlato** verrà visualizzato come consiglio per il prodotto esistente, ma non viceversa.

9.  Nel modulo Prodotto, seleziona **Salva**.

## <a name="import-products"></a>Importare prodotti

Puoi importare modelli per integrare dati di prodotto in blocco in Dynamics 365 Sales.

## <a name="revise-a-product"></a>Aggiornare un prodotto

Mantieni l'inventario prodotto aggiornato aggiornando rapidamente le proprietà dei prodotti in base alle esigenze e pubblicando nuovamente le informazioni in modo che gli agenti di vendita possano visualizzare le ultime modifiche all'inventario.

1.  Assicurarsi di disporre di uno dei seguenti ruoli di sicurezza o di autorizzazioni equivalenti: Amministratore di sistema, Addetto personalizzazione sistema, Direttore commerciale, Vicepresidente Vendite, Vicepresidente Marketing o Responsabile aziendale.
2.  Nella mappa del sito, selezionare **Prodotti**.
3.  Apri un prodotto che vuoi modificare e, sulla barra dei comandi, seleziona **Aggiorna**.
4.  Nella finestra di dialogo **Conferma revisione** selezionare **Conferma**. In questo lo stato del prodotto viene modificano in **In aggiornamento**.
5.  Una volta effettuate le modifiche, nella barra dei comandi, seleziona **Pubblica**.

    > [!TIP]
    > Per ripristinare le modifiche e continuare con l'ultima versione attiva del prodotto, seleziona **Ripristina**. In questo modo lo stato del prodotto viene modificato in **Attivo**.

## <a name="clone-a-product"></a>Clonare un prodotto 

Durante la creazione di un nuovo prodotto, puoi risparmiare tempo duplicando l'elemento esistente. Viene creata una copia del record di origine con tutti i dettagli ad eccezione del nome e dell'ID.

1.  Assicurarsi di disporre di uno dei seguenti ruoli di sicurezza o di autorizzazioni equivalenti: Amministratore di sistema, Addetto personalizzazione sistema, Direttore commerciale, Vicepresidente Vendite, Vicepresidente Marketing o Responsabile aziendale.
2.  Nella mappa del sito, selezionare **Prodotti**.
3.  Seleziona un record di prodotto da clonare e, sulla barra dei comandi, seleziona **Clona**. Viene visualizzata una finestra di dialogo di conferma.
4.  Seleziona **Conferma**.

Il nuovo record di prodotto viene visualizzato con gli stessi dettagli di quello di origine ad eccezione del nome e dell'ID.

## <a name="retire-a-product"></a>Ritirare un prodotto 

Se l'organizzazione non vende più un prodotto, è necessario ritirarlo in modo che non sia più disponibile agli agenti di vendita.

1.  Assicurati di disporre del ruolo di sicurezza Amministratore di sistema o Responsabile Sales Professional o di autorizzazioni equivalenti.
2.  Nella mappa del sito, selezionare **Prodotti**.
3.  Apri un prodotto che vuoi ripristinare e, sulla barra dei comandi, seleziona **Ritira**.
4.  Nella finestra di dialogo **Conferma ritiro** selezionare **Conferma**.


## <a name="delete-a-product"></a>Eliminare un prodotto

Per interrompere la vendita di un prodotto, eliminarlo.

> [!IMPORTANT]
> Non è possibile ripristinare un record eliminato.

1.  Assicurati di disporre del ruolo di sicurezza Amministratore di sistema o Responsabile Sales Professional o di autorizzazioni equivalenti.
2.  Nella mappa del sito, selezionare **Prodotti**.
3.  Seleziona un record di prodotto da eliminare e, sulla barra dei comandi, seleziona **Elimina**.
4.  Nella finestra di dialogo **Conferma eliminazione** seleziona **Continua**.
 
 ## <a name="quantity-factors-for-products"></a>Fattori di quantità per prodotti

I fattori di quantità supportano la vendita di prodotti basati su sottoscrizione. Per i prodotti basati su sottoscrizione, la quantità nella riga di offerta o nella voce di contratto di progetto è espressa come numero di mesi utente.

In genere, il prezzo del software con sottoscrizione è archiviato nel catalogo come prezzo per utente al mese. Puoi tuttavia utilizzare altre descrizioni di tempo. Durante il processo di vendita, il prezzo nella riga di offerta è in genere il prezzo per utente al mese negoziato e scontato ottenuto dall'agente di vendita IT. Ogni transazione ha un numero di utenti differente e un differente numero di mesi di sottoscrizione. La quantità utilizzata per calcolare la quantità della riga di offerta è un prodotto del numero di utenti e del numero di mesi di sottoscrizione.

I fattori di quantità si basano sugli attributi di prodotto. Quando configuri specifiche proprietà per un prodotto, puoi contrassegnare un sottoinsieme di queste proprietà, o tutte le proprietà, come fattori di quantità.

Il sistema verifica che solo le proprietà numeriche o le proprietà di prodotto che hanno un tipo di dati numerici siano contrassegnate come fattori di quantità. Quando un prodotto per il quale sono configurati fattori di quantità viene aggiunto a una riga di offerta, il campo **Quantità** in tale riga diventa un campo di sola lettura. Dopo aver immesso valori per le proprietà del prodotto che sono fattori di quantità, viene calcolata la quantità della riga di offerta.

Ad esempio, se sono presenti le seguenti proprietà: 

- **N. di utenti**: il numero di utenti 
- **N. di mesi**: il numero di mesi di sottoscrizione
- **SKU prodotto** 

Le proprietà **N. di utenti** e **N. di mesi** possono essere contrassegnate come fattori di quantità modificando le proprietà della riga prodotto. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]