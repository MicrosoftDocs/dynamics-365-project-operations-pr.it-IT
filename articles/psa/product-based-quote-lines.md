---
title: Righe di offerta basate su prodotto
description: In questo argomento vengono fornite informazioni sulle righe di offerta basate su prodotto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151258"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="e9100-103">Righe di offerta basate su prodotto</span><span class="sxs-lookup"><span data-stu-id="e9100-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="e9100-104">Puoi creare righe di offerta basate su prodotto in Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e9100-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="e9100-105">Le righe di offerta basate su prodotto possono essere righe "fuori catalogo" oppure articoli del catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="e9100-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="e9100-106">Catalogo prodotti</span><span class="sxs-lookup"><span data-stu-id="e9100-106">Product catalog</span></span>

<span data-ttu-id="e9100-107">I prodotti in un catalogo prodotti di Dynamics 365 hanno un'unità e un'unità di vendita predefinite.</span><span class="sxs-lookup"><span data-stu-id="e9100-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="e9100-108">Se vari prodotti condividono lo stesso set di attributi, puoi creare una famiglia di prodotti che ha anch'essa tali attributi.</span><span class="sxs-lookup"><span data-stu-id="e9100-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="e9100-109">Tutti i prodotti in una famiglia di prodotti ereditano lo stesso set di attributi.</span><span class="sxs-lookup"><span data-stu-id="e9100-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="e9100-110">Ad esempio, una società vende licenze di sottoscrizione per vari software.</span><span class="sxs-lookup"><span data-stu-id="e9100-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="e9100-111">Tutti i software con sottoscrizione hanno i due seguenti attributi:</span><span class="sxs-lookup"><span data-stu-id="e9100-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="e9100-112">Numero di utenti</span><span class="sxs-lookup"><span data-stu-id="e9100-112">Number of users</span></span> 
- <span data-ttu-id="e9100-113">Durata della sottoscrizione (in mesi)</span><span class="sxs-lookup"><span data-stu-id="e9100-113">Subscription duration (in months)</span></span>

<span data-ttu-id="e9100-114">Un ottimo modo di gestire questo tipo di catalogo è creare una famiglia di prodotti denominata **Software con sottoscrizione** che ha **Numero di utenti** e **Durata sottoscrizione** come attributi.</span><span class="sxs-lookup"><span data-stu-id="e9100-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="e9100-115">Puoi quindi aggiungere singoli prodotti, come **Dynamics 365 Sales** o **Dynamics 365 Field Service** alla famiglia di prodotti **Software con sottoscrizione**.</span><span class="sxs-lookup"><span data-stu-id="e9100-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="e9100-116">Aggiungere articoli del catalogo prodotti a un'offerta di progetto</span><span class="sxs-lookup"><span data-stu-id="e9100-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="e9100-117">Le pagine Offerta di progetto e Contratto di progetto presentano sezioni per due tipi di righe: righe basate su progetto e righe basate su prodotto.</span><span class="sxs-lookup"><span data-stu-id="e9100-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="e9100-118">Per le righe basate su prodotto, Dynamics 365 viene utilizzato per aggiungere elementi da un catalogo prodotti a un'offerta.</span><span class="sxs-lookup"><span data-stu-id="e9100-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="e9100-119">L'elenco a discesa nella riga di offerta o nella voce di contratto di progetto include tutti i prodotti e unità nel listino prezzi prodotto associato all'offerta o al contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="e9100-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="e9100-120">Puoi anche aggiungere prodotti che non fanno parte del listino prezzi prodotto dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="e9100-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="e9100-121">Inoltre, puoi selezionare prodotti in altri listini prezzi, oppure selezionare prodotti direttamente dal catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="e9100-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="e9100-122">Quando selezioni prodotti direttamente da un catalogo prodotti, il listino prezzi predefinito di quel prodotto viene utilizzato per ottenere il prezzo di vendita del prodotto.</span><span class="sxs-lookup"><span data-stu-id="e9100-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="e9100-123">Se un listino prezzi predefinito non è impostato, il prezzo è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e9100-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="e9100-124">Se una riga di offerta è basata su un catalogo prodotti, puoi sostituire il prezzo di vendita direttamente nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="e9100-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="e9100-125">Nota che una riga di offerta in Dynamics 365 include un campo **Prezzi**.</span><span class="sxs-lookup"><span data-stu-id="e9100-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="e9100-126">Sono disponibili due valori:</span><span class="sxs-lookup"><span data-stu-id="e9100-126">Two values are available:</span></span>

