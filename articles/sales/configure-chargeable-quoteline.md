---
title: Configurare i componenti addebitabili di una riga di offerta basata su progetto
description: Questo argomento fornisce informazioni sui componenti inclusi, addebitabili e non addebitabili nelle righe di preventivo basate sul progetto.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642548"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Configurare i componenti addebitabili di una riga di offerta basata su progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Una riga di preventivo basata su progetto può includere componenti e componenti addebitabili.

I componenti inclusi sono soggetti al metodo di fatturazione, alle suddivisioni dei clienti, ai limiti da non superare e alle impostazioni della frequenza di fatturazione definite nella riga dell'offerta basata sul progetto.
Un sottoinsieme dei componenti inclusi può essere contrassegnato come addebitabile utilizzando **Tipo di fatturazione**. È possibile selezionare una delle seguenti opzioni nel campo **Tipo di fatturazione** nel contesto di una riga di preventivo:

   - Addebitabile
   - Non addebitabile

I componenti addebitabili possono essere definiti sui ruoli e sulle categorie di transazioni.

L'addebito definito sui ruoli per una riga dell'offerta di progetto si applica solo alla classe di transazione **Tempo**. Se una riga di preventivo del progetto ha **Includi tempo** = **No**, la scheda **Ruoli addebitabili** non è disponibile.

L'addebito definito sulle categorie di transazioni per una riga del preventivo di progetto si applica solo alla classe di transazione **Spese**. Se una riga di preventivo del progetto ha **Includi spese** = **No**, la scheda **Categorie addebitabili** non è disponibile.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aggiornare un ruolo in modo che sia addebitabile o non addebitabile
Un ruolo può essere addebitabile o non addebitabile su una riga di preventivo basata sul progetto. Il tipo di fatturazione su un ruolo può essere configurato nella scheda **Ruoli addebitabili** di una riga di preventivo basata sul progetto. Per fare ciò, aggiorna l'opzione **Tipo di fatturazione** nella griglia secondaria **Ruoli addebitabili**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aggiornare una categoria di transazione in modo che sia addebitabile o non addebitabile
Una categoria di transazioni può essere addebitabile o non addebitabile su una riga di preventivo basata sul progetto. Il tipo di fatturazione su una transazione può essere configurato nella scheda **Categorie addebitabili** di una riga di preventivo basata sul progetto. Per fare ciò, aggiorna il campo **Tipo di fatturazione** nella griglia secondaria **Categorie addebitabili**. 

## <a name="resolve-chargeability"></a>Risolvere l'esigibilità

Una stima o un valore effettivo creato per il tempo sarà considerato addebitabile solo se il tempo è incluso nella riga del preventivo e se il ruolo è configurato come addebitabile.
Una stima o un valore effettivo creato per una spesa sarà considerato addebitabile solo se la spesa è inclusa nella riga del preventivo e se la categoria di transazione è configurata come addebitabile nella riga del preventivo. La tabella seguente mostra come l'esigibilità è predefinita su ciascun ricavo effettivo. Le impostazioni predefinite si basano sui componenti inclusi e sul tipo di fatturazione impostato nella riga del preventivo.

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