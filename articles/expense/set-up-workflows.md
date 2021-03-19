---
title: Impostare flussi di lavoro per la gestione delle spese
description: È possibile impostare un processo del flusso di lavoro utilizzato per esaminare e approvare i documenti di viaggio e di spesa.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276038"
---
# <a name="set-up-workflows-for-expense-management"></a>Impostare flussi di lavoro per la gestione delle spese

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

È possibile impostare un processo del flusso di lavoro per esaminare e approvare i documenti di viaggio e di spesa. Puoi definire flussi di lavoro per note spese, richieste di viaggio e richieste di anticipo in contanti.

Un flusso di lavoro rappresenta un processo aziendale e definisce il modo in cui un documento scorre attraverso il sistema. Il flusso di lavoro indica anche chi deve completare un'attività o approvare un documento. Ci sono diversi vantaggi nell'utilizzo del sistema di flusso di lavoro nella tua organizzazione:

- **Processi coerenti**: puoi definire il processo di approvazione per documenti specifici, come richieste di acquisto e note spese. L'utilizzo del sistema del flusso di lavoro aiuta a garantire che i documenti vengano elaborati e approvati in modo coerente ed efficiente.
- **Visibilità del processo**: puoi tenere traccia dello stato, della cronologia e delle metriche delle prestazioni di una specifica istanza del flusso di lavoro. Ciò ti consente di determinare se è necessario apportare modifiche al flusso di lavoro per migliorare l'efficienza.
- **Elenco di lavoro centralizzato**: gli utenti possono visualizzare un elenco di lavoro centralizzato per vedere le attività del flusso di lavoro e le approvazioni loro assegnate. 

## <a name="workflow-types"></a>Tipi di flusso di lavoro

Nella tabella seguente sono elencati i tipi di flusso di lavoro che puoi creare in **Gestione delle spese**.


|              <strong>Tipo</strong>              |                   <strong>Usa questo tipo per</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Approvazione automatica di note spese</strong> |            Creare flussi di lavoro di approvazione per le note spese.             |
|  <strong>Registrazione automatica di note spese</strong>   |        Creare flussi di lavoro di registrazione automatica per le note spese.        |
|       <strong>Voce di spesa</strong>        |     Creare flussi di lavoro di approvazione per le voci di spesa nelle note spese.      |
| <strong>Registrazione automatica delle voci di spesa</strong> | Creare flussi di lavoro di registrazione automatica per le voci di spesa nelle note spese. |
|       <strong>Richiesta di viaggio</strong>       |          Creare flussi di lavoro di approvazione per le richieste di viaggio.           |
|      <strong>Richiesta di anticipo in contanti</strong>      |         Creare flussi di lavoro di approvazione per richieste di anticipo in contanti.          |
|        <strong>Recupero dell'IVA</strong>        | Creare flussi di lavoro di approvazione per il recupero dell'IVA.  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]