---
title: Gestire membri del team
description: In questo argomento vengono fornite informazioni sulla prenotazione di risorse denominate per team di progetto e sull'assegnazione delle risorse ad attività.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131528"
---
# <a name="maintain-team-members"></a>Gestire membri del team

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi aggiungere una risorsa denominata a un team di progetto prenotandole direttamente nel team.

1. In Dynamics 365 Project Operations, vai a **Progetti** e apri il progetto per cui esegui le prenotazioni.
2. Nella pagina **Progetto**, nella scheda **Team**, seleziona **Nuovo**. 
3. Nella finestra di dialogo **Creazione rapida: Membro del team di progetto**, seleziona la risorsa prenotabile. Il campo **Ruolo** verrà popolato con il ruolo predefinito della risorsa, se a questa ne è stato assegnato uno. È possibile modificare il ruolo. 
4. Seleziona le date di inizio e di fine per la risorsa e quindi il metodo di allocazione della capacità della risorsa. 
5. Se il membro del team deve essere un responsabile approvazione di progetto, seleziona **Sì** nel campo **Responsabile approvazione di progetto**. Il membro del team può approvare voci di spesa e inserimenti ore inviati per il progetto. 
6. Seleziona **Salva**.

Ora puoi assegnare la risorsa prenotata ad attività nel progetto. Nella pagina **Progetto**, fai clic sulla scheda **Pianifica** per assegnare attività alla nuova risorsa. Il selettore di risorse eseguito dal campo **Risorse** nella griglia delle attività indicherà i membri del team che è possibile selezionare.


In Project Operations, le prenotazioni di risorse e le assegnazioni di attività non sono strettamente collegate. Quando utilizzi il selettore di risorse nella pianificazione, puoi assegnare attività a membri del team per più ore di quelle che le relative prenotazioni coprono nel progetto.

Le differenze tra le prenotazioni dei membri del team e le assegnazioni sono mostrate nelle schede **Team** e **Riconciliazione risorse**. Puoi anche riconciliare le differenze tra le prenotazioni e le assegnazioni per le risorse a un livello più dettagliato.

Utilizza il selettore di risorse nella scheda **Pianifica** per cercare e selezionare le risorse prenotabili che non fanno ancora parte del team di progetto. Queste risorse sono visualizzate nel selettore di risorse come **Altre risorse**.

Quando si effettua una selezione, la risorsa viene aggiunta al team di progetto e assegnata all'attività, ma non viene generata alcuna prenotazione.

Puoi utilizzare la funzionalità di prenotazione estesa della scheda **Riconciliazione** o la **Scheda di pianificazione** per prenotare la capacità della risorsa per il progetto.

Dopo la prenotazione di un membro del team nel progetto, puoi utilizzare **Gestisci prenotazioni** o la **scheda di pianificazione** direttamente per gestire le tue prenotazioni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]