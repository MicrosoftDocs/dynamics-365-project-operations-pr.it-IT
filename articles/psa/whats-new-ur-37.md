---
title: Novità o modifiche nella versione di aggiornamento 37 di Project Service Automation V3
description: Questo articolo elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 37 di Microsoft Dynamics 365 Project Service Automation V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922503"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novità o modifiche nella versione di aggiornamento 37 di Project Service Automation V3

[!include [banner](../includes/psa-now-project-operations.md)]

Siamo lieti di annunciare l'ultimo aggiornamento dell'app Microsoft Dynamics 365 Project Service Automation. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. È compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita la pagina delle soluzioni online dell'interfaccia di amministrazione per Dynamics 365 e installa l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](/power-platform/admin/install-remove-preferred-solution).

Questo articolo elenca le funzionalità e le correzioni nuove o modificate nella versione di aggiornamento 37 di Project Service Automation V3. Questa versione ha un numero di build V3.10.58.120 ed è generalmente disponibile tramite un aggiornamento automatico di novembre 2021.

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
