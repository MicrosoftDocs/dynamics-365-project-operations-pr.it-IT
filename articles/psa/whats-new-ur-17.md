---
title: Novità o modifiche nella versione di aggiornamento 17 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 17 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078832"
---
# <a name="project-service-automation-update-release-17-v3"></a>Versione di aggiornamento di Project Service Automation 17, V3

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.  Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 17 di PSA V3. Questa versione ha il numero di build V3.10.6.34 ed è generalmente disponibile tramite un aggiornamento automatico in marzo 2020.


## <a name="update-release-17"></a>Rilascio 17 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Generali**

- Risolto: aggiornamento di Project Service Automation per applicare le licenze Membro del team (Hub risorse progetto includerà i metadati del piano di servizio Membro del team 3.x)
 
**Tempo e spesa**

- Risolto: non è possibile modificare una stima spese da un prezzo diverso da zero (0) a zero (0). La modifica viene ignorata.

**Gestione progetti**

- Risolto: un controllo per i valori null è stato aggiunto sul nome della posizione di un membro del team.
- Risolto: campo **msdyn_userresourceid** sull'entità **msdyn_resourceassignment** deprecato.
- Risolto: l'aggiornamento da 2.x a 3.x gestisce ora i profili di lavoro sulle assegnazioni delle attività.

**Sales**

- Risolto: **Invoice.PreValidateInvoiceUpdate** gestisce ora lo scenario di riassegnazione corretta dei proprietari dei record.
- Risolto: quando la classe di transazione è **Ora** , **UnitGroup** non è modificabile per tutte le entità, tra cui **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** e **ContractLineDetails**. Tuttavia, **Unità** non è editabile solo per **JournalLine** e **InvoiceLineDetails**.


