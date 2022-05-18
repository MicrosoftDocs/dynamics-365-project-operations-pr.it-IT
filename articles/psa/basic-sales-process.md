---
title: Processi di vendita
description: In questo argomento vengono fornite informazioni sui processi di vendita di base.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bec8718e287500a7cbc778dc32758e793be8dc3b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580323"
---
# <a name="sales-processes"></a>Processi di vendita

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I processi di vendita utilizzati in un'organizzazione basata su progetto differiscono dai processi di vendita utilizzati in un'organizzazione basata su prodotto. Questa differenza si ha in quanto i cicli di vendita per le organizzazioni basate su progetto sono più lunghi e richiedono tecniche di stima personalizzate per analizzare e creare offerte per ogni transazione. Dynamics 365 Project Service Automation utilizza alcune delle funzionalità utilizzate nel processo di vendita per Dynamics 365 Sales. Di seguito sono riportati alcuni esempi.

- Un'entità Lead è utilizzata per tenere traccia del processo di vendita.
- I lead potenziali sono registrati come opportunità. Il processo di vendita può anche iniziare con un'opportunità.
- Si ha accesso a tutti gli elementi correlati di un'opportunità. Questi elementi includono team di vendita, parti interessate, probabilità, valutazioni, fasi di vendita e processi aziendali.
- Molteplici offerte vengono create per un'opportunità.
- Un'offerta è contrassegnata con **Chiusa come acquisita** per creare un ordine di vendita. In PSA, l'ordine di vendita viene personalizzato e denominato contratto di progetto.

Nella figura seguente viene illustrato un processo di vendita tipico in un'organizzazione basata su progetto.

