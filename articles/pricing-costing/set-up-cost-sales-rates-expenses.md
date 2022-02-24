---
title: Impostare tariffe di vendita e costo per le spese
description: Questo argomento fornisce informazioni su come configurare le tariffe di costo e vendita per le categorie di spesa e transazione.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 34e3c24ae1aa999954af9b347633820d265ac0c3
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877225"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Impostare tariffe di vendita e costo per le spese

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi impostare i prezzi di costo e di vendita per le categorie di transazioni in Dynamics 365 Project Operations. Poiché i prezzi di costo e di vendita sono progettati per le spese, anche ciascuna categoria di transazione che le include deve essere impostata come categoria di spesa. Questa configurazione garantisce la precisione nella funzionalità downstream. I prezzi di vendita e di costo per le categorie di transazione possono essere elencati solo in una valuta, che deve essere la valuta nell'intestazione del listino prezzi.

Per impostare le tariffe di vendita e costo per le categorie di transazione, completa i seguenti passaggi. 

1. Vai a **Vendite** > **Clienti** > **Listini prezzi**.
2. Per creare un nuovo listino prezzi, seleziona **Nuovo**. 
3. In **Prezzi categoria**, nel menu della griglia secondaria, seleziona **Nuovo prezzo di categoria**. 
4. Nella pagina **Creazione rapida** inserisci la categoria di transazione e l'unità per cui stai creando il nuovo prezzo.

La tabella seguente elenca i campi della scheda **Generale** e nella pagina **Creazione rapida** di una riga di prezzo di categoria che devi tenere a mente quando crei i prezzi di categoria in un listino prezzi di vendita o costo:

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| Categoria di transazione | Scheda **Generale** e pagine **Creazione rapida** | Seleziona la categoria di transazione per la quale stai creando un prezzo di vendita o di costo. | La categoria di transazione nella stima in entrata o nel valore effettivo per la spesa verrà confrontato con questa riga per impostare la tariffa di vendita o costo predefinita della categoria di transazione. |
| Pianificazione unità | Scheda **Generale** e pagine **Creazione rapida** | La pianificazione di unità predefinita proviene dalla pianificazione di unità della categoria di transazione. | Non vi è alcun impatto downstream da questo campo. |
| Unità | Scheda **Generale** e pagine **Creazione rapida** | Seleziona l'unità per la quale vengono impostate le tariffe. | L'unità sulla stima o sul valore effettivo in entrata viene confrontata con l'unità su questa riga per impostare la tariffa predefinita per la stima o il valore effettivo di spesa. |
| Metodo di determinazione dei prezzi | Scheda **Generale** e pagine **Creazione rapida** | I possibili valori del campo **Metodo di determinazione dei prezzi** sono **Prezzo unitario**, **Al costo** e **Ricarico sul costo**. | Durante l'impostazione del prezzo, se selezioni **Prezzo per unità** blocchi il campo **Percentuale** nella riga del prezzo di categoria. Se **Al costo** viene selezionato, i campi **Prezzo** e **Percentuale** sono bloccati nel listino prezzi di vendita. La selezione di **Ricarico sul costo** blocca il campo **Prezzo** del listino prezzi di vendita. Su una riga di valore effettivo in entrata per la spesa, il metodo di determinazione dei prezzi **Al costo** o **Ricarico sul costo** fa sì che alla riga di vendita non fatturata corrispondente venga assegnato un prezzo che è uguale al prezzo di costo effettivo o calcolato come ricarico sul prezzo. |
| Prezzo | Scheda **Generale** e pagine **Creazione rapida** | Imposta una tariffa unitario per la combinazione di categoria di transazione e unità. Ad esempio, la tariffa per il chilometraggio è 10 USD per miglio e 8 USD per chilometro. | La tariffa del chilometraggio sarà la tariffa predefinita sul costo o prezzo unitario della stima in entrata o della riga effettiva per una classe di transazione spesa.|
| Percentuale | Scheda **Generale** e pagine **Creazione rapida** | Imposta una percentuale sul costo per la combinazione di categoria di transazione e unità. Ad esempio, la tariffa di vendita del biglietto aereo deve essere maggiorata del 10% rispetto al costo del biglietto aereo sostenuto. | Questa percentuale di ricarico sul costo è applicabile solo sul listino prezzi di vendita quando il metodo di calcolo del prezzo selezionato è **Ricarico sul costo**. |
| Valuta | Scheda **Generale** e pagine **Creazione rapida** | Per impostazione predefinita, questo valore proviene dalla valuta nell'intestazione del listino prezzi. Per i prezzi della categoria di transazione, la valuta non può essere sovrascritta. | Questa valuta utilizza per impostazione predefinita la valuta del prezzo unitario della riga effettiva in entrata per la classe di transazione spesa per costo e vendita. |

## <a name="pricing-methods-for-expenses"></a>Metodi di determinazione dei prezzi per le spese

Quando imposti i prezzi di categoria rilevanti solo nel contesto del prezzo di spesa, puoi utilizzare uno dei tre metodi di determinazione dei prezzi seguenti:

- **Prezzo unitario**
- **Al costo**
- **Ricarico sul costo**

### <a name="price-per-unit"></a>Prezzo unitario
Quando questo metodo di determinazione dei prezzi viene selezionato su una riga di prezzo di categoria collegata a un listino prezzi di vendita, il prezzo è predefinito per la combinazione di categoria e unità sia nella stima che nel valore effettivo. La stima si riferisce alle righe di stima di progetto per le spese, al dettaglio della riga di offerta e al dettaglio della voce di contratto per le spese.

### <a name="at-cost"></a>Al costo
Quando questo metodo di determinazione dei prezzi viene selezionato sulla riga di prezzo di categoria collegata a un listino prezzi di vendita, il prezzo è predefinito per la combinazione di categoria e unità solo nel valore effettivo di spesa. Ad esempio, i valori effettivi delle vendite non fatturate per la classe di transazione di spesa. Il prezzo unitario viene impostato sulle vendite effettive non fatturate dal prezzo unitario sul costo effettivo per quella spesa. L'impostazione predefinita del prezzo in base al costo non viene eseguita sulle stime di progetto per le spese o sui dettagli della riga di offerta e della voce del contratto per le spese.

### <a name="markup-over-cost"></a>Ricarico sul costo
Quando questo metodo di determinazione dei prezzi viene selezionato sulla riga di prezzo di categoria collegata a un listino prezzi di vendita, il prezzo è predefinito per la combinazione di categoria e unità solo in un valore effettivo di spesa. Ad esempio, i valori effettivi delle vendite non fatturate per la classe di transazione di spesa. Questo prezzo unitario viene impostato sulle vendite non fatturate effettive su un valore calcolato dal prezzo unitario sul costo effettivo per quella spesa dopo l'applicazione della percentuale di ricarico definita. L'impostazione predefinita del prezzo in base al costo non viene eseguita nelle stime di progetto per le spese o sui dettagli della riga di offerta e della voce del contratto per le spese.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
