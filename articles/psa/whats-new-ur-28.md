---
title: Novità o modifiche nella versione di aggiornamento 28 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 28 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930599"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novità o modifiche nella versione di aggiornamento 28 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate per Project Service Automation V3, versione di aggiornamento 28 Questa versione ha il numero di build V3.10.46.32 ed è generalmente disponibile tramite un aggiornamento automatico a gennaio 2021.

## <a name="update-release-28"></a>Rilascio 28 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Ore e spesa**

Sono stati risolti i seguenti problemi:

- Gli utenti possono utilizzare **Modifica in blocco** per aggiornare gli inserimenti ore che sono stati approvati e inviati.

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- Nei casi in cui il GUID dell'attività viene interpretato come un numero, le attività non possono essere aperte per la modifica utilizzando **Modifica attività** nella barra multifunzione nella pagina **Struttura di suddivisione del lavoro**.

**Sales**

Sono stati risolti i seguenti problemi:

- Viene generata un'eccezione di riferimento null quando il plug-in **GetEstimatesForProject** viene richiamato.
- **Contrassegna come pronto per la fatturazione** sulla griglia passaggi fondamentali aggiorna solo parzialmente gli attributi, ad eccezione dell'attributo **InvoiceStatus** che viene aggiornato.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
