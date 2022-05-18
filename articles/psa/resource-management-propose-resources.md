---
title: Proporre risorse di progetto
description: In questo argomento vengono fornite informazioni sulla proposta delle risorse di progetto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: fc18c5cbd1a564e186f533a3c0f972e60229a6d9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587453"
---
# <a name="propose-project-resources"></a>Proporre risorse di progetto

[!include [banner](../includes/psa-now-project-operations.md)]

I responsabili delle risorse possono proporre una risorsa al responsabile di progetto mediante una richiesta di risorsa.

1. Nella griglia delle richieste o nella richiesta stessa, seleziona **Cerca risorse**.
2. Nella pagina **Assistente di pianificazione**, seleziona la risorsa e quindi, nel riquadro **Crea prenotazione risorsa**, nel campo **Stato di prenotazione**, seleziona **Prenota**.

    ![Risorsa proposta selezionata.](media/Resource-Management-image62.png)

Lo stato viene aggiornato come segue:

- Nella pagina **Assistente di pianificazione**, gli indicatori di stato vengono aggiornati per indicare che la prenotazione è stata proposta ma che non è definitiva.

    ![Indicatori di stato per la prenotazione proposta nella pagina Assistente di pianificazione.](media/Resource-Management-image63.png)

- Nella richiesta di risorsa, lo stato diventa **Revisione necessaria**.

    ![Stato della richiesta di risorsa aggiornato a Revisione necessaria.](media/Resource-Management-image64.png)

- Nella scheda **Team** del progetto, il valore **Stato richiesta** del membro del team generico diventa **Revisione necessaria**.

    ![Stato della richiesta del membro del team generico aggiornato a Revisione necessaria nella scheda Team.](media/Resource-Management-image48.png)

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

![Visualizzare l'utilizzo delle risorse.](media/Resource-Management-image65.png)

Ogni cella nella griglia rappresenta la percentuale di utilizzo fatturabile della risorsa in un periodo, ad esempio un giorno, una settimana o un mese. Le seguenti formule vengono utilizzate per colorare le celle:

- **Verde:** utilizzo fatturabile \>= utilizzo di destinazione risorsa.
- **Giallo:** utilizzo di destinazione – 20 \<= utilizzo fatturabile \< utilizzo di destinazione
- **Rosso:** utilizzo fatturabile \< utilizzo di destinazione – 20

Poiché la vista **Utilizzo risorsa** è basata sulla scheda di pianificazione, puoi utilizzare le funzionalità di filtro della scheda di pianificazione per filtrare i risultati.

La griglia richiede l'impostazione di un utilizzo di destinazione per il ruolo o la singola risorsa. A questo proposito, seleziona **Risorse** \> **Ruoli risorsa**.

Inoltre, un ruolo predefinito deve essere assegnato a ogni risorsa prenotabile. Seleziona **Risorse** \> **Risorse**. Nella scheda **Project Service**, verifica che un ruolo risorsa sia definito e che il relativo campo **Predefinito** sia impostato su **Sì**. Puoi aggiungere ruoli aggiuntivi dove **Predefinito = No**. Il ruolo dove **Predefinito = Sì** viene utilizzato per valutare l'utilizzo della risorsa in base alla destinazione di quel ruolo.

![Ruolo predefinito impostato.](media/Resource-Management-image67.png)

Nella scheda **Project Service**, puoi impostare un singolo utilizzo di destinazione per la risorsa. Per il calcolo dell'utilizzo viene quindi utilizzato l'utilizzo di destinazione allo scopo di valutare la destinazione della risorsa anziché la destinazione del ruolo predefinito della risorsa.

L'utilizzo viene visualizzato per una risorsa solo se questa ha tempo addebitabile approvato durante il periodo visualizzato nella griglia.

## <a name="resource-availability"></a>Disponibilità delle risorse

È importante che i responsabili delle risorse siano in grado di visualizzare la disponibilità delle risorse e aggiornare le prenotazioni. In alcuni casi, non è necessaria una domanda formale (richiesta di risorsa), ma un responsabile delle risorse deve rispondere a una domanda non pianificata inviata tramite canali come un'e-mail, una telefonata o un sms. I responsabili delle risorse utilizzano la scheda di pianificazione per aggiornare le risorse e le prenotazioni.

Le ore lavorative di una risorsa sono utilizzate come base per il calcolo della disponibilità della risorsa. Le prenotazioni di risorse consumano la capacità delle risorse.

![Scheda di pianificazione.](media/Resource-Management-image68.png)

Nella scheda di pianificazione sono utilizzati colori e ombreggiature per indicare prenotazioni, disponibilità e sovraprenotazioni nonché lo stato delle prenotazioni. Una delle impostazioni della scheda di pianificazione consente di visualizzare una legenda.

Se una freccia a destra viene visualizzata accanto a una singola risorsa prenotabile nella scheda di pianificazione, la risorsa può essere espansa per visualizzare i dettagli del lavoro per il quale la risorsa è prenotata.

![Risorsa prenotabile espansa nella scheda di pianificazione.](media/Resource-Management-image69.png)

Poiché Dynamics 365 Project Service Automation utilizza il motore Universal Resource Scheduling, se è installata anche la soluzione Dynamics 365 Field Service, puoi visualizzare i dettagli delle prenotazioni delle risorse per progetti, ordini di lavoro e qualsiasi altra entità a cui hai esteso la pianificazione.

![Dettagli delle prenotazioni delle risorse per progetti e ordini di lavoro.](media/Resource-Management-image70.png)

Per visualizzare ulteriori dettagli su una singola risorsa, fai clic con il pulsante destro del mouse sulla stessa per aprire la scheda della risorsa.

![Scheda della risorsa.](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
