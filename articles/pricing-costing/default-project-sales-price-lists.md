---
title: Listini prezzi predefiniti
description: Questo articolo fornisce informazioni sulle vendite predefinite e sui listini prezzi di costo in Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410267"
---
# <a name="default-price-lists"></a>Listini prezzi predefiniti

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione lite: dalla transazione alla fatturazione proforma_

## <a name="sales-price-lists"></a>Listini prezzi di vendita

Ogni offerta e contratto di progetto in Dynamics 365 Project Operations contiene un listino prezzi di vendita predefinito. 

### <a name="price-list-default-on-project-quotes"></a>Listino prezzi predefinito per offerte di progetto
Il sistema completa il seguente processo per determinare quale listino prezzi impostare come predefinito per un'offerta di progetto:

1. Il sistema esamina i listini prezzi collegati ai listini prezzi di progetto dell'account. 
1. Se non sono presenti listini prezzi di progetto collegati al record dell'account, il sistema esamina i listini prezzi di vendita collegati ai parametri di progetto che corrispondono alla valuta dell'offerta di progetto.
1. Successivamente, il sistema verifica la validità delle date dei listini prezzi che rientrano nell'intervallo di date dell'offerta di progetto. In particolare, la data di creazione dell'offerta.
1. Se sono presenti più listini prezzi validi per la data dell'offerta di progetto, tutti i listini prezzi sono predefiniti nell'offerta di progetto.
1. Se non sono in vigore listini prezzi per la data dell'offerta di progetto, non è presente alcun listino prezzi di progetto predefinito nell'offerta di progetto. Apparirà un messaggio di avviso per l'offerta di progetto. Il messaggio indica che poiché non sono presenti listini prezzi di progetto collegati non verrà assegnato un prezzo ai valori effettivi e alle spese del progetto.

### <a name="price-list-default-on-project-contracts"></a>Listino prezzi predefinito per contratti di progetto 
Il sistema completa il seguente processo per determinare quale listino prezzi impostare come predefinito per un contratto di progetto:

1. Se il contratto viene creato da un'offerta, i listini prezzi di progetto dell'offerta vengono copiati separatamente e collegati al contratto di progetto.
1. Se il contratto viene creato da zero, il sistema esamina i listini prezzi collegati ai listini prezzi di progetto dell'account. Se non sono presenti listini prezzi di progetto collegati al record dell'account, il sistema esamina i listini prezzi di vendita collegati ai parametri di progetto che corrispondono alla valuta del contratto di progetto.
1. Successivamente, il sistema verifica la validità delle date dei listini prezzi che rientrano nell'intervallo di date del contratto di progetto. In particolare, la data di creazione del contratto.
1. Se sono presenti più listini prezzi validi per la data del contratto, tutti i listini prezzi sono predefiniti nel contratto.
1. Se non sono in vigore listini prezzi per la data del contratto, non è presente alcun listino prezzi di progetto predefinito per il contratto. Apparirà un messaggio di avviso per il contratto di progetto. Il messaggio indica che poiché non sono presenti listini prezzi di progetto collegati non verrà assegnato un prezzo ai valori effettivi e alle spese del progetto.

## <a name="cost-price-lists"></a>Listini prezzi di costo

Non sono disponibili listini prezzi di costo predefiniti per alcuna entità in Project Operations. La determinazione del listino prezzi di costo da utilizzare per i costi di progetto viene sempre eseguita per transazione. Il sistema completa il seguente processo per determinare quale listino prezzi usare per i costi di progetto:

1. Il sistema esamina i listini prezzi collegati all'unità organizzativa contratto del progetto.
1. Quindi, il sistema esamina la data di validità dei listini prezzi che corrispondono alla data del contesto di stima o contesto effettivo in entrata.

    - *Contesto di stima* si riferisce a uno dei tre contesti di stima in Project Operations:

        - Riga di stima del progetto
        - Dettagli riga di offerta
        - Dettagli voce di contratto

    - *Contesto attuale* si riferisce a una delle tre fonti per gli effettivi in Project Operations:

       - Scritture contabili in entrata create manualmente o le scritture contabili di correzione create in un giornale di registrazione
       - Righe del giornale di registrazione create durante l'invio dei registri di utilizzo del tempo, delle spese o dei materiali
       - Dettagli di riga fattura

    Quando Project Operations corrisponde alla validità della data della riga del giornale di registrazione in entrata o del dettaglio della riga della fattura nel *contesto attuale*, utilizza il campo **Data della transazione**.

    - Se sono presenti più listini prezzi validi per la data del contesto effettivo o del contesto attuale in entrata, viene selezionato il listino prezzi creato più di recente.
    - Se non sono presenti listini prezzi collegati all'unità organizzativa contratto del progetto, il sistema esamina i listini prezzi di costo collegati ai parametri di progetto che corrispondono alla valuta dell'offerta di progetto.

## <a name="enable-multi-currency-cost-price-list"></a>Abilita listino prezzi di costo a più valute

Questa impostazione può essere trovata in **Impostazioni** \> **Parametri**. Il valore predefinito è **No**.

Quando questa impostazione è abilitata (ovvero, il valore è impostato su **Sì**), il sistema si comporta nel modo seguente:

- Consente i listini dei prezzi di costo in qualsiasi valuta da associare con l'unità organizzativa. Ad esempio, un listino prezzi di costo nella valuta EUR può essere allegato a un'unità organizzativa nella valuta USD. Il sistema continuerà a convalidare che i listini prezzi di costo allegati a un'unità organizzativa non abbiano l'efficacia delle date sovrapposte.
- Convalida che i listini prezzi di costo allegati ai parametri del progetto non hanno validità della data sovrapposta, anche se hanno valute diverse. Questo comportamento è diverso dal comportamento predefinito (ovvero il comportamento quando il valore è impostato su **No**). Nel comportamento predefinito, solo i listini prezzi di costo che hanno la **stessa** valuta sono convalidati per l'efficacia della data non sovrapposta.
- Per un contesto di transazione in entrata, determina il listino prezzi di costo solo in base all'efficacia della data. Questo comportamento è diverso dal comportamento predefinito, in cui il sistema seleziona il listino prezzi di costo che corrisponde sia alla valuta del progetto che all'efficacia della data.

A causa di questi cambiamenti nel comportamento, i clienti di Project Operations saranno in grado di mantenere un listino prezzi di costo globale che sarà rilevante per l'intera azienda. Non dovranno avere listini prezzi in ciascuna valuta delle operazioni. Il listino prezzi globale avrà validità per data e consentirà di impostare tariffe di costo in qualsiasi valuta per una specifica combinazione di valori di dimensione dei prezzi. La valuta del listino prezzi di costo viene utilizzata solo per inserire i valori predefiniti quando **Prezzi dei ruoli**, **Prezzi di categoria** e **Listino prezzi** vengono creati i record degli articoli. Non verrà utilizzato per determinare il listino prezzi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
