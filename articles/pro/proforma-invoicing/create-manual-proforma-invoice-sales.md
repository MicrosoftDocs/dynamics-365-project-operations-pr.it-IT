---
title: Creare una fattura proforma manuale - semplice
description: Questo argomento fornisce informazioni sulla creazione manuale di una fattura proforma in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764508"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="4d7c9-103">Creare una fattura proforma manuale - semplice</span><span class="sxs-lookup"><span data-stu-id="4d7c9-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="4d7c9-104">_**Si applica a:** Distribuzione semplice: dalla transazione alla fatturazione proforma_</span><span class="sxs-lookup"><span data-stu-id="4d7c9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4d7c9-105">In Dynamics 365 Project Operations, le fatture proforma possono essere create manualmente secondo necessità.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="4d7c9-106">Puoi creare manualmente una fattura proforma dalla pagina elenco **Contratti di progetto** o dalla pagina dei dettagli **Contratto di progetto**.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="4d7c9-107">Pagina elenco Contratti di progetto</span><span class="sxs-lookup"><span data-stu-id="4d7c9-107">Project Contracts list page</span></span>

<span data-ttu-id="4d7c9-108">Dalla pagina elenco **Contratti di progetto** seleziona uno o più contratti di progetto e crea le fatture per tutti i record selezionati.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="4d7c9-109">Il sistema verifica quale dei contratti di progetto selezionati ha un backlog **Pronto per la fatturazione** datato prima della data odierna.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="4d7c9-110">Da questi contratti, il sistema crea bozze di fatture proforma.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="4d7c9-111">Se un contratto di progetto ha più clienti, potrebbe esserci una fattura creata per cliente e più fatture per contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="4d7c9-112">Tutte le fatture del progetto create sono disponibili nella pagina **Fattura** nella sezione **Fatturazione** dell'area **Vendite**.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="4d7c9-113">Pagina dei dettagli Contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="4d7c9-113">Project Contract details page</span></span>

<span data-ttu-id="4d7c9-114">Puoi creare una fattura proforma anche dalla pagina dei dettagli **Contratto di progetto**.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="4d7c9-115">Il sistema verifica che il contratto di progetto abbia un backlog **Pronto per la fatturazione** datato prima della data odierna.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="4d7c9-116">Da questi contratti, il sistema crea bozze di fatture proforma in base al numero di clienti su ciascuna voce di contratto.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="4d7c9-117">Quando viene creata una singola fattura proforma, viene visualizzata la pagina **Fattura**.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="4d7c9-118">Se vengono create più fatture per quel contratto di progetto, viene visualizzata la pagina di elenco **Fatture** per mostrare tutte le fatture create.</span><span class="sxs-lookup"><span data-stu-id="4d7c9-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
