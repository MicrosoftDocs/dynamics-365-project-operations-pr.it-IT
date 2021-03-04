---
title: Inviare una richiesta di risorse
description: In questo argomento vengono fornite informazioni sull'invio di una richiesta per una risorsa di progetto.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 173572be43149aea253bf7beddb993f8c50ab337
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149728"
---
# <a name="submitting-a-resource-request"></a>Inviare una richiesta di risorse

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

È possibile inviare un requisito di risorsa generato come richiesta di risorse. La richiesta viene quindi inviata a un responsabile delle risorse per essere evasa.

1. In Project Service Automation (PSA), nella pagina **Progetti**, fare clic sulla scheda **Team** per visualizzare un elenco di risorse prenotabili. 
2. Selezionare la risorsa generica con un requisito di risorsa nell'elenco e fare clic su **Invia richiesta**.

![Inviare una richiesta di risorse](media/RM-how-to-18.png)

Lo stato della richiesta del membro del team generico diventerà **Inviata**.

Dopo che la richiesta viene soddisfatta dal responsabile delle risorse, la risorsa generica verrà sostituita da una risorsa denominata se il responsabile delle risorse soddisfa la richiesta con la prenotazione di una risorsa denominata. In caso contrario, la risorsa generica rimarrà nel team e lo stato della richiesta diventerà **Revisione necessaria**, se il responsabile delle risorse ha proposto una risorsa denominata.
