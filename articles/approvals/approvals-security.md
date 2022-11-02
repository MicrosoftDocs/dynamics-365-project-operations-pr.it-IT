---
title: Sicurezza e approvazioni
description: Questo articolo fornisce informazioni sulla configurazione della sicurezza per l'utilizzo delle approvazioni in Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709402"
---
# <a name="security-and-approvals"></a>Sicurezza e approvazioni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

Microsoft Dynamics 365 Project Operations utilizza due ruoli di sicurezza per consentire l'approvazione di voci di tempo, spese e materiale:

- Responsabile approvazione di progetto
- Amministratore responsabile approvazione di progetto

## <a name="project-approver"></a>Responsabile approvazione di progetto

Devi disporre del ruolo di sicurezza **Responsabile approvazione di progetto** per approvare le voci di tempo, spesa e materiale del progetto. Devi inoltre avere accesso alle entità correlate pertinenti, ad esempio **Progetto**. Tale accesso può essere assegnato da qualcuno che dispone del ruolo **Responsabile di progetto**. Inoltre, devi essere un membro del team del progetto ed essere contrassegnato come responsabile approvazione.

Per approvare voci non di progetto, devi essere il responsabile dell'autore dell'invio.

## <a name="project-approver-admin"></a>Amministratore responsabile approvazione di progetto

> [!NOTE]
> La funzionalità [Set di approvazioni](approval-sets.md) deve essere abilitata per poter utilizzare la funzionalità Amministratore responsabile approvazione di progetto.

Il ruolo di sicurezza **Amministratore responsabile approvazione di progetto** consente agli utenti di ignorare i criteri e consente l'approvazione delle voci in tutti i progetti. L'assegnazione di questo ruolo ignorerà la logica di convalida che richiede l'appartenenza al team e di essere contrassegnato come responsabile approvazione. È necessario avere accesso alle tabelle correlate pertinenti, ad esempio **Project**, tramite i ruoli di sicurezza a te assegnati.

Il contesto utente SYSTEM ignora le convalide come il ruolo di sicurezza Amministratore responsabile approvazione di progetto.
