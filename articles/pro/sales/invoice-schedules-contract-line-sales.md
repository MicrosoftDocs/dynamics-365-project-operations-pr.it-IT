---
title: Creare pianificazioni di fatturazione in una voce di contratto basata su progetto - semplice
description: Questo argomento fornisce informazioni sulla creazione di pianificazioni di fatturazione e passaggi fondamentali.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 548858f6d2257343a632657ca386da03f1f330a9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003236"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Creare pianificazioni di fatturazione in una voce di contratto basata su progetto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Puoi collegare una pianificazione fatturazione in una voce di contratto basata su progetto. La fatturazione è consentita solo dopo che il contratto è stato acquisito per creare un contratto di progetto. Le pianificazioni di fatturazione consentono di creare automaticamente bozze di fattura per una voce di contratto basata su progetto. Se pensi di creare sempre le fatture manualmente, puoi saltare la creazione di pianificazioni di fatturazione in una voce di contratto basata su progetto o una voce di contratto.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Creare una pianificazione fatturazione di tempo e materiale per una voce di contratto basata su progetto

Quando una voce di contratto basata su progetto ha un metodo di fatturazione per tempo e materiali puoi creare una pianificazione fatturazione basata sulla data. Per generare automaticamente una pianificazione della fatturazione basata sulla data, completa i seguenti passaggi.

1. Vai a **Impostazioni** > **Frequenze di fatturazione** per impostare la frequenza di fatturazione.
2. Apri il contratto di progetto e nella scheda **Sommario** imposta la data di consegna richiesta.
3. Apri la voce di contratto tempo e materiale per la quale vuoi creare una pianificazione di fatturazione basata sulla data. 
4. Nella scheda **Pianificazione fatturazione** seleziona una data di inizio fatturazione e la frequenza di fatturazione. 
5. Nella griglia secondaria, seleziona **Genera pianificazione fatturazione**.

    Il sistema genera la pianificazione di fatturazione con le seguenti informazioni dei campi:

    - **Data esecuzione fattura** è impostato sulla data in base alla frequenza di fatturazione.
    - **Data limite transazione** è impostato sul giorno prima della **Data esecuzione fattura**.
    - **Stato di esecuzione** viene impostato automaticamente su **Non eseguito**. Quando il processo di creazione automatica della fattura viene eseguito per una determinata **Data esecuzione fattura**, questo campo viene impostato su **Esecuzione completata** o **Esecuzione non riuscita**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Creare una pianificazione fatturazione a prezzo fisso per una voce di contratto basata su progetto

Quando una voce di contratto basata su progetto ha un metodo di fatturazione a prezzo fisso, puoi creare una pianificazione di fatturazione basata su passaggio fondamentale. Completa i seguenti passaggi per generare automaticamente una pianificazione di fatturazione basata su passaggio fondamentale per un set fisso di passaggi fondamentali che vengono distribuiti equamente per il periodo di calendario.

1. Vai a **Impostazioni** > **Frequenze di fatturazione** per impostare la frequenza di fatturazione.
2. Apri il contratto di progetto e nella scheda **Sommario** imposta la data di consegna richiesta.
3. Apri la voce di contratto a prezzo fisso per cui vuoi creare una pianificazione di passaggi fondamentali. 
4. Nella scheda **Pianificazione fatturazione (passaggi fondamentali di fatturazione)** seleziona la data di inizio fatturazione e la frequenza di fatturazione. 
5. Nella griglia secondaria, seleziona **Genera passaggi fondamentali periodici**.

    Il sistema genera la pianificazione di fatturazione con le seguenti informazioni dei passaggi fondamentali.

    - **Nome passaggio fondamentale** è impostato sulla data indicata in base alla frequenza di fatturazione.
    - **Data passaggio fondamentale** è impostato sulla data indicata in base alla frequenza di fatturazione.
    - **Importo passaggio fondamentale** viene calcolato dividendo l'importo del contratto nella voce di contratto basata su progetto per il numero di passaggi fondamentali come indicato dalla frequenza, dall'inizio della fatturazione e dalle date di consegna richieste.
    - Se la voce di contratto ha un valore nel campo **Importo stimato delle imposte**, anche questo campo viene ripartito equamente su ogni passaggio fondamentale quando si generano passaggi fondamentali periodici.

I passaggi fondamentali di fatturazione devono essere uguali al valore di contratto della voce di contratto basata su progetto. Se non sono uguali, si verifica un errore. È possibile correggere l'errore verificando che i passaggi fondamentali di fatturazione totalizzino il valore di contratto della voce creando, modificando o eliminando i passaggi fondamentali. Dopo aver apportato le modifiche, aggiorna la pagina.

### <a name="manually-create-milestones"></a>Creare manualmente passaggi fondamentali

I passaggi fondamentali a prezzo fisso possono essere generati manualmente quando non vengono suddivisi periodicamente. Per creare manualmente un passaggio fondamentale, completa i seguenti passaggi.

1. Apri la voce di contratto a prezzo fisso per cui vuoi creare un passaggio fondamentale. 
2. Nella scheda **Pianificazione di fatturazione**, nella griglia secondaria, seleziona **+ Crea nuovo passaggio fondamentale voce di contratto**.
3. Nel modulo **Creazione passaggio fondamentale** inserisci le informazioni richieste in base alla tabella seguente. 

| Campo | Ufficio | Descrizione | Impatto downstream |
| --- | --- | --- | --- |
| Nome passaggio fondamentale | Creazione rapida | Campo di testo per il nome del passaggio fondamentale. | Questo campo è incluso nel passaggio fondamentale della voce di contratto di progetto e nella fattura. |
| Attività di progetto | Creazione rapida | Se il passaggio fondamentale è collegato a un'attività di progetto, utilizza questo riferimento per aggiungere logica personalizzata e impostare lo stato del passaggio fondamentale in base allo stato dell'attività. | Non vi è alcun impatto downstream di questo riferimento a un'attività. |
| Data passaggio fondamentale | Creazione rapida | La data in cui il processo di creazione automatica della fattura cerca lo stato di questo passaggio fondamentale per considerarlo per la fatturazione. | Questo è incluso nel passaggio fondamentale della voce di contratto di progetto e nella fattura. |
| Stato fattura | Creazione rapida | Quando viene creato il passaggio fondamentale, questo stato è sempre impostato su **Non pronto per la fatturazione** o **Non avviato**. | Questo è incluso nel passaggio fondamentale della voce di contratto di progetto e nella fattura. |
| Importo riga | Creazione rapida | L'importo o il valore del passaggio fondamentale che verrà fatturato al cliente. | Questo campo è incluso nel passaggio fondamentale della voce di contratto di progetto e nella fattura. |
| Imposta | Creazione rapida | L'importo delle imposte applicato al passaggio fondamentale. | Questo è incluso nel passaggio fondamentale della voce di contratto di progetto e nella fattura. |

4. Seleziona **Salva e chiudi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]