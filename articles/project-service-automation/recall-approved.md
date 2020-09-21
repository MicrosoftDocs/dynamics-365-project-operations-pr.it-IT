---
title: Richiamare inserimenti ore o voci di spesa approvati
description: In questo argomento vengono fornite informazioni su come richiamare una transazione di tempo o spesa approvata precedentemente.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752728"
---
# <a name="recall-approved-time-or-expense-entries"></a>Richiamare inserimenti ore o voci di spesa approvati

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un membro del team di progetto o un'altra persona che invia un inserimento ore o una voce di spesa può richiamare tale inserimento o voce dopo l'approvazione. La procedura per richiamare un inserimento ore o una voce di spesa approvato comporta due passaggi:

1. L'autore dell'invio richiede un richiamo.
2. Un responsabile approvazione approva il richiamo.

## <a name="request-a-recall"></a>Richiedere un richiamo

Segui questi passaggi per richiedere il richiamo di un inserimento ore o una voce di spesa approvato.

1. Per gli inserimenti ore, seleziona **Progetti** \> **Attività personali** \> **Inserimento ore**.

    OPPURE

    Per le voci di spesa, seleziona **Progetti** \> **Attività personali** \> **Spese**.

2. Per gli inserimenti ore, seleziona tutti gli inserimenti di una specifica combinazione di progetto e attività. In alternativa, nella griglia, seleziona le singole celle di tempo a una data specifica per un progetto specifico.

    OPPURE

    Per le voci di spesa, seleziona la riga della voce di spesa da richiamare.

3. Seleziona **Richiama**. Viene visualizzata una finestra di dialogo di conferma. Se l'inserimento ore e la voce di spesa selezionati sono già stati approvati, ti viene richiesto di immettere un motivo per il richiamo.
4. Immetti un motivo per il richiamo e quindi seleziona **OK** per confermare l'operazione. Il sistema invia alla persona che ha approvato la voce di spesa o l'inserimento ore una richiesta di approvazione del richiamo.

> [!NOTE]
> Sebbene sia possibile richiamare inserimenti ore e voci di spesa, se uno di questi è già stato fatturato al cliente, una richiesta di richiamo non può essere creata. Un utente che cerca di creare una richiesta di richiamo riceverà un messaggio indicante che l'inserimento ore o la voce di spesa non può essere richiamato in quanto è già stata fatturato.

## <a name="approve-or-reject-a-recall-request"></a>Approvare o rifiutare una richiesta di richiamo

Segui questi passaggi per approvare o rifiutare una richiesta di richiamo.

1. Seleziona **Progetti** \> **Attività personali** \> **Approvazioni**.
2. Nella pagina elenco **Approvazioni**, seleziona la vista **Richieste di richiamo da approvare**. Viene visualizzato un elenco di richieste di richiamo.
3. Seleziona uno o più inserimenti o voci e quindi seleziona **Approva** o **Rifiuta**.
4. Se selezioni **Approva**, viene visualizzato un messaggio di avviso che spiega l'impatto dell'approvazione. Seleziona **OK** per confermare l'operazione. La richiesta di richiamo viene approvata.

    OPPURE

    Se hai selezionato **Rifiuta**, la richiesta di richiamo viene rifiutata.

> [!NOTE]
> Come avviene quando si richiede un richiamo, anche per l'approvazione di un richiamo il sistema verifica le attività di fatturazione negli inserimenti ore o nelle voci di spesa. Se un inserimento ore o una voce di spesa è già stata fatturato o se si trova in una bozza di fattura, il responsabile approvazione riceve un messaggio di errore che indica che l'inserimento ore o la voce di spesa non può essere approvato in quanto è già stato fatturato.

## <a name="impact-of-a-recall-request"></a>Impatto di una richiesta di richiamo

Quando un'approvazione viene richiamata, si ha un impatto operativo e un impatto finanziario.

### <a name="operational-impact"></a>Impatto operativo

Se una richiesta di richiamo viene approvata, il record dell'approvazione viene contrassegnato come **Rifiutato**. Lo stato dell'inserimento ore o della voce di spesa diventa **Restituito** o **Rifiutato**, a seconda se si tratta di un inserimento ore o di una voce di spesa.

Il membro del team di progetto può visualizzare, modificare e quindi inviare di nuovo l'inserimento ore o la voce di spesa oppure eliminarlo completamente.

Se una richiesta di richiamo viene rifiutata, lo stato dell'inserimento ore o della voce di spesa rimane **Approvato** e l'inserimento o la voce non può essere modificato dal membro del team di progetto o dal responsabile approvazione per il progetto.

### <a name="financial-impact"></a>Impatto finanziario

Se una richiesta di richiamo viene approvata, i valori effettivi corrispondenti per costo e vendite vengono aggiornati nel modo seguente:

- Il campo **Stato rettifica** diventa **Rettificato**.
- Il campo **Stato fatturazione** diventa **Annullato**.

Quindi, nella tabella Valori effettivi vengono create scritture di storno. Per creare scritture di storno, il sistema copia i valori di campo dai valori effettivi originali. I soli valori che non vengono copiati sono i valori di quantità. Questi valori vengono invece stornati. Valori effettivi stornati vengono creati per i valori effettivi **Costo** e **Vendite non fatturate**. Il campo **Stato rettifica** dei valori effettivi stornati viene impostato su **Non rettificabile** e il campo **Stato di fatturazione** viene impostato su **Annullato**. A seguito di tali modifiche, la spesa registrata e il backlog dei ricavi del progetto non includono più gli importi che questi valori effettivi rappresentano.

Se una richiesta di richiamo viene rifiutata, non si ha alcun impatto finanziario sul progetto.

## <a name="changes-to-time-entry-records"></a>Modifiche ai record degli inserimenti ore

Nella figura seguente vengono illustrate le modifiche che si verificano per gli inserimenti ore approvati quando vengono richiamati.

![Transizioni dello stato degli inserimenti ore](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Modifiche ai record delle voci di spesa

Nella figura seguente vengono illustrate le modifiche che si hanno per le voci di spesa approvate quando vengono richiamate.

![Transizioni dello stato delle voci di spesa](media/ExpenseEntryStateTransitions.png)
