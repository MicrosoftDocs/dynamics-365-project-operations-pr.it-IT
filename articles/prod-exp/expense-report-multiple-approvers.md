---
title: Più responsabili approvatore per una nota spese
description: Questo argomento fornisce informazioni sulle note spese che richiedono l'approvazione di più responsabili.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 383ce9eda6d0604ce0dd090e27a5c6fd569bd9e5
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685291"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Più responsabili approvatore per una nota spese

A seconda dei criteri di approvazione delle spese dell'organizzazione, più di una persona potrebbe dover approvare una nota spese inviata da un dipendente. Quando imposti il processo del flusso di lavoro per l'approvazione della nota spese, puoi aggiungere elementi del flusso di lavoro che includono attività o passaggi per uno o più responsabili dell'approvazione della nota spese. Ad esempio, puoi richiedere che tutte le note spese siano approvate dal responsabile del dipendente che ha inviato il report e dal coordinatore della contabilità fornitori.

Se decidi di richiedere più approvatori della nota spese, puoi aggiungere gli elementi del flusso di lavoro in uno dei seguenti modi:

- Aggiungi un elemento di approvazione con un passaggio. Ad esempio, il passaggio potrebbe richiedere che una nota spese venga assegnata a un gruppo di utenti e che venga approvata dal 50% dei membri del gruppo di utenti.
- Aggiungi un elemento di approvazione con più passaggi. Ad esempio, l'elemento di approvazione potrebbe avere i seguenti passaggi:

    1. Il responsabile del dipendente che ha presentato la nota spese la approva.
    2. L'addetto alla contabilità fornitori verifica le ricevute e le voci della nota spese.
    3. Il proprietario del budget approva la nota spese.

- Aggiungi più elementi di approvazione, ognuno dei quali ha un passaggio. Ad esempio, puoi aggiungere un elemento di approvazione separato per ciascuno dei seguenti passaggi:

    1. Il responsabile del dipendente approva la nota spese.
    2. Il proprietario del budget approva la nota spese.


[!INCLUDE[footer-include](../includes/footer-banner.md)]