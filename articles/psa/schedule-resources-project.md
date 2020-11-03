---
title: Pianificare risorse per un progetto
description: Come pianificare le risorse per un progetto in Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079082"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Pianificare le risorse per un progetto (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Puoi verificare la disponibilità di una risorsa per ottenere una visione globale di come sono prenotate le risorse, oppure puoi filtrare la in base alle competenze, il team, la posizione e altre opzioni.  
  
Nella scheda di pianificazione sono visualizzati l'elenco di risorse e le relative disponibilità. Seleziona la modalità di visualizzazione per vedere la disponibilità in base a **Ore** , **Giorno** , **Settimana** o **Mese**.  
  
Prima di utilizzare la scheda di pianificazione, è importante configurarla. Per ulteriori informazioni, vedi [Configurare la scheda di pianificazione (Field Service, Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Se utilizzi una versione precedente, per la disponibilità delle risorse, vedi [Visualizzare la disponibilità delle risorse](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Per utilizzare la funzionalità di prenotazione della scheda di pianificazione, la geocodifica e i servizi di localizzazione, è necessario abilitare le mappe.  
> 
> 1. Nel menu principale seleziona **Pianificazione risorse** > **Amministrazione**.  
> 2. Fai clic su **Parametri di pianificazione**.  
> 3. Apri il record e scorri verso il basso fino alla sezione **Resource Scheduling Optimization**.  
> 4. Nel campo **Connetti a Mappe** scegli **Sì**.  
> 5. Accettare le condizioni e salvare il record.  
> 6. Nel menu principale seleziona **Project Service** > **Scheda di pianificazione**. Da qui, esistono diversi modi per pianificare manualmente un requisito di prenotazione. Seleziona il metodo più adatto per te.
  
## <a name="find-available-resources"></a>Trovare le risorse disponibili

1.  Nell'elenco **Requisiti di prenotazione** fai clic con il pulsante destro del mouse sulla prenotazione non pianificata e scegli una delle operazioni seguenti:  
  
- Scegli **Trova disponibilità - risorse correnti** per individuare una risorsa disponibile nell'elenco nella scheda di pianificazione.  
- Scegli **Trova disponibilità - Tutte le risorse** per individuare una risorsa disponibile nelle risorse del sistema  
   > [!NOTE]
   >  Se esegui tale operazione, i filtri mostreranno le opzioni per il requisito di prenotazione selezionato.  
  
2. Quando viene visualizzato uno slot disponibile, fai clic con il pulsante destro del mouse sull'intervallo di tempo nella scheda di pianificazione e scegli **Prenota qui**. In alternativa, trascina e rilascia il requisito della prenotazione sull'intervallo di tempo disponibile.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Prenota una risorsa mediante la visualizzazione giornaliera e trova chi è prenotato sotto la disponibilità
  
1.  Nella scheda di pianificazione seleziona **Modalità di visualizzazione** , quindi **Giorni**.  
  
    Questo diagramma illustra la visualizzazione griglia del numero di ore che una risorsa è prenotata al giorno e i quali giorni sono liberi.  
  
2.  Fai clic sul nome della risorsa che desideri prenotare, quindi seleziona **Prenota**.  
  
3.  Nella finestra dialogo **Crea prenotazione risorsa** scegli il progetto per cui desideri prenotare la risorsa con il metodo di prenotazione e gli orari di inizio e fine.  
  
4.  Al termine, seleziona **Prenota**.  
  
## <a name="view-to-the-schedule-board"></a>Visualizzare la scheda di pianificazione
  
1.  Seleziona un requisito di pianificazione non pianificato nell'elenco nella parte inferiore.  
  
2.  Trascina il requisito di prenotazione in una risorsa/intervallo di tempo disponibile nella scheda di pianificazione.  
  
3.  Al termine, seleziona **Prenota**.  
  
### <a name="additional-resources"></a>Risorse aggiuntive  
 [Guida di Resource Manager](../psa/resource-manager-guide.md)
