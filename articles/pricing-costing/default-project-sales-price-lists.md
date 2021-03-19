---
title: Listini prezzi predefiniti
description: Questo argomento fornisce informazioni sui listini prezzi di costo e vendita predefiniti in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 04c97429ab8ac769dd22b4127432d80de8fde937
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275588"
---
# <a name="default-price-lists"></a>Listini prezzi predefiniti

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

## <a name="sales-price-lists"></a>Listini prezzi di vendita

Ogni offerta e contratto di progetto in Dynamics 365 Project Operations contiene un listino prezzi di vendita predefinito. 

### <a name="price-list-default-on-project-quotes"></a>Listino prezzi predefinito per offerte di progetto
Il sistema completa il seguente processo per determinare quale listino prezzi impostare come predefinito per un'offerta di progetto:

1. Il sistema esamina i listini prezzi collegati ai listini prezzi di progetto dell'account. 
2. Se sono presenti listini prezzi di progetto collegati al record dell'account, il sistema esamina i listini prezzi di vendita collegati ai parametri di progetto che corrispondono alla valuta dell'offerta di progetto.
3. Successivamente, il sistema verifica la validità delle date dei listini prezzi che rientrano nell'intervallo di date dell'offerta di progetto. In particolare, la data di creazione dell'offerta.
4. Se sono presenti più listini prezzi validi per la data dell'offerta di progetto, tutti i listini prezzi sono predefiniti nell'offerta di progetto.
5. Se non sono in vigore listini prezzi per la data dell'offerta di progetto, non è presente alcun listino prezzi di progetto predefinito nell'offerta di progetto. Apparirà un messaggio di avviso per l'offerta di progetto. Il messaggio indica che poiché non sono presenti listini prezzi di progetto collegati non verrà assegnato un prezzo ai valori effettivi e alle spese del progetto.

### <a name="price-list-default-on-project-contracts"></a>Listino prezzi predefinito per contratti di progetto 
Il sistema completa il seguente processo per determinare quale listino prezzi impostare come predefinito per un contratto di progetto:

1. Se il contratto viene creato da un'offerta, i listini prezzi di progetto dell'offerta vengono copiati separatamente e collegati al contratto di progetto.
2. Se il contratto viene creato da zero, il sistema esamina i listini prezzi collegati ai listini prezzi di progetto dell'account. Se non sono presenti listini prezzi di progetto collegati al record dell'account, il sistema esamina i listini prezzi di vendita collegati ai parametri di progetto che corrispondono alla valuta del contratto di progetto.
4. Successivamente, il sistema verifica la validità delle date dei listini prezzi che rientrano nell'intervallo di date del contratto di progetto. In particolare, la data di creazione del contratto.
5. Se sono presenti più listini prezzi validi per la data del contratto, tutti i listini prezzi sono predefiniti nel contratto.
6. Se non sono in vigore listini prezzi per la data del contratto, non è presente alcun listino prezzi di progetto predefinito per il contratto. Apparirà un messaggio di avviso per il contratto di progetto. Il messaggio indica che poiché non sono presenti listini prezzi di progetto collegati non verrà assegnato un prezzo ai valori effettivi e alle spese del progetto.

## <a name="cost-price-lists"></a>Listini prezzi di costo

Non sono disponibili listini prezzi di costo predefiniti per alcuna entità in Project Operations. La determinazione del listino prezzi di costo da utilizzare per i costi di progetto viene sempre eseguita al momento. Il sistema completa il seguente processo per determinare quale listino prezzi usare per i costi di progetto:

1. Il sistema esamina innanzitutto i listini prezzi collegati all'unità organizzativa contratto del progetto.
2. Il sistema quindi esamina la data di validità dei listini prezzi che corrispondono alla data della riga di stima o valore effettivo in entrata. In questa situazione, *linea di stima* si riferisce a tutti e tre i contesti di stima in Project Operations:

    - Riga di stima del progetto
    - Dettagli riga di offerta
    - Dettagli voce di contratto
  
3. Se sono presenti più listini prezzi validi per la data del valore effettivo o della stima in entrata, viene selezionato il listino prezzi creato più di recente.
4. Se non sono presenti listini prezzi collegati all'unità organizzativa contratto del progetto, il sistema esamina i listini prezzi di costo collegati ai parametri di progetto che corrispondono alla valuta dell'offerta di progetto.
5. Quindi, il sistema esamina la data di validità dei listini prezzi che corrispondono alla data della riga di stima o valore effettivo in entrata. 
6. Se sono presenti più listini prezzi validi per la data del valore effettivo o della stima in entrata, viene selezionato il listino prezzi creato più di recente.
7. Se non sono presenti listini prezzi di costo collegati ai parametri del progetto che corrispondono alla valuta e alla data di validità, il sistema imposta la tariffa di costo su zero (0) nella riga di stima o valore effettivo in entrata.


[!INCLUDE[footer-include](../includes/footer-banner.md)]