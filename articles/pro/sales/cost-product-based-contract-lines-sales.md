---
title: Costo delle voci di contratto basate su prodotto - semplice
description: In questo argomento vengono fornite informazioni sulla creazione
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177246"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="8e87f-103">Costo delle voci di contratto basate su prodotto - semplice</span><span class="sxs-lookup"><span data-stu-id="8e87f-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="8e87f-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="8e87f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8e87f-105">Le voci di contratto basate su prodotto in Dynamics 365 Project Operations includono il campo **Prezzo di costo** che memorizza il prezzo di costo del prodotto per i calcoli della redditività downstream.</span><span class="sxs-lookup"><span data-stu-id="8e87f-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="8e87f-106">Quando una voce di contratto basata su prodotto viene creata per un prodotto del catalogo, il costo della riga di offerta basata su prodotto viene derivato per impostazione predefinita dal campo **Costo standard** nel catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="8e87f-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="8e87f-107">Il campo del **costo standard** nel catalogo dei prodotti viene impostato nella valuta di base dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="8e87f-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="8e87f-108">Quando il costo unitario è predefinito nella voce di contratto, viene convertito nella valuta di vendita del contratto.</span><span class="sxs-lookup"><span data-stu-id="8e87f-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="8e87f-109">Costo unitario su una voce di contratto basata su prodotto</span><span class="sxs-lookup"><span data-stu-id="8e87f-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="8e87f-110">Avere un costo unitario su una voce di contratto basata su prodotto consente costi diversi per un prodotto per ciascuna unità di vendita.</span><span class="sxs-lookup"><span data-stu-id="8e87f-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="8e87f-111">Sebbene non sempre necessario, esistono alcuni scenari in cui il costo del prodotto può essere scontato per il cliente dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="8e87f-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="8e87f-112">Prendi in considerazione lo scenario seguente:</span><span class="sxs-lookup"><span data-stu-id="8e87f-112">Consider the following scenario:</span></span>

<span data-ttu-id="8e87f-113">Fabrikam Robotics sta installando bracci robotici presso le linee di assemblaggio di Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="8e87f-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="8e87f-114">Fabrikam fornisce servizi di installazione, ma i bracci robotici vengono acquistati da Trey Research.</span><span class="sxs-lookup"><span data-stu-id="8e87f-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="8e87f-115">Se l'installazione di bracci robotici presso Adatum Corporation apre un nuovo settore verticale per Trey Research, potrebbero concedere uno sconto speciale per questo accordo a Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="8e87f-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="8e87f-116">In questo caso, Fabrikam crea una voce di contratto basata su prodotto per i bracci robotici e immette un costo unitario per questo contratto diverso dal costo standard dei bracci robotici di Trey Research.</span><span class="sxs-lookup"><span data-stu-id="8e87f-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
