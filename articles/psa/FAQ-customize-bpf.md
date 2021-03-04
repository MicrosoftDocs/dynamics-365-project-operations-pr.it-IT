---
title: Come si personalizza il processo aziendale Fasi del progetto?
description: Una panoramica su come personalizzare il processo aziendale Fasi del progetto.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d0168f187e6b0880713aac04bd87dbc2209197d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149008"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Come si personalizza il processo aziendale Fasi del progetto?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Le versioni precedenti dell'applicazione Project Service comportano un limite: i nomi delle fasi del processo aziendale Fasi del progetto devono corrispondere esattamente ai nomi inglesi previsti (**Quote**, **Plan**, **Close**). In caso contrario, le regole business, che si basano sui nomi di fase inglesi, non funzionano come previsto. Questo è il motivo per cui nel modulo di progetto non sono presenti azioni come **Cambia processo** o **Modifica processo** e la personalizzazione del processo aziendale non è incoraggiata. 

Questo limite è stato superato con la versione 2.4.5.48 e successive. Questo articolo fornisce soluzioni alternative nel caso sia necessario personalizzare il processo aziendale predefinito per le versioni precedenti.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Le regole business richiedono una corrispondenza esatta con i nomi di fase inglesi

Il processo aziendale Fasi del progetto include regole business che determinano i seguenti comportamenti nell'app:
- Quando il progetto è associato a un'offerta, il codice imposta il processo aziendale sulla fase **Quote**.
- Quando il progetto è associato a un contratto, il codice imposta il processo aziendale sulla fase **Plan**.
- Quando il processo aziendale è avanzato alla fase **Close**, il record del progetto viene disattivato. Quando il progetto viene disattivato, il modulo di progetto e la struttura di suddivisione del lavoro vengono impostati in sola lettura, le prenotazioni delle risorse con nome vengono rilasciate e tutti i listini prezzi associati vengono disattivati.

Le regole business sono basate sui nomi inglesi per le fasi di progetto. Questa dipendenza dai nomi di fase inglesi è il motivo principale per cui la personalizzazione del processo aziendale Fasi del progetto non è incoraggiata e per cui le azioni comuni del processo aziendale come **Cambia processo** o **Modifica processo** non sono presenti nell'entità di progetto.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Cosa succede se i nomi di fase non corrispondono ai nomi inglesi?

Nell'app Project Service versione 1.x sulla piattaforma 8.2, quando i nomi di fase nel processo aziendale non corrispondono esattamente ai nomi di fase inglesi, le regole business che impostano la fase appropriata per offerte o contratti o che chiudono il progetto sono ignorate. Non vengono visualizzati messaggi di errore. Di conseguenza, sembra possibile personalizzare il processo aziendale Fasi del progetto. Tuttavia, i processi automatici per offerte, contratti e la chiusura del progetto non saranno visibili.

Nell'app Project Service versione 2.4.4.30 o precedente sulla piattaforma 9.0, è stata introdotta un'importante modifica architetturale dei processi aziendali che ha necessitato la riscrittura delle regole business dei processi aziendali. Pertanto, se i nomi di fase di processo non corrispondono ai nomi inglesi previsti, non viene visualizzato alcun messaggio di errore. 

Quindi se si desidera personalizzare il processo aziendale Fasi del progetto per l'entità di progetto, è possibile soltanto aggiungere fasi completamente nuove al processo aziendale predefinito per tale entità, mantenendo nel contempo inalterate le fasi **Quote**, **Plan** e **Close**. Questa restrizione assicura che non si hanno errori inerenti alle regole business, le quali prevedono nomi di fasi inglesi nel processo aziendale.

Nella versione 2.4.5.48 o successive In una prossima versione, le regole business descritte in questo articolo sono state rimosse dal processo aziendale predefinito per l'entità di progetto. L'aggiornamento a quella versione o a una versione successiva consentirà la personalizzazione del processo aziendale predefinito o la sostituzione delle stesso con quello personale. 

