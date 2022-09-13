---
title: Copiare i contratti basati su progetti
description: Questo articolo fornisce informazioni sulla copia dei contratti di progetto in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410324"
---
# <a name="copy-project-based-contracts"></a>Copiare i contratti basati su progetti

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Puoi creare facilmente nuovi contratti di progetto eseguendo copie dei contratti esistenti in due modi:

- Nella pagina elenco **Contratti di progetto**, seleziona un contratto di progetto e quindi seleziona **Copia**.
- Nella pagina dei dettagli **Contratto di progetto** seleziona **Copia**.

In entrambi i casi, viene visualizzata una finestra di dialogo in cui è possibile selezionare i parametri del contratto copiato. Nella finestra di dialogo sono inclusi i campi seguenti. A seconda dei valori selezionati, il processo di copia potrebbe cambiare.

| Campo | Description | Impatto downstream |
| --- | --- | --- |
| Argomento | Immetti l'argomento del contratto di destinazione. Quando si apre la pagina della finestra di dialogo, il sistema imposta il nome del contratto di origine, ma la parola "copia" viene aggiunta ad esso. | Non vi è alcun impatto downstream per questo campo. |
| Cliente | Un riferimento alla società o al record di account del cliente. Quando si apre la finestra di dialogo, il sistema imposta questo campo sull'account nel contratto di origine. | Questo campo è il cliente principale del contratto. |
| Società proprietaria | L'azienda che è responsabile della consegna dei progetti associati a questa transazione. Quando si apre la finestra di dialogo, il sistema imposta questo campo sull'azienda proprietaria nel contratto di origine. | L'azienda proprietaria è la persona giuridica che eseguirà il progetto dopo la chiusura della transazione. La valuta dell'azienda proprietaria deve corrispondere alla valuta dell'unità contratto. |
| Unità di contratto | L'unità organizzativa responsabile della consegna dei progetti associati a questa transazione. Quando si apre la finestra di dialogo, il sistema imposta questo campo sull'unità di contratto nel contratto di origine. | L'unità contratto è la divisione dell'azienda che eseguirà i progetti dopo la chiusura della trattativa. Ogni unità di contratto ha una valuta. La valuta viene utilizzata per riportare i costi stimati ed effettivi sostenuti durante il progetto. |
| Valuta | La valuta in cui viene eseguita la transazione. Quando si apre la finestra di dialogo, il sistema imposta questo campo sulla valuta del contratto di origine. La valuta può essere modificata. In tal caso, il campo **Copia prezzi** è sempre impostato su **No** perché i listini prezzi sul contratto di origine non sono più rilevanti. | Questa valuta viene utilizzata per impostare i listini prezzi predefiniti, per generare stime finanziarie sul contratto e per fatturare al cliente quando la transazione viene acquisita. |
| Data di consegna richiesta | La data di consegna richiesta dal cliente. | Questa data viene utilizzata come data di fine quando crei date di fatturazione con una frequenza specifica. |
| Copia prezzi | Un valore che indica se il prezzo del contratto deve essere copiato dal contratto di origine. | Se il campo è impostato su **Sì**, i riferimenti del listino prezzi del prodotto e del progetto vengono copiati dal contratto di origine a quello di destinazione. Se impostata su **No**, vengono usati i listini prezzi predefiniti in base agli ultimi listini prezzi nei parametri dell'account o del progetto. |

Quando selezioni **OK** nella finestra di dialogo, il sistema crea una copia del contratto in base ai valori dei parametri selezionati. Si aprirà quindi il nuovo contratto.

Le seguenti informazioni **non** sono copiate dal contratto di origine al contratto di destinazione, perché sono specifiche di ogni contratto:

- Pianificazioni di fatturazione
- Clienti voce di contratto e contratto
- Riferimento del progetto nelle voci di contratto basate su progetto
- Informazioni sul budget del cliente

Le voci di contratto per progetti e prodotti, le stime sui dettagli delle voci di contratto e i valori da non superare a livello di contratto vengono copiati. L'immissione di valori predefiniti di prezzo e tariffa di costo dipendono dalla selezione del campo **Copia prezzi** nella pagina della finestra di dialogo **Copia parametri**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
