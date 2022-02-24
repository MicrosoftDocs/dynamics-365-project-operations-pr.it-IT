---
title: Copiare opportunità basate su progetto
description: Questo argomento fornisce informazioni su come copiare le opportunità basate su progetto in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 26ae5cc267bb06f958bbf9cdce2d80ccde9d3d24
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181661"
---
# <a name="copy-project-based-opportunities"></a>Copiare opportunità basate su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


Le opportunità di progetto possono essere facilmente copiate per creare nuove opportunità di progetto. 

1. Vai alla pagina elenco **Opportunità di progetto** e seleziona un'opportunità dall'elenco. Oppure apri la pagina dei dettagli di un'opportunità specifica. 
2. In entrambe le pagine, seleziona **Copia**. Si aprirà una pagina di dialogo che contiene le seguenti informazioni nei campi. A seconda dei valori selezionati in questa finestra di dialogo, il processo di copia potrebbe cambiare.

    | **Campo** | **Descrizione** | **Impatto downstream** |
    | --- | --- | --- |
    | Argomento | Immetti l'argomento rilevante dell'opportunità di destinazione. Quando si apre la finestra di dialogo, il sistema la imposterà sull'argomento dell'opportunità di origine con **copia** aggiunto ad esso. | Non vi è alcun impatto downstream per questo campo. |
    | Conto | Fa riferimento alla società o al record di account del cliente. Quando si apre la finestra di dialogo, il sistema la imposterà sull'account nell'opportunità di origine. | Questo campo è il cliente principale dell'opportunità. |
    | Unità contratto | L'unità organizzativa responsabile della consegna dei progetti associati a questa transazione. Quando si apre la finestra di dialogo, il sistema la imposterà sull'unità di contratto dell'opportunità di origine. | L'unità di contratto è la divisione dell'azienda che esegue i progetti dopo la chiusura della transazione. Ogni unità contratto ha una valuta e questa valuta viene utilizzata per riportare i costi stimati ed effettivi sostenuti durante il progetto. |
    | Valuta | La valuta in cui viene eseguita la transazione. Quando si apre la pagina della finestra di dialogo, il sistema la imposterà sulla valuta dell'opportunità di origine. | La valuta viene utilizzata per impostare un listino prezzi predefinito e creare stime finanziarie sull'offerta. La valuta viene utilizzata per fatturare al cliente quando la transazione viene acquisita. |
    | Copia prezzi | Un valore Sì/No che indica se il prezzo dell'opportunità deve essere copiato dall'opportunità di origine. | Se **Sì** è selezionato, i listini prezzi vengono copiati dall'opportunità di origine in quella di destinazione. Se viene selezionato **No**, i listini prezzi vengono impostati sui valori predefiniti in base agli ultimi listini prezzi impostati. |

3. Seleziona **OK**. Il sistema crea una copia dell'opportunità di progetto in base ai parametri selezionati e viene aperta la nuova opportunità di progetto.
