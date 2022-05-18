---
title: Correzioni in blocco di valori effettivi creati tramite voci di spesa e inserimenti ore approvati
description: In questo argomento viene indicato in che modo un amministratore può apportare correzioni singole o in blocco a voci di spesa e inserimenti ore precedentemente approvati, se la fatturazione non è completa.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 107ba01f2fd5717e1717824631aeee099d8a8205
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683367"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Correzioni in blocco di valori effettivi creati tramite voci di spesa e inserimenti ore approvati

[!include [banner](../includes/psa-now-project-operations.md)]

In alcuni casi, è possibile che l'immissione di voci di spesa e inserimenti ore avvenga in modo errato. È ad esempio possibile che un consulente selezioni la data errata durante la creazione di un inserimento ora o che trasponga i numeri quando inserisce una spesa. Sebbene un consulente non possa effettuare aggiornamenti alle voci inviate, un amministratore può correggere direttamente la voce per un progetto.

Per completare le procedure in questo argomento, devi disporre delle autorizzazioni amministratore.

## <a name="correct-approved-time-entries"></a>Correggere gli inserimenti ore approvati     

Completa i seguenti passaggi per correggere uno o più inserimenti ore per un progetto.

1. Nell'area **Vendite** seleziona **Transazioni**, quindi **Ora approvata**. 

2. In **Ora approvata** elenca, individua e seleziona uno o più inserimenti ore approvate da correggere. Puoi utilizzare il filtro per individuare voci correlate. Ad esempio, puoi filtrare in base a un ID progetto e selezionare tutti gli inserimenti ore approvati con tale ID progetto.

3. Seleziona **Voci corrette**. Viene automaticamente creato un nuovo giornale di registrazione correzione, con il tipo **Correzione dell'ora** assegnato. Le voci selezionate vengono aggiunte al giornale di registrazione. 

4. Nella pagina **Nuovo giornale di registrazione** immetti in **Descrizione** del testo per il giornale di registrazione correzione, quindi seleziona la scheda **Correzioni di inserimenti ore**.  
5. Nella sezione **Nuovi valori per gli inserimenti ore** aggiorna i campi con le informazioni corrette, come necessario. Puoi ad esempio modificare il progetto assegnato o la risorsa prenotabile.

6. Seleziona **Anteprima**. Nella finestra di dialogo seleziona **OK**. Nella scheda **Righe giornale di registrazione** è visualizzato un elenco dei valori effettivi originali correlati agli inserimenti ore selezionati che sono stati ripristinati, con le righe corrispondenti corrette che sono state create. Se è necessario apportare ulteriori correzioni, ripeti i passaggi 5 e 6. 

> [!NOTE]
> Tutti i valori effettivi corretti avranno gli stessi valori che hai selezionato nella sezione **Nuovi valori per gli inserimenti ore**.

7. Se le correzioni vengono visualizzate come previsto, seleziona **Conferma**. Nella finestra di dialogo seleziona **OK**.

8. Torna all'area **Vendite**, seleziona **Progetti** e quindi apri il progetto per il quale hai appena aggiornato gli inserimenti ore. 

9. Nella pagina **Progetti** visualizza le modifiche che hai apportato nella scheda **Valori effettivi**. 

> [!NOTE]
> Se la scheda **Valori effettivi** non è visibile, seleziona **Elementi correlati** > **Valori effettivi**.  

10. Nell'elenco **Visualizzazione associata valore effettivo** potrai vedere che gli inserimenti ore originali che sono stati ripristinati risultano ancora elencati, così come gli inserimenti ore corrette. 


## <a name="correct-approved-expense-entries"></a>Correggere le voci di spesa approvate

Completa i seguenti passaggi per correggere una o più voci di spesa. 

1. Nel riquadro di navigazione a sinistra dell'area **Vendite** in **Transazioni** seleziona **Spese approvate**.

2. Nell'elenco **Spese approvate** seleziona il progetto che desideri correggere, quindi seleziona **Voci corrette**. Verrà automaticamente creato un nuovo giornale di registrazione correzione, con il tipo **Correzione di spesa** assegnato. 

3. Nella pagina **Nuovo giornale di registrazione** inserisci in **Descrizione** del testo per la correzione e nella scheda **Correzione di spese** seleziona in **Nuovi valori per le spese** i campi dati che desideri correggere per le righe di spesa selezionate. Puoi ad esempio assegnare la spesa a un altro **Progetto** o correggere i valori di **Categoria di spesa**, **Data spesa** o **Risorsa prenotabile**.

4. Seleziona **Anteprima**. Nella finestra di dialogo seleziona **OK**. 

5. Verifica le correzioni nella scheda **Righe giornale di registrazione**. Potrai visualizzare un elenco dei valori effettivi originali correlati alle voci di spesa selezionate che sono state ripristinate, con le righe corrispondenti corrette che sono state create.

6. Se i valori risultano corretti come previsto, seleziona **Conferma**. Nella finestra di dialogo seleziona **OK**. Se non vengono visualizzati i valori previsti, seleziona **Annulla** per tornare all'elenco **Spese approvate**. Ripeti i passaggi da 2 a 5. 

> [!NOTE]
> I valori effettivi corretti avranno gli stessi valori che hai selezionato nella sezione **Nuovi valori per le spese**.

7. Dopo aver confermato il giornale di registrazione correzione, torna al progetto o ai progetti che hai aggiornato per visualizzare le modifiche.  

8. Nella pagina del progetto, nella scheda **Valori effettivi** controlla **Visualizzazione associata valore effettivo**. Viene visualizzato un elenco delle voci originali e di quelle corrette. Il grafico seguente mostra gli importi delle voci di spesa originali e gli importi delle voci di spesa corretti corrispondenti. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
