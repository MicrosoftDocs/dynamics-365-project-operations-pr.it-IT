---
title: Novità di maggio 2022 - Project Operations per scenari basati su risorse/materiali non stoccati
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di maggio 2022 di Microsoft Dynamics 365 Project Operations per scenari basati su risorse/non stoccate.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921399"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di maggio 2022 - Project Operations per scenari basati su risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.42.0.70
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

Non sono disponibili aggiornamenti per le mappe a doppia scrittura di Project Operations in questa versione. Per un elenco corrente e le versioni delle mappe a doppia scrittura di Project Operations, vedi [Versioni della mappa a doppia scrittura di Project Operations](../environment/resource-dual-write-maps.md).

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità
### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| --- | --- | --- |
| Gestione delle risorse | 2634019 | Messaggi di errore migliorati per le convalide aziendali quando si aggiungono membri del team generici come risorse. |
| Pianificazione e rilevamento dei progetti | 2648515 | Aggiornamenti limitati di **ownerid**, **state**, e **status** nelle entità di pianificazione. |
| Determinazione dei prezzi e fatturazione | 2653167 | Il separatore decimale della griglia **Stime** deve seguire le impostazioni del formato in **Opzioni personali**. |
| Determinazione dei prezzi e fatturazione| 2662251 | I valori nei campi **Unità corretta** e **Gruppo di unità** sono predefiniti durante la creazione di record nelle stime dei materiali. |
| Determinazione dei prezzi e fatturazione| 2571408 | Le vendite effettive non fatturate vengono contrassegnate con un ID fattura proforma per la creazione di una bozza di fattura. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestione progetti e contabilità in Dynamics 365 Finance

Per informazioni sulle correzioni di bug incluse in questo aggiornamento, accedi a Microsoft Dynamics Lifecycle Services (LCS), e visualizza [l'articolo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
