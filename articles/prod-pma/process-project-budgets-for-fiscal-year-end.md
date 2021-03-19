---
title: Trasferire i budget di progetto alla fine dell'anno fiscale
description: Questo articolo fornisce informazioni su come trasferire gli importi di budget residuo agli anni futuri e creare i dettagli del registro di budget.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289734"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Trasferire i budget di progetto alla fine dell'anno fiscale

[!include [banner](../includes/banner.md)]

Quando lavori a un progetto pluriennale, potresti avere un budget residuo alla fine dell'anno fiscale. Puoi trasferire gli importi di budget residuo a un anno futuro e creare i dettagli del registro di budget per gli importi nei conti di contabilità generale associati. Prima di riportare gli importi rimanenti, rivedi e analizza gli importi di budget residuo.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Rivedere e analizzare gli importi rimanenti di budget

Completa i seguenti passaggi per rivedere gli importi di budget di fine anno per i progetti, senza riportare gli importi.

1. Vai a **Gestione progetti e contabilità** > **Periodico** > **Budget** > **Riporto in avanti di budget**. 
2. Nella pagina **Processo di riporto in avanti di budget di progetto** nella scheda **Opzioni fine anno** verifica che **Riporto in avanti degli importi rimanenti di budget del progetto** non sia abilitato.
3. Nella scheda **Parametri** nel campo **Anno budget di progetto** seleziona l'anno fiscale per cui desideri visualizzare l'importo di budget residuo. 
4. Nel campo **Apertura anno fiscale** seleziona l'anno fiscale per cui desideri visualizzare l'importo di budget residuo. 
5. Nel campo **Da modello di previsione** seleziona **Budget residuo**. 
6. Per includere progetti che soddisfano i criteri selezionati e non hanno budget residuo, seleziona **Mostra rimanenti a zero**.  
7. Nella scheda **Seleziona budget** seleziona **Recupera tutti i budget** per caricare tutti i budget che corrispondono ai criteri selezionati, quindi seleziona **Elabora**. 
8. Per progettare una query di database che carichi un insieme specifico di budget nel riquadro, seleziona **Recupera i budget selezionati**.

Per ulteriori informazioni su una riga specifica nel riquadro, seleziona la riga e quindi seleziona **Visualizza i dettagli di budget** o **Visualizza account**.

## <a name="carry-forward-remaining-budget-amounts"></a>Riporto in avanti degli importi di budget residuo 

Quando elabori gli importi di budget residuo, puoi creare transazioni nella contabilità generale per gli importi che stai riportando in avanti. Per creare transazioni di contabilità generale, completa i passaggi nella sezione [Riporto in avanti degli importi di budget e creazione di transazioni di contabilità generale](#carry-forward). 

> [!NOTE]
> Gli importi di budget riportati vengono trasferiti al modello previsionale selezionato nella pagina **Modelli previsionali** come modello previsionale del riporto in avanti.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Riporto in avanti degli importi di budget e creazione di transazioni di contabilità generale

1.  Seleziona **Gestione progetti e contabilità** > **Periodico** > **Budget** > **Riporto in avanti di budget**. 
2. Nella pagina **Processo di riporto in avanti di budget di progetto** seleziona **Fine anno** e quindi abilita **Riporto in avanti degli importi rimanenti di budget del progetto** e **Crea voci del registro di budget nella contabilità generale**. 
3. Nella scheda **Parametri** nel gruppo di campi **Parametri di progetto** seleziona quanto segue:

   - **Anno budget di progetto**: seleziona l'inizio dell'anno fiscale per cui desideri visualizzare gli importi di budget residuo. 
   - **Profitti e perdite**: crea transazioni di profitti e perdite nella contabilità generale. 
   -  **WIP**: crea transazioni WIP (Work in Progress) nella contabilità generale.
   -  **Retribuzioni**: crea transazioni di allocazione retribuzioni nella contabilità generale. 

5. Nel gruppo di campi **Contabilità generale**, immetti le seguenti informazioni: 

   - Nel campo **Apertura anno fiscale** seleziona l'anno fiscale a cui desideri trasferire l'importo di budget residuo per i progetti. Il valore predefinito è un anno dopo il valore del campo **Anno budget di progetto**.
   -  Nel campo **Periodo riporto in avanti** seleziona il periodo per il quale vuoi creare i dettagli del registro di budget nella contabilità generale. Questo è in genere il primo periodo dell'apertura anno fiscale.

6. Nel gruppo di campi **Copia da/a**, immetti le seguenti informazioni:

   - Nel campo **Da modello di previsione** seleziona il modello di previsione di budget del progetto associato agli importi di budget residuo che vuoi trasferire per i progetti. 
   - Nel campo **A modello di budget di contabilità generale** seleziona il modello di budget di contabilità generale associato agli importi che vuoi trasferire alla contabilità generale. 
   -  Seleziona **Trasferisci valuta di vendita** per utilizzare la valuta di vendita del progetto per le transazioni di contabilità generale che vengono create quando trasferisci gli importi di budget per i progetti. Quando l'opzione non è selezionata, le transazioni utilizzano la valuta contabile. 
   -  Seleziona **Mostra rimanenti a zero** per includere i progetti che non hanno importi di budget residuo, ma soddisfano gli altri criteri selezionati nei progetti visualizzati nel riquadro inferiore.

7. Nella scheda **Seleziona budget** seleziona **Recupera tutti i budget** per caricare tutti i budget che corrispondono ai criteri selezionati. Per progettare una query di database che carichi un insieme specifico di budget di progetto nel riquadro, seleziona **Recupera i budget selezionati**.
8. Per ogni progetto che desideri elaborare, seleziona l'opzione all'inizio della riga per il progetto.

    > [!TIP]
    > Per selezionare tutti o la maggior parte dei progetti, seleziona il segno di spunta nell'angolo in alto a sinistra. Per escludere l'elaborazione di un progetto deseleziona il segno di spunta per quel progetto.

9. Per trasferire gli importi di budget residuo per i progetti selezionati all'anno fiscale selezionato e creare i dettagli del registro di budget nella contabilità generale, seleziona **Elabora**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Riporto in avanti degli importi di budget senza creazione di transazioni di contabilità generale

1. Vai a **Gestione progetti e contabilità** > **Periodico** > **Budget** > **Riporto in avanti di budget**.
2. Nella pagina **Processo di riporto in avanti di budget di progetto** nel campo **Opzioni fine anno** seleziona **Riporto in avanti degli importi rimanenti di budget del progetto**.
3. Nel gruppo **Parametri** nel campo **Anno budget di progetto** seleziona l'anno fiscale per cui desideri visualizzare gli importi di budget residuo.
4. Nel gruppo **Copia da/a**, immetti le seguenti informazioni:

   - Nel campo **Da modello di previsione** seleziona il modello di previsione di budget del progetto associato agli importi di budget residuo che vuoi trasferire per i progetti. 
   - Seleziona **Mostra rimanenti a zero** per includere progetti che soddisfano i criteri selezionati ma non hanno importi di budget residuo.
   - Nel gruppo **Seleziona budget** seleziona **Recupera tutti i budget** per caricare tutti i budget che corrispondono ai criteri selezionati. Per progettare una query di database che carichi un insieme specifico di budget di progetto nel riquadro, seleziona **Recupera i budget selezionati**.

5. Per ogni progetto che desideri elaborare, seleziona l'opzione all'inizio della riga per il progetto. 
6. Seleziona **Elabora** per trasferire gli importi di budget residuo per i progetti selezionati all'anno fiscale selezionato.



[!INCLUDE[footer-include](../includes/footer-banner.md)]