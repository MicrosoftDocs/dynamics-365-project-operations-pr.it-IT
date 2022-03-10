---
title: Annullare inserimenti ore e voci di spesa approvate precedentemente
description: In questo argomento vengono fornite informazioni su come annullare una transazione di tempo e spesa di progetto approvata.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 09b85ea302ac46171afbd531a551aa5fbf5492a3644cba3448be03009840228c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987441"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Annullare inserimenti ore o voci di spesa approvate precedentemente

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nell'ultima versione di Dynamics 365 Project Service Automation, i responsabili approvazione possono annullare gli inserimenti ore o le voci di spesa approvate precedentemente.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Annullare un inserimento ore o una voce di spesa approvata precedentemente

Segui questi passaggi per annullare un inserimento ore o una voce di spesa approvata precedentemente.

1. Seleziona **Progetti** \> **Attività personali** \> **Approvazioni**.
2. Nella pagina elenco **Approvazioni**, seleziona la vista **Approvazioni personali passate**. Viene visualizzato un elenco di inserimenti ore e voci di spesa approvate in precedenza.
3. Seleziona una o più voci o inserimenti e quindi seleziona **Annulla approvazione**. Viene visualizzato un messaggio di avviso.
4. Seleziona **OK** per annullare l'approvazione.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Comprendere l'impatto dell'annullamento dell'approvazione di un inserimento ore o di una voce di spesa

Quando si annulla un'approvazione, si ha un impatto operativo e un impatto finanziario.

### <a name="operational-impact"></a>Impatto operativo

Per quanto riguarda le operazioni, quando si annulla un'approvazione, lo stato del record diventa **Bozza** e l'approvazione non è più visualizzata nella vista **Approvazioni personali passate**. L'approvazione annullata è invece visualizzata nella vista **Inserimenti ore per l'approvazione** o nella vista **Voci di spesa per l'approvazione**, a seconda se si tratti di un inserimento ore o di una voce di spesa. Inoltre, lo stato dell'inserimento ore o della voce di spesa correlata diventa **Inviato**, di modo che la voce o l'inserimento correlato sia coerente con le approvazioni il cui stato è **Bozza**.

Come responsabile approvazione, puoi modificare alcuni campi di un'approvazione il cui stato è **Bozza**. Questi campi includono **Tipo di fatturazione** e **Ore fatturabili per inserimenti ore**. Dopo avere apportato le modifiche, puoi approvare di nuovo il record. In alternativa, puoi rifiutare la voce o l'inserimento. Se rifiuti l'approvazione di un inserimento ore, lo stato dell'inserimento diventa **Restituito**. Se rifiuti l'approvazione di una voce di spesa, lo stato diventa **Rifiutato**. Da un punto di vista funzionale, le voci e gli inserimenti restituiti e rifiutati hanno lo stesso comportamento di quelli il cui stato è **Bozza**. Un membro del team di progetto può apportare qualsiasi modifica necessaria alla voce o all'inserimento e quindi inviarlo di nuovo per l'approvazione oppure eliminarlo completamente.

### <a name="financial-impact"></a>Impatto finanziario

L'annullamento di un'approvazione ha anche un impatto finanziario su un progetto. Innanzitutto, i valori effettivi corrispondenti di costo e vendita vengono aggiornati nel modo seguente:

- Lo stato di rettifica diventa **Rettificato**.
- Lo stato di fatturazione diventa **Annullato**.

Quindi, nella tabella Valori effettivi vengono create scritture di storno. Per creare scritture di storno, il sistema copia i valori di campo dai valori effettivi originali. I soli valori che non vengono copiati sono i valori di quantità. Questi valori vengono invece stornati. Valori effettivi stornati vengono creati per i valori effettivi **Costo** e **Vendite non fatturate**. Il campo **Stato rettifica** dei valori effettivi stornati viene impostato su **Non rettificabile** e lo stato di fatturazione viene impostato su **Annullato**.

Dopo aver eseguito tali modifiche, l'importo che viene registrato come speso nel progetto e nel backlog dei ricavi del progetto non include più gli importi che questi valori effettivi rappresentano.


[!INCLUDE[footer-include](../includes/footer-banner.md)]