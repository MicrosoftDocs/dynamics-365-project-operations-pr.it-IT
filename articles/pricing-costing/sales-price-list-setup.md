---
title: Configurare un listino prezzi di vendita
description: Questo argomento fornisce informazioni sui listini prezzi di vendita per la determinazione dei prezzi del progetto.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176256"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="2e919-103">Configurare un listino prezzi di vendita</span><span class="sxs-lookup"><span data-stu-id="2e919-103">Set up a sales price list</span></span>

<span data-ttu-id="2e919-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="2e919-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2e919-105">Per le offerte e i contratti di progetto, un listino prezzi di progetto include un modello di sostituzione dei prezzi differente rispetto a un listino prezzi di prodotto.</span><span class="sxs-lookup"><span data-stu-id="2e919-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="2e919-106">In una riga di offerta basata su catalogo prodotti, puoi sostituire il prezzo per ruoli e categorie direttamente nella riga di offerta in quanto ogni riga di offerta punta esattamente a un articolo del catalogo.</span><span class="sxs-lookup"><span data-stu-id="2e919-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="2e919-107">Tuttavia, in una riga di offerta basata su progetto, non puoi sostituire il prezzo per ruoli e categorie direttamente nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="2e919-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="2e919-108">Puoi usare il listino prezzi di progetto per utilizzare i due modelli di sostituzione distinti.</span><span class="sxs-lookup"><span data-stu-id="2e919-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="2e919-109">Ti consigliamo di avere un listino prezzi distinto per le risorse del progetto e gli articoli del catalogo, per via delle differenze di comportamento tra i due quando si sostituisce il metodo di determinazione dei prezzi.</span><span class="sxs-lookup"><span data-stu-id="2e919-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="2e919-110">Ognuna delle seguenti entità può avere uno o più listini prezzi di vendita associati per la determinazione dei prezzi di progetto:</span><span class="sxs-lookup"><span data-stu-id="2e919-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="2e919-111">Cliente (account)</span><span class="sxs-lookup"><span data-stu-id="2e919-111">Customer (account)</span></span> 
- <span data-ttu-id="2e919-112">Opportunità</span><span class="sxs-lookup"><span data-stu-id="2e919-112">Opportunity</span></span> 
- <span data-ttu-id="2e919-113">Offerta</span><span class="sxs-lookup"><span data-stu-id="2e919-113">Quote</span></span> 
- <span data-ttu-id="2e919-114">Contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="2e919-114">Project Contract</span></span>

<span data-ttu-id="2e919-115">L'associazione di queste entità con un listino prezzi è indicata dai listini prezzi di progetto.</span><span class="sxs-lookup"><span data-stu-id="2e919-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="2e919-116">Puoi associare uno o più listini prezzi alle entità di vendita Cliente, Opportunità, Offerta e Contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="2e919-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="2e919-117">Un listino prezzi di progetto predefinito non viene automaticamente inserito in un record del cliente.</span><span class="sxs-lookup"><span data-stu-id="2e919-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="2e919-118">Tuttavia, puoi associare manualmente un listino prezzi di progetto al record del cliente.</span><span class="sxs-lookup"><span data-stu-id="2e919-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="2e919-119">Devi comunque associare manualmente un listino prezzi di progetto solo quando hai un accordo di determinazione dei prezzi personalizzato con il cliente.</span><span class="sxs-lookup"><span data-stu-id="2e919-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="2e919-120">Quando un listino prezzi di progetto è associato a un'entità di vendita, le informazioni seguenti vengono convalidate:</span><span class="sxs-lookup"><span data-stu-id="2e919-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="2e919-121">Il listino prezzi ha un contesto **Vendite**.</span><span class="sxs-lookup"><span data-stu-id="2e919-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="2e919-122">La valuta del listino prezzi corrisponde alla valuta del cliente.</span><span class="sxs-lookup"><span data-stu-id="2e919-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="2e919-123">In un contratto di progetto, il seguente ordine di precedenza viene utilizzato per impostare automaticamente i listini prezzi di progetto correlati:</span><span class="sxs-lookup"><span data-stu-id="2e919-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="2e919-124">Offerta</span><span class="sxs-lookup"><span data-stu-id="2e919-124">Quote</span></span>
2. <span data-ttu-id="2e919-125">Opportunità</span><span class="sxs-lookup"><span data-stu-id="2e919-125">Opportunity</span></span>
3. <span data-ttu-id="2e919-126">Cliente</span><span class="sxs-lookup"><span data-stu-id="2e919-126">Customer</span></span> 
4. <span data-ttu-id="2e919-127">Impostazioni globali</span><span class="sxs-lookup"><span data-stu-id="2e919-127">Global settings</span></span> 

<span data-ttu-id="2e919-128">Quando un listino prezzi di progetto viene immesso per impostazione predefinita, il sistema verifica che la valuta corrisponde alla valuta del cliente e che i listini prezzi predefiniti immessi abbiano un contesto **Vendite**.</span><span class="sxs-lookup"><span data-stu-id="2e919-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="2e919-129">Puoi associare più listini prezzi di progetto alle entità Cliente, Opportunità, Offerta e Contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="2e919-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="2e919-130">Questa funzionalità supporta prezzi predefiniti specifici della data per un contratto di progetto di lunga durata, dove puoi necessitare molteplici listini prezzi per gli aggiornamenti dei prezzi che si hanno a causa dell'inflazione.</span><span class="sxs-lookup"><span data-stu-id="2e919-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="2e919-131">Tuttavia, se i listini prezzi associati all'entità Cliente, Opportunità, Offerta o Contratto di progetto hanno date di validità sovrapposte, i prezzi predefiniti possono non essere corretti.</span><span class="sxs-lookup"><span data-stu-id="2e919-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="2e919-132">Pertanto, devi assicurarti che i listini prezzi di progetto con date di validità che si sovrappongono non siano associati a tali entità.</span><span class="sxs-lookup"><span data-stu-id="2e919-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
