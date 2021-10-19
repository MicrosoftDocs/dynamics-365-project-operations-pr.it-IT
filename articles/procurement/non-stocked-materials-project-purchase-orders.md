---
title: Ordinare materiali non stoccati per un progetto utilizzando gli ordini di acquisto per un progetto
description: Questo argomento spiega come ordinare materiali non stoccati per un progetto utilizzando gli ordini di acquisto per un progetto.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563027"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Ordinare materiali non stoccati per un progetto utilizzando gli ordini di acquisto per un progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Il reparto Approvvigionamento della tua organizzazione potrebbe utilizzare [ordini di acquisto](/dynamics365/supply-chain/procurement/purchase-order-overview) per tenere traccia degli ordini di beni e servizi. Gli ordini di acquisto per i materiali non stoccati possono essere attribuiti a un progetto. La fatturazione di questi ordini di acquisto registra il costo sul progetto.

## <a name="prerequisites"></a>Prerequisiti
Completare i seguenti passaggi per abilitare la funzionalità degli ordini di acquisto del progetto.

1. In Dynamics 365 Finance, vai all'area di lavoro **Gestione delle funzionalità** workspace.
2. Nell'elenco delle funzionalità, trova e seleziona la funzionalità, **Abilita gli ordini di acquisto del progetto su Project Operations per scenari basati su risorse/non stoccate**.
3. Selezionare **Abilita**.
4. Configura i materiali non stoccati e le fatture fornitore in sospeso come descritto in [Configura materiali non stoccati e fatture fornitore in sospeso](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Creare un ordine di acquisto del progetto dall'elenco degli ordini di acquisto del progetto

1. In Finance, vai a **Gestione progetti e contabilità** > **Progetti** > **Tutti i progetti** e seleziona un progetto.
2. Nel riquadro Azioni, nella scheda **Gestisci**, nel gruppo **Nuovo**, seleziona **Attività articolo** > **Ordine di acquisto**.
3. Nella pagina **Crea ordine di acquisto**, seleziona il fornitore con cui si desidera effettuare l'ordine di acquisto, inserisci altre informazioni appropriate, quindi seleziona **OK**.
4. Nella pagina **Ordine di acquisto**, seleziona la griglia **Righe ordine fornitore** e **Aggiungi riga**.
5. Immetti un numero di articolo, una quantità, un'unità, un prezzo unitario e altre informazioni a seconda dei casi.

    > [!NOTE]
    > Solo gli articoli e i servizi non stoccati possono essere utilizzati con gli ordini di acquisto del progetto. Gli articoli stoccati e le categorie di approvvigionamento non sono supportati.

6. Continua ad aggiungere articoli come richiesto e conferma l'ordine di acquisto.

    Le ricevute di merci e servizi possono essere registrate creando e registrando una ricevuta per i prodotti.

    > [!NOTE]
    > Le ricevute dei prodotti non vengono registrate nei valori effettivi del progetto in Microsoft Dataverse e non influiscono sul giornale di registrazione secondario del progetto.

    Dopo che un fornitore ha inviato la fattura per articoli e servizi nell'ordine di acquisto, il reparto acquisti può generare una fattura per l'ordine di acquisto accedendo a **Fattura** > **Genera** > **Fattura** nel riquadro Azioni. Per ulteriori informazioni sulle fatture fornitore in sospeso, vedi [Acquistare materiali non stoccati utilizzando una fattura fornitore in sospeso](pending-vendor-invoices.md).
