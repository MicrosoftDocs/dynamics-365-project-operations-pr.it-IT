---
title: Esaminare il backlog di fatturazione in progetti e contratti di progetto
description: In questo argomento vengono fornite informazioni su come esaminare backlog relativi a tempo, spese e prodotti e su come contrassegnarli come pronti per la fatturazione.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: db15ea136b9939c0a0631936bcadab538bf2dd4a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752695"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Esaminare il backlog di fatturazione in progetti e contratti di progetto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Quando una transazione è pronta affinché una fattura venga creata ed elaborata, la transazione deve essere contrassegnata con **Pronta per la fatturazione**. In questo argomento vengono descritti i tipi di transazioni che è possibile creare.

## <a name="review-the-time-and-material-billing-backlog"></a>Esaminare il backlog di fatturazione di tempo e materiali

Quando un inserimento ore o una voce di spesa viene inviata e approvata per un progetto, PSA crea un valore effettivo del progetto. Se la combinazione di progetto e classe di transazione è mappata a una voce di contratto per un progetto tempo e materiali, vengono creati due valori effettivi quando la voce viene approvata:

- Valore effettivo costo 
- Valore effettivo vendite non fatturate

I valori effettivi di vendite non fatturate rappresentano il backlog di fatturazione e il relativo stato di fatturazione deve essere impostato su **Pronto per la fatturazione**. Quando una fattura di progetto viene creata, i valori effettivi di vendite non fatturate contrassegnati con **Pronto per la fatturazione** vengono copiati come dettagli della riga fattura.

Per esaminare il backlog di fatturazione per tempo e materiali, seleziona **Vendite** \> **Fatturazione** \> **Backlog di fatturazione tempo e materiali**. Seleziona tutti i valori effettivi di vendite non fatturate pronti per essere fatturati e quindi seleziona **Pronto per la fatturazione**. Lo stato di fatturazione di questi valori effettivi diventa **Pronto per la fatturazione**.

![Backlog di fatturazione tempo e materiale](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Esaminare il backlog di fatturazione prodotto

In PSA, quando un contratto di progetto include voci di contratto basate su prodotto, tali voci vengono considerate per la fatturazione ogni volta che viene creata una fattura per il contratto di progetto. Qualsiasi prodotto con voci di contratto contrassegnate con **Pronto per la fatturazione** viene copiato nella fattura di progetto come righe fattura di progetto.

Per esaminare il backlog di fatturazione per i prodotti, seleziona **Vendite** \> **Fatturazione** \> **Backlog di fatturazione prodotto**. Seleziona tutte le voci di contratto basate su prodotto pronte per essere fatturate e quindi seleziona **Pronto per la fatturazione**. Lo stato di fatturazione di queste righe diventa **Pronto per la fatturazione**.

![Backlog di fatturazione prodotto](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Esaminare i passaggi fondamentali di fatturazione in contratti a prezzo fisso

Ogni voce di contratto di progetto con un metodo di fatturazione a prezzo fisso deve definire i passaggi fondamentali del contratto. Questi passaggi fondamentali possono essere fatturati solo se sono contrassegnati come **Pronto per la fatturazione**. 

Per esaminare i passaggi fondamentali di fatturazione, seleziona **Vendite** \> **Fatturazione** \> **Passaggi fondamentali prezzo fisso**. Seleziona i passaggi fondamentali che sono pronti per essere fatturati e quindi seleziona **Pronto per la fatturazione**. Lo stato di fatturazione di questi passaggi fondamentali diventa **Pronto per la fatturazione**.

![Passaggi fondamentali prezzo fisso](media/FPBacklog.png)