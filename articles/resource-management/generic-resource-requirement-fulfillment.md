---
title: Soddisfare i requisiti generici delle risorse
description: In questo argomento vengono fornite informazioni sulla prenotazione di risorse denominate per un requisito di risorsa generica.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897591"
---
# <a name="generic-resource-requirement-fulfillment"></a>Soddisfare i requisiti generici delle risorse

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi prenotare una risorsa denominata per sostituire una risorsa generica che ha un requisito di risorsa.

1. Nella pagina **Progetti**, seleziona la scheda **Team**.
2. Seleziona la risorsa generica che ha un requisito di risorsa nell'elenco e seleziona **Prenota**. Oppure apri il requisito di risorsa e seleziona **Prenota**.
3. Nella pagina **Assistente di pianificazione**, seleziona una risorsa denominata per prenotarla per il team di progetto e seleziona **Prenota**.

Al termine della prenotazione di una risorsa denominata, questa sostituisce la risorsa generica.

Anche le assegnazioni nella pianificazione vengono aggiornate con la risorsa denominata.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Soddisfare un requisito di risorsa generica con molteplici risorse denominate
Soddisfare un requisito di risorsa generica con molteplici risorse denominate è simile ad assegnare una singola risorsa denominata. Ad esempio, supponiamo di avere un'attività di una durata di cinque giorni con 120 ore di lavoro richiesto. Questa attività non può essere completata da una risorsa che ha un orario di lavoro tipico di otto ore al giorno per cinque giorni alla settimana. 

Il requisito è di 120 ore di ingegneria robotica durante cinque giorni, ovvero 24 ore al giorno.

Questo è un esempio di quando più risorse denominate sono necessarie per soddisfare una richiesta di risorse generiche. Devi quindi prenotare più risorse per soddisfare il requisito.

La differenza principale in questo scenario è che la risorsa generica rimane nel team assegnato all'attività e i membri del team di risorse denominate prenotate non sono assegnati come parte della posizione. Il responsabile di progetto può assegnare il lavoro come appropriato alle risorse denominate. La vista **Riconciliazione** può consentire a un responsabile di progetto di suddividere le prenotazioni tra molteplici risorse per le assegnazioni delle attività. Questa operazione non viene eseguita automaticamente in quanto negli scenari più complessi, come nel caso in cui il requisito è costituito da un gruppo di attività, il sistema deve supporre l'intenzione con la quale il responsabile di progetto desidera eseguire le assegnazioni. Poiché il sistema non può comprendere l'intenzione, è probabile che quanto supposto sia differente da quanto previsto e quindi si avrà un risultato incorretto o imprevedibile. Il risultato prevedibile è che la risorsa generica rimane assegnata fino a che il responsabile di progetto non crea deliberatamente assegnazioni mediante la vista **Riconciliazione**.


