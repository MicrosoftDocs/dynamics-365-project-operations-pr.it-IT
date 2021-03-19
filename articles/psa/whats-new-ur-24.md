---
title: Novità o modifiche nella versione di aggiornamento 24 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 24 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c789a65f1996d082410b3d8dd9e76e5065e708a2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280493"
---
# <a name="project-service-automation-update-release-24-v3"></a>Versione di aggiornamento di Project Service Automation 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 24 di Project Service Automation V3. Questa versione ha il numero di build V 3.10.42.43 ed è generalmente disponibile tramite un aggiornamento automatico in ottobre 2020

## <a name="update-release-24"></a>Rilascio 24 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Sales**

Sono stati risolti i seguenti problemi:

- Problema durante l'impostazione del listino prezzi predefinito dei prodotti.
- Le prestazioni della conclusione dell'offerta sono lente a causa del listino prezzi incorporato e della copia dei record dei prezzi del ruolo.
- **Contratto di progetto/Hub di vendita** > **Voce prodotto/Quantità riga ordine** viene automaticamente arrotondato al numero intero più vicino.
- Eleva i privilegi di sistema durante la lettura dei listini prezzi.
- Copia i campi dell'indirizzo del cliente **address1_freighttermscode** e **address1_shippingmethodcode** per Offerta/Ordine. 


**Tempo e spesa**

Sono stati risolti i seguenti problemi:

- La **Griglia di inserimento ore** non supporta il comportamento dell'ora **Solo data**.
- **Inserimento ore** non si aggiorna automaticamente. È richiesto un aggiornamento manuale.
- Impossibile importare gli inserimenti ore da un'assegnazione quando c'è un'interruzione (0 ore) nelle assegnazioni di una risorsa.
- Quando si crea un inserimento ore, imposta l'inizio come **msdyn_date**.
- Riabilita la modifica di massa per l'inserimento ore.

**Gestione risorse**

Sono stati risolti i seguenti problemi:

- Il tentativo di aggiornare lo stato di una prenotazione giornaliera senza un requisito genera un'eccezione null-ref.
- Errore durante il caricamento della **Visualizzazione riconciliazione**.


**Gestione progetti**

Sono stati risolti i seguenti problemi:

- In **Pianificazione di progetti**, quando si passa da **Manuale** ad **Automatico**, il salvataggio automatico non viene completato.
- I costi di spesa non devono essere calcolati per la varianza nella **Griglia di registrazione di progetto**.
- Comportamento incoerente per le colonne **Tag delle stime** durante il caricamento rispetto alla modifica del tipo **Scala cronologica**.
- Il costo effettivo di un progetto potrebbe non riflettere i totali di **Valori effettivi**.
- **Data di fine prevista** nella scheda **Riepilogo** non corrisponde a **Pianificazione WBS**.
- **Aggiorna ore effettive** su rientro negativo non funziona correttamente.
- Un project manager esterno alla **BU** radice non può creare un progetto.
- Le modifiche all'attività o alla categoria in **Stime di spesa** non sono persistenti.
- **Copia del contratto** copia le pianificazioni fatture e lo stato di esecuzione.
- Il pulsante **Aggiorna valori effettivi** calcola in modo errato le attività di riepilogo.
- Componente aggiuntivo Microsoft Project: corregge l'errore di riferimento nullo se un membro del team dispone di un'unità di di gestione risorse vuota.



[!INCLUDE[footer-include](../includes/footer-banner.md)]