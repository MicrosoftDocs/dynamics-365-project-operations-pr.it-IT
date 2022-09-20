---
title: Sostituzioni prezzo data di validità
description: Questo articolo spiega come impostare le sostituzioni dei prezzi per prezzi specifici nel listino prezzi.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445971"
---
# <a name="date-effective-price-overrides"></a>Sostituzioni prezzo data di validità 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

*Sostituzioni prezzo data di validità* fornisce un modo per ignorare o modificare prezzi specifici nel listino prezzi. Ad esempio, hai un listino prezzi standard valido dal 1 gennaio 2022 al 31 dicembre 2022. Questo listino prezzi ha prezzi per molti ruoli. Il prezzo impostato per il ruolo **Tecnico di rete** è di 100 dollari USA (USD) all'ora. Quando un tecnico di rete registra l'ora tra il 1 gennaio 2022 e il 31 dicembre 2022, l'ora ha un prezzo di 100 USD. Il 1 ottobre 2022 è necessario adeguare il prezzo *solo* per il ruolo **Tecnico di rete**, da 100 USD all'ora a 110 USD all'ora. La funzione **Sostituzioni prezzo data di validità** ti consente di impostare questa modifica come sostituzione della riga per quel prezzo di ruolo specifico. Pertanto, non è necessario copiare l'intero listino prezzi e modificare il prezzo di una sola riga.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Sostituzioni del prezzo in vigore in base alla data per il prezzo della manodopera

Il processo di impostazione delle sostituzioni dei prezzi in base alla data per il tempo di lavoro su un progetto consiste in due passaggi fondamentali.

1. Abilita la funzionalità **Sostituzioni prezzo data di validità**.
1. Sostituzione per data di validità di prezzi specifici.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Abilita la funzionalità Sostituzioni prezzo data di validità

> [!NOTE]
> Dopo aver abilitato la funzione **Sostituzioni prezzo data di validità**, non può essere disabilitata.

Per abilitare la funzionalità **Sostituzioni prezzo data di validità**, attieniti alla seguente procedura.

1. Vai a **Impostazioni** \> **Parametri**.
1. Apri il record **Parametti**.
1. Nel riquadro azioni, nella scheda **Controllo funzionalità**, seleziona **Abilita sostituzioni prezzo data di validità**.
1. Nella finestra di dialogo di conferma seleziona **OK**.
1. Dopo qualche istante, aggiorna il browser. Ora dovrebbero essere disponibili funzionalità di sostituzione del prezzo in base alla data. Saprai che queste funzionalità sono state abilitate se **Abilita sostituzioni prezzo data di validità** non viene più visualizzato nel riquadro azioni.

### <a name="set-up-a-date-effective-price-override"></a>Sostituzione per data di validità di prezzi specifici

Le sostituzioni prezzo data di validità possono essere configurate nei listini prezzi **Costo**, **Vendite** o **Acquisto**.

> [!NOTE]
>Il comportamento di **Sostituzioni prezzo data di validità** attualmente presenta le seguenti limitazioni:
>
> - Solo i prezzi dei ruoli e i ricarichi dei prezzi dei ruoli supportano la funzionalità **Sostituzioni prezzo data di validità** funzione in Project Operations.
> - Quando si copia un listino prezzi utilizzando l'azione **Copia** nella pagina **Dettagli Listino Prezzi** e quando si crea un listino prezzi di progetto da un listino prezzi standard o personalizzato durante la creazione del contratto, le sostituzioni dei prezzi in base alla data di validità **non** vengono copiate dal listino prezzi di origine.

Per impostare una sostituzione del prezzo in vigore per data per un prezzo del ruolo o un markup del prezzo del ruolo, attieniti alla seguente procedura.

