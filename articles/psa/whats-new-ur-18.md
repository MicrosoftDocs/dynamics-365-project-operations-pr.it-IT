---
title: Novità o modifiche nella versione di aggiornamento 18 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 18 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078830"
---
# <a name="project-service-automation-update-release-18-v3"></a>Versione di aggiornamento di Project Service Automation 18, V3

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 18 di Project Service Automation V3. Questa versione ha il numero di build V3.10.8.12 ed è generalmente disponibile tramite un aggiornamento automatico nell'aprile 2020.

## <a name="update-release-18"></a>Rilascio 18 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Tempo e spesa**

- Corretto: i flussi **Richiama** , **Richiesta** e **Annulla approvazione** generano eccezioni con messaggi di errore poco chiari.
- Corretto: quando **Annulla approvazione** non riesce per una spesa, non viene generato un errore di eccezione rilevante.
- Corretto: la griglia di inserimento dell'ora gestisce erroneamente i giorni non lavorativi in Australia dopo il cambio dell'ora legale (DST) in ottobre.
- Corretto: una logica predefinita errata impedisce l'invio delle spese.
- Corretto: quando l'approvazione dell'immissione del tempo non riesce, l'approvazione rimane nello stato **In sospeso**.
- Corretto: errori SQL nelle approvazioni in blocco (deadlock/timeout).
- Corretto: problemi significativi relativi alle prestazioni nell'esperienza utente causati dall'aggiornamento dei membri del team durante l'approvazione delle immissioni del tempo.

**Gestione progetti**

- Corretto: notifica del fuso orario spostata dalla visualizzazione **Riconciliazione** al modulo principale **Progetto**.
- Corretto: il modello di calendario non è correttamente predefinito quando si apre un nuovo modulo di progetto.
- Corretto: per i browser basati su Cromo, gli utenti non sono in grado di selezionare facilmente le attività precedenti da eliminare.
- Corretto: la creazione o la copia di un **progetto da modello vuoto** recupera assegnazioni non correlate.
- Corretto: in casi limite specifici, la creazione di una nuova assegnazione dalla griglia delle attività comporta la creazione di record duplicati.
- Corretto: in modalità manuale, gli utenti non sono in grado di aggiornare le date di inizio dell'attività in modo che siano successive alla data corrente salvata.

**Gestione risorse**

- Corretto: la riga del totale parziale della visualizzazione **Riconciliazione** calcola erroneamente la varianza delle prenotazioni dopo l'estensione delle prenotazioni.
- Corretto: la visualizzazione **Riconciliazione** visualizza erroneamente le assegnazioni delle risorse quando la risorsa prenotabile ha un calendario che non corrisponde al calendario del progetto.

**Sales**

- Corretto: quando le immissioni del tempo sono state nuovamente approvate ( **Approva > Annulla >** approva di nuovo), viene creato un duplicato non addebitabile effettivo.
