---
title: Copia dei contratti di progetto - semplice
description: Questo argomento fornisce informazioni sulla copia di contratti di progetto in Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee769dbd553e4a174cb71ce7a883f828e587ce36
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003591"
---
# <a name="copy-project-contracts---lite"></a>Copia dei contratti di progetto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi creare facilmente nuovi contratti di progetto eseguendo copie dei contratti esistenti in due modi: 

  - Nella pagina elenco **Contratti di progetto**, seleziona un contratto di progetto e quindi seleziona **Copia**.
  - Nella pagina dei dettagli **Contratto di progetto** seleziona **Copia**.

Si aprirà una pagina della finestra di dialogo in cui è possibile selezionare i parametri del contratto copiato. Nella finestra di dialogo sono inclusi i campi seguenti. A seconda dei valori selezionati in questa finestra di dialogo, il processo di copia potrebbe cambiare.

| **Campo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- |
| Argomento | Immetti l'argomento del contratto di destinazione. Quando si apre la pagina della finestra di dialogo, il sistema imposta questo campo sul nome del contratto di origine con **-copia** aggiunto ad esso. | Non vi è alcun impatto downstream per questo campo. |
| Cliente | Riferimento alla società o al record di account del cliente. Quando si apre la finestra di dialogo, il sistema imposterà questo campo sull'account nel contratto di origine. | Questo campo è il cliente principale del contratto. |
| Unità contratto | L'unità organizzativa responsabile della consegna del progetto o dei progetti associati a questa transazione. Quando si apre la pagina della finestra di dialogo, il sistema la imposterà sull'unità di contratto del contratto di origine. | L'unità contratto è la divisione dell'azienda che eseguirà i progetti dopo la chiusura della trattativa. Ogni unità di contratto ha una valuta. La valuta viene utilizzata per riportare i costi stimati ed effettivi sostenuti durante il progetto. |
| Valuta | La valuta in cui viene eseguita la transazione. Quando si apre la pagina della finestra di dialogo, il sistema imposterà questo campo sulla valuta del contratto di origine. La valuta può essere modificata. In tal caso, il campo **Copia prezzi** è sempre impostato su **No** perché i listini prezzi sul contratto di origine non sono più rilevanti. | La valuta viene utilizzata per impostare i listini prezzi predefiniti, per generare stime finanziarie sul contratto e per fatturare al cliente quando la transazione viene acquisita. |
| Data consegna richiesta | La data di consegna richiesta dal cliente. | Questa data viene utilizzata come data di fine quando crei date di fatturazione con una frequenza specifica. |
| Copia prezzi | Indica se il prezzo del contratto deve essere copiato dal contratto di origine. | Se il campo è impostato su **Sì**, i riferimenti del listino prezzi del prodotto e del progetto vengono copiati dal contratto di origine a quello di destinazione. Se viene selezionato **No**, i listini prezzi vengono impostati sui valori predefiniti in base agli ultimi listini prezzi nei parametri dell'account o del progetto. |

Quando selezioni **OK** nella pagina della finestra di dialogo, il sistema crea una copia del contratto in base ai parametri selezionati. Si aprirà il nuovo contratto.

Le seguenti informazioni non vengono copiate dal **contratto di origine** in **quello di destinazione**:

  - Pianificazioni di fatturazione
  - Clienti voce di contratto e contratto
  - Riferimento del progetto nelle voci di contratto basate su progetto
  - Informazioni sul budget del cliente

Poiché queste informazioni sono specifiche per ogni contratto, questi campi e record non vengono copiati. Le voci di contratto per progetti e prodotti, le stime sui dettagli delle voci di contratto e i valori da non superare a livello di contratto vengono copiati. I valori predefiniti di prezzo e tariffa di costo dipendono dalla selezione del campo **Copia prezzi** nella pagina della finestra di dialogo **Copia parametri**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]