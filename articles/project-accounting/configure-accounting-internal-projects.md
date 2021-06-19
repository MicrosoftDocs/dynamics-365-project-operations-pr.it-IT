---
title: Configurare la contabilità per i progetti interni
description: Questo argomento fornisce informazioni su come impostare le procedure contabili per i progetti interni in Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012861"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurare la contabilità per i progetti interni

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

I progetti interni consentono alle aziende di tenere traccia dei costi relativi alle attività che non vengono fatturate a un cliente. Esempi di progetti interni sono:

- Sviluppo di un prodotto, come un'app mobile, e monitoraggio dei costi associati allo sviluppo.
- Gestione dei tempi e delle spese di prevendita. Questo progetto interno di prevendita può essere convertito in un secondo momento in un progetto fatturabile se si acquisisce l'offerta.

Qualsiasi progetto non associato a un contratto in Dynamics 365 Project Operations viene considerato come interno. I profili di costi e ricavi di progetto non sono usati per determinare le regole contabili per il progetto. Il costo interno del progetto viene sempre registrato utilizzando i principi di profitti e perdite. I conti contabili per le registrazioni sono definiti nella pagina **Impostazione registrazione contabile**.

- Le transazioni temporali vengono registrate addebitando conto di **Costo** e accreditando il conto **Allocazione retribuzioni**.
- Le transazioni di spesa vengono registrate addebitando conto di **Costo** e accreditando il **Conto di contropartita predefinito per le spese**.
- Le transazioni degli articoli vengono registrate addebitando il conto **Costo** e accreditando il conto **Costo - Articolo**.

Dopo che le transazioni sono state registrate nel progetto, se il progetto è associato a un contratto di progetto, il sistema annulla tutte le transazioni accumulate e crea nuove transazioni fatturabili. Le transazioni fatturabili seguono le regole contabili definite nel rispettivo profilo di costi e ricavi del progetto.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
