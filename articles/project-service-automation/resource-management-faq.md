---
title: Domande frequenti sulla gestione delle risorse
description: In questo argomento vengono illustrate le domande frequenti sulla gestione delle risorse.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752697"
---
# <a name="resource-management-faq"></a>Domande frequenti sulla gestione delle risorse

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Qual è la differenza tra un membro del team e un requisito di risorsa?

Un membro del team di progetto può essere assegnato ad attività, prenotato o sovraprenotato e impostato come revisore. Un requisito di risorsa può esistere senza un membro del team di progetto, come bozza di nota della domanda. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Qual è la differenza tra ore proposte e ore prenotate provvisoriamente?

La differenza tra le ore proposte e le ore prenotate provvisoriamente è la visibilità. Le ore proposte sono visibili solo ai responsabili delle risorse e al responsabile di progetto che ha avviato la domanda utilizzando una richiesta di risorse. Le ore prenotate provvisoriamente sono visibili a tutti coloro che hanno accesso alla scheda di pianificazione.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Come è possibile visualizzare le ore prenotate provvisoriamente per le risorse in un team?

Le prenotazioni provvisorie possono essere eseguite quando si prenota un requisito di risorsa. Le risorse prenotate provvisoriamente in un team di progetto sono visualizzate come membri del team che hanno ore prenotate provvisoriamente. Sono inoltre visualizzate anche nella scheda di pianificazione.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Come si modificano le ore richieste nonché le date di inizio e fine di una risorsa (generica o denominata) prenotata?

Dopo la prenotazione delle risorse, selezionare **Gestisci prenotazioni** per apportare le modifiche necessarie.

## <a name="what-resources-types-does-project-service-automation-support"></a>Quali sono i tipi di risorse supportati da Project Service Automation?

**Utente** e **Contatto** sono gli unici tipi di risorse supportati in Dynamics 365 Project Service Automation. Benché sia possibile creare altri tipi di risorse (ad esempio **Attrezzature** e **Gruppo**), nessuno caso d'uso end-to-end è supportato per tali risorse.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Qual è la differenza tra un'assegnazione e una prenotazione?

Le assegnazioni sono l'assegnazione di risorse alle attività di progetto nella pianificazione di progetto. Le risorse possono essere reali o generiche. Le prenotazioni sono l'allocazione provvisoria o definitiva delle risorse a un progetto. Le prenotazioni definitive consumano la capacità di una risorsa. Idealmente, per le risorse reali, prenotazioni e assegnazioni dovrebbero corrispondere in quanto non differiscono. Tuttavia, in PSA questa concordanza non è obbligatoria. La vista Riconciliazione mostra a un responsabile di progetto dove prenotazioni e assegnazioni non corrispondono.