---
title: Determinare il tipo di distribuzione
description: Questo argomento fornisce informazioni per determina il tipo di distribuzione di Project Operations giusto per la tua azienda.
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1aae04230104d27db2f62db8e674697fd83460ac
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948110"
---
# <a name="determine-your-deployment-type"></a>Determinare il tipo di distribuzione

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_

> [!IMPORTANT]
> Dopo aver acquistato la licenza, inizia da qui per determinare il miglior modello di distribuzione di Dynamics 365 Project Operations usando il [Flusso di installazione guidato](https://aka.ms/provisionprojectoperations).
> Dopo aver completato il flusso di installazione guidata, verrai indirizzato al portale di gestione corretto per completare l'installazione. Vedi i dettagli di distribuzione per completare l'installazione.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clienti esistenti di Dynamics che utilizzano Dynamics 365 Project Service Automation
Project Operations include le funzionalità fornite con Project Service Automation. Un percorso di aggiornamento verrà rilasciato per questi clienti nel primo ciclo di rilascio del 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clienti esistenti di Dynamics 365 Finance che utilizzando Gestione progetti e contabilità 

I clienti esistenti di Finance che utilizzano la funzionalità Gestione progetti e contabilità possono continuare a utilizzarlo così com'è. Vedi [Project Operations per scenari di materiali stoccati/ordini di produzione](#pma).


## <a name="deployment-regions"></a>Aree di distribuzione
Per determinare quali aree supportano la distribuzione di Project Operations, vedi [Disponibilità geografica per report Dynamics 365 e Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Seleziona **Visualizza report** ed espandi **Dynamics 365 > App per le operazioni > Dynamics 365 Project Operations** per visualizzare le aree supportate.

## <a name="deployment-types"></a>Tipi di distribuzione
Project Operations supporta più opzioni di distribuzione per soddisfare le tue esigenze. Che tu sia un cliente Dynamics 365 nuovo o esistente, Project Operations può supportare le tue esigenze.

Il nostro [Questionario sulla distribuzione](https://aka.ms/provisionprojectoperations) ti aiuterà a determinare la giusta distribuzione. I risultati ti guideranno verso uno dei seguenti tipi di distribuzione:

- [Distribuzione semplice: dalla transazione alla fatturazione proforma](#lite)
- [Project Operations per scenari di risorse/materiali non stoccati](#integrated)
- [Project Operations per scenari di materiali stoccati/ordini di produzione](#pma)

Project Operations supporta scenari di materiali stoccati/ordini di produzione e scenari basati su risorse/materiali non stoccati nello stesso ambiente tramite configurazioni a livello di persona giuridica. Ad esempio, Contoso può utilizzare le funzionalità per materiali stoccati/ordini di produzione nel proprio stabilimento di produzione negli Stati Uniti (Persona giuridica = Contoso Manufacturing United States). Contoso può utilizzare le funzionalità per materiali non stoccati/basate su risorse disponibili nello stabilimento Contoso Robotics Arms nel Regno Unito (Persona giuridica = Contoso Robotics - Regno Unito).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Distribuzione semplice: dalla transazione alla fatturazione proforma

La distribuzione semplice include le seguenti funzionalità:

- Processo di vendita per progetti che estendono le esperienze delle applicazioni Dynamics 365 Sales
- Pianificazione del progetto utilizzando Microsoft Project per il Web
- Determinazione dei prezzi multidimensionale
- Gestione delle risorse unificata
- Registrazione del tempo
- Spesa di base
- Fatturazione proforma per la revisione e le modifiche del responsabile del progetto 

#### <a name="deployment-steps"></a>Passaggi per la distribuzione
Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).

Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](lite-preview-subscription-sign-up.md) e [Eseguire il provisioning di un nuovo ambiente](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations per scenari di risorse/materiali non stoccati
Project Operations per scenari di risorse/materiali non stoccati includono le seguenti funzionalità:
 
- Processo di vendita per progetti che estendono l'applicazione Dynamics 365 Sales
- Pianificazione del progetto utilizzando Microsoft Project per il Web
- Determinazione dei prezzi multidimensionale
- Gestione delle risorse unificata
- Registrazione del tempo
- Spesa di base
- Spesa completa
- OCR ricevuta
- Fatturazione proforma e per il cliente 
- Riconoscimento dei ricavi per progetti

#### <a name="deployment-steps"></a>Passaggi per la distribuzione
Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).

Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](resource-sign-up-preview-subscription.md) e [Eseguire il provisioning di un nuovo ambiente](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations per scenari di materiali stoccati/ordini di produzione

- Pianificazione di un progetto tramite la struttura di suddivisione del lavoro
- Gestione delle risorse
- Registrazione del tempo
- Spesa completa
- OCR ricevuta
- Fatturazione completa
- Riconoscimento ricavi
- Ordini di produzione
- Supporto materiali stoccati con inventario

#### <a name="deployment-steps"></a>Passaggi per la distribuzione
Determina il miglior modello di distribuzione di Project Operations utilizzando il [questionario sulla distribuzione](https://aka.ms/provisionprojectoperations).

Per questa distribuzione, vedi [Iscriversi per gli abbonamenti in anteprima](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) e [Eseguire il provisioning di un nuovo ambiente](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]