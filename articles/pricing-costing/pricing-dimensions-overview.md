---
title: Panoramica delle dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni sulle dimensioni di determinazione dei prezzi in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898221"
---
# <a name="pricing-dimensions-overview"></a>Panoramica delle dimensioni di determinazione dei prezzi

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le dimensioni utilizzate nelle risorse umane per impostare prezzi e costi rientrano in due categorie:

- Persone
- Lavoro pianificato

Di conseguenza, sono disponibili due tipi di valori per le dimensioni di determinazione dei prezzi:

- **Set di opzioni**: dimensioni che sono enumerazioni fisse per un set di valori.
- **Valori basati su entità**: dimensioni che possono essere un set di valori differenti.

## <a name="pricing-dimensions"></a>Dimensioni di determinazione dei prezzi

Dynamics 365 Project Operations viene fornito con un set predefinito di dimensioni dei prezzi. Puoi visualizzare queste dimensioni di determinazione dei prezzi in **Project Operations** > **Parametri**. Nel record del parametro, nella scheda **Dimensione di determinazione dei prezzi basata su importo**, verifica che i campi **Vendite applicabili a** e **Costo applicabile a** del ruolo **msdyn_resourcecategory** e dell'unità organizzativa di gestione risorse **msdyn_organizationalunit** siano impostati su **Sì**. Con questi campi abilitati puoi impostare il prezzo e il costo di ogni combinazione di unità organizzativa e ruolo.

Se devi determinare il prezzo o il costo delle risorse utilizzando ulteriori attributi, puoi creare entità, dimensioni e campi personalizzati.

## <a name="pricing-human-resource-time"></a>Determinare il prezzo del tempo delle risorse umane
Il modo in cui un'organizzazione determina il prezzo del tempo delle risorse umane è spesso un fattore strategico importante che influenza direttamente la redditività dell'organizzazione. Collabora con i team finanziari e i responsabili delle procedure quando l'organizzazione è pronta per identificare il modo in cui configurare tassi di fatturazione e di costo per il tempo delle risorse umane.

Altre considerazioni per la determinazione dei prezzi includono se riutilizzare campi o entità che non sono al momento dimensioni di determinazione dei prezzi, ma che vengono applicate come tali per l'organizzazione. I campi come **Categoria di transazione** (**msdyn_transactioncategory**) e **Risorsa prenotabile** (**bookableresource**) sono esempi di possibili dimensioni. 

Considera se la dimensione di determinazione dei prezzi deve essere una tabella o un set di opzioni. Se prevedi modifiche ai valori di una dimensione superiori a 10 o 12 e necessiti di ulteriori attributi per questi valori, puoi creare un'entità anziché un set di opzioni. La gestione di un set di opzioni, ad esempio l'aggiunta o la rimozione di valori, richiede un amministratore o uno sviluppatore mentre l'aggiunta di nuove righe a una tabella può essere eseguita dalla maggior parte degli utenti.

L'esempio seguente presenta tassi di fatturazione configurati in base al ruolo e all'unità organizzativa di gestione risorse a cui la risorsa appartiene. I tassi di costo sono in genere basati sulla fascia tariffaria del dipendente e sull'unità organizzativa a cui appartiene. In questo esempio, le tabelle di tassi di fatturazione e costo saranno simili a quanto segue.

**Tassi di fatturazione di esempio**

| Ruolo        | Unità organizzativa    |Unità      |Prezzo      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Sviluppatore   | Contoso US  |Hour | 200|USD     |
| Sviluppatore   | Contoso India |Hour|   112|USD     |


**Tassi di costo di esempio**

| Fascia salariale     | Unità organizzativa    |Unità      |Prezzo      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Mia società_Fascia1 | Contoso US  |Hour | 145|USD     |
| Mia società_Fascia2 | Contoso India |Hour|   67|USD     |
