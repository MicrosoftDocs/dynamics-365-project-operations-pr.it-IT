---
title: Creare soluzioni personalizzate per le dimensioni di determinazione dei prezzi
description: Questo articolo spiega come creare una soluzione personalizzata per la creazione di dimensioni di determinazione dei prezzi personalizzate.
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
ms.openlocfilehash: 0df6728634b169c8a1a128aba1555d79fee5719f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929035"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Creare soluzioni personalizzate per le dimensioni di determinazione dei prezzi

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Tutte le modifiche alle dimensioni di determinazione dei prezzi personalizzate devono essere contenute in una soluzione separata. Questo procedura consigliata importante fornisce flessibilità per aggiornamenti o rimozioni future delle modifiche, agevola il riutilizzo del lavoro e semplifica il trasferimento di tali modifiche a un'altra istanza. Dopo aver apportato tutte le modifiche necessarie, esporta la soluzione come **Soluzione gestita** e importala in altre istanze per riutilizzare la configurazione per la determinazione dei prezzi.

1. Seleziona **Impostazioni** > **Soluzioni** e quindi seleziona **Nuovo**. 
2. Assegna un nome alla soluzione, **dimensioni di determinazione dei prezzi di \<your organization name>**, immetti le informazioni richieste e quindi seleziona **Salva**.

> ![Creare una soluzione personalizzata per le dimensioni di determinazione dei prezzi.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Aggiungere tutte le entità necessarie e i componenti correlati alla soluzione per le dimensioni di determinazione dei prezzi
Devi aggiungere le seguenti entità di Project Service alla soluzione per la determinazione dei prezzi. Completa i passaggi in questa procedura per apportare alcune importanti modifiche allo schema nella soluzione per la determinazione dei prezzi di modo che le entità siano consapevoli delle nuove dimensioni di determinazione dei prezzi.

1. Seleziona **Impostazioni** > **Soluzioni** e quindi fai doppio clic su **dimensioni di determinazione dei prezzi di \<your organization name>**. 
2. In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Aggiungi record esistente** > **Entità**.
3. Nella finestra di dialogo **Componenti della soluzione**, seleziona le seguenti entità:

- Effettiva
- Risorsa prenotabile
- Riga di stima
- Attività di progetto
- Dettagli di riga fattura
- Riga giornale di registrazione
- Dettagli di voce di contratto di progetto
- Membro del team di progetto
- Dettagli riga di offerta
- Ricarico prezzo ruolo
- Prezzo ruolo 
- Inserimento ore 

> ![Aggiungere entità esistenti alla soluzione per le dimensioni di determinazione dei prezzi.](media/Existing-entities-to-PD-solution.png)

> ![Seleziona componenti soluzione.](media/Dimension-Components.png)

> [!NOTE]
> Assicurati di includere tutti i moduli e tutte le viste per ogni entità selezionata.

4. Quando viene richiesto di includere le entità dipendenti per le entità selezionate, seleziona **No**.

> ![Non includere i componenti correlati.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
