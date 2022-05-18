---
title: Configurare listini prezzi
description: Questo argomento fornisce informazioni su come configurare i listini prezzi di costo e di vendita.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 77809f63230530e2e6553b76e56d37249b060ab9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584739"
---
# <a name="set-up-price-lists"></a>Configurare listini prezzi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

I listini prezzi in Dynamics 365 Project Operations rappresentano un catalogo di tariffe. Le tariffe sono per costo, vendita e fatturazione. A seconda che il listino prezzi esprima tariffe di costo o tariffe di vendita e fatturazione, il contesto del listino è **Vendita** o **Costo**.

Le seguenti estensioni sono specifiche per Project Operations e vengono applicate ai listini prezzi di Dynamics 365 Sales.

- **Contesto**: questo campo ha i valori supportati, **Costo** e **Vendita**. Il valore **Acquisto** non è supportato. Imposta il contesto su **Costo** per creare un listino prezzi di costo o impostare il contesto su **Vendita** per un listino prezzi di vendita. I listini prezzi di costo risolvono il prezzo per il tipo di costo nei record delle stime e dei valori effettivi. I listini prezzi di vendita risolvono il prezzo sui record stimati ed effettivi dei tipi di vendita non fatturati e fatturati.
- **Unità di tempo**: questa è l'unità di tempo predefinita per la quale viene impostato il prezzo nella relativa tabella **Prezzo ruolo** per questo listino prezzi.
- **Entità listino prezzi**: questo campo nascosto viene utilizzato da Project Operations per differenziare i listini prezzi specifici per offerta o contratto da quelli standard e applicabili a livello globale.

## <a name="price-list-header"></a>Intestazione listino prezzi

La tabella seguente include i campi della scheda **Generale** di un listino prezzi che sono univoci per Project Operations o presentano cambiamenti significativi nel comportamento dai listini prezzi in Sales.

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| Nome | Scheda **Generale** e moduli **Creazione rapida** | L'identità del listino prezzi. | Il listino prezzi viene visualizzato con questo valore in tutte le pagine dell'elenco e nelle opzioni a discesa.|
| Contesto | Scheda **Generale** e moduli **Creazione rapida** | Questo campo può essere impostato su **Costo** o **Vendita**. | Un listino prezzi impostato su **Costo** viene utilizzato per cercare il prezzo per le stime dei costi e i costi effettivi. Un listino prezzi impostato su **Vendita** viene utilizzato per cercare il prezzo per le stime di vendita e le vendite effettive. Solo i listini prezzi che hanno il contesto impostato su **Vendite** possono essere collegati a listini prezzi di progetto per clienti, offerte di progetto o contratti di progetto. |
| Data di inizio | Scheda **Generale** e moduli **Creazione rapida** | La data di inizio del periodo di validità del listino prezzi. | Con il campo **Data di fine**, questo campo viene utilizzato per determinare quale listino prezzi è applicabile per una determinata riga di stima o valore effettivo. |
| Data di fine | Scheda **Generale** e moduli **Creazione rapida** | La data di fine del periodo di validità del listino prezzi. | Con il campo **Data di inizio**, questo campo viene utilizzato per determinare quale listino prezzi è applicabile per una determinata riga di stima o valore effettivo. |
| Valuta | Scheda **Generale** e moduli **Creazione rapida** | Questo campo viene utilizzato per impostare la valuta predefinita per ogni ruolo, categoria o voce di listino prezzi correlata a questo listino prezzi. | Nei listini prezzi di **vendita**, ruoli, categorie o voci di listino non possono essere creati in valute diverse da questa valuta. Nei listini prezzi di **costo** puoi creare una riga di prezzo per il ruolo in qualsiasi valuta. La valuta qui definita viene utilizzata come predefinita. L'impostazione dell'utente correlata ai prezzi del ruolo può sostituire questo valore per abilitare l'impostazione della tariffa del costo del lavoro in qualsiasi valuta. Le tariffe di costo delle categorie e i costi delle voci di listino possono essere impostati solo nella valuta qui definita. |
| Unità di tempo | Scheda **Generale** e moduli **Creazione rapida** | Questo campo viene utilizzato per impostare l'unità di tempo predefinita per ogni ruolo correlato a questo listino prezzi. | Il valore di questo campo viene utilizzato solo per l'impostazione del prezzo del ruolo correlato. Nei listini prezzi di **costo** e **vendita** puoi creare una riga di prezzo per il ruolo in qualsiasi unità di tempo. L'unità di tempo qui definita viene utilizzata come predefinita. L'impostazione dell'utente correlata ai prezzi del ruolo può sostituire questo valore per abilitare l'impostazione della tariffa del costo della fatturazione del lavoro in qualsiasi unità di tempo. |
| Descrizione | Scheda **Generale** e moduli **Creazione rapida** | Questo è un campo di testo che permette di inserire una descrizione su più righe del listino prezzi. | Questo campo è mostrato nelle visualizzazioni **associate** nel listino prezzi di varie entità che hanno relativi listini prezzi. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]