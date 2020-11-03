---
title: Esaminare le risorse proposte
description: In questo argomento vengono fornite informazioni su come proporre risorse di progetto.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078843"
---
# <a name="review-proposed-resources"></a>Esaminare le risorse proposte

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I responsabili delle risorse possono proporre una risorsa al responsabile di progetto mediante una richiesta di risorsa.

1. Nella griglia delle richieste o nella richiesta stessa, seleziona **Cerca risorse**.
2. Nella pagina **Assistente di pianificazione** , seleziona la risorsa e quindi, nel riquadro **Crea prenotazione risorsa** , nel campo **Stato di prenotazione** , seleziona **Prenota**.

Lo stato viene aggiornato come segue:

- Nella pagina **Assistente di pianificazione** , gli indicatori di stato vengono aggiornati per indicare che la prenotazione è stata proposta ma che non è definitiva.
- Nella richiesta di risorsa, lo stato diventa **Revisione necessaria**.
- Nella scheda **Team** del progetto, il valore **Stato richiesta** del membro del team generico diventa **Revisione necessaria**.

Il responsabile di progetto può accettare o rifiutare la proposta.

Quando i responsabili di progetto elaborano i requisiti di risorsa, possono utilizzare uno dei seguenti approcci:

- Proporre molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare le ore richieste. Le ore proposte vengono quindi suddivise tra molteplici risorse che possono soddisfare le ore richieste. In questo scenario, le ore non possono sovrapporsi.
- Proporre meno risorse del necessario. In questo scenario, la capacità della risorsa proposta è inferiore alle ore necessarie specificate dal richiedente. Pertanto, quando il richiedente accetta le risorse proposte, un requisito di risorsa non soddisfatto viene creato per acquisire la domanda restante.
- Prenotare molteplici risorse per soddisfare la domanda se nessuna singola risorsa è disponibile per completare il lavoro.
- Prenotare meno risorse del necessario. In questo scenario, le ore prenotate sono inferiori alle ore richieste. Il sistema ti guida per proporre risorse anziché prenotazioni, di modo che il richiedente possa verificare e tenere traccia della domanda restante.

## <a name="billable-utilization"></a>Utilizzo fatturabile

Le risorse possono avere un utilizzo di destinazione fatturabile. Questo utilizzo di destinazione è definito come attributo per il ruolo predefinito di una risorsa o impostato nel record della singola risorsa prenotabile. I calcoli dell'utilizzo sono basati sulle ore effettive che le risorse hanno indicato utilizzando inserimenti ore approvati.

Le seguenti formule vengono utilizzate per calcolare l'utilizzo:

- Utilizzo fatturabile = Ore effettive addebitabili ÷ Capacità della risorsa
- Utilizzo non fatturabile = Tempo effettivo con ID tipo di fatturazione = Non addebitabile, Complementare o Non disponibile ÷ Capacità della risorsa
- Interno = Tempo effettivo senza contratto di vendita ÷ Capacità della risorsa
- Capacità della risorsa = Ore lavorative della risorsa - Fuori sede - Giorni non lavorativi

La vista **Utilizzo risorsa** si trova nel riquadro **Risorse**.

Ogni cella nella griglia rappresenta la percentuale di utilizzo fatturabile della risorsa in un periodo, ad esempio un giorno, una settimana o un mese. Le seguenti formule vengono utilizzate per colorare le celle:

- **Verde:** utilizzo fatturabile \>= utilizzo di destinazione risorsa.
- **Giallo:** utilizzo di destinazione – 20 \<= utilizzo fatturabile \< utilizzo di destinazione
- **Rosso:** utilizzo fatturabile \< utilizzo di destinazione – 20

Poiché la vista **Utilizzo risorsa** è basata sulla scheda di pianificazione, puoi utilizzare le funzionalità di filtro della scheda di pianificazione per filtrare i risultati.

La griglia richiede l'impostazione di un utilizzo di destinazione per il ruolo o la singola risorsa. A questo proposito, seleziona **Risorse** \> **Ruoli risorsa**.

Inoltre, un ruolo predefinito deve essere assegnato a ogni risorsa prenotabile. Seleziona **Risorse** \> **Risorse**. Nella scheda **Project Service** , verifica che un ruolo risorsa sia definito e che il relativo campo **Predefinito** sia impostato su **Sì**. Puoi aggiungere ruoli aggiuntivi dove **Predefinito = No**. Il ruolo dove **Predefinito = Sì** viene utilizzato per valutare l'utilizzo della risorsa in base alla destinazione di quel ruolo.

Nella scheda **Project Service** , puoi impostare un singolo utilizzo di destinazione per la risorsa. Per il calcolo dell'utilizzo viene quindi utilizzato l'utilizzo di destinazione allo scopo di valutare la destinazione della risorsa anziché la destinazione del ruolo predefinito della risorsa.

L'utilizzo viene visualizzato per una risorsa solo se questa ha tempo addebitabile approvato durante il periodo visualizzato nella griglia.

## <a name="resource-availability"></a>Disponibilità delle risorse

È importante che i responsabili delle risorse siano in grado di visualizzare la disponibilità delle risorse e aggiornare le prenotazioni. In alcuni casi, non è necessaria una domanda formale (richiesta di risorsa), ma un responsabile delle risorse deve rispondere a una domanda non pianificata inviata tramite canali come un'e-mail, una telefonata o un sms. I responsabili delle risorse utilizzano la scheda di pianificazione per aggiornare le risorse e le prenotazioni.

Le ore lavorative di una risorsa sono utilizzate come base per il calcolo della disponibilità della risorsa. Le prenotazioni di risorse consumano la capacità delle risorse.

Nella scheda di pianificazione sono utilizzati colori e ombreggiature per indicare prenotazioni, disponibilità e sovraprenotazioni nonché lo stato delle prenotazioni. Una delle impostazioni della scheda di pianificazione consente di visualizzare una legenda.

Se una freccia a destra viene visualizzata accanto a una singola risorsa prenotabile nella scheda di pianificazione, la risorsa può essere espansa per visualizzare i dettagli del lavoro per il quale la risorsa è prenotata.

Poiché Dynamics 365 Project Operations utilizza il motore Universal Resource Scheduling, se è installata anche la soluzione Dynamics 365 Field Service, puoi visualizzare i dettagli delle prenotazioni delle risorse per progetti, ordini di lavoro e qualsiasi altra entità a cui hai esteso la pianificazione.

Per visualizzare ulteriori dettagli su una singola risorsa, fai clic con il pulsante destro del mouse sulla stessa per aprire la scheda della risorsa.

