---
title: Valori predefiniti della dimensione finanziaria
description: Questo argomento fornisce informazioni su come impostare i valori predefiniti della dimensione finanziaria.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eec85b83cad4cd8fb6e0ec9c026c6a571bccf7f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287378"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="a17e4-103">Valori predefiniti della dimensione finanziaria</span><span class="sxs-lookup"><span data-stu-id="a17e4-103">Financial dimension defaults</span></span>

<span data-ttu-id="a17e4-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="a17e4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a17e4-105">Dynamics 365 Project Operations utilizza il framework [Dimensioni finanziarie](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) in Dynamics 365 Finance per fornire ulteriori informazioni sulle transazioni di contabilità generale e contabilità secondaria del progetto.</span><span class="sxs-lookup"><span data-stu-id="a17e4-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="a17e4-106">Le dimensioni finanziarie predefinite possono essere impostate su un cliente, una fonte di finanziamento del progetto, un passaggio fondamentale, una voce di contratto di progetto o un progetto.</span><span class="sxs-lookup"><span data-stu-id="a17e4-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="a17e4-107">Definire le dimensioni finanziarie predefinite per un cliente</span><span class="sxs-lookup"><span data-stu-id="a17e4-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="a17e4-108">I valori predefiniti della dimensione del cliente sono specificati in Finance.</span><span class="sxs-lookup"><span data-stu-id="a17e4-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="a17e4-109">Completa i seguenti passaggi per impostare i valori predefiniti delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a17e4-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="a17e4-110">Vai a **Contabilità clienti** > **Clienti** > **Tutti i clienti**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="a17e4-111">Nella pagina **Clienti** nella scheda **Dimensioni finanziarie** imposta i valori di dimensione finanziaria per un cliente specifico.</span><span class="sxs-lookup"><span data-stu-id="a17e4-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="a17e4-112">Definire le dimensioni finanziarie predefinite per contratti di progetto</span><span class="sxs-lookup"><span data-stu-id="a17e4-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="a17e4-113">I contratti di progetto vengono creati e gestiti in Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="a17e4-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="a17e4-114">Gli attributi contabili per i contratti di progetto sono impostati nel modulo **Gestione progetti e contabilità** in Finance.</span><span class="sxs-lookup"><span data-stu-id="a17e4-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="a17e4-115">Impostare le dimensioni finanziarie per una fonte di finanziamento del progetto</span><span class="sxs-lookup"><span data-stu-id="a17e4-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="a17e4-116">Vai a **Gestione progetti e contabilità** > **Progetti** > **Contratti di progetto**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="a17e4-117">Seleziona il record che desideri aggiornare e nella scheda **Contratto di progetto** seleziona **Mostra contabilità predefinita**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="a17e4-118">Espandi **Informazioni correlate** e seleziona la scheda **Fonti di finanziamento**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="a17e4-119">Imposta i valori predefiniti della dimensione finanziaria.</span><span class="sxs-lookup"><span data-stu-id="a17e4-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="a17e4-120">Tieni presente che le dimensioni finanziarie sono predefinite dal conto cliente.</span><span class="sxs-lookup"><span data-stu-id="a17e4-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="a17e4-121">Impostare le dimensioni finanziarie per una voce di contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="a17e4-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="a17e4-122">Vai a **Gestione progetti e contabilità** > **Progetti** > **Contratti di progetto**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="a17e4-123">Seleziona il record che desideri aggiornare e nella scheda **Contratto di progetto** seleziona **Mostra contabilità predefinita**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="a17e4-124">Espandi **Informazioni correlate** e seleziona la scheda **Voci di contratto**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="a17e4-125">Imposta i valori predefiniti della dimensione finanziaria.</span><span class="sxs-lookup"><span data-stu-id="a17e4-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="a17e4-126">Le impostazioni predefinite della dimensione finanziaria sono applicabili e possono essere utilizzate solo con le voci di contratto a prezzo fisso (passaggio fondamentale).</span><span class="sxs-lookup"><span data-stu-id="a17e4-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="a17e4-127">Questi valori predefiniti vengono utilizzati nelle transazioni di conto di progetto e nelle righe fattura correlate.</span><span class="sxs-lookup"><span data-stu-id="a17e4-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="a17e4-128">Definire le dimensioni finanziarie predefinite per i progetti</span><span class="sxs-lookup"><span data-stu-id="a17e4-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="a17e4-129">I progetti vengono creati e gestiti in CDS.</span><span class="sxs-lookup"><span data-stu-id="a17e4-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="a17e4-130">Gli attributi contabili per i progetti sono impostati nel modulo **Gestione progetti e contabilità** in Finance.</span><span class="sxs-lookup"><span data-stu-id="a17e4-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="a17e4-131">Vai a **Gestione progetti e contabilità** > **Progetti** > **Tutti i progetti**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="a17e4-132">Seleziona il record che desideri aggiornare e nella scheda **Progetto** seleziona **Mostra contabilità predefinita**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="a17e4-133">Espandi **Informazioni correlate** e seleziona la scheda **Configurazione**.</span><span class="sxs-lookup"><span data-stu-id="a17e4-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="a17e4-134">Imposta i valori predefiniti della dimensione finanziaria.</span><span class="sxs-lookup"><span data-stu-id="a17e4-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="a17e4-135">Tieni presente che le dimensioni finanziarie sono predefinite dal conto cliente.</span><span class="sxs-lookup"><span data-stu-id="a17e4-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="a17e4-136">Se il progetto è associato a una voce di contratto con più clienti di contratto di progetto, il cliente principale viene utilizzato per le dimensioni finanziarie predefinite.</span><span class="sxs-lookup"><span data-stu-id="a17e4-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="a17e4-137">Le dimensioni finanziarie predefinite del progetto vengono utilizzate per impostare i valori predefiniti della riga di giornale di registrazione per le transazioni di ore, spese e commissioni nel **Giornale di registrazione integrazione Project Operations** e sulle righe di fattura di progetto correlate.</span><span class="sxs-lookup"><span data-stu-id="a17e4-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]