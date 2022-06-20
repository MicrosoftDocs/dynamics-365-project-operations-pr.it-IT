---
title: Creare e verificare i giornali di registrazione correzioni
description: Questo articolo fornisce informazioni su come creare e confermare un giornale di registrazione di correzioni.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928069"
---
# <a name="create-and-confirm-correction-journals"></a>Creare e verificare i giornali di registrazione correzioni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Di tanto in tanto, una voce di spesa o un inserimento ore potrebbe essere inserito in modo errato. Ad esempio, un consulente potrebbe selezionare la data sbagliata quando crea un inserimento ore o potrebbe selezionare il progetto sbagliato quando inserisce una spesa. Se un consulente non può aggiornare le voci inviate, un amministratore back-end può correggere direttamente i valori effettivi per un progetto.

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

7. Dopo aver confermato il giornale di registrazioni correzioni, torna al progetto o ai progetti che hai aggiornato per visualizzare le modifiche.

8. Nella pagina del progetto, nella scheda **Valori effettivi** rivedi l'elenco **Visualizzazione associata valore effettivo**. Viene visualizzato un elenco delle voci originali e di quelle corrette.


## <a name="correct-approved-material-usage-logs"></a>Correggere i registri di utilizzo del materiale approvati

Completa i seguenti passaggi per correggere una o più voci del registro di utilizzo del materiale.

1. Nell'area **Vendite**, nel riquadro di navigazione a sinistra, sotto **Transazioni**, seleziona **Valori effettivi**.

2. Nell'elenco **Valori effettivi** utilizza i filtri di colonna per selezionare la classe di transazione **Materiale**, in modo che vengano mostrati solo i valori effettivi per i materiali. Utilizza altri filtri di colonna per limitare ulteriormente i valori effettivi visualizzati. Dopo aver trovato il set desiderato di valori effettivi, seleziona i valori effettivi, quindi seleziona **Voci corrette**. Viene creato automaticamente un nuovo giornale di registrazioni correzioni e il tipo **Correzione materiale** è assegnato.

3. Sulla pagina **Nuovo giornale di registrazione**, nel campo **Descrizione** immetti una descrizione per la correzione. Poi, sulla scheda **Correzione materiale** nella sezione **Nuovi valori per materiali** seleziona i campi dati da correggere per le righe materiale selezionate. Ad esempio, puoi assegnare il materiale a un altro progetto o correggere il prodotto, la data del materiale o il conto lavoro.

4. Selezionare **Anteprima**. Quindi, nella finestra di dialogo seleziona **OK**.

5. Sulla scheda **Righe giornale di registrazione** verifica le correzioni. È possibile visualizzare un elenco dei valori effettivi originali correlati alle voci materiale selezionate che sono state stornate e alle righe corrispondenti corrette che sono state create.

6. Se i valori risultano corretti come previsto, seleziona **Conferma**. Quindi, nella finestra di dialogo seleziona **OK**. Se i valori non sono quelli previsti, seleziona **Annulla** per tornare all'elenco **Valori effettivi**. Ripeti quindi i passaggi da 2 a 5.

7. Dopo aver confermato il giornale di registrazioni correzioni, torna al progetto o ai progetti che hai aggiornato per visualizzare le modifiche.

8. Nella pagina del progetto, nella scheda **Valori effettivi** rivedi l'elenco **Visualizzazione associata valore effettivo**. Viene visualizzato un elenco delle voci originali e di quelle corrette.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
