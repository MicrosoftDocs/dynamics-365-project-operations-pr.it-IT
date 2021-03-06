---
title: Panoramica dei processi di vendita
description: In questo argomento vengono fornite informazioni sui processi di vendita di base.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: e66d96a940f3b22d5d1f3372d2b6767a4482d925
ms.sourcegitcommit: 7750485f8685a2ca5e1b3c165ead24a3b583c447
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3891580"
---
# <a name="sales-processes-overview"></a>Panoramica dei processi di vendita

I processi di vendita utilizzati in un'organizzazione basata su progetto differiscono dai processi di vendita utilizzati in un'organizzazione basata su prodotto. Questo perché i cicli di vendita per le organizzazioni basate su progetto sono più lunghi e richiedono tecniche di stima personalizzate per analizzare e creare offerte per ogni transazione. Dynamics 365 Project Operations utilizza alcune delle seguenti funzionalità utilizzate in un processo di vendita:

- Un record Lead è utilizzato per tenere traccia del processo di vendita.
- I lead potenziali sono registrati come opportunità.
- Tutti gli elementi correlati di un'opportunità sono accessibili. Questi elementi includono team di vendita, parti interessate, probabilità, valutazioni, fasi di vendita e processi aziendali.
- Molteplici offerte vengono create per un'opportunità.
- Un'offerta è contrassegnata con lo stato **Chiusa come acquisita** per creare un ordine di vendita. In Project Operations, l'ordine di vendita viene personalizzato e denominato contratto di progetto.

## <a name="estimate-a-sale"></a>Stimare una vendita
Il valore di una vendita può essere stimato in base a progetti completati precedentemente e alla complessità degli stessi. Per i progetti che comportano estensioni a progetti precedenti, o progetti dove l'esperienza del fornitore è alta e si utilizzano modelli di lavoro noti, puoi utilizzare un processo di stima più semplice. I progetti più complessi hanno in genere un processo di acquisto più lungo. Pertanto, vi sono più fasi nel processo di stima di vendite. All'inizio del processo, il team di vendita utilizza l'input di account manager ed esperti in materia per creare una stima di alto livello per ogni componente distinto del lavoro richiesto. Questi componenti di lavoro sono rappresentati da righe di offerta. 

Puoi creare una stima generale dell'offerta. Questa stima sarà successivamente sostituita da una stima più dettagliata basata su un piano di progetto che crei utilizzando i modelli di progetto standardizzati. Tali modelli consentono di creare una pianificazione e determinare i valori monetari dell'offerta e i relativi componenti (righe di offerta). 

Puoi creare molteplici offerte per un progetto e raggrupparle in un unico record opportunità. Una delle offerte viene quindi contrassegnata con **Chiusa come acquisita** e viene creato un contratto di progetto o una descrizione dei lavori. Un contratto di progetto specifica il valore stabilito di ogni componente (voce di contratto) accettato dal cliente per la consegna. Viene creata anche una descrizione dei lavori come documento Microsoft Word. Tutte le fatture inviate al cliente nel corso dell'esecuzione del progetto fanno riferimento al contratto di progetto o alla descrizione dei lavori.

Puoi anche creare offerte alternative in un record opportunità o configurare il sistema di modo che un contratto di progetto sia creato quando si acquisisce un'offerta. In questo caso, puoi allegare un documento di Word che rappresenta la descrizione dei lavori al record del contratto di progetto.

## <a name="configure-the-sales-process"></a>Configurare il processo di vendita
Puoi utilizzare i flussi di processi aziendali per configurare il processo di vendita. Questi flussi forniscono un'interfaccia visiva guidata per far avanzare le trattative nelle fasi del processo di vendita.

Ad esempio, la tua azienda potrebbe includere le sei fasi seguenti nel processo di vendita:

1. Impostazione come qualificato
2. Stima
3. Verifica interna
4. Contratto
5. Consegna
6. Chiuso
 
La tua organizzazione potrebbe utilizzare entità differenti per rappresentare la stessa transazione durante l'evoluzione della stessa. All'inizio del processo di vendita, una transazione è rappresentata dall'entità Opportunità. Con il passare del tempo e quando emergono nuovi dettagli, potresti utilizzare stime generali per creare una o più offerte. Se una di queste offerte viene esaminata dalle parti interessate interne e dei clienti, l'entità Offerta rappresenta la transazione. Dopo l'accettazione dell'offerta da parte del cliente, un contratto di progetto o una descrizione dei lavori rappresenta la transazione. Per supportare questo comportamento, i processi aziendali sono strutturati di modo che ogni fase del processo sia collegata a una tabella di database differente.

La fase **Imposta come qualificato** del processo di vendita può essere supportata da un'entità Opportunità. Le fasi **Stima** e **Verifica interna** possono essere supportate da un'entità Offerta. Le fasi **Contratto**, **Consegna** e **Chiusura** possono essere supportate da un'entità Contratto di progetto.

Durante lo spostamento delle transazioni da una fase all'altra, ti viene richiesto di creare un record di entità appropriato per guidarti durante il processo. Le fasi possono essere condizionali. Ad esempio, se richiedi una verifica interna di un'offerta solo se l'offerta utilizza un listino prezzi personalizzato, puoi configurare tale condizione nella fase appropriata del processo aziendale. La fase **Verifica interna** viene quindi visualizzata solo per le offerte che utilizzano un listino prezzi personalizzato. Per tutte le altre transazioni e offerte, la fase **Stima** è seguita dalla fase **Contratto**.

> [!NOTE]
> Project Operations dispone di pagine specifiche per i record entità Opportunità, Offerta, Ordine e Fattura. È necessario creare questi record utilizzando le pagine di informazioni sul progetto per queste entità. In caso contrario, non sarai in grado di aprire i record dalla pagina **Informazioni sul progetto**. Se vuoi aprire un record dalla pagina **Informazioni sul progetto** devi eliminare il record e ricrearlo utilizzando la pagina **Informazioni sul progetto** in cui la logica aziendale per ciascuno di questi tipi di entità garantisce che il campo **Tipo** del record sia impostato correttamente e tutti i concetti obbligatori siano inizializzati correttamente.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Tenere traccia delle revisioni di offerte e piani di progetto nel ciclo di vendita
In Project Operations, puoi tenere traccia delle revisioni di un'offerta. Devi invece contrassegnare l'offerta esistente come **Chiusa come persa** e quindi creare una nuova offerta. Puoi copiare un'offerta o clonare un'offerta basata su progetto.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Tenere traccia di commenti e approvazioni di offerte e contratti di progetto
Puoi gestire la revisione e l'approvazione di offerte e contratti di progetto mediante la bacheca record e i post. L'organizzazione può creare plug-in e flussi di lavoro personalizzati per assegnare, reindirizzare, riassegnare e gestire notifiche relative alla revisione e all'approvazione di elementi di lavoro.
