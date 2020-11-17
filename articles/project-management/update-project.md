---
title: Aggiornare un progetto
description: Questo argomento fornisce informazioni sull'aggiornamento di progetti in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131438"
---
# <a name="update-a-project"></a>Aggiornare un progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Di seguito è riportato un riepilogo dei campi che possono essere aggiornati in un progetto dopo che è stato creato e le implicazioni applicabili degli aggiornamenti.

## <a name="project-detail-fields"></a>Campi dei dettagli di progetto

- **Nome**: il titolo del progetto.
- **Descrizione**: una panoramica del progetto.
- **Cliente**: l'azienda a cui verrà consegnato il progetto.
- **Modello calendario**: le ore lavorative del progetto. Quando il campo viene modificato, l'intera pianificazione viene ricalcolata.
- **Valuta**: la valuta per il progetto. Il valore predefinito di questo campo si basa sulla valuta definita nell'unità contratto. Quando l'unità contratto viene aggiornata, viene aggiornato anche il campo.
- **Unità contratto**: l'unità organizzativa che rappresenta la divisione o gruppo dell'azienda che è il responsabile principale dell'acquisizione della vendita e della gestione della fornitura del lavoro e dei servizi al cliente. 
- **Responsabile di progetto**: il membro del team di progetto che ha l'autorità di rivedere e approvare gli inserimenti ore e le spese.

## <a name="estimate-fields"></a>Campi di stima

- **Data di inizio stimata**: la data in cui inizierà il progetto. Quando questo campo viene aggiornato, tutte le attività del progetto si sposteranno proporzionalmente con la nuova data di inizio.
- **Data di fine**: la data in cui è prevista la fine del progetto.
- **Lavoro richiesto**: il lavoro richiesto stimato del progetto. Quando le attività vengono aggiunte al progetto, questo campo non è più modificabile.
- **Costo della manodopera stimato**: il costo stimato della manodopera del progetto. Quando i costi di manodopera vengono aggiunti al progetto, questo campo non è più modificabile.
- **Spese stimate**: le spese stimate del progetto. Quando le spese vengono aggiunte al progetto, questo campo non è più modificabile.

## <a name="project-actual-fields"></a>Campi effettivi del progetto
- **Inizio effettivo**: la data di inizio del progetto.
- **Fine effettiva**: da aggiornare quando un progetto è stato completato.

## <a name="project-status-fields"></a>Campi relativi allo stato del progetto

- **Stato di progetto generale**: lo stato complessivo del progetto fornito dal responsabile di progetto.
- **Commenti**: una descrizione dello stato attuale del progetto fornita dal responsabile di progetto.

