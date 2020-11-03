---
title: Configurazione di componenti addebitabili di una voce di contratto basata su progetto
description: Questo argomento fornisce informazioni su come aggiungere componenti addebitabili alle voci di contratto in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d665a6351d2315d185e64e4eb6b0b8859f7bbc4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078783"
---
# <a name="configuring-chargeable-components-of-a-project-based-contract-line"></a>Configurazione di componenti addebitabili di una voce di contratto basata su progetto

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

Una voce di contratto basata su progetto ha i componenti *inclusi* e *addebitabili*.

I componenti inclusi sono componenti soggetti a:

  - Metodo di fatturazione e suddivisioni dei clienti
  - Limite da non superare 
  - Impostazioni della frequenza della fattura definite nella voce di contratto basata su progetto

Un sottoinsieme dei componenti inclusi può essere contrassegnato come addebitabile usando il campo **Tipo di fatturazione**. Il campo **Tipo di fatturazione** è un set di opzioni che consente i seguenti valori nel contesto di una voce di contratto:

  - Addebitabile
  - Non addebitabile

I componenti addebitabili possono essere definiti sulle attività, sui ruoli e sulle categorie di transazioni.

L'esigibilità è definita nelle attività per una voce di contratto di progetto e si applica a tutte le classi di transazione incluse in quella riga. Se il campo **Includi attività** di una voce di contratto è vuoto o impostato su *Intero progetto* , la scheda **Attività addebitabili** non è disponibile.

L'esigibilità definita nei ruoli per una voce di contratto di progetto si applica solo alla classe di transazione **Tempo**. Se il campo **Includi tempo** di una voce di contratto è impostato su **No** , la scheda **Ruoli addebitabili** non è disponibile.

L'esigibilità è definita nelle categorie di transazione per una voce di contratto di progetto e si applica solo alla classe di transazione **Spesa**. Se il campo **Includi spese** è impostato su **No** , la scheda **Categorie addebitabili** non è disponibile.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Aggiornare un'attività di progetto in modo che sia addebitabile o non addebitabile

Un'attività di progetto può essere addebitabile o non addebitabile in una specifica voce di contratto, il che rende possibile la seguente configurazione:

Se una voce di contratto basata su progetto include **Tempo** e l'attività **T1** è associata ad essa come addebitabile. Se è presente una seconda voce di contratto che include **Spesa** , puoi associare l'attività T1 nella voce di contratto come non addebitabile. Il risultato è che tutto il tempo registrato sull'attività è addebitabile e tutte le spese non sono addebitabili.

Il tipo di fatturazione di un'attività può essere configurato nella scheda **Attività addebitabili** di una voce di contratto basata su progetto aggiornando il campo **Tipo di fatturazione** nella griglia secondaria Attività voce di contratto. In alternativa, puoi aggiornare il campo **Tipo di fatturazione** nella griglia secondaria dell'impostazione della fatturazione di attività di un progetto che mostra le voci di contratto associate a un'attività.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Aggiornare un ruolo come addebitabile o non addebitabile

Un ruolo può essere addebitabile o non addebitabile su una specifica voce di contratto.

Il tipo di fatturazione di un ruolo può essere configurato nella scheda **Ruoli addebitabili** di una voce di contratto. A tale scopo, aggiorna il campo **Tipo di fatturazione** nella griglia secondaria **Ruoli addebitabili**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Aggiornare una categoria di transazione come addebitabile o non addebitabile

Una categoria di transazione può essere addebitabile o non addebitabile su una specifica voce di contratto.

Il tipo di fatturazione di una transazione può essere configurato nella scheda **Categorie addebitabili** di una voce di contratto basata di progetto. A tale scopo, aggiorna il campo **Tipo di fatturazione** nella griglia secondaria **Categorie addebitabili**.

### <a name="resolve-chargeability"></a>Risolvere l'esigibilità

Una stima o un valore effettivo creato per il tempo sarà considerato addebitabile solo se il **tempo** è incluso nella voce di contratto e se l' **attività** e il **ruolo** sono configurati come addebitabili nella voce di contratto.

Una stima o un valore effettivo creato per la spesa sarà considerato addebitabile solo se la **spesa** è inclusa nella voce di contratto e se le categorie **Attività** e **Transazione** sono configurate come addebitabili nella voce di contratto.


| Include il tempo | Include la spesa | Include le attività | Ruolo           | Categoria.       | Attività                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Sì           | Sì              | Progetto intero | Addebitabile     | Addebitabile     | Fatturazione in base all'ora effettiva: **addebitabile** </br> Tipo di fatturazione su un valore effettivo di spesa: **addebitabile**           |
| Sì           | Sì              | Attività selezionate | Addebitabile     | Addebitabile     | Fatturazione in base all'ora effettiva: **addebitabile** </br> Tipo di fatturazione su un valore effettivo di spesa: **addebitabile**           |
| Sì           | Sì              | Attività selezionate | Non addebitabile | Addebitabile     | Fatturazione in base all'ora effettiva: **non addebitabile** </br> Tipo di fatturazione su un valore effettivo di spesa: **addebitabile**       |
| Sì           | Sì              | Attività selezionate | Addebitabile     | Addebitabile     | Fatturazione in base all'ora effettiva: **non addebitabile** </br> Tipo di fatturazione su un valore effettivo di spesa: **non addebitabile** |
| Sì           | Sì              | Attività selezionate | Non addebitabile | Addebitabile     | Fatturazione in base all'ora effettiva: **non addebitabile** </br> Tipo di fatturazione su un valore effettivo di spesa: **non addebitabile** |
| Sì           | Sì              | Attività selezionate | Non addebitabile | Non addebitabile | Fatturazione in base all'ora effettiva: **non addebitabile** </br> Tipo di fatturazione su un valore effettivo di spesa: **non addebitabile** |
| No            | Sì              | Progetto intero | Non può essere impostato   | Addebitabile     | Fatturazione in base all'ora effettiva: **non disponibile**</br>Tipo di fatturazione su un valore effettivo di spesa: **addebitabile**          |
| No            | Sì              | Progetto intero | Non può essere impostato   | Non addebitabile | Fatturazione in base all'ora effettiva: **non disponibile**</br> Tipo di fatturazione su un valore effettivo di spesa: **non addebitabile**     |
| Sì           | No               | Progetto intero | Addebitabile     | Non può essere impostato   | Fatturazione in base all'ora effettiva: **addebitabile** </br> Tipo di fatturazione su un valore effettivo di spesa: **non disponibile**        |
| Sì           | No               | Progetto intero | Non addebitabile | Non può essere impostato   | Fatturazione in base all'ora effettiva: **non addebitabile** </br>Tipo di fatturazione su un valore effettivo di spesa: **non disponibile**   |
