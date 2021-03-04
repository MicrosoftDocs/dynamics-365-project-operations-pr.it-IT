---
title: Flusso di lavoro per la gestione delle spese
description: Questo argomento spiega come utilizzare il sistema di flusso di lavoro in Microsoft Dynamics 365 Finance per impostare un processo di revisione per le note spese in Gestione spese.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960567"
---
# <a name="expense-management-workflow"></a>Flusso di lavoro per la gestione delle spese

Puoi utilizzare il sistema di flusso di lavoro per impostare un processo di revisione per le note spese in Gestione spese. Puoi impostare un flusso di lavoro che utilizza i seguenti criteri per determinare chi approva le note spese:

- La gerarchia dei dipendenti e i limiti di approvazione predefiniti
- Approvazione multilivello che supporta approvatori temporanei e un approvatore finale
- Dimensioni finanziarie e responsabilità del progetto
- Assegnazione a utenti o gruppi di utenti specifici

Puoi creare approvazioni del flusso di lavoro per note spese, richieste di viaggio, anticipi di cassa e recupero dell'IVA.

**Esempio**

Il processo seguente è un esempio del flusso di lavoro di gestione delle spese per una nota spese.

1. Un dipendente crea e salva una nota spese.
2. Il dipendente invia la nota spese per l'approvazione. Il responsabile approvazione viene identificato in base alle regole definite durante l'impostazione del flusso di lavoro.
3. Il responsabile approvatore riceve una notifica indicante che una nota spese è pronta per l'approvazione. Il responsabile approvatore esamina la nota spese e verifica che siano soddisfatte le seguenti condizioni:

    - Le spese non violano alcun criterio di spesa. Se una spesa viola un criterio, il responsabile approvatore verifica che la nota spese includa una motivazione aziendale valida.
    - Le ricevute elettroniche sono collegate alla nota spese.

4. Il responsabile approvatore approva la nota spese.
5. La nota spese viene assegnata al coordinatore della contabilità fornitori per la registrazione.
6. Si verifica uno dei seguenti passaggi, a seconda che la registrazione automatica sia configurata o meno:

    - Se è configurata la registrazione automatica, la nota spese viene elaborata per il pagamento e lo stato della nota spese viene aggiornato.
    - Se la registrazione automatica non è configurata, il coordinatore della contabilità fornitori verifica che tutte le ricevute originali siano state inviate e che le ricevute siano corrispondenti alle spese nella nota spese. Anche tutti i codici IVA inseriti nella nota spese devono essere verificati come corretti.

Dopo aver verificato questi requisiti, viene registrata la nota spese.

Dopo la registrazione della nota spese, il pagamento viene autorizzato per la nota spese e il dipendente viene rimborsato.


[!INCLUDE[footer-include](../includes/footer-banner.md)]