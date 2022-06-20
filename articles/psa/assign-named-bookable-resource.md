---
title: Prenotare risorse prenotabili denominate per un team di progetto e assegnarvi attività
description: In questo articolo vengono fornite informazioni su come prenotare le risorse denominate per team di progetto e assegnare le risorse ad attività.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 61c9b47088e836c0a9c78477adf891df3d14853b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919329"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Prenotare risorse prenotabili denominate per un team di progetto e assegnarvi attività 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Puoi aggiungere una risorsa denominata a un team di progetto prenotandole direttamente nel team. A tale scopo, eseguire la procedura seguente.

1. In Project Service Automation, seleziona **Progetti** e apri il progetto per cui esegui le prenotazioni.
2. Nella pagina **Progetto**, nella scheda **Team**, fai clic su **Nuovo**. 

![Aggiungere un membro del team dalla scheda Team.](media/RM-how-to-1.png)

3. Nella finestra di dialogo **Creazione rapida: Membro del team di progetto**, seleziona la risorsa prenotabile. Il campo **Ruolo** verrà popolato con il ruolo predefinito della risorsa, se a questa ne è stato assegnato uno. Se necessario, puoi cambiare il ruolo. 
4. Seleziona le date di inizio e di fine per la risorsa e quindi il metodo di allocazione della capacità della risorsa. 
5. Se il membro del team deve essere un responsabile approvazione di progetto, seleziona **Sì** nel campo **Responsabile approvazione di progetto**. Ciò significa che il membro del team può approvare voci di spesa e inserimenti ore inviati per il progetto. 
6. Fai clic su **Salva**.

![Aggiungere un membro del team nel modulo di creazione rapida.](media/RM-how-to-2.png)


Ora puoi assegnare la risorsa prenotata ad attività nel progetto. Nella pagina **Progetto**, fai clic sulla scheda **Pianifica** per assegnare attività alla nuova risorsa. Il selettore di risorse eseguito dal campo **Risorse** nella griglia delle attività indicherà i membri del team che è possibile selezionare.

![Assegnare un membro del team ad un'attività nella scheda Pianifica.](media/RM-how-to-3.png)

Nella versione 3 di Project Service Automation (PSA), le prenotazioni delle risorse e le assegnazioni di attività non sono strettamente correlate. Ciò significa che quando utilizzi il selettore di risorse nella pianificazione, puoi assegnare attività a membri del team per più ore di quelle che le relative prenotazioni coprono nel progetto.
Puoi vedere le differenze tra le prenotazioni dei membri del team e le assegnazioni nella scheda **Team** o nella scheda **Riconciliazione risorse**. Puoi inoltre riconciliare le differenze tra prenotazioni e assegnazioni delle risorse a un livello più dettagliato.

![Scheda Riconciliazione risorse.](media/RM-how-to-4.png)

Puoi anche utilizzare il selettore di risorse nella scheda **Pianifica** per cercare e selezionare le risorse prenotabili che non fanno ancora parte del team di progetto. Queste sono visualizzate nel selettore di risorse come **Altre risorse**.

![Assegnare una risorsa non membro del team ad un'attività.](media/RM-how-to-5.png)

Quando si esegue tale operazione, la risorsa viene aggiunta al team di progetto e assegnata all'attività, ma non viene generata alcuna prenotazione.

![Membro del team con assegnazioni e nessuna prenotazione.](media/RM-how-to-6.png)

Puoi utilizzare la funzionalità di prenotazione estesa della scheda **Riconciliazione** o la **Scheda di pianificazione** per prenotare la capacità della risorsa per il progetto.

![Estendere le prenotazioni per un membro del team nella scheda Riconciliazione risorse.](media/RM-how-to-7.png)

Dopo la prenotazione di un membro del team nel progetto, puoi utilizzare Gestisci prenotazioni o la scheda di pianificazione direttamente per gestire le tue prenotazioni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
