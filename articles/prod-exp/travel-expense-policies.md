---
title: Configurare i criteri di spesa
description: Puoi definire i criteri di spesa che i dipendenti devono seguire quando inseriscono e inviano note spese e richieste di viaggio in Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079023"
---
# <a name="set-up-expense-policies"></a>Configurare i criteri di spesa

[!include [banner](../includes/banner.md)]

Puoi definire i criteri che i dipendenti devono seguire quando inseriscono e inviano note spese e richieste di viaggio.         
L'implementazione dei criteri di spesa può aiutarti a gestire le spese in modo efficace.         

Ad esempio, puoi impostare un criterio per le spese dell'hotel a New York City, in cui si stabilisce che la spesa per notte non può superare USD 250.       
Se un lavoratore invia una nota spese o una richiesta di viaggio in cui la tariffa della camera supera questo importo, il sistema avviserà il        
lavoratore che l'importo dei criteri per la spesa è stato superato. Puoi configurare il messaggio che il lavoratore riceverà quando        
definisci i criteri.      
        
Puoi definire tre tipi di criteri:         
        
- Avviso: consente al lavoratore di inviare una nota spese o una richiesta di viaggio, ma la spesa verrà contrassegnata per tutti gli approvatori e        
  per i report successivi.        

- Errore: richiede al lavoratore di rivedere la spesa per conformarsi ai criteri prima di inviare la nota spese o la richiesta di viaggio.       
 
 - Giustificazione: richiede al lavoratore o a un responsabile di inserire una giustificazione per il superamento dell'importo dei criteri prima di inviare la nota spese o la richiesta di viaggio.        

## <a name="policy-tips"></a>Suggerimenti per i criteri
Di seguito sono riportati alcuni suggerimenti che possono essere utili durante la creazione di nuovi criteri per la gestione delle spese. 
* I criteri hanno una data di validità e non avranno effetto se vengono creati con una data successiva alla data in cui si è verificata la spesa. Ad esempio, se oggi crei un nuovo criterio per applicare una spesa massima per i pasti di $50, qualsiasi spesa esistente inserita a partire da ieri non verrà verificata rispetto a questo criterio.
* Quando si crea un criterio per una categoria di spesa che può essere dettagliata, considera l'aggiunta di una condizione per il tipo di riga di spesa. Alcuni criteri come la richiesta di ricevuta potrebbero non avere senso per le righe dettagliate e dovrebbero essere applicati solo alla riga di intestazione o a una riga non dettagliata. 
* Per impostazione predefinita, i criteri di gestione delle spese vengono valutati rispetto all'entità di origine. Per gli scenari interaziendali, puoi impostare invece la valutazione del criterio rispetto all'entità di destinazione (entità mutuataria). Per eseguire i criteri sull'entità di destinazione, attiva la funzionalità "Valuta criteri di spesa rispetto alla persona giuridica mutuataria" nell'area di lavoro **Gestione delle funzionalità**.

## <a name="when-to-evaluate-policies"></a>Quando valutare i criteri

Nei parametri di gestione delle spese, puoi scegliere di valutare i criteri di gestione delle spese quando viene salvata una riga o quando viene inviata una nota spese. Se scegli di valutare quando una riga viene salvata, gli utenti avranno visibilità in anticipo su ciò che devono fare per completare la loro nota spese tutto insieme. In caso contrario, puoi ritardare la valutazione del criterio e risparmiare tempo convalidando alla fine, durante l'invio al flusso di lavoro.
