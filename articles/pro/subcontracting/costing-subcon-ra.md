---
title: Stima dei costi delle assegnazioni di risorse in conto lavoro
description: Questo articolo spiega come Microsoft Dynamics 365 Project Operations calcola la stima dei costi delle assegnazioni di risorse in conto lavoro.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 40603c1d2dfdd49909d9a4bf5085f43201e8f6bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932347"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Stima dei costi delle assegnazioni di risorse in conto lavoro

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le assegnazioni delle attività dei membri del team di progetto in conto lavoro vengono calcolate utilizzando il listino prezzi **Acquisto** allegato al conto lavoro nel relativo record del membro del team. Questo è diverso dal modo in cui vengono calcolate le assegnazioni delle risorse dei dipendenti per cui le assegnazioni delle attività delle risorse dei dipendenti vengono calcolate utilizzando il listino prezzi **Costo** allegato all'unità contratto del progetto. 

Per i membri generici del team di progetto in conto lavoro, le assegnazioni vengono valutate utilizzando un'impostazione del prezzo basata sui ruoli nel listino prezzi di acquisto allegato al conto lavoro. I prezzi di acquisto possono anche essere impostati in modo specifico per ciascuna risorsa. A questi prezzi specifici delle risorse verrà data la priorità quando le assegnazioni di attività di costo dei membri del team di progetto nominati sono lavoratori a contratto. 

La priorità dell'utilizzo del prezzo di acquisto specifico del ruolo rispetto a quello specifico della risorsa è determinata dall'impostazione della priorità della dimensione del prezzo in **Parametri > Dimensione di determinazione dei prezzi basata su importo**.

Questa funzionalità di derivazione dinamica dei prezzi in base all'impostazione della dimensione per i prezzi di acquisto dei terzisti è simile alla modalità di derivazione dei costi e delle tariffe per i dipendenti a tempo pieno. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Creazione di assegnazioni di attività per ottenere stime dei costi delle risorse del terzista

Le assegnazioni di attività per i terzisti possono essere create in due modi: 
- Usando la scheda **Attività**.
- Usando la scheda **Team**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Creazione di assegnazioni di risorse utilizzando la scheda Attività
Usando l'elenco **Risorse** nella scheda **Attività** per un'attività specifica, puoi creare un'assegnazione di attività per una risorsa denominata o una risorsa generica. Se selezioni una risorsa denominata dall'elenco a discesa **Risorse assegnate** dell'attività e questa risorsa è un lavoratore a contratto, la risorsa denominata viene assegnata all'attività e viene creato un record del membro del team di progetto corrispondente con il tipo di lavoratore impostato su **Lavoratore a contratto** e **Validità** impostato su **Non valido**. Come passaggio successivo, sarà necessario aprire il record del membro del team di progetto e selezionare un conto lavoro e una riga di conto lavoro. Ciò aggiornerà l'assegnazione dell'attività per avere un riferimento alla riga di conto lavoro e al conto lavoro e aggiornerà anche lo stato del membro del team su **Valido**.

Se scegli di creare un membro del team generico dall'elenco a discesa **Risorse assegnate** dell'attività, la finestra di dialogo **Creazione generica di membri del team** consente di selezionare un conto lavoro e una riga di conto lavoro. Quando la risorsa generica viene assegnata all'attività e viene creato il record del membro del team di progetto corrispondente, puoi notare che il record del membro del team di progetto viene creato con il tipo di lavoratore impostato su **Lavoratore a contratto** e **Validità** impostato su **Valido**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Creazione di membri del team di progetto utilizzando la scheda Team
Utilizzando la scheda Team nel progetto, puoi creare un membro del team generico o denominato. Quando si crea il membro del team, è possibile selezionare il conto lavoro e la riga di conto lavoro. Dopo che il membro del team è stato creato, dovrai assegnare il membro del team a un'attività utilizzando l'elenco a discesa **Risorse assegnate** dell'attività. 

## <a name="updating-estimates"></a>Aggiornamento delle stime
Dopo aver assegnato i membri del team di progetto alle attività, dovrai accedere alla scheda **Stime** nel progetto e selezionare **Aggiorna prezzi** per garantire che le tariffe di costo delle assegnazioni delle risorse del terzista vengano aggiornate in base al listino prezzi di acquisto allegato al conto lavoro. Le stime non vengono generate per le attività non assegnate in Microsoft Dynamics 365 Project Operations. Di conseguenza, dovrai creare assegnazioni di attività per valutare le varie attività nel progetto. 

> [NOTA!] I membri del team di progetto che hanno **Tipo di lavoratore** come **Lavoratore a contratto** ma non hanno un riferimento di conto lavoro sono contrassegnati come **Non valido** nella griglia **Membri del team di progetto**. Se sono presenti membri del team di progetto con questo stato, apri il record dei membri del team di progetto e aggiorna manualmente i campi della riga di conto lavoro e del conto lavoro in modo che la stima del costo finanziario rifletta accuratamente il costo del terzista nella scheda **Stime**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
