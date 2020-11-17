---
title: Unità di vendita e unità
description: In questo argomento vengono fornite informazioni su unità di vendita e unità.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 58ce821d11d729f6e2c33e5a50344458e395db4d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130583"
---
# <a name="unit-groups-and-units"></a>Unità di vendita e unità

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Le unità di vendita e le unità sono entità di base in Microsoft Dynamics 365. Un'unità è una singola unità di misura e molteplici unità possono essere raggruppate in unità di vendita. Un'unità di vendita è talvolta denominata pianificazione di unità nell'interfaccia utente di Dynamics 365. 

Di seguito sono riportati alcuni esempi di unità e unità di vendita:
 
- **Unità di vendita**: distanza 
    - **Unità**: miglio, chilometro e così via.
- **Unità di vendita**: tempo
    - **Unità**: ora, giorno, settimana e così via. 

Quando imposti molteplici unità in un'unità di vendita, devi anche impostare un fattore di conversione tra le stesse designando la prima unità che hai configurato come unità predefinita o primaria per l'unità di vendita. 

Ad esempio, in un'unità di vendita **Tempo**, se imposti **Ora** come prima unità, il sistema designa **Ora** come unità predefinita. Se l'unità seguente impostata è **Giorno**, devi impostare un fattore di conversione da **Giorno** a **Ora**. Se quindi aggiungi **Settimana** come terza unità, devi impostare un fattore di conversione per **Settimana** in termini di **Giorno** o **Ora**. 

L'immagine seguente mostra un esempio di impostazione per l'unità **Giorno**, dove il campo **Quantità** mostra il numero di ore in un giorno, e **Settimana**, dove il campo **Quantità** mostra il numero di giorni in una settimana.

> ![Unità di vendita: pagina Informazioni](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Utilizzare unità e unità di vendita

Dynamics 365 Project Service Automation utilizza unità e unità di vendita per elaborare stime nonché voci di spesa e inserimenti ore. 

Per le spese, ogni categoria di spesa include un'unità di vendita e un'unità predefinite. Tali valori vengono immessi come valori predefiniti nelle voci di listino prezzi per le categorie di spesa. 

Ad esempio, hai una categoria di spesa denominata **Indennità trasferta** Questa categoria ha un'unità di vendita denominata **Distanza** e un'unità predefinita denominata **Miglio**. Se imposti l'unità di vendita **Distanza** in modo da avere due unità (**Miglio** e **Chilometro**), puoi impostare due prezzi per la categoria **Indennità trasferta** in un listino prezzi: prezzo al miglio e prezzo al chilometro.

| Categoria di spesa  | Unità di vendita  | Unità      | Metodo di determinazione dei prezzi  | Prezzo unitario  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Indennità trasferta           | Distanza      | Miglio      | Prezzo unitario    | 10 USD            |
| Indennità trasferta           | Distanza      | Chilometro | Prezzo unitario    |  6 USD            |

Quando immetti una spesa per un progetto, il sistema determina il prezzo mediante la combinazione di categoria e unità della spesa. 

| Descrizione spesa        | Categoria di spesa  | Unità  | Quantità  | Prezzo unitario   |
|----------------------------|---------------------|-------|-----------|----------------|
| Tragitto fino a ubicazione cliente | Indennità trasferta             | Miglio  | 10        | 10 USD         |

Per il tempo, ogni intestazione del listino prezzi include un campo **Unità di tempo predefinita**. Il valore viene impostato quando crei l'intestazione del listino prezzi. Questa unità viene quindi utilizzata per impostare tutti i prezzi basati su ruolo nel listino prezzi.

Le righe di stima per il campo **Tempo in offerta** possono essere espresse in qualsiasi unità di tempo. Tuttavia, per le righe di stima e gli inserimenti ore puoi utilizzare solo l'unità di tempo **Ora**. Se l'unità nell'inserimento ore o nella riga di stima non corrisponde all'unità nella riga di listino prezzi per quel ruolo, il sistema converte il prezzo nelle unità definite nella stima di progetto o nella transazione di progetto effettiva.

L'esempio seguente illustra come PSA utilizza l'unità di vendita, le unità e i fattori di conversione.
- Unità

   - **Unità di vendita**: tempo 
   - **Unità**: ora 
    
    - **Giorno** - Fattore di conversione: 8 ore       
    - **Settimana** - Fattore di conversione: 40 ore  
        
- Configurazione listino prezzi nel progetto A:

    - **Nome**: prezzi di vendita Regno Unito 2016 
    - **Unità di tempo predefinita**: giorno 
    - **Valuta**: GBP

| Ruolo      | Unità di vendita | Unità | Unità organizzativa | Prezzo   |
|-----------|------------|------|---------------------|---------|
| Sviluppatore | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Inserimento ore

Nella tabella seguente è visualizzata la transazione lato vendita risultante creata da PSA per un progetto di tre ore.


| Progetto   | Attività    | Ruolo      | Quantità | Unità  | Prezzo unitario | Importo vendite non fatturate |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Progetto A | Progetta  | Sviluppatore | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Domande frequenti sulle unità di tempo

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>PSA esegue la conversione in differenti unità per le spese?
N. La conversione di unità è disponile solo per il tempo. Per le spese, se il sistema non trova un prezzo per la combinazione di unità e categoria di spesa, per impostazione predefinita il prezzo è impostato su 0,00.

### <a name="why-does-psa-convert-time-units"></a>Perché PSA converte le unità di tempo?
In alcuni paesi o aree geografiche, per legge è necessario configurare i tassi di fatturazione in giorni. La negoziazione dei prezzi e gli sconti durante il ciclo di offerta vengono eseguiti utilizzando tassi giornalieri per ogni ruolo fatturabile. La stima di pianificazione e l'inserimento ore sono in ore. Per supportare questa differenza nelle unità di tempo, PSA converte le unità di tempo.

### <a name="can-time-units-be-changed-on-project-estimates"></a>È possibile modificare le unità di tempo nelle stime di progetto?
N. La stima di pianificazione è attualmente limitata alle ore e non può essere modificata.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>È possibile modificare, eliminare e aggiungere unità e unità di vendita?
Sì. Con l'eccezione dell'unità di vendita **Tempo** e dell'unità **Ora**, tutte le unità possono essere modificate, eliminate e aggiunte. In PSA, l'unità di vendita **Tempo** e l'unità **Ora** non possono essere eliminate. Tuttavia, possono essere aggiornate con un testo tradotto per il campo **Nome**.
