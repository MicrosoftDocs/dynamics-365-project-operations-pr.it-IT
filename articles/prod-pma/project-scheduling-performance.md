---
title: Prestazioni della pianificazione delle risorse di progetto
description: Questo argomento fornisce informazioni su come migliorare le prestazioni della pianificazione delle risorse per un gran numero di progetti.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 726788e9ecb7fc70648d06d0a5036becd7a45d2a
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682881"
---
# <a name="project-resource-scheduling-performance"></a>Prestazioni della pianificazione delle risorse di progetto

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


I problemi di prestazioni relativi alla pianificazione delle risorse possono verificarsi quando il numero di progetti raggiunge le migliaia. Per migliorare le prestazioni della pianificazione delle risorse, è disponibile una funzione che consente agli utenti di ridurre il tempo necessario per aprire il modulo di disponibilità delle risorse. In particolare, viene rimosso il processo di sincronizzazione di roll-up della capacità delle risorse e viene utilizzata la tabella **ResProjectResource** per velocizzare la ricerca delle risorse. Nota che la tabella **ResRollup** non verrà più utilizzata.

> [!IMPORTANT]
> Se esiste una dipendenza dal processo di sincronizzazione di roll-up della capacità delle risorse o dalla tabella **ResProjectResource**, non utilizzare questa funzione.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Abilitare il miglioramento delle prestazioni della pianificazione delle risorse
Per abilitare il miglioramento delle prestazioni della pianificazione delle risorse, completa i seguenti passaggi.

1. Vai a **Gestione funzionalità** > **Tutto** e nell'elenco delle funzionalità individua **Abilita la funzione di miglioramento delle prestazioni della pianificazione delle risorse di progetto**.
2. Seleziona **Abilita ora**.

> [!NOTE]
> Se non riesci a trovare la funzione nell'elenco, seleziona **Controlla aggiornamenti** per aggiornare l'elenco.

3. Aggiorna il browser, quindi vai a **Gestione progetti e contabilità** > **Periodico** > **Risorse di progetto** > **Sincronizza la capacità dei calendari delle risorse in tutte le società**.
4. Imposta **Rimuovi record di capacità esistenti** su **Sì** per rimuovere i dati precedenti. Se desideri generare dati incrementali, imposta su **No**.
5. Nel campo **Codice periodo** seleziona il periodo in cui generare i dati. Se selezioni un codice periodo, non è necessario definire una data di inizio e di fine.
6. Se lasci il campo **Codice periodo** vuoto, seleziona le date di inizio e fine specifiche per generare i dati.
7. Seleziona **OK**.

 > [!NOTE]
 > Verranno distribuiti i dati generali della tabella **ResCalendarCapacity** in tutte le società nel tuo ambiente, quindi il processo batch deve essere eseguito solo in una persona giuridica. I dati in questo processo batch sono necessari per calcolare la capacità delle risorse tramite il calendario associato.

8. Vai a **Gestione progetti e contabilità** > **Periodico** > **Risorse di progetto** > **Popola risorse di progetto in tutte le società** e poi seleziona **OK**. Questo è lo script di aggiornamento dei dati per i dati generali nelle tabelle **ResProjectResource**, **ResCalendarDateTimeRange** e **ResEffectiveDateTimeRange**. Anche i valori per il campo **PSAPRojSchedRole.RootActivity** vengono aggiornati. Se lo script non viene eseguito, riceverai un avviso quando proverai a eseguire le operazioni di pianificazione delle risorse.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Disattivare il miglioramento delle prestazioni della pianificazione delle risorse

1. Vai a **Gestione funzionalità** > **Tutto** e cerca **Abilita la funzione di miglioramento delle prestazioni della pianificazione delle risorse di progetto**.
2. Seleziona la funzione, quindi seleziona il pulsante **Disabilita**.
3. Aggiorna il browser.
4. Vai a **Gestione progetti e contabilità** > **Periodico** > **Sincronizzazione capacità** > **Sincronizza i roll-up della capacità delle risorse**.
5. Nella pagina **Sincronizzazione roll-up della capacità** imposta **Rimuovi record di capacità esistenti** su **Sì** per rimuovere i dati precedenti. Se desideri generare dati incrementali, imposta su **No**.
6. Nel campo **Codice periodo** seleziona il periodo in cui generare i dati. Se selezioni un codice periodo, non è necessario definire una data di inizio e di fine.
7. Se lasci il campo **Codice periodo** vuoto, seleziona le date di inizio e fine specifiche per generare i dati.
8. Seleziona **OK**.

> [!NOTE]
> Verranno distribuiti i dati generali della tabella **ResRollup** in tutte le società nel tuo ambiente, quindi il processo batch deve essere eseguito solo in una persona giuridica. Questo processo batch è necessario per tutte le visualizzazioni **Disponibilità delle risorse**. Se questo processo batch non viene eseguito, i dati **ResRollup** verranno generati istantaneamente, il che può richiedere tempo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]