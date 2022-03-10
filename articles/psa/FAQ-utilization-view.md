---
title: Visualizzare l‘utilizzo addebitabile per le risorse
description: In questo argomento vengono fornite informazioni sulla vista utilizzo risorse.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 32dba5acd95c1d192556153240ebd51343112be53aa3db93e5e6f127c2d960e9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007151"
---
# <a name="view-chargeable-utilization-for-resources"></a>Visualizzare l‘utilizzo addebitabile per le risorse

[!include [banner](../includes/psa-now-project-operations.md)]
 
La **vista utilizzo** nella pagina **Utilizzo risorse di Project Service** mostra l'utilizzo addebitabile per ogni risorsa prenotabile. Poiché la vista è basata sulla scheda di pianificazione, include molte delle funzionalità di quella scheda.

> ![Vista Utilizzo.](media/FAQ-utilization-1.png)
 

Il calcolo dell'utilizzo addebitabile viene eseguito in questo modo:

   Utilizzo addebitabile = (ore effettive addebitabili)/(capacità della risorsa).

Le celle rappresentano l'utilizzo addebitabile calcolato per il periodo selezionato (giorni, settimane, o mesi).

I colori in ogni cella mostrano l'utilizzo addebitabile per una risorsa rispetto al relativo utilizzo addebitabile di destinazione. 

L'utilizzo di destinazione può essere impostato nel ruolo predefinito della risorsa o nella singola risorsa stessa. Il calcolo considera dapprima la persona per la destinazione e quindi il ruolo predefinito della risorsa.

## <a name="set-target-on-a-resource"></a>Impostare la destinazione in una risorsa

1. Seleziona **Risorse** \> **Risorse**. 
2. Selezionare una risorsa per aprire il record. 
3. Nella scheda **Project Service**, è possibile impostare l'utilizzo di destinazione della risorsa.

> ![Utilizzo della scheda Project Service per impostare l'utilizzo di destinazione.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Impostare l'utilizzo di destinazione in un ruolo

1. Selezionare **Risorse** \> **Ruoli risorsa**. 
2. Selezionare un ruolo e aprire il record. 
3. Impostare l'utilizzo di destinazione per il ruolo.

> ![Utilizzo di Ruoli risorsa per impostare l'utilizzo di destinazione.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Calcolare un utilizzo addebitabile per una risorsa

Per calcolare l'utilizzo addebitabile per una risorsa, è necessario completare alcuni prerequisiti. 

### <a name="set-default-role-for-individual-resource"></a>Impostare il ruolo predefinito per una singola risorsa

Innanzi tutto, l'utilizzo di destinazione deve essere impostato sulla singola risorsa o sui ruoli risorsa. Se si utilizzano i ruoli delle risorse per le destinazioni, ogni singola risorsa deve avere un ruolo predefinito. 

1. A questo proposito, selezionare **Risorse** \> **Risorse**. 
2. Selezionare una risorsa, aprire il record e quindi selezionare la scheda **Project Service**. 
3. Nella griglia **Ruolo risorsa**, assicurarsi che è presente un ruolo per la risorsa e che **Predefinito** è impostato su **Sì**.
 
### <a name="change-billing-type-for-resource-role"></a>Modificare il tipo di fatturazione per il ruolo risorsa

I ruoli risorsa devono essere impostati per avere un tipo di fatturazione **Addebitabile**. 

1. Selezionare **Risorse** \> **Ruoli risorsa**. 
2. Aprire il record che si intende aggiornare e quindi impostare il tipo di fatturazione predefinito su **Addebitabile**.

### <a name="set-working-hours-for-resource-role"></a>Impostare le ore lavorative per il ruolo risorsa
 
La risorsa deve avere delle ore lavorative per il calcolo della capacità. 

1. Seleziona **Risorse** \> **Risorse**. 
2. Selezionare una risorsa per aprire il record, quindi selezionare **Mostra ore lavorative**. 
3. È possibile aggiornare in blocco l'elenco delle risorse applicando un **modello di ore lavorative** dalla vista **Elenco risorse**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Risoluzione dei problemi relativi alle ore effettive addebitabili

Le ore effettive addebitabili provengono dall'entità **Valori effettivi**. I valori effettivi con un tipo di fatturazione **Addebitabile** sono inclusi nel calcolo e per questo motivo è necessario avere progetti dove i valori effettivi sono addebitabili.

Se non si sta visualizzando l'utilizzo addebitabile, di seguito sono elencati alcuni punti da verificare:

- La risorsa ha ore lavorative definite per la capacità.
- La risorsa ha una destinazione di utilizzo definita singolarmente o un ruolo predefinito. Il ruolo ha una destinazione di utilizzo.
- I valori effettivi hanno un tipo di fatturazione **Addebitabile** per il periodo per cui si prevede un calcolo dell'utilizzo. Verificare quanto segue se sono visualizzati valori effettivi con tipi di fatturazione differenti da Addebitabile:

  - Il ruolo utilizzato per il valore effettivo ha un tipo di fatturazione predefinito differente da Addebitabile.
  - Il ruolo nella voce di contratto di progetto che supporta il progetto è stato impostato come non addebitabile.
  - Il progetto non ha una voce di contratto associata.



[!INCLUDE[footer-include](../includes/footer-banner.md)]