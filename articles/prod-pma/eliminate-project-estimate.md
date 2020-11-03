---
title: Eliminare una stima di progetto
description: Questo argomento fornisce informazioni sull'eliminazione di una stima di progetto una volta completata.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078929"
---
# <a name="eliminate-a-project-estimate"></a>Eliminare una stima di progetto

[!include [banner](../includes/banner.md)]

Le stime di progetto forniscono una vista finanziaria del il lavoro stimato e pianificato per un progetto. Per utilizzare le stime per un progetto, è necessario collegare il progetto a un progetto di stima. Un progetto di stima si basa sempre su un progetto esistente, tuttavia più progetti possono fare riferimento a un singolo progetto di stima. Ai progetti di stima possono essere collegati solo progetti a prezzo fisso e di investimento e tali progetti devono appartenere allo stesso gruppo di progetti del progetto di stima.

Il progetto di stima deve essere completo per poter essere eliminato. I passaggi seguenti spiegano come eliminare una stima.

1. Vai a **Gestione progetti e contabilità** > **Tutti i progetti** e apri il progetto. 
2. Nella scheda **Gestione** seleziona **Stime** e nella pagina **Stima** seleziona **Elimina**.
3. Nella pagina **Elimina stima** nella scheda **Generale** imposta le seguenti opzioni:

   - **Codice periodo** : Seleziona il codice del periodo per scegliere i progetti di stima appropriati. 
   - **Data di stima** : Seleziona la data di stima appropriata per l'eliminazione.
   - **Elimina con gli avvisi WIP** : Abilita questa opzione per fornire una notifica quando una stima collegata a un lavoro in corso (WIP) verrà eliminata. Quando questa opzione non è abilitata, l'eliminazione non può continuare se esistono transazioni non stimate. 
   > [!NOTE]
   > Questa opzione è disponibile solo quando l'eliminazione viene applicata a un progetto di stima. Non è disponibile se usi le registrazioni periodiche. Questa impostazione funziona con le impostazioni nella scheda **Stima** della pagina **Parametri di progetto** nel gruppo di campi **Consenti eliminazione quando esistono transazioni non stimate**.
   - **Imposta la fase su Finito** : Abilita questa opzione per impostare la fase del progetto di stima su **Finito** dopo aver eseguito l'eliminazione.
   - **Stampa elenco stime** : Seleziona le informazioni da includere quando viene stampato l'elenco delle stime.
   - **Mostra infolog** : Abilita questa opzione per visualizzare l'infolog.
   - **Data registrazione** : Scegli la data di registrazione contabile della stima.

4.  Seleziona **OK**.
5. Una volta completato il processo di eliminazione, il progetto di stima eliminato viene visualizzato con un valore negativo. 

Se non intendevi eliminare una stima, puoi selezionare la stima eliminata e selezionare **Annulla eliminazione**.   
