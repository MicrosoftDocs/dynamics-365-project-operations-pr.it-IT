---
title: Assegnare risorse prenotabili generiche a un'attività e a un team di progetto
description: In questo argomento vengono fornite informazioni sulla prenotazione di risorse generiche per attività e team di progetto.
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127073"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Assegnare risorse prenotabili generiche a un'attività e generare requisiti di risorsa 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Oltre a prenotare e assegnare risorse denominate o reali al tuo progetto, puoi assegnare risorse generiche ad attività di progetto. Queste risorse possono essere utilizzate come segnaposto per le risorse denominate fino a che non si è pronti ad assegnare risorse denominate al progetto. 

1. In Project Service Automation (PSA), apri la pagina **Progetto** e nella scheda **Pianifica**, immetti il nome posizione della risorsa generica nella cella **Risorsa** della pianificazione. In alternativa, fai clic sull'icona **Risorsa** nella cella per aprire il selettore di risorse e quindi immetti il nome della risorsa generica che intendi creare.

![Creare e assegnare un membro del team generico](media/RM-how-to-9.png)

Viene aperto il pannello **Creazione rapida: Membro del team di progetto**. 

2. Immetti il ruolo e l'unità organizzativa del membro del team di risorse generiche e quindi fai clic su **Salva**.

![Creazione rapida di un membro del team generico](media/RM-how-to-10.png)

3. Dopo aver creato il nuovo membro del team di risorse generiche, questo viene assegnato all'attività. Puoi continuare ad assegnare quella risorsa generica ad altre attività nella pianificazione.

![Assegnare un membro del team generico esistente ad attività](media/RM-how-to-11.png)

4. Dopo aver assegnato la risorsa generica, puoi generare un requisito di risorsa e soddisfarlo prenotando direttamente o inviando una richiesta di risorsa a un responsabile delle risorse.

![Generare un requisito per un membro del team generico](media/RM-how-to-12.png)

Nella griglia dei membri del team, oltre a poter utilizzare il selettore di risorse come indicato in precedenza, puoi aggiungere risorse generiche direttamente. Le risorse sono aggiunte con un requisito di risorsa basato sulle date di inizio/fine e sul metodo di allocazione specificati nel pannello **Creazione rapida: Membro del team di progetto**.

Puoi osservare una differenza se aggiungi il membro del team generico direttamente e quindi assegni più attività alla risorsa generica delle ore richieste che deve coprire. Fai clic su **Genera requisito** per rigenerare il requisito ed equilibrare le ore richieste rispetto alle assegnazioni.

Puoi anche fare clic sul collegamento **Requisito di risorsa** nella griglia del team per aprire il requisito e aggiungere competenze, risorse preferite e così via.

![Requisito di risorsa](media/RM-how-to-13.png)

