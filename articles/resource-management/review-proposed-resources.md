---
title: Esaminare le risorse proposte
description: In questo articolo vengono fornite informazioni su come proporre risorse di progetto.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f20dda2b7b384608b8f4b548c18ac21d07fee07
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924849"
---
# <a name="review-proposed-resources"></a>Esaminare le risorse proposte

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I responsabili delle risorse possono proporre una risorsa al responsabile di progetto mediante una richiesta di risorsa.

Per rivedere le risorse proposte, effettua i seguenti passaggi:

1. Dalla griglia **Richiesta** o nella richiesta stessa, seleziona **Cerca risorse**.
2. Nella pagina **Assistente di pianificazione**, seleziona la risorsa e quindi conferma che tutte le ore proposte siano incluse nella prenotazione proposta.
3. Nel riquadro **Crea prenotazione risorsa**, imposta il campo **Stato di prenotazione** su **Proposto**, quindi seleziona **Prenota**.

    > [!NOTE]
    > Se imposti **Stato di prenotazione** su **Proposto** non prenota definitivamente la risorsa e non sostituisce la risorsa generica con il membro del team denominato.

    Lo stato viene aggiornato come segue:

    - Nella pagina **Assistente di pianificazione**, gli indicatori di stato vengono aggiornati per indicare che la prenotazione è stata proposta ma che non è definitiva.
    - Nella richiesta di risorsa, lo stato diventa **Revisione necessaria**.
    - Nella scheda **Team** del progetto, il valore **Stato richiesta** del membro del team generico diventa **Revisione necessaria**.

Il responsabile di progetto può accettare o rifiutare la proposta.

Quando i responsabili di progetto elaborano i requisiti di risorsa, possono utilizzare uno dei seguenti approcci:

- Proporre molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare le ore richieste. Le ore proposte vengono quindi suddivise tra molteplici risorse che possono soddisfare le ore richieste. In questo scenario, le ore non possono sovrapporsi.
- Proporre meno risorse del necessario. In questo scenario, la capacità della risorsa proposta è inferiore alle ore necessarie specificate dal richiedente. Quando il richiedente accetta le risorse proposte, un requisito di risorsa non soddisfatto viene creato per acquisire la domanda restante.
- Prenotare molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare il lavoro.
- Prenota meno risorse del necessario. In questo scenario, le ore prenotate sono inferiori alle ore richieste. Il sistema ti guida per proporre risorse anziché prenotazioni, di modo che il richiedente possa verificare e tenere traccia della domanda restante.

## <a name="resource-availability"></a>Disponibilità delle risorse

I Resource Manager devono essere in grado di visualizzare la disponibilità delle risorse e aggiornare le prenotazioni. In alcuni casi, non vi è alcuna richiesta formale (richiesta di risorse). Tuttavia, un resource manager deve rispondere a una richiesta non pianificata che arriva attraverso altri canali come e-mail, telefonate o messaggi istantanei. I resource manager utilizzano **Scheda di pianificazione** per aggiornare le risorse e le prenotazioni.

Le ore lavorative di una risorsa sono utilizzate come base per il calcolo della disponibilità della risorsa. Le prenotazioni di risorse consumano la capacità delle risorse.

La **Scheda di pianificazione** utilizza colori e ombreggiature per indicare prenotazioni, disponibilità e sovraprenotazioni nonché lo stato delle prenotazioni. Un'impostazione nella **Scheda di pianificazione** consente di visualizzare una legenda.

Se una freccia a destra viene visualizzata accanto a una singola risorsa prenotabile nella **Scheda di pianificazione**, la risorsa può essere espansa per visualizzare i dettagli del lavoro per il quale la risorsa è prenotata.

Poiché Dynamics 365 Project Operations utilizza il motore Universal Resource Scheduling, se è installata anche la soluzione Dynamics 365 Field Service, puoi visualizzare i dettagli delle prenotazioni delle risorse per progetti, ordini di lavoro e qualsiasi altra entità a cui hai esteso la pianificazione.

Per visualizzare ulteriori dettagli su una singola risorsa, fai clic con il pulsante destro del mouse sulla stessa per aprire la scheda della risorsa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
