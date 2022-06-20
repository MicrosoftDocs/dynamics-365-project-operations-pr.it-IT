---
title: Prenotazioni e assegnazioni
description: In questo articolo vengono fornite informazioni sulle differenze tra prenotazioni di risorse e assegnazioni di risorse.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918593"
---
# <a name="bookings-vs-assignments"></a>Prenotazioni e assegnazioni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le prenotazioni sono l'allocazione provvisoria o definitiva delle risorse a un progetto. Le prenotazioni definitive consumano la capacità di una risorsa. Le prenotazioni rappresentano concetti organizzativi per i team per capire in che modo le risorse saranno impegnate nei vari progetti. Dynamics 365 Project Operations considera le prenotazioni un concetto a livello di progetto. 

Diversamente dalle prenotazioni, le assegnazioni sono l'impegno delle risorse per le attività di progetto nella pianificazione di progetto. Le risorse possono essere denominate o generiche.  Quando un requisito di risorsa viene ricavato dalle assegnazioni di attività del progetto, Project Operations utilizza i profili di lavoro dell'assegnazione delle risorse per creare i profili dei dettagli di requisito di risorsa. Tuttavia, un riferimento alle assegnazioni di risorse non viene mantenuto. Gli aggiornamenti alle prenotazioni ricavate dal requisito di risorsa non aggiornano le assegnazioni delle risorse.

In genere, la somma delle prenotazioni per una risorsa sarà uguale alla somma delle assegnazioni della risorsa in una o più attività. Tuttavia, in Project Operations questa concordanza non è obbligatoria. La vista **Riconciliazione** mostra a un responsabile di progetto dove prenotazioni e assegnazioni non corrispondono.




[!INCLUDE[footer-include](../includes/footer-banner.md)]