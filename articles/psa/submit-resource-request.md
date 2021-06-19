---
title: Inviare una richiesta di risorse
description: In questo argomento vengono fornite informazioni sull'invio di una richiesta per una risorsa di progetto.
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013176"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]