---
title: Novità o modifiche nella versione di aggiornamento 23 di Project Service Automation V3
description: Questo argomento elenca le funzionalità e le correzioni disponibili nella versione di aggiornamento 23 di Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078823"
---
# <a name="project-service-automation-update-release-23-v3"></a>Versione di aggiornamento di Project Service Automation 23, V3

Siamo lieti di annunciare l'ultimo aggiornamento per l'applicazione Project Service Automation per Dynamics 365. Questa versione include alcuni importanti miglioramenti in termini di qualità, prestazioni e usabilità. Questa versione è compatibile con Dynamics 365 9.x. Per eseguire l'aggiornamento a questa versione, visita l'interfaccia di amministrazione di Dynamics 365 online e vai alla pagina delle soluzioni per installare l'aggiornamento. Per ulteriori informazioni, vedere [Installare, aggiornare o rimuovere una soluzione preferita](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Questo argomento elenca le funzionalità e le correzioni nuove o modificate per l'aggiornamento rilascio 23 di Project Service Automation V3. Questa versione ha il numero di build V 3.10.34.30 ed è generalmente disponibile tramite un aggiornamento automatico in agosto 2020

## <a name="update-release-23"></a>Rilascio 23 dell'aggiornamento

### <a name="bug-fixes"></a>Correzioni di bug

**Tempo e spesa**

Sono stati risolti i seguenti problemi:
- Gestisci il caso limite in **Eliminazione membro del team di progetto** per fornire un'eccezione significativa.
- L'importazione dell'assegnazione risulta in una schermata di rimozione vuota.

**Gestione risorse**

Sono stati risolti i seguenti problemi:

- La **Scheda risorsa griglia di utilizzo delle risorse** mostra dati errati quando la scala temporale è superiore a cinque giorni.
- Quando i clienti creano una risorsa prenotabile, il plug-in non riesce ad aggiungere automaticamente la risorsa a un gruppo Microsoft Office 365.
- La visualizzazione **Riconciliazione** mostra i contorni manuali in modo errato nella visualizzzione **Settimana** o **Mese**.

**Gestione progetti**

Sono stati risolti i seguenti problemi:

- Un numero eccessivo di entità **RetrieveMultiple per usersettings** stanno causando una riduzione delle prestazioni per le approvazioni dei progetti e altre operazioni.
- La ricerca delle risorse della griglia **Pianificazione delle attività** è limitata per mostrare solo fino a cinque membri del team di progetto. 
- La ricerca delle risorse della griglia **Pianificazione delle attività** non filtra le risorse inattive.
- La modalità manuale non funziona come previsto nella struttura di suddivisione del lavoro di pianificazione del progetto.
- La griglia **Pianificazione delle attività** mostra **Categorie di transazioni inattive**.
- La griglia **Assegnazione delle risorse** viene arrotondata in modo errato quando un'attività ha più assegnazioni.
- I valori di arrotondamento sono diversi tra il costo pianificato e il costo effettivo per una singola attività.

**Sales**

Sono stati risolti i seguenti problemi:

- Il doppio clic su **Recupera tutte le categorie di transazioni** crea più righe.