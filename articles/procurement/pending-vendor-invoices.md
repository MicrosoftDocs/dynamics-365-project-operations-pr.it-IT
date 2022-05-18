---
title: Acquistare materiali non stoccati o categorie di approvvigionamento utilizzando una fattura fornitore in sospeso
description: Questo argomento spiega come registrare le fatture fornitore in sospeso.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612662"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Acquistare materiali non stoccati o categorie di approvvigionamento utilizzando una fattura fornitore in sospeso

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Poiché un'azienda acquista materiali non stoccati o categorie di approvvigionamento per un progetto, i costi possono essere immediatamente registrati sul progetto. 

Ad esempio, Contoso Robotics US sta eseguendo un progetto di rinnovo delle apparecchiature e necessita di licenze software. Queste licenze vengono acquistate da un fornitore di terze parti.  Utilizzando Dynamics 365 Finance, l'addetto alla contabilità fornitori registra un documento di fattura fornitore in sospeso e attribuisce i costi di licenza direttamente al progetto di rinnovo dell'attrezzatura. 

> [!IMPORTANT]
> Prima di utilizzare la funzionalità descritta in questo argomento, esamina e applica le configurazioni richieste. Per ulteriori informazioni, vedi [Abilita materiali non stoccati e fatture fornitore in sospeso](configure-materials-nonstocked.md) e [Utilizzare le categorie di approvvigionamento con ordini di acquisto di progetto e fatture fornitore in sospeso](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Registrare una fattura fornitore in sospeso relativa al progetto 

Le fatture fornitore in sospeso possono essere registrate nella pagina **Fatture fornitore in sospeso** (**Contabilità fornitori** > **Fatture** > **Fatture fornitore in sospeso**). Completa i seguenti passaggi per registrare una fattura fornitore in sospeso relativa al progetto:

1. Vai a **Contabilità fornitori** > **Fatture** e seleziona **Nuovo**. 
1. Nel campo **Conto fatture** seleziona un fornitore e quindi nel campo **Numero** immetti l'identificazione della fattura fornitore.
1. Aggiungi una riga alla fattura fornitore, quindi, nel campo **Numero articolo** seleziona l'articolo non stoccato acquistato dal fornitore. In alternativa, nel campo **Categoria approvvigionamento** seleziona la categoria di approvvigionamento acquistata dal fornitore.   
1. Aggiungi la quantità che è stata acquistata. Il sistema inserisce il prezzo unitario in base alla configurazione del prezzo dell'articolo non stoccato. 
1. Verifica l'importo totale e altri dettagli richiesti sulla riga.
1. Nei dettagli di riga, sulla scheda **Progetto** seleziona l'ID del progetto in cui verrà registrato questo articolo.
1. Facoltativo: seleziona il numero dell'attività e aggiorna la categoria del progetto e la proprietà della riga.
1. Registra la fattura fornitore in sospeso. Quando la fattura viene registrata, il sistema registra le seguenti informazioni:
    
    - L'importo del saldo del fornitore.
    - L'importo dell'IVA.
    - Il costo relativo al progetto viene registrato nel conto di integrazione dell'approvvigionamento.
    - La transazione del costo effettivo del progetto in Dataverse.  Questa transazione viene ulteriormente elaborata utilizzando il [giornale di integrazione Project Operations](../project-accounting/project-operations-integration-journal.md). La registrazione di questo giornale di registrazione sposta l'importo dal conto di integrazione dell'approvvigionamento al conto dei costi del progetto. 
    - Acquisti fatturati al cliente del progetto utilizzando il metodo di fatturazione tempi e materiali. Inoltre, vengono create transazioni di vendita non fatturate per gli acquisti in Dataverse. Il listino prezzi dei prodotti in Dataverse viene utilizzato per i prezzi di vendita e gli importi per le transazioni di vendita non fatturate.
