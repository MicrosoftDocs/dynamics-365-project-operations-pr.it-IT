---
title: Impostare le tariffe di vendita e costi per i prodotti del catalogo - semplice
description: Questo argomento fornisce informazioni su come configurare le tariffe di costo e vendita per le voci di un catalogo prodotti.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764558"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="76ae6-103">Impostare le tariffe di vendita e costi per i prodotti del catalogo - semplice</span><span class="sxs-lookup"><span data-stu-id="76ae6-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="76ae6-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="76ae6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="76ae6-105">L'impostazione dei prezzi per gli articoli del catalogo prodotti in Dynamics 365 Project Operations è uguale all'impostazione in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="76ae6-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="76ae6-106">In Project Operations, i prodotti non possono essere stimati o utilizzati nei progetti, quindi non è necessario impostare i prezzi del catalogo prodotti sui listini prezzi del progetto per offerte e contratti.</span><span class="sxs-lookup"><span data-stu-id="76ae6-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="76ae6-107">Usa il campo **Prezzo del prodotto** di un'offerta, un contratto o un conto per impostare i prezzi del catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="76ae6-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="76ae6-108">Non impostare i prezzi del catalogo prodotti nei listini prezzi del progetto.</span><span class="sxs-lookup"><span data-stu-id="76ae6-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="76ae6-109">I listini prezzi di progetto sono esclusivi di Project Operations.</span><span class="sxs-lookup"><span data-stu-id="76ae6-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="76ae6-110">La logica aziendale specifica dell'applicazione copia i listini prezzi da un'offerta a un contratto.</span><span class="sxs-lookup"><span data-stu-id="76ae6-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="76ae6-111">Il risultato è un listino prezzi di progetto specifico del contratto.</span><span class="sxs-lookup"><span data-stu-id="76ae6-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="76ae6-112">L'operazione di copia può ritardare il processo di acquisizione dell'offerta se il listino prezzi di progetto dell'offerta diventa troppo grande.</span><span class="sxs-lookup"><span data-stu-id="76ae6-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="76ae6-113">I listini prezzi dei prodotti non vengono copiati per creare listini prezzi personalizzati nei contratti.</span><span class="sxs-lookup"><span data-stu-id="76ae6-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="76ae6-114">Poiché non è coinvolta la copia, le prestazioni del processo di offerta non vengono influenzate.</span><span class="sxs-lookup"><span data-stu-id="76ae6-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
