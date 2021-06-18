---
title: Creare campi ed entità personalizzati come dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni su come creare entità o set di opzioni personalizzati.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000531"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Creare campi ed entità personalizzati come dimensioni di determinazione dei prezzi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Completa i passaggi seguenti quando intendi creare un set di opzioni o un'entità per usarla come dimensione di determinazione dei prezzi. Per ulteriori informazioni, vedi [Panoramica delle dimensioni di determinazione dei prezzi](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Ti consigliamo di apportare le modifiche alle dimensioni di determinazione dei prezzi personalizzate in una soluzione distinta. Questa importante best practice offre flessibilità in futuro per aggiornare o rimuovere le modifiche secondo necessità. Ciò aiuterà anche il riutilizzo del tuo lavoro e renderà più facile trasferire queste modifiche su un'altra istanza. Dopo aver apportato tutte le modifiche richieste, esporta questa soluzione come **Soluzione gestita** e importala in altre istanze per riutilizzare la configurazione dei prezzi.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Creare campi e set di opzioni personalizzati nella soluzione per le dimensioni di determinazione dei prezzi

Una dimensione di determinazione dei prezzi può essere un set di opzioni o un'entità. Entrambi devono essere creati nella soluzione per la determinazione dei prezzi. I passaggi in questa procedura illustrano il modo in cui creare dimensioni basate su entità e dimensioni basate su set di opzioni.

### <a name="entity-based-dimensions"></a>Dimensioni basata su entità
Per creare dimensioni basate su entità, segui questi passaggi:

1. Vai a **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità**.
3. Seleziona **Nuovo** per creare una nuova entità denominata **Titolo standard**. 
4. Immetti le altre informazioni e quindi seleziona **Salva**.

> ![Definizione dell'entità Titolo standard](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensioni basate su set di opzioni 
Puoi creare due dimensioni basate su set di opzioni. 

- Utilizzare **Ubicazione lavoro risorsa** per monitorare il prezzo della posizione del lavoro presso **Casa** o **In loco**. 
- Utilizzare **Ore lavorative della risorsa** con valori **Regolare** e **Straordinario** per applicare un markup quando il lavoro è completo.

Il grafico seguente fornisce una visualizzazione della dimensione **Ubicazione lavoro risorsa**. 

> ![Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ubicazione lavoro risorsa](media/Option-set-PD-called-Resource-Work-Location.png)

Il grafico seguente fornisce una visualizzazione della dimensione **Ore lavoro risorsa**. 

> ![Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ore lavorative risorsa](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Vai a **Impostazioni** > **Soluzioni** e fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Set di opzioni**. 
3. Seleziona **Nuovo** per creare un nuovo set di opzioni, immetti le altre informazioni richieste e quindi seleziona **Salva**.

## <a name="create-data-for-entity-based-dimensions"></a>Creare dati per le dimensioni basate su entità

Puoi creare dati per le dimensioni basate su entità manualmente oppure utilizzando le chiamate di importazione o di servizio di Microsoft Excel. Utilizza i passaggi in questa procedura per creare due titoli standard, **Sistemista** e **Sistemista esperto**, a partire dalla dimensione basata su entità **Titolo standard**. Se intendi creare pochi dati, come illustrato nel seguente esempio, puoi utilizzare un modulo standard.

1. Selezionare **Ricerca avanzata**.
2. Seleziona l'entità **Titolo standard**, quindi seleziona **Risultati**. Tutte le righe nell'entità **Titolo standard** verranno visualizzate.
3. Seleziona **Nuovo** e nel campo **Nome** immetti "Systems Engineer" e seleziona **Salva**.
4. Chiudi la pagina. 
5. Ripeti i passaggi da 1 a 3 per creare un altro titolo standard, ovvero "Sistemista esperto".

> ![Dati di esempio per l'entità Titolo standard](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]