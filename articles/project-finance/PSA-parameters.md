---
title: Parametri di integrazione di Project Service Automation
description: Questo argomento spiega come configurare la modalità di immissione dei dati predefiniti durante l'integrazione di Microsoft Dynamics 365 for Project Service Automation con Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: ade812ac-2f8f-4761-a474-0fd7246967df
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e46823f8bd3aef2ba9be271560c3a532be8ef0d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752635"
---
# <a name="project-service-automation-integration-parameters"></a>Parametri di integrazione di Project Service Automation

[!include[banner](../includes/banner.md)]

Nella pagina **Parametri di integrazione di Project Service Automation** puoi configurare la modalità di immissione dei dati predefiniti durante l'integrazione di Dynamics 365 Project Service Automation con Dynamics 365 Finance. Affinché i progetti vengano sincronizzati correttamente da Project Service Automation a Finance, è necessario configurare i seguenti campi.

Per aprire la pagina **Parametri di integrazione di Project Service Automation**, vai a **Gestione progetti e contabilità** \> **Imposta** \> **Parametri di integrazione di Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - L'integrazione delle attività di progetto, le categorie delle transazioni di spesa, le stime delle ore, le stime delle spese e il blocco delle funzionalità sono disponibili nella versione 8.0.
> - L'integrazione dei dati effettivi è disponibile nella versione 8.0.1 o successiva.


| Tabulazione                    | Campo                | Descrizione |
|------------------------|----------------------|-------------|
| Generale                | Tipo di progetto predefinito | Seleziona il tipo di progetto predefinito. Quando i progetti vengono sincronizzati da Project Service Automation, questo valore viene utilizzato se non è stato fornito un valore predefinito nel modello di integrazione. Durante la sincronizzazione, il campo **Tipo di progetto** dei nuovi progetti è impostato su questo valore. Tuttavia, il valore potrebbe essere aggiornato quando le righe del contratto di progetto vengono sincronizzate da Project Service Automation. |
|                        | Categoria temporale        | Selezionare la categoria temporale predefinita. Questo valore viene utilizzato quando le stime delle ore vengono sincronizzate da Project Service Automation. Quando le stime delle ore e i valori effettivi vengono sincronizzati da Project Service Automation, il campo **Categoria** delle nuove stime orarie del previsioni delle ore di progetto in Finance è impostato su questo valore. |
|                        | Categoria corrispettivi         | Selezionare la categoria di corrispettivi. Questo valore viene utilizzato quando i valori effettivi dei corrispettivi vengono sincronizzati da Project Service Automation. Quando i valori effettivi dei corrispettivi vengono sincronizzati da Project Service Automation, il campo **Categoria** delle nuove transazioni di corrispettivi in Finance è impostato su questo valore. |
| Impostazioni predefinite del gruppo di progetto | Tipo progetto         | Fai clic su **Nuovo** per aggiungere una riga in cui puoi selezionare il tipo di progetto per cui impostare il gruppo di progetti predefinito. Un tipo di progetto specifico può essere selezionato solo una volta nella configurazione. |
|                        | Gruppo di progetto        | Seleziona il gruppo di progetto predefinito per il tipo di progetto selezionato. Quando i nuovi progetti vengono sincronizzati da Project Service Automation, il campo **Gruppo di progetto** è impostato sul valore predefinito per il tipo di progetto se non è stato fornito un valore predefinito nel modello di integrazione. |
| Impostazioni predefinite per il tipo di fatturazione  | Tipo di fatturazione         | Fai clic su **Nuovo** per aggiungere una riga in cui puoi selezionare il tipo di fatturazione per cui impostare la proprietà della riga predefinita. Un tipo di fatturazione specifico può essere selezionato solo una volta nella configurazione. |
|                        | Proprietà riga        | Seleziona la proprietà riga predefinita per il tipo di fatturazione selezionato. Quando nuove stime orarie, nuove stime di spesa o nuovi valori effettivi vengono sincronizzati da Project Service Automation, il campo **Proprietà riga** è impostato sul valore predefinito per il tipo di fatturazione. |
| Blocco funzionalità  | Non applicabile       | Seleziona la funzionalità da disabilitare in Finance per progetti e contratti originati da Project Service Automation. Ad esempio, puoi disattivare la possibilità di modificare contratti e progetti, creare strutture di suddivisione del lavoro e inserire fogli presenze in Finance. I campi relativi alla contabilità continueranno ad essere abilitati, anche se resi non disponibili dall'impostazione dei parametri. Per impostazione predefinita, tutte le funzionalità sono abilitate. |
