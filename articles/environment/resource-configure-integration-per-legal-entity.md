---
title: Configurare l'integrazione di Project Operations per persona giuridica
description: Questo argomento fornisce informazioni sull'impostazione dell'integrazione per persona giuridica in Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000081"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurare l'integrazione di Project Operations per persona giuridica 

_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_

Questo argomento ti guida attraverso i passaggi necessari per la configurazione Dynamics 365 Project Operations per la persona giuridica.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Abilitare le chiavi di funzionalità in Dynamics 365 Finance

Completa i seguenti passaggi per abilitare le funzioni richieste.

1. In Dynamics 365 Finance, vai all'area di lavoro **Gestione delle funzionalità** workspace.
2. Nell'**elenco delle funzionalità**, trova e attiva le seguenti funzionalità:
  
    - **Abilita più voci di contratto per un progetto**
    - **Abilita Project Operations in Dynamics 365 Customer Engagement**

> [!NOTE]
> Se non vedi le **chiavi di funzionalità** elencate, verifica che la tua versione di Finance soddisfi i requisiti di versione minima (versione dell'applicazione 10.0.13 con tutti gli aggiornamenti di qualità applicati o superiore). Seleziona **Controlla aggiornamenti** per aggiornare l'elenco delle funzionalità.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definire lo scenario di distribuzione di Project Operations per una persona giuridica

È possibile abilitare Project Operations in Dynamics 365 Customer Engagement a livello di persona giuridica. Puoi avere una persona giuridica che utilizza Project Operations in Dynamics 365 Customer Engagement per scenari basati su risorse/non stoccate. Nello stesso ambiente, puoi avere un'altra persona giuridica che utilizza Project Operations per scenari di ordini di produzione/stoccati.

1. In Dynamics 365 Finance, vai a **Gestione progetti e contabilità** > **Imposta** > **Parametri Gestione globale progetti e contabilità**.
2. Nell'elenco delle persone giuridiche disponibili, seleziona le entità in cui sono attive più voci di contratto per abilitare le funzionalità di Project Operations in Dynamics 365 Customer Engagement. Lascia deselezionate le persone giuridiche che utilizzeranno Project Operations per gli scenari di ordini di produzione/stoccati.

> [!NOTE]
> Una persona giuridica può essere selezionata solo se non dispone di progetti esistenti.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurare i parametri di Gestione progetti e contabilità

Ogni persona giuridica che utilizza Project Operations in Dynamics 365 Customer Engagement necessita di una serie di parametri predefiniti. Questi parametri vengono configurati nella scheda **Project Operations** della pagina **Parametri di Gestione progetti e contabilità**. I parametri sono i seguenti:

  - **Tipo di fatturazione predefinito**: Project Operations utilizza un set fisso di valori predefiniti per il tipo di fatturazione che devono essere associati alle proprietà della riga Finance. Crea un record per ogni tipo di fatturazione: **Non specificato**, **Addebitabile**, **Non addebitabile**, **Gratuito** e **Non disponibile**.
  - **Impostazioni predefinite della categoria di progetto**: seleziona le categorie di progetto predefinite da utilizzare per ogni tipo di transazione. Queste impostazioni predefinite verranno utilizzate nel **giornale dell'integrazione di Project Operations** e nelle stime in cui non è specificata alcuna categoria di transazione per il valore effettivo del progetto.
  - **Previsioni**: seleziona il modello previsionale da utilizzare per le stime di tempi e costi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]