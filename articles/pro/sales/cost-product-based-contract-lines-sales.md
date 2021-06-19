---
title: Costo delle voci di contratto basate su prodotto - semplice
description: In questo argomento vengono fornite informazioni sulla creazione
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003546"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="bb059-103">Costo delle voci di contratto basate su prodotto - semplice</span><span class="sxs-lookup"><span data-stu-id="bb059-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="bb059-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="bb059-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="bb059-105">Le righe di contratto basate sul prodotto in Dynamics 365 Project Operations includono il campo **Prezzo di costo** che memorizza il prezzo di costo del prodotto per i calcoli della redditività downstream.</span><span class="sxs-lookup"><span data-stu-id="bb059-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="bb059-106">Quando viene creata una riga di contratto basata sul prodotto per un prodotto catalogo, il costo della riga viene impostato per impostazione predefinita dal campo **Costo standard** nel catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="bb059-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="bb059-107">Il campo del **costo standard** nel catalogo dei prodotti viene impostato nella valuta di base dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="bb059-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="bb059-108">Quando il costo unitario è predefinito nella voce di contratto, viene convertito nella valuta di vendita del contratto.</span><span class="sxs-lookup"><span data-stu-id="bb059-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="bb059-109">Costo unitario su una voce di contratto basata su prodotto</span><span class="sxs-lookup"><span data-stu-id="bb059-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="bb059-110">Avere un costo unitario su una voce di contratto basata su prodotto consente costi diversi per un prodotto per ciascuna unità di vendita.</span><span class="sxs-lookup"><span data-stu-id="bb059-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="bb059-111">Sebbene non sempre necessario, esistono alcuni scenari in cui il costo del prodotto può essere scontato per il cliente dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="bb059-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="bb059-112">Prendi in considerazione lo scenario seguente:</span><span class="sxs-lookup"><span data-stu-id="bb059-112">Consider the following scenario:</span></span>

<span data-ttu-id="bb059-113">Fabrikam Robotics sta installando bracci robotici presso le linee di assemblaggio di Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="bb059-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="bb059-114">Fabrikam fornisce servizi di installazione ma Robotic Arms proviene da Trey Research.</span><span class="sxs-lookup"><span data-stu-id="bb059-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="bb059-115">Se l'installazione di bracci robotici presso Adatum Corporation apre un nuovo settore verticale per Trey Research, potrebbero concedere uno sconto speciale per questo accordo a Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="bb059-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="bb059-116">In questo caso, Fabrikam crea una riga di contratto basata sul prodotto per Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="bb059-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="bb059-117">Per questo contratto viene inserito un costo unitario.</span><span class="sxs-lookup"><span data-stu-id="bb059-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="bb059-118">Il costo è diverso dal costo di Robotic Arms di Trey Research.</span><span class="sxs-lookup"><span data-stu-id="bb059-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]