---
title: Creare una pianificazioni di fatturazione in una voce di contratto basata su progetto
description: Questo argomento fornisce informazioni su come creare pianificazioni e passaggi fondamentali di fatturazione per le voci di contratto.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 23378b51c8324a60918ad494e7f659dbbc94e2a8
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4079108"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Creare una pianificazioni di fatturazione in una voce di contratto basata su progetto 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Puoi creare una pianificazioni di fatturazione in una voce di contratto basata su progetto. La fatturazione è consentita solo dopo che il contratto è stato acquisito e stai creando un contratto di progetto. Una pianificazione fatturazione consente la creazione automatica di bozze di fattura per una voce di contratto basata su progetto. Se, tuttavia, crei solo fatture manualmente, puoi saltare la creazione delle pianificazioni fatturazione nelle voci di contratto.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Creare una pianificazione della fatturazione per tempi e materiali per una voce di contratto

Quando una voce di contratto basata su progetto ha un metodo di fatturazione per tempo e materiali puoi creare una pianificazione fatturazione basata sulla data. Per generare automaticamente una pianificazione della fatturazione basata sulla data, completa i seguenti passaggi.

1. Vai a **Impostazioni** > **Frequenze di fatturazione** e configura una frequenza di fatturazione.
2. Vai al record del contratto di progetto e nella scheda **Riepilogo** , nel campo **Data di consegna richiesta** seleziona una data.
3. Apri la voce di contratto **Tempistica e materiali** per cui stai creando una pianificazione della fatturazione basata sulla data. 
4. Nella scheda **Pianificazione fatturazione** , seleziona la data di inizio fatturazione e la frequenza di fatturazione.
5. Nella griglia secondaria, seleziona **Genera pianificazione fatturazione**. La pianificazione della fatturazione viene generata con i campi **Data esecuzione fattura** , **Data limite transazione** e **Stato di esecuzione** impostati nel modo seguente:

    - **Data esecuzione fattura** : è la data dettata dalla frequenza della fatturazione.
    - **Data limite transazione** : il giorno prima della data di esecuzione fattura.
    - **Stato di esecuzione** : viene impostato automaticamente su **Non eseguito**. Quando il processo di creazione automatica della fattura viene eseguito per una determinata data di esecuzione della fattura, aggiorna questo campo in **Esecuzione completata** o **Esecuzione non riuscita**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Creare una pianificazione della fatturazione a prezzo fisso per una voce di contratto

Quando la voce di contratto ha un metodo di fatturazione fisso, puoi creare una pianificazione della fatturazione basata su passaggi fondamentali. 

> [!NOTE]
> I passaggi fondamentali non possono essere creati su una voce di contratto se non è presente alcun progetto mappato alla voce di contratto.

Completa i passaggi seguenti per generare una pianificazione della fatturazione basata su passaggi fondamentali per un insieme fisso di passaggi fondamentali distribuiti per il periodo di calendario.

1. Vai a **Impostazioni** > **Frequenze di fatturazione** e configura una frequenza di fatturazione.
2. Vai al record del contratto di progetto e nella scheda **Riepilogo** , nel campo **Data di consegna richiesta** seleziona una data.
3. Apri la voce di contratto **Prezzo fisso** per cui stai creando una pianificazione dei passaggi fondamentali. Nella scheda **Passaggi fondamentali di fatturazione** , seleziona la data di inizio fatturazione e la frequenza di fatturazione. 
4. Nella griglia secondaria, seleziona **Genera passaggi fondamentali periodici**. La pianificazione fatturazione viene generata con i campi **Nome passaggio fondamentale** , **Data passaggio fondamentale** e **Importo passaggio fondamentale** impostati come segue:

    - **Nome passaggio fondamentale** : è la data dettata dalla frequenza della fatturazione.
    - **Data fondamentale** : è la data dettata dalla frequenza della fatturazione.
    - **Importo passaggio fondamentale** : è l'importo calcolato dividendo l'importo del contratto nella voce di contratto per il numero di passaggi fondamentali come stabilito dalla frequenza e dalle date di inizio della fatturazione e di consegna richieste.

    Se la voce di contratto ha un valore nel campo **Importo previsto delle imposte** , questo campo viene anche ripartito equamente su ogni passaggio fondamentale quando si generano passaggi fondamentali periodici.

I passaggi fondamentali di fatturazione devono essere uguali al valore di contratto della voce di contratto. In caso contrario, riceverai un errore nella pagina **Voce di contratto**. Puoi correggere l'errore verificando che i passaggi fondamentali di fatturazione totalizzino il valore di contratto della voce creando, modificando o eliminando i passaggi fondamentali. Dopo aver apportato le modifiche, aggiorna la pagina per rimuovere l'errore.

### <a name="manually-create-milestones"></a>Creare manualmente passaggi fondamentali

Puoi generare passaggi fondamentali a prezzo fisso manualmente quando non vengono suddivisi periodicamente. Completa i passaggi seguenti per creare manualmente un passaggio fondamentale.

1. Apri la voce di contratto a prezzo fisso per cui stai creando un passaggio fondamentale e nella scheda **Pianificazione fatturazione** , nella griglia secondaria, seleziona **+ Crea nuovo passaggio fondamentale della voce di contratto**. 
2. Nella pagina **Creazione passaggio fondamentale** immetti le informazioni richieste in base alla tabella seguente.

| Campo | Ufficio | Pertinenza, scopo e indicazioni | Impatto downstream |
| --- | --- | --- | --- |
| Nome passaggio fondamentale | Creazione rapida | Campo di testo per il nome del passaggio fondamentale. | Viene riportato sul passaggio fondamentale della voce di contratto del progetto e sulla fattura. |
| Attività di progetto | Creazione rapida | Se il passaggio fondamentale è legato all'attività di progetto, puoi utilizzare questo riferimento per aggiungere logica personalizzata e impostare lo stato del passaggio fondamentale in base allo stato dell'attività. | L'applicazione non ha alcun impatto downstream di questo riferimento a un'attività. |
| Data passaggio fondamentale | Creazione rapida | Imposta la data in cui il processo di creazione automatica della fattura deve cercare lo stato di questo passaggio fondamentale per considerarlo per la fatturazione. | Viene riportato sul passaggio fondamentale della voce di contratto del progetto e sulla fattura. |
| Stato fattura | Creazione rapida | Quando viene creato un passaggio fondamentale, questo stato è sempre impostato su **Non pronto per la fatturazione** o **Non avviato**. | Viene riportato sul passaggio fondamentale della voce di contratto del progetto e sulla fattura. |
| Importo riga | Creazione rapida | Importo o valore del passaggio fondamentale che verrà fatturato al cliente. | Viene riportato sul passaggio fondamentale della voce di contratto del progetto e sulla fattura. |
| Imposta | Creazione rapida | L'importo delle imposte applicato al passaggio fondamentale. | Viene riportato sul passaggio fondamentale della voce di contratto del progetto e sulla fattura. |

3. Seleziona **Salva e chiudi**.
