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
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="99c0d-103">Configurare l'integrazione di Project Operations per persona giuridica</span><span class="sxs-lookup"><span data-stu-id="99c0d-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="99c0d-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="99c0d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="99c0d-105">Questo argomento ti guida attraverso i passaggi necessari per la configurazione Dynamics 365 Project Operations per la persona giuridica.</span><span class="sxs-lookup"><span data-stu-id="99c0d-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="99c0d-106">Abilitare le chiavi di funzionalità in Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="99c0d-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="99c0d-107">Completa i seguenti passaggi per abilitare le funzioni richieste.</span><span class="sxs-lookup"><span data-stu-id="99c0d-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="99c0d-108">In Dynamics 365 Finance, vai all'area di lavoro **Gestione delle funzionalità** workspace.</span><span class="sxs-lookup"><span data-stu-id="99c0d-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="99c0d-109">Nell'**elenco delle funzionalità**, trova e attiva le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="99c0d-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="99c0d-110">**Abilita più voci di contratto per un progetto**</span><span class="sxs-lookup"><span data-stu-id="99c0d-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="99c0d-111">**Abilita Project Operations in Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="99c0d-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="99c0d-112">Se non vedi le **chiavi di funzionalità** elencate, verifica che la tua versione di Finance soddisfi i requisiti di versione minima (versione dell'applicazione 10.0.13 con tutti gli aggiornamenti di qualità applicati o superiore).</span><span class="sxs-lookup"><span data-stu-id="99c0d-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="99c0d-113">Seleziona **Controlla aggiornamenti** per aggiornare l'elenco delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="99c0d-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="99c0d-114">Definire lo scenario di distribuzione di Project Operations per una persona giuridica</span><span class="sxs-lookup"><span data-stu-id="99c0d-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="99c0d-115">È possibile abilitare Project Operations in Dynamics 365 Customer Engagement a livello di persona giuridica.</span><span class="sxs-lookup"><span data-stu-id="99c0d-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="99c0d-116">Puoi avere una persona giuridica che utilizza Project Operations in Dynamics 365 Customer Engagement per scenari basati su risorse/non stoccate.</span><span class="sxs-lookup"><span data-stu-id="99c0d-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="99c0d-117">Nello stesso ambiente, puoi avere un'altra persona giuridica che utilizza Project Operations per scenari di ordini di produzione/stoccati.</span><span class="sxs-lookup"><span data-stu-id="99c0d-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="99c0d-118">In Dynamics 365 Finance, vai a **Gestione progetti e contabilità** > **Imposta** > **Parametri Gestione globale progetti e contabilità**.</span><span class="sxs-lookup"><span data-stu-id="99c0d-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="99c0d-119">Nell'elenco delle persone giuridiche disponibili, seleziona le entità in cui sono attive più voci di contratto per abilitare le funzionalità di Project Operations in Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="99c0d-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="99c0d-120">Lascia deselezionate le persone giuridiche che utilizzeranno Project Operations per gli scenari di ordini di produzione/stoccati.</span><span class="sxs-lookup"><span data-stu-id="99c0d-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="99c0d-121">Una persona giuridica può essere selezionata solo se non dispone di progetti esistenti.</span><span class="sxs-lookup"><span data-stu-id="99c0d-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="99c0d-122">Configurare i parametri di Gestione progetti e contabilità</span><span class="sxs-lookup"><span data-stu-id="99c0d-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="99c0d-123">Ogni persona giuridica che utilizza Project Operations in Dynamics 365 Customer Engagement necessita di una serie di parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="99c0d-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="99c0d-124">Questi parametri vengono configurati nella scheda **Project Operations** della pagina **Parametri di Gestione progetti e contabilità**.</span><span class="sxs-lookup"><span data-stu-id="99c0d-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="99c0d-125">I parametri sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="99c0d-125">The parameters are:</span></span>

  - <span data-ttu-id="99c0d-126">**Tipo di fatturazione predefinito**: Project Operations utilizza un set fisso di valori predefiniti per il tipo di fatturazione che devono essere associati alle proprietà della riga Finance.</span><span class="sxs-lookup"><span data-stu-id="99c0d-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="99c0d-127">Crea un record per ogni tipo di fatturazione: **Non specificato**, **Addebitabile**, **Non addebitabile**, **Gratuito** e **Non disponibile**.</span><span class="sxs-lookup"><span data-stu-id="99c0d-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="99c0d-128">**Impostazioni predefinite della categoria di progetto**: seleziona le categorie di progetto predefinite da utilizzare per ogni tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="99c0d-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="99c0d-129">Queste impostazioni predefinite verranno utilizzate nel **giornale dell'integrazione di Project Operations** e nelle stime in cui non è specificata alcuna categoria di transazione per il valore effettivo del progetto.</span><span class="sxs-lookup"><span data-stu-id="99c0d-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="99c0d-130">**Previsioni**: seleziona il modello previsionale da utilizzare per le stime di tempi e costi.</span><span class="sxs-lookup"><span data-stu-id="99c0d-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]