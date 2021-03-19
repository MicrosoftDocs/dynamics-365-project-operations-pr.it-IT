---
title: Copiare offerte basate su progetto
description: Questo argomento fornisce informazioni su come copiare le offerte basate su progetto in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b1ce6c2b644319f2d822010a34c57c591f82edc9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278153"
---
# <a name="copy-project-based-quotes"></a>Copiare offerte basate su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi facilmente creare una nuova offerta di progetto copiandone una esistente. 

- Per copiare un'offerta di progetto, nella pagina elenco **Offerte di progetto** o nella pagina dei dettagli **Offerta di progetto**, seleziona l'offerta di progetto che vuoi copiare, quindi seleziona **Copia**.

Si aprirà una pagina della finestra di dialogo in cui è possibile inserire i parametri della copia. Nella tabella seguente sono elencati i campi inclusi nella pagina della finestra di dialogo. A seconda dei valori selezionati, il processo di copia potrebbe cambiare.

| **Campo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- |
| Argomento | Inserisci l'argomento o il nome pertinente dell'offerta di destinazione. Quando si apre la finestra di dialogo, il sistema la imposterà sull'argomento dell'offerta di origine con **-copia** aggiunto ad esso. | |
| Potenziale cliente | Riferimento alla società o al record di account del cliente. Quando si apre la finestra di dialogo, il sistema la imposterà sull'account nell'offerta di origine. | Questo campo è il cliente principale dell'offerta. |
| Unità contratto | L'unità organizzativa responsabile della consegna del progetto o dei progetti associati a questa transazione.
Quando si apre la finestra di dialogo, il sistema la imposterà sull'unità di contratto dell'offerta di origine. | L'unità di contratto è la divisione dell'azienda che eseguirà i progetti dopo la chiusura della trattativa. Ogni unità di contratto ha una valuta. La valuta viene utilizzata per riportare i costi stimati ed effettivi sostenuti durante l'esecuzione del progetto. |
| Valuta | È la valuta in cui viene eseguita la transazione. Quando si apre la finestra di dialogo, il sistema la imposterà sulla valuta dell'offerta di origine. Questo può essere modificato e, se cambia, il campo **Copia prezzi** è sempre impostato su **No**. Questo perché i listini prezzi sull'offerta di origine non sono più rilevanti. | La valuta viene utilizzata per impostare un listino prezzi predefinito, per generare una stima finanziaria sull'offerta e, infine, per fatturare al cliente quando la transazione viene acquisita. |
| Data consegna richiesta | Questa è la data di consegna richiesta dal cliente. | Viene utilizzata come data di fine quando si creano date di fatturazione con una frequenza specifica. |
| Copia prezzi | Un valore Sì/No indica se il prezzo dell'offerta deve essere copiato dall'offerta di origine. | Se viene selezionato **Sì** , il listino prezzi del progetto e i riferimenti del listino prezzi del prodotto vengono copiati dall'offerta di origine all'offerta di destinazione. Se viene selezionato **No**, i listini prezzi vengono reimpostati in base agli ultimi listini prezzi impostati sui parametri dell'account o del progetto. |

Quando selezioni **OK** nella pagina della finestra di dialogo, il sistema crea una copia dell'offerta di progetto in base ai parametri selezionati nella finestra di dialogo. Si apre la nuova offerta di progetto. 

> [!NOTE]
> Le seguenti informazioni non vengono copiate dall'offerta di origine a quella di destinazione:
>
> - Pianificazioni di fatturazione
> - Offerte e clienti della riga di offerta
> - Riferimento del progetto nelle righe di offerta basate sul progetto - Informazioni sul budget del cliente
>
>Poiché queste informazioni sono molto specifiche per ogni offerta, questi campi e record non vengono copiati. Le righe di offerta per progetti e prodotti, le stime sui dettagli delle righe di offerta e i valori da non superare a livello di offerta vengono copiati. I valori predefiniti di prezzo e tasso di costo dipendono dall'opzione **Copia prezzi** selezionata nella pagina della finestra di dialogo **Copia parametri**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]