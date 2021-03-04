---
title: Copiare un progetto
description: Questo argomento fornisce informazioni sulla copia di progetti in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131798"
---
# <a name="copy-a-project"></a>Copiare un progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Con Dynamics 365 Project Operations, puoi creare rapidamente nuovi progetti selezionando **Copia progetto** nel modulo **Progetti**. Per copiare un progetto, apri il progetto che desideri copiare e quindi seleziona **Copia progetto**. L'azione copierà:

- Proprietà del progetto
- Struttura di suddivisione del lavoro
- Membri del team di progetto
- Stime di progetto
- Stime di spesa del progetto

## <a name="project-properties"></a>Proprietà del progetto

Quando il progetto viene copiato, vengono copiati i valori nei seguenti campi:

- Nome
- Descrizione
- Cliente
- Modello calendario
- Valuta
- Unità contratto
- Responsabile di progetto
- Stato
- Stato di progetto generale
- Commenti
- Stime
- Data di inizio prevista
- Data di fine
- Lavoro (ore)
- Costo della manodopera stimato
- Costo spese stimato

## <a name="work-breakdown-structure"></a>Struttura di suddivisione del lavoro

Quando il progetto viene copiato, viene copiata l'intera struttura di suddivisione del lavoro caricata dalle risorse. Le risorse denominate vengono sostituite dalle risorse generiche. Se le risorse denominate non hanno lo stesso orario di lavoro della risorsa generica, la pianificazione verrà ricalcolata e la durata delle attività potrebbe cambiare.

## <a name="project-team-members"></a>Membri del team di progetto

Quando un team di progetto viene copiato dal progetto di origine, vengono copiate le risorse generiche. Anche le assegnazioni di risorse generiche vengono gestite come se fossero nel progetto di origine. Le risorse denominate verranno convertite in membri generici del team.

## <a name="estimates"></a>Stime

Quando il progetto viene copiato, le righe di stima delle risorse e delle spese vengono copiate dal progetto di origine. 

Per informazioni su come accedere a livello di codice a Copia progetto, vedi [Sviluppare modelli di progetto con Copia progetto](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]