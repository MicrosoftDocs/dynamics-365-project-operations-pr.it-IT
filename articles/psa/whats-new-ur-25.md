---
title: Novità o modifiche nella versione di aggiornamento 25 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 25 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280448"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novità o modifiche nella versione di aggiornamento 25 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per Project Service Automation V3, rilascio di aggiornamento 25 Questa versione ha un numero di build di V 3.10.43.76 ed è generalmente disponibile tramite l'aggiornamento automatico di ottobre 2020.

## <a name="update-release-25"></a>Rilascio 25 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Ore e spesa**

Il problema seguente è stato risolto:

- Grafico di inserimenti ore che mostra dati aggiuntivi basati su un intervallo troppo grande per essere recuperato.

**Gestione risorse**

Il problema seguente è stato risolto:

- Aggiunto il codice del Package Deployer per saltare l'importazione della patch Universal Resource Scheduling se esiste già una patch di versione successiva.

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- Corretti arrotondamenti e discrepanze nei tassi di cambio con conseguente costo pianificato errato nella griglia di tracciabilità del progetto.
- Supporta la possibilità di visualizzare due o più griglie di reazione sul modulo **Progetto**.
- Convalida fornita per la possibilità di assegnare un'attività oltre la data di fine del calendario, che si traduce in un'assegnazione di risorse non riuscita.
- Gestione degli errori migliorata per la risoluzione dell'eccezione di riferimento nullo generata da:

    - Plug-in **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** quando un'attività di progetto viene creata senza un progetto associato
    - Plug-in **PreProjectTeamMemberCreate**
    - Plug-in **PostProjectTeamMemberDelete**
    - Plug-in **PreValidateProjectTaskDelete**

**Sales**

Sono stati risolti i seguenti problemi:

- Gestione degli errori migliorata per risolvere le eccezioni di riferimento nullo generate da **Copia progetto: gestione stime HelperResource**.
- **Non pronto per la fatturazione** in un **Backlog di fatturazione tempo e materiale** non cancella lo stato di fatturazione.
- Corretto l'errore di etichettatura dei pulsanti **Prezzi** nella scheda **Prezzo ruolo** e **Articoli di catalogo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]