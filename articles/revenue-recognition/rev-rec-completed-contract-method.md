---
title: Gestire le stime dei ricavi
description: Questo argomento fornisce informazioni su come gestire le stime dei ricavi per i progetti.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279008"
---
# <a name="manage-revenue-estimates"></a>Gestire le stime dei ricavi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Puoi creare, calcolare, registrare, stornare o eliminare le stime delle entrate. Puoi farlo manualmente o utilizzando un processo periodico. Questo argomento fornisce informazioni su come gestire le stime dei ricavi per i progetti.

### <a name="manage-revenue-estimates-manually"></a>Gestisci le stime dei ricavi manualmente

Nel progetto di stima dei ricavi a prezzo fisso o nella pagina **Richiesta di preventivo** (**Contabilità e gestione dei progetti** > **Report e richieste di informazioni** > **Richieste di informazioni sulle stime e report**), selezionare **Stime**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Gestire le stime dei ricavi utilizzando un processo periodico

Andare a **Gestione del progetto e contabilità** > **Periodico** > **Stime** e seleziona il processo corrispondente.

## <a name="create-a-revenue-estimate"></a>Creare una stima delle entrate

Completare la seguente procedura per creare una stima dei ricavi. 

1. Andare a **Contabilità e gestione progetti** > **Periodico** > **Stime**.
2. Seleziona **Nuovo**. Nella pagina **Creazione stima**, seleziona i seguenti parametri:

   - **Codice periodo**: questo codice determina la frequenza con cui vengono pubblicate le stime.
   - **Data di stima**: la data in cui viene elaborata la stima.
   - **Continuo**: selezionare questa casella di controllo per creare stime solo se le stime sono state registrate nel periodo precedente o se la stima è la prima stima che è stata creata. Se l'opzione non è selezionata, le stime vengono create anche se non sono state registrate nel periodo precedente.
   - **Metodo Costo per il completamento**: definire come stimare il lavoro rimanente del progetto. Per ulteriori informazioni, vedere [Costo per completare i metodi](cost-complete-methods.md).
   - **Metodo di completamento**: selezionare un metodo di completamento dalle seguenti opzioni:
     - **Automatico**: la percentuale di completamento viene calcolata automaticamente e in base alle linee di costo incluse nel calcolo. Il modello di costo definisce le righe di costo incluse.
     - **Manuale**: la percentuale di completamento è uguale alla percentuale di completamento dell'ultima stima. Dopo aver creato il preventivo, puoi modificare l'opzione **Calcolo manuale** nella pagina **Stime**.
     - **Dal modello di costo**: una combinazione dei metodi automatico e manuale. Questa opzione viene impostata automaticamente o manualmente, a seconda del valore predefinito nel modello di costo.
   - **Modello di previsione**: selezionare un modello di previsione per la stima.
   - **Stampa elenco preventivo**: crea e mostra un elenco di preventivi. L'elenco contiene lo stato della funzione corrente. È possibile stampare eventuali avvisi sul preventivo sul report. Le seguenti condizioni fanno apparire degli avvisi nell'elenco delle stime:
     - Una percentuale di completamento superiore al 100 percento.
     - Una percentuale di completamento inferiore allo 0 percento.
     - Un importo negativo nella colonna **Da completare**.
     - Un preventivo senza importo del contratto corrispondente.
     - Un preventivo senza stima dei prezzi allegato.
   - **Mostra Infolog**: selezionare questa opzione per ricevere un messaggio che contiene informazioni sui progetti di stima che sono stati elaborati durante l'esecuzione del lavoro.


## <a name="post-wip-or-accruals"></a>Pubblica WIP o ratei

Dopo che le stime sono state valutate, vengono mantenute, diminuite o aumentate. Puoi quindi pubblicare la WIP quando lavori usando il principio di valutazione **Contratto completato** o registrare i ratei quando lavori utilizzando il principio di valutazione **Percentuale completata**.
  
Lo stato del periodo di stima viene modificato da **Creato** a **Registrato**.

## <a name="reverse-wip-or-accruals"></a>WIP storni o ratei

Utilizzare l'opzione inversa per accreditare WIP o ratei già registrati, quindi creare stime per il periodo.

> [!NOTE]
> Per stornare un periodo che si trova tra altri periodi, invertire i periodi di stima necessari e quindi ripubblicarli. Poiché tutti i periodi successivi dipendono dalle stime del periodo precedente, non saltare alcun periodo.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Elimina il progetto preventivo e finisci il progetto

Il passaggio finale del processo di stima consiste nell'eliminare il progetto di stima e terminare il progetto a prezzo fisso quando la percentuale di completamento raggiunge il 100 percento.

Quando si esegue l'eliminazione si verifica quanto segue:

- Per un progetto a prezzo fisso con un contratto completato, i valori WIP vengono cancellati dai conti collettivi e registrati nei conti profitti e perdite.
- Per un progetto a prezzo fisso con una percentuale completata, i ratei vengono rimossi dal conto profitti e perdite.

La stima cambia lo stato in **Eliminato**.

> [!NOTE]
> In casi speciali, la percentuale può estendersi oltre il 100 percento. Quando ciò accade, ridurre la percentuale di completamento utilizzando il **metodo Imposta costo per il completamento su zero** per raggiungere il 100 percento.

## <a name="reverse-elimination"></a>Eliminazione inversa

1. Vai a **Contabilità e gestione progetti** > **Periodico** > **Stime** > **Eliminazione inversa**. 
2. Nel riquadro azioni, nella scheda **Processo**, nel gruppo **Mantieni**, selezionare **Stima**. 
3. Selezionare **Eliminazione inversa**.

Utilizzare questa pagina per annullare tutte le eliminazioni con una data di stima specificata e con uno stato di stima **Eliminato**. Lo stato della transazione cambia dopo aver selezionato i campi appropriati.

Questo cambia automaticamente anche lo stato del progetto in **In corso** se la fase del progetto è finita. Lo stato della stima del periodo del progetto torna a **Inserito**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]