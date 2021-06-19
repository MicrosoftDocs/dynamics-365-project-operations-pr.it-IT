---
title: Creare una soluzione per le dimensioni di determinazione dei prezzi personalizzate
description: In questo argomento vengono fornite informazioni sulla creazione di soluzioni per dimensioni di determinazione dei prezzi.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010341"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Creare una soluzione per le dimensioni di determinazione dei prezzi personalizzate

 _**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_ 

>[!IMPORTANT]
>Tutte le modifiche alle dimensioni di determinazione dei prezzi personalizzate devono essere contenute in una soluzione separata. Questa procedura consigliata importante fornisce flessibilità per aggiornare o rimuovere modifiche come necessario, agevola il riutilizzo del lavoro e semplifica il trasferimento di tali modifiche ad altre istanze. Dopo aver apportato tutte le modifiche necessarie, esporta questa soluzione come soluzione **Gestita** e importala in altre istanze per riutilizzarla.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Creare una soluzione per le dimensioni di determinazione dei prezzi personalizzate

1.  Seleziona **Impostazioni** > **Soluzioni** e quindi seleziona **Nuovo**.
2.  Assegna un nome alla soluzione, *dimensioni dei prezzi di <your organization name>*.
3. Immetti le altre informazioni e quindi seleziona **Salva**.

  ![Creazione di una soluzione di determinazione dei prezzi personalizzata](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Aggiungere tutte le entità necessarie e i componenti correlati alla soluzione per le dimensioni di determinazione dei prezzi

Aggiungi le seguenti entità di Project Service alla tua soluzione tariffaria per apportare importanti modifiche allo schema nella soluzione tariffaria. Dopo aver completato questa procedura, le entità riconosceranno le nuove dimensioni di prezzo.

1.  Seleziona **Impostazioni** > **Soluzioni**, quindi fai doppio clic su **<*nome dell'organizzazione*> dimensioni di determinazione dei prezzi**.
2.  In Esplora soluzioni, nel riquadro di spostamento a sinistra, seleziona **Aggiungi record esistente** > **Entità**.
3.  Nella finestra di dialogo **Componenti della soluzione**, seleziona le seguenti entità:
 
   - **Effettiva**
   - **Risorsa prenotabile**
   - **Riga di stima**
   - **Attività di progetto**
   - **Dettagli di riga fattura**
   - **Riga giornale di registrazione**
   - **Dettagli di voce di contratto di progetto**
   - **Membro del team di progetto**
   - **Dettagli riga di offerta**
   - **Ricarico prezzo ruolo**
   - **Prezzo ruolo**
   - **Inserimento ore**
 
   ![Aggiungi entità esistenti alla soluzione per le dimensioni di determinazione dei prezzi](./media/Existing-entities-to-PD-solution.png)
 
 4. Per ciascuna entità, rivedere i componenti aggiunti e l'elenco finale delle risorse dell'entità per ciascuna entità. 

   >[!NOTE]
   > Include tutti i moduli e tutte le viste per ogni entità selezionata.

  ![Entità aggiunta](./media/solution-component-selection.png)


5.  Quando viene richiesto di includere eventuali entità dipendenti per le entità selezionate, seleziona **No, non includere i componenti richiesti.**

    ![Comprese le entità dipendenti](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]