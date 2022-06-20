---
title: Analisi delle offerte di progetto
description: In questo articolo vengono fornite informazioni sull'analisi delle offerte di progetto.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 9db924c16c5eca17e7962ff1d88b09e581347fa5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919283"
---
# <a name="analysis-of-project-quotes"></a>Analisi delle offerte di progetto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analizza le offerte di progetto per stimare la redditività. Inoltre, analizza l'allineamento dell'offerta alle aspettative dei clienti rispetto alla data di consegna o di completamento e al budget.

## <a name="profitability-analysis"></a>Analisi della redditività

Project Service Automation analizza la redditività utilizzando il margine lordo e il margine lordo rettificato.

- I margini lordi vengono calcolati mediante la formula seguente:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Il margine lordo rettificato viene calcolato mediante la formula seguente:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Se i valori del margine lordo e del margine lordo rettificato differiscono di un margine importante, molto del lavoro nell'offerta viene classificato come non addebitabile.

## <a name="analysis-of-customer-expectations"></a>Analisi delle aspettative dei clienti

È possibile analizzare le offerte e generare grafici per le aspettative dei clienti in relazione a pianificazione e budget se si immettono valori nei campi seguenti:

- Il campo **Data consegna richiesta** nell'intestazione dell'offerta.
- Il campo **Budget cliente** per ogni riga dell'offerta (per le righe basate su progetto e le righe basate su prodotto).

L'analisi delle aspettative dei clienti rispetto alla pianificazione viene eseguita confrontando la data di fine più recente del dettaglio della riga di offerta alla data di consegna richiesta in tutte le righe di offerta nell'offerta.

L'analisi delle aspettative dei clienti rispetto al budget viene eseguita confrontando la somma del totale del budget del cliente all'importo indicato in tutte le righe dell'offerta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
