---
title: Novità o modifiche nella versione di aggiornamento 40 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 40 di Microsoft Dynamics 365 Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912797"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novità o modifiche nella versione di aggiornamento 40 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 40 di Project Service Automation V3. Questa versione ha un numero di build di V3.10.61.61 ed è generalmente disponibile tramite un aggiornamento automatico a febbraio 2022.

## <a name="update-release-40"></a>Rilascio 40 dell'aggiornamento

### <a name="features"></a>Funzionalità
La fase 1 dell'aggiornamento da Project Service Automation a Project Operations - Lite sarà rilasciata a febbraio 2022 a tutti i clienti. Per controllare l'idoneità, vedi [Aggiornamento da Project Service Automation a Project Operations](upgrade-project-operations-non-stocked.md). Se l'applicazione non compare nella tua istanza nell'interfaccia di amministrazione di Power Platform, contatta il supporto e richiedi che la versione sia abilitata per i tuoi ambienti. La tua richiesta deve includere un elenco di ID ambiente in cui la versione deve essere abilitata.

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**Ore e spesa**
- Una voce di nota manca quando un inserimento ore viene rifiutato o annullato. 

**Vendite**

- Quando aggiorni le stime dei costi o delle vendite utilizzando plug-in predefiniti, ti è erroneamente consentito inviare payload JSON che non sono validi al di fuori dell'interfaccia utente.
- Quando aggiorni le righe di offerta utilizzando la visualizzazione rapida, puoi attivare le offerte.
