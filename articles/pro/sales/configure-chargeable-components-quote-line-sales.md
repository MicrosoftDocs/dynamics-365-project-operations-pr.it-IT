---
title: Configurare i componenti addebitabili di una riga di offerta - semplice
description: Questo argomento fornisce informazioni sulla configurazione dei componenti addebitabili e non addebitabili di una riga di offerta basata su progetto.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177111"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Configurare i componenti addebitabili di una riga di offerta - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Una riga di offerta basata su progetto ha il concetto di componenti *inclusi* e *addebitabili*.

I componenti inclusi sono soggetti a:

  - Metodo di fatturazione e suddivisioni dei clienti
  - Limite da non superare 
  - Impostazioni della frequenza della fattura definite nella riga di offerta basata su progetto

Un sottoinsieme dei componenti inclusi può essere contrassegnato come addebitabile usando il campo **Tipo di fatturazione**. Il campo **Tipo di fatturazione** è un set di opzioni che consente i seguenti valori nel contesto di una riga di offerta:

  - Addebitabile
  - Non addebitabile

I componenti addebitabili possono essere definiti sulle attività, sui ruoli e sulle categorie di transazioni.

L'esigibilità è definita nelle attività per una riga di offerta e si applica a tutte le classi di transazione incluse in quella riga. Se il campo **Includi attività** è impostato su **Intero progetto** o viene lasciato vuoto, la scheda **Attività addebitabili** non è disponibile.

L'esigibilità è definita nei ruoli di una riga di offerta e si applica solo alla classe di transazione **Tempo**. Se il campo **Includi tempo** è impostato su **No** su una riga di offerta di progetto, la scheda **Ruoli addebitabili** non è disponibile.

L'esigibilità è definita nelle categorie di transazione per una riga di offerta e si applica solo alla classe di transazione **Spesa**. Se il campo **Includi spese** è impostato su **No** su una riga di offerta di progetto, la scheda **Categorie addebitabili** non è disponibile.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Aggiornare un'attività di progetto in modo che sia addebitabile o non addebitabile

Un'attività di progetto può essere addebitabile o non addebitabile nel contesto di una specifica riga di offerta basata su progetto, il che rende possibile la seguente configurazione:

Se una riga di offerta basata su progetto include **Tempo** e l'attività **T1**, l'attività è associata alla riga di offerta come addebitabile. Se è presente una seconda riga di offerta che include **Spese**, puoi associare l'attività **T1** nella riga di offerta come non addebitabile. Il risultato è che tutto il tempo registrato sull'attività è addebitabile e tutte le spese registrate sull'attività non sono addebitabili.

Il tipo di fatturazione di un'attività può essere configurato nella scheda **Attività addebitabili** di una riga di offerta basata su progetto aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Attività riga offerta**. In alternativa, puoi aggiornare il tipo di fatturazione per un'attività di progetto nel campo **Tipo di fatturazione** nella griglia secondaria dell'impostazione fatturazione attività di un progetto che mostra le righe di offerta associate a un'attività.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aggiornare un ruolo in modo che sia addebitabile o non addebitabile

Un ruolo può essere addebitabile o non addebitabile nel contesto di una specifica riga di offerta basata su progetto.

Il tipo di fatturazione di un ruolo può essere configurato nella scheda **Ruoli addebitabili** di una riga di offerta aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Ruoli addebitabili**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aggiornare una categoria di transazione in modo che sia addebitabile o non addebitabile

Una categoria di transazione può essere addebitabile o non addebitabile su una specifica riga di offerta.

Il tipo di fatturazione di una transazione può essere configurato nella scheda **Categorie addebitabili** di una riga di offerta aggiornando il campo **Tipo di fatturazione** nella griglia secondaria **Categorie addebitabili**.

### <a name="resolve-chargeability"></a>Risolvere l'esigibilità
Una stima o un valore effettivo creato per il tempo sarà considerato addebitabile solo se il **tempo** è incluso nella voce di contratto e se l'**attività** e il **ruolo** sono configurati come addebitabili nella riga di offerta.

Una stima o un valore effettivo creato per la spesa sarà considerato addebitabile solo se la **spesa** è inclusa nella riga di offerta e se l'**attività** e la **categoria di transazioni** sono configurati come addebitabili nella riga di offerta.

| Include il tempo | Include la spesa | Attività incluse | Ruolo | Categoria. | Attività | Fatturazione |
| --- | --- | --- | --- | --- | --- | --- |
| Sì | Sì | Progetto intero | Addebitabile | Addebitabile | Non può essere impostato | Fatturazione in base all'ora effettiva: addebitabile </br>Tipo di fatturazione su un valore effettivo di spesa: addebitabile |
| Sì | Sì | Solo le attività selezionate | Addebitabile | Addebitabile | Addebitabile | Fatturazione in base all'ora effettiva: addebitabile</br>Tipo di fatturazione su un valore effettivo di spesa: addebitabile |
| Sì | Sì | Solo le attività selezionate | Non addebitabile | Addebitabile | Addebitabile | Fatturazione in base all'ora effettiva: non addebitabile</br>Tipo di fatturazione su un valore effettivo di spesa: addebitabile |
| Sì | Sì | Solo le attività selezionate | Addebitabile | Addebitabile | Non addebitabile | Fatturazione in base all'ora effettiva: non addebitabile</br> Tipo di fatturazione su un valore effettivo di spesa: non addebitabile |
| Sì | Sì | Solo le attività selezionate | Non addebitabile | Addebitabile | Non addebitabile | Fatturazione in base all'ora effettiva: non addebitabile</br> Tipo di fatturazione su un valore effettivo di spesa: non addebitabile |
| Sì | Sì | Solo le attività selezionate | Non addebitabile | Non addebitabile | Addebitabile | Fatturazione in base all'ora effettiva: non addebitabile</br> Tipo di fatturazione su un valore effettivo di spesa: non addebitabile |
| No | Sì | Progetto intero | Non può essere impostato | Addebitabile | Non può essere impostato | Fatturazione in base all'ora effettiva: non disponibile </br>Tipo di fatturazione su un valore effettivo di spesa: addebitabile |
| No | Sì | Progetto intero | Non può essere impostato | Non addebitabile | Non può essere impostato | Fatturazione in base all'ora effettiva: non disponibile </br>Tipo di fatturazione su un valore effettivo di spesa: non addebitabile |
| Sì | No | Progetto intero | Addebitabile | Non può essere impostato | Non può essere impostato | Fatturazione in base all'ora effettiva: addebitabile</br>Tipo di fatturazione su un valore effettivo di spesa: non disponibile |
| Sì | No | Progetto intero | Non addebitabile | Non può essere impostato | Non può essere impostato | Fatturazione in base all'ora effettiva: non addebitabile </br>Tipo di fatturazione su un valore effettivo di spesa: non disponibile |
