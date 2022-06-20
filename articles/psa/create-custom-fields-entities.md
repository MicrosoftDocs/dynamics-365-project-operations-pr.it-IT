---
title: Creare campi ed entità personalizzati
description: In questo articolo viene illustrato come creare set di opzioni ed entità nella soluzione utilizzata sulla piattaforma Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3b6f675d604f3b6a6f2465c413ceff3d16815e12
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926919"
---
# <a name="create-custom-fields-and-entities"></a>Creare campi ed entità personalizzati 

[!include [banner](../includes/psa-now-project-operations.md)]

Completa i passaggi seguenti ogni volta che intendi creare un set di opzioni o un'entità personalizzato nella piattaforma Power Apps.  
Le procedure illustrate in questo articolo devono essere completate tramite l'interfaccia Web di Project Service Automation (PSA).

> [!IMPORTANT]
> Ti consigliamo di apportare le modifiche alle dimensioni di determinazione dei prezzi personalizzate in una soluzione distinta. Questo procedura consigliata importante fornisce flessibilità per aggiornamenti o rimozioni future delle modifiche, agevola il riutilizzo del lavoro e semplifica il trasferimento di tali modifiche a un'altra istanza. Dopo aver apportato tutte le modifiche necessarie, esporta questa soluzione come **Soluzione gestita** e importala in altre istanze per riutilizzare la configurazione per la determinazione dei prezzi.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Creare campi e set di opzioni personalizzati nella soluzione per le dimensioni di determinazione dei prezzi

Una dimensione di determinazione dei prezzi può essere un set di opzioni o un'entità. Entrambi devono essere creati nella soluzione per la determinazione dei prezzi. I passaggi in questa procedura illustrano il modo in cui creare dimensioni basate su entità e dimensioni basate su set di opzioni.

### <a name="entity-based-dimensions"></a>Dimensioni basata su entità

1. In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**.
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Entità**.
3. Fai clic su **Nuovo** per creare una nuova entità denominata **Titolo standard**. Immetti le altre informazioni e quindi fai clic su **Salva**.

> ![Definizione dell'entità Titolo standard.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensioni basate su set di opzioni 
Puoi creare due dimensioni basate su set di opzioni. Utilizza **Ubicazione lavoro risorsa** per tenere traccia del prezzo del lavoro nell'ubicazione **Abitazione** e del lavoro **In loco** e utilizza **Ore lavorative risorsa** con i valori **Normale** e **Straordinario** per applicare un ricarico quando il lavoro è ultimato.


1. In PSA fai clic su **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Set di opzioni**. 
3. Fai clic su **Nuovo** per creare un nuovo set di opzioni, immetti le altre informazioni richieste e quindi fai clic su **Salva**.

> ![Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ubicazione lavoro risorsa.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Set di opzioni basato sulla dimensione di determinazione dei prezzi denominata Ore lavorative risorsa.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Creare dati per le dimensioni basate su entità

Puoi creare dati per le dimensioni basate su entità manualmente oppure utilizzando le chiamate di importazione o di servizio di Microsoft Excel. Utilizza i passaggi in questa procedura per creare due titoli standard, **Sistemista** e **Sistemista esperto**, a partire dalla dimensione basata su entità **Titolo standard**. Se intendi creare pochi dati, come illustrato nel seguente esempio, puoi utilizzare un modulo standard.

1. In PSA fai clic su **Ricerca avanzata**. Selezionar l'entità **Titolo standard**, quindi fai clic su **Risultati**. Tutte le righe nell'entità **Titolo standard** verranno visualizzate.
2. Fai clic su **Nuovo**. Nel campo **Nome** immetti "Sistemista" e quindi fai clic su **Salva**.
3. Chiudere il modulo. 
4. Ripeti i passaggi da 1 a 3 per creare un altro titolo standard, ovvero "Sistemista esperto".

> ![Dati di esempio per l'entità Titolo standard.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
