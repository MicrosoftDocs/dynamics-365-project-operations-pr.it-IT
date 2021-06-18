---
title: Valori effettivi
description: Questo argomento fornisce informazioni su come utilizzare i valori effettivi in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996616"
---
# <a name="actuals"></a>Valori effettivi 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I valori effettivi rappresentano l'avanzamento finanziario e programmato rivisto e approvato di un progetto. Vengono creati come risultato dell'approvazione di voci di tempo, spese, utilizzo di materiale, scritture contabili e fatture.

## <a name="journal-lines-and-time-submission"></a>Invio righe giornale di registrazione e tempo

Per ulteriori informazioni sull'inserimento ore, vedi [Panoramica dell'inserimento ore](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tempistica e materiali

Quando un inserimento ore inviato è collegato a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.

### <a name="fixed-price"></a>Prezzo fisso

Quando un inserimento ore inviato è collegato a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.

### <a name="default-pricing"></a>Prezzi predefiniti

La logica di creazione dei prezzi predefiniti risiede nella riga giornale di registrazione. I valori di campo di un inserimento ore vengono copiati nella riga giornale di registrazione. Questi valori includono la data della transazione, la voce di contratto a cui il progetto è mappato e la valuta nel listino prezzi appropriato.

I campi che determinano i prezzi predefiniti, ad esempio **Ruolo** e **Unità gestione risorse**, sono utilizzati per determinare il prezzo appropriato nella riga giornale di registrazione. Puoi aggiungere un campo personalizzato all'inserimento ore. Se il valore del campo deve essere propagato ai valori effettivi, crea il campo nelle tabelle **Valori effettivi** e **Riga giornale di registrazione**. Utilizza il codice personalizzato per propagare il valore del campo selezionato da Inserimento ore a Valori effettivi attraverso la riga giornale di registrazione utilizzando le origini delle transazioni. Per ulteriori informazioni sulle origini e le connessioni delle transazioni, vedi [Collegamento dei valori effettivi ai record originali](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Invio righe giornale di registrazione e spesa di base

Per ulteriori informazioni sull'inserimento spese, vedi [Panoramica della spesa](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tempistica e materiali

Quando una spesa di base inviata è collegata a un progetto mappato a una riga di contratto tempistica e materiali, il sistema crea due righe di giornale di registrazione, una per i costi e una per le vendite non fatturate.

### <a name="fixed-price"></a>Prezzo fisso

Quando una voce di spesa di base inviata viene collegata a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.

### <a name="default-pricing"></a>Prezzi predefiniti

La logica per l'immissione dei prezzi predefiniti per le spese si basa sulla categoria di spesa. La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato. I campi che determinano i prezzi predefiniti, ad esempio **Categoria di transazione** e **Unità**, sono utilizzati per determinare il prezzo appropriato nella riga giornale di registrazione. Tuttavia, ciò funziona solo quando il metodo di determinazione dei prezzi nel listino prezzi è **Prezzo unitario**. Se il metodo di determinazione dei prezzi è **Al costo** o **Ricarico sul costo**, il prezzo immesso alla creazione della voce di spesa viene utilizzato per il costo e il prezzo nella riga giornale di registrazione vendite viene calcolato in base al metodo di determinazione dei prezzi. 

È possibile aggiungere un campo personalizzato alla voce di spesa. Se il valore del campo deve essere propagato ai valori effettivi, crea il campo nelle tabelle **Valori effettivi** e **Riga giornale di registrazione**. Utilizza il codice personalizzato per propagare il valore del campo selezionato da Inserimento ore a Valori effettivi attraverso la riga giornale di registrazione utilizzando le origini delle transazioni. Per ulteriori informazioni sulle origini e le connessioni delle transazioni, vedi [Collegamento dei valori effettivi ai record originali](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Righe giornale di registrazione e invio del registro dell'utilizzo di materiale

Per ulteriori informazioni sulla voce di spesa, vedi [Registro dell'utilizzo di materiale](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Tempistica e materiali

Quando una voce del registro dell'utilizzo di materiale inviata è collegata a un progetto mappato a una voce di contratto di tempo e materiali, il sistema crea due righe giornale di registrazione, una per i costi e una per le vendite non fatturate.

### <a name="fixed-price"></a>Prezzo fisso

Quando una voce del registro dell'utilizzo di materiale viene collegata a un progetto mappato a una voce di contratto a prezzo fisso, il sistema crea una riga giornale di registrazione per i costi.

### <a name="default-pricing"></a>Prezzi predefiniti

La logica per l'immissione dei prezzi predefiniti per il materiale si basa sulla combinazione di prodotto e unità. La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato. I campi che determinano i prezzi predefiniti, ad esempio **ID prodotto** e **Unità**, sono utilizzati per determinare il prezzo appropriato nella riga giornale di registrazione. Tuttavia, ciò funziona solo per i prodotti del catalogo. Per i prodotti fuori catalogo, il prezzo immesso quando viene creata la voce del registro dell'utilizzo di materiale viene utilizzata per il prezzo di costo e di vendita nelle righe giornale di registrazione. 

È possibile aggiungere un campo personalizzato alla voce **Registro dell'utilizzo di materiale**. Se il valore del campo deve essere propagato ai valori effettivi, crea il campo nelle tabelle **Valori effettivi** e **Riga giornale di registrazione**. Utilizza il codice personalizzato per propagare il valore del campo selezionato da Inserimento ore a Valori effettivi attraverso la riga giornale di registrazione utilizzando le origini delle transazioni. Per ulteriori informazioni sulle origini e le connessioni delle transazioni, vedi [Collegamento dei valori effettivi ai record originali](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Utilizza giornali di registrazione per registrare i costi

Puoi utilizzare i giornali di registrazione per registrare costi o ricavi nelle classi di materiali, imposte, tempo, spese o transazioni fiscali. I giornali di registrazione possono per gli scopi seguenti:

- Sposta i valori effettivi di transazioni da un altro sistema in Microsoft Dynamics 365 Project Operations.
- Registra i costi che si sono verificati in un altro sistema. Questi costi possono includere costi di approvvigionamento o subappalto.

> [!IMPORTANT]
> L'applicazione non convalida il tipo di riga del giornale di registrazione o il prezzo correlato immesso nella riga del giornale di registrazione. Pertanto, solo un utente che è pienamente consapevole dell'impatto contabile che i valori effettivi hanno sul progetto deve utilizzare i giornali di registrazione per creare i valori effettivi. A causa dell'impatto di questo tipo di giornale di registrazione, è consigliabile scegliere con attenzione chi ha accesso per creare i giornali di registrazione.

## <a name="record-actuals-based-on-project-events"></a>Registrare valori effettivi basati su eventi di progetto

Project Operations registra le transazioni finanziarie che si hanno durante un progetto. Queste transazioni vengono registrate come valori effettivi. Nella tabella seguente sono riportati i differenti tipi di valori effettivi creati, a seconda se il progetto è un progetto tempistica e materiali, prezzo fisso, interno o in fase di prevendita.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>La risorsa appartiene alla stessa unità organizzativa dell'unità contratto del progetto

<table>
<thead>
<tr>
<th rowspan="3">Event</th>
<th colspan="4">Progetto fatturabile o venduto</th>
<th rowspan="3">Progetto nella fase di prevendita</th>
<th rowspan="3">Progetto interno</th>
</tr>
<tr>
<th colspan="2">Tempistica e materiali</th>
<th colspan="2">Prezzo fisso</th>
</tr>
<tr>
<th>Valori effettivi</th>
<th>Valuta delle transazioni</th>
<th>Prezzo fisso</th>
<th>Valuta delle transazioni</th>
</tr>
</thead>
<tbody>
<tr>
<td>Viene creato un inserimento ore.</td>
<td colspan="6">Nessuna impegno nell'entità Valori effettivi</td>
</tr>
<tr>
<td>Viene inviato un inserimento ore.</td>
<td colspan="6">Nessuna impegno nell'entità Valori effettivi</td>
</tr>
<tr>
<td rowspan="2">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</td>
<td>Valore effettivo costo</td>
<td>Valuta unità contratto</td>
<td rowspan="2">Valore effettivo costo</td>
<td rowspan="2">Valuta unità contratto
<td rowspan="2">Valore effettivo costo</td>
<td rowspan="2">Valore effettivo costo</td>
</tr>
<tr>
<td>Valore effettivo vendite non fatturate - Addebitabile</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td rowspan="3">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</td>
<td>Valore effettivo costo</td>
<td>Valuta unità contratto</td>
<td rowspan="3">Valore effettivo costo</td>
<td rowspan="3">Valuta unità contratto</td>
<td rowspan="3">Valore effettivo costo</td>
<td rowspan="3">Valore effettivo costo</td>
</tr>
<tr>
<td>Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td>Valore effettivo vendite non fatturate - Non addebitabile per la differenza</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td rowspan="2">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</td>
<td>Storno vendite non fatturate</td>
<td>Valuta contratto di progetto</td>
<td rowspan="2">Vendite fatturate per passaggio fondamentale</td>
<td rowspan="2">Valuta contratto di progetto</td>
<td rowspan="2">Non applicabile</td>
<td rowspan="2">Non applicabile</td>
</tr>
<tr>
<td>Vendite fatturate</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td rowspan="3">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</td>
<td>Storno vendite non fatturate</td>
<td>Valuta contratto di progetto</td>
<td rowspan="3">Non applicabile</td>
<td rowspan="3">Non applicabile</td>
<td rowspan="3">Non applicabile</td>
<td rowspan="3">Non applicabile</td>
</tr>
<tr>
<td>Vendite fatturate - Addebitabile per la nuova quantità</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td>Vendite fatturate - Non addebitabile per la differenza</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td rowspan="2">Una fattura viene rettificata per aumentare la quantità addebitabile.</td>
<td>Vendite fatturate - Storno</td>
<td>Valuta contratto di progetto</td>
<td rowspan="5">
<ul>
<li>Storno vendite fatturate per passaggio fondamentale</li>
<li>Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></li>
</ul>
</td>
<td rowspan="5">Valuta contratto di progetto</td>
<td rowspan="5">Non applicabile</td>
<td rowspan="5">Non applicabile</td>
</tr>
<tr>
<td>Vendite fatturate</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td rowspan="3">Una fattura viene rettificata per diminuire la quantità addebitabile.</td>
<td>Vendite fatturate - Storno</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td>Vendite fatturate per la nuova quantità</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td>Vendite non fatturate - Addebitabile per la differenza</td>
<td>Valuta contratto di progetto</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>La risorsa appartiene a un'unità organizzativa che differisce dall'unità contratto del progetto

<table>
<thead>
<tr>
<th rowspan="3">Event</th>
<th colspan="4">Progetto fatturabile o venduto</th>
<th rowspan="3">Progetto nella fase di prevendita</th>
<th rowspan="3">Progetto interno</th>
</tr>
<tr>
<th colspan="2">Tempistica e materiali</th>
<th colspan="2">Prezzo fisso</th>
</tr>
<tr>
<th>Valori effettivi</th>
<th>Valuta delle transazioni</th>
<th>Prezzo fisso</th>
<th>Valuta delle transazioni</th>
</tr>
</thead>
<tbody>
<tr>
<td>Viene creato un inserimento ore.</td>
<td colspan="6">Nessuna impegno nell'entità Valori effettivi</td>
</tr>
<tr>
<td>Viene inviato un inserimento ore.</td>
<td colspan="6">Nessuna impegno nell'entità Valori effettivi</td>
</tr>
<tr>
<td rowspan="4">La tempistica viene approvata e non si ha nessun aumento o modifica delle ore fatturabili durante l'approvazione.</td>
<td>Valore effettivo costo</td>
<td>Valuta unità contratto</td>
<td rowspan="4">Valore effettivo costo</td>
<td rowspan="4">Valuta unità contratto</td>
<td rowspan="4">Valore effettivo costo</td>
<td rowspan="4">Valore effettivo costo</td>
</tr>
<tr>
<td>Valore effettivo vendite non fatturate - Addebitabile</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td>Costo unità gestione risorse</td>
<td>Valuta unitaria gestione risorse</td>
</tr>
<tr>
<td>Vendite interorganizzative</td>
<td>Valuta unità contratto</td>
</tr>
<tr>
<td rowspan="5">La tempistica viene approvata e si ha una diminuzione delle ore fatturabili durante l'approvazione.</td>
<td>Valore effettivo costo</td>
<td>Valuta unità contratto</td>
<td rowspan="5">Valore effettivo costo</td>
<td rowspan="5">Valuta unità contratto</td>
<td rowspan="5">Valore effettivo costo</td>
<td rowspan="5">Valore effettivo costo</td>
</tr>
<tr>
<td>Costo unità gestione risorse</td>
<td>Valuta unitaria gestione risorse</td>
</tr>
<tr>
<td>Vendite interorganizzative</td>
<td>Valuta unità contratto</td>
</tr>
<tr>
<td>Valore effettivo vendite non fatturate - Addebitabile per la nuova quantità</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td>Valore effettivo vendite non fatturate - Non addebitabile per la differenza</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td rowspan="2">Una fattura è confermata e non si ha nessun aumento o modifica delle ore fatturabili.</td>
<td>Storno vendite non fatturate</td>
<td>Valuta contratto di progetto</td>
<td rowspan="2">Vendite fatturate per passaggio fondamentale</td>
<td rowspan="2">Valuta contratto di progetto</td>
<td rowspan="2">Non applicabile</td>
<td rowspan="2">Non applicabile</td>
</tr>
<tr>
<td>Vendite fatturate</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td rowspan="3">Una fattura è confermata e si ha una diminuzione delle ore fatturabili.</td>
<td>Storno vendite non fatturate</td>
<td>Valuta contratto di progetto</td>
<td rowspan="3">Non applicabile</td>
<td rowspan="3">Non applicabile</td>
<td rowspan="3">Non applicabile</td>
<td rowspan="3">Non applicabile</td>
</tr>
<tr>
<td>Vendite fatturate - Addebitabile per la nuova quantità</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td>Vendite fatturate - Non addebitabile per la differenza</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td rowspan="2">Una fattura viene rettificata per aumentare la quantità addebitabile.</td>
<td>Vendite fatturate - Storno</td>
<td>Valuta contratto di progetto</td>
<td rowspan="5">
<ul>
<li>Storno vendite fatturate per passaggio fondamentale</li>
<li>Modifica dello stato del passaggio fondamentale da <strong>Fatturato</strong> a <strong>Pronto per fattura</strong></li>
</ul>
</td>
<td rowspan="5">Valuta contratto di progetto</td>
<td rowspan="5">Non applicabile</td>
<td rowspan="5">Non applicabile</td>
</tr>
<tr>
<td>Vendite fatturate</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td rowspan="3">Una fattura viene rettificata per diminuire la quantità addebitabile.</td>
<td>Vendite fatturate - Storno</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td>Vendite fatturate per la nuova quantità</td>
<td>Valuta contratto di progetto</td>
</tr>
<tr>
<td>Vendite non fatturate - Addebitabile per la differenza</td>
<td>Valuta contratto di progetto</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
