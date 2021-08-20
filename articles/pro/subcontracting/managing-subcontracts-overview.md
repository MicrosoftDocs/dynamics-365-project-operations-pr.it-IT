---
title: Gestione dei conti lavoro in Project Operations
description: Questo argomento fornisce una panoramica del processo di gestione end-to-end dei conti lavoro in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994236"
---
# <a name="subcontract-management-in-project-operations"></a>Gestione dei conti lavoro in Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Conti lavoro in Microsoft Dynamics 365 Project Operations supporta il seguente flusso del processo aziendale.

![Flusso del processo dei conti lavoro](../media/SubcontractingProcessFlow.png)

Di seguito è riportata una descrizione dettagliata del processo di conti lavoro.

1. Il project manager crea un conto lavoro con un fornitore. Per impostazione predefinita, per il conto lavoro vengono utilizzati i listini prezzi associati al record del fornitore. Il conto fornitore ha un tipo di relazione di tipo **fornitore** o **venditore**.
2. Il project manager può dettagliare tutti gli acquisti come voci nel conto lavoro. Le righe del conto lavoro possono riguardare tempi, spese o prodotti. La classe di transazione selezionata su ogni riga di conto lavoro determina a cosa serve la riga.
3. L'account manager del fornitore e il project manager possono eseguire iterazioni sul conto lavoro. È possibile apportare modifiche ai prezzi nei listini prezzi di acquisto associati al conto lavoro.
4. A questo punto o in una fase successiva del processo, se la riga di conto lavoro è per il tempo, l'account manager del fornitore associa i contatti a ciascuna riga di conto lavoro. Questa associazione fornisce informazioni al project manager che sta lavorando sul conto lavoro. Quando un contatto è associato a una riga di conto lavoro, il sistema crea automaticamente una risorsa prenotabile dal contatto, se non esiste già una risorsa prenotabile.
5. Il metodo di fatturazione su ciascuna riga di subappalto può essere di tipo **prezzo fisso** o **tempo e materiale**. Per le righe di conto lavoro a prezzo fisso, è possibile impostare una pianificazione fattura basata su passaggi fondamentali.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
