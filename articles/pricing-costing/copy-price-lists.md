---
title: Copiare listini prezzi
description: Questo argomento fornisce informazioni su come copiare i listini prezzi in Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad09bdce563a48843b3ed96e7aaabd9c0d5960336b9e1c74fddb9b61f760f4cd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003731"
---
# <a name="copy-price-lists"></a>Copiare listini prezzi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi creare copie dei listini prezzi in Dynamics 365 Project Operations. Ad esempio, puoi creare listini prezzi per l'anno successivo utilizzando un listino prezzi dell'anno in corso.  In alternativa, puoi copiare un listino prezzi per le tariffe di fatturazione e i prezzi di vendita dai listini prezzi per il costo. 

Per fare una copia del listino prezzi, completa i seguenti passaggi.

1. Apri il listino prezzi di cui vuoi fare una copia e seleziona **Copia**.
2. Immetti le informazioni necessarie per copiare il listino prezzi. La tabella seguente mostra le considerazioni da tenere presenti quando si immettono le informazioni.

| Campo | Descrizione | Impatto downstream |
| --- | --- | --- |
| Nome | Il nome del listino prezzi di origine con **-copia** aggiunto. | Il listino prezzi include questo valore in tutte le pagine dell'elenco e nelle opzioni a discesa. |
| Contesto | Inserisci il contesto che desideri per il listino prezzi di destinazione. | Un listino prezzi che ha il contesto impostato su **Costo** viene utilizzato per cercare il prezzo per le stime dei costi e i costi effettivi. Un listino prezzi che ha il contesto impostato su **Vendite** viene utilizzato per cercare il prezzo per le stime delle vendite e le vendite effettive. Solo i listini prezzi che hanno il contesto impostato su **Vendite** possono essere collegati a un listino prezzi di progetto per un cliente, un'offerta o un contratto. |
| Data di inizio | La data di inizio del periodo di validità del listino prezzi. | Insieme a **Data di fine**, questo campo viene utilizzato per determinare quale listino prezzi è applicabile per una determinata riga di stima o valore effettivo. |
| Data di fine | La data di fine del periodo di validità del listino prezzi. | Insieme a **Data di inizio**, questo campo viene utilizzato per determinare quale listino prezzi è applicabile per una determinata riga di stima o valore effettivo. |
| Valuta | La valuta del listino prezzi di origine. Questo valore può essere modificato. | Quando viene modificato, tutte le righe di prezzo risultanti per manodopera, spese e articoli del catalogo prodotti vengono convertite nella valuta del listino prezzi di destinazione durante la copia. |
| Unità di tempo | La valuta del listino prezzi di origine. Questo valore può essere modificato. | Quando viene modificato, tutte le righe di prezzo risultanti per articoli di manodopera vengono convertite nell'unità del listino prezzi di destinazione durante la copia. Viene utilizzata la conversione dall'impostazione dell'unità per l'unità di tempo del listino prezzi di origine e l'unità di tempo del listino prezzi di destinazione. |
| Descrizione | Una descrizione del listino prezzi di origine con **-copia** aggiunto. Questo è un campo di testo e permette di inserire una descrizione su più righe del listino prezzi. | Questo campo è mostrato nelle visualizzazioni **associate** nel listino prezzi di varie entità che hanno relativi listini prezzi. |

3. Salva il listino prezzi. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Aggiornare un listino prezzi applicando un ricarico a tutti i prezzi

1. Nelle schede **Ruolo**, **Categoria** e **Voce di listino** di un listino prezzi, è possibile selezionare **Aggiorna prezzi** per applicare un ricarico su tutti i prezzi nella griglia secondaria. 
2. Nella pagina di dialogo che si apre, inserisci un ricarico. Puoi anche inserire una percentuale di aumento negativa per diminuire i prezzi di una determinata percentuale. 
3. Seleziona **OK** nella pagina di dialogo e quindi verifica che i prezzi nella griglia secondaria riflettano le modifiche apportate.


[!INCLUDE[footer-include](../includes/footer-banner.md)]