1. Apri la pagina del listino prezzi per il quale si desidera impostare la sostituzione del prezzo in base alla data di entrata in vigore.
1. Seleziona la scheda **Prezzi ruolo**. Questa scheda elenca tutti i record **Prezzo ruolo** nel listino prezzi.
1. Seleziona il record **Prezzo ruolo** per il quale desideri impostare un nuovo prezzo di sostituzione in base alla data, quindi tocca due volte (o fai doppio clic su) **Prezzo ruolo** per aprire la pagina **Dettagli prezzo ruolo**.
1. Seleziona la scheda **Sostituzioni data di validità**. La griglia in questa scheda elenca tutte le sostituzioni dei prezzi in vigore per il record **Prezzo ruolo** selezionato.
1. Nella barra degli strumenti sopra la griglia, seleziona **Sostituzione prezzo nuovo ruolo**. Viene visualizzato il dispositivo di scorrimento **Sostituzione prezzo nuovo ruolo**.
1. Specificare la data di decorrenza, l'unità e il nuovo prezzo per la sostituzione del prezzo. Quindi seleziona **Salva** e chiudi il modulo.

> [!NOTE]
> - Una sostituzione del prezzo in vigore per data per un prezzo del ruolo o un ricarico del prezzo del ruolo è applicabile alla stessa combinazione di valori della dimensione del prezzo che esiste nell'elemento padre **Prezzo ruolo** o nella riga **Ricarico prezzo ruolo**.
> - La data selezionata nel campo **Data inizio validità** deve rientrare nelle date di validità del listino prezzi principale. La sostituzione del prezzo avrà effetto dalla data selezionata nel campo **Data inizio validità** e si applicherà fino alla fine della data di fine del listino prezzi principale. Se imposti un'altra sostituzione del prezzo con decorrenza dalla data per lo stesso prezzo del ruolo, la prima sostituzione del prezzo avrà effetto alla data selezionata nel campo **Data inizio validità** e si applicherà fino all'inizio della seconda sostituzione.

## <a name="examples"></a>Esempi

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Esempio 1: determinazione della data di inizio validità per un prezzo del ruolo con sostituzioni del prezzo del ruolo

L'esempio seguente mostra come viene determinata la data di inizio validità per un prezzo del ruolo specifico per il quale sono impostate le sostituzioni del prezzo del ruolo.

**Listino prezzi A: dal 1 gennaio al 30 giugno**

*Prezzo ruolo*

| Prezzo ruolo | Unità | Prezzo | Inizio validità sui prezzi per le transazioni in entrata |
|---|---|---|---|
| Tecnico di rete | Ora | 100 | Questo prezzo verrà utilizzato su tutte le transazioni la cui data di transazione è compresa tra il 1 gennaio e il 14 marzo. |

*Sostituzione prezzo ruolo*

| Data inizio validità | Unità | Prezzo | Inizio validità sui prezzi per le transazioni in entrata |
|---|---|---|---|
| Marzo 15 | Ora | 110 | Questo prezzo verrà utilizzato su tutte le transazioni la cui data di transazione è compresa tra il 15 e il 30 marzo. |
| Aprile 1 | Ora | 120 | Questo prezzo verrà utilizzato su tutte le transazioni la cui data di transazione è compresa tra il 1 aprile e il 30 giugno. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Esempio 2: determinazione della data di inizio validità per il ricarico di un prezzo del ruolo con sostituzioni del ricarico del prezzo del ruolo

L'esempio seguente mostra come viene determinata la data di inizio validità per un prezzo di ricarico del ruolo specifico per il quale sono impostate le sostituzioni del prezzo di ricarico del ruolo.

**Listino prezzi A: dal 1 gennaio al 30 giugno**

*Prezzo ruolo*

| Prezzo ruolo | Orario di lavoro | Unità | Prezzo | Inizio validità sui prezzi per le transazioni in entrata |
|---|---|---|---|---|
| Tecnico di rete | Regolare | Ora | 100 | Questo prezzo verrà utilizzato su tutte le transazioni la cui data di transazione è compresa tra il 1 gennaio e il 14 marzo. |

*Ricarico prezzo ruolo*

| Unità organizzativa | Orario di lavoro | % di ricarico |
|---|---|---|
| Contoso US | Straordinario | 10% |

*Sostituzione del ricarico del prezzo del ruolo*

| Data inizio validità | Prezzo | Inizio validità sui prezzi per le transazioni in entrata |
|---|---|---|
| Marzo 15 | 20% | Questa percentuale di ricarico verrà utilizzata su tutte le transazioni la cui data di transazione è compresa tra il 15 e il 30 marzo. |
| Aprile 1 | 25% | Questo ricarico verrà utilizzato su tutte le transazioni la cui data di transazione è compresa tra il 1 aprile e il 30 giugno. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
