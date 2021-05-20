---
title: Acquistare materiali non stoccati con una fattura fornitore in sospeso
description: Questo argomento spiega come registrare le fatture fornitore in sospeso.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880656"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Acquistare materiali non stoccati con una fattura fornitore in sospeso

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Poiché un'azienda acquista materiali non stoccati per un progetto, i costi possono essere immediatamente registrati a fronte del progetto. 

Per esempio, Contoso Robotics US sta eseguendo un progetto di rinnovo delle apparecchiature e necessita di licenze software. Queste licenze vengono acquistate da un fornitore di terze parti.  Utilizzando Dynamics 365 Finance, l'addetto alla contabilità fornitori registra un documento di fattura fornitore in sospeso e attribuisce i costi della licenza direttamente al progetto di rinnovo dell'attrezzatura. 

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
    - La transazione effettiva del progetto in Dataverse. Questa transazione viene ulteriormente elaborata utilizzando il [giornale di integrazione Project Operations](../project-accounting/project-operations-integration-journal.md). La registrazione di questo giornale di registrazione sposta l'importo dal conto di integrazione dell'approvvigionamento al conto dei costi del progetto.
