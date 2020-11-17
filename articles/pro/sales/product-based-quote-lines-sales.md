---
title: Panoramica delle righe dell'offerta basate su prodotto - semplice
description: Questo argomento fornisce informazioni sull'utilizzo delle righe di offerta basate su prodotto.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178193"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="33821-103">Panoramica delle righe dell'offerta basate su prodotto - semplice</span><span class="sxs-lookup"><span data-stu-id="33821-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="33821-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="33821-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33821-105">Puoi creare righe di offerta basate su prodotto in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="33821-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="33821-106">Le righe di offerta basate su prodotto possono essere aggiunte manualmente oppure possono essere articoli del catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="33821-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="33821-107">Catalogo prodotti</span><span class="sxs-lookup"><span data-stu-id="33821-107">Product catalog</span></span>

<span data-ttu-id="33821-108">Ogni prodotto nel catalogo prodotti ha un'unità e un'unità di vendita predefinite.</span><span class="sxs-lookup"><span data-stu-id="33821-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="33821-109">Se più prodotti condividono lo stesso set di attributi, puoi creare una famiglia di prodotti che ha anch'essa tali attributi.</span><span class="sxs-lookup"><span data-stu-id="33821-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="33821-110">Ad esempio, una società vende licenze di sottoscrizione per diversi tipi di software.</span><span class="sxs-lookup"><span data-stu-id="33821-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="33821-111">Tutti i software con sottoscrizione hanno i due seguenti attributi:</span><span class="sxs-lookup"><span data-stu-id="33821-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="33821-112">Numero di utenti</span><span class="sxs-lookup"><span data-stu-id="33821-112">Number of users</span></span>
- <span data-ttu-id="33821-113">Durata della sottoscrizione misurata in mesi</span><span class="sxs-lookup"><span data-stu-id="33821-113">A subscription duration measured in months</span></span>

<span data-ttu-id="33821-114">Per gestire questo tipo di catalogo crea una famiglia di prodotti denominata **Software con sottoscrizione** che ha il numero di utenti e la durata sottoscrizione come attributi.</span><span class="sxs-lookup"><span data-stu-id="33821-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="33821-115">Successivamente, puoi aggiungere singoli prodotti alla famiglia di prodotti **Software con sottoscrizione**.</span><span class="sxs-lookup"><span data-stu-id="33821-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="33821-116">Aggiungere articoli del catalogo prodotti a un'offerta di progetto</span><span class="sxs-lookup"><span data-stu-id="33821-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="33821-117">Le pagine **Offerta di progetto** e **Contratto di progetto** presentano sezioni per righe basate su progetto e righe basate su prodotto.</span><span class="sxs-lookup"><span data-stu-id="33821-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="33821-118">Per le righe basate su prodotto, l'elenco a discesa nella riga di offerta o nella voce di contratto di progetto include tutti i prodotti e unità nel listino prezzi prodotto.</span><span class="sxs-lookup"><span data-stu-id="33821-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="33821-119">Puoi anche aggiungere prodotti che non fanno parte del listino prezzi di prodotto.</span><span class="sxs-lookup"><span data-stu-id="33821-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="33821-120">Inoltre, puoi selezionare prodotti in altri listini prezzi oppure direttamente dal catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="33821-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="33821-121">Quando selezioni prodotti direttamente da un catalogo prodotti, il listino prezzi predefinito di quel prodotto viene utilizzato per ottenere il prezzo di vendita del prodotto.</span><span class="sxs-lookup"><span data-stu-id="33821-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="33821-122">Se un listino prezzi predefinito non è impostato, il prezzo è zero (0).</span><span class="sxs-lookup"><span data-stu-id="33821-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="33821-123">Quando una riga di offerta è basata su un catalogo prodotti, puoi sostituire il prezzo di vendita direttamente nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="33821-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="33821-124">Una riga di offerta nel campo **Prezzi** con due valori disponibili:</span><span class="sxs-lookup"><span data-stu-id="33821-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="33821-125">**Sostituisci prezzo**</span><span class="sxs-lookup"><span data-stu-id="33821-125">**Override Pricing**</span></span>
- <span data-ttu-id="33821-126">**Usa predefinita**</span><span class="sxs-lookup"><span data-stu-id="33821-126">**Use Default**</span></span>

<span data-ttu-id="33821-127">Se selezioni **Sostituisci prezzo**, il prezzo predefinito non è impostato.</span><span class="sxs-lookup"><span data-stu-id="33821-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="33821-128">Devi quindi immettere un prezzo per il prodotto nella riga di offerta.</span><span class="sxs-lookup"><span data-stu-id="33821-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="33821-129">Se selezioni **Usa predefinito**, viene utilizzato il prezzo di vendita predefinito e il campo è bloccato per la modifica.</span><span class="sxs-lookup"><span data-stu-id="33821-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="33821-130">I prezzi di vendita predefiniti vengono immessi nelle righe basate su prodotto di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="33821-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="33821-131">Il campo **Prezzi** viene quindi impostato su **Sostituisci prezzo** di modo che sia possibile modificare il prezzo predefinito nelle righe di offerta.</span><span class="sxs-lookup"><span data-stu-id="33821-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="33821-132">Si tratta di una sostituzione specifica di Project Operations al comportamento delle righe basate su prodotto in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="33821-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
