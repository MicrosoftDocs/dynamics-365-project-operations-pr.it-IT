---
title: Panoramica della fatturazione interaziendale
description: Questo argomento fornisce informazioni ed esempi sulla fatturazione interaziendale per i progetti.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002646"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="96aa5-103">Panoramica della fatturazione interaziendale</span><span class="sxs-lookup"><span data-stu-id="96aa5-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="96aa5-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="96aa5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="96aa5-105">La tua organizzazione potrebbe avere più divisioni, filiali e altre persone giuridiche che trasferiscono prodotti e servizi tra loro per i progetti.</span><span class="sxs-lookup"><span data-stu-id="96aa5-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="96aa5-106">L'entità giuridica che fornisce il servizio o il prodotto è denominata *persona giuridica che effettua la concessione*.</span><span class="sxs-lookup"><span data-stu-id="96aa5-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="96aa5-107">L'entità giuridica che riceve il servizio o il prodotto è denominata *persona giuridica richiedente*.</span><span class="sxs-lookup"><span data-stu-id="96aa5-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="96aa5-108">L'illustrazione seguente mostra uno scenario tipico in cui due persone giuridiche, Contoso Robotics USA (la persona giuridica mutuataria) e Contoso Robotics UK (la persona giuridica che concede il prestito) condivide le risorse per consegnare un progetto al cliente, Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="96aa5-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="96aa5-109">Per questo scenario, Contoso Robotics USA è incaricata di consegnare il lavoro ad Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="96aa5-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Fatturazione interaziendale](./media/IntercompanyScenario.png) 

<span data-ttu-id="96aa5-111">Dynamics 365 Project Operations utilizza il flusso seguente per elaborare le transazioni interaziendali:</span><span class="sxs-lookup"><span data-stu-id="96aa5-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="96aa5-112">Le risorse della persona giuridica che effettua la concessione registrano le transazioni di tempo o di spesa interaziendali registrando tempi e costi a fronte dei progetti della persona giuridica richiedente.</span><span class="sxs-lookup"><span data-stu-id="96aa5-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="96aa5-113">I costi e tempi sono registrati nella società richiedente utilizzando il listino prezzi unitario di costo della società richiedente.</span><span class="sxs-lookup"><span data-stu-id="96aa5-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="96aa5-114">Le transazioni di vendita non fatturate interaziendali sono registrate nella società richiedente utilizzando il listino prezzi unitario di costo della società richiedente.</span><span class="sxs-lookup"><span data-stu-id="96aa5-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="96aa5-115">I ricavi non fatturati vengono registrati nella società richiedente utilizzando il listino prezzi di vendita del contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="96aa5-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="96aa5-116">Il cliente può essere fatturato quando vengono registrati i ricavi non fatturati.</span><span class="sxs-lookup"><span data-stu-id="96aa5-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="96aa5-117">Il cliente non deve attendere il completamento dell'elaborazione della fattura interaziendale.</span><span class="sxs-lookup"><span data-stu-id="96aa5-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="96aa5-118">Le fatture dei clienti interaziendali vengono create periodicamente nella società che effettua la concessione.</span><span class="sxs-lookup"><span data-stu-id="96aa5-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="96aa5-119">Le fatture vengono create manualmente o utilizzando un processo periodico automatizzato.</span><span class="sxs-lookup"><span data-stu-id="96aa5-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="96aa5-120">È possibile creare un'unica fattura per ciascuna persona giuridica debitrice oppure è possibile creare fatture separate per progetto.</span><span class="sxs-lookup"><span data-stu-id="96aa5-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="96aa5-121">Quando viene registrata una fattura cliente interaziendali nella persona giuridica che effettua la concessione, la fattura fornitore in sospeso corrispondente viene creata nella persona giuridica richiedente.</span><span class="sxs-lookup"><span data-stu-id="96aa5-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="96aa5-122">I costi nella fattura fornitore in sospeso verranno registrati nel registro secondario del progetto quando la fattura viene registrata.</span><span class="sxs-lookup"><span data-stu-id="96aa5-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="96aa5-123">Il diagramma seguente illustra la fatturazione interaziendale in quanto si riferisce a eventi contabili e registrazioni previste nella contabilità generale.</span><span class="sxs-lookup"><span data-stu-id="96aa5-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Flusso interaziendale](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="96aa5-125">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="96aa5-125">Additional resources</span></span>

- [<span data-ttu-id="96aa5-126">Configurare la fatturazione interaziendale</span><span class="sxs-lookup"><span data-stu-id="96aa5-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="96aa5-127">Registrare transazioni interaziendali</span><span class="sxs-lookup"><span data-stu-id="96aa5-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="96aa5-128">Creare fatture interaziendali per clienti e fornitori</span><span class="sxs-lookup"><span data-stu-id="96aa5-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]