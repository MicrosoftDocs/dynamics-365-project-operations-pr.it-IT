---
title: Gestire unità complesse per le voci del contratto basate su prodotto - semplice
description: Questo argomento fornisce informazioni sul supporto della vendita di prodotti basati su abbonamento.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177381"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Gestire unità complesse per le voci del contratto basate su prodotto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Dynamics 365 Project Operations utilizza fattori di quantità per supportare la vendita di prodotti basati su sottoscrizione. Per i prodotti basati su sottoscrizione, la quantità nel contratto o nella voce di contratto di progetto è espressa come numero di mesi utente.

Il prezzo del software con sottoscrizione è archiviato nel catalogo come prezzo per utente al mese. Durante il processo di vendita, il prezzo nella voce di contratto è in genere il prezzo per utente al mese negoziato e scontato ottenuto dall'agente di vendita. Ogni transazione ha un numero di utenti differente e un differente numero di mesi di sottoscrizione. La quantità utilizzata per calcolare l'importo della voce di contratto è un prodotto del numero di utenti e del numero di mesi di sottoscrizione.

Per supportare questo tipo di vendita, Project Operations supporta il concetto di *fattori di quantità*. I fattori di quantità si basano sugli attributi di prodotto. Quando configuri specifiche proprietà per un prodotto, puoi contrassegnare un sottoinsieme di queste proprietà, o tutte le proprietà, come fattori di quantità.

Project Operations verifica che solo le proprietà numeriche o le proprietà di prodotto che hanno un tipo di dati numerici siano contrassegnate come fattori di quantità. Quando un prodotto con fattori di quantità configurati viene aggiunto a una voce di contratto, il campo **Quantità** diventa di sola lettura. Dopo aver immesso valori per le proprietà del prodotto che sono fattori di quantità, Project Operations calcola la quantità della voce di contratto.

Ad esempio, Dynamics 365 Sales potrebbe avere le proprietà seguenti:

- **N. di utenti**: il numero di utenti.
- **N. di mesi**: il numero di mesi di sottoscrizione.
- **SKU prodotto**: l'unità di stockkeeping (SKU) per il prodotto.

Le proprietà **N. di utenti** e **N. di mesi** possono essere contrassegnate come fattori di quantità modificando le proprietà della riga prodotto.

Per creare fattori di quantità dalle proprietà del prodotto, completa i seguenti passaggi.

1. In **Project Operations**, seleziona **Prodotti di vendita**.
2. Apri il prodotto per il quale vuoi impostare i fattori di quantità. Assicurati che il prodotto abbia le proprietà già impostate.
3. Nella pagina **Informazioni sul progetto** seleziona la scheda **Fattori di quantità**.
4. Nella griglia secondaria, seleziona **+ Nuovo calcolo campo**.
5. Immetti il nome del **fattore di quantità** e seleziona il valore della proprietà associato al calcolo del campo.
6. Salva e chiude il modulo.
7. Ripeti i passaggi 2-6 per tutte le proprietà che insieme comporranno la quantità per la voce di contratto basata su prodotto.

Con i fattori di quantità impostati, quando l'utente crea una voce di contratto per questo prodotto, la quantità della voce di contratto viene bloccata. La quantità viene quindi calcolata come prodotto dei valori di proprietà per quella voce di contratto.
