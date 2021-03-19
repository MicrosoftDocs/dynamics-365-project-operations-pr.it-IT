---
title: Spese interaziendali
description: Questo argomento fornisce informazioni su come utilizzare le spese interaziendali per assegnare le spese di un lavoratore alla persona giuridica per la quale è stato eseguito il lavoro.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271538"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="a4eaf-103">Spese interaziendali</span><span class="sxs-lookup"><span data-stu-id="a4eaf-103">Intercompany expenses</span></span>

<span data-ttu-id="a4eaf-104">Un lavoratore dipendente di una persona giuridica in un'organizzazione potrebbe svolgere il lavoro per un'altra persona giuridica nella stessa organizzazione.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="a4eaf-105">Puoi utilizzare le spese interaziendali per assegnare le spese di un lavoratore alla persona giuridica per la quale è stato eseguito il lavoro.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="a4eaf-106">La persona giuridica che impiega il lavoratore è chiamata persona giuridica che presta la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="a4eaf-107">La persona giuridica per la quale il lavoratore sostiene le spese è denominata persona giuridica che prende in prestito la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="a4eaf-108">Prima che un lavoratore possa creare e inviare le spese interaziendali, è necessario abilitare le righe spese interaziendali.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="a4eaf-109">Nella persona giuridica, nella pagina **Parametri di gestione spese** seleziona **Consenti righe spesa interaziendale**.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="a4eaf-110">Registrazione delle imposte per spese interaziendali</span><span class="sxs-lookup"><span data-stu-id="a4eaf-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4eaf-111">Prima di poter utilizzare le fasce IVA associate alla persona giuridica concedente (origine) anziché alla persona giuridica richiedente (destinazione) nella nota spese, devi abilitare la funzionalità nell'impostazione IVA di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="a4eaf-112">Quando il parametro **Persona giuridica per registrazione imposte interaziendali** è impostato su **Origine** e **Applica regole di tassazione vendite** è impostato su **No**, viene utilizzata la combinazione fiscale per la persona giuridica concedente.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="a4eaf-113">Quando lo stesso parametro è impostato su **Destinazione**, verrà utilizzata la combinazione fiscale per la persona giuridica che prende in prestito la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="a4eaf-114">Per le persone giuridiche negli Stati Uniti, quando il parametro è impostato su **Origine**, il campo **Contabilità IVA** deve essere configurato anche nella nuova pagina **Gruppi di registrazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="a4eaf-115">Il motore di contabilità utilizzerà le informazioni di questo campo per la registrazione contabile relativa alle imposte.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="a4eaf-116">Il comportamento è coerente per le righe di spesa registrate con o senza un progetto.</span><span class="sxs-lookup"><span data-stu-id="a4eaf-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]