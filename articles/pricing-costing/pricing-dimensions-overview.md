---
title: Panoramica delle dimensioni di determinazione dei prezzi
description: Questo argomento fornisce informazioni sulle dimensioni di determinazione dei prezzi in Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 4b3b71c0b64a24f6914c70c4383eee654e7d4947ececaf9b4e6394f45a081a4c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001976"
---
# <a name="pricing-dimensions-overview"></a>Panoramica delle dimensioni di determinazione dei prezzi

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

Le dimensioni utilizzate nelle risorse umane per impostare prezzi e costi rientrano in due categorie:

- Persone
- Lavoro pianificato

Di conseguenza, sono disponibili due tipi di valori per le dimensioni di determinazione dei prezzi:

- **Set di opzioni**: dimensioni che sono enumerazioni fisse per un set di valori.
- **Valori basati su entità**: dimensioni che possono essere un set di valori differenti.

## <a name="pricing-dimensions"></a>Dimensioni di determinazione dei prezzi

Dynamics 365 Project Operations include un set predefinito di dimensioni di determinazione dei prezzi. Puoi visualizzare queste dimensioni di determinazione dei prezzi in **Project Operations** > **Parametri**. Nel record del parametro, nella scheda **Dimensione di determinazione dei prezzi basata su importo**, verifica che i campi **Vendite applicabili a** e **Costo applicabile a** del ruolo **msdyn_resourcecategory** e dell'unità organizzativa di gestione risorse **msdyn_organizationalunit** siano impostati su **Sì**. Con questi campi abilitati puoi impostare il prezzo e il costo di ogni combinazione di unità organizzativa e ruolo.

![Screenshot dei parametri di Project Service con il campo "Vendite applicabili a" evidenziato.](media/PS-OOB-parameters.png)

Se devi determinare il prezzo o il costo delle risorse utilizzando ulteriori attributi, puoi creare entità, dimensioni e campi personalizzati. Per ulteriori informazioni, vedere gli argomenti seguenti. 
  
  > [!NOTE]
  > Le procedure devono essere completate nell'ordine in cui sono elencate.

1. [Creare una soluzione per le dimensioni di determinazione dei prezzi personalizzate](../sales/create-solution-custompd.md)
2. [Creazione di campi ed entità personalizzati](create-custom-fields-entities-pricing-dimensions.md)
3. [Aggiungere campi personalizzati all'impostazione e alle entità transazionali ](add-custom-fields-price-setup-transactional-entities.md)
4. [Configurare campi personalizzati come dimensioni di determinazione dei prezzi ](set-up-custom-fields-pricing-dimensions.md)
5. [Aggiornare attributi di plug-in per includere nuove dimensioni di determinazione dei prezzi](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Determinare il prezzo del tempo delle risorse umane
Il modo in cui un'organizzazione determina il prezzo del tempo delle risorse umane è spesso un fattore strategico importante che influenza direttamente la redditività dell'organizzazione. Collabora con i team finanziari e i responsabili delle procedure quando l'organizzazione è pronta per identificare il modo in cui configurare tassi di fatturazione e di costo per il tempo delle risorse umane.

Altre considerazioni per la determinazione dei prezzi includono se riutilizzare campi o entità che non sono al momento dimensioni di determinazione dei prezzi, ma che vengono applicate come tali per l'organizzazione. I campi come **Categoria di transazione** (**msdyn_transactioncategory**) e **Risorsa prenotabile** (**bookableresource**) sono esempi di possibili dimensioni. 

Considera se la dimensione di determinazione dei prezzi deve essere una tabella o un set di opzioni. Se prevedi modifiche ai valori di una dimensione superiori a 10 o 12 e necessiti di ulteriori attributi per questi valori, puoi creare un'entità anziché un set di opzioni. La gestione di un set di opzioni, ad esempio l'aggiunta o la rimozione di valori, richiede un amministratore o uno sviluppatore mentre l'aggiunta di nuove righe a una tabella può essere eseguita dalla maggior parte degli utenti.

L'esempio seguente presenta tassi di fatturazione configurati in base al ruolo e all'unità organizzativa di gestione risorse a cui la risorsa appartiene. I tassi di costo sono in genere basati sulla fascia tariffaria del dipendente e sull'unità organizzativa a cui appartiene. In questo esempio, le tabelle di tassi di fatturazione e costo saranno simili a quanto segue.

**Tassi di fatturazione di esempio**

| Ruolo        | Unità organizzativa    |Unità      |Prezzo      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Developer   | Contoso (USA)  |Ora | 200|USD     |
| Developer   | Contoso India |Ora|   112|USD     |


**Tassi di costo di esempio**

| Fascia salariale     | Unità organizzativa    |Unità      |Prezzo      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Mia società_Fascia1 | Contoso (USA)  |Ora | 145|USD     |
| Mia società_Fascia2 | Contoso India |Ora|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]