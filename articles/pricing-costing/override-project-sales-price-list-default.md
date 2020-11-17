---
title: Sostituire i listini prezzi di vendita di progetto
description: Questo argomento fornisce informazioni sulla creazione di listini prezzi di vendita personalizzati.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130853"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="38c3d-103">Sostituire i listini prezzi di vendita di progetto</span><span class="sxs-lookup"><span data-stu-id="38c3d-103">Override project sales price lists</span></span>

<span data-ttu-id="38c3d-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati, Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="38c3d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="38c3d-105">Listini prezzi di progetto specifici per il cliente</span><span class="sxs-lookup"><span data-stu-id="38c3d-105">Customer-specific project price lists</span></span>

<span data-ttu-id="38c3d-106">Gli accordi sui prezzi specifici del cliente possono essere impostati come listini prezzi di progetto in un record di conto in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="38c3d-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="38c3d-107">Per impostare un listino prezzi di progetto specifico per il cliente, nell'area **Vendite** vai al record del conto.</span><span class="sxs-lookup"><span data-stu-id="38c3d-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="38c3d-108">Apri la pagina elenco **Conti**.</span><span class="sxs-lookup"><span data-stu-id="38c3d-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="38c3d-109">Individua e fai doppio clic su un record cliente per aprire la pagina dei dettagli del **conto**.</span><span class="sxs-lookup"><span data-stu-id="38c3d-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="38c3d-110">Nella scheda **Listini prezzi di progetto** seleziona \*\*+ Nuovo listino prezzi di progetto^^.</span><span class="sxs-lookup"><span data-stu-id="38c3d-110">On the **Project Price lists** tab, select \*\*+ New Project Price List^^.</span></span>
4. <span data-ttu-id="38c3d-111">Nella pagina **Nuovo listino prezzi di progetto** seleziona un listino prezzi dal menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="38c3d-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="38c3d-112">Solo i listini prezzi che hanno il contesto impostato su **Vendite** e la cui valuta corrisponde alla valuta del conto sono inclusi.</span><span class="sxs-lookup"><span data-stu-id="38c3d-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="38c3d-113">Immetti un nome per l'associazione e seleziona **Salva**.</span><span class="sxs-lookup"><span data-stu-id="38c3d-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="38c3d-114">Il listino prezzi di progetto specifico per il cliente è stato creato.</span><span class="sxs-lookup"><span data-stu-id="38c3d-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="38c3d-115">Questo listino prezzi verrà utilizzato per i prezzi di progetto predefiniti sulle offerte di progetto o sui contratti creati per questo cliente in cui la data di creazione dell'offerta o del contratto di progetto rientra nella data di validità del listino prezzi.</span><span class="sxs-lookup"><span data-stu-id="38c3d-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="38c3d-116">Prezzi personalizzati in offerte di progetto</span><span class="sxs-lookup"><span data-stu-id="38c3d-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="38c3d-117">Nelle offerte di progetto, è possibile avere prezzi di progetto che iniziano con un listino prezzi standard predefinito che viene impostato dal cliente o dai parametri del progetto.</span><span class="sxs-lookup"><span data-stu-id="38c3d-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="38c3d-118">Quando è necessario un prezzo personalizzato per il lavoro relativo al progetto su una particolare offerta, è possibile ottenerlo dall'entità associata ai listini prezzi di progetto.</span><span class="sxs-lookup"><span data-stu-id="38c3d-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="38c3d-119">Completa i seguenti passaggi per impostare il prezzo del progetto specifico dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="38c3d-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="38c3d-120">Apri l'offerta di progetto e seleziona la scheda **Listini prezzi di progetto**.</span><span class="sxs-lookup"><span data-stu-id="38c3d-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="38c3d-121">Nella griglia secondaria seleziona **Crea determinazione dei prezzi personalizzata**.</span><span class="sxs-lookup"><span data-stu-id="38c3d-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="38c3d-122">Tutti i listini prezzi di progetto allegati all'offerta vengono copiati in nuovi listini prezzi.</span><span class="sxs-lookup"><span data-stu-id="38c3d-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="38c3d-123">I nomi dei nuovi listini prezzi riflettono il nome dell'offerta con il timbro data-ora della creazione di questi listini prezzi.</span><span class="sxs-lookup"><span data-stu-id="38c3d-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="38c3d-124">Puoi utilizzare ciascuno di questi listini prezzi e aggiornare i prezzi di manodopera (prezzo del ruolo) e di spesa (prezzo della categoria).</span><span class="sxs-lookup"><span data-stu-id="38c3d-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="38c3d-125">Questi prezzi saranno applicabili solo a questa offerta di progetto.</span><span class="sxs-lookup"><span data-stu-id="38c3d-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="38c3d-126">Listini prezzi in un contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="38c3d-126">Price lists on a project contract</span></span>

<span data-ttu-id="38c3d-127">In un contratto di progetto, il prezzo del progetto è sempre predefinito come un listino prezzi personalizzato con il nome del contratto e il timestamp della data di creazione aggiunto al nome.</span><span class="sxs-lookup"><span data-stu-id="38c3d-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="38c3d-128">Questo è vero se il contratto è stato creato quando l'offerta è stata acquisita o se il contratto è stato creato da zero.</span><span class="sxs-lookup"><span data-stu-id="38c3d-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="38c3d-129">Se necessario, è possibile rimuovere questa associazione al listino prezzi personalizzato e associare un listino prezzi standard al contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="38c3d-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="38c3d-130">Quando associ un listino prezzi standard ai listini prezzi di progetto su offerta o contratto, eventuali modifiche apportate ai prezzi nel listino prezzi avranno effetto su tutte le offerte e i contratti che utilizzano il listino prezzi.</span><span class="sxs-lookup"><span data-stu-id="38c3d-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
