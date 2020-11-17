---
title: Novità o modifiche nella versione di aggiornamento 19 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 19 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126847"
---
# <a name="project-service-automation-update-release-19-v3"></a>Versione di aggiornamento di Project Service Automation 19, V3

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 19 di PSA V3. Questa versione ha il numero di build V3.10.30.41 ed è generalmente disponibile tramite un aggiornamento automatico a maggio 2020.

## <a name="update-release-19"></a>Rilascio 19 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Tempo e spesa**

Sono stati risolti i seguenti problemi: 

- Gli errori derivati dalle importazioni dell'inserimento ore non vengono visualizzati correttamente.
- La griglia Inserimento ore non supporta il comportamento del campo **Solo data**.
- Le risorse del progetto non sono in grado di creare una spesa con un progetto.

**Gestione progetti**

Sono stati risolti i seguenti problemi: 

-  L'attività del nipote provoca una stima dello sforzo errata durante il calcolo del completamento (EAC).

**Sales**

Sono stati risolti i seguenti problemi: 

- L'azione **Ricalcola** non funzione con i dettagli della voce di contratto delle spese o con i dettagli della riga di offerta.
- **Aggiorna prezzi** mancante per stime di spesa.
-  I clienti non sono in grado di selezionare le ragioni dello stato del contratto personalizzato dalla pagina **Contratto di progetto**.
- Prestazioni compromesse dell'esperienza cliente durante la creazione del listino prezzi personalizzato da un'offerta.
- I clienti rilevano incoerenze nei valori predefiniti di **unità** nelle pagine **Dettagli riga di offerta** e **Dettagli voce di contratto**.
- L'aggiunta di elementi della categoria di transazioni non addebitabili a una voce di contratto addebitabile non rispetterà il tipo di fatturazione **Non addebitabile** della categoria di transazione.
- I clienti non possono utilizzare i ruoli e la categoria appena aggiunti nei contratti precedentemente creati.
- I clienti riscontrano prestazioni compromesse per Recupero non necessario in PreValidateProjectTeamMemberUpdate.cs
- I ruoli configurati come non addebitabili nell'elenco **Categorie di risorse** devono essere aggiunti alla scheda **Ruoli addebitabili** come **Non0chargeable** sulla voce di contratto per un progetto.
- I clienti possono riscontrare prestazioni compromesse durante la creazione di un progetto perché **GetBookableResourceIdFromUser** recupera tutte le colonne di risorse prenotabili anziché solo l'ID principale.
- All'entità **TransactionType** manca il plug-in di aggiornamento preliminare per impedire agli utenti di accedere a **Unità** e **UnitGroups** che non sono validi per i tipi di transazione.
- Il passaggio **Rimuovi** non funziona per l'importazione dell'inserimento ore.
