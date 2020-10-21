---
title: Inviare una richiesta di risorsa
description: È possibile inviare un requisito di risorsa generato come richiesta di risorse. La richiesta viene quindi inviata a un responsabile delle risorse per essere evasa.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961718"
---
# <a name="submit-a-resource-request"></a>Inviare una richiesta di risorsa

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

È possibile inviare un requisito di risorsa generato come richiesta di risorse. La richiesta viene quindi inviata a un responsabile delle risorse per essere evasa.

1. In Dynamics 365 Project Operations, nella pagina **Progetti**, seleziona la scheda **Team** per visualizzare un elenco di risorse prenotabili. 
2. Seleziona la risorsa generica con un requisito di risorsa nell'elenco e fai clic su **Invia richiesta**.

Lo stato della richiesta del membro del team generico diventerà **Inviata**.

Dopo che la richiesta viene soddisfatta, la risorsa generica viene sostituita da una risorsa denominata se il responsabile delle risorse soddisfa la richiesta con la prenotazione di una risorsa denominata. In caso contrario, se il responsabile delle risorse propone una risorsa denominata, la risorsa generica rimane nel team e lo stato della richiesta diventerà **Revisione necessaria**.
