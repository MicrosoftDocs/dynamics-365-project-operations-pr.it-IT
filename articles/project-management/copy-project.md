---
title: Copiare un progetto
description: In questo argomento vengono fornite informazioni sulla copia di progetti in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091259"
---
# <a name="copy-a-project"></a>Copiare un progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Con Dynamics 365 Project Operations, puoi creare rapidamente nuovi progetti selezionando **Copia progetto** nel modulo **Progetti**. Per copiare un progetto, apri il progetto che desideri copiare e quindi seleziona **Copia progetto**. L'azione copierà quanto segue:

- Proprietà del progetto 
- Struttura di suddivisione del lavoro
- Membri del team di progetto
- Stime di progetto
- Stime di spesa del progetto
- Stime dei materiali di progetto

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
- Data di inizio stimata: questa è la data in cui il progetto viene creato dalla copia.
- Data di fine stimata: questa data viene modificata in base alla data di inizio del nuovo progetto creato dalla copia.
- Lavoro (ore)
- Costo manodopera stimato
- Costo spese stimato
- Costo materiale stimato

> [!NOTE]
> Il progetto di copia è un'operazione a esecuzione prolungata. Vengono copiati anche i record del progetto, i relativi attributi e molte entità correlate. A causa dell'esecuzione prolungata dell'operazione, dopo l'avvio della copia, la pagina del progetto di destinazione è bloccata per la modifica fino al completamento dell'operazione di copia.

## <a name="work-breakdown-structure"></a>Struttura di suddivisione del lavoro

Quando il progetto viene copiato, viene copiata l'intera struttura di suddivisione del lavoro caricata dalle risorse. Le risorse denominate vengono sostituite dalle risorse generiche. Se le risorse denominate non hanno lo stesso orario di lavoro della risorsa generica, la pianificazione verrà ricalcolata e la durata delle attività potrebbe cambiare.

## <a name="project-team-members"></a>Membri del team di progetto

Quando un team di progetto viene copiato dal progetto di origine, vengono copiate le risorse generiche. Anche le assegnazioni di risorse generiche vengono gestite come se fossero nel progetto di origine. Le risorse denominate verranno convertite in membri generici del team.

## <a name="estimates"></a>Stime

Quando il progetto viene copiato, le righe di risorse, spese e stima dei materiali vengono copiate dal progetto di origine. 

Per informazioni su come accedere a livello di codice a Copia progetto, vedi [Sviluppare modelli di progetto con Copia progetto](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
