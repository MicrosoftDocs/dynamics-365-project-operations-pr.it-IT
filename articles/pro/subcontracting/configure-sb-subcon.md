---
title: Configurare la scheda di pianificazione per mostrare i lavoratori a contratto e la capacità in conto lavoro
description: Questo argomento descrive come configurare la scheda di pianificazione in Microsoft Dynamics 365 Project Operations per mostrare la capacità delle risorse in conto lavoro durante l'assegnazione del personale ai requisiti delle risorse del progetto.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903451"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurare la scheda di pianificazione per mostrare i lavoratori a contratto e la capacità in conto lavoro 

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

La scheda di pianificazione in Microsoft Dynamics 365 Project Operations può essere utilizzata per la ricerca di risorse in due modi:

- Ricerca generale delle risorse senza il contesto di alcun requisito di risorse specifico basato sul progetto.
- Ricerca di risorse specifiche dei requisiti in cui il requisito del progetto fornirà il contesto per le risorse suggerite.

Per informare la scheda di pianificazione della capacità delle risorse in conto lavoro e dei lavoratori a contratto, è necessario aggiornare le impostazioni della scheda di pianificazione. Questi aggiornamenti includono: 
- Aggiornamento delle impostazioni della scheda di pianificazione per la ricerca generale delle risorse.
- Aggiornamento delle impostazioni della scheda di pianificazione per la ricerca delle risorse in base a requisiti.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Aggiornamento delle impostazioni della scheda di pianificazione per la ricerca generale delle risorse
### <a name="update-filters-for-general-resource-search"></a>Aggiornamento dei filtri per la ricerca generale delle risorse
Quando cerchi una risorsa, i filtri disponibili nella scheda di pianificazione devono essere aggiornati in modo da poter cercare anche risorse esterne specificando uno o tutti i seguenti elementi:
  - Tipo di lavoratore, se le risorse mostrate devono essere lavoratori a contratto o dipendenti.
  - Società fornitore a cui appartiene una risorsa.
  - Risorse che appartengono a una riga di conto lavoro o un conto lavoro specifici.
    
### <a name="update-retrieve-resource-query"></a>Aggiornamento della query recupera risorse
Anche la query utilizzata per la ricerca deve essere aggiornata per utilizzare questi attributi di filtro aggiuntivi. Utilizza i passaggi seguenti per aggiornare la configurazione della scheda di pianificazione per la ricerca generale delle risorse:  
1. Apri **Impostazioni della scheda di pianificazione** per una specifica scheda di pianificazione.
2. Apri la scheda **Impostazioni generali** e scorri fino ad **Altre impostazioni**.
3. Nell'elenco delle impostazioni in questa sezione, aggiorna **Layout filtro** su **Layout di filtro predefinito per Project Operations semplice**.
4. Aggiorna **Query Recupera risorse** su **Query Recupera risorse predefinita per Project Operations semplice**.

![Aggiornamento delle impostazioni della scheda di pianificazione per la ricerca generale delle risorse](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Aggiornamento delle impostazioni della scheda di pianificazione per la ricerca delle risorse in base a requisiti
### <a name="update-filters-for-requirement-specific-resource-search"></a>Aggiornamento dei filtri per la ricerca delle risorse in base a requisiti 
Quando cerchi una risorsa, i filtri disponibili nella scheda di pianificazione devono essere aggiornati in modo da poter cercare anche risorse esterne specificando uno o tutti i seguenti elementi:
 - Tipo di lavoratore, se le risorse mostrate devono essere lavoratori a contratto o dipendenti.
 - Società fornitore a cui appartiene una risorsa.
 - Risorse che appartengono a una riga di conto lavoro o un conto lavoro specifici.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Aggiornamento della query recupera risorse per la ricerca di risorse in base a requisiti 
Anche la query utilizzata per la ricerca deve essere aggiornata per utilizzare questi attributi di filtro aggiuntivi. Utilizza i passaggi seguenti per aggiornare la configurazione della scheda di pianificazione per la ricerca delle risorse in base a requisiti:

1. Apri **Impostazioni della scheda di pianificazione** per una scheda di pianificazione specifica e quindi seleziona **Apri impostazioni predefinite** per aprire le impostazioni per la ricerca in base ai requisiti.
2. Apri la scheda **Impostazioni generali** e scorri fino ad **Altre impostazioni**.
3. Nell'elenco delle impostazioni in questa sezione, aggiorna **Layout filtro** su **Layout di filtro predefinito per Project Operations semplice**.
4. Aggiorna **Query Recupera risorse** su **Query Recupera risorse predefinita per Project Operations semplice**.
5. Apri la scheda **Tipi di pianificazione** e vai a **Progetto**.
6. Sotto le impostazioni per **Progetto**, aggiorna **Query Recupera risorse di Assistente di pianificazione** su **Query Recupera risorse predefinita per Project Operations semplice** e aggiorna **Query Recupera vincoli di Assistente di pianificazione** su **Query Recupera vincoli predefinita per Project Operations semplice**.

![Aggiornamento delle impostazioni della scheda di pianificazione per la ricerca delle risorse in base a requisiti](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
