---
title: Conto lavoro nell'accesso in anteprima al ciclo di ottobre 2021
description: Questo argomento fornisce una panoramica delle funzionalità di conto lavoro in Project Operations che fanno parte della versione di accesso in anteprima al ciclo di ottobre 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383700"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Conto lavoro nell'accesso in anteprima al ciclo di ottobre 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento fornisce una panoramica delle funzionalità di conto lavoro in Dynamics 365 Project Operations che fanno parte della versione di accesso in anteprima al ciclo di ottobre 2021. Questo set di funzionalità non è pronto per gli ambienti di produzione o live, quindi queste funzionalità rimarranno nella versione di accesso in anteprima al ciclo dell'intero set di funzionalità. Si consiglia vivamente di non utilizzare il set di funzionalità di conto lavoro per gli scenari di produzione live fino a quando non viene rimosso il banner di anteprima. 

L'elenco seguente fornisce una panoramica di ciò che è attualmente disponibile nella versione di accesso in anteprima al ciclo di ottobre 2021:

1. Il project manager crea un conto lavoro con un fornitore. Per impostazione predefinita, per il conto lavoro vengono utilizzati i listini prezzi associati al record del fornitore. Il conto fornitore ha un tipo di relazione di tipo **fornitore** o **venditore**.

2. Il project manager può dettagliare tutti gli acquisti come voci nel conto lavoro. Le righe del conto lavoro possono riguardare tempi, spese o prodotti. La classe di transazione della voce di conto lavoro determina a cosa serve la riga.

3. L'account manager del fornitore e il project manager possono eseguire iterazioni sul conto lavoro. È possibile apportare modifiche ai prezzi nei listini prezzi di acquisto associati al conto lavoro.

4. A questo punto o in una fase successiva del processo, se la riga di conto lavoro è per il tempo, l'account manager del fornitore associa i contatti dei fornitori a ciascuna riga di conto lavoro. Questa associazione fornisce informazioni al project manager che sta lavorando sul conto lavoro. Quando un contatto fornitore è associato a una riga di conto lavoro, il sistema crea automaticamente una risorsa prenotabile dal contatto, se non esiste già una risorsa prenotabile.

5. Il metodo di fatturazione su ciascuna riga di subappalto può essere di tipo **prezzo fisso** o **tempo e materiale**. Per le righe di conto lavoro a prezzo fisso viene impostata una pianificazione fattura basata su passaggi fondamentali.

I passaggi rimanenti nel flusso del processo aziendale per il conto lavoro delineati nella Panoramica non sono attualmente disponibili. Con l'aggiunta di nuove funzionalità, questo argomento verrà aggiornato. 

L'illustrazione seguente rappresenta la versione di accesso in anteprima al conto lavoro in contrasto con il processo aziendale end-to-end.

![Flusso del processo dei conti lavoro](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Versione di accesso in anteprima al ciclo delle voci di conto lavoro basate sulla quantità e righe di conto lavoro basate sul lavoro
Nella versione di accesso in anteprima al ciclo di ottobre 2021, sono supportate solo le voci di conto lavoro basate sulla quantità. Ciò significa che una voce di conto lavoro può essere utilizzata per acquistare ore, spese o materiali da un fornitore ma non un intero corpo di lavoro. Ciò significa anche che la quantità acquistata (unità di tempo, spese o quantità di materiali) in una voce di conto lavoro può essere utilizzata in qualsiasi progetto nel sistema.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
