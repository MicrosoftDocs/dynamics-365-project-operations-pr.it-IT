---
title: Novità o modifiche nella versione di aggiornamento 35 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nell'aggiornamento versione Microsoft Dynamics 365 Project Service Automation 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473270"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Novità o modifiche nella versione di aggiornamento 35 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 35 di Project Service Automation V3. Questa versione ha il numero di build V3.10.56.110 ed è generalmente disponibile tramite un aggiornamento automatico di settembre 2021.

## <a name="update-release-35"></a>Rilascio 35 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**Ore e spesa**

- Il responsabile dell'approvazione del progetto riceve un errore di privilegio di lettura quando approva le voci di spesa con un ruolo **Responsabile approvazione di progetto**.
- Il responsabile dell'approvazione del progetto riceve un errore di privilegio di scrittura su **msdyn_projectapproval** quando annullano una voce di orario approvato con un ruolo **Responsabile approvazione di progetto**.
- Quando selezioni **Copia settimana** in un inserimento ore nel modulo dell'app Dynamics 365 per telefoni - Hub risorse di progetto, si verifica il seguente errore: "...\OfficeProductivity_RibbonRules.js.map: errore HTTP: codice di stato 404, net:: ERR_HTTP_RESPONSE_CODE_FAILURE."
- I criteri **Riprova** approvano automaticamente le voci che erano state precedentemente rifiutate.
- La griglia secondaria **Set di approvazione** mostra le azioni della barra multifunzione non applicabili.
- Mancano le icone per **Attività di progetto** e **Ruolo risorsa** sull'entità **Inserimento ore**.
- Quando si importano le assegnazioni di risorse, le voci di orario importate non hanno la durata corretta per le assegnazioni create tramite attività in modalità manuale.
- **Elimina** manca nella pagina **Ricerca avanzata per i record inserimento ore**.
- **Salva** manca nella pagina **Informazioni sull'inserimento ore**. Questo problema impedisce il salvataggio delle modifiche alla chiusura della pagina.

**Pianificazione di un progetto**

- Le griglie **Assegnazione risorse** e **Riconciliazione risorse** non ordinano gli attributi raggruppati in ordine alfabetico.
- Le attività non possono essere create se il comportamento della data è personalizzato su **Solo data**.

**Gestione delle risorse**

- Se Dynamics 365 Field Service e Project Service Automation sono installati, si verificano problemi di sovrapposizione quando **Visualizzazione associata requisito di risorsa** è associato a una pagina principale.
- Fai doppio clic su **Salva** nella finestra di dialogo **Creazione rapida: Membro del team di progetto** impedisce la creazione del requisito delle risorse.

**Vendite**

- Viene generata un'eccezione se si elimina un'attività associata a un'offerta con stato **Acquisita**.
