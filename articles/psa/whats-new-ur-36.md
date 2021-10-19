---
title: Novità o modifiche nella versione di aggiornamento 36 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nell'aggiornamento versione Microsoft Dynamics 365 Project Service Automation 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606776"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novità o modifiche nella versione di aggiornamento 36 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 36 di Project Service Automation V3. Questa versione ha il numero di build V3.10.57.152 ed è generalmente disponibile tramite un aggiornamento automatico in ottobre 2021.

## <a name="update-release-36"></a>Rilascio 36 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**GeneralE**
- Il nome del campo **Modello orario di lavoro predefinito** è tradotto in modo errato nella pagina **Parametri progetto**.
- I plug-in asincroni non gestiscono correttamente le eccezioni relative a **SharedVariableService**.

**Ore e spesa**
- Quando mancano righe del giornale di registrazione o l'utente non dispone dei privilegi corretti per leggere le righe del giornale di registrazione, si verifica un errore errato quando le approvazioni del progetto vengono annullate.
- Gli utenti non possono annullare un'approvazione quando una voce di spesa o di tempo ha più di un'approvazione di progetto associata.
- **Assenza** e **Ferie** sono tradotti in modo errato per la lingua cinese in una ricerca sulla pagina di creazione rapida **Inserimento ore**.

**Gestione delle risorse**
- L'utente non può cercare risorse in **Assistente di pianificazione** quando la modalità di visualizzazione è impostata su **Giorno**, **Settimana** o **Mese**.
- Le risorse generiche possono erroneamente avere nomi di posizione vuoti. 
- La chiusura di un contratto come perso non annulla le prenotazioni future.

**Vendite**
- Quando un ambiente ha un grande volume di prodotti, le prestazioni diminuiscono nella griglia **Stima dei materiali**.
- Quando si crea un progetto da un modello, la valuta del progetto non è predefinita per l'unità di contrattazione del rispettivo responsabile di progetto.
- Gli importi effettivi non sempre corrispondono a ciò che si riflette sul progetto dovuto oppure gli importi diventano negativi in specifici scenari di richiamo.
- Si verifica un errore quando si associa un progetto creato dal modello di progetto a una riga di contratto.
- Gli utenti possono eliminare una riga di contratto con i passaggi fondamentali, **Pronto per la fatturazione** e **Fattura creata**. Questo non dovrebbe essere permesso.
- Quando le stime vengono importate da un progetto, l'addebito dei dettagli riga di offerta è impostato in modo errato quando la fatturazione basata sull'attività è abilitata per la riga di preventivo.
- Quando aggiungi un traguardo di fatturazione a prezzo fisso, il traguardo non si riflette nella griglia secondaria del traguardo finché la pagina non viene aggiornata.
- Un'eccezione di riferimento null viene generata quando si crea un contratto di progetto con un nome di preventivo nullo.
- Le attività in modalità manuale in cui la valuta del progetto è diversa dalla valuta della risorsa generano stime dei prezzi errate.
- Gli utenti non possono richiamare una transazione che è stata corretta correttamente da una fattura correttiva.
- Le categorie di transazione disattivate vengono visualizzate nella griglia **Stime di spesa**.