- <span data-ttu-id="e9100-127">Sostituisci prezzo</span><span class="sxs-lookup"><span data-stu-id="e9100-127">Override pricing</span></span>  
- <span data-ttu-id="e9100-128">Usa predefinito</span><span class="sxs-lookup"><span data-stu-id="e9100-128">Use default</span></span>

<span data-ttu-id="e9100-129">Se imposti questo campo su **Sostituisci prezzo**, Dynamics 365 non imposta un prezzo predefinito.</span><span class="sxs-lookup"><span data-stu-id="e9100-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="e9100-130">Devi immettere un prezzo per il prodotto nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="e9100-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="e9100-131">Se imposti questo campo su **Usa predefinito**, Dynamics 365 utilizza il prezzo di vendita predefinito e blocca il campo per impedirne la modifica.</span><span class="sxs-lookup"><span data-stu-id="e9100-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="e9100-132">Dopo l'installazione di PSA, i prezzi di vendita predefiniti vengono immessi nelle righe basate su prodotto di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="e9100-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="e9100-133">Il campo **Prezzi** viene quindi impostato su **Sostituisci prezzo** di modo che sia possibile modificare il prezzo predefinito nelle righe di offerta.</span><span class="sxs-lookup"><span data-stu-id="e9100-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Impostare Sostituisci prezzo](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="e9100-135">Fattori di quantità per prodotti</span><span class="sxs-lookup"><span data-stu-id="e9100-135">Quantity factors for products</span></span>

<span data-ttu-id="e9100-136">PSA utilizza fattori di quantità per supportare la vendita di prodotti basati su sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e9100-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="e9100-137">Per i prodotti basati su sottoscrizione, la quantità nella riga di offerta o nella voce di contratto di progetto è espressa come numero di mesi utente.</span><span class="sxs-lookup"><span data-stu-id="e9100-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="e9100-138">In genere, il prezzo del software con sottoscrizione è archiviato nel catalogo come prezzo per utente al mese.</span><span class="sxs-lookup"><span data-stu-id="e9100-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="e9100-139">Puoi tuttavia utilizzare altre descrizioni di tempo.</span><span class="sxs-lookup"><span data-stu-id="e9100-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="e9100-140">Durante il processo di vendita, il prezzo nella riga di offerta è in genere il prezzo per utente al mese negoziato e scontato ottenuto dall'agente di vendita IT.</span><span class="sxs-lookup"><span data-stu-id="e9100-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="e9100-141">Ogni transazione ha un numero di utenti differente e un differente numero di mesi di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e9100-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="e9100-142">La quantità utilizzata per calcolare la quantità della riga di offerta è un prodotto del numero di utenti e del numero di mesi di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e9100-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="e9100-143">Per supportare questo tipo di vendita, PSA ha introdotto il concetto di fattori di quantità.</span><span class="sxs-lookup"><span data-stu-id="e9100-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="e9100-144">I fattori di quantità si basano sugli attributi di prodotto in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e9100-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="e9100-145">Quando configuri specifiche proprietà per un prodotto, PSA consente di contrassegnare un sottoinsieme di queste proprietà, o tutte le proprietà, come fattori di quantità.</span><span class="sxs-lookup"><span data-stu-id="e9100-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="e9100-146">PSA verifica che solo le proprietà numeriche o le proprietà di prodotto che hanno un tipo di dati numerici siano contrassegnate come fattori di quantità.</span><span class="sxs-lookup"><span data-stu-id="e9100-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="e9100-147">Quando un prodotto per il quale sono configurati fattori di quantità viene aggiunto a una riga di offerta, il campo **Quantità** in tale riga diventa un campo di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e9100-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="e9100-148">Dopo aver immesso valori per le proprietà del prodotto che sono fattori di quantità, PSA calcola la quantità della riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="e9100-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="e9100-149">Ad esempio, Dynamics 365 potrebbe avere le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9100-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="e9100-150">**N. di utenti** - Il numero di utenti</span><span class="sxs-lookup"><span data-stu-id="e9100-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="e9100-151">**N. di mesi** - Il numero di mesi di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="e9100-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="e9100-152">**SKU prodotto**</span><span class="sxs-lookup"><span data-stu-id="e9100-152">**Product SKU**</span></span> 

<span data-ttu-id="e9100-153">Le proprietà **N. di utenti** e **N. di mesi** possono essere contrassegnate come fattori di quantità modificando le proprietà della riga prodotto.</span><span class="sxs-lookup"><span data-stu-id="e9100-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Contrassegnare N. di utenti e N. di mesi come fattori di qualità](media/basic-guide-11.png)
 
