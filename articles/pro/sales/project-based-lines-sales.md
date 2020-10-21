---
title: Righe di opportunità basate su progetto (Pro)
description: In questo argomento vengono fornite informazioni sulle righe di opportunità basate su progetto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896376"
---
# <a name="project-based-opportunity-lines-pro"></a>Righe di opportunità basate su progetto (Pro)

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le righe di opportunità basate su progetto sono disponibili solo nelle opportunità basate su progetto. I record di opportunità basate su progetto hanno il valore del campo **Tipo** impostato su **Basato sul lavoro**.

Le righe di opportunità basate su progetto sono le voci che verranno consegnate al cliente utilizzando un progetto. Tuttavia, un progetto non può essere collegato a una riga di opportunità basata su progetto. I progetti possono essere collegati alle voci dalla fase **Offerta** in poi perché in genere l'opportunità si trova in una fase iniziale del ciclo di vita di una transazione. La determinazione del numero di progetti che verranno utilizzati per consegnare il lavoro al cliente è una decisione che viene presa successivamente nella fase di vendita. È possibile utilizzare la fase di opportunità per identificare i componenti di consegna discreti per il cliente. Le decisioni relative al numero effettivo di progetti utilizzati per fornire questi componenti possono essere rimandate fino a quando non si conoscono maggiori informazioni sul lavoro stesso.

Di seguito sono riportati i campi in una riga di opportunità basata su progetto:

| **Campo** | **Luogo** | **Pertinenza, scopo e indicazioni** | **Impatto downstream** |
| --- | --- | --- | --- |
| Tipo di prodotto | Scheda Generale (nascosta) | Puoi selezionare una delle opzioni seguenti:</br>- Servizio basato sul progetto (disponibile solo quando è installato Dynamics 365 Project Operations)</br>- Prodotto (disponibile solo quando sono installati Project Operations e Dynamics 365 Sales) | Il valore di questo campo è impostato su **Servizio basato sul progetto** quando si crea una riga di opportunità basata su progetto dalla griglia delle righe basate su progetto nell'opportunità. <br> Se modifichi o sostituisci questo valore, la funzionalità del progetto non sarà abilitata sulle voci basate su progetto. |
| Opportunità | Scheda Generale | Questo campo è di sola lettura e fa riferimento al record di opportunità padre a cui appartiene questa voce. | Non vi è alcun impatto downstream da questo campo. |
| Nome | Scheda Generale | Questo campo di testo modificabile può essere utilizzato per assegnare una breve identità alla voce. | Questo valore viene riportato nella riga dell'offerta quando si crea un'offerta da questa opportunità. |
| Budget cliente | Scheda Generale | Questo campo di valuta modificabile può essere utilizzato per tenere traccia dell'importo che il cliente è disposto a spendere per questa voce. | Questo valore viene riportato nel campo corrispondente della riga dell'offerta quando si crea un'offerta da questa opportunità. |
| Metodo di fatturazione | Scheda Generale | Di seguito sono riportati i valori possibili di questo campo modificabile:</br>- Tempistica e materiali</br>- Prezzo fisso | Questo valore viene riportato nel campo corrispondente della riga dell'offerta quando si crea un'offerta da questa opportunità. Dopo aver creato la riga dell'offerta, il campo è bloccato e non può essere modificato. Assegna un valore a questo campo nel modo più accurato possibile. Se è necessario modificare il valore di questo campo nella riga dell'offerta, elimina e ricrea la riga dell'offerta. |
