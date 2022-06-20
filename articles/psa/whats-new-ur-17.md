---
title: Novità o modifiche nella versione di aggiornamento 17 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 17 di Project Service Automation V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915695"
---
# <a name="project-service-automation-update-release-17-v3"></a>Versione di aggiornamento di Project Service Automation 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità.  Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 17 di PSA V3. Questa versione ha il numero di build V3.10.6.34 ed è generalmente disponibile tramite un aggiornamento automatico in marzo 2020.


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
- Risolto: quando la classe di transazione è **Ora**, **UnitGroup** non è modificabile per tutte le entità, tra cui **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** e **ContractLineDetails**. Tuttavia, **Unità** non è editabile solo per **JournalLine** e **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
