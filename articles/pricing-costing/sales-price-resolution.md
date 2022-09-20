---
title: Determinare i prezzi di vendita per stime e valori effettivi basati su progetto
description: Questo articolo fornisce informazioni su come vengono determinati i prezzi di vendita per le stime e i valori effettivi basati su progetto.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475374"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Determinare i prezzi di vendita per stime e valori effettivi basati su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Per determinare i prezzi di vendita su stime e valori effettivi in Microsoft Dynamics 365 Project Operations, il sistema utilizza prima la data e la valuta nella stima in entrata o nel valore effettivo per determinare il listino prezzi di vendita. Nel contesto attuale, in particolare, il sistema utilizza il campo **Data della transazione** per determinare quale listino prezzi è applicabile. Il valore di **Data della transazione** della stima in entrata o effettivo viene confrontato con i valori **Inizio validità (Indipendente da fuso orario)** e **Fine validità (Indipendente da fuso orario)** nel listino prezzi. Dopo che il listino prezzi di vendita è stato determinato, il sistema determina la tariffa di vendita o fatturazione.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>La determinazione delle tariffe di vendita sulle righe di stima e valori effettivi per il tempo

Il contesto di stima per **Ora** si riferisce a:

- Dettagli della riga di offerta per **Ora**.
- Dettagli della riga di offerta per **Ora**.
- Assegnazione delle risorse a un progetto.

Il contesto attuale per **Ora** si riferisce a:

- Scritture contabili di immissione e correzione per **Ora**.
- Le scritture contabili che vengono create quando viene inviato un inserimento ore.
- Dettagli della riga di fattura per **Ora**. 

Dopo che un listino prezzi per le vendite è stato determinato, il sistema completa i seguenti passaggi per impostare la tariffa di fatturazione predefinita.

1. Il sistema utilizza la combinazione di campi **Ruolo**, **Società resourcing** e **Unità gestione risorse** nella stima o nel contesto attuale per **Ora** contro le righe di prezzo del ruolo nel listino prezzi. Questa corrispondenza presuppone che vengano utilizzate dimensioni di determinazione del prezzo predefinite per le tariffe di fatturazione. Se hai configurato i prezzi in base ad altri campi al posto o in aggiunta a **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse**, verrà utilizzata tale combinazione per recuperare una riga di prezzo del ruolo corrispondente.
1. Se il sistema trova una riga di prezzo del ruolo con una tariffa di fatturazione per la combinazione di campi **Ruolo**, **Società resourcing** e **Unità gestione risorse**, questa è la tariffa di fatturazione predefinita.

> [!NOTE]
> Se configuri una diversa priorità per i campi **Ruolo**, **Società di gestione risorse** e **Unità gestione risorse** oppure se hai altre dimensioni con priorità più alta, questo comportamento precedente cambia di conseguenza. Il sistema recupera i record dei prezzi dei ruoli che hanno valori che corrispondono a ciascun valore della dimensione dei prezzi in ordine di priorità. Le righe con valori Null per quelle dimensioni vengono per ultime.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>La determinazione delle tariffe di vendita sulle righe di stima e valori effettivi per Spesa

Il contesto di stima per **Spesa** si riferisce a:

- Dettagli della riga di offerta per **Spesa**.
- Dettagli della voce di contatto per **Spesa**.
- Le righe di stima di spesa su un progetto.

Il contesto attuale per **Spesa** si riferisce a:

- Scritture contabili di immissione e correzione per **Spesa**.
- Le scritture contabili che vengono create quando viene inviata una spesa.
- Dettagli della riga della fattura per **Spesa**. 

Dopo che un listino prezzi per le vendite è stato determinato, il sistema completa i seguenti passaggi per impostare il prezzo unitario di vendita predefinito.

1. Il sistema utilizza la combinazione dei campi **Categoria** e **Unità** nella riga di stima per **Spesa** contro la categoria nella riga di prezzo nel listino prezzi.
1. Se il sistema trova una riga di prezzo di categoria con una tariffa di vendita per la combinazione di campi **Categoria** e **Unità**, questa riga è utilizzata come tariffa di vendita predefinita.
1. Se il sistema trova una riga di prezzo della categoria corrispondente, il metodo di determinazione del prezzo può essere utilizzato per impostare il prezzo di vendita predefinito. La tabella seguente mostra il comportamento predefinito per i prezzi di spesa in Project Operations.

    | Contesto | Metodo di determinazione dei prezzi | Prezzo predefinito |
    | --- | --- | --- |
    | Stima | Prezzo unitario | Basato sulla riga di prezzo della categoria. |
    |        | Al costo | 0.00 |
    |        | Ricarico sul costo | 0.00 |
    | Effettiva | Prezzo unitario | Basato sulla riga di prezzo della categoria. |
    |        | Al costo | In base al costo effettivo correlato. |
    |        | Ricarico sul costo | Viene applicato un ricarico come definito dalla riga del prezzo della categoria sulla tariffa di costo unitario del costo effettivo correlato. |

1. Se il sistema non può abbinare i valori **Categoria** e **Unità**, la tariffa di vendita è impostata su **0** (zero) per impostazione predefinita.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>La determinazione delle tariffe di vendita nelle righe effettive e di stima per Materiale

Il contesto di stima per **Materiale** si riferisce a:

- Dettagli della riga di offerta per **Materiale**.
- Dettagli della voce di contatto per **Materiale**.
- Righe di stima dei materiali in un progetto.

Il contesto attuale per **Materiale** si riferisce a:

- Scritture contabili di immissione e correzione per **Materiale**.
- Le scritture contabili che vengono create quando viene inviato un registro di uso dei materiali.
- Dettagli della riga della fattura per **Materiale**. 

Dopo che un listino prezzi per le vendite è stato determinato, il sistema completa i seguenti passaggi per impostare il prezzo unitario di vendita predefinito.

1. Il sistema utilizza la combinazione dei campi **Prodotto** e **Unità** nella riga di stima per la corrispondenza del **Materiale** con le righe di voci di listino prezzi nel listino prezzi.
1. Se il sistema trova una riga di voce di listino con una tariffa di vendita per la combinazione di campi **Prodotto** e **Unità** e se il metodo di determinazione dei prezzi è **Importo valuta**, viene utilizzato il prezzo di vendita specificato nella riga del listino prezzi. 
1. Se i valori dei campi **Prodotto** e **Unità** non corrispondono o se il metodo di determinazione dei prezzi è diverso da **Importo in valuta**, la tariffa di vendita è impostata su **0** (zero) per impostazione predefinita. Questo comportamento si verifica perché Project Operations supporta solo il metodo di determinazione del prezzo **Importo in valuta** per i materiali utilizzati in un progetto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
