---
title: Impostare le tariffe di vendita e costi per i prodotti del catalogo - semplice
description: Questo argomento fornisce informazioni su come configurare le tariffe di costo e vendita per le voci di un catalogo prodotti.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176706"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="f8c21-103">Impostare le tariffe di vendita e costi per i prodotti del catalogo - semplice</span><span class="sxs-lookup"><span data-stu-id="f8c21-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="f8c21-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="f8c21-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="f8c21-105">L'impostazione dei prezzi per gli articoli del catalogo prodotti in Dynamics 365 Project Operations è uguale a quella di Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="f8c21-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="f8c21-106">Poiché i prodotti non possono essere stimati o utilizzati nei progetti in Project Operations, non è necessario impostare i prezzi del catalogo prodotti sui listini prezzi di progetto per offerte e contratti.</span><span class="sxs-lookup"><span data-stu-id="f8c21-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="f8c21-107">I prezzi del catalogo prodotti devono essere impostati nel campo **Prezzo prodotto** di un'offerta, un contratto o un conto.</span><span class="sxs-lookup"><span data-stu-id="f8c21-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="f8c21-108">Non impostare i prezzi del catalogo prodotti nei listini prezzi di progetto per queste entità.</span><span class="sxs-lookup"><span data-stu-id="f8c21-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="f8c21-109">I listini prezzi di progetto sono esclusivi di Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f8c21-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="f8c21-110">Esiste una logica aziendale specifica dell'applicazione che copia i listini prezzi da un'offerta a un contratto.</span><span class="sxs-lookup"><span data-stu-id="f8c21-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="f8c21-111">Il risultato è un listino prezzi di progetto specifico del contratto.</span><span class="sxs-lookup"><span data-stu-id="f8c21-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="f8c21-112">L'operazione di copia può ritardare il processo di acquisizione dell'offerta se il listino prezzi di progetto dell'offerta diventa troppo grande.</span><span class="sxs-lookup"><span data-stu-id="f8c21-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="f8c21-113">I listini prezzi dei prodotti non vengono copiati per creare listini prezzi personalizzati nei contratti.</span><span class="sxs-lookup"><span data-stu-id="f8c21-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="f8c21-114">Ciò significa che i listini prezzi dei prodotti non influiscono sulle prestazioni del processo di acquisizione dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="f8c21-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
