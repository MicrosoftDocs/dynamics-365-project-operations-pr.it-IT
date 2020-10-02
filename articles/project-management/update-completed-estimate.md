---
title: Aggiornare la stima al completamento
description: Questo argomento fornisce informazioni sull'aggiornamento della proiezione dell'impegno su un progetto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897771"
---
# <a name="update-estimate-at-completion"></a>Aggiornare la stima al completamento

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

È normale per un responsabile di progetto aggiornare le stime originali di un'attività. Le nuove proiezioni di progetto sono la percezione delle stime di un responsabile di progetto, considerato lo stato corrente del progetto. Tuttavia, non raccomandiamo la modifica delle cifre di riferimento da parte dei responsabili di progetto, poiché la linea di base del progetto rappresenta l'origine di riferimento stabilita per la pianificazione e la stima dei costi del progetto ed è stata concordata dalle parti interessate.

Vi sono due modi per un responsabile di progetto di eseguire una nuova proiezione del lavoro richiesto per le attività:

- Sostituisci la stima predefinita di completamento con una nuova stima del lavoro richiesto rimanente effettivo per l'attività. 
- Sostituire la percentuale di avanzamento predefinita con una nuova stima dell'avanzamento effettivo dell'attività.

Ognuno di questi approcci genera un nuovo calcolo di stima di completamento, stima al completamento, percentuale di avanzamento e scostamento risorse previsto dell'attività. La stima di completamento, la stima al completamento e la percentuale di avanzamento delle attività di riepilogo vengono ricalcolate e producono una nuova proiezione dello scostamento risorse.