> ![Processo di vendita in un'organizzazione basata su progetto.](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Stima di una vendita
Il valore di una vendita può essere stimato in base a progetti completati precedentemente e alla complessità degli stessi. Per i progetti che comportano estensioni a progetti precedenti, o progetti dove l'esperienza del fornitore è alta e si utilizzano modelli di lavoro noti, puoi utilizzare un processo di stima più semplice. I progetti più complessi hanno in genere un processo di acquisto più lungo. Pertanto, vi sono più fasi nel processo di stima di vendite. All'inizio del processo, il team di vendita utilizza l'input di account manager ed esperti in materia per iniziare a creare una stima di alto livello per ogni componente distinto del lavoro richiesto. Questi componenti di lavoro sono rappresentati da righe di offerta. 

Puoi creare una stima generale dell'offerta. Questa stima sarà successivamente sostituita da una stima più dettagliata basata su un piano di progetto che crei utilizzando i modelli di progetto standardizzati. Tali modelli consentono di creare una pianificazione e determinare i valori monetari dell'offerta e i relativi componenti (righe di offerta). 

Puoi creare molteplici offerte per un progetto e raggrupparle in un unico tipo di entità Opportunità. Una di queste offerte viene quindi contrassegnata con **Chiusa come acquisita** e viene creato un contratto di progetto o una descrizione dei lavori. Un contratto di progetto specifica il valore stabilito di ogni componente (voce di contratto) accettato dal cliente per la consegna. Viene creata anche una descrizione dei lavori come documento Microsoft Word. Tutte le fatture inviate al cliente nel corso dell'esecuzione del progetto fanno riferimento al contratto di progetto o alla descrizione dei lavori.

Puoi anche creare offerte alternative in un tipo di entità Opportunità o configurare il sistema di modo che un contratto di progetto sia creato quando si acquisisce un'offerta. In questo caso, puoi allegare un documento di Word che rappresenta la descrizione dei lavori al record del contratto di progetto.

![Chiudere un'offerta per creare un contratto di progetto.](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Configurare il processo di vendita
Puoi utilizzare i processi aziendali in Microsoft Dynamics 365 per configurare il processo di vendita. I processi aziendali forniscono al personale di vendita un interfaccia visiva guidata che possono utilizzare per spostare le transazioni nelle fasi successive tipiche della propria azienda.

Ad esempio, la tua azienda potrebbe includere le sei fasi seguenti nel processo di vendita:

1. Impostazione come qualificato
2. Stima
3. Verifica interna
4. Contratto
5. Consegna
6. Chiusura

Queste sei fasi sono rappresentate da frecce di espansione (\>) che selezioni per espandere ogni tipo di entità Opportunità creata.

![Configurazione del processo aziendale in Dynamics 365.](media/basic-guide-3.png)
 
La tua organizzazione potrebbe utilizzare entità differenti per rappresentare la stessa transazione durante l'evoluzione della stessa. All'inizio del processo di vendita, una transazione è rappresentata dall'entità Opportunità. Con il passare del tempo e quando emergono nuovi dettagli, potresti utilizzare stime generali per creare una o più offerte. Se una di queste offerte viene esaminata dalle parti interessate interne e dei clienti, l'entità Offerta rappresenta la transazione. Dopo l'accettazione dell'offerta da parte del cliente, un contratto di progetto o una descrizione dei lavori rappresenta la transazione. Per supportare questo comportamento, i processi aziendali sono strutturati di modo che ogni fase del processo sia collegata a una tabella di database differente.

La fase **Imposta come qualificato** del processo di vendita può essere supportata da un'entità Opportunità. Le fasi **Stima** e **Verifica interna** possono essere supportate da un'entità Offerta. Le fasi **Contratto**, **Consegna** e **Chiusura** possono essere supportate da un'entità Contratto di progetto.

Durante lo spostamento delle transazioni da una fase all'altra, ti viene richiesto di creare un record di entità appropriato per guidarti durante il processo. Le fasi possono essere condizionali. Ad esempio, se richiedi una verifica interna di un'offerta solo se l'offerta utilizza un listino prezzi personalizzato, puoi configurare tale condizione nella fase appropriata del processo aziendale. La fase **Verifica interna** viene quindi visualizzata solo per le offerte che utilizzano un listino prezzi personalizzato. Per tutte le altre transazioni e offerte, la fase **Stima** è seguita dalla fase **Contratto**.

> [!NOTE]
> PSA include pagine specifiche per le entità Opportunità, Offerta, Ordine e Fattura. Devi creare opportunità, offerte, ordini e fatture di Project Service utilizzando le pagine di informazioni di progetto per queste entità. Se utilizzi un'altra pagina per creare un record, non potrai aprire il record dalla pagina **Informazioni sul progetto**. Se desideri aprire un record dalla pagina **Informazioni sul progetto**, devi eliminare il record e ricrearlo utilizzando la pagina **Informazioni di progetto**. Nella pagina **Informazioni di progetto**, la logica di business di ognuna di queste entità assicura la corretta impostazione del campo **Tipo** del record e la corretta inizializzazione di tutti i concetti obbligatori.

> ![Informazioni sul progetto per un nuovo ordine.](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Differenze tra Project Service Automation e Sales
Sebbene il processo di vendita in PSA utilizzi le funzionalità di base del processo di vendita in Sales, vi sono alcune differenze a causa delle variazioni nelle procedure aziendali delle organizzazioni basate su progetto. Di seguito sono riportati alcuni esempi.

- **Offerte di progetto** - In Project Service Automation, un'offerta viene chiusa dopo la creazione di un contratto di progetto da un'offerta. In Sales, puoi mantenere un'offerta aperta dopo averla acquisita. Il motivo di questa differenza è che una corrispondenza tra un'offerta e un contratto di progetto è migliore per le organizzazioni basate su progetto. 
- **Attivazione e revisioni** - In PSA l'attivazione e gli aggiornamenti non sono supportati per le offerte di progetto. In Sales, un'offerta può essere bloccata per impedire ulteriori modifiche.
- **Chiudere un'offerta come acquisita o persa** - In PSA, quando un'offerta di progetto viene chiusa come acquisita o persa, l'opportunità rimane aperta. Tutte le altre offerte dell'opportunità vengono chiuse come perse. In Sales, quando un'offerta viene chiusa come acquisita o persa, all'utente viene richiesto di intraprendere un'azione in relazione all'opportunità. A seconda dell'input dell'utente, l'opportunità sottostante può essere chiusa o lasciata aperta.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Tenere traccia delle revisioni di offerte e piani di progetto nel ciclo di vendita
In PSA, puoi tenere traccia delle revisioni di un'offerta. Devi invece contrassegnare l'offerta esistente come **Chiusa come persa** e quindi creare una nuova offerta. Puoi copiare un'offerta o clonare un'offerta basata su progetto utilizzando PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Tenere traccia di commenti e approvazioni di offerte e contratti di progetto
Puoi gestire la revisione e l'approvazione di offerte e contratti di progetto mediante la bacheca record e i post. L'organizzazione può creare plug-in e flussi di lavoro personalizzati per assegnare, reindirizzare, riassegnare e gestire notifiche relative alla revisione e all'approvazione di elementi di lavoro.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
