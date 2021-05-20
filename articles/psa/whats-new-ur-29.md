---
title: Novità o modifiche nella versione di aggiornamento 29 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 29 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948647"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novità o modifiche nella versione di aggiornamento 29 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 29 di Project Service Automation V3. Questa versione ha un numero di build di V3.10.47.7 ed è generalmente disponibile tramite un aggiornamento automatico a febbraio 2021.

## <a name="update-release-29"></a>Rilascio 29 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Ore e spesa**

Sono stati risolti i seguenti problemi:

- Gli utenti non possono vedere le ore lavorative registrate nei giorni non lavorativi nella griglia di inserimento ore.
- Le voci di spesa approvate possono essere modificate nella griglia.

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- Logica di convalida mancante per garantire che le ore di lavoro per l'assegnazione delle risorse non possano essere negative.
- L'azione personalizzata, **AssignResourcesForTask** aggiorna tutti i campi anziché solo i campi modificati.
- Quando si copia un progetto in un ambiente con plug-in o flussi di lavoro registrati nell'evento **CreateProject**, l'attributo **msdyn_bulkgenerationstatus** non viene aggiornato se **CopyWBSToProject** non riesce.
- Quando si espande il calendario del progetto, i giorni lavorativi non vengono ordinati in ordine crescente, causando il mancato aggiornamento di alcune attività del progetto.
- La modifica del responsabile di progetto su un progetto esistente attiva la logica predefinita dell'unità organizzativa.

**Vendite**

Sono stati risolti i seguenti problemi:

- La scheda **Esecuzione contratto** nella pagina **Contratto** non riesce silenziosamente durante l'inizializzazione quando non sono presenti righe di contratto.