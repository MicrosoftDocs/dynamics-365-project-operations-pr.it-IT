---
title: Perché il prezzo viene impostato automaticamente su zero per gli effettivi vendita spese?
description: I seguenti tre controlli consentono di risolvere il problema relativo all'impostazione automatica del prezzo su 0 per gli effettivi vendita spese.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 8c2270b07b6f8765a6ec1f506fe1767a1841950b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122078"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Perché il prezzo viene impostato automaticamente su zero per gli effettivi vendita spese?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Queste domande frequenti si applicano agli effettivi spese dove la classe di transazione è impostata su Spesa e il tipo di transazione è Vendite non fatturate. I seguenti tre controlli consentono di risolvere il problema relativo all'impostazione automatica del prezzo (tariffa di fatturazione) su 0 per gli effettivi vendita spese.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Controllo 1: identificare il listino prezzi di vendita per il progetto

Individuare il progetto nel campo del progetto dell'effettivo e passare alla pagina del progetto. Accedere quindi alla scheda Vendite e sulla griglia delle voci di contratto di progetto, fare clic sul collegamento nel campo Contratto di progetto. Viene visualizzata la pagina Contratto di progetto. Nella pagina Contratto di progetto, andare alla scheda Listini prezzi di progetto. Verificare se almeno un listino prezzi è allegato a tale scheda.

Se nessun listino prezzi è allegato alla griglia Listini prezzi di progetto del contratto di progetto, procedere come segue

- Allegare un listino prezzi alla griglia Listini prezzi di progetto. I listini prezzi che è possibile allegare devono avere il campo Contesto impostato su Vendite e il campo Valuta deve corrispondere al campo Valuta nel contratto di progetto. Dopo aver effettuato le correzioni necessarie, ricreare una voce di spesa, approvarla e verificare che l'effettivo vendite non fatturate visualizzi un prezzo valido.
- Se si hanno uno o più listini prezzi allegati nella griglia Listini prezzi di progetto del contratto di progetto, procedere al controllo 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Controllo 2: i listini prezzi identificati precedentemente sono validi per la data specifica dell'effettivo spese?

Affinché Project Service consideri un listino prezzi per l'impostazione automatica del prezzo, il listino prezzi deve essere applicabile per la data dell'effettivo vendita spese. Controllare quanto segue per verificare se i listini prezzi identificati precedentemente sono applicabili:

- Cominciare verificando che i campi della data di inizio e della data di fine nella scheda Generale dei listini prezzi allegati non siano vuoti. Se quei campi sono vuoti per i listini prezzi identificati in precedenza, il problema è stato isolato. 
- Prendere nota del campo della data di inizio dell'effettivo vendita spese e controllare se qualsiasi listino prezzi identificato è applicabile per tale data. Ad esempio, la data dell'effettivo spese deve rientrare nella data di inizio e nella data di fine sul listino prezzi. 
    - Se non vi sono listini prezzi che coprono quella data per l'effettivo vendita spese, il problema è stato isolato. Modificare la data di inizio e quella di fine del listino prezzi per assicurarsi che il listino prezzi copra la data dell'effettivo spese. 
    - Se vi sono più listini prezzi che coprono la data dell'effettivo vendita spese, il problema è stato isolato. È possibile risolvere questo problema modificando la data di inizio e quella di fine dei listini prezzi affinché sia presente un solo listino prezzi che copre la data dell'effettivo spese. 
    - Se esiste un solo listino prezzi che copre la data dell'effettivo spese, passare al controllo 3.
Dopo aver effettuato le correzioni necessarie, ricreare una voce di spesa, approvarla e verificare che l'effettivo vendite non fatturate visualizzi un prezzo valido.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Controllo 3: esiste un prezzo valido per la categoria di spesa nel listino prezzi di progetto applicabile? 

Se il controllo 1 e il controllo 2 sono stati completati correttamente, si dovrebbe ora disporre di un solo listino prezzi di progetto che è applicabile per la data dell'effettivo vendita spese. Aprire il listino prezzi di progetto e accedere alla scheda Prezzi categoria. Assicurarsi che vi sia una riga nella griglia per la categoria di spesa specifica dell'effettivo spese.
 
- Se non è disponibile alcun riga, il problema è stato isolato. Creare una riga nella griglia dei prezzi di categoria per la categoria dell'effettivo spese. Successivamente, ricreare una voce di spesa, approvarla e verificare che l'effettivo vendite non fatturate visualizzi un prezzo valido. 
- Se è presente una riga per la categoria di spesa nella griglia dei prezzi di categoria, verificare se ha un prezzo valido.

Per comprendere cosa si intende con prezzo valido, utilizzare questi metodi:

- Se il campo Metodo di determinazione dei prezzi nella riga dei prezzi di categoria è impostato su Al costo, la tariffa unitaria dell'effettivo vendita spese verrà automaticamente impostato sul valore nella voce di spesa.
- Se il campo Metodo di determinazione dei prezzi nella riga dei prezzi di categoria è impostato su Percentuale ricarico, verificare se il campo Percentuale è impostato su un valore valido. La tariffa unitaria dell'effettivo vendita spese viene impostata automaticamente applicando questa percentuale di ricarico sul prezzo nella voce di spesa.
- Se il campo Metodo di determinazione dei prezzi nella riga dei prezzi di categoria è impostato su Prezzo unitario, verificare se il campo Prezzo è impostato su un valore valido. La tariffa unitaria dell'effettivo vendita spese verrà impostata automaticamente sull'importo forfettario specificato nel campo Prezzo.

Se il prezzo impostato per categoria di spesa non è valido, il problema è stato isolato. La soluzione consiste nel modificare la riga dei prezzi di categoria con un prezzo valido per la categoria di spesa in conformità con le regole descritte sopra. Successivamente, ricreare una voce di spesa, approvarla e verificare che l'effettivo vendite non fatturate visualizzi un prezzo valido.

Se non viene ancora visualizzato un prezzo valido per l'effettivo vendita spese dopo aver eseguito i tre controlli descritti precedentemente, creare un ticket di supporto.


