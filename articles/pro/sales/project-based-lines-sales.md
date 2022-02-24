---
title: Righe di opportunità basate su progetto - semplice
description: In questo argomento vengono fornite informazioni sulle righe di opportunità basate su progetto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cac6125abc7269ee95667ae589d5a748b3d4190c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272528"
---
# <a name="project-based-opportunity-lines---lite"></a>Righe di opportunità basate su progetto - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le righe di opportunità basate su progetto sono disponibili solo nelle opportunità basate su progetto. I record di opportunità basate su progetto hanno il valore del campo **Tipo** impostato su **Basato sul lavoro**.

Le righe di opportunità basate su progetto sono le voci che verranno consegnate al cliente utilizzando un progetto. Tuttavia, un progetto non può essere collegato a una riga di opportunità basata su progetto. I progetti possono essere collegati alle voci dalla fase **Offerta** in poi perché in genere l'opportunità si trova in una fase iniziale del ciclo di vita di una transazione. La determinazione del numero di progetti che verranno utilizzati per consegnare il lavoro al cliente è una decisione che viene presa successivamente nella fase di vendita. È possibile utilizzare la fase di opportunità per identificare i componenti di consegna discreti per il cliente. Le decisioni relative al numero effettivo di progetti utilizzati per fornire questi componenti possono essere rimandate fino a quando non si conoscono maggiori informazioni sul lavoro stesso.

Di seguito sono riportati i campi in una riga di opportunità basata su progetto:

| **Campo** | **Luogo** | **Descrizione** | **Impatto downstream** |
| --- | --- | --- | --- |
| Tipo di prodotto | Scheda Generale (nascosta) | Puoi selezionare una delle opzioni seguenti:</br>- Servizio basato su progetto (disponibile solo quando Dynamics 365 Project Operations è installato)</br>- Prodotto (disponibile solo quando sono installati Project Operations e Dynamics 365 Sales) | Il valore di questo campo è impostato su **Servizio basato sul progetto** quando si crea una riga di opportunità basata su progetto dalla griglia delle righe basate su progetto nell'opportunità. <br> Se modifichi o sostituisci questo valore, la funzionalità del progetto non sarà abilitata sulle voci basate su progetto. |
| Opportunità | Scheda Generale | Questo campo è di sola lettura e fa riferimento al record di opportunità padre a cui appartiene questa voce. | Non vi è alcun impatto downstream da questo campo. |
| Nome | Scheda Generale | Questo campo di testo modificabile può essere utilizzato per assegnare una breve identità alla voce. | Questo valore viene riportato nella riga dell'offerta quando si crea un'offerta da questa opportunità. |
| Budget cliente | Scheda Generale | Questo campo di valuta modificabile può essere utilizzato per tenere traccia dell'importo che il cliente è disposto a spendere per questa voce. | Questo valore viene riportato nel campo corrispondente della riga dell'offerta quando si crea un'offerta da questa opportunità. |
| Metodo di fatturazione | Scheda Generale | Di seguito sono riportati i valori possibili di questo campo modificabile:</br>- Tempistica e materiali</br>- Prezzo fisso | Questo valore viene riportato nel campo corrispondente della riga dell'offerta quando si crea un'offerta da questa opportunità. Dopo aver creato la riga dell'offerta, il campo è bloccato e non può essere modificato. Assegna un valore a questo campo nel modo più accurato possibile. Se è necessario modificare il valore di questo campo nella riga dell'offerta, elimina e ricrea la riga dell'offerta. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]