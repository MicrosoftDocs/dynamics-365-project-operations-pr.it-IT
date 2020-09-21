---
title: Home page delle dimensioni di determinazione di prezzi e costi
description: In questo argomento viene fornita una panoramica delle dimensioni di determinazione dei prezzi.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752627"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Home page delle dimensioni di determinazione di prezzi e costi

Le dimensioni utilizzate nelle risorse umane per impostare prezzi e costi rientrano in due categorie:

- Persone
- Lavoro pianificato

Di conseguenza, in Project Service Automation (PSA) sono disponibili due tipi di valori per le dimensioni di determinazione dei prezzi: 

- **Set di opzioni** - Dimensioni che sono enumerazioni fisse per un set di valori.
- **Valori basati su entità** - Dimensioni che possono essere un set di valori differenti.

## <a name="pricing-dimensions"></a>Dimensioni di determinazione dei prezzi

PSA include un set predefinito di dimensioni di determinazione dei prezzi. Puoi visualizzare queste dimensioni selezionando **Project Service** > **Parametri**. Nel record del parametro, nella scheda **Dimensione di determinazione dei prezzi basata su importo**, verifica che i campi **Vendite applicabili a** e **Costo applicabile a** del ruolo **msdyn_resourcecategory** e dell'unità organizzativa di gestione risorse **msdyn_organizationalunit** siano impostati su **Sì**. Ciò ti consentirà di impostare il prezzo e il costo di ogni combinazione di unità organizzativa e ruolo.

![Screenshot dei parametri di Project Service con il campo "Vendite applicabili a" evidenziato](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Se hai utilizzato i campi predefiniti di ruolo e unità organizzativa come dimensioni di determinazione dei prezzi prima della versione 3 di PSA, non vi sono differenze. Puoi continuare a utilizzare Project Service come di consueto. 

Se devi determinare il prezzo o il costo delle risorse utilizzando ulteriori attributi, puoi creare entità, dimensioni e campi personalizzati. Per ulteriori informazioni, vedi gli argomenti seguenti, ma nota che devi completare le procedure nell'ordine indicato di seguito:

- [Creare campi ed entità personalizzati](create-custom-fields-entities.md)
- [Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali](field-references.md)
- [Impostare campi personalizzati come dimensioni di determinazione dei prezzi](set-up-pricing-dimensions.md)
- [Aggiornare attributi di plug-in per includere nuove dimensioni di determinazione dei prezzi](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Determinare il prezzo del tempo delle risorse umane
Il modo in cui un'organizzazione determina il prezzo del tempo delle risorse umane è spesso un fattore strategico importante che influenza direttamente la redditività dell'organizzazione. Collabora con i team finanziari e i responsabili delle procedure quando l'organizzazione è pronta per identificare il modo in cui configurare tassi di fatturazione e di costo per il tempo delle risorse umane.

Altre considerazioni per la determinazione dei prezzi includono se riutilizzare campi o entità che non sono al momento dimensioni di determinazione dei prezzi, ma che vengono applicate come tali per l'organizzazione. I campi come **Categoria di transazione** (**msdyn_transactioncategory**) e **Risorsa prenotabile** (**bookableresource**) sono esempi di possibili dimensioni. 

Devi inoltre considerare se la dimensione di determinazione dei prezzi deve essere una tabella o un set di opzioni. Se prevedi modifiche ai valori di una dimensione superiori a 10 o 12 e necessiti di ulteriori attributi per questi valori, puoi creare un'entità anziché un set di opzioni. La gestione di un set di opzioni, ad esempio l'aggiunta o la rimozione di valori, richiede un amministratore o uno sviluppatore mentre l'aggiunta di nuove righe a una tabella può essere eseguita dalla maggior parte degli utenti.

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
