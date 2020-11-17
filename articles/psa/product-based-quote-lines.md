---
title: Righe di offerta basate su prodotto
description: In questo argomento vengono fornite informazioni sulle righe di offerta basate su prodotto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 9c3b2b35abe894e79d6f55a7ddd6e5c64d0f12f2
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123205"
---
# <a name="product-based-quote-lines"></a>Righe di offerta basate su prodotto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Puoi creare righe di offerta basate su prodotto in Dynamics 365 Project Service Automation. Le righe di offerta basate su prodotto possono essere righe "fuori catalogo" oppure articoli del catalogo prodotti.

## <a name="product-catalog"></a>Catalogo prodotti

I prodotti in un catalogo prodotti di Dynamics 365 hanno un'unità e un'unità di vendita predefinite. Se vari prodotti condividono lo stesso set di attributi, puoi creare una famiglia di prodotti che ha anch'essa tali attributi. Tutti i prodotti in una famiglia di prodotti ereditano lo stesso set di attributi.

Ad esempio, una società vende licenze di sottoscrizione per vari software. Tutti i software con sottoscrizione hanno i due seguenti attributi:

- Numero di utenti 
- Durata della sottoscrizione (in mesi)

Un ottimo modo di gestire questo tipo di catalogo è creare una famiglia di prodotti denominata **Software con sottoscrizione** che ha **Numero di utenti** e **Durata sottoscrizione** come attributi. Puoi quindi aggiungere singoli prodotti, come **Dynamics 365 Sales** o **Dynamics 365 Field Service** alla famiglia di prodotti **Software con sottoscrizione**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Aggiungere articoli del catalogo prodotti a un'offerta di progetto

Le pagine Offerta di progetto e Contratto di progetto presentano sezioni per due tipi di righe: righe basate su progetto e righe basate su prodotto. Per le righe basate su prodotto, Dynamics 365 viene utilizzato per aggiungere elementi da un catalogo prodotti a un'offerta. L'elenco a discesa nella riga di offerta o nella voce di contratto di progetto include tutti i prodotti e unità nel listino prezzi prodotto associato all'offerta o al contratto di progetto. Puoi anche aggiungere prodotti che non fanno parte del listino prezzi prodotto dell'offerta.

Inoltre, puoi selezionare prodotti in altri listini prezzi, oppure selezionare prodotti direttamente dal catalogo prodotti. Quando selezioni prodotti direttamente da un catalogo prodotti, il listino prezzi predefinito di quel prodotto viene utilizzato per ottenere il prezzo di vendita del prodotto. Se un listino prezzi predefinito non è impostato, il prezzo è 0 (zero).

Se una riga di offerta è basata su un catalogo prodotti, puoi sostituire il prezzo di vendita direttamente nella riga di offerta. Nota che una riga di offerta in Dynamics 365 include un campo **Prezzi**. Sono disponibili due valori:

- Sostituisci prezzo  
- Usa predefinito

Se imposti questo campo su **Sostituisci prezzo**, Dynamics 365 non imposta un prezzo predefinito. Devi immettere un prezzo per il prodotto nella riga di offerta. Se imposti questo campo su **Usa predefinito**, Dynamics 365 utilizza il prezzo di vendita predefinito e blocca il campo per impedirne la modifica.

Dopo l'installazione di PSA, i prezzi di vendita predefiniti vengono immessi nelle righe basate su prodotto di un'offerta. Il campo **Prezzi** viene quindi impostato su **Sostituisci prezzo** di modo che sia possibile modificare il prezzo predefinito nelle righe di offerta.

> ![Impostare Sostituisci prezzo](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Fattori di quantità per prodotti

PSA utilizza fattori di quantità per supportare la vendita di prodotti basati su sottoscrizione. Per i prodotti basati su sottoscrizione, la quantità nella riga di offerta o nella voce di contratto di progetto è espressa come numero di mesi utente.

In genere, il prezzo del software con sottoscrizione è archiviato nel catalogo come prezzo per utente al mese. Puoi tuttavia utilizzare altre descrizioni di tempo. Durante il processo di vendita, il prezzo nella riga di offerta è in genere il prezzo per utente al mese negoziato e scontato ottenuto dall'agente di vendita IT. Ogni transazione ha un numero di utenti differente e un differente numero di mesi di sottoscrizione. La quantità utilizzata per calcolare la quantità della riga di offerta è un prodotto del numero di utenti e del numero di mesi di sottoscrizione.

Per supportare questo tipo di vendita, PSA ha introdotto il concetto di fattori di quantità. I fattori di quantità si basano sugli attributi di prodotto in Dynamics 365. Quando configuri specifiche proprietà per un prodotto, PSA consente di contrassegnare un sottoinsieme di queste proprietà, o tutte le proprietà, come fattori di quantità.

PSA verifica che solo le proprietà numeriche o le proprietà di prodotto che hanno un tipo di dati numerici siano contrassegnate come fattori di quantità. Quando un prodotto per il quale sono configurati fattori di quantità viene aggiunto a una riga di offerta, il campo **Quantità** in tale riga diventa un campo di sola lettura. Dopo aver immesso valori per le proprietà del prodotto che sono fattori di quantità, PSA calcola la quantità della riga di offerta.

Ad esempio, Dynamics 365 potrebbe avere le proprietà seguenti: 

- **N. di utenti** - Il numero di utenti 
- **N. di mesi** - Il numero di mesi di sottoscrizione
- **SKU prodotto** 

Le proprietà **N. di utenti** e **N. di mesi** possono essere contrassegnate come fattori di quantità modificando le proprietà della riga prodotto. 

> ![Contrassegnare N. di utenti e N. di mesi come fattori di qualità](media/basic-guide-11.png)
 
