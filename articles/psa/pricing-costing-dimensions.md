---
title: Home page delle dimensioni di determinazione di prezzi e costi
description: In questo argomento viene fornita una panoramica delle dimensioni di determinazione dei prezzi.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7dbee508cea074a8c443506d280a1b52eb698202
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593617"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Home page delle dimensioni di determinazione di prezzi e costi

[!include [banner](../includes/psa-now-project-operations.md)]

Le dimensioni utilizzate per impostare i prezzi e i costi della manodopera nelle organizzazioni basate su progetto sono influenzate dai seguenti attributi:

- Persone che svolgono un lavoro simile alla loro esperienza, al ruolo o alla geografia
- Lavoro da eseguire simile alla sua complessità o all'ora del giorno

Data la natura tipica di questi attributi del lavoro e le persone richieste per eseguire il lavoro, ci sono due tipi di valori di dimensione di determinazione dei prezzi disponibili in Project Service Automation: 

- **Set di opzioni**: attributi che sono enumerazioni fisse per un set di valori.
- **Valori basati su entità**: attributi che possono avere una serie variabile di valori che sono finiti ma possono cambiare nel tempo.

## <a name="pricing-dimensions"></a>Dimensioni di determinazione dei prezzi

PSA include un set predefinito di dimensioni di determinazione dei prezzi. Puoi visualizzare queste dimensioni selezionando **Project Service** > **Parametri**. Nel record del parametro, nella scheda **Dimensione di determinazione dei prezzi basata su importo**, verifica che i campi **Vendite applicabili a** e **Costo applicabile a** del ruolo **msdyn_resourcecategory** e dell'unità organizzativa di gestione risorse **msdyn_organizationalunit** siano impostati su **Sì**. Ciò ti consentirà di impostare il prezzo e il costo di ogni combinazione di unità organizzativa e ruolo.

![Screenshot dei parametri di Project Service con il campo "Vendite applicabili a" evidenziato.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Se hai utilizzato i campi predefiniti di ruolo e unità organizzativa come dimensioni di determinazione dei prezzi prima della versione 3 di PSA, non vi sono differenze. Puoi continuare a utilizzare Project Service come di consueto. 

Se devi determinare il prezzo o il costo delle risorse utilizzando ulteriori attributi, puoi creare entità, dimensioni e campi personalizzati. Per ulteriori informazioni, vedi gli argomenti seguenti, ma nota che devi completare le procedure nell'ordine indicato di seguito:

- [Creare campi ed entità personalizzati](create-custom-fields-entities.md)
- [Aggiungere campi personalizzati alla configurazione dei prezzi e ad entità transazionali](field-references.md)
- [Configurare campi personalizzati come dimensioni di determinazione dei prezzi ](set-up-pricing-dimensions.md)
- [Aggiornare attributi di plug-in per includere nuove dimensioni di determinazione dei prezzi](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Determinare il prezzo del tempo delle risorse umane
Il modo in cui un'organizzazione determina il prezzo del tempo delle risorse umane è spesso un fattore strategico importante che influenza direttamente la redditività dell'organizzazione. Collabora con i team finanziari e i responsabili delle procedure quando l'organizzazione è pronta per identificare il modo in cui configurare tassi di fatturazione e di costo per il tempo delle risorse umane.

Altre considerazioni per la determinazione dei prezzi includono se riutilizzare campi o entità che non sono al momento dimensioni di determinazione dei prezzi, ma che vengono applicate come tali per l'organizzazione. I campi come **Categoria di transazione** (**msdyn_transactioncategory**) e **Risorsa prenotabile** (**bookableresource**) sono esempi di possibili dimensioni. 

Considera se la dimensione di determinazione dei prezzi deve essere una tabella o un set di opzioni. Se prevedi modifiche ai valori di una dimensione superiori a 10 o 12 e necessiti di ulteriori attributi per questi valori, crea un'entità anziché un set di opzioni. La gestione di un set di opzioni, ad esempio l'aggiunta o la rimozione di valori, richiede un amministratore o uno sviluppatore mentre l'aggiunta di nuove righe a una tabella può essere eseguita dalla maggior parte degli utenti aziendali.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
