---
title: Distribuire Project Operations Lite
description: Questo articolo fornisce informazioni su come installare la distribuzione semplice di Project Operations, con la fatturazione proforma.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810983"
---
# <a name="deploy-project-operations-lite"></a>Distribuire Project Operations Lite

_**Si applica a:** Distribuzione lite: dalla transazione alla fatturazione proforma_



Project Operations supporta più modelli di distribuzione. Per determinare il miglior modello di distribuzione, vedi [Tipi di distribuzione](determine-deployment-type.md).


> [!IMPORTANT]
> Questa distribuzione, Distribuzione semplice: dalla transazione alla fatturazione proforma, si traduce in una **Distribuzione solo su Dataverse di Project Operations**.

- [Installare Project Operations in un nuovo ambiente Dataverse](#new)
- [Installare in un ambiente Dataverse esistente](#existing)
- [Installa in un ambiente Dataverse esistente con i componenti di doppia scrittura](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Installare Project Operations Lite in un nuovo ambiente Dataverse

1. In quanto [amministratore globale o Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con una licenza Project Operations, crea un nuovo ambiente Dataverse nell'[interfaccia di amministrazione di PowerPlatform](https://admin.powerplatform.com). Assicurati che **Crea un database per questo ambiente** e **App Dynamics 365** siano abilitati. Per altre informazioni, vedi [Creare e gestire ambienti nell'interfaccia di amministrazione di Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Seleziona **Microsoft Dynamics 365 Project Operations** dall'elenco di distribuzione delle app Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installare Project Operations Lite in un ambiente Dataverse esistente 
1. In quanto [amministratore globale o Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con una licenza Project Operations, individuare l'ambiente nell'[interfaccia di amministrazione di PowerPlatform](https://admin.powerplatform.com) in cui desideri installare Project Operations.
1. Installa **Microsoft Dynamics 365 Project Operations** dall'elenco di distribuzione delle app Dynamics 365. Per ulteriori informazioni, vedi [Gestire le app Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Installa Project Operations Lite in un ambiente Dataverse esistente in cui sono già presenti soluzioni di doppia scrittura

Se desideri continuare a eseguire Project Operations in modalità di distribuzione Lite, devi seguire questi passaggi:

1. In quanto [amministratore globale o Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) con una licenza Project Operations, individuare l'ambiente nell'[interfaccia di amministrazione di PowerPlatform](https://admin.powerplatform.com) in cui desideri installare Project Operations.
1. Installa **Microsoft Dynamics 365 Project Operations** dall'elenco di distribuzione delle app Dynamics 365. Per ulteriori informazioni, vedi [Gestire le app Dynamics 365](/power-platform/admin/manage-apps).
1. Poiché il tuo ambiente ha componenti di doppia scrittura che aiutano con l'integrazione con le app per la finanza e le operazioni installate, l'installazione di Project Operations installerà anche le funzionalità e le estensioni necessarie per integrare i dati relativi al progetto nelle app per la finanza e le operazioni. Poiché vuoi eseguire Project Operations nella distribuzione Lite, questi componenti di integrazione devono essere rimossi poiché creeranno restrizioni e sovraccarico per gli scenari di distribuzione Lite. Disinstalla manualmente le soluzioni **Doppia scrittura Dynamics 365 Project Operations** e **Mappe di entità di doppia scrittura Dynamics 365 Project Operations** per rimuovere questi componenti.
1. Vai a **Project Operations -> Impostazioni -> Parametri**. Apri la pagina dei dettagli **Parametro progetto** e imposta il campo **Comportamento di aggiornamento della soluzione** su **Solo Lite**. Ciò garantisce che eventuali aggiornamenti successivi di Project Operations non riporteranno i componenti di integrazione in Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
