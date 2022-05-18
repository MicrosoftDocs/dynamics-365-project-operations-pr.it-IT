---
title: Ordinare materiali non stoccati per un progetto utilizzando gli ordini di acquisto per un progetto
description: Questo argomento spiega come ordinare materiali non stoccati per un progetto utilizzando gli ordini di acquisto per un progetto.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2aa8fb94e2f9cbf91182f3f169339284d3eb9f44
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612708"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Ordinare le categorie di approvvigionamento o i materiali non stoccati per un progetto utilizzando gli ordini di acquisto di progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Il reparto Approvvigionamento della tua organizzazione potrebbe utilizzare [ordini di acquisto](/dynamics365/supply-chain/procurement/purchase-order-overview) per tenere traccia degli ordini di beni e servizi. Gli ordini di acquisto per categorie di approvvigionamento o materiali non stoccati possono essere attribuiti a un progetto. La fatturazione di questi ordini di acquisto registra il costo sul progetto.

## <a name="prerequisites"></a>Prerequisiti
Completare i seguenti passaggi per abilitare la funzionalità degli ordini di acquisto del progetto.

1. In Dynamics 365 Finance, vai all'area di lavoro **Gestione funzionalità**.
2. Nell'elenco delle funzionalità, trova e seleziona la funzionalità, **Abilita gli ordini di acquisto del progetto su Project Operations per scenari basati su risorse/non stoccate**.
3. Selezionare **Abilita**.
4. Configura i materiali non stoccati e le fatture fornitore in sospeso come descritto in [Configura materiali non stoccati e fatture fornitore in sospeso](configure-materials-nonstocked.md).
5. Configura le categorie di approvvigionamento come descritto in [Utilizzare le categorie di approvvigionamento con ordini di acquisto di progetto e fatture fornitore in sospeso](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Creare un ordine di acquisto del progetto dall'elenco degli ordini di acquisto del progetto

1. In Finance, vai a **Gestione progetti e contabilità** > **Progetti** > **Tutti i progetti** e seleziona un progetto.
2. Nel riquadro Azioni, nella scheda **Gestisci**, nel gruppo **Nuovo**, seleziona **Attività articolo** > **Ordine di acquisto**.
3. Nella pagina **Crea ordine di acquisto**, seleziona il fornitore con cui si desidera effettuare l'ordine di acquisto, inserisci altre informazioni appropriate, quindi seleziona **OK**.
4. Nella pagina **Ordine di acquisto**, seleziona la griglia **Righe ordine fornitore** e **Aggiungi riga**.
5. Immetti un numero di articolo o una categoria di approvvigionamento, una quantità, un'unità, un prezzo unitario e altre informazioni a seconda dei casi.

    > [!NOTE]
    > Solo le categorie di approvvigionamento, gli articoli non stoccati e i servizi possono essere utilizzati con gli ordini di acquisto del progetto. Gli articoli stoccati non sono supportati.

6. Continua ad aggiungere articoli o categorie di approvvigionamento come richiesto e conferma l'ordine di acquisto.

    Le ricevute di merci e servizi possono essere registrate creando e registrando una ricevuta per i prodotti.

    > [!NOTE]
    > Le ricevute dei prodotti non vengono registrate nei valori effettivi del progetto in Microsoft Dataverse e non influiscono sul giornale di registrazione secondario del progetto.

    Dopo che un fornitore ha inviato la fattura per articoli e servizi nell'ordine di acquisto, il reparto acquisti può generare una fattura per l'ordine di acquisto accedendo a **Fattura** > **Genera** > **Fattura** nel riquadro Azioni. Per ulteriori informazioni sulle fatture fornitore in sospeso, vedi [Acquistare materiali non stoccati utilizzando una fattura fornitore in sospeso](pending-vendor-invoices.md).
