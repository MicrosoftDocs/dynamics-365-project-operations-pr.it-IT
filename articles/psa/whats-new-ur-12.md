---
title: Novità o modifiche nella versione di aggiornamento 12 di Project Service Automation V3
description: In questo articolo vengono fornite informazioni su novità nella versione di aggiornamento 12 di Project Service Automation V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 28539b2e1331c8509e40aaf771f4d88d6f54e022
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922641"
---
# <a name="project-service-automation-update-release-12-v3"></a>Versione di aggiornamento di Project Service Automation 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Dynamics 365 Project Service Automation (PSA). Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per aggiornare a questa versione, visitare l'interfaccia di amministrazione di Dynamics 365 online e andare alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 12 di Project Service Automation V3. Questa versione ha il numero di build V3.10.2.34 ed è generalmente disponibile tramite un aggiornamento automatico in ottobre 2019.

## <a name="update-release-12"></a>Rilascio 12 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

- Tempo e spesa

    - Risolto: la messaggistica degli errori di immissione dell'ora è stata aggiornata con un contesto più pertinente.
    - Risolto: la pianificazione e la griglia di immissione dell'ora visualizzano correttamente la barra di scorrimento verticale quando richiesto.
    - Risolto: Gli inserimenti ore e spese inviati possono essere approvati.
    - Risolto: il messaggio di annullamento della finestra di dialogo di conferma dell'approvazione è stato corretto per riflettere lo stato dell'approvazione quando cambia da **Approvato** in **Inviato**.
    - Risolto: i campi **Prezzo**, **Unità** e **Quantità** sono ora bloccati sul record Spese dopo che è stato approvato.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
