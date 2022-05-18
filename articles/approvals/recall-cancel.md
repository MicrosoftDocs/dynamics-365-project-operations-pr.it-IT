---
title: Richiamare gli inserimenti precedentemente approvati
description: Questo argomento spiega come un membro del team di progetto può richiedere il ritiro di record di tempo, spese e utilizzo del materiale precedentemente inviati e approvati e come un project manager può approvare o rifiutare le richieste di richiamo.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586579"
---
# <a name="recall-previously-approved-entries"></a>Richiamare gli inserimenti precedentemente approvati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Un membro del team di progetto che invia un inserimento ore, una voce di spesa o un utilizzo di materiale può richiamare tale inserimento o voce dopo l'approvazione. Il processo di richiamo si svolge in due passaggi principali:

1. L'autore dell'invio richiede un richiamo.
2. Un responsabile approvazione approva la richiesta di richiamo.

## <a name="request-a-recall"></a>Richiedere un richiamo

Segui questi passaggi per richiedere il richiedere un richiamo delle voci approvate di tempo, spesa o utilizzo del materiale.

1. Segui uno di questi passaggi, a seconda del tipo di voce che desideri richiamare:

    - Per gli inserimenti ore, vai in **Progetti** \> **Attività personali** \> **Inserimento ore** e seleziona tutti gli inserimenti di una specifica combinazione di progetto e attività. In alternativa, nella griglia, seleziona le singole celle di tempo a una data specifica per un progetto specifico.
    - Per le voci di spesa, vai in **Progetti** \> **Attività personali** \> **Spese** e seleziona la riga della voce di spesa da richiamare.
    - Per le voci di utilizzo del materiale, vai in **Progetti** \> **Attività personali** \> **Registro dell'utilizzo del materiale** e seleziona la riga della voce di utilizzo del materiale da richiamare.

2. Seleziona **Richiama**. Viene visualizzata una finestra di dialogo di conferma. Se le voci di inserimento ore, spesa o utilizzo del materiale selezionate sono già state approvate, ti viene richiesto di immettere un motivo per il richiamo.
3. Immetti un motivo per il richiamo e quindi seleziona **OK** per confermare l'operazione. Il sistema invia alla persona che ha approvato la voce di spesa o l'inserimento ore una richiesta di approvazione del richiamo.

> [!IMPORTANT]
> Non è possibile creare una richiesta di richiamo per una voce di inserimento ore, spesa o utilizzo del materiale approvata che è già stata fatturata al cliente. Se ci provi, riceverai un messaggio in cui si afferma che non è possibile richiamare la voce di inserimento ore, spesa o utilizzo del materiale perché è stata già fatturata. In questo caso, puoi richiedere il richiamo della voce solo se viene utilizzata una fattura correttiva per emettere un credito completo o un rimborso al cliente sulla fattura originale.

## <a name="approve-or-reject-a-recall-request"></a>Approvare o rifiutare una richiesta di richiamo

Segui questi passaggi per approvare o rifiutare una richiesta di richiamo.

1. Seleziona **Progetti** \> **Attività personali** \> **Approvazioni**.
2. Nella pagina elenco **Approvazioni**, seleziona la vista **Richieste di richiamo da approvare**. Viene visualizzato un elenco di richieste di richiamo.
3. Seleziona uno o più inserimenti o voci e quindi seleziona **Approva** o **Rifiuta**.
4. Se selezioni **Approva**, viene visualizzato un messaggio di avviso che spiega l'impatto dell'approvazione. Seleziona **OK** per confermare l'operazione. La richiesta di richiamo viene approvata.

    OPPURE

    Se hai selezionato **Rifiuta**, la richiesta di richiamo viene rifiutata.

> [!IMPORTANT]
> Quando un richiamo viene approvato, proprio come quando viene richiesto, il sistema verifica l'eventuale attività di fatturazione in base alle voci relative a inserimento ore, spese o utilizzo del materiale. Se un inserimento ore o una voce di spesa è già stata fatturato o se si trova in una bozza di fattura, il responsabile approvazione riceve un messaggio di errore che indica che l'inserimento ore o la voce di spesa non può essere approvato in quanto è già stato fatturato. In questo caso, il responsabile dell'approvazione può approvare il richiamo solo se viene utilizzata una fattura correttiva per emettere un credito completo o un rimborso al cliente sulla fattura originale.

## <a name="impact-of-a-recall-request"></a>Impatto di una richiesta di richiamo

Quando un'approvazione viene richiamata, si ha un impatto operativo e un impatto finanziario.

### <a name="operational-impact"></a>Impatto operativo

Se una richiesta di richiamo viene approvata, il record dell'approvazione viene contrassegnato come **Rifiutato**. Lo stato dell'inserimento ore o della voce di spesa diventa **Restituito** o **Rifiutato**, a seconda se si tratta di un inserimento ore o di una voce di spesa o utilizzo del materiale.

Il membro del team di progetto può visualizzare, modificare e quindi inviare di nuovo l'inserimento ore o la voce di spesa oppure eliminarlo completamente.

Se una richiesta di richiamo viene rifiutata, lo stato dell'inserimento ore o della voce di spesa rimane **Approvato** e l'inserimento o la voce non può essere modificato dal membro del team di progetto o dal responsabile approvazione per il progetto.

### <a name="financial-impact"></a>Impatto finanziario

Se una richiesta di richiamo viene approvata, i valori effettivi corrispondenti per costo e vendite vengono aggiornati nel modo seguente:

- Il campo **Stato rettifica** diventa **Rettificato**.
- Il campo **Stato fatturazione** diventa **Annullato**.

Quindi, nella tabella Valori effettivi vengono create scritture di storno. Per creare scritture di storno, il sistema copia i valori di campo dai valori effettivi originali. I soli valori che non vengono copiati sono i valori di quantità. Questi valori vengono invece stornati. Valori effettivi stornati vengono creati per i valori effettivi **Costo** e **Vendite non fatturate**. Il campo **Stato rettifica** dei valori effettivi stornati viene impostato su **Non rettificabile** e il campo **Stato di fatturazione** viene impostato su **Annullato**. A seguito di tali modifiche, la spesa registrata e il backlog dei ricavi del progetto non includono più gli importi che questi valori effettivi rappresentano.

Se una richiesta di richiamo viene rifiutata, non si ha alcun impatto finanziario sul progetto.

## <a name="changes-to-time-entry-records"></a>Modifiche ai record degli inserimenti ore

Nella figura seguente vengono illustrate le modifiche che si verificano per gli inserimenti ore approvati e i record di approvazione corrispondenti quando vengono richiamati.

![Transizioni dello stato degli inserimenti ore.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Modifiche ai record delle voci di spesa e utilizzo del materiale

Nella figura seguente vengono illustrate le modifiche che si verificano per le voci di spesa e utilizzo del materiale approvate e i record di approvazione corrispondenti quando vengono richiamati.

![Transizioni dello stato delle voci di spesa.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
