---
title: Novità o modifiche nella versione di aggiornamento 14 di Project Service Automation V3
description: Questo argomento fornisce informazioni sulle novità dell'aggiornamento rilascio 14 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124823"
---
# <a name="project-service-automation-update-release-14-v3"></a>Versione di aggiornamento di Project Service Automation 14, V3
Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Dynamics 365 Project Service Automation (PSA). Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per aggiornare a questa versione, visitare l'interfaccia di amministrazione di Dynamics 365 online e andare alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 14 di PSA V3. Questa versione ha il numero di build V3.10.4.21 ed è disponibile secondo la seguente pianificazione:

- **Disponibilità generale (aggiornamento automatico):** gennaio 2020
- **Aggiornamento automatico:** febbraio 2020

## <a name="update-release-14"></a>Rilascio 14 dell'aggiornamento

### <a name="enhancements"></a>Miglioramenti

- Sales

     - I valori personalizzati del campo **Dettagli riga di offerta** vengono copiati in **Dettagli riga contratto di progetto** quando un'offerta viene aggiornata **come acquisita**.
     - I progetti confermati possono essere **chiusi come persi**.

- Gestione risorse

     - Quando si estendono le prenotazioni, verrà visualizzata una finestra di dialogo per la conferma degli utenti con il riepilogo dei risultati della prenotazione e fornire un collegamento a Gestisci prenotazioni.


### <a name="bug-fixes"></a>Correzioni di bug

- Tempo e spesa

     - Risolto: migliorata l'esperienza dell'utente quando l'utente non seleziona alcuna voce da correggere.

- Gestione risorse

     - Risolto: la prenotazione di una risorsa più volte crea l'overflow del nome della risorsa prenotabile.

- Sales

     - Risolto: il prezzo di vendita totale non viene calcolato fino a quando l'utente non inserisce anche un prezzo di costo per le stime di spesa in un progetto.
     - Risolto: la chiusura di un'offerta come **acquisita** non riesce se il contratto di progetto associato non è in stato di **Bozza**.

