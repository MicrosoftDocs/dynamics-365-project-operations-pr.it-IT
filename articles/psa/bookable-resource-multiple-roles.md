---
title: Stimare le vendite e i costi del progetto quando una risorsa prenotabile ricopre più ruoli per un progetto
description: Questo articolo spiega come utilizzare le dimensioni dei prezzi per supportare la determinazione di prezzi e di costi per una risorsa che ricopre più ruoli in un progetto.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5adaa7b83aae69c15aa268e723417172f1b56f42
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916155"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Stimare le vendite e i costi del progetto quando una risorsa prenotabile ricopre più ruoli per un progetto 

[!include [banner](../includes/psa-now-project-operations.md)]

Le aziende basate su progetti hanno spesso la necessità di una risorsa che esegua più ruoli in un progetto. Ognuno di questi ruoli potrebbe avere un prezzo e un costo diverso, il che significa che il tempo della stessa risorsa sul progetto potrebbe ottenere una stima finanziaria diversa a seconda del costo e delle tariffe per ciascuno dei ruoli. Project Service Automation consente l'impostazione dei valori nel record del membro del team per la risorsa denominata e consente sostituzioni diverse su ciascuna delle attività a cui è assegnato il membro del team.

L'esempio seguente spiega come la semplice sostituzione di questo valore consenta a una risorsa di avere più ruoli in un progetto con costi e tariffe di fatturazione differenti.

## <a name="create-tasks"></a>Creare attività
Crea due attività di progetto per 40 ore ciascuna, Attività A e Attività B. Seleziona Attività A come predecessore dell'Attività B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Impostazione di ruolo e unità organizzativa per un membro del team di progetto generico

1. Nella pagina **Pianifica** seleziona la riga **Attività** per l'attività A. 
2. Nel campo **Risorse** seleziona **Crea** nel menu a discesa.
3. Nella pagina **Creazione rapida dei membri del team** specifica gli attributi del membro del team generico che può eseguire questa attività.
4. Seleziona il ruolo e l'unità organizzativa appropriati, quindi seleziona **Salva e chiudi**. Un membro del team generico viene creato e assegnato a questa attività. 

Ripeti questi passaggi per l'attività B e assicurati che il ruolo e l'unità organizzativa del membro del team generico creato per l'attività B sia diverso dall'attività A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Impostazione di ruolo e unità organizzativa per un'attività di progetto

1. Dopo aver creato l'attività A, seleziona l'attività e quindi seleziona **Modifica attività**.
2. Nella pagina **Dettagli attività** trova i campi **Ruolo** e **Unità organizzativa**, aggiungi i valori di una risorsa che eseguirà questa attività. 

  > [!NOTE]
  > Se stai completando questi scenari utilizzando i dati demo di Project Service Automation, seleziona **Consulting Lead** per il ruolo e **Fabrikam US** come unità organizzativa.

3. Seleziona l'attività B, quindi seleziona **Modifica attività**.
4. Nella pagina **Dettagli attività** trova i campi **Ruolo** e **Unità organizzativa**, aggiungi i valori di una risorsa che eseguirà questa attività. Assicurati che i valori nei campi **Ruolo** e **Unità organizzativa** per l'attività B siano diversi dai valori per l'attività A. 

  > [!NOTE]
  > Se stai completando questi scenari utilizzando i dati demo di Project Service Automation, seleziona **Network Technician** per il ruolo e **Fabrikam US** come unità organizzativa.

5. Salva e chiudi la pagina **Dettagli attività**. 

## <a name="team-member-and-estimates-behavior"></a>Membro del team e stima del comportamento 

1. Nella pagina **Dettagli attività** seleziona in **Membro del team** i due membri del team generici e quindi seleziona **Genera requisiti**. 
2. Seleziona la riga del membro del team per **Consulting Lead** e poi seleziona **Prenota**. Viene visualizzata la scheda di pianificazione e viene prenotata una risorsa per quel requisito.
3. Seleziona la riga del membro del team per **Network Technician** e poi seleziona **Prenota**. Viene visualizzata la scheda di pianificazione e viene prenotata la stessa risorsa per quel requisito.

### <a name="team-member-grid"></a>Griglia del membro del team 
Nella griglia **Membro del team** nota che i due record dei membri del team generici sono stati eliminati e sostituiti da una risorsa. Esiste un set di valori per quella risorsa che mostra un set di valori predefinito per **Ruolo** e **Unità organizzativa**.
Quando espandi la riga del record del membro del team puoi visualizzare assegnazioni distinte del record del membro del team per entrambe le attività. Ogni riga di assegnazione ha valori specifici dell'attività per **Ruolo** e **Unità organizzativa**. 

### <a name="estimates-grid"></a>Griglia delle stime 
Quando passi alla griglia **Stime** puoi notare che entrambe le assegnazioni per la stessa risorsa hanno un prezzo diverso.
Il prezzo dell'assegnazione per la risorsa nell'attività A viene calcolato utilizzando il valore dell'attributo **Ruolo** di **Consulting Lead**. Il prezzo dell'assegnazione per la stessa risorsa nell'attività B viene calcolato utilizzando il valore dell'attributo **Ruolo** di **Network Technician**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
