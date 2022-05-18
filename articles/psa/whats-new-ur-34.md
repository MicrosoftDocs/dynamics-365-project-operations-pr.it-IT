---
title: Novità o modifiche nella versione di aggiornamento 34 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 34 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: c7a4feaeebf8fa2ef3447dc6dfc3d0903266f3b2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588695"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novità o modifiche nella versione di aggiornamento 34 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 34 di Project Service Automation V3. Questa versione ha il numero di build V3.10.55.38 ed è generalmente disponibile tramite un aggiornamento automatico di luglio 2021.

## <a name="update-release-34"></a>Rilascio 34 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug
Sono stati risolti i seguenti problemi.

**GeneralE**

- Gli aggiornamenti guidati dall'editore non attivano il nuovo flusso di lavoro di approvazione moderno.
- Gli attributi **Stato di destinazione** e **Tipo di azione** non sono presenti nella pagina principale **Set di approvazioni**.

**Ore e spesa**

- Impossibile approvare una richiesta di richiamo utilizzando il flusso di approvazione moderno.
- La copia di una settimana di inserimenti di ore non funziona quando si copiano voci che non sono correlate all'utente connesso.

**Pianificazione di un progetto**

- I contorni dell'assegnazione delle risorse sono danneggiati durante l'importazione dal componente aggiuntivo desktop di Microsoft Project.

**Gestione delle risorse**

- Quando si pubblica un progetto dal componente aggiuntivo client desktop di Microsoft Project, la data di fine dei requisiti esistenti viene modificata.
- La precisione decimale supera i due decimali nella finestra di dialogo di conferma dell'estensione delle prenotazioni.

**Vendite**

- Quando si aggiunge una riga basata su prodotti con un prodotto esistente a un contratto di progetto, viene visualizzata un'eccezione **chiave non trovata nel dizionario**.
- I lead non possono essere qualificati quando un tipo di ordine viene mappato da un lead a un'opportunità.
