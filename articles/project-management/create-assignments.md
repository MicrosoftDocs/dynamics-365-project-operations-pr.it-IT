---
title: Creare assegnazioni di risorse
description: Questo argomento fornisce informazioni sulla creazione di assegnazioni di risorse generiche e denominate.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d2e7c9a340a482a62afc0c9f0aa46c24fda27ca6ef56fdc0160f06af846c0b53
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987891"
---
# <a name="create-resource-assignments"></a>Creare assegnazioni di risorse

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


Un'assegnazione di risorse è l'associazione diretta di un membro del team di progetto a un'attività del nodo foglia. In questo argomento vengono fornite informazioni sui diversi modi per assegnare risorse.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Creare un membro del team generico mediante l'assegnazione di attività


Quando crei un membro del team generico tramite l'assegnazione di attività, crei un segnaposto o una risorsa generica. Questa risorsa generica descrive le caratteristiche della risorsa denominata che desideri utilizzare per le attività. Successivamente generi un requisito (o invii una richiesta utilizzando il requisito) che viene utilizzato per cercare e prenotare la risorsa denominata.

1. Nella griglia Pianificazione di un'attività, seleziona l'icona Risorsa nella cella della **risorsa**.
2. Digita un nome da utilizzare come nome della risorsa segnaposto. Ad esempio, "Program Manager".
3. Seleziona **Crea** e nel campo **Creazione rapida: membro del team di progetto**, imposta il ruolo per la risorsa generica.
4. Assegna le attività a questa risorsa segnaposto selezionando la risorsa nel **selettore delle risorse** per l'attività. Le risorse elencate in **Membri del team**.
5. Dopo l'assegnazione della risorsa generica, seleziona la risorsa generica nella scheda **Team** e quindi **Genera requisito** per creare un requisito di risorsa per la risorsa generica.
6. Seleziona **Prenota** per la risorsa generica e utilizza la scheda di pianificazione per trovare e prenotare una risorsa reale. Puoi anche inviare il requisito che deve essere soddisfatto da un responsabile delle risorse.
7. Quando la risorsa generica è completamente soddisfatta (l'adempimento parziale del requisito della risorsa non si tradurrà in un'assegnazione di risorse) con una risorsa denominata, la risorsa generica viene rimossa dal team. Le assegnazioni di attività per la risorsa generica vengono assegnate alla risorsa denominata che ha soddisfatto il requisito di risorsa della risorsa generica.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Assegnare una risorsa denominata dall'elenco di tutte le risorse prenotabili

Puoi utilizzare la casella di ricerca nel **selettore delle risorse** per cercare tutte le risorse prenotabili attive in Project Service e assegnarle a un'attività del nodo foglia. Le risorse assegnate questo modo sono aggiunte al team senza alcuna prenotazione. Ciò equivale ad aggiungere un membro del team e a selezionare **Nessuno** come metodo di allocazione. La risorsa è visualizzata nelle schede **Team**, **Assegnazione risorse** e **Riconciliazione** come risorse con soltanto assegnazioni e un disavanzo di prenotazione. Prenotare se desideri utilizzarne la relativa disponibilità.

1. Dalla griglia delle attività, dalla bacheca o dalla sequenza temporale, vai alla cella **Assegnato a**.
2. Nella casella di ricerca, inizia a digitare un nome. I risultati della ricerca per il nome sono visualizzati nel **selettore delle risorse** in **Altre risorse**.
3. Seleziona la risorsa che desideri assegnare all'attività o seleziona il nome della risorsa sotto **Altre risorse del team**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]