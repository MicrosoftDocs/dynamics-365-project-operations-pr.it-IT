---
title: Configurare la contabilità per i progetti interni
description: Questo argomento fornisce informazioni su come impostare le procedure contabili per i progetti interni in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287603"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurare la contabilità per i progetti interni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

I progetti interni consentono alle aziende di tenere traccia dei costi relativi alle attività che non vengono fatturate a un cliente. Esempi di progetti interni sono:

- Sviluppo di un prodotto, come un'app mobile, e monitoraggio dei costi associati allo sviluppo.
- Gestione dei tempi e delle spese di prevendita. Questo progetto interno di prevendita può essere convertito in un secondo momento in un progetto fatturabile se si acquisisce l'offerta.

Qualsiasi progetto non associato a un contratto in Dynamics 365 Project Operations viene considerato come interno. I profili di costi e ricavi di progetto non sono usati per determinare le regole contabili per il progetto. Il costo interno del progetto viene sempre registrato utilizzando i principi di profitti e perdite. I conti contabili per le registrazioni sono definiti nella pagina **Impostazione registrazione contabile**.

- Le transazioni temporali vengono registrate addebitando conto di **Costo** e accreditando il conto **Allocazione retribuzioni**.
- Le transazioni di spesa vengono registrate addebitando conto di **Costo** e accreditando il **Conto di contropartita predefinito per le spese**.

Dopo che le transazioni sono state registrate nel progetto, se il progetto è associato a un contratto di progetto, il sistema annulla tutte le transazioni accumulate e crea nuove transazioni fatturabili. Le transazioni fatturabili seguono le regole contabili definite nel rispettivo profilo di costi e ricavi del progetto.




[!INCLUDE[footer-include](../includes/footer-banner.md)]