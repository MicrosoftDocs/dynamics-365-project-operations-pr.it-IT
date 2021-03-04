---
title: Novità o modifiche nella versione di aggiornamento 16 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 16 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 882ee6c25e5d88db22e051254c7fd82dc787ab73
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143638"
---
# <a name="project-service-automation-update-release-16-v3"></a>Versione di aggiornamento di Project Service Automation 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.  Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedi [Installare o aggiornare una soluzione preferita](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 16 di PSA V3. Questa versione ha il numero di build V3.10.6.34 ed è generalmente disponibile tramite un aggiornamento automatico in gennaio 2020.


## <a name="update-release-16"></a>Rilascio 16 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

-   Tempo e spesa

    -   Risolto: gli utenti che tentano di inviare voci di spesa e inserimenti ore eliminati per le approvazioni riceveranno ora messaggi di errore rilevanti.

-   Gestione progetti

    -   Risolto: le unità gestione risorse definite per i membri del team nei modelli sono rispettate con i modelli applicati a un nuovo progetto.

    -   Risolto: gestione migliorata della riassegnazione della proprietà dei record.

    -   Risolto: i progetti in fase di copia non potranno essere copiati fino al completamento di tutte le operazioni di copia.

-   Gestione risorse

    -   Risolto: l'estensione delle prenotazioni gestiscono ora correttamente le durate brevi e non creano più valori pari a 0 (zero) ore per le prenotazioni estese.

    -   Risolto: la visualizzazione della riconciliazione è ora soggetta a rendering quando il fuso orario del progetto è +5:30 GMT e l'ora dell'utente è diversa.

-   Sales

    -   Risolto: quando un progetto mappato a una voce di contratto veniva rimosso e veniva mappato un nuovo progetto, i record effettivi sul nuovo progetto non venivano rivalutati in base alle regole di fatturazione e determinazione dei prezzi definite nella voce di contratto. Questo problema è stato risolto in questa versione. Prezzi e record effettivi sul nuovo progetto mappato verranno annullati e ricreati correttamente in base alle regole di fatturazione e determinazione dei prezzi della voce di contratto. Anche i record effettivi del progetto non mappato verranno rivalutati e ricreati di conseguenza.

    -   Risolto: è stata aggiunta un'ulteriore convalida al campo **Quantità** di un riga di stima per garantire che i valori null non siano persistenti.

    -   Risolto: quando sono stati aggiornati i valori effettivi su un progetto, è stato aggiunto un pulsante di aggiornamento al modulo principale del progetto per consentire agli utenti di risincronizzare i valori effettivi.

    -   Risolto: quando gli utenti eseguono l'aggiornamento da 2.X a 3.X, saranno consentiti progetti con un valore NULL per il nome del progetto.



[!INCLUDE[footer-include](../includes/footer-banner.md)]