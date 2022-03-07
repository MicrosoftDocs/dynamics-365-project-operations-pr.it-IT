---
title: Novità o modifiche nella versione di aggiornamento 21 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 21 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002332"
---
# <a name="project-service-automation-update-release-21-v3"></a>Versione di aggiornamento di Project Service Automation 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 21 di Project Service Automation V3. Questa versione ha il numero di build V 3.10.32.50 ed è generalmente disponibile tramite un aggiornamento automatico a giugno 2020.

## <a name="update-release-21"></a>Rilascio 21 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Tempo e spesa**

Sono stati risolti i seguenti problemi:

- Quando si ospita il **controllo Griglia inserimento ore** nei dashboard, la griglia non utilizza l'intera larghezza del contenitore della griglia del dashboard.
- Per fusi orari specifici, il controllo della griglia **inserimento ore** non visualizza i record.
- Gli inserimenti ore successivi alle 21:00 vengono visualizzati nel giorno sbagliato.
- Gli utenti non possono inviare le spese se la categoria di spesa, **Ricevuta spesa obbligatoria** non ha valore.

**Gestione risorse**

Sono stati risolti i seguenti problemi:

- Le prenotazioni inattive vengono visualizzate nella visualizzazione **Riconciliazione**.
- Nell'evasione di risorse generiche manca la convalida per garantire la presenza di uno stato di prenotazione valido.

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- Le griglie del modulo **Progetto** (**Assegnazione risorse**, **Attività**, visualizzazione **Riconciliazione**, **Stime di spesa**) rimangono modificabili anche quando un progetto non è attivo.
- I clienti duplicati non possono essere uniti a clienti collegati a contratti di progetto confermati.
- Quando viene aggiunta una risorsa che non dispone di un calendario valido, il sistema non restituisce un messaggio di errore descrittivo.
- Il pulsante **Aggiungi attività** sulla griglia delle attività è abilitato quando il progetto è collegato al **componente aggiuntivo Microsoft Project**.
- L'impegno cresce in modo incontrollabile quando un'attività con una categoria viene assegnata a una risorsa con un ruolo per il quale è stato definito un prezzo di costo.

**Sales**

Sono stati apportati i seguenti miglioramenti:

- **Frequenza di fatturazione** e **Inizio fatturazione** sono stati spostati nella scheda **Pianificazione fatturazione**.

Sono stati risolti i seguenti problemi:

- **Prezzo di vendita totale** è zero (0) per **Categoria** nonostante **Ruolo** abbia un prezzo di vendita totale diverso da zero.
- I clienti non possono modificare il valore del campo **Stato fattura** in **Pronto per la fatturazione** quando un altro processo personalizzato aggiorna un campo aggiuntivo.
- Il pulsante **Aggiorna righe fattura** può creare più righe duplicate se viene selezionato ripetutamente.
- Il pulsante **Aggiorna prezzi** non funziona nella griglia secondaria **Prezzi ruolo** del modulo di **visualizzazione rapida**.
- La logica **Risoluzione listino prezzi di vendita** gestisce in modo inaccurato i fusi orari, determinando una selezione errata dei listini prezzi.
- Il **costo effettivo totale** di un progetto può essere disattivato di un importo in frazione dopo l'approvazione di una singola voce.
- La logica **Risoluzione prezzi** non fornisce un messaggio di errore descrittivo se **RolePrice recuperato** non ha valori nei campi **"Unità primaria"** e **"Prezzo in unità primaria"**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]