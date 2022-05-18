---
title: Panoramica dell'utilizzo della risorsa
description: In questo argomento vengono fornite informazioni sull'utilizzo delle risorse in Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e24bbb33cdf34426d4e7fff21b68fcaea2fcef5e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587131"
---
# <a name="resource-utilization-overview"></a>Panoramica dell'utilizzo della risorsa

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le risorse possono avere un utilizzo di destinazione fatturabile. Questo utilizzo di destinazione è definito come attributo per il ruolo predefinito di una risorsa o impostato nel record della singola risorsa prenotabile. I calcoli dell'utilizzo sono basati sulle ore effettive che le risorse hanno indicato utilizzando inserimenti ore approvati.

Le seguenti formule vengono utilizzate per calcolare l'utilizzo:

  - Utilizzo fatturabile = Ore effettive addebitabili ÷ Capacità della risorsa
  - Utilizzo non fatturabile = Tempo effettivo con ID tipo di fatturazione = Non addebitabile, Complementare o Non disponibile ÷ Capacità della risorsa
  - Interno = Tempo effettivo senza contratto di vendita ÷ Capacità della risorsa
  - Capacità della risorsa = Ore lavorative della risorsa - Fuori sede - Giorni non lavorativi

La vista **Utilizzo risorsa** si trova nel riquadro **Risorse**.

Ogni cella nella griglia rappresenta la percentuale di utilizzo fatturabile della risorsa in un periodo, ad esempio un giorno, una settimana o un mese. Le seguenti formule vengono utilizzate per colorare le celle:

  - **Verde**: utilizzo fatturabile >= utilizzo di destinazione risorsa
  - **Giallo**: utilizzo di destinazione – 20 <= utilizzo fatturabile < utilizzo di destinazione
  - **Rosso**: utilizzo fatturabile <= utilizzo di destinazione – 20

Poiché la vista **Utilizzo risorsa** è basata sulla scheda di pianificazione, puoi utilizzare le funzionalità di filtro della scheda di pianificazione per filtrare i risultati.

La griglia richiede l'impostazione di un utilizzo di destinazione per il ruolo o la singola risorsa. A questo proposito, seleziona **Risorse** > **Ruoli risorsa**.

Inoltre, un ruolo predefinito deve essere assegnato a ogni risorsa prenotabile. Seleziona **Risorse** > **Risorse**. Nella scheda **Project Service** verifica che un ruolo risorsa sia definito e che il relativo campo **Predefinito** sia impostato su **Sì**. Puoi aggiungere ruoli aggiuntivi dove **Predefinito** = **No**. Il ruolo dove **Predefinito** = **Sì** viene utilizzato per valutare l'utilizzo della risorsa in base alla destinazione di quel ruolo.

Nella scheda **Project Service**, puoi impostare un singolo utilizzo di destinazione per la risorsa. Per il calcolo dell'utilizzo viene quindi utilizzato l'utilizzo di destinazione allo scopo di valutare la destinazione della risorsa anziché la destinazione del ruolo predefinito della risorsa.

L'utilizzo viene visualizzato per una risorsa solo se ha tempo addebitabile approvato durante il periodo visualizzato nella griglia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]