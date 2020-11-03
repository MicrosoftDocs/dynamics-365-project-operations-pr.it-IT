---
title: Configurare le categorie di spesa
description: Questo argomento fornisce informazioni su come configurare le categorie di spesa e le categorie condivise per le note spese.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078766"
---
# <a name="set-up-expense-categories"></a>Configurare le categorie di spesa

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Quando i dipendenti creano note spese, ogni spesa che registrano deve essere associata a una categoria di spesa. Le categorie di spesa derivano da categorie condivise che possono essere condivise tra le persone giuridiche dell'organizzazione. A seconda di come è definita l'organizzazione, queste categorie di spesa possono essere condivise anche in altre aree. In base alla definizione dell'organizzazione e alle linee guida del team di implementazione, è necessario determinare se le categorie utilizzate nella gestione delle spese verranno utilizzate solo in Gestione spese o debbano essere condivise in altre aree.

> [!NOTE]
> Queste categorie possono essere condivise tra Gestione progetti e contabilità e Gestione spese oppure tra Gestione progetti e contabilità e Produzione. Tuttavia, non possono essere condivise tra Gestione spese e Produzione.

Prima di poter iniziare il processo di configurazione, è necessario prendere le seguenti decisioni per ciascuna categoria di spesa:

- Qual è la categoria di spesa? Gli esempi includono categorie per voli, hotel o chilometraggio.
- La categoria di spesa può essere utilizzata anche in Gestione progetti e contabilità? In caso affermativo, devi anche prendere le decisioni seguenti:

    - Quali conti di costo verranno utilizzati per le seguenti spese?

        - Costo
        - Allocazione retribuzioni
        - WIP - valore costo
        - Elemento di costo
        - WIP - elemento valore di costo
        - Perdita maturata
        - WIP - perdita maturata

    - Quali conti ricavi verranno utilizzati per le seguenti fonti di ricavi?

        - Ricavi fatturati
        - Ricavi maturati - valore delle vendite
        - WIP - valore delle vendite
        - Ricavi maturati - produzione
        - WIP - produzione
        - Ricavi maturati - profitti
        - WIP - profitti
        - Ricavi maturati - abbonamento
        - WIP - abbonamento

- Qual è il tipo di spesa?
- Qual è il metodo di pagamento predefinito per la categoria di spesa?
- Le spese nella categoria di spesa devono essere dettagliate?
- Qual è il conto predefinito principale per la categoria di spesa?
- Qual è la fascia IVA articoli predefinita per la categoria di spesa?
- Sono consentiti metodi di pagamento aggiuntivi per la categoria di spesa? In caso affermativo, quali?
- Ci sono sottocategorie in questa categoria di spesa? In caso affermativo, devi anche prendere le decisioni seguenti:

    - Alcune delle sottocategorie sono escluse dal recupero IVA?
    - Qual è la fascia IVA articoli delle sottocategorie?
