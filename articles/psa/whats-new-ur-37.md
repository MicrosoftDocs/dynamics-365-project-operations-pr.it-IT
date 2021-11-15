---
title: Novità o modifiche nella versione di aggiornamento 37 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nell'aggiornamento versione Microsoft Dynamics 365 Project Service Automation 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727610"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novità o modifiche nella versione di aggiornamento 37 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 37 di Project Service Automation V3. Questa versione ha un numero di build V3.10.58.120 ed è generalmente disponibile tramite un aggiornamento automatico di novembre 2021.

## <a name="update-release-37"></a>Rilascio 37 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

Sono stati risolti i seguenti problemi.

**Ore e spesa**
- Gli utenti non sono in grado di eliminare un inserimento ore cancellando la cella.
- La visualizzazione **Approvazioni personali non riuscite** contiene solo le approvazioni di progetto con stato **Inviato**.

**Gestione dei progetti**
- Gli utenti ricevono un errore di eccezione di riferimento nullo quando aprono un progetto nel componente aggiuntivo desktop Microsoft se il nome della posizione del membro del team di progetto è vuoto.
- Non c'è il pulsante **Salva** nella pagina **Attività di progetto** e gli utenti non possono salvare le modifiche ai record di attività.
- Gli utenti non possono eliminare un progetto che ha un'attività associata a un'offerta con stato **Acquisita**.

**Vendite**
- Il campo **Valuta** nella pagina **Progetto** viene aggiornato per corrispondere alla valuta del modello applicato.
- Il costo viene calcolato in modo errato sulle attività che hanno più valute.
