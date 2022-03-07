---
title: Importare una stima in una voce di contratto basata su progetto - semplice
description: Questo argomento fornisce informazioni sull'importazione delle stime finanziarie da un progetto in una voce di contratto.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fb85d835789da82f22ae007addb6757ab3c166180992e4ce3a5c85606be6671d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997251"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Importare una stima in una voce di contratto basata su progetto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

In Dynamics 365 Project Operations, puoi importare stime da un progetto in una voce di contratto basata su progetto.

1. Verifica che il campo **Progetto** nella voce del contratto basata su progetto sia compilato.
2. Nella scheda **Dettagli voce di contratto**, seleziona nella griglia secondaria **Importa da stima di progetto**. Si apre una pagina di dialogo con le opzioni di riepilogo. Le opzioni di riepilogo disponibili sono **Classe di transazione**, **Categoria**, **Ruolo** e **Attività di progetto**.
3. In base alla selezione del riepilogo, viene copiata la stima dal progetto per tutte le classi di transazione e le attività incluse in questa voce di contratto. Per verificare quali classi di transazione sono incluse, nella scheda **Generale** nella voce di contratto basata su progetto controlla i valori per i campi **Includi tempo**, **Includi spese** e **Includi commissioni**. 
4. Per verificare quali attività sono incluse, seleziona la scheda **Attività addebitabili** nella voce di contratto. A seconda delle attività associate con il campo **Classi di transazione incluse** impostato su **Sì**, tutte le stime per tali combinazioni di attività e classi di transazione vengono importate nella voce di contratto.

Quando importi le stime, il sistema imposta il prezzo in base ai listini prezzi di progetto allegati al contratto e al tipo di fatturazione impostato nella voce di contratto. Se un'attività, un ruolo o una categoria è configurato nella voce di contratto come non addebitabile, la riga della stima importata verrà impostata come non addebitabile e non si sommerà al valore di contratto della voce di contratto.

Quando una voce di contratto include dettagli, i campi **Valore contratto** e **Imposta stimata** sulla voce di contratto vengono riepilogati e non possono essere modificati.

Quando sono selezionate più opzioni di riepilogo, il sistema tenta il riepilogo in base a tutte le opzioni selezionate. L'output del riepilogo produce più voci di contratto importate rispetto a quando selezioni una sola opzione di riepilogo.

Ad esempio, se il progetto ha le seguenti righe di stima per le spese:

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
| Attività A | Biglietto aereo | 1/10/2020 | 4 | 400 | 1600 |
| Attività B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Attività C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Quando l'utente seleziona il riepilogo per **Classe di transazione**, verranno importate le seguenti informazioni:

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 1/10/2020 | 3.34 | 840 | 2800 |

Quando l'utente seleziona il riepilogo per **Classe di transazione** e **Categoria**, verranno importate le seguenti informazioni:

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
| Attività A | Biglietto aereo | 1/10/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 1/10/2020 | 6 | 200 | 1200 |

Quando l'utente seleziona il riepilogo per **Classe di transazione**, **Categoria** e **Attività nodo foglia**, verranno importate le seguenti informazioni. Nota che questo risultato è lo stesso di quello presente nel progetto:

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
| Attività A | Biglietto aereo | 1/10/2020 | 4 | 400 | 1600 |
| Attività B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Attività C | Hotel | 1/11/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]