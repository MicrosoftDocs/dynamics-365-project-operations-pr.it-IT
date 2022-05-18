---
title: Concetti chiave
description: In questo argomento vengono fornite informazioni sui concetti chiave per la gestione delle risorse in Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 3a0305ab35a28348798f9d9c7452b3bee75412e4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601253"
---
# <a name="key-concepts"></a>Concetti chiave

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nella tabella seguente vengono definiti i concetti chiave utilizzati nell'app Dynamics 365 Project Service Automation.

| Concetto                    | Definizione |
|----------------------------|------------|
| Membro del team di progetto        | Come parte del team di progetto, un membro del team di progetto può essere una risorsa denominata che ha prenotazioni, una risorsa denominata che non ha prenotazioni oppure una risorsa generica. Le risorse generiche non hanno prenotazioni, sono locali al progetto e non hanno vincoli di capacità nei progetti. |
| Risorsa generica di progetto   | Un risorsa segnaposto che consente di formare un team e assegnare risorse a un piano di progetto senza dover conoscere la risorsa denominata. Il calendario di progetto viene utilizzato come calendario della risorsa generica. Le risorse generiche possono essere aggiunte a un team di progetto e assegnate ad attività. |
| Ore prenotate               | Le ore delle risorse sono prenotate definitivamente per un progetto per garantire il completamento del lavoro del progetto. Le ore prenotate sono consumate a partire dalla capacità globale della risorsa. Le prenotazioni sono possibili solo per le risorse denominate e non per quelle generiche. |
| Ore assegnate             | Le ore delle risorse sono assegnate ad attività nella pianificazione di progetto. Le assegnazioni vengono eseguite per le risorse denominate o quelle generiche. Le assegnazioni possono essere indipendenti dalle prenotazioni. |
| Ore richieste             | La capacità richiesta ma non ancora soddisfatta da una risorsa denominata. Le ore richieste sono rilevanti solo per i membri del team generici che hanno generato i requisiti di risorsa. |
| Domanda                     | Il carico di lavoro corrente e quello in arrivo. In Project Service Automation, la domanda viene visualizzata come requisiti di risorsa o richieste di risorsa. |
| Requisito di risorsa       | Un'entità utilizzata per acquisire ore richieste, date di inizio e di fine, competenze, geografia e altre dimensioni di determinazione dei prezzi per le risorse richieste. I requisiti di risorsa vengono generati dai membri del team di progetto o creati individualmente. |
| Richiesta di risorsa           | Un'entità utilizzata come "busta" per trasmettere il requisito di risorsa che deve essere soddisfatto da un responsabile delle risorse. |
| Ruolo predefinito della risorsa      | Il ruolo in cui una risorsa viene raggruppata per il calcolo dell'utilizzo. Si suppone che la risorsa abbia le competenze richieste per il ruolo e che soddisfi l'utilizzo di destinazione per quel ruolo. |
| Unità organizzativa della risorsa | L'unità organizzativa a cui una risorsa è assegnata. |
| Profilo di distribuzione                    | Ore di assegnazione, attività o requisito suddivise in una distribuzione giornaliera. Ad esempio, un'attività di 40 ore durante cinque giorni può essere ripartita in otto ore al giorno per cinque giorni. |
| Vista Riconciliazione        | Una vista che mostra le prenotazioni e le assegnazioni di ogni membro del team di progetto. Questa vista consente al responsabile di progetto di individuare qualsiasi differenza tra prenotazioni e assegnazioni e di intraprendere un'azione correttiva. |
| Ore lavorative                 | Un'entità utilizzata per identificare la capacità della risorsa nonché le ore lavorative e non lavorative. Questa entità è nota anche come calendario risorsa. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
