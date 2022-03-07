---
title: Personale di un progetto con lavoratori a contratto e capacità in conto lavoro
description: Questo argomento spiega come gestire i requisiti del progetto utilizzando lavoratori a contratto o capacità in conto lavoro in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902889"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Personale di un progetto con lavoratori a contratto e capacità in conto lavoro

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

I membri generici del team di progetto possono essere impiegati con dipendenti o lavoratori a contratto. Quando si assegna personale a un progetto con lavoratori a contratto, è possibile limitare le opzioni di personale a lavoratori a contratto specifici assegnati a una riga di conto lavoro. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Ricerca dei requisiti di risorse del personale con lavoratori a contratto che appartengono a una specifica riga di conto lavoro

Per cercare i requisiti di risorse del personale con lavoratori a contratto che appartengono a una specifica riga di conto lavoro, segui questi passaggi:

1. Crea un membro del team di progetto generico che faccia riferimento a una riga di conto lavoro e a un conto lavoro.
2. Genera un requisito di risorsa per questo membro del team di progetto generico utilizzando il pulsante **Genera requisito** nella griglia secondaria dei membri del team di progetto.
3. Seleziona la riga del membro del team e quindi seleziona il pulsante **Prenota** sulla griglia secondaria. 
4. Questo apre la scheda di pianificazione con il contesto dei requisiti. Come per altri attributi quali date, ruolo e campi dell'unità organizzativa, anche i filtri della scheda di pianificazione vengono compilati automaticamente con i campi della riga del fornitore, del conto lavoro e della riga di conto lavoro dal requisito di risorsa.
5. Il sistema cerca le risorse che soddisfano i criteri di filtro e le elenca. 
6. Seleziona una delle risorse filtrate e prenota la risorsa per il requisito. 
7. Viene creato un membro del team di progetto generico e aggiornato con i riferimenti alla riga di conto lavoro e al conto lavoro. Vai a **Stime progetto** e seleziona **Aggiorna prezzi** per visualizzare il costo aggiornato dell'assegnazione della risorsa. 

> [!NOTE]
> L'aggiornamento del membro del team di progetto con un riferimento di riga di conto lavoro e di conto lavoro potrebbe non essere sempre possibile durante la prenotazione se la risorsa è assegnata a più righe di conto lavoro. Se il sistema non è in grado di aggiornare il membro del team di progetto con un conto lavoro e una riga di conto lavoro, apri il record del membro del team di progetto e aggiorna manualmente questi campi in modo che la stima del costo finanziario rifletta accuratamente il costo del conto lavoro.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Ricerca e requisiti di risorse del personale con qualsiasi lavoratore a contratto

Per cercare i requisiti di risorse del personale con qualsiasi lavoratore a contratto, segui questi passaggi:

1. Crea un membro del team di progetto generico.
2. Genera un requisito di risorsa per questo membro del team di progetto generico utilizzando il pulsante **Genera requisito** nella griglia secondaria dei membri del team di progetto.
3. Seleziona la riga del membro del team e quindi seleziona il pulsante **Prenota** sulla griglia secondaria. 
4. Questo apre la scheda di pianificazione con il contesto dei requisiti. Come per altri attributi quali date, ruolo e campi dell'unità organizzativa, anche i filtri della scheda di pianificazione vengono compilati automaticamente con i campi della riga del fornitore, del conto lavoro e della riga di conto lavoro dal requisito di risorsa. Poiché per il requisito non sono stati inseriti valori di riga di conto lavoro o di conto lavoro, questi attributi saranno vuoti nel riquadro dei filtri.
5. Il sistema cerca le risorse che soddisfano i criteri di filtro e le elenca.
6. Aggiorna il campo **Tipo di lavoratore** nella casella di filtro su **Lavoratore a contratto** per limitare la ricerca ai lavoratori a contratto. Aggiorna **Fornitore** nel riquadro del filtro per selezionare un fornitore per limitare la ricerca in modo da mostrare solo i lavoratori a contratto che appartengono a una società fornitore specifica.
7. Seleziona un lavoratore a contratto dall'elenco e prenota la risorsa per il requisito.
8. Viene creato un membro del team di progetto. Tuttavia, il membro del team di progetto non viene aggiornato con alcuna riga di conto lavoro o alcun conto lavoro e pertanto l'assegnazione delle risorse non verrà calcolata utilizzando il prezzo del conto lavoro. Aggiorna manualmente il membro del team di progetto con una riga di conto lavoro e vai a **Stime progetto** e seleziona **Aggiorna prezzi** per visualizzare il costo aggiornato dell'assegnazione della risorsa.

> [!NOTE]
> I membri del team di progetto che hanno **Tipo di lavoratore** come **Lavoratore a contratto** ma non hanno un riferimento di conto lavoro sono contrassegnati come **Non valido** nella griglia **Membri del team di progetto**. Se sono presenti membri del team di progetto con questo stato, apri il record dei membri del team di progetto e aggiorna manualmente i campi della riga di conto lavoro e del conto lavoro in modo che la stima del costo finanziario rifletta accuratamente il costo del terzista nella scheda **Stime**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
