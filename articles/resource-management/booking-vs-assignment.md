---
title: Prenotazioni e assegnazioni
description: Questo argomento fornisce informazioni sulle differenze tra le prenotazioni delle risorse e le assegnazioni delle risorse.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012771"
---
# <a name="bookings-vs-assignments"></a>Prenotazioni e assegnazioni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le prenotazioni sono l'allocazione provvisoria o definitiva delle risorse a un progetto. Le prenotazioni definitive consumano la capacità di una risorsa. Le prenotazioni rappresentano concetti organizzativi per i team per capire in che modo le risorse saranno impegnate nei vari progetti. Dynamics 365 Project Operations considera le prenotazioni un concetto a livello di progetto. 

Diversamente dalle prenotazioni, le assegnazioni sono l'impegno delle risorse per le attività di progetto nella pianificazione di progetto. Le risorse possono essere denominate o generiche.  Quando un requisito di risorsa viene ricavato dalle assegnazioni di attività del progetto, Project Operations utilizza i profili di lavoro dell'assegnazione delle risorse per creare i profili dei dettagli di requisito di risorsa. Tuttavia, un riferimento alle assegnazioni di risorse non viene mantenuto. Gli aggiornamenti alle prenotazioni ricavate dal requisito di risorsa non aggiornano le assegnazioni delle risorse.

In genere, la somma delle prenotazioni per una risorsa sarà uguale alla somma delle assegnazioni della risorsa in una o più attività. Tuttavia, in Project Operations questa concordanza non è obbligatoria. La vista **Riconciliazione** mostra a un responsabile di progetto dove prenotazioni e assegnazioni non corrispondono.




[!INCLUDE[footer-include](../includes/footer-banner.md)]