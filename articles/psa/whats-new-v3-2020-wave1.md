---
title: Novità o modifiche nella prima ondata 2020 di Project Service Automation versione 3.x
description: In questo articolo vengono fornite informazioni su novità e modifiche nel primo ciclo 2020 di Project Service Automation versione 3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c762f2e7931046d32464cfa8486ef8405aa7d836
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928621"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novità o modifiche nella prima ondata 2020 di Project Service Automation versione 3

[!include [banner](../includes/psa-now-project-operations.md)]

L'articolo evidenzia le considerazioni chiave sull'aggiornamento quando si passa all'ultima versione del primo ciclo 2020 di Project Service Automation (PSA) versione 3.x.

## <a name="time-entry"></a>Inserimento ore
L'esperienza di inserimento ore è stata estesa per offrire le funzionalità per l'estensione dell'inserimento ore in più scenari di clienti. Ciò include la possibilità di aggiungere tipi di voci che ora guidano comportamenti specifici in base al nome dello schema del campo **Impostazioni di inserimento ore**, visualizzato come **Origine dell'ora**. Una nuova soluzione, denominata Time, Expense, Statusing and Approvals (TESA) è stata aggiunta per supportare questa funzionalità.

### <a name="upgrade-consideration"></a>Considerazioni sull'aggiornamento
Per supportare questa funzionalità, i ruoli all'interno di PSA sono stati aggiornati per includere nuovi privilegi. Questi privilegi concedono l'accesso in lettura alla nuova entità, **Impostazioni di inserimento ore**.

Agli utenti che richiedono la possibilità di registrare l'ora deve essere concesso il ruolo utente **Utente con inserimento ore** oltre ai ruoli esistenti. Questo ruolo include le nuove funzionalità e garantisce che l'inserimento ore continui a funzionare.

Inoltre, se si dispone di moduli di app personalizzati che includono tutti i moduli per l'entità di inserimento ore, dovrai rimuovere il modulo **Modulo di creazione rapida inserimento ore TESA** dal modulo.

### <a name="currently-extended-time-entry-changes"></a>Modifiche di inserimento ore attualmente esteso
Per ridurre al minimo l'impatto per gli utenti attuali dell'inserimento ore, questo cambio di ruolo è l'unico requisito fondamentale necessario per continuare a utilizzare l'inserimento ore. Se sono state create visualizzazioni personalizzate o esperienze di inserimento ore separate, è necessario impostare i campi **Impostazioni di inserimento ore** con il valore di PSA corretto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
