---
title: Novità o modifiche nella versione di aggiornamento 30 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 30 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010431"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novità o modifiche nella versione di aggiornamento 30 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution.md).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 30 di Project Service Automation V3. Questa versione ha il numero di build V3.10.51.61 ed è generalmente disponibile tramite un aggiornamento automatico nell'aprile 2021.

## <a name="update-release-30"></a>Rilascio 30 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Ore e spesa**

Sono stati risolti i seguenti problemi:

- Si verifica un errore quando si crea e si salva un inserimento ore nella pagina **Creazione rapida** se il campo **Ruolo** viene rimosso.
- Il filtro Inserimento ora applica l'operatore di filtro errato.
- I fogli presenze copiati non sono visualizzati automaticamente quando selezioni **Copia settimana** nel controllo dell'inserimento ore.

**Gestione risorse**

Sono stati risolti i seguenti problemi:

- Quando estendi una prenotazione, lo stato di prenotazione assegnato alla prenotazione definitiva non è corretto. L'estensione di una prenotazione rispetta lo stato di prenotazione definito come **Confermato** nei metadati di configurazione della prenotazione.
- Quando non viene specificato uno stato di prenotazione valido, il messaggio di errore non viene localizzato correttamente.

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- I progetti non possono essere creati in una valuta e includere attività correlate in un'altra valuta.

**Vendite**

Sono stati risolti i seguenti problemi:

- Quando un listino prezzi viene copiato, i prezzi non vengono aggiornati.
- La chiusura di un'offerta come acquisita non riesce quando il dettaglio del costo comporta un valore per l'origine.
- Nell'entità **Attività di progetto**, **Costo stimato** è stato rinominato in **Costo pianificato (base)**.
- Quando vengono create o eliminate fatture, viene generata un'eccezione di riferimento nulla.
