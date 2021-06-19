---
title: Creare modelli previsionali per i budget di progetto
description: Questo argomento descrive come creare un modello di previsione per i budget residuo.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006292"
---
# <a name="create-forecast-models-for-project-budgets"></a>Creare modelli previsionali per i budget di progetto 

[!include [banner](../includes/banner.md)]

Questo argomento descrive come creare un modello di previsione per i budget residuo. Un progetto soggetto al controllo di budget utilizza due tipi di budget: originale e rimanente. Quando crei un budget di progetto, devi specificare i modelli di previsione di budget originale e rimanente creati nella pagina **Modelli previsionali**. I budget di progetto basati sui modelli specificati vengono creati quando si impegna il budget di progetto.

> [!NOTE]
> Un modello di previsione utilizzato per il controllo di budget non può avere un sottomodello o essere utilizzato come sottomodello.

1. Seleziona **Gestione progetti e contabilità** > **Impostazione** > **Previsioni**  > **Modelli previsionali**.
2. Seleziona **Nuovo** per creare un nuovo modello previsionale, quindi immetti un numero ID modello e un nome per il nuovo modello. 
3. Imposta l'opzione **Interrotto** su **Sì** per impedire qualsiasi modifica alle righe di previsione per il modello previsionale. 
4. Se le righe di previsione a cui è associato il modello devono generare previsioni di flusso di cassa nella contabilità generale, imposta **Includi in previsioni del flusso di cassa** su **Sì.** 
5. Per utilizzare la data del progetto come data della fattura, imposta **Data fattura prevista** su **Sì**. 
6. Nel campo **Tipo di budget** seleziona uno dei tipi di modello indicati di seguito:

   - **Budget originale**: utilizza gli importi di budget originale impegnati quando il budget iniziale viene creato e approvato.
   - **Budget residuo**: utilizza gli importi di budget residuo durante la durata del progetto. I saldi in questo modello di previsione vengono ridotti dalle transazioni effettive e aumentati o diminuiti dalle revisioni di budget.
   - **Riporto in avanti**: utilizzare gli importi di budget da riportare in avanti per il progetto. Il riporto in avanti è un processo opzionale che può essere eseguito per trasferire importi di budget non utilizzati da un anno fiscale a un altro.

7. Imposta le opzioni seguenti come necessario:

   - Abilita **Data fattura prevista** per utilizzare la data del progetto come data della fattura.
   - Abilita **Previsione con WIP** per prevedere in base al lavoro in corso (WIP), quindi seleziona il tipo di WIP. 
   - Puoi mantenere l'impostazione predefinita del **Tipo di budget** come **Nessuno** o inserire un nuovo tipo. Il tipo di budget non può essere modificato dopo aver modificato un record.     
    > [!NOTE]
    > Se modifichi il tipo di budget predefinito, tutte le altre opzioni non saranno disponibili per gli aggiornamenti e non potrai riutilizzare questo modello di previsione. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]