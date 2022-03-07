---
title: Perché il prezzo viene impostato automaticamente su zero per gli effettivi vendita ora?
description: Risoluzione del problema relativo all'impostazione automatica su zero del prezzo per gli effettivi vendita ora.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 2df4ce2d6391e70fea8e8f15c1b5774c9a9bfbe5f5ef2e6d8da8668afd34d4c9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992571"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Perché il prezzo viene impostato automaticamente su zero per gli effettivi vendita ora?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Queste domande frequenti si applicano agli effettivi dove la classe di transazione è impostata su Ora e il tipo di transazione è Vendite non fatturate. I seguenti tre controlli consentono di risolvere il problema relativo all'impostazione automatica del prezzo (tasso di fatturazione) su 0 per gli effettivi vendita ora.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Controllo 1: identificare il listino prezzi di vendita per il progetto

Individuare il progetto nel campo del progetto dell'effettivo e passare alla pagina del progetto. Accedere alla scheda Vendite e nella griglia delle voci di contratto di progetto, fare clic sul collegamento nel campo Contratto di progetto. Viene visualizzata la pagina Contratto del progetto. Nella pagina Contratto di progetto, andare alla scheda Listini prezzi di progetto. Verificare se almeno un listino prezzi è allegato a tale scheda. Se nessun listino prezzi è visualizzato nella griglia Listini prezzi di progetto del contratto di progetto, il problema è stato isolato. Allegare un listino prezzi alla griglia Listini prezzi di progetto. I listini prezzi che è possibile allegare devono avere il campo Contesto impostato su Vendite e il campo Valuta deve corrispondere al campo Valuta nel contratto di progetto. Dopo aver effettuato le correzioni necessarie, ricreare un inserimento ore, visualizzarlo e verificare che l'effettivo vendite non fatturati visualizzi un prezzo valido. 

Se si hanno uno o più listini prezzi nella griglia Listini prezzi di progetto del contratto di progetto, procedere al controllo successivo nel documento.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Controllo 2: i listini prezzi identificati precedentemente sono validi per la data specifica dell'effettivo vendita ora?

Affinché Project Service consideri un listino prezzi per l'impostazione automatica del prezzo, il listino prezzi deve essere applicabile per la data nell'effettivo vendita ora. Controllare quanto segue per verificare se i listini prezzi identificati precedentemente sono applicabili:
- Verificare che i campi della data di inizio e della data di fine nella scheda Generale dei listini prezzi allegati non siano vuoti. Se quei campi sono vuoti per i listini prezzi identificati in precedenza, il problema è stato isolato. 
- Prendere nota del campo della data di inizio nell'effettivo vendita ora e controllare se qualsiasi listino prezzi identificato è applicabile per tale data. Ad esempio, la data dell'effettivo vendita ora deve rientrare nella data di inizio e nella data di fine del listino prezzi. 
    - Se non vi sono listini prezzi che coprono quella data dell'effettivo vendita ora, il problema è stato isolato. Modificare le date di inizio e fine del listino prezzi per verificare che il listino prezzi copre la data dell'effettivo vendita ora. 
    - Se vi sono più listini prezzi che coprono la data dell'effettivo vendita ora, il problema è stato isolato. È possibile risolvere questo problema modificando le date di inizio e fine dei listini prezzi affinché sia presente un solo listino prezzi che copre la data dell'effettivo vendita ora. 
    - Se esiste un solo listino prezzi che copre quella data dell'effettivo vendita ora, passare al controllo 3.
Dopo aver effettuato le correzioni necessarie, ricreare un inserimento ore, visualizzarlo e verificare che l'effettivo vendita ora visualizzi un prezzo valido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Controllo 3: esiste un prezzo nel listino prezzi per le dimensioni di determinazione dei prezzi dell'effettivo vendita ora?

Se il controllo 1 e il controllo 2 sono stati completati correttamente, ora si dovrebbe disporre di un solo listino prezzi che è applicabile per la data dell'effettivo vendita ora. Aprire il listino prezzi e accedere alla tabella Prezzi ruolo. Assicurarsi che vi sia una riga nella griglia per le dimensioni di determinazione dei prezzi dell'effettivo vendita ora.

Se non è disponibile alcuna riga nella griglia dei prezzi di ruolo per le dimensioni di determinazione dei prezzi dell'effettivo vendita ora, il problema è stato isolato. Creare una riga nella griglia dei prezzi di ruolo per le dimensioni di determinazione dei prezzi dell'effettivo vendita ora. Successivamente, ricreare un inserimento ore, approvarlo e verificare che l'effettivo vendita ora visualizzi un prezzo valido.

Se non viene ancora visualizzato un prezzo valido per l'effettivo vendita ora dopo aver eseguito i tre controlli descritti precedentemente, creare un ticket di supporto. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]