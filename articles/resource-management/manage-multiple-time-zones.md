---
title: Gestire i fusi orario
description: Quando viene creato un progetto, il fuso orario si basa sul fuso orario definito nel modello di ore lavorative applicato.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c3feb05e1b2e81add1b0df886a5a69ced229eb72
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578529"
---
# <a name="manage-time-zones"></a>Gestire i fusi orario

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


## <a name="projects"></a>Progetti

Quando viene creato un progetto, il fuso orario si basa sul fuso orario definito nel modello di ore lavorative applicato. Sul modulo **Progetto**, le date sono sempre relative al fuso orario dell'utente che ha effettuato l'accesso a ciascuna scheda, ad eccezione della scheda **Attività**. Quando visualizzi la struttura di suddivisione del lavoro, le date verranno sempre visualizzate nel fuso orario del progetto.

## <a name="tasks"></a>Attività

Quando viene creata un'attività, l'ora di inizio, l'ora di fine e le ore/giorno sono controllate dalle ore lavorative del progetto. Ad esempio, se un'attività viene creata con un progetto il cui fuso orario è -8 PST e ha le seguenti ore lavorative: dalle 9:00 alle 17:00 dal lunedì al venerdì, qualsiasi attività creata senza un'assegnazione rispetterà l'ora di inizio e l'ora di fine del calendario del progetto.

## <a name="manage-resources-with-time-zones"></a>Gestire le risorse con i fusi orari

Per risultati accurati e prevedibili durante l'utilizzo di **Estendi prenotazione**, ci sono due prerequisiti chiave che devono essere soddisfatti:  

- L'utente deve configurare il fuso orario del proprio dispositivo in modo che corrisponda al fuso orario definito nelle **Impostazioni di personalizzazione** del sistema.
 
  ![Impostazioni di fuso orario in Windows 10.](media/reconcile-assignments-03.png)

  ![Impostazioni di fuso orario nelle impostazioni di personalizzazione.](media/reconcile-assignments-04.png)
 
- La risorsa prenotabile deve avere almeno un minuto di orario di lavoro che si sovrappone ai profili utilizzati per definire l'estensione richiesta. Ad esempio, le seguenti risorse con orari di lavoro compresi tra le 9:00 e le 19:00. 

  ![Confronto dei profili delle risorse.](media/reconcile-assignments-05.png)

La tabella seguente mostra:

- Un modello di calendario di progetto
- Risorsa A: questa risorsa ha lo stesso calendario ed è nello stesso fuso orario del progetto. L'ora di inizio delle prenotazioni sarà alle 9:00.
- Risorsa B: questa risorsa si trova in un fuso orario diverso da quello del progetto e inizia alle 7:00 del suo fuso orario. Tuttavia, le prenotazioni inizieranno alle 9:00 in quanto è il primo orario di inizio del profilo dell'assegnazione.
- Risorse C e D: le risorse si trovano in fusi orari diversi, sia diversi l'uno dall'altro che dal progetto, e le loro prenotazioni iniziano non prima dei rispettivi orari di inizio disponibili.

|Entity  |Calendari  |
|-|-|
|Modello di calendario di progetto   | ![calendario di progetto.](media/reconcile-assignments-06.png) |
|Risorsa A  | ![Calendario della risorsa A.](media/reconcile-assignments-06.png) |
|Risorsa B  |  ![Calendario della risorsa B.](media/reconcile-assignments-07.png) |
|Risorsa C  |  ![Calendario della risorsa C.](media/reconcile-assignments-08.png) |
|Risorsa D  | ![Calendario della risorsa D.](media/reconcile-assignments-09.png)  |
 
Quando ti sposti nella vista **Riconciliazione**, vengono visualizzate le assegnazioni di risorse e le relative prenotazioni insufficienti.

![Visualizzazione di riconciliazione prima dell'estensione.](media/reconcile-assignments-10.png)

Dopo che la funzionalità di estensione della prenotazione è stata utilizzata per ciascuna risorsa, le prenotazioni vengono estese per ogni risorsa perché le ore lavorative di ciascuna risorsa si sovrappongono ai profili dell'insufficienza.

![Visualizzazione di riconciliazione dopo l'estensione della prenotazione.](media/reconcile-assignments-11.png) 

Tieni presente che esaminando attentamente i dettagli delle prenotazioni puoi visualizzare le differenze nell'orario di inizio delle prenotazioni. Le prenotazioni iniziano non prima dell'ora di inizio del profilo di assegnazione e non prima dell'ora di inizio disponibile della risorsa.

![Nuove prenotazioni delle risorse nella scheda di pianificazione.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]