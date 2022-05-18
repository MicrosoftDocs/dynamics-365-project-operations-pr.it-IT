---
title: Novità della versione di novembre 2021 - Distribuzione di Project Operations Lite
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di novembre 2021 della distribuzione di Project Operations Lite.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f3a19cddd1b91fc76c852153526fb7197a9f92c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587775"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Novità della versione di novembre 2021 - Distribuzione di Project Operations Lite

_Si applica a: Distribuzione semplice: dalla transazione alla fatturazione proforma_

Questo argomento si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

In questa release sono incluse le seguenti funzionalità:

- Le API del servizio di pianificazione del progetto supportano ora la possibilità di creare ed eliminare i bucket di progetto

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-in-dataverse"></a>Project Operations in Dataverse

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Prezzi e fatturazione | 2358236 | La correzione fattura deve consentire correzioni con righe a prezzo zero. |
| Gestione risorse | 2410072 | Consente la configurazione di una risorsa assegnata all'attività come project manager. |
| Prezzi e fatturazione | 2430234 | Risoluzione di un problema di calcolo delle prestazioni di costo. |
| Ore e spesa | 2436978 | Possibilità di immettere l'ora nel formato hh:mm. |
| Prezzi e fatturazione | 2448623 | Possibilità di aggiornare i listini prezzi dopo che sono stati associati a un'unità organizzativa. |
| Ore e spesa | 2460396 | Possibilità di eliminare un inserimento ore cancellando la cella. |
| Prezzi e fatturazione | 2467386 | Possibilità di eliminare un progetto con un'attività, anche quando l'attività è associata a un'offerta acquisita. |
| Ore e spesa | 2461744 | La visualizzazione **Approvazioni personali non riuscite** contiene solo le approvazioni di progetto nella fase **Inviato**. |
| Ore e spesa | 2464082 | Rimozione del collegamento dalle approvazioni del progetto nel set di approvazioni in caso di corrispondenza della stato di destinazione. |
| Ore e spesa | 2468108 | Il lavoro di pianificazione non deve impostare uno stato **Elaborazione** per il set di approvazione. |
| Ore e spesa | 2471503 | Eliminazione dei set di approvazione che risalgono a sette giorni prima. |
| Prezzi e fatturazione | 2480687 | Il riferimento alla riga dell'offerta non deve essere rimosso quando viene creato un passaggio fondamentale riga di offerta. |
