---
title: Creare campi ed entità personalizzati come dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni su come creare entità o set di opzioni personalizzati.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078914"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Creare campi ed entità personalizzati come dimensioni di determinazione dei prezzi

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Completa i passaggi seguenti ogni volta che intendi creare un set di opzioni o un'entità personalizzato.

> [!IMPORTANT]
> Ti consigliamo di apportare le modifiche alle dimensioni di determinazione dei prezzi personalizzate in una soluzione distinta. Questo procedura consigliata importante fornisce flessibilità per aggiornamenti o rimozioni future delle modifiche, agevola il riutilizzo del lavoro e semplifica il trasferimento di tali modifiche a un'altra istanza. Dopo aver apportato tutte le modifiche necessarie, esporta questa soluzione come **Soluzione gestita** e importala in altre istanze per riutilizzare la configurazione per la determinazione dei prezzi.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Creare una soluzione personalizzata per le dimensioni di determinazione dei prezzi
1. Vai in **Impostazioni** > , **Soluzioni** e quindi seleziona **Nuovo** per creare una nuova soluzione. 
2. Assegna un nome alla soluzione, **dimensioni di determinazione dei prezzi di \<your organization name>** , immetti le informazioni richieste e quindi seleziona **Salva**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Creare campi e set di opzioni personalizzati nella soluzione per le dimensioni di determinazione dei prezzi

Una dimensione di determinazione dei prezzi può essere un set di opzioni o un'entità. Entrambi devono essere creati nella soluzione per la determinazione dei prezzi. I passaggi in questa procedura illustrano il modo in cui creare dimensioni basate su entità e dimensioni basate su set di opzioni.

### <a name="entity-based-dimensions"></a>Dimensioni basata su entità

1. Vai a **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità**.
3. Seleziona **Nuovo** per creare una nuova entità denominata **Titolo standard**. 
4. Immetti le altre informazioni e quindi seleziona **Salva**.


### <a name="option-set-based-dimensions"></a>Dimensioni basate su set di opzioni 
Puoi creare due dimensioni basate su set di opzioni. Utilizza **Ubicazione lavoro risorsa** per tenere traccia del prezzo del lavoro nell'ubicazione **Abitazione** e del lavoro **In loco** e utilizza **Ore lavorative risorsa** con i valori **Normale** e **Straordinario** per applicare un ricarico quando il lavoro è ultimato.


1. Vai a **Impostazioni** > **Soluzioni** e fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Set di opzioni**. 
3. Seleziona **Nuovo** per creare un nuovo set di opzioni, immetti le altre informazioni richieste e quindi seleziona **Salva**.

## <a name="create-data-for-entity-based-dimensions"></a>Creare dati per le dimensioni basate su entità

Puoi creare dati per le dimensioni basate su entità manualmente oppure utilizzando le chiamate di importazione o di servizio di Microsoft Excel. Utilizza i passaggi in questa procedura per creare due titoli standard, **Sistemista** e **Sistemista esperto** , a partire dalla dimensione basata su entità **Titolo standard**. Se intendi creare pochi dati, come illustrato nel seguente esempio, puoi utilizzare un modulo standard.

1. Seleziona **Ricerca avanzata** , seleziona l'entità **Titolo standard** e quindi seleziona **Risultati**. Tutte le righe nell'entità **Titolo standard** verranno visualizzate.
2. Seleziona **Nuovo** e nel campo **Nome** immetti "Systems Engineer" e seleziona **Salva**.
3. Chiudi il modulo. 
4. Ripeti i passaggi da 1 a 3 per creare un altro titolo standard, ovvero "Sistemista esperto".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Aggiungere tutte le entità necessarie e i componenti correlati alla soluzione per le dimensioni di determinazione dei prezzi
Devi aggiungere le seguenti entità alla soluzione per la determinazione dei prezzi. Utilizza i passaggi in questa procedura per apportare alcune importanti modifiche allo schema nella soluzione per la determinazione dei prezzi di modo che le entità siano consapevoli delle nuove dimensioni di determinazione dei prezzi.

1. Seleziona **Impostazioni** > **Soluzioni** e fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Aggiungi record esistente** > **Entità**.
3. Nella finestra di dialogo **Componenti della soluzione** , seleziona le seguenti entità:

  - Valore effettivo
  - Risorsa prenotabile
  - Riga di stima
  - Dettagli di riga fattura
  - Riga giornale di registrazione
  - Dettagli di voce di contratto di progetto
  - Membro del team di progetto
  - Dettagli riga di offerta
  - Ricarico prezzo ruolo
  - Prezzo ruolo 
  - Inserimento ore 


> [!NOTE]
> Assicurati di includere tutti i moduli e tutte le viste per ogni entità selezionata.

4. Quando viene richiesto di includere le entità dipendenti per le entità selezionate sopra, seleziona **No**.

