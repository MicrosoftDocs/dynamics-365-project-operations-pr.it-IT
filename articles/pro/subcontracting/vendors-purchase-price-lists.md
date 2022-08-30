---
title: Gestione listini fornitori e acquisti in Project Operations
description: Questo articolo fornisce informazioni che ti aiuteranno a creare e gestire i dati del fornitore e i listini prezzi di acquisto per il conto lavoro.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3cd883fed8a59f1c54c39e2d051b9748833ba692
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261892"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Gestione listini fornitori e acquisti in Project Operations


_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

## <a name="vendors-in-project-operations"></a>Fornitori in Project Operations

In Microsoft Dynamics 365 Project Operations, i conti fornitore hanno una relazione di tipo **fornitore** o **venditore**. Puoi selezionare solo un record di account che ha uno di questi tipi di relazione come fornitore su un conto lavoro.

Puoi associare uno o più listini prezzi di acquisto a un record fornitore. Tuttavia, ogni listino prezzi di acquisto associato a un record fornitore deve avere una data di validità distinta. Project Operations non supporta la sovrapposizione di date di validità nei listini prezzi di acquisto.

Per impostazione predefinita, i seguenti campi e concetti in un record fornitore vengono utilizzati per qualsiasi conto lavoro creato per il fornitore:

- Condizioni di pagamento
- Contatto fatturazione
- Contatto primario

    > [!NOTE]
    > Per impostazione predefinita, il referente principale del fornitore viene utilizzato come account manager del fornitore del conto lavoro.

- Valuta
- Listini di acquisto correnti

## <a name="purchase-price-lists-in-project-operations"></a>Listini di acquisto in Project Operations

Un listino prezzi dove il campo **Contesto** è impostato su **Acquisto** è considerato un listino prezzi di acquisto. I listini prezzi di acquisto possono essere definiti per rappresentare un catalogo di tariffe di acquisto per tempi, spese e materiali. I listini prezzi di acquisto sono simili ai listini prezzi di vendita e di costo in Project Operations. I seguenti concetti si applicano ai listini prezzi di acquisto nello stesso modo in cui si applicano ai listini prezzi di costo e di vendita:

- **Data di validità** – I listini prezzi di acquisto hanno validità per data. La data di validità è rappresentata dai campi della data di inizio e della data di fine su ciascun listino prezzi. L'intervallo di tempo tra la data di inizio e la data di fine è il periodo della data di validità.
- **Valuta** – La valuta nell'intestazione del listino prezzi viene utilizzata come valuta in cui sono espressi i prezzi di acquisto per manodopera, categorie di spesa e prodotti nel catalogo.
- **Unità di tempo predefinita** – L'unità di tempo predefinita esprime i prezzi della manodopera per gli acquisti. Il campo dell'unità di tempo in un listino prezzi viene utilizzato solo per fornire un valore predefinito. Tale valore può essere modificato nelle singole righe del prezzo del ruolo.

I listini prezzi di acquisto possono essere associati ai record fornitore come associazioni note come listini prezzi di progetto. Questi listini prezzi vengono utilizzati per immettere i prezzi predefiniti nelle righe del contratto di conto lavoro. Per impostazione predefinita, quando a un record fornitore sono associati più listini prezzi di acquisto, per i conti lavoro creati per il fornitore viene utilizzato il listino prezzi più aggiornato. Solo i listini prezzi dove il campo **Contesto** è impostato su **Acquisto** possono essere associati ai record del fornitore.

### <a name="subcontract-specific-purchase-price-lists"></a>Listini prezzi di acquisto specifici per il conto lavoro

I listini prezzi di acquisto possono anche essere associati ai conti lavoro come associazioni note come listini prezzi di progetto. Questi listini prezzi vengono utilizzati per immettere i prezzi predefiniti nelle righe del contratto di conto lavoro. Per impostazione predefinita, quando più listini prezzi di acquisto sono associati a un conto lavoro, ciascuno deve avere una data di validità distinta. Project Operations non supporta i listini prezzi di acquisto con sovrapposizione della data di validità. Solo i listini prezzi dove il campo **Contesto** è impostato su **Acquisto** possono essere associati ai conti lavoro.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
