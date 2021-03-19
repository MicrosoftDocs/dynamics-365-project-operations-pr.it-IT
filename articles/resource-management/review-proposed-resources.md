---
title: Esaminare le risorse proposte
description: In questo argomento vengono fornite informazioni su come proporre risorse di progetto.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279278"
---
# <a name="review-proposed-resources"></a>Esaminare le risorse proposte

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I responsabili delle risorse possono proporre una risorsa al responsabile di progetto mediante una richiesta di risorsa.

1. Nella griglia delle richieste o nella richiesta stessa, seleziona **Cerca risorse**.
2. Nella pagina **Assistente di pianificazione**, seleziona la risorsa e quindi, nel riquadro **Crea prenotazione risorsa**, nel campo **Stato di prenotazione**, seleziona **Prenota**.

Lo stato viene aggiornato come segue:

- Nella pagina **Assistente di pianificazione**, gli indicatori di stato vengono aggiornati per indicare che la prenotazione è stata proposta ma che non è definitiva.
- Nella richiesta di risorsa, lo stato diventa **Revisione necessaria**.
- Nella scheda **Team** del progetto, il valore **Stato richiesta** del membro del team generico diventa **Revisione necessaria**.

Il responsabile di progetto può accettare o rifiutare la proposta.

Quando i responsabili di progetto elaborano i requisiti di risorsa, possono utilizzare uno dei seguenti approcci:

- Proporre molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare le ore richieste. Le ore proposte vengono quindi suddivise tra molteplici risorse che possono soddisfare le ore richieste. In questo scenario, le ore non possono sovrapporsi.
- Proporre meno risorse del necessario. In questo scenario, la capacità della risorsa proposta è inferiore alle ore necessarie specificate dal richiedente. Pertanto, quando il richiedente accetta le risorse proposte, un requisito di risorsa non soddisfatto viene creato per acquisire la domanda restante.
- Prenotare molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare il lavoro.
- Prenotare meno risorse del necessario. In questo scenario, le ore prenotate sono inferiori alle ore richieste. Il sistema ti guida per proporre risorse anziché prenotazioni, di modo che il richiedente possa verificare e tenere traccia della domanda restante.

## <a name="resource-availability"></a>Disponibilità delle risorse

È importante che i responsabili delle risorse siano in grado di visualizzare la disponibilità delle risorse e aggiornare le prenotazioni. In alcuni casi, non è necessaria una domanda formale (richiesta di risorsa), ma un responsabile delle risorse deve rispondere a una domanda non pianificata inviata tramite canali come un'e-mail, una telefonata o un sms. I responsabili delle risorse utilizzano la scheda di pianificazione per aggiornare le risorse e le prenotazioni.

Le ore lavorative di una risorsa sono utilizzate come base per il calcolo della disponibilità della risorsa. Le prenotazioni di risorse consumano la capacità delle risorse.

Nella scheda di pianificazione sono utilizzati colori e ombreggiature per indicare prenotazioni, disponibilità e sovraprenotazioni nonché lo stato delle prenotazioni. Una delle impostazioni della scheda di pianificazione consente di visualizzare una legenda.

Se una freccia a destra viene visualizzata accanto a una singola risorsa prenotabile nella scheda di pianificazione, la risorsa può essere espansa per visualizzare i dettagli del lavoro per il quale la risorsa è prenotata.

Poiché Dynamics 365 Project Operations utilizza il motore Universal Resource Scheduling, se è installata anche la soluzione Dynamics 365 Field Service, puoi visualizzare i dettagli delle prenotazioni delle risorse per progetti, ordini di lavoro e qualsiasi altra entità a cui hai esteso la pianificazione.

Per visualizzare ulteriori dettagli su una singola risorsa, fai clic con il pulsante destro del mouse sulla stessa per aprire la scheda della risorsa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]