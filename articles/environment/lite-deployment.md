---
title: Distribuire Project Operations - semplice
description: 'Questo argomento fornisce informazioni su come installare la distribuzione semplice di Project Operations: dalla transazione alla fatturazione proforma.'
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642188"
---
# <a name="deploy-project-operations---lite"></a>Distribuire Project Operations - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations supporta più modelli di distribuzione. Per determinare il miglior modello di distribuzione, vedi [Tipi di distribuzione](determine-deployment-type.md).


> [!IMPORTANT]
> Questa distribuzione, Distribuzione semplice: dalla transazione alla fatturazione proforma, si traduce in una **Distribuzione solo su Common Data Service di Project Operations**.

- [Installare Project Operations in un nuovo ambiente CDS](#new)
- [Installare in un ambiente CDS esistente](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Installare Project Operations in un nuovo ambiente CDS

1. In quanto [amministratore globale o Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) con una licenza Project Operations, crea un nuovo ambiente CDS nell'[interfaccia di amministrazione di PowerPlatform](https://admin.powerplatform.com). Assicurati che **Database CDS** e **App Dynamics 365** siano abilitate. Per altre informazioni, vedi [Creare e gestire ambienti nell'interfaccia di amministrazione di Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Seleziona **Microsoft Dynamics 365 Project Operations** dall'elenco di distribuzione delle app Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Installare Project Operations in un ambiente CDS esistente

1. In quanto [amministratore globale o Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) con una licenza Project Operations, individuare l'ambiente nell'[interfaccia di amministrazione di PowerPlatform](https://admin.powerplatform.com) in cui desideri installare Project Operations.
2. Installa **Microsoft Dynamics 365 Project Operations** dall'elenco di distribuzione delle app Dynamics 365. Per ulteriori informazioni, vedi [Gestire le app Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]