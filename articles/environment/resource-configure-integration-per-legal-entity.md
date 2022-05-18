---
title: Configurare l'integrazione di Project Operations per persona giuridica
description: Questo argomento fornisce informazioni sull'impostazione dell'integrazione per persona giuridica in Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585843"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurare l'integrazione di Project Operations per persona giuridica 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento ti guida attraverso i passaggi necessari per la configurazione Dynamics 365 Project Operations per la persona giuridica.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Abilitare le chiavi di funzionalità in Dynamics 365 Finance

Completa i seguenti passaggi per abilitare le funzioni richieste.

1. In Dynamics 365 Finance, vai all'area di lavoro **Gestione funzionalità**.
2. Nell'**elenco delle funzionalità**, trova e attiva le seguenti funzionalità:
  
    - **Abilita più voci di contratto per un progetto**
    - **Abilitare Project Operations in Dynamics 365 Customer Engagement**

> [!NOTE]
> Se non vedi le **chiavi di funzionalità** elencate, verifica che la tua versione di Finance soddisfi i requisiti di versione minima (versione dell'applicazione 10.0.13 con tutti gli aggiornamenti di qualità applicati o superiore). Seleziona **Controlla aggiornamenti** per aggiornare l'elenco delle funzionalità.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definire lo scenario di distribuzione di Project Operations per una persona giuridica

Puoi abilitare Project Operations in Dynamics 365 Customer Engagement a livello di persona giuridica. Puoi avere una persona giuridica utilizzando Project Operations in Dynamics 365 Customer Engagement per scenari basati su risorse/non stoccate. Nello stesso ambiente, puoi avere un'altra persona giuridica che utilizza Project Operations per scenari di ordini di produzione/stoccati.

1. In Dynamics 365 Finance, vai a **Gestione progetti e contabilità** > **Impostazioni** > **Parametri globali Gestione progetti e contabilità**.
2. Nell'elenco delle persone giuridiche disponibili, seleziona le entità in cui saranno abilitate più righe di contratto e le funzionalità Project Operations in Dynamics 365 Customer Engagement. Lascia deselezionate le persone giuridiche che utilizzeranno Project Operations per gli scenari di ordini di produzione/stoccati.

> [!NOTE]
> Una persona giuridica può essere selezionata solo se non dispone di progetti esistenti.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurare i parametri di Gestione progetti e contabilità

Ogni persona giuridica che utilizza Project Operations in Dynamics 365 Customer Engagement necessita di un set di parametri predefiniti. Questi parametri vengono configurati nella scheda **Project Operations** della pagina **Parametri di Gestione progetti e contabilità**. I parametri sono i seguenti:

  - **Tipo di fatturazione predefinito**: Project Operations utilizza un set fisso di valori predefiniti per il tipo di fatturazione che devono essere associati alle proprietà della riga Finance. Crea un record per ogni tipo di fatturazione: **Non specificato**, **Addebitabile**, **Non addebitabile**, **Gratuito** e **Non disponibile**.
  - **Impostazioni predefinite della categoria di progetto**: seleziona le categorie di progetto predefinite da utilizzare per ogni tipo di transazione. Queste impostazioni predefinite verranno utilizzate nel **giornale dell'integrazione di Project Operations** e nelle stime in cui non è specificata alcuna categoria di transazione per il valore effettivo del progetto.
  - **Previsioni**: seleziona il modello previsionale da utilizzare per le stime di tempi e costi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]