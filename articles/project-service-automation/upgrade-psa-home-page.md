---
title: Home page degli aggiornamenti
description: In questo argomento viene indicato dove trovare informazioni importanti sulle funzionalità nuove e modificate di Dynamics 365 Project Service Automation nonché la procedura per eseguire l'aggiornamento alla versione più recente.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752681"
---
# <a name="upgrade-home-page"></a>Home page degli aggiornamenti

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Aggiornamento da PSA versione 2.x o 1.x alla versione 3.x

### <a name="new-instances"></a>Nuove istanze

A partire dal 17 maggio 2019, quando Project Service Automation viene selezionato durante il provisioning di una nuova istanza, la versione 3.x viene installata per impostazione predefinita.

### <a name="existing-instances"></a>Istanze esistenti

In precedenza, i clienti con un'istanza di PSA versione 2.x che dovevano eseguire l'aggiornamento alla versione 3.x, ovvero la versione basata sull'interfaccia client unificata di PSA, dovevano contattare il supporto tecnico Microsoft e fornire i dettagli relativi all'istanza di modo che fosse possibile abilitare l'istanza per l'aggiornamento alla versione 3.x. A partire dal 1 ° marzo 2020, i clienti con un'istanza di PSA versione 2.x che devono eseguire l'aggiornamento alla versione 3.x, saranno in grado di aggiornare le proprie istanze direttamente dal portale di amministrazione senza contattare il supporto tecnico Microsoft.  

> [!NOTE]
> PSA versione 3.x include modifiche importanti. È basata sul framework Unified Interface per offrire un'esperienza utente migliorata. L'app riprogettata fornisce un'interfaccia utente coerente e uniforme e segue i principi di progettazione interattiva per la visualizzazione ottimale su uno schermo o dispositivo di qualsiasi dimensione. Altre modifiche sono state apportate all'applicazione. Alcune delle aree che sono state modificate sono quelle relative a determinazione dei prezzi, prenotazione e assegnazione di risorse, tempo, spese e approvazioni.

Prima di iniziare la procedura di aggiornamento, ti consigliamo di completare le seguenti operazioni:

- Verifica se Dynamics 365 Field Service e Project Service Automation sono entrambi installati nell'istanza identificata. Se entrambe le soluzioni sono installate, devi pianificarne l'aggiornamento prima di ricominciare a utilizzare regolarmente l'istanza.
- Leggi attentamente gli argomenti seguenti. La conoscenza e la comprensione delle modifiche tra le diverse versioni renderanno più agevole la procedura di aggiornamento. Questi argomenti forniscono informazioni sulle principali modifiche in PSA, nonché considerazioni e suggerimenti per la pianificazione dell'aggiornamento alla versione 3.x.

    - [Novità o modifiche in Project Service Automation versione 3](whats-new-changed-v3.md)
    - [Considerazioni sull'aggiornamento - Da Project Service Automation versione 2.x o 1.x alla versione 3.x](upgrade-v3.md)

- Aggiorna la tua istanza sandbox per valutare le modifiche nell'implementazione prima di eseguire l'aggiornamento dell'istanza di produzione.

Dopo aver letto gli argomenti indicati sopra e quando sei pronto ad eseguire l'aggiornamento a PSA versione 3.x o alla versione basata su UCI, invia una richiesta al supporto tecnico Microsoft per rendere l'aggiornamento disponibile nell'interfaccia di amministrazione. Nella richiesta, fornisci i dettagli sull'istanza.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Versioni precedenti di PSA (PSA versione 2.x) in un'istanza appena creata

A partire dal 17 maggio 2019, tutte le nuove istanze hanno UCI come client predefinito. Per l'allineamento a questa modifica, il provisioning di PSA versione 3.x e Field Service versione 8.x viene eseguito per impostazione predefinita, in quanto tali versioni sono progettate per l'utilizzo con il client UCI.

A partire dal 1° marzo 2020, i clienti di Dynamics PSA non saranno più in grado di creare nuovi ambienti con versioni precedenti di PSA, ad esempio PSA versione 2.x o precedente. Qualsiasi nuovo ambiente supporterà solo la versione 3.x di PSA.

> [!NOTE]
> Per la migliore esperienza quando utilizzi versioni precedenti delle applicazioni Field Service e PSA, vai alla pagina **Impostazioni di sistema** e imposta il campo **Utilizza solo la nuova Unified Interface (scelta consigliata)** su **No** in quanto queste versioni non sono progettate per essere caricate correttamente in UCI. Dopo aver disattivato UCI, puoi aprire ed eseguire queste versioni di Field Service e PSA utilizzando il client Web precedente. Per istruzioni su come disabilitare il client UCI, vedi [Abilitare solo Unified Interface](../admin/enable-unified-interface-only.md).
