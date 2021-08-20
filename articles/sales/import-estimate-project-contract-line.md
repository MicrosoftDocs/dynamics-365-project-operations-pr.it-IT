---
title: Importare una stima in una voce di contratto basata su progetto
description: Questo argomento fornisce informazioni su come importare le stime da un progetto a una voce di contratto.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea513ca8126eadbf563f3c6cb3e966f81703ae805d12881f865cdc1dd77e191d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990096"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importare una stima in una voce di contratto basata su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

In Dynamics 365 Project Operations, puoi importare stime da un progetto in una voce di contratto basata su progetto.

1. Verifica che il campo **Progetto** nella voce del contratto basata su progetto sia compilato.
2. Nella scheda **Dettagli voce di contratto**, seleziona nella griglia secondaria **Importa da stima di progetto**. Si apre una pagina di dialogo con le opzioni di riepilogo. Le opzioni di riepilogo disponibili sono **Classe di transazione**, **Categoria**, **Ruolo** e **Attività di progetto**. In base alla selezione del riepilogo, viene copiata la stima dal progetto per tutte le classi di transazione incluse in questa voce di contratto. 
3. Per verificare quali classi di transazione sono incluse, nella scheda **Generale** nella voce di contratto controlla i valori per i campi **Includi tempo**, **Includi spese** e **Includi commissioni**.

Quando importi le stime, l'applicazione imposta il prezzo in base ai listini prezzi di progetto allegati al contratto e al tipo di fatturazione impostato nella voce di contratto. Se un ruolo o una categoria è configurato nella voce di contratto come non addebitabile, la riga della stima importata per il ruolo o la categoria è non addebitabile e non si sommerà al valore di contratto della voce di contratto.

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
| &nbsp;  | &nbsp;  | 1/10/2020 | 3.34 | 840 | 2800 |

Quando l'utente seleziona il riepilogo per **Classe di transazione** e **Categoria**, verranno importate le seguenti informazioni:

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
| Attività A | Biglietto aereo | 1/10/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 1/10/2020 | 6 | 200 | 1200 |

Quando l'utente seleziona il riepilogo per **Classe di transazione**, **Categoria** e **Attività nodo foglia**, verranno importate le seguenti informazioni. Nota che questo risultato è lo stesso di quello che era nel progetto:

| Attività | Categoria. | Data | Quantità | Prezzo unitario | Importa |
| --- | --- | --- | --- | --- | --- |
| Attività A | Biglietto aereo | 1/10/2020 | 4 | 400 | 1600 |
| Attività B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Attività C | Hotel | 1/11/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]