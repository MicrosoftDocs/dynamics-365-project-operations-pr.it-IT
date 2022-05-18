---
title: Panoramica dei valori effettivi
description: In questo argomento vengono fornite informazioni sui valori effettivi di progetto.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7ab2638d82eb5ba928d95ca6a524a1566f21e1ba
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587591"
---
# <a name="actuals-overview"></a>Panoramica dei valori effettivi

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I valori effettivi sono la quantità di lavoro completata in un progetto. È possibile risalire ai valori effettivi di progetto fino ai relativi documenti di origine. Questi documenti di origine includono inserimenti ore, voci di spesa e scritture contabili nonché fatture.

![Come risalire ai valori effettivi di progetto fino a documenti di origine.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Inviare un inserimento ore

In PSA, quando un inserimento ore viene inviato per un progetto mappato a una voce di contratto tempistica e materiali, vengono create due righe giornale di registrazione. Una riga è per i costi e l'altra per le vendite non fatturate. Quando un inserimento ore viene inviato per un progetto mappato a una voce di contratto a prezzo fisso, una riga giornale di registrazione viene creata solo per i costi. 

La logica di immissione dei prezzi predefiniti risiede nella riga giornale di registrazione. Tutti i valori di campo di un inserimento ore vengono copiati nella riga giornale di registrazione. Questi campi includono la data della transazione, la voce di contratto a cui il progetto è mappato e la valuta nel listino prezzi appropriato. 

I campi che determinano i prezzi predefiniti, ad esempio **Ruolo** e **Unità organizzativa**, causano l'immissione di un prezzo appropriato per impostazione predefinita nella riga giornale di registrazione. Se aggiungi un campo personalizzato nell'inserimento ore e il valore di campo deve essere propagato ai valori effettivi, crea il campo nell'entità Valori effettivi e utilizza i mapping dei campi per copiare il campo dall'inserimento ore nel valore effettivo.

## <a name="submitting-an-expense-entry"></a>Inviare una voce di spesa

In PSA, quando una voce di spesa viene inviata per un progetto mappato a una voce di contratto di tempo e materiale, vengono create due righe giornale di registrazione. Una riga è per i costi e l'altra per le vendite non fatturate. Quando una voce di spesa viene inviata per un progetto mappato a una voce di contratto a prezzo fisso, una riga giornale di registrazione viene creata solo per i costi.

La logica per l'immissione di prezzi predefiniti per le spese è basata sulla categoria di spesa selezionata nella pagina **Voce di spesa**. La data di transazione, la voce di contratto a cui il progetto è mappato e la valuta sono tutti utilizzati per determinare il listino prezzi appropriato. Tuttavia, per il prezzo stesso, l'importo immesso dall'utente viene impostato direttamente per impostazione predefinita nelle righe giornale di registrazione correlate per costi e vendite.

Nella versione corrente di PSA, la voce basata su categoria dei prezzi predefiniti unitari nelle voci di spesa non è disponibile.

## <a name="using-entry-journals-to-record-costs"></a>Utilizzare giornali di registrazione inserimenti per registrare i costi

In PSA, i giornali di registrazione inserimenti ti consentono di registrare costi o ricavi nelle classi di materiali, imposte, tempo, spese o transazioni fiscali. Un giornale di registrazione ha un'intestazione, righe e un'azione **Conferma**. Di seguito sono riportati alcuni scenari in cui puoi utilizzare un giornale di registrazione:

- Devi registrare vendite e costi effettivi di materiali in un progetto.
- Devi spostare gli effettivi di transazioni da un altro sistema a PSA.
- Devi registrare i costi incorsi in un altro sistema, ad esempio costi di approvvigionamento o conto lavoro.

> [!IMPORTANT]
> L'utilizzo dei giornali di registrazione inserimenti per creare i valori effettivi deve essere eseguito solo da un utente che sia pienamente consapevole dell'impatto contabile che i dati effettivi hanno sul progetto. Questo perché l'applicazione non convalida il tipo di riga di giornale di registrazione o il prezzo correlato immesso nella riga di giornale di registrazione. A causa dell'impatto di questo tipo di giornale, presta la dovuta attenzione a chi ha accesso per creare giornali di registrazione inserimenti.     


## <a name="recording-actuals-based-on-project-events"></a>Registrare effettivi basati su eventi di progetto

PSA registra le transazioni finanziarie che si hanno durante un progetto. Queste transazioni vengono registrate come **valori effettivi**. Nella tabella seguente sono riportati i differenti tipi di valori effettivi creati, a seconda se il progetto è un progetto tempistica e materiali, prezzo fisso, interno o in fase di prevendita.

**La risorsa appartiene alla stessa unità organizzativa dell'unità contratto del progetto**

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

**La risorsa appartiene a un'unità organizzativa che differisce dall'unità contratto del progetto**

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
