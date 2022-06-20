---
title: Novità o modifiche nella versione di aggiornamento 13 di Project Service Automation V3
description: In questo articolo vengono fornite informazioni su novità nella versione di aggiornamento 13 di Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f4898391922f5ecbc99d78e49358ea749fe27b3f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930691"
---
# <a name="project-service-automation-update-release-13-v3"></a>Versione di aggiornamento di Project Service Automation 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Dynamics 365 Project Service Automation (PSA). Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per aggiornare a questa versione, visitare l'interfaccia di amministrazione di Dynamics 365 online e andare alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 13 di Project Service Automation V3. Questa versione ha il numero di build V3.10.3.18 ed è disponibile secondo la seguente pianificazione:

- **Disponibilità generale (aggiornamento automatico):** novembre 2019
- **Aggiornamento automatico:** dicembre 2019


## <a name="update-release-13"></a>Rilascio 13 dell'aggiornamento 

### <a name="bug-fixes"></a>Correzioni di bug

- Tempo e spesa

     - Risolto: la funzionalità di ricerca nella pagina **Approvazione delle spese** non funziona durante la ricerca per scopo della spesa.

- Gestione risorse

     - Risolto: i numeri nella riconciliazione sono stati aggiornati per essere giustificati correttamente.
     - Risolto: le risorse denominate non possono essere assegnate alle attività tramite la scheda **Pianifica**.

- Gestione progetti

     - Risolto: l'eccezione di riferimento null durante l'assegnazione del membro del team quando in **TransactionType** mancano le informazioni di impostazione per **Unità** e **DefaultGroup**.

- Sales

     - Risolto: i record duplicati del tipo di transazione restituiscono un errore quando vengono creati i record del prezzo del ruolo.
     - Risolto: pulsanti aggiuntivi per **Nuova opportunità**, **Offerta**, **Riga ordine** e **Aggiungi prodotto** sono visibili nei comandi per Opportunità, Offerte, Prodotti ordine e nella griglia secondaria Righe basate su progetto.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
