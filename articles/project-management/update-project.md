---
title: Creare e aggiornare un progetto
description: Questo articolo fornisce informazioni sull'aggiornamento dei progetti in Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911095"
---
# <a name="create-and-update-a-project"></a>Creare e aggiornare un progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Di seguito è riportato un riepilogo dei campi che possono essere aggiornati in un progetto dopo che è stato creato. Sono incluse anche eventuali implicazioni applicabili basate su questi aggiornamenti.

## <a name="project-detail-fields"></a>Campi dei dettagli di progetto

- **Nome**: il titolo del progetto.
- **Descrizione**: una panoramica del progetto.
- **Cliente**: l'azienda a cui verrà consegnato il progetto.
- **Modello calendario**: le ore lavorative del progetto. Modificando questo campo, l'intera programmazione viene ricalcolata.
- **Valuta**: la valuta per il progetto. Il valore predefinito di questo campo si basa sulla valuta specificata nell'unità contratto. Quando l'unità contratto viene aggiornata, viene aggiornato anche il campo.
- **Unità contratto**: l'unità organizzativa che rappresenta la divisione o gruppo dell'azienda che è il responsabile principale dell'acquisizione della vendita e della gestione della fornitura del lavoro e dei servizi al cliente.  Quando l'unità organizzativa del responsabile di progetto non è definita, questo campo usa per impostazione predefinita il valore definito nei parametri del progetto.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
