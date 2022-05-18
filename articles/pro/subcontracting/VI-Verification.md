---
title: Verifica delle fatture fornitore con valori effettivi approvati
description: Questo argomento spiega come Microsoft Dynamics 365 Project Operations consente ai project manager di verificare le fatture fornitore con i valori effettivi che sono stati approvati quando gli appaltatori hanno eseguito il lavoro e registrato le ore, nonché le spese e i materiali utilizzati dai membri del team di progetto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585475"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verifica delle fatture fornitore con valori effettivi approvati

[!include [banner](../../includes/dataverse-preview.md)]

_ **Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma

Microsoft Dynamics 365 Project Operations consente ai project manager di verificare le righe di fattura fornitore nei seguenti modi:

- Usa il campo **Stato verifica** nelle righe di fattura fornitore.
- Se le righe di fattura fornitore fanno riferimento a una riga di conto lavoro, collega i costi effettivi dall'attività del terzista a tali righe di fattura fornitore. Il collegamento viene creato abbinando i costi effettivi alle righe di fattura fornitore.

    > [!NOTE]
    > Sebbene sia possibile tenere traccia dello stato di verifica per le righe di fattura fornitore che non fanno riferimento a un conto lavoro, i costi effettivi non possono essere collegati a tali righe di fattura fornitore.

## <a name="verification-status"></a>Stato verifica

Il campo **Stato verifica** su una riga di fattura fornitore indica lo stato della verifica. Gli stati seguenti sono supportati:

1. Non avviato
2. In corso
3. Completamento

Le righe di fattura fornitore con stato di verifica di **Non avviato** possono essere modificate.

Le righe di fattura fornitore con stato di verifica di **In corso** non possono più essere modificate. Per una riga di fattura fornitore che fa riferimento a un conto lavoro, lo stato di verifica viene impostato automaticamente su **In corso** non appena il primo costo effettivo viene abbinato alla riga di fattura fornitore.

Le righe di fattura fornitore con stato di verifica di **Completato** non possono più essere modificate. Quando tutte le righe di una fattura fornitore hanno questo stato di verifica, la fattura fornitore può essere confermata.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Abbinare costi effettivi a righe di fattura fornitore

L'abbinamento dei costi effettivi aiuta il processo di verifica di una riga di fattura fornitore. Per abbinare i costi effettivi a una riga di fattura fornitore, attieniti alla seguente procedura.

1. Apri la riga di fattura fornitore e seleziona la scheda **Valori effettivi costo non corrispondenti**. Una griglia mostra un elenco di costi effettivi che fanno riferimento alla stessa riga di conto lavoro della riga di fattura fornitore.
2. Selezionare uno o più costi effettivi, quindi seleziona **Corrispondenza** sulla barra degli strumenti sopra la griglia. Il sistema convalida che i costi effettivi selezionati possono essere abbinati. Dopo che la convalida è stata superata, i costi effettivi vengono collegati alla riga di fattura fornitore.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Criteri di convalida utilizzati per collegare i costi effettivi alle righe di fattura fornitore

Durante il processo di corrispondenza, è possibile stabilire un collegamento tra un costo effettivo e una riga di fattura fornitore solo se sono soddisfatte entrambe le condizioni seguenti:

- Il campo **Stato rettifica** per ogni costo effettivo selezionato deve essere vuoto. In altre parole, i costi effettivi non devono essere stati sostituiti da altri costi effettivi durante un processo di richiamo, annullamento dell'approvazione o correzione del giornale di registrazione.
- I valori dei seguenti campi vengono corrisposti tra la riga di fattura fornitore e il costo effettivo selezionato. Se un campo non è impostato nella riga di fattura fornitore, non viene considerato per la corrispondenza.

    - Contratto di progetto
    - Voce di contratto di progetto
    - Classe di transazione
    - Project
    - Attività
    - Categoria di risorsa
    - Categoria di transazione
    - Prodotto
    - Riga conto lavoro
    - Risorsa prenotabile

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Valori effettivi costo non corrispondenti da una riga di fattura fornitore

La mancata corrispondenza dei costi effettivi può anche aiutare il processo di verifica di una fattura fornitore, consentendo la rimozione dei collegamenti stabiliti in precedenza. I costi effettivi possono essere non corrispondenti solo dalle righe di fattura fornitore con stato di verifica di **In corso**. Per annullare la corrispondenza dei costi effettivi da una riga di fattura fornitore, attieniti alla seguente procedura.

1. Apri la riga di fattura fornitore e seleziona la scheda **Valori effettivi costo corrispondenti**. Una griglia mostra un elenco di costi effettivi che fanno riferimento alla riga di fattura fornitore.
2. Selezionare uno o più costi effettivi, quindi seleziona **Annulla corrispondenza** sulla barra degli strumenti sopra la griglia.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
