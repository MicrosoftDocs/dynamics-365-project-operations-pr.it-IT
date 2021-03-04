---
title: Panoramica delle modalità di gestione delle risorse
description: Questo argomento fornisce informazioni sulla funzionalità Gestione delle risorse in Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118523"
---
# <a name="resource-management-modes-overview"></a>Panoramica delle modalità di gestione delle risorse

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_


Dynamics 365 Project Operations supporta due modalità per eseguire il flusso di prenotazione complessivo. La modalità di gestione è definita come un parametro del progetto e può essere modificata se le esigenze aziendali cambiano.    

## <a name="central-mode"></a>Modalità centrale
Per le organizzazioni che centralizzano l'allocazione delle risorse ai progetti, la modalità centrale fornisce un modo per garantire che i responsabili di progetto possano definire i requisiti di risorsa a livello di progetto. L'evasione dei requisiti di risorsa è delegato a un responsabile delle risorse. I responsabili di progetto possono accettare o rifiutare le risorse proposte dal responsabile delle risorse.

![Modalità centrale](./media/resource-management-central.png)

Per gestire le risorse con la modalità centrale, vedi:

- [Assegnare risorse prenotabili generiche a un'attività e generare requisiti di risorsa](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Prenotare risorse denominate da requisiti di risorsa](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Inviare una richiesta di risorsa](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Soddisfare una richiesta di risorse](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Accettare o rifiutare una risorsa di progetto proposta da una richiesta di risorsa](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modalità ibrida
Per le organizzazioni che richiedono flessibilità nell'allocazione delle risorse, la modalità ibrida consente sia ai responsabili di progetto che ai responsabili delle risorse di prenotare le risorse.

![Modalità ibrida](./media/resource-management-hybrid.png)

Oltre al processo in modalità centrale supportato, vedi i seguenti argomenti per gestire tutti gli altri flussi di prenotazione supportati in modalità ibrida:

Prenota una risorsa direttamente per un progetto:
- [Prenotare risorse prenotabili denominate per un team di progetto e assegnarvi attività](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Prenota una risorsa da un requisito di risorsa:
- [Assegnare risorse prenotabili generiche a un'attività e generare requisiti di risorsa](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Prenotare risorse denominate da requisiti di risorsa](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]