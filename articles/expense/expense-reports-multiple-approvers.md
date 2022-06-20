---
title: Note spese e più approvatori
description: In questo articolo vengono fornite informazioni sui report di spesa che richiedono l'approvazione da parte di più persone.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88f42535e4826d1f618bd542eec3b26a6fde1a97
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914463"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]