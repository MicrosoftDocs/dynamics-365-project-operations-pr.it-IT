---
title: Panoramica delle modalità di gestione delle risorse
description: In questo argomento vengono fornite informazioni sulla funzionalità di gestione delle risorse in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94db65a2ddbdc6a7226c70907bcce4c45b4a3923
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000891"
---
# <a name="resource-management-modes-overview"></a>Panoramica delle modalità di gestione delle risorse

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


Dynamics 365 Project Operations supporta due modalità per poter eseguire l'intero flusso di prenotazione. La modalità di gestione è definita come un parametro del progetto e può essere modificata se le esigenze aziendali cambiano.    

## <a name="central-mode"></a>Modalità centrale
Per le organizzazioni che centralizzano l'allocazione delle risorse ai progetti, la modalità centrale fornisce un modo per garantire che i responsabili di progetto possano definire i requisiti di risorsa a livello di progetto. L'evasione dei requisiti di risorsa è delegato a un responsabile delle risorse. I responsabili di progetto possono accettare o rifiutare le risorse proposte dal responsabile delle risorse.

![Modalità centrale](./media/resource-management-central.png)

Per gestire le risorse con la modalità centrale, vedi:

- [Assegnare risorse prenotabili generiche a un'attività e generare requisiti di risorsa](/dynamics365/project-service/assign-generic-bookable-resource)
- [Prenotare risorse denominate da requisiti di risorsa](/dynamics365/project-service/book-named-resource)
- [Inviare una richiesta di risorsa](/dynamics365/project-service/submit-resource-request)
- [Soddisfare una richiesta di risorse](/dynamics365/project-service/resource-management-fulfill-requests)
- [Accettare o rifiutare una risorsa di progetto proposta da una richiesta di risorsa](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modalità ibrida
Per le organizzazioni che richiedono flessibilità nell'allocazione delle risorse, la modalità ibrida consente sia ai responsabili di progetto che ai responsabili delle risorse di prenotare le risorse.

![Modalità ibrida](./media/resource-management-hybrid.png)

Oltre al processo in modalità centrale supportato, vedi i seguenti argomenti per gestire tutti gli altri flussi di prenotazione supportati in modalità ibrida:

Prenota una risorsa direttamente per un progetto:
- [Prenotare risorse prenotabili denominate per un team di progetto e assegnarvi attività](/dynamics365/project-service/assign-named-bookable-resource)

Prenota una risorsa da un requisito di risorsa:
- [Assegnare risorse prenotabili generiche a un'attività e generare requisiti di risorsa](/dynamics365/project-service/assign-generic-bookable-resource)
- [Prenotare risorse denominate da requisiti di risorsa](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]