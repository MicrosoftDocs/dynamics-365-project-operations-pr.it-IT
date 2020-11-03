---
title: Creazione di una fattura proforma manuale
description: Questo argomento fornisce informazioni sulla creazione manuale di una fattura proforma in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4079105"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="32193-103">Creazione di una fattura proforma manuale</span><span class="sxs-lookup"><span data-stu-id="32193-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="32193-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="32193-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="32193-105">In Dynamics 365 Project Operations, le fatture proforma possono essere create manualmente secondo necessità.</span><span class="sxs-lookup"><span data-stu-id="32193-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="32193-106">Puoi creare manualmente una fattura proforma dalla pagina elenco **Contratti di progetto** o dalla pagina dei dettagli **Contratto di progetto**.</span><span class="sxs-lookup"><span data-stu-id="32193-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="32193-107">Pagina elenco Contratti di progetto</span><span class="sxs-lookup"><span data-stu-id="32193-107">Project Contracts list page</span></span>

<span data-ttu-id="32193-108">Dalla pagina elenco **Contratti di progetto** seleziona uno o più contratti di progetto e crea le fatture per tutti i record selezionati.</span><span class="sxs-lookup"><span data-stu-id="32193-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="32193-109">Il sistema verifica quale dei contratti di progetto selezionati ha un backlog **Pronto per la fatturazione** datato prima della data odierna.</span><span class="sxs-lookup"><span data-stu-id="32193-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="32193-110">Da questi contratti, il sistema crea bozze di fatture proforma.</span><span class="sxs-lookup"><span data-stu-id="32193-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="32193-111">Se un contratto di progetto ha più clienti, potrebbe esserci una fattura creata per cliente e più fatture per contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="32193-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="32193-112">Tutte le fatture del progetto create sono disponibili nella pagina **Fattura** nella sezione **Fatturazione** dell'area **Vendite**.</span><span class="sxs-lookup"><span data-stu-id="32193-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="32193-113">Pagina dei dettagli Contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="32193-113">Project Contract details page</span></span>

<span data-ttu-id="32193-114">È anche possibile creare una fattura proforma dalla pagina dei dettagli **Contratto di progetto** che crea la fattura per lo specifico contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="32193-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="32193-115">Il sistema verifica che il contratto di progetto abbia un backlog **Pronto per la fatturazione** datato prima della data odierna.</span><span class="sxs-lookup"><span data-stu-id="32193-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="32193-116">Da questi contratti, il sistema crea bozze di fatture proforma in base al numero di clienti su ciascuna voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="32193-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="32193-117">Quando viene creata una singola fattura proforma, viene visualizzata la pagina **Fattura**.</span><span class="sxs-lookup"><span data-stu-id="32193-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="32193-118">Se sono presenti più fatture create per quel contratto di progetto, la pagina elenco **Fatture** si apre per mostrare tutte le fatture create.</span><span class="sxs-lookup"><span data-stu-id="32193-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
