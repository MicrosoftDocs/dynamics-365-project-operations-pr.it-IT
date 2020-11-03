---
title: Spese interaziendali
description: Un lavoratore dipendente di una persona giuridica in un'organizzazione potrebbe svolgere il lavoro per un'altra persona giuridica nella stessa organizzazione. In questa situazione puoi utilizzare la funzione Spese interaziendali per attribuire le spese del lavoratore alla persona giuridica per la quale ha eseguito il lavoro.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4079027"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="57140-104">Spese interaziendali</span><span class="sxs-lookup"><span data-stu-id="57140-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57140-105">Un lavoratore dipendente di una persona giuridica in un'organizzazione potrebbe svolgere il lavoro per un'altra persona giuridica nella stessa organizzazione.</span><span class="sxs-lookup"><span data-stu-id="57140-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="57140-106">In questa situazione puoi utilizzare la funzione Spese interaziendali per attribuire le spese del lavoratore alla persona giuridica per la quale ha eseguito il lavoro.</span><span class="sxs-lookup"><span data-stu-id="57140-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="57140-107">La persona giuridica che impiega il lavoratore è chiamata persona giuridica che presta la risorsa.</span><span class="sxs-lookup"><span data-stu-id="57140-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="57140-108">La persona giuridica per la quale il lavoratore sostiene le spese è denominata persona giuridica che prende in prestito la risorsa.</span><span class="sxs-lookup"><span data-stu-id="57140-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="57140-109">Prima che un lavoratore possa creare e inviare le spese per il lavoro svolto per una persona giuridica diversa, nella persona giuridica che presta la risorsa, nella pagina **Parametri di gestione spese** seleziona l'opzione **Consenti righe spese interaziendali**.</span><span class="sxs-lookup"><span data-stu-id="57140-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="57140-110">Registrazione delle imposte per spese interaziendali</span><span class="sxs-lookup"><span data-stu-id="57140-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57140-111">Se vuoi utilizzare i gruppi di imposte associati alla persona giuridica che presta la risorsa (origine) invece della persona giuridica che prende in prestito la risorsa (destinazione) nella tua nota spese, è necessario configurarla nell'impostazione IVA di contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="57140-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="57140-112">Quando il parametro di contabilità generale **Persona giuridica per registrazione imposte interaziendali** è impostato su **Origine** e **Applica regole tassazione IVA** è impostato su **No** , verrà utilizzata la combinazione fiscale della persona giuridica che presta la risorsa.</span><span class="sxs-lookup"><span data-stu-id="57140-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="57140-113">Quando lo stesso parametro è impostato su **Destinazione** , verrà utilizzata la combinazione fiscale per la persona giuridica che prende in prestito la risorsa.</span><span class="sxs-lookup"><span data-stu-id="57140-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="57140-114">Per le persone giuridiche negli Stati Uniti, quando il parametro è impostato su **Origine** , il campo **Contabilità IVA** deve essere configurato anche nella nuova pagina **Gruppi di registrazione contabile**.</span><span class="sxs-lookup"><span data-stu-id="57140-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="57140-115">Il motore di contabilità utilizzerà le informazioni di questo campo per la registrazione contabile relativa alle imposte.</span><span class="sxs-lookup"><span data-stu-id="57140-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="57140-116">Il comportamento è coerente per le righe di spesa registrate con o senza un progetto.</span><span class="sxs-lookup"><span data-stu-id="57140-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
