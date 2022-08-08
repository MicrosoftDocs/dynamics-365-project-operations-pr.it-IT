---
title: Funzionalità rimosse o deprecate in Dynamics 365 Project Operations
description: In questo articolo vengono descritte le funzionalità rimosse, o di cui è stata progettata la rimozione da Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028334"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Funzionalità rimosse o deprecate in Dynamics 365 Project Operations

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, distribuzione lite: transazioni di fatturazione proforma e Project Operations per scenari basati su materiali stoccati/produzione_

In questo articolo vengono descritte le funzionalità rimosse, o di cui è stata progettata la rimozione da Dynamics 365 Project Operations.

- Una funzionalità *rimossa* non è più disponibile nel prodotto.
- Una funzionalità *deprecata* non è in fase di sviluppo attivo e potrebbe essere rimossa in un aggiornamento futuro.

Questo elenco ha lo scopo di aiutarti a considerare queste rimozioni e deprecazioni per la tua pianificazione.

> [!NOTE]
> Informazioni dettagliate sugli oggetti nelle app per finanza e operazioni sono disponibili nei [**Report tecnici di riferimento**](/dynamics/s-e/global/axtechrefrep_61). È possibile confrontare le diverse versioni dei report per ottenere informazioni sugli oggetti che sono stati modificati o rimossi in ogni versione delle app per la finanza e le operazioni.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funzionalità rimosse o deprecate nella versione di marzo 2022 di Project Operations

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parametro "Crea sempre transazione di rettifica" di Gestione progetti e contabilità.

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo della deprecazione/rimozione** | Le operazioni di rettifica sono necessarie ai fini del controllo. Dopo la deprecazione, questo parametro sarà nascosto. Il sistema creerà sempre transazioni di rettifica, proprio come fa attualmente quando il parametro è impostato su **sì**. |
| **Sostituita da un'altra funzionalità?** | No |
| **Aree del prodotto interessate** | Applicazione |
| **Opzioni di distribuzione** | Project Operations per scenari basati su materiali stoccati/produzione |
| **Stato** | Deprecato: entro il 1 marzo 2023, nasconderemo il parametro e modificheremo il comportamento del sistema in modo che le transazioni di rettifica vengano sempre create. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parametro "Utilizza data di rettifica come nuova data di progetto" di Gestione progetti e contabilità.

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo della deprecazione/rimozione** | Questo parametro è stato originariamente utilizzato per consentire le rettifiche quando un periodo fiscale era chiuso. Tuttavia, non è più necessario, perché la data contabile della transazione può essere modificata alla prima data del periodo aperto, se configurata. La data del progetto non deve essere modificata, perché rappresenta la data in cui è avvenuta la transazione. |
| **Sostituita da un'altra funzionalità?** | No |
| **Aree del prodotto interessate** | Applicazione |
| **Opzioni di distribuzione** | Project Operations per scenari basati su materiali stoccati/produzione |
| **Stato** | Deprecato: entro il 1 marzo 2023, nasconderemo il parametro e modificheremo il comportamento del sistema in modo che la data del progetto non venga mai modificata durante le rettifiche. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Flusso di lavoro per la richiesta di risorse in Project Operations per scenari basati su materiali stoccati/produzione

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo della deprecazione/rimozione** | Deprecato a causa del basso utilizzo e delle limitazioni del volume delle transazioni. |
| **Sostituita da un'altra funzionalità?** | No |
| **Aree del prodotto interessate** | Applicazione |
| **Opzioni di distribuzione** | Project Operations per scenari basati su materiali stoccati/produzione |
| **Stato** | Deprecato: entro il 1 marzo 2023, disabiliteremo l'opzione per richiedere le risorse per il progetto utilizzando il flusso di lavoro. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Pagina della proposta di fattura del progetto senza viste Intestazione e Righe

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo della deprecazione/rimozione** | Deprecato a causa di miglioramenti alla pagina che è stata introdotta insieme alla chiave di funzionalità **Utilizza proposta di fattura di progetto e moduli di giornali di registrazione fatture con la vista Intestazione e Righe**. |
| **Sostituita da un'altra funzionalità?** | Sì |
| **Aree del prodotto interessate** | Applicazione |
| **Opzioni di distribuzione** | Project Operations per scenari scenari basati su materiali stoccati/produzione, Project Operations per scenari di risorse/materiali non stoccati |
| **Stato** | Deprecato: entro il 1 marzo 2023, la pagina precedente (legacy) verrà disattivata e verrà attivata la chiave di funzionalità **Utilizza proposta di fattura di progetto e moduli di giornali di registrazione fatture con la vista Intestazione e Righe** per impostazione predefinita. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funzionalità rimosse o deprecate nella versione di dicembre 2021 di Project Operations

### <a name="collaboration-workspaces"></a>Collaborazione in aree di lavoro

[Creare o collegare un'area di lavoro di collaborazione (progetto)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo della deprecazione/rimozione** | Deprecata a causa del basso utilizzo. I clienti che utilizzano Project Operations per scenari di risorse/materiali non stoccati possono usare la [Collaborazione con i gruppi di Office](../project-management/collaboration-groups.md). |
| **Sostituita da un'altra funzionalità?** | No |
| **Aree del prodotto interessate** | Applicazione  |
| **Opzioni di distribuzione** | Project Operations per scenari basati su materiali stoccati/produzione |
| **Stato** | Deprecato: entro il 1° dicembre 2022, prevediamo di non supportare più le aree di lavoro di collaborazione. |
