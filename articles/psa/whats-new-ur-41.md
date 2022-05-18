---
title: Novità o modifiche nella versione di aggiornamento 41 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nell'aggiornamento versione Microsoft Dynamics 365 Project Service Automation 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580921"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novità o modifiche nella versione di aggiornamento 41 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 41 di Project Service Automation V3. Questa versione ha il numero di build V3.10.62.162 ed è generalmente disponibile tramite un aggiornamento automatico in marzo 2022.

## <a name="update-release-41"></a>Rilascio 41 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**Gestione progetti**
- Quando tenti di creare un progetto da un modello basato su un progetto creato dal componente aggiuntivo desktop, viene visualizzato il seguente messaggio di errore: "Convalida del campo Lavoro pianificato di assegnazione risorse. La data di fine di ogni porzione di tempo di assegnazione risorse non deve precedere la relativa data di inizio".

**Ore e spesa**
- Quando tenti di eliminare un inserimento ore, viene visualizzato il seguente messaggio di errore "Si è verificato un errore imprevisto dal codice ISV".

**Vendite**
- Quando crei una fattura per un passaggio fondamentale a prezzo fisso, i campi **Descrizione** e **Descrizione esterna** non sono popolati. 
