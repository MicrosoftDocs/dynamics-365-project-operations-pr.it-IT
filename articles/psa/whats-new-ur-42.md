---
title: Novità o modifiche nella versione di aggiornamento 42 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nell'aggiornamento versione Microsoft Dynamics 365 Project Service Automation 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589201"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novità o modifiche nella versione di aggiornamento 42 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 42 di Project Service Automation V3. Questa versione ha il numero di build V3.10.73.61 ed è generalmente disponibile tramite un aggiornamento automatico nell'aprile 2022.

## <a name="update-release-42"></a>Rilascio 42 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**Ore e spesa**

- Quando un foglio presenze viene rifiutato, l'utente che lo ha rifiutato viene identificato erroneamente come **Sistema**.
- Quando vengono importate gli inserimenti ore, il valore **Categoria di risorse** manca.
- I responsabili dell'approvazione del progetto possono approvare i progetti inviati quando le loro autorizzazioni non sono specificatamente impostate su **Può approvare**.

**Vendite**

- Quando i valori effettivi vengono registrati su attività di livello non radice, i costi effettivi vengono aggregati in modo non corretto.
