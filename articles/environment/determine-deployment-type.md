---
title: Determinare il tipo di distribuzione
description: Questo argomento fornisce informazioni per determina il tipo di distribuzione di Project Operations giusto per la tua azienda.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078880"
---
# <a name="determine-your-deployment-type"></a>Determinare il tipo di distribuzione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

> [!IMPORTANT]
> Dopo aver acquistato la licenza, inizia qui per determinare il miglior modello di distribuzione di Dynamics 365 Project Operations utilizzando il [flusso di installazione guidata](https://aka.ms/provisionprojectoperations).
> Dopo aver completato il flusso di installazione guidata, verrai indirizzato al portale di gestione corretto per completare l'installazione. Vedi i dettagli di distribuzione per completare l'installazione.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clienti esistenti di Dynamics che utilizzano Dynamics 365 Project Service Automation
Project Operations include le funzionalità fornite con Project Service Automation. In futuro verrà rilasciato un percorso di aggiornamento per questi clienti.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clienti esistenti di Dynamics 365 Finance che utilizzando Gestione progetti e contabilità 

I clienti esistenti di Finance che utilizzano la funzionalità Gestione progetti e contabilità possono continuare a utilizzarla così com'è. Vedi [Project Operations per scenari di materiali stoccati/ordini di produzione](#pma).


## <a name="deployment-types"></a>Tipi di distribuzione
Project Operations supporta più opzioni di distribuzione per soddisfare le tue esigenze. Che tu sia un cliente Dynamics 365 nuovo o esistente, Project Operations può supportare le tue esigenze.

Il nostro [Questionario sulla distribuzione](https://aka.ms/provisionprojectoperations) ti aiuterà a determinare la giusta distribuzione. I risultati ti guideranno verso uno dei seguenti tipi di distribuzione:

- [Distribuzione semplice: dalla transazione alla fatturazione proforma](#lite)
- [Project Operations per scenari di risorse/materiali non stoccati](#integrated)
- [Project Operations per scenari di materiali stoccati/ordini di produzione](#pma)

Project Operations supporta scenari di materiali stoccati/ordini di produzione e scenari basati su risorse/materiali non stoccati nello stesso ambiente tramite configurazioni a livello di persona giuridica. Ad esempio, Contoso può utilizzare le funzionalità di materiali stoccati/ordini di produzione nel proprio stabilimento di produzione negli Stati Uniti (persona giuridica = Contoso Manufacturing United States). Contoso può utilizzare le funzionalità basate su risorse/materiali non stoccati nella struttura di assistenza Contoso Robotics Arms nel Regno Unito (persona giuridica = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Distribuzione semplice: dalla transazione alla fatturazione proforma

La distribuzione semplice include le seguenti funzionalità:

- Pianificazione del progetto utilizzando Microsoft Project per il Web
- Determinazione dei prezzi multidimensionale
- Gestione delle risorse unificata
- Registrazione del tempo
- Spesa di base
- Proposta di fattura

#### <a name="deployment-steps"></a>Passaggi per la distribuzione
Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).

Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](lite-preview-subscription-sign-up.md) e [Eseguire il provisioning di un nuovo ambiente](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations per scenari di risorse/materiali non stoccati
Project Operations per scenari di risorse/materiali non stoccati includono le seguenti funzionalità:
  
- Pianificazione del progetto utilizzando Microsoft Project per il Web
- Determinazione dei prezzi multidimensionale
- Gestione delle risorse unificata
- Registrazione del tempo
- Spesa di base
- Spesa completa
- OCR ricevuta
- Fattura completa
- Riconoscimento ricavi

#### <a name="deployment-steps"></a>Passaggi per la distribuzione
Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).

Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](resource-sign-up-preview-subscription.md) e [Eseguire il provisioning di un nuovo ambiente](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations per scenari di materiali stoccati/ordini di produzione

- Pianificazione di un progetto tramite la struttura di suddivisione del lavoro
- Gestione risorse
- Registrazione del tempo
- Spesa completa
- OCR ricevuta
- Fattura completa
- Riconoscimento ricavi
- Ordini di produzione
- Supporto materiali

#### <a name="deployment-steps"></a>Passaggi per la distribuzione
Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).

Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Eseguire il provisioning di un nuovo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

