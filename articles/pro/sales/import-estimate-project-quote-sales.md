---
title: Importare stime per un progetto in una riga di offerta basata su progetto - semplice
description: Questo argomento fornisce informazioni su come importare le stime da un progetto a una riga di offerta.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc1643751be25864e641ea297180fbefb1f2161
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003276"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importare stime per un progetto in una riga di offerta basata su progetto 

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma, Project Operations per scenari basati su risorse/materiali non stoccati_

Se un progetto viene creato durante la fase di prevendita, è possibile scegliere di importare la stima finanziaria dal progetto sulla riga di basata sul progetto.

1. Assicurati che la riga di offerta basata su progetto contenga le informazioni sul progetto nel campo **Progetto**.
2. Nella scheda **Dettagli riga di offerta**, seleziona **Importa da stima di progetto**.
3. Nella finestra di dialogo che si apre, seleziona una delle opzioni di riepilogo seguenti.

  - **Classe di transazione**
  - **Categoria**
  - **Ruolo** 
  - **Attività di progetto**

In base alla selezione, viene copiata la stima dal progetto per tutte le classi di transazione incluse in questa riga di offerta. Per verificare quali classi di transazioni sono incluse, seleziona la scheda **Generale** nella riga di offerta basata su progetto e controlla i valori per **Includi tempo**, **Includi spese**, **Includi materiali** e **Includi commissioni**.  Per verificare quali attività sono incluse, seleziona la scheda **Attività addebitabili** nella riga di offerta.

A seconda delle attività associate e delle classi di transazione incluse, le stime per tali combinazioni di attività e classi di transazione vengono importate nella riga di offerta.

Quando si importano le stime, il sistema imposterà il prezzo in base ai listini prezzi di progetto allegati all'offerta e al tipo di fatturazione impostato nella riga di offerta basata su progetto. Se un'attività, un ruolo o una categoria è configurato nella riga dell'offerta basata su progetto come non addebitabile, la riga della stima importata verrà impostata come non addebitabile e non si sommerà al valore quotato della riga dell'offerta.

Quando una riga di offerta include dettagli, i campi **Valore offerta** e **Imposta stimata** sulla riga dell'offerta vengono riepilogati e non possono essere modificati.

Quando sono selezionate più opzioni di riepilogo, il sistema tenta il riepilogo in base a tutte le opzioni selezionate. Ciò significa che l'output delle righe di offerta importate sarà maggiore rispetto alla selezione di una sola opzione di riepilogo.

Ad esempio, se il progetto ha le seguenti righe di stima per le spese.

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
| Attività A | Biglietto aereo | 1/10/2020 | 4 | 400 | 1600 |
| Attività B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Attività C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Quando l'utente seleziona il riepilogo per classe di transazione, verranno importate le seguenti informazioni.

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
|||1/10/2020 | 3.34 | 840 | 2800 |

Quando l'utente seleziona il riepilogo per classe di transazione e categoria, verranno importate le seguenti informazioni.

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
| Attività A | Biglietto aereo | 1/10/2020 | 4 | 400 | 1600 |
| | Hotel | 1/10/2020 | 6 | 200 | 1200 |

Quando l'utente seleziona il riepilogo per classe di transazione, categoria e attività del nodo foglia, verranno importate le seguenti informazioni. Notare che questo risultato è lo stesso di quello che era nel progetto.

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
| Attività A | Biglietto aereo | 1/10/2020 | 4 | 400 | 1600 |
| Attività B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Attività C | Hotel | 1/11/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
