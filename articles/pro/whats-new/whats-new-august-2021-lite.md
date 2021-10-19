---
title: Novità di agosto 2021 - Distribuzione lite di Project Operations
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di agosto 2021 della distribuzione semplice di Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323511"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Novità di agosto 2021 - Distribuzione lite di Project Operations

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

  - Project Operations in ambiente Dataverse versione 4.13.0.152

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- **Set di approvazione**: i set di approvazione consentono di raggruppare le richieste di approvazione di ore, spese o utilizzo dei materiali in sottoinsiemi di operazioni più piccoli. Questo raggruppamento consente di elaborare le approvazioni per progetto, in un ordine specifico e consente di riprovare e mettere in sequenza. Il raggruppamento delle richieste migliora l'affidabilità e la tracciabilità del processo di approvazione per grandi volumi di approvazioni. Per ulteriori informazioni, vedi [Set di approvazione](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| Determinazione dei prezzi e fatturazione | 2295625 | Il nome del passaggio fondamentale deve essere copiato dalla pianificazione delle fatture nei dettagli della voce della fattura. |
| Determinazione dei prezzi e fatturazione | 2316323 | Lo sconto non deve essere modificabile su una fattura proforma in Project Operations per scenari basati sulle risorse. |
| Gestione delle opportunità | 2338619 | Le regole di business **Opportunità** e **Offerta** devono essere invocate solo nelle pagine. |
| Gestione delle risorse | 2316523 | Usando **Invia richiesta** da un requisito di risorsa a cui è associato un ruolo non dovrebbe visualizzare un errore. |
| Gestione delle risorse | 2326885 | La creazione di un requisito di risorse tramite un progetto non dovrebbe visualizzare un errore. |
| Tempistica e spesa | 2335584 | Flussi di attività deprecati nell'inserimento ore. |
| Tempistica e spesa | 2336884 | Il pulsante dell'inserimento ore **Copia settimana** deve funzionare non solo per l'utente corrente. |