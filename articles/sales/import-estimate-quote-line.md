---
title: Importare le stime per un progetto su una riga di offerta basata su progetto
description: Questo argomento fornisce informazioni sull'importazione delle stime da un progetto a una riga di offerta.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c0fe18b33207f73848709b99334f64aadc7867a
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078792"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importare le stime per un progetto su una riga di offerta basata su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_


Se un progetto viene creato durante la fase di prevendita, è possibile scegliere di importare la stima finanziaria dal progetto sulla riga di basata sul progetto.

1. Assicurati che la riga dell'offerta basata sul progetto contenga le informazioni sul progetto nel campo **Progetto**.
2. Nella scheda **Dettagli riga di offerta** , seleziona **Importa da stima di progetto**.
3. Nella finestra di dialogo che si apre, seleziona una delle opzioni di riepilogo seguenti:

  - **Classe di transazione**
  - **Categoria**
  - **Ruolo** 
  - **Attività di progetto**

In base alla selezione, viene copiata la stima dal progetto per tutte le classi di transazione incluse in questa riga di offerta. Per verificare quali classi di transazione sono incluse, seleziona la scheda **Generale** nella riga dell'offerta basata sul progetto e controlla i valori per **Includi tempo** , **Includi spese** e **Includi commissioni**.

Quando si importano le stime, il sistema imposterà il prezzo in base ai listini prezzi di progetto allegati all'offerta e al tipo di fatturazione impostato nella riga dell'offerta basata su progetto. Se un ruolo o una categoria è configurato nella riga dell'offerta basata sul progetto come non addebitabile, la riga della stima importata verrà impostata come non addebitabile e non si sommerà al valore quotato della riga dell'offerta.

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
| | | 1/10/2020 | 3.34 | 840 | 2800 |

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
