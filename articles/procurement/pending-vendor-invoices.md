---
title: Acquistare materiali non stoccati con una fattura fornitore in sospeso
description: Questo argomento spiega come registrare le fatture fornitore in sospeso.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547294"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Acquistare materiali non stoccati con una fattura fornitore in sospeso

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Poiché un'azienda acquista materiali non stoccati per un progetto, i costi possono essere immediatamente registrati a fronte del progetto. 

Ad esempio, Contoso Robotics US sta eseguendo un progetto di rinnovo delle apparecchiature e necessita di licenze software. Queste licenze vengono acquistate da un fornitore di terze parti.  Utilizzando Dynamics 365 Finance, l'addetto alla contabilità fornitori registra un documento di fattura fornitore in sospeso e attribuisce i costi della licenza direttamente al progetto di rinnovo dell'attrezzatura. 

> [!IMPORTANT]
> Prima di utilizzare la funzionalità descritta in questo argomento, esamina e applica le configurazioni richieste. Per ulteriori informazioni, vedi [Abilitare materiali non stoccati e fatture fornitore in sospeso](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Registrare una fattura fornitore in sospeso relativa al progetto 

Le fatture fornitore in sospeso possono essere registrate nella pagina **Fatture fornitore in sospeso** (**Contabilità fornitori** > **Fatture** > **Fatture fornitore in sospeso**). Completa i seguenti passaggi per registrare una fattura fornitore in sospeso relativa al progetto:

1. Vai a **Contabilità fornitori** > **Fatture** e seleziona **Nuovo**. 
2. Nel campo **Conto fattura** seleziona un fornitore e nel campo **Numero**, immetti l'identificazione della fattura del fornitore.
3. Aggiungi una riga alla fattura fornitore e nel campo **Codice articolo** seleziona l'articolo non stoccato acquistato dal fornitore. 

    > [!NOTE]
    > Le righe della fattura fornitore basate su una categoria di approvvigionamento non possono essere registrate nel progetto. 
    
5. Aggiungi la quantità acquistata. Il sistema popolerà il prezzo unitario in base alla configurazione del prezzo dell'articolo non stoccato. 
6. Verifica l'importo totale e altri dettagli richiesti sulla riga.
7. Nei dettagli della linea, nella scheda **Progetto** seleziona l'ID del progetto in cui verrà registrato l'elemento.
8. Facoltativamente, seleziona il numero dell'attività e aggiorna la categoria del progetto e la proprietà della riga.
9. Registra la fattura fornitore in sospeso. Quando la fattura viene registrata, il sistema registra:
    
    - L'importo del saldo del fornitore.
    - L'importo dell'IVA.
    - Il costo relativo al progetto viene registrato nel conto di integrazione dell'approvvigionamento.
    - La transazione del costo effettivo del progetto in Dataverse.  Questa transazione viene ulteriormente elaborata utilizzando il [giornale di integrazione Project Operations](../project-accounting/project-operations-integration-journal.md). La registrazione di questo giornale di registrazione sposta l'importo dal conto di integrazione dell'approvvigionamento al conto dei costi del progetto. 
    - Acquisti fatturati al cliente del progetto utilizzando il metodo di fatturazione tempi e materiali. Inoltre, vengono create transazioni di vendita non fatturate per gli acquisti in Dataverse. Il listino prezzi dei prodotti in Dataverse viene utilizzato per i prezzi di vendita e gli importi per le transazioni di vendita non fatturate.
