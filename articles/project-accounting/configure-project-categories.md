---
title: Configurare categorie di progetto
description: In questo argomento vengono fornite informazioni sulla configurazione delle categorie di progetto.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895971"
---
# <a name="configure-project-categories"></a><span data-ttu-id="4799e-103">Configurare categorie di progetto</span><span class="sxs-lookup"><span data-stu-id="4799e-103">Configure project categories</span></span>

<span data-ttu-id="4799e-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="4799e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4799e-105">Project Operations offre solide funzionalità per la categorizzazione dei ricavi e delle spese sui progetti.</span><span class="sxs-lookup"><span data-stu-id="4799e-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="4799e-106">Le categorie consentono di creare report e analizzare le transazioni di progetto e di guidare la registrazione nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="4799e-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="4799e-107">Il diagramma seguente illustra la correlazione tra categorie di transazioni, categorie condivise e categorie di progetto.</span><span class="sxs-lookup"><span data-stu-id="4799e-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="4799e-108">Le categorie di transazioni sono il raggruppamento di base per le transazioni di progetto.</span><span class="sxs-lookup"><span data-stu-id="4799e-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="4799e-109">All'interno di quel raggruppamento, c'è un insieme di categorie condivise che possono essere condivise tra applicazioni e moduli.</span><span class="sxs-lookup"><span data-stu-id="4799e-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="4799e-110">Entrando ancora più nello specifico, le categorie di progetto sono il livello di categorie più granulare.</span><span class="sxs-lookup"><span data-stu-id="4799e-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="4799e-111">Le categorie di progetto sono specifiche per persona giuridica, modulo e applicazione.</span><span class="sxs-lookup"><span data-stu-id="4799e-111">Project categories are specific to legal entity, module, and application.</span></span>

![Correlazione tra categorie di transazioni, categorie condivise e categorie di progetto](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="4799e-113">Categorie di transazioni</span><span class="sxs-lookup"><span data-stu-id="4799e-113">Transaction categories</span></span>

<span data-ttu-id="4799e-114">Le categorie di transazioni rappresentano il raggruppamento di base per le transazioni di progetto e non sono specifiche della società o del tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="4799e-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="4799e-115">Ad esempio, Contoso Robotics utilizza le categorie Progettazione, Viaggio, Installazione e Transazione di servizio per raggruppare le transazioni di progetto.</span><span class="sxs-lookup"><span data-stu-id="4799e-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="4799e-116">Le categorie di transazione sono definite nel modulo Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4799e-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="4799e-117">Vai a **Impostazioni** \> **Categorie di transazione** per aprire il modulo.</span><span class="sxs-lookup"><span data-stu-id="4799e-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="4799e-118">Crea una nuova categoria di transazione selezionando **Nuovo** o selezionando **Importa da Excel**.</span><span class="sxs-lookup"><span data-stu-id="4799e-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="4799e-119">Categorie condivise</span><span class="sxs-lookup"><span data-stu-id="4799e-119">Shared categories</span></span>

<span data-ttu-id="4799e-120">Dynamics 365 utilizza il concetto di categorie condivise per classificare le spese in diverse applicazioni, ad esempio Dynamics 365 Finance, Dynamics 365 Supply Chain e Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4799e-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="4799e-121">Per ogni categoria di transazione creata, Project Operations crea automaticamente quattro categorie condivise correlate: ore, spese, commissioni e articolo.</span><span class="sxs-lookup"><span data-stu-id="4799e-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="4799e-122">Puoi rivedere e modificare le categorie condivise andando su **Gestione progetti e contabilità** \> **Configura** \> **Categorie** \> **Categorie condivise**.</span><span class="sxs-lookup"><span data-stu-id="4799e-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="4799e-123">Categorie progetti</span><span class="sxs-lookup"><span data-stu-id="4799e-123">Project categories</span></span>

<span data-ttu-id="4799e-124">Le categorie di progetto rappresentano il livello più granulare di configurazione delle categorie e devono essere configurate separatamente, e per ogni azienda, da un contabile di progetto.</span><span class="sxs-lookup"><span data-stu-id="4799e-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="4799e-125">Vai a **Gestione progetti e contabilità** \> **Configura** \> **Categorie** \> **Categorie di progetto**.</span><span class="sxs-lookup"><span data-stu-id="4799e-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="4799e-126">Seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="4799e-126">Select **New**.</span></span>
3. <span data-ttu-id="4799e-127">Seleziona l'**ID categoria** della categoria condivisa creata nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="4799e-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="4799e-128">Project Operations consente di utilizzare solo le categorie condivise associate alle categorie di transazione.</span><span class="sxs-lookup"><span data-stu-id="4799e-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="4799e-129">Seleziona un gruppo di categorie.</span><span class="sxs-lookup"><span data-stu-id="4799e-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="4799e-130">Gruppi di categorie</span><span class="sxs-lookup"><span data-stu-id="4799e-130">Category groups</span></span>

<span data-ttu-id="4799e-131">I gruppi di categorie vengono utilizzati per condividere proprietà, principalmente profili di registrazione, tra le categorie di progetto correlate.</span><span class="sxs-lookup"><span data-stu-id="4799e-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="4799e-132">Deve essere presente almeno un gruppo di categorie per ogni tipo di transazione e ad ogni categoria di progetto è assegnato un gruppo.</span><span class="sxs-lookup"><span data-stu-id="4799e-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="4799e-133">Le specifiche di registrazione in Project Operations sono definite dalle regole del profilo dei costi e dei ricavi del progetto, dalle categorie di progetto e dai gruppi di categorie.</span><span class="sxs-lookup"><span data-stu-id="4799e-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="4799e-134">Puoi configurare gruppi di categorie andando a **Gestione progetti e contabilità** \> **Configura** \> **Categorie** \> **Gruppi di categorie**.</span><span class="sxs-lookup"><span data-stu-id="4799e-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
