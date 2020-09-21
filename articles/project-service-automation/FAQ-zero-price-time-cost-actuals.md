---
title: Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo ora?
description: Risoluzione del problema relativo all'impostazione automatica su zero del prezzo per gli effettivi costo ora.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752750"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Perché il prezzo viene impostato automaticamente su zero per gli effettivi costo ora?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Queste domande frequenti si applicano agli effettivi dove la classe di transazione è impostata su Ora e il tipo di transazione è Costo. I seguenti tre controlli consentono di risolvere il problema relativo all'impostazione automatica del prezzo su 0 degli effettivi costo ora.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Controllo 1: identificare il listino prezzi di costo per il progetto

Individuare il progetto nel campo del progetto dell'effettivo e quindi passare alla pagina del progetto. Fare clic sul collegamento dell'unità contratto nel campo. Nella pagina Unità contratto, verificare se l'unità contratto ha un listino prezzi nella griglia Listini prezzi di costo.

Se sono presenti più listini prezzi, il problema è stato isolato. Project Service supporta un solo listino prezzi per unità organizzativa. Rimuovere tutti i listini prezzi da questa entità fino a che non vi sia un solo listino prezzi allegato alla griglia Listini prezzi di costo dell'unità organizzativa.

Se non sono presenti listini prezzi allegati all'unità organizzativa, prendere nota della valuta dell'unità organizzativa. Accedere a Project Service e quindi a Parametri e aprire la scheda Listini prezzi. Verificare se sono presenti listini prezzi con contesto impostato su Costo e con la valuta corrispondente alla valuta dell'unità organizzativa.
 
Se non sono presenti listini prezzi che soddisfano quei criteri, il problema è stato isolato. Verificare di disporre di almeno un listino prezzi il cui contesto è impostato su Costo e la cui valuta corrisponde alla valuta dell'unità organizzativa.

Se sono presenti più listini prezzi che soddisfano quei criteri, continuare a leggere questo documento per eseguire ulteriori controlli.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Controllo 2: i listini prezzi identificati precedentemente sono validi per la data specifica dell'effettivo costo ora?

Affinché Project Service consideri un listino prezzi per l'impostazione automatica del prezzo, il listino prezzi deve essere applicabile per la data dell'effettivo costo ora. Controllare quanto segue per verificare se i listini prezzi identificati precedentemente sono applicabili:

- Verificare che i campi della data di inizio e della data di fine nella scheda Generale dei listini prezzi allegati non siano vuoti. Se quei campi sono vuoti per i listini prezzi identificati in precedenza, il problema è stato isolato. 
- Prendere nota del campo della data di inizio dell'effettivo costo ora e controllare se qualsiasi listino prezzi identificato è applicabile per tale data. Ad esempio, la data dell'effettivo costo ora deve rientrare nella data di inizio e nella data di fine sul listino prezzi. 
    - Se non vi sono listini prezzi che coprono quella data per l'effettivo costo ora, il problema è stato isolato. Modificare la data di inizio e quella di fine del listino prezzi per assicurarsi che il listino prezzi copra la data dell'effettivo costo ora. 
    - Se vi sono più listini prezzi che coprono la data dell'effettivo costo ora, il problema è stato isolato. È possibile risolvere questo problema modificando la data di inizio e quella di fine dei listini prezzi affinché sia presente un solo listino prezzi che copre la data dell'effettivo costo ora. 
    - Se esiste un solo listino prezzi che copre la data dell'effettivo costo ora, passare al controllo successivo nel documento.
Dopo aver effettuato le correzioni necessarie, ricreare un inserimento ore, approvarlo e verificare che l'effettivo costo ora visualizzi un prezzo valido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Controllo 3: esiste un prezzo nel listino prezzi per le dimensioni di determinazione dei prezzi dell'effettivo costo ora?

Se il controllo 1 e il controllo 2 sono stati completati correttamente, si dovrebbe ora disporre di un solo listino prezzi che è applicabile per la data dell'effettivo costo ora. Aprire il listino prezzi e accedere alla scheda Prezzi ruolo. Assicurarsi che vi sia una riga nella griglia per le dimensioni di determinazione dei prezzi dell'effettivo costo ora.

Se non è disponibile alcuna riga nella griglia dei prezzi di ruolo per le dimensioni di determinazione dei prezzi dell'effettivo costo ora, il problema è stato isolato. Creare una riga nella griglia dei prezzi di ruolo per le dimensioni di determinazione dei prezzi dell'effettivo costo ora. Successivamente, ricreare un inserimento ore, approvarlo e verificare che l'effettivo costo ora visualizzi un prezzo valido.
 
Se non viene ancora visualizzato un prezzo valido per l'effettivo costo ora dopo aver eseguito i tre controlli descritti precedentemente, creare un ticket di supporto.



