---
title: Novità o modifiche nella versione di aggiornamento 38 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 38 di Microsoft Dynamics 365 Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915190"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novità o modifiche nella versione di aggiornamento 38 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 38 di Project Service Automation V3. Questa versione ha un numero di build di V3.10.59.117 ed è generalmente disponibile tramite un aggiornamento automatico a dicembre 2021.

## <a name="update-release-38"></a>Rilascio 38 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**Ore e spesa**

- Si verifica un'eccezione quando la lunghezza dei registri dei set di approvazioni supera i 100.000 record.
- Gli utenti non possono accedere alla griglia **Inserimento ore** dalla pagina principale **Inserimento ore**.
- La finestra di dialogo **Importazione inserimento ore** non mostra alcun testo quando nessun elemento è idoneo per l'importazione.
- Gli utenti possono creare set di approvazioni in cui il campo **Stato destinazione** è impostato su **Sconosciuto**.

**Gestione progetti**

- I profili di distribuzione non vengono visualizzati correttamente nelle assegnazioni di risorse per UTC(+09:30) e UTC(+10:00) all'inizio dell'ora legale.
- Il campo **Colonna aggiuntiva** per le strutture di suddivisione del lavoro è nascosto in alcune impostazioni internazionali.
- Il selettore della data per il controllo del calendario nella griglia **Attività progetto** non è localizzata correttamente per il cinese.

**Vendite**

- I valori **Prestazioni contratto** e **Costo effettivo progetto** non corrispondono quando le risorse prenotabili con unità contratto e valute diverse inviano inserimenti ore.
- Un flusso di lavoro personalizzato per confermare automaticamente le fatture non riesce quando le fatture vengono importate come soluzione gestita. Viene visualizzato il seguente messaggio: "Messaggio Microsoft.Xrm.Sdk.InvalidPluginExecutionException: stato fattura non valido".
- Quando **Radice** viene selezionato come opzione di riepilogo e il progetto dispone di stime da una combinazione di classi di transazioni (ad esempio, una combinazione di stime di tempo, spese e materiali), il sistema riepiloga le classi di transazione come un'unica riga di commissione.
- Negli scenari in cui viene aggiunta una riga di spesa prima che una riga di contratto sia associata a un progetto, il prezzo corretto non viene inserito come valore predefinito nel campo **Aggiorna prezzo**.
- Non sono consentiti importi di vendita negativi nelle entità **Progetto** e **Attività**.
