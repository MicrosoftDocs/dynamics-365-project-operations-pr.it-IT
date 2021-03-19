---
title: Prenotare risorse denominate da requisiti di risorsa
description: In questo argomento vengono fornite informazioni sulla prenotazione di risorse denominate per un requisito di risorsa generica.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 50858d4fc55285b2e91117c6cbfb2419931b4197
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291039"
---
# <a name="book-named-resources-from-resource-requirements"></a>Prenotare risorse denominate da requisiti di risorsa

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Puoi prenotare una risorsa denominata per sostituire una risorsa generica che ha un requisito di risorsa.

1. In Project Service Automation (PSA), nella pagina **Progetti**, fai clic sulla scheda **Team**.
2. Seleziona la risorsa generica che ha un requisito di risorsa nell'elenco e fai clic su **Prenota**. Oppure apri il requisito di risorsa e fai clic su **Prenota**.


![Prenotare un membro del team generico](media/RM-how-to-14.png)


3. Nella pagina **Assistente di pianificazione**, seleziona una risorsa denominata per prenotarla per il team di progetto e fai clic su **Prenota**.

![Prenotare un membro del team generico utilizzando l'assistente di pianificazione](media/RM-how-to-15.png)

Al termine della prenotazione di una risorsa denominata, questa sostituisce la risorsa generica.

![Membro del team denominato che sostituisce un membro del team generico](media/RM-how-to-16.png)

Anche le assegnazioni nella pianificazione vengono aggiornate con la risorsa denominata.

![Membro del team denominato assegnato ad attività di progetto](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Soddisfare un requisito di risorsa generica con molteplici risorse denominate
Soddisfare un requisito di risorsa generica con molteplici risorse denominate è simile ad assegnare una singola risorsa denominata. Ad esempio, supponiamo di avere un'attività di una durata di cinque giorni con 120 ore di lavoro richiesto. Questa attività non può essere completata da una risorsa che ha un orario di lavoro tipico di otto ore al giorno per cinque giorni alla settimana. 

![Un'attività che necessita di 120 ore di lavoro in cinque giorni](media/RM-how-to-21.png)

Il requisito è di 120 ore di ingegneria robotica durante cinque giorni, ovvero 24 ore al giorno.

![Requisito giornaliero](media/RM-how-to-22.png)

Questo è un esempio di quando più risorse denominate sono necessarie per soddisfare una richiesta di risorse generiche. Devi quindi prenotare più risorse per soddisfare il requisito.

![Prenotare molteplici risorse per soddisfare il requisito](media/RM-how-to-23.png)

La differenza principale in questo scenario è che la risorsa generica rimane nel team assegnato all'attività e i membri del team di risorse denominate prenotate non sono assegnati come parte della posizione. Il responsabile di progetto può assegnare il lavoro come appropriato alle risorse denominate. La vista **Riconciliazione** può consentire a un responsabile di progetto di suddividere le prenotazioni tra molteplici risorse per le assegnazioni delle attività. Questa operazione non viene eseguita automaticamente in quanto negli scenari più complessi, come nel caso in cui il requisito è costituito da un gruppo di attività, il sistema deve supporre l'intenzione con la quale il responsabile di progetto desidera eseguire le assegnazioni. Poiché il sistema non può comprendere l'intenzione, è probabile che quanto supposto sia differente da quanto previsto e che si abbia quindi un risultato incorretto o imprevedibile. Il risultato prevedibile è che la risorsa generica rimane assegnata fino a che il responsabile di progetto non crea deliberatamente assegnazioni mediante la vista **Riconciliazione**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]