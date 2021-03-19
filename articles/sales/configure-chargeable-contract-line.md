---
title: Configurare i componenti addebitabili di una voce di contratto basata su progetto
description: Questo argomento fornisce informazioni sui componenti inclusi, addebitabili e non addebitabili nelle voci del contratto.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2266d8e0fe998e7161ede4cb4eaf7d3c70c54f71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278693"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurare i componenti addebitabili di una voce di contratto basata su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Una voce di contratto basata su progetto ha il concetto di componenti inclusi, addebitabili e non addebitabili.

I componenti inclusi sono soggetti al metodo di fatturazione, alle suddivisioni dei clienti, ai limiti da non superare e alle impostazioni della frequenza di fatturazione definite nella voce di contratto basata su progetto.

Un sottoinsieme dei componenti inclusi può essere contrassegnato come addebitabile aggiornando il campo **Tipo di fatturazione**.

I componenti addebitabili possono essere definiti sui ruoli e sulle categorie di transazioni.

Per una voce di contratto di progetto, l'esigibilità definita su un ruolo si applica solo alla classe di transazione **Tempo**. Se **Includi tempo** è impostato su **No** su una voce di contratto di progetto, la scheda **Ruoli addebitabili** non è disponibile.

L'esigibilità è definita nelle categorie di transazione per una voce di contratto di progetto e si applica solo alla classe di transazione **Spesa**. Se **Includi spese** è impostato su **No** su una voce di contratto di progetto, la scheda **Categorie addebitabili** non è disponibile.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aggiornare un ruolo in modo che sia addebitabile o non addebitabile

Un ruolo può essere addebitabile o non addebitabile su una specifica voce di contratto basata su progetto.

Nella scheda **Ruoli addebitabili** di una voce di contratto basata su progetto, nella griglia secondaria **Categorie addebitabili**, nel campo **Tipo di fatturazione**, aggiorna il tipo di fatturazione per un ruolo.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aggiornare una categoria di transazione in modo che sia addebitabile o non addebitabile

Una categoria di transazione può essere addebitabile o non addebitabile su una specifica voce di contratto basata su progetto.

Nella scheda **Categorie addebitabili** di una voce di contratto basata su progetto, nella griglia secondaria **Categorie addebitabili**, nel campo **Tipo di fatturazione**, aggiorna il tipo di fatturazione per una transazione.

### <a name="resolve-chargeability"></a>Risolvere l'esigibilità

Una stima o un valore effettivo creato per il tempo sarà considerato addebitabile solo se il tempo è incluso nella voce di contratto e se il ruolo è configurato come addebitabile nella voce di contratto.

Una stima o un valore effettivo creato per la spesa sarà considerato addebitabile solo se la spesa è inclusa nella voce di contratto e se la categoria di transazione è configurata come addebitabile nella voce di contratto.

| Include il tempo | Include la spesa | Ruolo | Categoria. | Attività |
| --- | --- | --- | --- | --- |
| Sì | Sì | Addebitabile | Addebitabile | Fatturazione in base all'ora effettiva: addebitabile </br>Tipo di fatturazione su un valore effettivo di spesa: addebitabile |
| Sì | Sì | Non addebitabile | Addebitabile | Fatturazione in base all'ora effettiva: non addebitabile </br>Tipo di fatturazione su un valore effettivo di spesa: addebitabile |
| Sì | Sì | Non addebitabile | Non addebitabile | Fatturazione in base all'ora effettiva: non addebitabile </br>Tipo di fatturazione su un valore effettivo di spesa: non addebitabile |
| No | Sì | Non può essere impostato | Addebitabile | Fatturazione in base all'ora effettiva: non disponibile </br>Tipo di fatturazione su un valore effettivo di spesa: addebitabile |
| No | Sì | Non può essere impostato | Non addebitabile | Fatturazione in base all'ora effettiva: non disponibile </br>Tipo di fatturazione su un valore effettivo di spesa: non addebitabile |
| Sì | No | Addebitabile | Non può essere impostato | Fatturazione in base all'ora effettiva: addebitabile </br>Tipo di fatturazione su un valore effettivo di spesa: non disponibile |
| Sì | No | Non addebitabile | Non può essere impostato | Fatturazione in base all'ora effettiva: non addebitabile </br> Tipo di fatturazione su un valore effettivo di spesa: non disponibile |


[!INCLUDE[footer-include](../includes/footer-banner.md)]