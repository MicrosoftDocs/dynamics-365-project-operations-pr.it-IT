---
title: Prestazioni delle proposte di fatturazione progetto
description: Questo argomento fornisce informazioni sui miglioramenti delle prestazioni delle proposte di fatturazione progetto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269795"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="f354c-103">Prestazioni delle proposte di fatturazione progetto</span><span class="sxs-lookup"><span data-stu-id="f354c-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f354c-104">Quando crei una nuova proposta di fatturazione, potresti riscontrare problemi di prestazioni con l'aumento del numero di progetti e sottoprogetti.</span><span class="sxs-lookup"><span data-stu-id="f354c-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="f354c-105">Per migliorare le prestazioni, è disponibile una funzione che riduce il tempo necessario per creare una nuova proposta di fatturazione per le transazioni di progetto registrate.</span><span class="sxs-lookup"><span data-stu-id="f354c-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="f354c-106">Abilitare il miglioramento delle prestazioni delle proposte di fatturazione progetto</span><span class="sxs-lookup"><span data-stu-id="f354c-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="f354c-107">Per abilitare la funzionalità di miglioramento delle prestazioni delle proposte di fatturazione progetto, completa i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="f354c-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="f354c-108">Vai a **Gestione funzionalità** > **Tutte**.</span><span class="sxs-lookup"><span data-stu-id="f354c-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="f354c-109">Nell'elenco delle funzionalità, individua **Miglioramento delle prestazioni delle proposte di fatturazione progetto**.</span><span class="sxs-lookup"><span data-stu-id="f354c-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="f354c-110">Seleziona **Abilita ora**.</span><span class="sxs-lookup"><span data-stu-id="f354c-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="f354c-111">Aggiorna il browser, quindi crea una nuova proposta di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="f354c-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="f354c-112">Disabilitare il miglioramento delle prestazioni delle proposte di fatturazione progetto</span><span class="sxs-lookup"><span data-stu-id="f354c-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="f354c-113">Per disabilitare la funzionalità di miglioramento delle prestazioni delle proposte di fatturazione progetto, completa i seguenti passaggi.</span><span class="sxs-lookup"><span data-stu-id="f354c-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="f354c-114">Vai a **Gestione funzionalità** > **Tutte**.</span><span class="sxs-lookup"><span data-stu-id="f354c-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="f354c-115">Nell'elenco delle funzionalità, individua **Miglioramento delle prestazioni delle proposte di fatturazione progetto**.</span><span class="sxs-lookup"><span data-stu-id="f354c-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="f354c-116">Seleziona **Disabilita**.</span><span class="sxs-lookup"><span data-stu-id="f354c-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="f354c-117">Aggiorna il browser.</span><span class="sxs-lookup"><span data-stu-id="f354c-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="f354c-118">Le prestazioni della proposta di fattura non possono essere applicate quando le regole di fatturazione sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="f354c-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="f354c-119">Durante il processo batch per creare proposte di fattura, il numero di sottoattività suddivide le attività in un numero massimo basato sul numero di contratti con transazioni fatturabili, indipendentemente da ciò che hai inserito.</span><span class="sxs-lookup"><span data-stu-id="f354c-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="f354c-120">Ad esempio, se inserisci **3** per il numero di attività secondarie per la creazione di proposte di fattura in batch e sono presenti solo due contratti con transazioni fatturabili, vengono create solo due attività secondarie.</span><span class="sxs-lookup"><span data-stu-id="f354c-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
