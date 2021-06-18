---
title: Creare un modello di ore lavorative
description: Questo argomento descrive come creare un modello delle ore lavorative in Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997201"
---
# <a name="create-a-work-hours-template-project-service"></a>Creare un modello delle ore lavorative (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Per creare e gestire un progetto, è necessario applicare un modello di calendario al progetto. Il modello di calendario definisce i seguenti attributi del progetto:

- Orario lavorative, inclusa l'ora di inizio e di fine
- Giorni lavorativi
- Eccezioni di calendario come giorni non lavorativi

Il modello di calendario applicato a un progetto è una copia del modello di calendario definito nelle impostazioni dell'organizzazione.

> [!NOTE]
> Se modifichi il modello di calendario, tali modifiche non si propagano alle ore lavorative del progetto. Per modificare le ore lavorative del progetto, è necessario applicare un nuovo modello.

Per creare un modello di calendario per la tua organizzazione, ci sono due requisiti chiave:

- Definisci le ore lavorative desiderate del modello utilizzando una risorsa prenotabile nuova o esistente.
- Crea un nuovo modello di calendario e associa il modello alla risorsa prenotabile.

**Definisci le ore lavorative del modello**

1. Seleziona **Risorse** \> **Risorse**.
2. Crea una nuova risorsa a cui fare riferimento nel modello di calendario o seleziona una risorsa esistente.
3. Seleziona la scheda **Ore lavorative** della risorsa e completa le istruzioni in [Impostare le ore lavorative per una risorsa](/dynamics365/field-service/set-work-hours-resource.md) per configurare le regole del calendario.

**Creare un nuovo modello di calendario**

1. Vai a **Impostazioni** \> **Modello di calendario**.
2. Seleziona **Nuovo** e inserisci un nome, una descrizione e una risorsa modello.


> [!NOTE]
> Quando si fa riferimento a una risorsa in un modello di calendario, una copia del calendario della risorsa viene associata al modello di calendario. Se le ore lavorative del modello copiato cambiano, tali modifiche non verranno propagate al modello di calendario.


### <a name="see-also"></a>Vedi anche  
 [Configurare le risorse](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
