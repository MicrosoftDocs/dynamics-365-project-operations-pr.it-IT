---
title: Novità o modifiche nella versione di aggiornamento 39 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nell'aggiornamento versione Microsoft Dynamics 365 Project Service Automation 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588741"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Novità o modifiche nella versione di aggiornamento 39 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 39 di Project Service Automation V3. Questa versione ha il numero di build V3.10.60.170 ed è generalmente disponibile tramite un aggiornamento automatico in gennaio 2022.

## <a name="update-release-39"></a>Rilascio 39 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**GeneralE**

- Sono stati apportati diversi miglioramenti alla mappa del sito per la traduzione araba.

**Gestione progetti**

- Si verifica un errore quando si cambia il project manager di un progetto in un utente che è già un membro del team nel progetto.

**Vendite**

- Il proprietario del **Listino prezzi contratto di progetto** non è corretto quando il listino prezzi viene creato automaticamente. 
- La validità della data di un listino prezzi non viene rispettata quando il listino prezzi viene applicato al parametro del progetto.
- L'unità contratto potrebbe non avere il valore predefinito corretto durante la modifica di due preventivi separati.
