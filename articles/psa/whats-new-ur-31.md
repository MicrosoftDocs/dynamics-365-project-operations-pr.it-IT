---
title: Novità o modifiche nella versione di aggiornamento 31 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 31 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 70a8bd381c27c9a3dd3b33c582e5616fad280e95
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586763"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novità o modifiche nella versione di aggiornamento 31 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 31 di Project Service Automation V3. Questa versione ha il numero di build V3.10.52.77 ed è generalmente disponibile tramite un aggiornamento automatico a maggio 2021.

## <a name="update-release-31"></a>Rilascio 31 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Ore e spesa**

Sono stati risolti i seguenti problemi:

- I pulsanti di comando per il controllo dell'inserimento ore nella pagina **Risorsa prenotabile** erano confusi.
- Un'eccezione di riferimento nulla è stata generata in **Project.SetTrackingFields** quando si approva un inserimento ore.

**Gestione risorse**

Sono stati risolti i seguenti problemi:

- **Crea membro del team** non visualizza correttamente l'impostazione dei metadati di configurazione della prenotazione per **Stato Impegnato predefinito della prenotazione**.
- Quando si aggiorna da PSA 1.X a 3.X, il processo di aggiornamento non riesce per **UpgradeResourceRequirements**.


**Vendite**

Sono stati risolti i seguenti problemi:

- Il ricavo effettivo converte gli importi nella valuta di progetto nella griglia di rilevamento.
- L'impostazione predefinita della valuta non è chiara quando si creano righe di giornale di registrazione, righe di preventivo e righe di contratto in scenari in cui la valuta di base di un'organizzazione è diversa dalla valuta di progetto.
- La query **In attesa di convalida del giornale di registrazione** non filtra per progetto.
- Le vendite rimanenti vengono calcolate in modo errato su un progetto.
- Le offerte basate su un contatto non riescono quando vengono create senza un listino prezzi.
- Non viene visualizzata alcuna casella di selezione di elaborazione quando selezioni **Conferma fattura**.
- Non viene visualizzata alcuna casella di selezione di elaborazione quando selezioni **Crea fattura**.
- La chiusura di un'offerta come persa non annulla le prenotazioni.







