---
title: Note spese e più approvatori
description: Questo argomento fornisce informazioni sulle note spese che richiedono l'approvazione di più persone.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897096"
---
# <a name="expense-reports-and-multiple-approvers"></a>Note spese e più approvatori

_**Si applica a:** Project Operations per scenari basati su risorse/non stoccate, Distribuzione semplice: dalla transazione alla fatturazione proforma_

A seconda dei criteri di approvazione delle spese dell'organizzazione, più di una persona potrebbe dover approvare una nota spese inviata. Quando imposti il processo del flusso di lavoro per l'approvazione della nota spese, puoi aggiungere elementi del flusso di lavoro che includono attività o passaggi per uno o più responsabili dell'approvazione della nota spese. Ad esempio, puoi richiedere che tutte le note spese siano approvate da due persone separate, il responsabile del dipendente che ha inviato il report e il coordinatore della contabilità fornitori.

Se decidi di richiedere più approvatori della nota spese, puoi aggiungere gli elementi del flusso di lavoro in uno dei seguenti modi:

- Aggiungi un elemento di approvazione con un passaggio. Ad esempio, il passaggio potrebbe richiedere che una nota spese venga assegnata a un gruppo di utenti e che venga approvata dal 50% dei membri del gruppo di utenti.
- Aggiungi un elemento di approvazione con più passaggi. Ad esempio, l'elemento di approvazione potrebbe avere i seguenti passaggi:

    1. Il responsabile del dipendente che ha presentato la nota spese la approva.
    2. L'addetto alla contabilità fornitori verifica le ricevute e le voci della nota spese.
    3. Il proprietario del budget approva la nota spese.

- Aggiungi più elementi di approvazione, ognuno dei quali ha un passaggio. Ad esempio, puoi aggiungere un elemento di approvazione separato per ciascuno dei seguenti passaggi:

    1. Il responsabile del dipendente approva la nota spese.
    2. Il proprietario del budget approva la nota spese.
