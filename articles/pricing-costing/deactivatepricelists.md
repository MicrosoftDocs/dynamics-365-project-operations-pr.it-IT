---
title: Disattivare listini prezzi
description: Questo argomento spiega come disattivare o rimuovere listini prezzi non utilizzati o datati.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aca58eed2a0ee5e108d40636529802a7feec5b8dd060ba6c0eabc6d0b92b2e2f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997656"
---
# <a name="deactivate-price-lists"></a>Disattivare listini prezzi 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Per rimuovere i listini prezzi datati o inutilizzati da Dynamics 365 Project Operations, è necessario completare due passaggi. 

1. Rimuovere o eliminare il listino prezzi da pagine specifiche.
2. Disattivare o eliminare il listino prezzi da Listini prezzi attivi nella pagina **Listini prezzi**.

>[!IMPORTANT]
> Devi completare entrambi i passaggi per rimuovere completamente un listino prezzi. L'esecuzione unicamente del passaggio 2, che consiste nell'eliminare o disattivare direttamente il listino prezzi dalla visualizzazione Listini prezzi attivi, non è sufficiente. È anche necessario eliminare l'associazione di questo listino prezzi da tutti i luoghi menzionati al passaggio 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Eliminare il listino prezzi da pagine specifiche
1. Per eliminare un listino prezzi da Project Operations, visualizza le seguenti pagine:  

      - Pagina **Parametri progetto** > scheda **Listini prezzi**
      - Pagina **Unità organizzativa** > griglia **Listino prezzi**
      - Pagina **Conto** > griglia **Listini prezzi di progetto**
      - Pagina **Offerte di progetto** > griglia **Listini prezzi di progetto**: si applica a tutte le offerte di progetto attive.
      - Pagina **Contratti di progetto** > griglia **Listini prezzi di progetto**: si applica a tutti i contratti di progetto attivi.

 2. Per ogni pagina, devi selezionare il listino prezzi che desideri eliminare, quindi seleziona **Elimina**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Eliminare o disattivare il listino prezzi nella pagina Listini prezzi
 
1. Per eliminare un listino prezzi dai listini prezzi attivi, accedi a **Vendite** > **Clienti** > **Listini prezzi**. 
2. Seleziona il listino prezzi che vuoi eliminare e quindi seleziona **Elimina**. Se si fa riferimento al listino prezzi in qualsiasi transazione esistente, non potrai eliminarlo. In tal caso, puoi disattivare il listino prezzi di modo che non appaia in nessuna visualizzazione. 
3. Per disattivare il listino prezzi, selezionare di nuovo il listino prezzi, quindi seleziona **Disattiva**.   
