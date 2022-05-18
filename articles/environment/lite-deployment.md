---
title: Distribuire Project Operations - semplice
description: 'Questo argomento fornisce informazioni su come installare la distribuzione semplice di Project Operations: dalla transazione alla fatturazione proforma.'
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580737"
---
# <a name="deploy-project-operations---lite"></a>Distribuire Project Operations - semplice

_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_



Project Operations supporta più modelli di distribuzione. Per determinare il miglior modello di distribuzione, vedi [Tipi di distribuzione](determine-deployment-type.md).


> [!IMPORTANT]
> Questa distribuzione, Distribuzione semplice: dalla transazione alla fatturazione proforma, si traduce in una **Distribuzione solo su Dataverse di Project Operations**.

- [Installare Project Operations in un nuovo ambiente Dataverse](#new)
- [Installare in un ambiente Dataverse esistente](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Installare Project Operations in un nuovo ambiente Dataverse

1. In quanto [amministratore globale o Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con una licenza Project Operations, crea un nuovo ambiente Dataverse nell'[interfaccia di amministrazione di PowerPlatform](https://admin.powerplatform.com). Assicurati che **Crea un database per questo ambiente** e **App Dynamics 365** siano abilitati. Per altre informazioni, vedi [Creare e gestire ambienti nell'interfaccia di amministrazione di Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Seleziona **Microsoft Dynamics 365 Project Operations** dall'elenco di distribuzione delle app Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installare Project Operations in un ambiente Dataverse esistente
1. Assicurati che l'ambiente non sia stato configurato con la [doppia scrittura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) poiché l'installazione installerà le funzionalità [Project Operations per scenari basati su risorse/materiali non stoccati](project-operations-integrated-deployment-overview.md).
2. In quanto [amministratore globale o Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con una licenza Project Operations, individuare l'ambiente nell'[interfaccia di amministrazione di PowerPlatform](https://admin.powerplatform.com) in cui desideri installare Project Operations.
3. Installa **Microsoft Dynamics 365 Project Operations** dall'elenco di distribuzione delle app Dynamics 365. Per ulteriori informazioni, vedi [Gestire le app Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
