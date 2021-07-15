---
title: Panoramica delle voci di contratto basate su prodotto - semplice
description: In questo argomento vengono fornite informazioni sulle voci di contratto basate su prodotto.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369741"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="0c2b1-103">Panoramica delle voci di contratto basate su prodotto - semplice</span><span class="sxs-lookup"><span data-stu-id="0c2b1-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="0c2b1-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="0c2b1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0c2b1-105">Puoi creare righe di contratto basate su prodotto in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="0c2b1-106">Le voci di contratto basate su prodotto possono essere righe create manualmente oppure articoli del catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="0c2b1-107">Catalogo prodotti</span><span class="sxs-lookup"><span data-stu-id="0c2b1-107">Product catalog</span></span>

<span data-ttu-id="0c2b1-108">I prodotti nel catalogo prodotti hanno un'unità e un'unità di vendita predefinite.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="0c2b1-109">Se vari prodotti condividono lo stesso set di attributi, puoi creare una famiglia di prodotti che ha anch'essa tali attributi.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="0c2b1-110">Tutti i prodotti in una famiglia di prodotti ereditano lo stesso set di attributi.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="0c2b1-111">Ad esempio, una società vende licenze di sottoscrizione per diversi tipi di software.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="0c2b1-112">Tutti i software con sottoscrizione hanno i due seguenti attributi:</span><span class="sxs-lookup"><span data-stu-id="0c2b1-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="0c2b1-113">Numero di utenti</span><span class="sxs-lookup"><span data-stu-id="0c2b1-113">Number of users</span></span>
- <span data-ttu-id="0c2b1-114">Durata della sottoscrizione (in mesi)</span><span class="sxs-lookup"><span data-stu-id="0c2b1-114">Subscription duration (in months)</span></span>

<span data-ttu-id="0c2b1-115">Per mantenere questo tipo di catalogo, crea una famiglia di prodotti denominata **Software di sottoscrizione**.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="0c2b1-116">Aggiungi gli attributi **Numero di utenti** e **Durata sottoscrizione** alla famiglia di prodotti.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="0c2b1-117">Quindi, aggiungi i singoli prodotti alla famiglia di prodotti **Software di sottoscrizione**.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="0c2b1-118">Aggiungere articoli del catalogo prodotti a un contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="0c2b1-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="0c2b1-119">I contratti di progetto presentano sezioni per due tipi di righe: basate su progetto e basate su prodotto.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="0c2b1-120">Le righe basate su prodotto includono tutti i prodotti e le unità nel listino prezzi del prodotto nel contratto.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="0c2b1-121">Puoi aggiungere prodotti che non fanno parte del listino prezzi del prodotto del contratto.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="0c2b1-122">Puoi selezionare prodotti in altri listini prezzi, oppure direttamente dal catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="0c2b1-123">Quando selezioni prodotti direttamente da un catalogo prodotti, il listino prezzi predefinito di quel prodotto viene utilizzato per ottenere il prezzo di vendita del prodotto.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="0c2b1-124">Se un listino prezzi predefinito non è impostato, il prezzo è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="0c2b1-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="0c2b1-125">Se una voce di contratto è basata su un catalogo prodotti, puoi sostituire il prezzo di vendita direttamente nella riga.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="0c2b1-126">Una voce di contratto ha il campo **Prezzi** con due valori:</span><span class="sxs-lookup"><span data-stu-id="0c2b1-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="0c2b1-127">**Sostituisci prezzo**</span><span class="sxs-lookup"><span data-stu-id="0c2b1-127">**Override pricing**</span></span>
- <span data-ttu-id="0c2b1-128">**Predefinito dell'utente**</span><span class="sxs-lookup"><span data-stu-id="0c2b1-128">**Use default**</span></span>

<span data-ttu-id="0c2b1-129">Se imposti il campo **Prezzi** su **Sostituisci prezzo**, il prezzo predefinito non è impostato.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="0c2b1-130">Immetti un prezzo per il prodotto nella voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="0c2b1-131">Se imposti il campo su **Usa predefinito**, viene utilizzato il prezzo di vendita predefinito e il campo non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="0c2b1-132">Dopo l'installazione di Project Operations, i prezzi di vendita predefiniti vengono immessi nelle righe basate su prodotto di un contratto.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="0c2b1-133">Il campo **Prezzi** viene quindi impostato su **Sostituisci prezzo** di modo che sia possibile modificare il prezzo predefinito nelle voci di contratto.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="0c2b1-134">Si tratta di una sostituzione specifica di Project Operations al comportamento delle righe basate su prodotto in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0c2b1-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]