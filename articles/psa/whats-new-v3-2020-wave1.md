---
title: Novità o modifiche nella prima ondata 2020 di Project Service Automation versione 3.x
description: Questo argomento fornisce informazioni sulle novità e sulle modifiche nella prima ondata 2020 di Project Service Automation versione 3.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
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
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078822"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novità o modifiche nella prima ondata 2020 di Project Service Automation versione 3
In questo argomento sono presenti considerazioni importanti sull'aggiornamento quando si passa all'ultima versione della prima ondata 2020 di Project Service Automation (PSA) versione 3.x.

## <a name="time-entry"></a>Inserimento ore
L'esperienza di inserimento ore è stata estesa per offrire le funzionalità per l'estensione dell'inserimento ore in più scenari di clienti. Ciò include la possibilità di aggiungere tipi di voci che ora guidano comportamenti specifici in base al nome dello schema del campo **Impostazioni di inserimento ore** , visualizzato come **Origine dell'ora**. Una nuova soluzione, denominata Time, Expense, Statusing and Approvals (TESA) è stata aggiunta per supportare questa funzionalità.

### <a name="upgrade-consideration"></a>Considerazioni sull'aggiornamento
Per supportare questa funzionalità, i ruoli all'interno di PSA sono stati aggiornati per includere nuovi privilegi. Questi privilegi concedono l'accesso in lettura alla nuova entità, **Impostazioni di inserimento ore**.

Agli utenti che richiedono la possibilità di registrare l'ora deve essere concesso il ruolo utente **Utente con inserimento ore** oltre ai ruoli esistenti. Questo ruolo include le nuove funzionalità e garantisce che l'inserimento ore continui a funzionare.

Inoltre, se si dispone di moduli di app personalizzati che includono tutti i moduli per l'entità di inserimento ore, dovrai rimuovere il modulo **Modulo di creazione rapida inserimento ore TESA** dal modulo.

### <a name="currently-extended-time-entry-changes"></a>Modifiche di inserimento ore attualmente esteso
Per ridurre al minimo l'impatto per gli utenti attuali dell'inserimento ore, questo cambio di ruolo è l'unico requisito fondamentale necessario per continuare a utilizzare l'inserimento ore. Se sono state create visualizzazioni personalizzate o esperienze di inserimento ore separate, è necessario impostare i campi **Impostazioni di inserimento ore** con il valore di PSA corretto.