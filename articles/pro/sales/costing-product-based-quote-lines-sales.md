---
title: Costo delle righe dell'offerta basate sul prodotto
description: Questo argomento fornisce informazioni sull'applicazione di un prezzo di costo a una riga di offerta basata su prodotto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118928"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="6e8ce-103">Costo delle righe dell'offerta basate sul prodotto</span><span class="sxs-lookup"><span data-stu-id="6e8ce-103">Costing product-based quote lines</span></span>

<span data-ttu-id="6e8ce-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="6e8ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6e8ce-105">Le righe di offerta basate sul prodotto in Dynamics 365 Project Operations hanno anche un campo **Prezzo di costo**.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="6e8ce-106">Questo campo viene utilizzato per tener traccia del prezzo di costo del prodotto nella riga di offerta e per i calcoli della redditività downstream.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="6e8ce-107">Quando una riga di offerta basata su prodotto viene creata per un prodotto del catalogo, il costo della riga di offerta basata sul prodotto viene derivato per impostazione predefinita dal campo **Costo standard** nel catalogo prodotti.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="6e8ce-108">Il campo del costo standard nel catalogo dei prodotti viene impostato nella valuta di base dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="6e8ce-109">Il costo unitario predefinito nella riga dell'offerta basata sul prodotto viene convertito nella valuta di vendita dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="6e8ce-110">Costo unitario su una riga dell'offerta basata sul prodotto</span><span class="sxs-lookup"><span data-stu-id="6e8ce-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="6e8ce-111">Lo scopo di avere un costo unitario su una riga di offerta basata sul prodotto è quello di consentire costi diversi per un prodotto per ciascuna vendita.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="6e8ce-112">Questo non è uno scenario tipico, ma a volte il costo del prodotto può essere scontato dal fornitore a seconda del cliente della vendita finale.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="6e8ce-113">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6e8ce-113">For example:</span></span>

<span data-ttu-id="6e8ce-114">Fabrikam Robotics sta installando bracci robotici presso le linee di assemblaggio di A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="6e8ce-115">Fabrikam fornisce servizi di installazione, ma i bracci robotici vengono acquistati da Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="6e8ce-116">Se l'installazione di bracci robotici presso A Datum Corporation apre un nuovo settore verticale per i bracci robotici di Trey, Trey potrebbe concedere uno sconto speciale per questo accordo a Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="6e8ce-117">In questo caso, Fabrikam creerà una riga di offerta basata sul prodotto per Bracci robotici e inserirà un costo unitario speciale per questa offerta.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="6e8ce-118">Questo costo è diverso dal costo standard di Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="6e8ce-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
