---
title: Configurare l'integrazione della carta di credito
description: Questo argomento spiega come importare e gestire le transazioni con carta di credito relative alle spese.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120863"
---
# <a name="set-up-credit-card-integration"></a>Configurare l'integrazione della carta di credito

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le transazioni con carta di credito relative alle spese possono essere impostate in modo che vengano importate automaticamente in base a una pianificazione ricorrente. In alternativa, le transazioni possono essere importate manualmente in base alle necessità. Le transazioni con carta di credito vengono importate tramite l'entità di dati Transazioni con carta di credito.

## <a name="import-credit-card-transactions"></a>Importare le transazioni con carta di credito

1. Nella pagina **Transazioni con carta di credito** seleziona **Importa transazioni**. Se stai aprendo la gestione dei dati per la prima volta, il sistema deve aggiornare l'elenco delle entità di dati prima di poter continuare.
2. Nella campo **Nome** immetti una descrizione univoca per il processo di importazione.
3. Nel campo **Formato dei dati di origine** seleziona il formato del file che contiene le transazioni della carta di credito da importare.
4. Seleziona **Carica**, quindi trova e seleziona il file da importare.
5. Dopo che il file è stato caricato, convalida la mappatura del file di transazione della carta di credito e le colonne dell'entità di dati delle transazioni della carta di credito selezionando il collegamento **Visualizza mappa** sul riquadro. Se sono presenti errori di mappatura o se è necessario modificare la mappatura, apporta le modifiche alla mappatura dalla scheda **Visualizzazione della mappatura** o dalla scheda **Dettagli della mappatura**.
6. Per automatizzare le transazioni con carta di credito, seleziona **Crea processo dati ricorrente**. Quindi puoi impostare la ricorrenza che definisce la frequenza con cui devono essere importate le transazioni con carta di credito. Al termine, seleziona **OK**.
7. Per importare ora il file selezionato, seleziona **Importa**.
8. Se si verificano errori durante l'importazione, puoi visualizzare il log di esecuzione o i dati di gestione temporanea per vedere gli errori che è necessario correggere per garantire una corretta importazione.

> [!NOTE]
> Se devi importare più di un formato di file, è necessario creare processi di importazione separati per ogni tipo di formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Riassegnare le transazioni con carta di credito per i dipendenti licenziati

Dopo che un record di dipendente viene terminato, l'account Active Directory Domain Services (AD DS) del dipendente viene disabilitato. Tuttavia, potrebbero essere attive transazioni con carta di credito che devono ancora essere spesate e rimborsate. Dalla pagina **Transazioni con carta di credito** puoi riassegnare il dipendente per qualsiasi transazione con carta di credito in cui il dipendente associato è stato licenziato.

Seleziona una o più transazioni con carta di credito, quindi seleziona **Riassegna transazioni**. È quindi possibile selezionare un altro dipendente a cui assegnare le transazioni con carta di credito. Dopo che le transazioni con carta di credito sono state riassegnate, possono essere selezionate per una nota spese e pagate attraverso il normale processo di rimborso della nota spese.
