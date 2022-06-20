---
title: Novità o modifiche nella versione di aggiornamento 43 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 43 di Microsoft Dynamics 365 Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915327"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Novità o modifiche nella versione di aggiornamento 43 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 43 di Project Service Automation V3. Questa versione ha il numero di build V3.10.74.200 ed è generalmente disponibile tramite un aggiornamento automatico a maggio 2022.

## <a name="update-release-43"></a>Rilascio 43 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.


**Ore e spesa**

- Quando si importanogli inserimenti ore da prenotazioni o assegnazioni di risorse, il riferimento alla relativa risorsa prenotabile non viene mantenuto.
- Quando la griglia di inserimenti ore viene espansa a schermo intero, la navigazione nella griglia con il tasto Tab non funziona.
- Quando si invia un inserimento ore creato da un altro utente, il campo **Inviato da** è compilato in modo errato con l'utente che ha creato il foglio presenze.