## <a name="workarounds-for-earlier-versions"></a>Soluzioni per le versioni precedenti

Se l'aggiornamento non è possibile, è possibile personalizzare il processo aziendale Fasi del progetto per l'entità di progetto in uno dei due seguenti modi:

1. Aggiungere fasi supplementari alla configurazione predefinita, mantenendo nel contempo i nomi di fase inglesi per **Quote**, **Plan** e **Close**.


![Aggiunta di fasi alla configurazione predefinita](media/FAQ-Customize-BPF-1.png)
 
2. Creare il proprio processo aziendale e impostarlo come processo aziendale principale per l'entità di progetto, in modo da poter utilizzare i nomi di fase desiderati. Tuttavia, se si intende utilizzare le fasi di progetto standard **Quote**, **Plan** e **Close**, è necessario effettuare alcune modifiche. La logica più complessa è quella relativa alla chiusura del progetto, che è ancora possibile eseguire disattivando il record del progetto.

![Personalizzazione del flusso del processo aziendale](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Ulteriori considerazioni per l'app Project Service versione 2.4.4.30 o precedente sulla piattaforma 9.0

In Project Service 2.4.4.30 o versione precedente sulla piattaforma 9.0, con un processo aziendale personalizzato, il campo **Nome fase** nell'entità di progetto utilizzata nel grafico **Progetto per fase** e le viste dell'elenco di progetti non verranno aggiornati in quanto associati al processo aziendale Fasi del progetto predefinito. È possibile risolvere questo problema come segue:

- Aggiungere un campo personalizzato per acquisire la fase corrente del processo aziendale che viene aggiornata quando l'utente avanza nel processo aziendale personalizzato.

- Modificare il grafico **Progetto per fase** per utilizzare il campo personalizzato anziché la configurazione predefinita.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Procedura per creare un processo aziendale personalizzato per l'entità di progetto

Per creare un processo aziendale personalizzato per l'entità di progetto, procedere come segue:

1. Andare a **Impostazioni** > **Centro processi**. Non copiare il processo aziendale Fasi del progetto in quanto vengono copiate anche le regole business di Project Service.

  ![Creare processi](media/FAQ-Customize-BPF-3.png)

2. Utilizzare lo strumento di progettazione dei processi per creare i nomi di fase desiderati. Se si desidera la stessa funzionalità delle fasi predefinite **Quote**, **Plan** e **Close**, è necessario crearla in base ai nomi di fase del processo aziendale personalizzato.

   ![Strumento di progettazione dei processi utilizzato per personalizzare il processo aziendale](media/FAQ-Customize-BPF-4.png) 

3. Nello strumento di progettazione dei processi, fare clic su **Flusso di elaborazione ordine** e spostare il processo aziendale personalizzato sopra il processo aziendale Fasi del progetto affinché sia il processo aziendale principale.


   [Utilizzo di Flusso di elaborazione ordine](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>La procedura seguente si applica all'app Project Service 2.4.4.30 o versione precedente sulla piattaforma 9.0

4. Aggiungere un nuovo campo personalizzato all'entità di progetto per acquisire le fasi personalizzate nel processo aziendale personalizzato. Sarà necessario aggiungere delle regole business (plug-in/flusso di lavoro) per aggiornare questo campo quando la fase del processo aziendale personalizzato viene aggiornata.

   ![Personalizzazione dell'entità di progetto](media/FAQ-Customize-BPF-6-720.png)

5. Modificare il grafico **Progetto per fase** per utilizzare il nuovo campo personalizzato per le fasi.

   ![Utilizzo del grafico Progetto per fase](media/FAQ-Customize-BPF-7-720.png)

6. Modificare tutte le viste per l'entità di progetto per includere il campo personalizzato per le fasi.

   ![Modifica delle viste nell'entità di progetto](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]