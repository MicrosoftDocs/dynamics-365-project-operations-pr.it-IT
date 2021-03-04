---
title: Novità di febbraio 2021 - Project Operations per scenari basati su risorse/non stoccate
description: Questo argomento fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di febbraio 2021 di Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ba44ea471f7d72d1e816ec74de304d3fdcf1f68
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141323"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di febbraio 2021 - Project Operations per scenari basati su risorse/non stoccate

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento si applica ai seguenti componenti e versioni di Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse 4.7.0.95
- Gestione progetti e contabilità in ambiente Dynamics 365 Finance versione 10.0.16 

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Area funzionalità** | **Numero di riferimento** | **Aggiornamento di qualità** |
| --- | --- | --- |
| **Prezzi e fatturazione** | 2053736 | I dettagli della riga della fattura sono ora accessibili andando in **Fattura** > **Informazioni correlate**. |
| **Prezzi e fatturazione** | 2122613 | Le azioni **Attiva** e **Disattiva** sono state rimosse dalle entità associate **Listino prezzi**. |
| **Prezzi e fatturazione** | 2128606 | Risolto il problema con **ullReferenceException** nel plug-in **GetEstimatesForProject**. |
| **Distribuzione e configurazione** | 2139346 | Risolto il problema con l'importazione della soluzione non gestita **Dynamics365ProjectOperationsDualWrite**. |
| **Distribuzione e configurazione** | 2140569 | La soluzione di progetto non deve essere installata negli ambienti Dataverse Teams. |
| **Distribuzione e configurazione** | 2086991 | Personalizzazione della localizzazione limitata delle risorse web. |
| **Gestione delle opportunità** | 2136794 | Viene visualizzato il messaggio di errore corretto quando i processo **Conferma fattura** o **Contrassegna fattura come pagata** non riescono. |
| **Gestione delle opportunità** | 2139330 | La modifica del responsabile di progetto su un progetto non deve ripristinare la società proprietaria sul valore predefinito. |
| **Gestione delle opportunità** | 2146376 | L'importo dell'imposta corretto in un valore effettivo non addebitabile viene creato dalla conferma della fattura. |
| **Pianificazione e rilevamento dei progetti** | 2099879 | La distribuzione dell'ambiente Dataverse deve creare una categoria di transazione predefinita con un ID statico e non generarne una in modo casuale per ambiente. |
| **Pianificazione e rilevamento dei progetti** | 2128577 | Corretti i privilegi dell'utente Project Service per aggiornare la categoria di transazione su un'assegnazione di risorse. |
| **Pianificazione e rilevamento dei progetti** | 2164035 | Problemi risolti con la funzione **Copia progetto**. |
| **Inserimento ore** | 2129161 | Vengono applicate restrizioni più rigide per garantire che gli utenti non possano modificare e aggiornare un inserimento ore inviato o approvato. |
| **Inserimento ore** | 2103572 | L'approvazione dell'ora per inserimenti ore non di progetto non deve cercare il ruolo di approvatore del progetto. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Contabilità e gestione dei progetti in Dynamics 365 Finance 

Per ulteriori informazioni sulla gestione dei progetti e la contabilità in Dynamics 365 Finance, vedi [Novità di gennaio 2021 - Project Operations per scenari basati su risorse/non stoccate](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Aggiornamenti normativi

Per informazioni sugli aggiornamenti normativi per le app Finance and Operations, vedi [Aggiornamenti normativi](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Un altro modo per conoscere gli aggiornamenti normativi è accedere a Lifecycle Services (LCS) e visualizzare gli aggiornamenti normativi pianificati utilizzando lo strumento di ricerca dei problemi. La ricerca dei problemi ti consente di cercare per paese, tipo di funzionalità e versione.


[!INCLUDE[footer-include](../includes/footer-banner.md)]