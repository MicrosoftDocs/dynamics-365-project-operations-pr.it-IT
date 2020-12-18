---
title: Sviluppare i modelli di progetto con Copia progetto
description: Questo argomento fornisce informazioni su come creare modelli di progetto utilizzando l'azione personalizzata Copia progetto.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642413"
---
# <a name="develop-project-templates-with-copy-project"></a>Sviluppare i modelli di progetto con Copia progetto

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations supporta la capacità di copiare un progetto e ripristinare eventuali assegnazioni alle risorse generiche che ne rappresentano il ruolo. I clienti possono utilizzare questa funzionalità per creare modelli di progetto di base.

Quando selezioni **Copia progetto**, lo stato del progetto di destinazione viene aggiornato. Usa il **motivo stato** per determinare quando l'azione di copia è stata completata. La selezione di **Copia progetto** aggiorna anche la data di inizio del progetto sulla data di inizio corrente se non viene rilevata alcuna data di destinazione nell'entità del progetto di destinazione.

## <a name="copy-project-custom-action"></a>Azione personalizzata Copia progetto 

### <a name="name"></a>Nome 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parametri di input
Sono presenti tre parametri di input:

| Parametro          | Digita   | Valori                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | Stringa | **{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Riferimento entità | Progetto di origine |
| Destinazione             | Riferimento entità | Progetto di destinazione |


- **{"clearTeamsAndAssignments":true}**: il comportamento predefinito di Project per il Web e rimuove tutte le assegnazioni e i membri del team.
- **{"removeNamedResources":true}**: il comportamento predefinito di Project Operations e ripristina le assegnazioni a risorse generiche.

Per ulteriori valori predefiniti delle azioni, vedi [Usare le azioni API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Specificare i campi da copiare 
Quando l'azione viene chiamata, **Copia progetto** guarda la vista del progetto **Copia colonne di progetto** per determinare quali campi copiare quando il progetto viene copiato.
