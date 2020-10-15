---
title: Pianificazioni della fatturazione su righe di offerta basate su progetto
description: Questo argomento fornisce informazioni sulla creazione di pianificazioni e passaggi fondamentali di fatturazione per le righe di offerta.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ecaf4d872873473b0e7fe3b08d62c6fe5af9c3d
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908281"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Pianificazioni della fatturazione su righe di offerta basate su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Una riga di offerta basata su progetto offre la possibilità di esprimere una pianificazione della fatturazione. Si tratta di un'opzione facoltativa durante la fase di offerta perché l'applicazione non supporta la fatturazione di un progetto quando è collegato a una riga dell'offerta. La fatturazione è consentita solo dopo che l'offerta è stata acquisita. L'unico impatto downstream della creazione di una pianificazione della fatturazione durante la fase di offerta è che questa pianificazione della fatturazione viene copiata nella riga di contratto basata sul progetto. Se non crei una pianificazione della fatturazione durante la fase di offerta, sarà possibile farlo nella riga di contratto basata sul progetto.

Nel complesso, lo scopo delle pianificazioni della fatturazione è consentire la creazione automatica di bozze di fatture per una riga di contratto basata su progetto. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Creare una pianificazione della fatturazione per tempi e materiali per una riga di offerta basata su progetto

Quando il metodo di fatturazione per una riga di offerta basata su progetto è Tempo e materiale, il sistema genera una pianificazione della fatturazione basata sulla data. Per generare automaticamente una pianificazione della fatturazione basata sulla data, completa i seguenti passaggi.

1. Vai a **Impostazioni** > **Frequenze di fatturazione** e configura una frequenza di fatturazione.
2. Nella pagina **Offerta** apri l'offerta di progetto e nella scheda **Riepilogo**, imposta una data di consegna richiesta.
3. Apri la riga dell'offerta di tempo e materiale per la quale è necessario creare una pianificazione della fatturazione basata sulla data. 
4. Nella scheda **Pianificazione fatturazione**, seleziona i valori nei campi **Inizio fatturazione** e **Frequenza di fatturazione**. 
5. Nella griglia secondaria, seleziona **Genera pianificazione fatturazione**.
6. L'applicazione genera la pianificazione della fatturazione con i campi **Data esecuzione fattura**, **Data limite transazione** e **Stato di esecuzione** impostati nel modo seguente:

    - **Data esecuzione fattura** è impostato sulla data dettata in base alla frequenza della fatturazione.
    - **Data limite transazione** è impostato il giorno prima della **Data esecuzione fattura**.
    - **Stato di esecuzione** viene impostato automaticamente su **Non eseguito**. Quando il processo di creazione automatica della fattura viene eseguito per una determinata data di esecuzione della fattura, aggiornerà questo campo in **Esecuzione completata** o **Esecuzione non riuscita**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Creare una pianificazione della fatturazione a prezzo fisso per una riga di offerta basata su progetto

Quando la riga dell'offerta basata sul progetto ha un metodo di fatturazione **Fisso**, il sistema crea una pianificazione della fatturazione basata su passaggi fondamentali. Completa i passaggi seguenti per generare automaticamente questa pianificazione per un insieme fisso di passaggi fondamentali che vengono equamente distribuiti per il periodo di calendario.

1. Vai a **Impostazioni** > **Frequenze di fatturazione** e configura una frequenza di fatturazione.
2. Nella pagina **Offerta** apri l'offerta di progetto e nella scheda **Riepilogo**, imposta una data di consegna richiesta.
3. Aprire la riga dell'offerta a prezzo fisso per cui è necessario creare una pianificazione dei passaggi fondamentali. 
4. Nella scheda **Pianificazione fatturazione**, seleziona i valori nei campi **Inizio fatturazione** e **Frequenza di fatturazione**. 
5. Nella griglia secondaria, seleziona **Genera passaggi fondamentali periodici**.
6. L'applicazione genera la pianificazione della fatturazione con un nome, una data e un importo per il passaggio fondamentale.

    - Il nome del passaggio fondamentale è impostato sulla data dettata in base alla frequenza della fatturazione.
    - La data del passaggio fondamentale è impostato sulla data dettata in base alla frequenza della fatturazione.
    - L'importo del passaggio fondamentale viene calcolato dividendo l'importo dell'offerta sulla riga di offerta basata sul progetto per il numero di passaggi fondamentali come stabilito dalla frequenza e dalle date di inizio della fatturazione e di consegna richieste.
    - Se la riga dell'offerta include anche un importo IVA stimato, questo valore viene suddiviso equamente tra ogni passaggio fondamentale quando si generano passaggi fondamentali periodici.

### <a name="manually-create-milestones"></a>Creare manualmente passaggi fondamentali

I passaggi fondamentali a prezzo fisso possono anche essere generati manualmente quando non vengono suddivisi periodicamente. Per creare manualmente un passaggio fondamentale:

Apri la riga dell'offerta a prezzo fisso per cui è necessario creare un passaggio fondamentale. Nella scheda **Pianificazione della fatturazione**, nella griglia secondaria, seleziona **+ Crea un nuovo passaggio fondamentale della riga di offerta** e immetti le informazioni richieste in base alla tabella seguente.

| **Campo** | **Luogo** | **Pertinenza, scopo e indicazioni** | **Impatto downstream** |
| --- | --- | --- | --- |
| Nome passaggio fondamentale | Creazione rapida | Il nome del passaggio fondamentale. | Viene propagato sul passaggio fondamentale della riga di contratto del progetto e sulla fattura |
| Attività di progetto | Creazione rapida | Se il passaggio fondamentale è legato all'attività di progetto, è possibile utilizzare questo riferimento per aggiungere logica personalizzata e impostare lo stato del passaggio fondamentale in base allo stato dell'attività. | L'applicazione non ha alcun impatto downstream di questo riferimento a un'attività. |
| Data passaggio fondamentale | Creazione rapida | Imposta la data in cui il processo di creazione automatica della fattura deve cercare lo stato di questo passaggio fondamentale per considerarlo per la fatturazione. | Viene propagato sul passaggio fondamentale della riga di contratto del progetto e sulla fattura. |
| Stato fattura | Creazione rapida | Quando viene creato un passaggio fondamentale, questo stato è sempre impostato su **Non pronto per la fatturazione**. | Viene propagato sul passaggio fondamentale della riga di contratto del progetto e sulla fattura. |
| Importo riga | Creazione rapida | Importo o valore del passaggio fondamentale che verrà fatturato al cliente. | Viene propagato sul passaggio fondamentale della riga di contratto del progetto e sulla fattura. |
| Imposta | Creazione rapida | Importo dell'imposta che verrà applicato al passaggio fondamentale. | Viene propagato sul passaggio fondamentale della riga di contratto del progetto e sulla fattura. |