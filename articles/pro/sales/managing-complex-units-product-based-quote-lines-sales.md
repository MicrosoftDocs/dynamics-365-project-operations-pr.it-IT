---
title: Gestione di unità complesse come per utente, per mese per le righe di offerta basate su prodotto - semplice
description: Questo argomento fornisce informazioni sulla gestione di unità complesse per le righe di offerta basate su prodotto.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78bdb64d901cf68ce02c168987c2386e1416f6ee
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994771"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Gestione di unità complesse come per utente, per mese per le righe di offerta basate su prodotto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations utilizza fattori di quantità per supportare la vendita di prodotti basati su sottoscrizione. Per i prodotti basati su sottoscrizione, la quantità nella riga di offerta o nella voce di contratto di progetto è espressa come numero di mesi utente.

In genere, il prezzo del software con sottoscrizione è archiviato nel catalogo come prezzo per utente al mese. Durante il processo di vendita, il prezzo nella riga di offerta è in genere il prezzo per utente al mese negoziato e scontato ottenuto dall'agente di vendita IT. Ogni transazione ha un numero di utenti differente e un differente numero di mesi di sottoscrizione. La quantità utilizzata per calcolare la riga di offerta è un prodotto del numero di utenti e del numero di mesi di sottoscrizione.

Per supportare questo tipo di vendita, Project Operations ha introdotto il concetto di fattori di quantità. I fattori di quantità si basano sugli attributi di prodotto in Dynamics 365. Quando configuri specifiche proprietà per un prodotto, Project Operations consente di contrassegnare un sottoinsieme o tutte le proprietà come fattori di quantità.

Project Operations verifica che solo le proprietà numeriche o le proprietà di prodotto che hanno un tipo di dati numerici siano contrassegnate come fattori di quantità. Quando aggiungi un prodotto con fattori di quantità a una riga di offerta, il campo **Quantità** diventa di sola lettura. Dopo aver immesso valori per le proprietà del prodotto che sono fattori di quantità, Project Operations calcola la quantità della riga di offerta.

Ad esempio, Dynamics 365 Sales potrebbe avere le proprietà seguenti:

- **N. di utenti**: il numero di utenti
- **N. di mesi**: il numero di mesi di sottoscrizione
- **SKU prodotto**

Le proprietà **N. di utenti** e **N. di mesi** possono essere contrassegnate come fattori di quantità modificando le proprietà della riga prodotto.

Per creare fattori di quantità dalle proprietà del prodotto, segui questi passaggi:

1. Nel riquadro di spostamento a sinistra di Project Operations, vai a **Vendite** > **Prodotti**.
2. Apri il prodotto per il quale è necessario configurare i fattori di quantità. Assicurati che il prodotto abbia proprietà già configurate.
3. Nella pagina **Informazioni di progetto** per il prodotto, seleziona la scheda **Fattori di quantità**.
4. Nella griglia secondaria, seleziona **+ Nuovo calcolo campo**.
5. Immetti il nome del fattore di quantità e seleziona il valore della proprietà associato al calcolo del campo.
6. Salva e chiude il modulo. Ripeti questi passaggi per tutte le proprietà da utilizzare per calcolare la quantità per la riga dell'offerta basata sul prodotto.

Quando si crea una riga di offerta basata sul prodotto per un prodotto, la quantità della riga di offerta verrà bloccata. La quantità verrà calcolata come prodotto dei valori della proprietà immessi per quella riga dell'offerta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]