---
title: Novità o modifiche nella versione di aggiornamento 45 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 45 di Microsoft Dynamics 365 Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169158"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Novità o modifiche nella versione di aggiornamento 45 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 45 di Project Service Automation V3. Questa versione ha il numero di build V3.10.76.168 ed è generalmente disponibile tramite un aggiornamento automatico di luglio 2022.

## <a name="update-release-45"></a>Rilascio 45 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**Vendite**

- Gli utenti non possono creare fatture correttamente dopo aver tentato di creare una fattura senza vendite non fatturate, se visualizzano anche la stessa istanza della pagina e non la aggiornano.

**Ore e spesa**

- Quando Approvazioni moderne è abilitata e viene approvata un'approvazione di progetto richiamata, la fase di registrazione viene aggiornata in modo non corretto a **Richiesta di richiamo approvata**.
- Quando Approvazioni moderne è abilitata e Flussi cloud è inattiva, il processo di approvazione non va a buon fine e gli utenti che eseguono l'invio o l'approvazione non vengono informati.
