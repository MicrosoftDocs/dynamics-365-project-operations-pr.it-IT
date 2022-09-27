---
title: Novità o modifiche nella versione di aggiornamento 47 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 47 di Microsoft Dynamics 365 Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477235"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Novità o modifiche nella versione di aggiornamento 47 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 45 di Project Service Automation V3. Questa versione ha il numero di build V3.10.78.8 ed è generalmente disponibile tramite un aggiornamento automatico di luglio 2022.

## <a name="update-release-47"></a>Rilascio 47 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**Gestione risorse**
- È stata aggiornata una convalida per garantire che gli utenti non possano attivare un'eccezione di riferimento null quando tentano di creare un membro del team di progetto senza una **risorsa prenotabile**.
