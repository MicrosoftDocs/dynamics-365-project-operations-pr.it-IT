---
title: Novità di aprile 2022 - Project Operations per scenari basati su risorse/materiali non stoccati
description: Questo articolo fornisce informazioni sugli aggiornamenti di qualità disponibili nella versione di aprile 2022 di Microsoft Dynamics 365 Project Operations per scenari basati su risorse/materiali non stoccati.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110889"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novità di aprile 2022 - Project Operations per scenari basati su risorse/materiali non stoccati

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo articolo si applica ai seguenti componenti e versioni di Microsoft Dynamics 365 Project Operations:

- Project Operations in ambiente Dataverse versione 4.41.0.45
- Gestione progetti e contabilità in un ambiente Dynamics 365 Finance versione 10.0.26

## <a name="features-included-in-this-release"></a>Funzioni incluse in questo rilascio

Le categorie di approvvigionamento possono essere usate in ordini di acquisto di progetto e fatture fornitore in sospeso. Per altre informazioni, vedi [Utilizzare le categorie di approvvigionamento con ordini di acquisto di progetto e fatture fornitore in sospeso](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aggiornamenti delle mappe a doppia scrittura di Project Operations

La tabella seguente mostra le mappe a doppia scrittura che sono state modificate o aggiunte nella versione di Project Operations di marzo 2022.

| Mapping entità | Versione aggiornata | Commenti |
| -------------- | ------------------- | ------------|
| Entità di esportazione riga di fattura fornitore progetto integrazione Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Questa mappa supporta l'uso delle categorie di approvvigionamento con ordini di acquisto di progetto e fatture fornitore in sospeso. |

Esegui sempre l'ultima versione della mappa nel tuo ambiente e abilita tutte le mappe di tabelle correlate mentre aggiorni la tua soluzione Project Operations Dataverse e la versione della soluzione Finance. Alcune funzionalità potrebbero non funzionare correttamente se l'ultima versione della mappa non è attivata. Puoi vedere la versione attiva della mappa nella colonna **Versione** della pagina **Doppia scrittura**. Per attivare una nuova versione della mappa, seleziona **Versioni mappa tabella** e l'ultima versione, quindi salva la versione selezionata. Se hai personalizzato un mapping di tabella predefinito, applica nuovamente le modifiche. Per ulteriori informazioni, vedi [Gestione del ciclo di vita di un'applicazione](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se riscontri un problema durante l'avvio della mappa, segui le istruzioni nella sezione [Problema di colonne di tabella mancanti sulle mappe](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) della guida alla risoluzione dei problemi della doppia scrittura.

## <a name="quality-updates"></a>Aggiornamenti di qualità

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Area funzionalità | Numero di riferimento | Aggiornamento di qualità |
| ------------ | ---------------- | -------------- |
| Tempistica e spesa | 2573900 | La funzionalità **Approvazione moderna** deve essere abilitata per impostazione predefinita. |
| Determinazione dei prezzi e fatturazione | 2603313 | Risolto un errore di record duplicato che impediva l'aggiunta di righe di offerta e contratto con un prodotto. |
| Distribuzione e configurazione | 2611368 | I clienti devono essere in grado di aggiungere fino a cinque entità personalizzate alla soluzione usando la finestra di progettazione app moderna. |
| Tempistica e spesa | 2628285 | Risolto un problema che influiva sulla possibilità di impostare la corretta categoria di risorse per l'importazione dell'ora. |
| Gestione delle opportunità| 2628815 | Aggiorna il limite di caratteri della descrizione dettagliata della riga di offerta in modo che corrisponda al limite di caratteri dell'oggetto dell'attività, così che l'importazione abbia esito positivo per le attività in cui l'oggetto è più lungo di 100 caratteri. |
| Tempistica e spesa| 2629547 | Il campo **Inviato da** delle approvazioni di progetto deve puntare all'utente che ha inviato il record. |
| Tempistica e spesa| 2629865 | Il campo **Copia categoria** delle attività quando i progetti vengono copiati. |
| Tempistica e spesa| 2636463 | Corretti i filtri sulle approvazioni nei moduli di approvazione moderni. |
| Pianificazione e rilevamento dei progetti | 2648300 | Risolto un problema che impediva la modifica del proprietario del progetto. |
| Determinazione dei prezzi e fatturazione | 2563000 | Le righe del giornale di registrazione per una vendita non fatturata in cui la valuta è diversa dalla valuta del contratto non devono essere consentite. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestione progetti e contabilità in Dynamics 365 Finance

Per informazioni sulle correzioni di bug incluse in questo aggiornamento, accedi a Microsoft Dynamics Lifecycle Services (LCS), e visualizza [l'articolo KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
