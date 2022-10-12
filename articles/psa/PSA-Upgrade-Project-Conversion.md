---
title: Modifiche della funzionalità per Project Service Automation in Project Operations
description: Questo articolo fornisce una panoramica delle modifiche alla funzionalità per Microsoft Dynamics 365 Project Service Automation in Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621238"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Modifiche della funzionalità per Project Service Automation in Project Operations

Dopo aver aggiornato correttamente un progetto da Microsoft Dynamics 365 Project Service Automation 3.X a Dynamics 365 Project Operations Lite, la modifica delle attività del progetto nella struttura di suddivisione del lavoro (WBS) della griglia delle attività non è possibile. I clienti potranno esaminare le WBS nella griglia di monitoraggio in cui sono stati aggiunti nuovi campi per fornire tutti i dettagli relativi all'attività. Per i progetti in cui sono necessarie modifiche alla WBS, puoi convertire selettivamente i progetti idonei nella nuova esperienza di pianificazione Project for the Web.

## <a name="project-conversion-process"></a>Processo di conversione di un progetto

Segui questi passaggi per convertire un progetto.

1. Apri la pagina principale del progetto e seleziona **Converti** nel riquadro Azioni.
1. Nella finestra del messaggio di conferma, seleziona **OK** per avviare la conversione del progetto. Si verifica quanto segue:

    1. Viene visualizzata una barra dei messaggi nella pagina principale del progetto con l'indicazione "È in corso la conversione della pianificazione del progetto. Non è possibile apportare modifiche al progetto fino al completamento della conversione."
    1. Verrai reindirizzato all'elenco dei progetti.

    Una volta completata la conversione del progetto, si verificano le seguenti azioni:

    1. Il project manager assegnato riceve una notifica sul lato destro dell'applicazione.
    1. La barra dei messaggi che indica che la conversione è in corso viene rimossa.
    1. La scheda **Pianificazione** mostra la nuova esperienza di pianificazione con Project for the Web. Qualsiasi utente che dispone delle licenze e dei ruoli di sicurezza appropriati può modificare la WBS.
    1. Il campo **Motore di programmazione** viene aggiornato a **Project for the Web**.
    1. Il pulsante **Converti** viene rimosso dal riquadro Azioni.

> [!IMPORTANT]
> Non è consentita la conversione in blocco dei progetti. Qualsiasi tentativo di aggiornare un grande volume di progetti contemporaneamente verrà limitato. Questa limitazione aiuta a garantire prestazioni elevate per tutti i clienti.

## <a name="manual-tasks-vs-automatic-tasks"></a>Attività manuali e attività automatiche

Quando un ambiente viene aggiornato da Project Service Automation a Project Operations, tutte le attività nella WBS vengono considerate automaticamente pianificate. Il concetto di attività pianificate manualmente non è disponibile in Project for the Web. Tuttavia, puoi definire il comportamento di pianificazione preferito per i tuoi progetti utilizzando l'impostazione della [modalità di pianificazione](/project-management/scheduling-modes.md) quando crei nuovi progetti.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operazioni con restrizioni per progetti di pre-conversione

Questa sezione delinea le differenze funzionali che puoi aspettarti quando i progetti non sono stati convertiti.

### <a name="copy-project"></a>Copia del progetto

L'operazione **Copia** è supportata solo sui progetti convertiti. I progetti aggiornati non possono essere copiati prima della conversione.

### <a name="move-project"></a>Spostamento del progetto

Una modifica alla data di inizio di un progetto non sposterà proporzionalmente l'inizio delle attività a meno che il progetto non sia stato convertito.

## <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Quali sono le differenze tra i progetti convertiti e i nuovi progetti creati dopo il completamento dell'aggiornamento?

Per i progetti convertiti dopo l'aggiornamento dell'ambiente, verrà impostato un flag che indica alla pianificazione di rispettare solo il calendario del progetto. Questo comportamento corrisponde al comportamento in Project Service Automation. Tuttavia, il flag non verrà impostato per i nuovi progetti creati dopo l'aggiornamento. Pertanto, la pianificazione rispetterà l'orario di lavoro delle risorse quando vengono assegnate a un'attività.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Cosa devo fare se il mio progetto non viene convertito?

Se il tuo progetto non viene convertito, il primo passaggio consiste nell'esaminare i registri degli errori per identificare eventuali problemi comuni correlati alla tua WBS. Se i registri non indicano un errore specifico su cui puoi intervenire, contatta l'assistenza clienti in modo che il tuo caso possa essere esaminato ulteriormente.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Come vengono gestite le chiusure di attività in Project for the Web?

Project for the Web non rispetta le chiusure di attività che l'impresa definisce a livello di organizzazione. Tuttavia, rispetterà altri tipi di giorni liberi definiti in un determinato modello di orario di lavoro.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Quali sono le limitazioni di Project for the Web?

Vedi [Creare una struttura di suddivisione del lavoro: limitazioni del progetto](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Posso aspettarmi modifiche alle mie stime di costi e vendite?

In rari casi in cui i profili di assegnazione delle risorse vengono ricalcolati oppure rientrano in un limite di data diverso rispetto al progetto di origine, potresti notare delle differenze nelle stime di vendita e dei costi. Come parte del processo di aggiornamento, i clienti devono testare un insieme rappresentativo di progetti campione, in modo che possano comprendere eventuali modifiche alla pianificazione.
