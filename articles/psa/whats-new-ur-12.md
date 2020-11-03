---
title: Novità o modifiche nella versione di aggiornamento 12 di Project Service Automation V3
description: Questo argomento fornisce informazioni sulle novità dell'aggiornamento rilascio 12 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 62c3a0c5cfbecb568faef570da309c20afd86de9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078837"
---
# <a name="project-service-automation-update-release-12-v3"></a>Versione di aggiornamento di Project Service Automation 12, V3
Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Dynamics 365 Project Service Automation (PSA). Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per aggiornare a questa versione, visitare l'interfaccia di amministrazione di Dynamics 365 online e andare alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 12 di Project Service Automation V3. Questa versione ha il numero di build V3.10.2.34 ed è generalmente disponibile tramite un aggiornamento automatico in ottobre 2019.

## <a name="update-release-12"></a>Rilascio 12 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

- Tempo e spesa

    - Risolto: la messaggistica degli errori di immissione dell'ora è stata aggiornata con un contesto più pertinente.
    - Risolto: la pianificazione e la griglia di immissione dell'ora visualizzano correttamente la barra di scorrimento verticale quando richiesto.
    - Risolto: Gli inserimenti ore e spese inviati possono essere approvati.
    - Risolto: il messaggio di annullamento della finestra di dialogo di conferma dell'approvazione è stato corretto per riflettere lo stato dell'approvazione quando cambia da **Approvato** in **Inviato**.
    - Risolto: i campi **Prezzo** , **Unità** e **Quantità** sono ora bloccati sul record Spese dopo che è stato approvato.

- Gestione progetti

    - Risolto: l'azione **Nuovo** nel modulo principale **Membro del team** è stata rimossa.
    - Risolto: le assegnazioni delle risorse sono state aggiornate per tenere conto degli errori di arrotondamento non accurati, che portano a uno spostamento nella data di fine di un'attività.
    - Risolto: nella griglia delle attività, all'utente vengono visualizzati errori sul lato server.
    - Risolto: il nome del membro del team ora viene visualizzato nel selettore di persone dell'attività anziché nel nome della posizione.

- Gestione risorse

    - Risolto: i dettagli sui requisiti delle risorse per i progetti creati da un modello ora utilizzano il calendario del progetto.
    - Risolto: le abilità e le competenze ora vengono automaticamente impostate dai dati master del ruolo nel requisito della risorsa creato per quel ruolo.

- Sales

    - Risolto: ID oggetto duplicato trovato nel modulo **Contratto principale**.
    - Risolto: la logica è stata aggiornata per rendere la scheda **Analisi offerta** visibile in modo da visualizzare l'impostazione dei metadati della scheda.
    - Risolto: la data contabile sul record effettivo ora proviene dalla data di registrazione ora/spesa e non dalla data dell'approvazione.
