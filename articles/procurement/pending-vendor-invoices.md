---
title: Acquistare materiali non stoccati con una fattura fornitore in sospeso
description: Questo argomento spiega come registrare le fatture fornitore in sospeso.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993803"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="1f123-103">Acquistare materiali non stoccati con una fattura fornitore in sospeso</span><span class="sxs-lookup"><span data-stu-id="1f123-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="1f123-104">_**Si applica a:** Project Operations per scenari basati su risorse/materiali non stoccati_</span><span class="sxs-lookup"><span data-stu-id="1f123-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1f123-105">Poiché un'azienda acquista materiali non stoccati per un progetto, i costi possono essere immediatamente registrati a fronte del progetto.</span><span class="sxs-lookup"><span data-stu-id="1f123-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="1f123-106">Per esempio, Contoso Robotics US sta eseguendo un progetto di rinnovo delle apparecchiature e necessita di licenze software.</span><span class="sxs-lookup"><span data-stu-id="1f123-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="1f123-107">Queste licenze vengono acquistate da un fornitore di terze parti.</span><span class="sxs-lookup"><span data-stu-id="1f123-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="1f123-108">Utilizzando Dynamics 365 Finance, l'addetto alla contabilità fornitori registra un documento di fattura fornitore in sospeso e attribuisce i costi della licenza direttamente al progetto di rinnovo dell'attrezzatura.</span><span class="sxs-lookup"><span data-stu-id="1f123-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="1f123-109">Prima di utilizzare la funzionalità descritta in questo argomento, esamina e applica le configurazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="1f123-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="1f123-110">Per ulteriori informazioni, vedi [Abilitare materiali non stoccati e fatture fornitore in sospeso](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="1f123-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="1f123-111">Registrare una fattura fornitore in sospeso relativa al progetto</span><span class="sxs-lookup"><span data-stu-id="1f123-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="1f123-112">Le fatture fornitore in sospeso possono essere registrate nella pagina **Fatture fornitore in sospeso** (**Contabilità fornitori** > **Fatture** > **Fatture fornitore in sospeso**).</span><span class="sxs-lookup"><span data-stu-id="1f123-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="1f123-113">Completa i seguenti passaggi per registrare una fattura fornitore in sospeso relativa al progetto:</span><span class="sxs-lookup"><span data-stu-id="1f123-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="1f123-114">Vai a **Contabilità fornitori** > **Fatture** e seleziona **Nuovo**.</span><span class="sxs-lookup"><span data-stu-id="1f123-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="1f123-115">Nel campo **Conto fattura** seleziona un fornitore e nel campo **Numero**, immetti l'identificazione della fattura del fornitore.</span><span class="sxs-lookup"><span data-stu-id="1f123-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="1f123-116">Aggiungi una riga alla fattura fornitore e nel campo **Codice articolo** seleziona l'articolo non stoccato acquistato dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="1f123-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1f123-117">Le righe della fattura fornitore basate su una categoria di approvvigionamento non possono essere registrate nel progetto.</span><span class="sxs-lookup"><span data-stu-id="1f123-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="1f123-118">Aggiungi la quantità acquistata.</span><span class="sxs-lookup"><span data-stu-id="1f123-118">Add the quantity purchased.</span></span> <span data-ttu-id="1f123-119">Il sistema popolerà il prezzo unitario in base alla configurazione del prezzo dell'articolo non stoccato.</span><span class="sxs-lookup"><span data-stu-id="1f123-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="1f123-120">Verifica l'importo totale e altri dettagli richiesti sulla riga.</span><span class="sxs-lookup"><span data-stu-id="1f123-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="1f123-121">Nei dettagli della linea, nella scheda **Progetto** seleziona l'ID del progetto in cui verrà registrato l'elemento.</span><span class="sxs-lookup"><span data-stu-id="1f123-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="1f123-122">Facoltativamente, seleziona il numero dell'attività e aggiorna la categoria del progetto e la proprietà della riga.</span><span class="sxs-lookup"><span data-stu-id="1f123-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="1f123-123">Registra la fattura fornitore in sospeso.</span><span class="sxs-lookup"><span data-stu-id="1f123-123">Post pending vendor invoice.</span></span> <span data-ttu-id="1f123-124">Quando la fattura viene registrata, il sistema registra:</span><span class="sxs-lookup"><span data-stu-id="1f123-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="1f123-125">L'importo del saldo del fornitore.</span><span class="sxs-lookup"><span data-stu-id="1f123-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="1f123-126">L'importo dell'IVA.</span><span class="sxs-lookup"><span data-stu-id="1f123-126">The sales tax amount.</span></span>
    - <span data-ttu-id="1f123-127">Il costo relativo al progetto viene registrato nel conto di integrazione dell'approvvigionamento.</span><span class="sxs-lookup"><span data-stu-id="1f123-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="1f123-128">La transazione effettiva del progetto in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1f123-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="1f123-129">Questa transazione viene ulteriormente elaborata utilizzando il [giornale di integrazione Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="1f123-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="1f123-130">La registrazione di questo giornale di registrazione sposta l'importo dal conto di integrazione dell'approvvigionamento al conto dei costi del progetto.</span><span class="sxs-lookup"><span data-stu-id="1f123-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
